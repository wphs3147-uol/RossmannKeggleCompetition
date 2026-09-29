# Rossmann Store Sales Forecasting

An end-to-end, reproducible example of feature engineering and time-aware
evaluation for retail sales forecasting.

The main analysis is in [`notebooks/rossmann_forecasting_demo.ipynb`](notebooks/rossmann_forecasting_demo.ipynb).
It uses the included mock sales data for a transparent evaluation.

Kaggle competition page: https://www.kaggle.com/competitions/rossmann-store-sales/

## Project overview

This project is based on the Rossmann Store Sales forecasting problem. The aim is to predict daily sales turnover for Rossmann stores using historical sales data and store-level information.

The dataset contains daily observations for stores, including variables such as date, store number, whether the store was open, whether a promotion was running, state holidays, school holidays, and the observed sales value. A separate store-description file contains additional information about each store, such as store type, assortment type, competition distance, and longer-term promotion details.

The evaluation holds out the final month of labelled data rather than using the official Kaggle test set, whose true values are hidden. The model is trained on earlier dates and forecast performance is compared with the known holdout values.

The demonstration includes:

1. Auditing a small retail dataset.
2. Creating calendar, lag, and rolling-window features.
3. Splitting chronologically to avoid leakage.
4. Comparing a seasonal baseline with a tree-based model.
5. Evaluating the forecast with MAE and RMSE.
6. Inspecting which features drive the prediction.
