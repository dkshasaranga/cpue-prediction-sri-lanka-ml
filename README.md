# CPUE Prediction in Sri Lankan Fisheries Using Machine Learning

This repository contains the implementation developed for the MSc thesis:

**"Evaluating Machine Learning Models for Predicting Catch Per Unit Effort in Sri Lankan Fisheries"**

The study evaluates multiple machine learning approaches for predicting Catch Per Unit Effort (CPUE) in the spotted sardinella (*Amblygaster sirm*) fishery using fisheries operational records and environmental data collected from Sri Lanka between 2000 and 2020.

## Objectives

- Predict CPUE using machine learning techniques
- Compare direct regression models and Delta-based machine learning models
- Address zero-inflated CPUE data
- Evaluate models using time-aware cross-validation
- Interpret model predictions using SHAP and permutation importance

## Models Evaluated

### Direct Models
- Huber Regression
- Random Forest
- Extra Trees
- XGBoost
- LightGBM
- CatBoost

### Delta-Based Models
- Logistic Regression + Random Forest
- Logistic Regression + XGBoost
- Random Forest + Random Forest
- Random Forest + XGBoost
- XGBoost + XGBoost
- LightGBM + LightGBM
- CatBoost + CatBoost (CAT_CAT)

## Methodology

- Data preprocessing and feature engineering
- CPUE lag feature generation
- Environmental data integration
- TimeSeriesSplit cross-validation
- Model comparison using RMSE, MAE, and R²
- Friedman statistical significance testing
- SHAP and permutation importance analysis

## Key Findings

- Delta-based models consistently outperformed direct regression models.
- The CAT_CAT model achieved the best overall predictive performance.
- Historical CPUE information (CPUE_Lag1) was the most influential predictor.
- Environmental and operational variables contributed substantially to model performance.
- Time-aware validation provided realistic performance estimates while reducing temporal information leakage.

## Disclaimer

The fisheries dataset used in this study was obtained from the National Aquatic Resources Research and Development Agency (NARA), Sri Lanka, and is not included in this repository.
