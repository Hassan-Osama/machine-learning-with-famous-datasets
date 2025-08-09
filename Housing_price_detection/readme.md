# Housing Price Prediction

This project aims to predict housing prices using a variety of regression techniques on a real estate dataset. The goal is to explore data preprocessing, feature engineering, and multiple machine learning models to achieve accurate price predictions.

## Project Overview

Predicting house prices accurately is crucial for buyers, sellers, and real estate professionals. This project applies classical regression models along with tree-based ensemble methods to model the relationship between housing features and their prices.

## Dataset

The dataset contains housing data with features such as:

- Square footage
- Number of bedrooms and bathrooms
- Date of sale (processed into year, month, day)
- Other property-related features

## Data Preprocessing

- Converted date columns to separate year, month, and day features.  
- Dropped irrelevant features such as unique IDs.  
- Handled multicollinearity by removing features with high correlation.  
- Split the dataset into training and testing sets.

## Models Explored

- **Linear Regression**  
- **K-Nearest Neighbors Regression (KNN)**  
- **Decision Tree Regression**  
- **Random Forest Regression**

Hyperparameters were tuned for KNN, Decision Trees, and Random Forest using GridSearchCV.

## Results

- **The linear regression model** struggled due to apparent non-linearity in the data.

- **Decision tree model** improved performance.

- **Random Forest** achieved the best performance, highlighting the benefit of ensemble non-linear methods on this dataset.
