# COMPAS Recidivism — Python ML Workflow (DNSC 6330, Assignment 1)

Reproduced an R-based COMPAS recidivism analysis end-to-end in Python, covering EDA, logistic regression, confusion matrix diagnostics, and racial fairness metrics.

**Skills:** Python · pandas · NumPy · Matplotlib · statsmodels · scikit-learn · Fairness Analysis

---

## What This Project Demonstrates

- Translating a full ML pipeline from R to Python while preserving analytical integrity
- Exploratory data analysis: distributions, crosstabs, demographic breakdowns
- Logistic regression with explicit feature formulas and reference category control
- Group-conditional error rates (FPR/FNR) across racial subgroups
- Fairness disparity reporting: delta FPR/FNR relative to Caucasian baseline

---

## Dataset

ProPublica COMPAS Recidivism — Broward County, FL (2016)
Filtered cohort: ~6,170 defendants · Target: `two_year_recid`

---

## Notebook

`Assignment 1.ipynb` — runs top-to-bottom and reproduces all outputs

**Section breakdown:**
1. Load & filter COMPAS dataset
2. Data cleaning and feature engineering
3. EDA: demographics, decile score distributions by race
4. Logistic regression model
5. Overall confusion matrix metrics (accuracy, precision, recall, FPR, FNR)
6. Race-level confusion matrices and group error rates
7. Disparity table relative to Caucasian baseline
8. Companion `decile_score >= 7` rule check
9. Interpretation and responsible ML discussion

---

## Setup

```bash
pip install pandas numpy matplotlib statsmodels scikit-learn
jupyter notebook "Assignment 1.ipynb"
```
