# EE 769 — Introduction to Data Science & Machine Learning

Coursework for **EE 353/769 (Jul–Nov 2024), IIT Bombay**. Four graded programming assignments, each a self-contained Jupyter notebook with analysis, observations and references.

| # | Folder | Topic | Methods | Data |
|---|--------|-------|---------|------|
| A1 | [`A1-exploratory-data-analysis`](A1-exploratory-data-analysis) | Exploratory & descriptive analysis | Type fixes, missing/unexpected values, SQL queries (in-memory SQLite) incl. a merged table, Altair/seaborn plots, state-level CPI analysis | LA housing projects, LA restaurant inspections, All-India CPI |
| A2 | [`A2-linear-models-from-scratch`](A2-linear-models-from-scratch) | Linear models, regularisation & logistic regression | Gradient-descent linear regression with L1/L2 regularisation (lasso/ridge) and logistic regression, implemented with NumPy; checked against scikit-learn / statsmodels | Synthetic data generated in the notebook |
| A3 | [`A3-classification-transfer-learning`](A3-classification-transfer-learning) | Classification & feature engineering; transfer learning | EDA, outlier removal, one-hot encoding, grid-search CV over Random Forest / SVM / MLP, feature importance; ResNet-18 fine-tuning (ants vs bees), MobileNetV2 on Fashion-MNIST | Bank marketing (UCI), hymenoptera, CIFAR-10 |
| A4 | [`A4-unsupervised-learning`](A4-unsupervised-learning) | Unsupervised learning | Skew reduction, correlation pruning, PCA, t-SNE, K-Means, DBSCAN, silhouette analysis | Customer segmentation data |

## Repository layout
```
A1-… to A4-…     one folder per assignment: README.md, notebook, data/
requirements.txt Python dependencies
FUTURE_SCOPE.md  known issues, improvements and further work
```

## Setup
```bash
python -m venv .venv
.venv\Scripts\activate          # Windows (source .venv/bin/activate on macOS/Linux)
pip install -r requirements.txt
```
Launch each notebook from inside its own folder so the relative `data/` path resolves:
```bash
cd A4-unsupervised-learning
jupyter notebook clustering.ipynb
```
The notebooks were written in Google Colab. On Colab the Drive-mount cell still works, but the `data/` paths then refer to files you upload next to the notebook.

## Data notes
- CSV datasets for A1, A3 (`bank.csv`) and A4 are included.
- A3's image datasets are not tracked (large): download the *hymenoptera* ants/bees set into `A3-…/data/hymenoptera_data/{train,val}` — CIFAR-10 and Fashion-MNIST download automatically on first run.
- Lecture slides, assignment handouts, the course textbook and reference papers are instructor or publisher material and are intentionally not part of this repository.

See [`FUTURE_SCOPE.md`](FUTURE_SCOPE.md) for improvements and next steps.
