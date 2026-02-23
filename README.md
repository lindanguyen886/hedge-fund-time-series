# Hedge Fund Time Series Forecasting

Financial forecasting project using LightGBM to model multi-horizon time-series behavior in hedge fund data.
Kaggle competition: https://www.kaggle.com/competitions/ts-forecasting/overview

---

## Key Result

Achieved **Weighted RMSE ≈ 0.079** using time-aware validation, LightGBM tuning, and cross-sectional modeling.

---

## Problem

Predict a continuous financial target (`y_target`) across multiple forecast horizons using:

- time-indexed signals
- entity identifiers
- structured tabular features

Challenges:
- heavy-tailed distribution
- missing data
- nonlinear relationships
- cross-sectional dependencies

---

## Approach

- Time-based validation split to avoid leakage
- Gradient boosting model (LightGBM)
- Early stopping for optimal iteration
- Diagnostics by forecast horizon
- Iterative hyperparameter tuning

Final model:

- learning_rate = 0.05  
- num_leaves = 256  
- n_estimators = 270  
- random_state = 42  

---

## Model Insight

- Strong performance for short-term predictions  
- Errors increase with longer horizons  
- Model captures nonlinear structure  
- Extreme tail events remain difficult to predict  

---

## Why This Matters

Financial time-series data is noisy and unstable.  
This project demonstrates practical modeling decisions for handling:

- missing values
- heavy-tailed targets
- temporal leakage
- cross-sectional structure

---

## Status

Work in progress.

Completed:
- EDA
- validation design
- baseline modeling
- hyperparameter tuning
- diagnostics

In progress:
- feature engineering
- regularization improvements
- horizon-specific models

---

## Tech Stack

Python · Pandas · NumPy · LightGBM · Scikit-learn · Matplotlib

---

## Notes

Dataset from Kaggle competition (not included due to licensing).  
Repository contains modeling workflow and methodology only.

---

## Author

Linda Nguyen  
M.M. Data Analytics — University of Windsor
