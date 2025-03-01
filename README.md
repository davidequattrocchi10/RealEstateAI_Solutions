# RealEstateAI Solutions: Advanced Regression Models for Real Estate Price Prediction

## Overview
RealEstateAI Solutions aims to optimize real estate price evaluation using advanced regularization techniques in linear regression models. 
This project implements and compares Lasso, Ridge, and Elastic Net regression to provide more accurate and robust price predictions, mitigating overfitting and enhancing model generalization.

## Problem Statement
The project addresses the need for precise real estate price estimates in a market where traditional linear regression may suffer from overfitting. 
By exploring effective regularization methods, the solution strives to:
- Improve predictive performance.
- Control model complexity.
- Deliver more reliable pricing estimates for real estate agents and investors.

## Project Structure
- **Data Preparation**:  
  - Load and preprocess the dataset (Download the dataset from this link: https://www.kaggle.com/datasets/yasserh/housing-prices-dataset)
  - Handle missing values and encode categorical variables (e.g., mapping 'yes'/'no' to 1/0, ordinal encoding for `furnishingstatus`).
  - Visualize feature correlations using a heatmap.
  
- **Dataset Splitting**:  
  - Split the dataset into training and testing sets (70% train, 30% test).

- **Model Evaluation**:  
  - Define a function to evaluate models using metrics such as Mean Squared Error (MSE), Mean Absolute Error (MAE), and R² score.

- **Custom Cross Validation**:  
  - Implement a custom cross validation function using KFold.
  - Standardize the data within each fold to avoid data leakage.
  - Assess the model performance on different splits of the training set.

- **Model Implementation and Tuning**:  
  - Apply Lasso, Ridge, and Elastic Net regression.
  - For each model, perform cross validation on the training set.
  - Build a pipeline (scaler + model) and use GridSearchCV for hyperparameter tuning.
  - Train the final model on the entire training set with the best parameters and predict on the test set.

- **Performance Comparison and Visualization**:  
  - Compare models based on MAE and R².
  - Visualize the results with bar plots and analyze the distribution of residuals.

## Conclusion
This project demonstrates how regularization techniques, combined with cross validation and proper data preprocessing,
can significantly enhance the reliability of regression models in predicting real estate prices. 
The use of pipelines and hyperparameter tuning across GridSearchCV ensures a robust approach, minimizing overfitting and ensuring the model generalizes well to unseen data.
