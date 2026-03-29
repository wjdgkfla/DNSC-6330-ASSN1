# Assignment 1 - Translating an R Machine Learning Workflow into Python (COMPAS)

## Purpose of the Analysis
This notebook reproduces the Lecture 01 COMPAS analysis by translating the original R workflow into Python. The goal is to preserve all substantive analytical steps: EDA, preprocessing, model development, diagnostics, and interpretation.

## Notebook Included
- `Assignment 1.ipynb` - Complete Python translation of the Lecture 01 COMPAS workflow

## Reference Material
This notebook replicates the R-based lecture notebook (`Lecture-01-alignment.ipynb`) covered during Lecture 01: Foundations of the Alignment Problem (DNSC 6330). The R reference notebook is provided by the instructor in course materials; this submission contains the Python equivalent.

## Libraries Used
- `pandas`
- `numpy`
- `matplotlib`
- `statsmodels`
- `scikit-learn`

## How This Notebook Meets the Assignment Requirements

### 1) Replicate Exploratory Data Analysis (EDA)
Assignment requirement: Load dataset, perform preprocessing, and reproduce descriptive statistics and visualizations.

This notebook includes:
- SECTION 2: Load COMPAS dataset from ProPublica URL (equivalent to R `read.csv()`)
- SECTION 3: Data cleaning/filtering (equivalent to `dplyr::filter()` logic)
- SECTION 4: Feature engineering and categorical variable creation (equivalent to `factor()` and `relevel()`)
- SECTION 5: EDA summaries by age, race, sex, and decile scores
- Visualizations: Histograms of decile scores by race and crosstabs of demographic variables

### 2) Reproduce Model Development Pipeline
Assignment requirement: Implement the same modeling approach with clear documentation of feature selection and parameter choices.

This notebook includes:
- SECTION 6: Modeling dataset preparation
- SECTION 7: Logistic regression using `statsmodels.formula.api.glm()` (R equivalent: `glm(..., family=binomial(link="logit"))`)
- Explicit feature formula and explicit reference categories using `Treatment(reference=...)`

### 3) Replicate Model Evaluation and Diagnostics
Assignment requirement: Implement diagnostic procedures and ensure conceptual correspondence to the R workflow.

This notebook includes:
- SECTION 8-10: Predicted probabilities, binary classification, and overall confusion matrix metrics (accuracy, precision, recall, FPR, FNR)
- SECTION 11: Race-level confusion matrices and group-conditional error rates
- SECTION 12: Disparity table (`delta_FPR`, `delta_FNR`) relative to Caucasian baseline
- SECTION 12A: Companion lecture-rule check using `decile_score >= 7`
- SECTION 13: Comprehensive interpretation and Responsible ML implications

### 4) Documentation and Reproducibility
Assignment requirement: Fully reproducible and clearly organized.

This notebook includes:
- Clear markdown headers and section structure
- Inline explanations for data-quality filtering and variable transformations
- Organized pipeline: data loading -> preprocessing -> EDA -> modeling -> evaluation -> interpretation
- Executable cells with saved outputs for grading and verification

## Thresholding Clarification (Lecture 01 Consistency)
Lecture 01 presents two related binary-decision framings:
- Explicit COMPAS rule framing: classify high risk via `decile_score >= 7`
- Live-coding model-diagnostics framing: classify via `pred_prob >= 0.5`

This notebook follows the live-coding model-diagnostics pathway for the main confusion-matrix analysis and includes a companion Section 12A with the explicit `decile_score >= 7` check.

## Reproducibility Instructions

### Environment Setup
1. Create and activate a Python 3.11+ environment:
```bash
python3 -m venv compas_env
source compas_env/bin/activate  # Windows: compas_env\Scripts\activate
```

2. Install dependencies:
```bash
pip install pandas numpy matplotlib statsmodels scikit-learn
```

### Running the Notebook
1. Launch Jupyter:
```bash
jupyter notebook
```

2. Open `Assignment 1.ipynb` and run all cells in order.

3. Verify outputs include:
- EDA summaries and visualizations
- Logistic regression summary table
- Overall confusion matrix metrics
- Race-level fairness metrics and disparity table
- Companion `decile_score >= 7` diagnostic metrics
- Final interpretation section

## Verification Checklist
- All notebook sections execute without errors.
- Data loads from ProPublica COMPAS source.
- Filtered sample size matches lecture expectations (~6,170 records).
- Histograms show decile-score distributions by race.
- Logistic model produces expected directionality for key coefficients.
- Fairness disparity results are present and interpretable.
- Outputs are embedded in the notebook.

## Note on Minor Numeric Differences
Small differences versus R can appear due to implementation details (optimization tolerances and floating-point behavior). Substantive conclusions remain the same.
