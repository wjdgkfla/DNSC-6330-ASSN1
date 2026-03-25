# Assignment 1 - Translating the R COMPAS Workflow into Python

## Overview
This repository contains the Python translation of the Lecture 01 R workflow.

Notebook:
- `Lecture-01-alignment-python.ipynb`

The notebook reproduces the Lecture 01 analytical pipeline:
1. Data loading from the COMPAS source dataset.
2. Data cleaning and filtering consistent with the R notebook.
3. Feature engineering and factor/reference handling.
4. Exploratory data analysis (summary statistics and visualizations).
5. Logistic regression model development.
6. Model diagnostics and fairness-related evaluation metrics.

## Libraries Used
- `pandas`
- `numpy`
- `matplotlib`
- `statsmodels`
- `scikit-learn`

## Reproducibility Instructions
1. Create/activate a Python 3.11+ environment.
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib statsmodels scikit-learn
   ```
3. Open and run all cells in:
   - `Lecture-01-alignment-python.ipynb`

## Expected Outputs
- EDA summaries for demographics and score distributions.
- Logistic regression summary table.
- Overall confusion matrix and metrics.
- Race-level fairness metrics (including FPR/FNR disparities).

## Notes
- Minor numerical differences versus R may occur because optimization and default settings differ slightly across libraries.
