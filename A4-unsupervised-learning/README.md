# A4 — Unsupervised learning (customer segmentation)

Notebook: `clustering.ipynb`

Segment customers in `data/Customer-Data - 2.csv` using clustering.

## Pipeline
1. Visualise and summarise the data.
2. Reduce skew with log / power / exponential transformations (Q1a).
3. Drop highly correlated or unsuitable variables (Q1b).
4. Dimensionality reduction (PCA, t-SNE) for visualisation.
5. Cluster with K-Means and DBSCAN; choose parameters with silhouette analysis; interpret the clusters.

## Run
```bash
jupyter notebook clustering.ipynb
```
Launch from this folder. A walkthrough-video link is at the top of the notebook.
