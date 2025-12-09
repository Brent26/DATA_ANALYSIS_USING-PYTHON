# Customer Churn Analysis — ADA Assignment Final

This repository contains a Jupyter Notebook performing exploratory data analysis, hypothesis testing, and a simple predictive model on a customer churn dataset.

**Primary notebook**: `ADA ASSGIN FINAL.ipynb`

## Overview
- **Goal:** Explore customer churn drivers, test relationships between variables and churn, and build a baseline logistic regression model to predict churn.
- **Workflows included:** data loading and cleaning, missing-value handling, EDA (plots and summaries), hypothesis testing (chi-square), feature scaling, model training, and evaluation (classification report and confusion matrix).

## Files
- **`ADA ASSGIN FINAL.ipynb`**: Main notebook with the full analysis and visualizations.
- **Dataset (expected):** `churn_real.xlsx` — the notebook reads this file using `openpyxl`.

## Requirements
- Python (3.8+ recommended)
- Key packages used in the notebook:
  - `pandas`, `numpy`
  - `matplotlib`, `seaborn`
  - `openpyxl`
  - `scipy`
  - `scikit-learn`
  - `IPython`

Optional: create a `requirements.txt` with these packages if you want reproducible installs.

## Setup (Windows PowerShell)
1. Create and activate a virtual environment:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install packages (example):

```powershell
pip install pandas numpy matplotlib seaborn openpyxl scipy scikit-learn ipython
```

3. Start Jupyter and open the notebook:

```powershell
jupyter notebook
```

Open `ADA ASSGIN FINAL.ipynb` in the browser and run cells in order.

## Notebook highlights
- Loads `churn_real.xlsx` and inspects missing values and types.
- Converts `Total Charges` to numeric and fills missing values with the mode.
- Plots numeric summaries and per-churn-group comparisons (`Monthly Charges`, `Total Charges`, `Tenure Months`, `CLTV`).
- Visualizes churn distribution (pie chart) and categorical variable relationships (countplots by churn label).
- Computes skewness and creates regression/KDE/box plots against `Churn Score`.
- Performs chi-square tests for relationships (e.g., `Phone Service`, `Contract`, `Senior Citizen`) vs `Churn Label`.
- Scales numeric features, splits data, trains a Logistic Regression model, and reports performance (classification report and confusion matrix).

## Results (where to find them)
- Model accuracy and classification metrics are printed in the notebook near the logistic regression section.
- Confusion matrix is displayed using `ConfusionMatrixDisplay`.
- Chi-square results (statistic, p-value, dof) are printed in the hypothesis-testing cells.

## Next steps / Suggestions
- Try additional models (Random Forest, XGBoost) and compare ROC/AUC.
- Perform feature engineering (categorical encoding, interaction terms).
- Run cross-validation and hyperparameter tuning (GridSearchCV).
- Create a small script to serialize the trained model and a simple inference notebook.

## Contact
If you want me to run tests, add a `requirements.txt`, or convert the notebook into a reproducible script, tell me which option you'd like next.
