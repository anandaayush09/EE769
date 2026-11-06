# A2 — Linear models, regularisation & logistic regression from scratch

Notebook: `linear_models.ipynb`

Linear regression with L1/L2 regularisation (lasso/ridge) and a logistic-regression classifier, built with only basic NumPy linear algebra and Matplotlib plotting, then checked against library implementations.

## Contents
- A generator for correlated input matrices: standard-normal columns multiplied by a generator matrix `S` (identity → independent features, otherwise correlated).
- Synthetic regression targets with controllable noise.
- Mean-squared-error gradient, L1/L2 penalty terms and a regularised gradient-descent solver; normalised RMSE as the error metric; effect of regularisation strength; comparison with scikit-learn and statsmodels, with timing.
- Sigmoid-based logistic regression on generated linearly separable binary data.
- 14 numbered questions, each followed by observations.

## Data
None required — all data is simulated inside the notebook (set a random seed for exact reproducibility; see `FUTURE_SCOPE.md`).

## Run
```bash
jupyter notebook linear_models.ipynb
```
