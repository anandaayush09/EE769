# A1 — Exploratory & descriptive data analysis

Notebook: `eda.ipynb`

## Problem 1 — Los Angeles open data
Two datasets from the City of Los Angeles: the **LAHD affordable housing projects list (2003–present)** and **restaurant and market health inspections**. For each:
1. Check and fix data types (e.g. funding and in-service dates → datetime).
2. Handle missing values: drop rows where the share is tiny, impute otherwise, leave sparse single columns alone.
3. Find unexpected entries (empty strings in `grade`, an odd service code of 401) and correct them.
4. Query the tables with SQL (in-memory SQLite via SQLAlchemy), including a merged result, and plot distributions and relationships.

## Problem 2 — State-level Consumer Price Index
Analysis of the All-India CPI (rural/urban) index file from data.gov.in.

## Data (`data/`)
- `LAHD_Affordable_Housing_Projects_List__2003_to_Present_.csv`
- `Restaurant_and_Market_Health_Inspections.csv` (16.6 MB)
- `All_India_Index_july2019_20Aug2020_dec20_1_5.csv`

## Run
```bash
jupyter notebook eda.ipynb
```
Launch from this folder. Stored outputs include interactive Altair charts, which is why the file is ~10 MB; GitHub may not render them (open locally or in nbviewer).
