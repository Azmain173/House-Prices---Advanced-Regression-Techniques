# House-Prices---Advanced-Regression-Techniques



This repository contains my solution to the [House Prices - Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques) Kaggle competition. The goal of this competition is to predict the sale price of residential homes in Ames, Iowa, using advanced regression techniques.

## Table of Contents
1. [Problem Description](#problem-description)
2. [Dataset](#dataset)
3. [Preprocessing](#preprocessing)
4. [Modeling](#modeling)
5. [Results](#results)
6. [Dependencies](#dependencies)
7. [How to Run](#how-to-run)
8. [License](#license)

---

## Problem Description
The competition involves predicting the final sale price of homes based on 79 explanatory variables describing various aspects of residential homes. The challenge is to handle missing data, categorical variables, and feature engineering to build a robust regression model.

---

## Dataset
The dataset consists of two files:
- `train.csv`: Contains the training data with 1460 rows and 81 columns (including the target variable `SalePrice`).
- `test.csv`: Contains the test data with 1459 rows and 80 columns (excluding the target variable).

The dataset includes features such as:
- **Numerical features**: Lot area, total basement square footage, number of bedrooms, etc.
- **Categorical features**: House style, neighborhood, roof type, etc.

---

## Preprocessing
The preprocessing steps were crucial for preparing the data for modeling. Here's an overview of the steps I took:

1. **Handling Missing Values**:
   - Numerical features: Missing values were filled with the median of the respective column.
   - Categorical features: Missing values were filled with the mode (most frequent value) of the respective column.

2. **Feature Engineering**:
   - Created new features such as `TotalSF` (total square footage) by combining `TotalBsmtSF`, `1stFlrSF`, and `2ndFlrSF`.
   - Transformed skewed numerical features using logarithmic transformation to reduce the impact of outliers.

3. **Encoding Categorical Variables**:
   - Used **One-Hot Encoding** for categorical variables with low cardinality.
   - Applied **Label Encoding** for ordinal categorical variables (e.g., `ExterQual`, `KitchenQual`).

4. **Scaling Numerical Features**:
   - Standardized numerical features using `StandardScaler` to ensure all features were on the same scale.

5. **Target Variable Transformation**:
   - Applied a logarithmic transformation to the target variable `SalePrice` to normalize its distribution.

---

## Modeling
I experimented with several regression models, including:
- **Linear Regression**
- **Ridge Regression**
- **Lasso Regression**
- **Random Forest Regressor**
- **XGBoost Regressor**
- **LightGBM Regressor**

The final model was selected based on cross-validation performance and the Root Mean Squared Logarithmic Error (RMSLE) metric.

---

## Results
The best-performing model achieved an RMSLE of **X.XXXX** on the test set, placing me in the **top Y%** of the competition leaderboard.

---

## Dependencies
To run the code in this repository, you need the following Python libraries:
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- xgboost
- lightgbm

You can install the dependencies using the following command:
```bash
pip install -r requirements.txt
