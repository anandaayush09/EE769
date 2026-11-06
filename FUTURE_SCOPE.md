# Future Scope & Improvements

## 1. Known issues
| Where | Issue | Fix |
|-------|-------|-----|
| All notebooks | Written for Colab; only the data paths were adapted, nothing was re-run after the move | Run each notebook top to bottom in a fresh environment and refresh the stored outputs |
| `A1/eda.ipynb` | ~10 MB because of embedded interactive Altair charts (~3 MB each); GitHub won't render them | Save static PNG versions or strip outputs (`nbstripout`) and publish a rendered HTML copy |
| `A2/linear_models.ipynb` | Data is random with no fixed seed, so results differ per run | Set `np.random.seed(...)` / use `default_rng(seed)` |
| `A2/linear_models.ipynb` | Question 14 appears before Question 13 | Reorder the cells |
| `A2/linear_models.ipynb` | The cell defining `generate_data_and_calculate_nrmse` starts with a stray space, which raises `IndentationError` on a current IPython (it ran on the older Colab kernel) | Delete the leading space on the first line of that cell |
| `A3/…ipynb` | Mixes scikit-learn, PyTorch and TensorFlow in one notebook; permutation importance uses only `n_repeats=2` | Split into two notebooks (tabular / transfer learning); use ≥10 repeats |
| `A3/…ipynb` | Model weights saved to a temp directory and discarded | Save the best checkpoint to `models/` (gitignored) so results can be reloaded |
| `A3`, `A4` | Colab mount cell kept inside a try/except; Colab users must upload data manually | Add a small `download_data.py` that fetches the datasets |

## 2. Per-assignment extensions
- **A1:** a reusable cleaning module (type fixing, imputation report); join the inspection data with geographic/neighbourhood data for spatial maps; automated data-quality report (e.g. `ydata-profiling`).
- **A2:** add elastic net, momentum/Adam optimisers and a closed-form solution to compare against gradient descent; cross-validated choice of regularisation; bias–variance study over sample size; polynomial features.
- **A3:** handle class imbalance (class weights, SMOTE); calibrated probabilities and threshold tuning; gradient boosting (XGBoost/LightGBM) baseline; SHAP explanations; try fine-tuning vs feature-extraction for ResNet and report data-augmentation ablations.
- **A4:** Gaussian mixture and hierarchical clustering; stability analysis across seeds; cluster profiling with business-style personas; evaluate with multiple internal indices (Davies-Bouldin, Calinski-Harabasz).

## 3. Repository-wide
- **Reproducibility:** pin versions in `requirements.txt` (or `pyproject.toml`), fix random seeds, record the Python version.
- **Structure:** extract shared helpers (loading, plotting, metrics) into a `src/` package; keep notebooks thin.
- **Tests & CI:** smoke-test notebooks with `nbmake`/`papermill` on small samples via GitHub Actions; lint with `ruff`.
- **Data management:** `download_data.py` for the image datasets, or Git LFS for the larger CSVs; document data licences and sources.
- **Docs:** add a LICENSE, embed key result figures in each README, and add a short results summary table per assignment.
