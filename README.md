# House-Price-Predicion-AdvancedRegression
End-to-end house price prediction using Scikit-learn with advanced preprocessing pipelines, feature engineering, and Random Forest regression

# 🏠 House Prices Prediction using Machine Learning

## Overview

This project focuses on predicting residential house prices using supervised machine learning techniques. The objective is to build an end-to-end machine learning pipeline that can accurately estimate a property's selling price based on various structural, locational, and quality-related features.

The project follows a complete machine learning workflow, including data exploration, preprocessing, feature engineering, pipeline creation, model training, hyperparameter tuning, and model evaluation.

---

## Problem Statement

House price prediction is a regression problem where the goal is to estimate the selling price of a house using its characteristics. Accurate price prediction helps buyers, sellers, real estate agencies, and financial institutions make informed decisions.

The target variable is:

- **SalePrice**

---

## Dataset

**Source:** Kaggle - House Prices: Advanced Regression Techniques

The dataset contains information about residential houses in Ames, Iowa.

### Dataset Summary

| Property | Value |
|----------|-------|
| Training Samples | 1460 |
| Test Samples | 1459 |
| Features | 79 |
| Target Variable | SalePrice |

The features describe:

- Lot characteristics
- Building quality
- House dimensions
- Basement information
- Garage information
- Neighborhood
- Exterior & interior quality
- Utilities
- Sale information

---

## Project Workflow

- Data Loading
- Data Understanding
- Exploratory Data Analysis (EDA)
- Missing Value Analysis
- Data Cleaning
- Feature Engineering
- Data Preprocessing
- Pipeline Construction
- Model Training
- Hyperparameter Tuning
- Model Evaluation
- Feature Importance Analysis

---

## Exploratory Data Analysis

The following analyses were performed:

- Distribution of SalePrice
- Missing Value Analysis
- Correlation Analysis
- Numerical Feature Analysis
- Categorical Feature Analysis
- Outlier Detection
- Feature Relationships

---

## Data Preprocessing

A preprocessing pipeline was created using **Scikit-learn's Pipeline** and **ColumnTransformer**.

Different preprocessing strategies were applied based on the nature of missing values.

### Numerical Features

- Missing values representing absent features → Filled with **0**
- Genuine missing values → Filled using **Median**
- Feature Scaling using **StandardScaler**

### Categorical Features

- Missing values representing absent features → Filled with **"None"**
- Genuine missing values → Filled using **Most Frequent Value**
- One-Hot Encoding using **OneHotEncoder**

---

## Machine Learning Pipeline

The preprocessing workflow consists of:

- Multiple preprocessing pipelines
- ColumnTransformer
- Random Forest Regressor

This approach ensures:

- No data leakage
- Consistent preprocessing
- Reproducible workflow
- Clean and maintainable code

---

## Models Evaluated

The following regression models were explored:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor

Random Forest Regressor achieved the best overall performance.

---

## Model Performance

| Metric | Score |
|---------|--------|
| R² Score | **0.869** |
| MAE | **18,256.72** |
| RMSE | **29,860.81** |

---

## Feature Importance

The trained Random Forest model was analyzed to determine the most influential features contributing to house price prediction.

Examples include:

- Overall Quality
- Ground Living Area
- Garage Capacity
- Neighborhood
- Total Basement Area

*(See `images/feature_importance.png` for visualization.)*

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

## Repository Structure

```
house-prices-prediction/
│
├── data/
├── notebook/
├── images/
├── README.md
├── requirements.txt
├── environment.yml
├── .gitignore
└── LICENSE
```

---

## Key Learnings

During this project, I learned how to:

- Perform end-to-end regression modeling
- Handle different types of missing values
- Build modular preprocessing pipelines
- Prevent data leakage
- Use ColumnTransformer effectively
- Compare multiple machine learning models
- Perform hyperparameter tuning
- Interpret feature importance
- Build production-style Scikit-learn pipelines

---

## Future Improvements

Potential enhancements include:

- Feature Engineering
- Gradient Boosting Regressor
- XGBoost
- LightGBM
- SHAP Explainability
- Model Deployment using Flask or FastAPI

---

## Author

**Ayush**

Engineering Student | AI & Data Science

---

## Acknowledgements

Dataset provided by the **Kaggle House Prices: Advanced Regression Techniques** competition.
