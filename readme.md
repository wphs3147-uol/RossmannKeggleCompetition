# Rossmann Store Sales Forecasting Project

Kaggle competition page: https://www.kaggle.com/competitions/rossmann-store-sales/

## Project overview

This project is based on the Rossmann Store Sales forecasting problem. The aim is to predict daily sales turnover for Rossmann stores using historical sales data and store-level information.

The dataset contains daily observations for stores, including variables such as date, store number, whether the store was open, whether a promotion was running, state holidays, school holidays, and the observed sales value. A separate store-description file contains additional information about each store, such as store type, assortment type, competition distance, and longer-term promotion details.

In this workshop version, we do not use the official Kaggle test set for evaluation because the true sales values are hidden. Instead, we create our own transparent test period by holding out the final month of the labelled training data. The model is trained on earlier dates and then used to forecast sales for the held-out final month, allowing the predictions to be compared with the true sales values.

The workflow includes:

1. Loading and inspecting the Rossmann data.
2. Merging daily sales data with store-level information.
3. Creating a time-based train/test split.
4. Building a simple baseline forecast.
5. Engineering useful features from dates, promotions, store information, and recent sales history.
6. Training XGBoost regression models.
7. Evaluating forecasts using RMSPE.
8. Inspecting prediction errors and feature importance.

The project illustrates the importance of feature engineering in real-world forecasting problems.
