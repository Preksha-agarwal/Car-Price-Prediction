# Car Price Prediction Using Multiple Linear Regression

## Overview

This project aims to predict the Manufacturer's Suggested Retail Price (MSRP) of cars using a multiple linear regression model. The dataset used for this analysis contains various features of cars, including engine specifications, vehicle type, and manufacturer details. The goal is to explore the data, preprocess it, and build a robust predictive model. The complete analysis and model development has been done on Python.

## Python Libraries used

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Statsmodels

## Dataset

The dataset used in this project is taken from Kaggle and is called Car features and MSRP. It contains various features related to cars, such as:

- Make
- Model
- Year
- Engine Specifications
- Vehicle Type
- Price (MSRP)

## Data Exploration

The initial phase involved exploring the dataset to understand its structure and identify any anomalies. Key steps included:

- Checking for duplicates and null values.
- Conducting univariate and bivariate analyses using visualizations to understand feature distributions and correlations with MSRP.
- Checking for correlations in the data

## Data Preprocessing

Data preprocessing steps included:

1. **Handling Missing Values**: Dropping or imputing missing values based on their impact on the dataset.
2. **Encoding Categorical Features**: Using One-Hot Encoding for nominal variables and Ordinal Encoding for ordinal variables.
3. **Feature Scaling**: Standardizing numerical features to bring them onto a similar scale.
4. **Outlier Treatment**: Identifying and removing outliers based on the interquartile range.

## Model Training

### Train-Test Split

The dataset was split into training and testing sets using an 80-20 ratio.

### Feature Engineering

- **Power Transformation**: Used box-cox transformation to normalize the target variable (MSRP).
- **Variance Inflation Factor (VIF)**: Computed VIF to check for multicollinearity
- **Principal Component Analysis (PCA)**: Applied to reduce multicollinearity and dimensionality.

### Model Selection

Multiple models were trained and evaluated:
- **Linear Regression**
- **Ridge Regression**
- **Lasso Regression**

Cross-validation was employed to assess model performance, with metrics such as R² and Mean Squared Error calculated.

## Results

The best-performing model was identified based on cross-validation scores. Residual plots were used to check for patterns in the errors, and various metrics were calculated to evaluate model performance.

## Conclusions

Achieved an adjusted R-squared value of 80.88% which was increased to a value of 82.60% by Ridge Regularization. The mean squared error of the model reduced from 0.16 to 0.11 using Ridge regression

## Future Work

Future enhancements could include:

- Experimenting with more advanced models (e.g., Random Forest, Gradient Boosting).
- Incorporating additional datasets for improved accuracy.
- Developing a web application for real-time price prediction.
