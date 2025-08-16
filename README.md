# Satellite Orbit Anomaly Detection

This repository contains the code and data for residual-based satellite manoeuvre detection using ARIMA and XGBoost models. 
The project compares time series approaches for anomaly detection in orbital element data.

## Repository Structure

The repository follows the workflow described in the report:

- **`1_clean_and_tidy.ipynb`** - Preprocessing pipeline for orbital element data and manoeuvre ground-truth records
- **`2_eda.ipynb`** - Exploratory Data Analysis (EDA) and satellite selection
- **`3_ARIMA Implementation.ipynb`** - ARIMA model fitting and residual analysis  
- **`4_XGBoost Implementation.ipynb`** - XGBoost implementation with Optuna hyperparameter optimization
- **`5_Result Analysis.ipynb`** - Model comparison, precision-recall analysis, and visualization

**Note:** `.pkl` files contain saved outputs from model optimization and evaluation. These can be loaded directly to reproduce results without re-running computationally expensive steps.

## Requirements

pandas, numpy, matplotlib, seaborn, scikit-learn, xgboost, optuna, statsmodels, scipy

## Usage

1. **Data Preparation**: Run `1_clean_and_tidy.ipynb` to standardize input files
2. **Exploration**: Use `2_eda.ipynb` to reproduce exploratory analysis  
3. **Model Training**:
   - `3_ARIMA Implementation.ipynb` for ARIMA forecasting (~10 min runtime)
   - `4_XGBoost Implementation.ipynb` for XGBoost optimization (~2-3 hours)
4. **Results**: Use `5_Result Analysis.ipynb` to generate plots and model comparisons
