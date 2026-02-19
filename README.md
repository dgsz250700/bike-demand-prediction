# Bike Rental Demand Prediction using Polynomial Regression and Lasso

## Project Overview

Climate change and environmental degradation have increased the need for sustainable mobility solutions. Promoting bicycle-sharing systems is one effective strategy to reduce CO₂ emissions.

This project develops predictive regression models to estimate bike rental demand based on temporal and weather-related features. The objective is to support operational planning and identify the key factors influencing system usage.

The project follows the complete Machine Learning lifecycle:
- Exploratory Data Analysis (EDA)
- Data cleaning and preprocessing
- Model training
- Hyperparameter selection via cross-validation
- Model evaluation
- Model interpretation

Academic project developed in 2026 as part of a Machine Learning course.

---

## Dataset

The dataset contains **17,380 observations** and includes:

- Target variable: number of rented bikes
- Weather-related features (temperature, humidity, wind speed, etc.)
- Temporal features (hour, season, day, etc.)

The dataset was adapted for academic purposes from an original bike-sharing dataset.

---

## Objectives

- Build a **Polynomial Regression model** to predict demand.
- Build a **Lasso Regression model** with L1 regularization.
- Select optimal hyperparameters using cross-validation (RMSE metric).
- Compare model performance using R², RMSE, and MAE.
- Identify the most influential predictors using Lasso.

---

## Data Preparation

- Exploratory analysis using `pandas`
- Data quality checks
- Feature preprocessing
- Train/Test split with `random_state = 77`
- Model selection using cross-validation

---

## Models Implemented

### 1. Polynomial Regression

- Candidate degrees: `[2, 3]`
- Hyperparameter selected via cross-validation (10-fold)
- Selection metric: **RMSE**
- Best degree: **3**

### 2. Lasso Regression

- Candidate α values: `[1, 2, 3, 4, 5]`
- Hyperparameter selected via cross-validation
- Selection metric: **RMSE**
- Best α: **1**

---

## Model Evaluation

Models were evaluated on the test set using:

- **R² (Coefficient of Determination)**
- **RMSE (Root Mean Squared Error)**
- **MAE (Mean Absolute Error)**

### Best Model

Polynomial Regression (degree = 3) achieved better performance on the test set compared to Lasso.

This suggests that moderate non-linear relationships improve predictive accuracy, while Lasso provides a more interpretable sparse model.

---

## Key Insights

Using Lasso regression, the most influential variables affecting bike demand were identified.

Main drivers include:
- Weather conditions
- Temporal patterns (hour, season)
- Environmental factors

These findings can support:
- Better bike distribution strategies
- Demand forecasting
- Data-driven mobility planning

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib


