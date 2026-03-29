# Assignment 1 - Translating an R Machine Learning Workflow into Python (COMPAS)

## Purpose of the Analysis
This repository reproduces the Lecture 01 COMPAS analysis by translating the original R notebook workflow into Python. The goal is to preserve all substantive analytical steps: EDA, preprocessing, model development, diagnostics, and interpretation.

Notebook included:
- `Assignment 1.ipynb`

Reference notebook translated:
- `Lecture-01-alignment.ipynb` (R)

## Libraries Used
- `pandas`
- `numpy`
- `matplotlib`
- `statsmodels`
- `scikit-learn`

## How This Notebook Matches the Assignment Rubric
### 1) Replicate EDA
- Loads the same COMPAS dataset used in lecture.
- Applies equivalent filtering and cleaning logic.
- Recreates variable transformations/factor handling used in R.
- Reproduces descriptive statistics and core visualizations.

### 2) Reproduce Model Development Pipeline
- Implements logistic regression as in the R workflow.
- Uses equivalent feature set and reference-category treatment.
- Documents modeling steps and parameter choices in notebook sections.

### 3) Replicate Model Evaluation and Diagnostics
- Produces confusion matrix and standard evaluation metrics.
- Reports race-level diagnostics (including FPR/FNR disparities).
- Includes interpretation and notes on small R-vs-Python implementation differences.

### 4) Documentation and Reproducibility
- Notebook is organized from data loading to final interpretation.
- Major workflow stages are labeled and explained.
- Running cells top-to-bottom reproduces the analysis outputs.

## Reproducibility Instructions
1. Create and activate a Python 3.11+ environment.
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib statsmodels scikit-learn
   ```
3. Open Jupyter and run all cells in:
   - `Assignment 1.ipynb`

## Expected Outputs
- EDA summaries for age, race, sex, and score distributions.
- Logistic regression summary table.
- Overall confusion matrix and classification metrics.
- Race-level fairness diagnostics and disparity table.

## Submission Checklist (for GitHub repo)
- Python notebook implementing full workflow: included.
- README containing purpose, libraries, and reproducibility instructions: included.

## Note on Minor Differences
Small numeric differences versus R may appear due to differences in optimization defaults and floating-point behavior across libraries. Analytical conclusions remain the same.
