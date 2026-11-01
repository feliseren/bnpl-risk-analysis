# BNPL Risk Analysis & Prediction

## Overview

This project focuses on analyzing and predicting repayment risks among Buy Now Pay Later (BNPL) users using Machine Learning techniques.

The project aims to identify users who are likely to experience late payments or payment defaults, segment users based on their behavior, and understand the key factors influencing repayment risks.

The analysis combines classification, clustering, feature engineering, and model explainability to provide a comprehensive understanding of BNPL user behavior.

## Objectives

- Analyze BNPL user characteristics and repayment behavior.
- Predict the probability of payment default.
- Segment users based on their behavioral patterns and risk levels.
- Develop a BNPL Risk Index to measure individual user risk.
- Identify important features influencing repayment predictions using SHAP.

## Technologies & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- SHAP

## Project Workflow

### 1. Data Exploration & Cleaning
- Load and explore the dataset.
- Check missing values.
- Check duplicate records.
- Clean and prepare the data for analysis.

### 2. Feature Engineering

Create additional features to improve model performance, including:
- Purchase-to-income ratio.
- Income-to-purchase ratio.
- Log transformations.
- Credit score risk indicators.
- Purchase and income risk flags.

### 3. User Segmentation

K-Means clustering is used to group BNPL users into four behavioral personas:

- Responsible User
- Promo Hunter
- Frequent Borrower
- High Risk Borrower

### 4. Classification Models

Three classification algorithms are implemented and compared:

- Logistic Regression
- Random Forest
- XGBoost

### 5. Model Evaluation

The models are evaluated using several metrics:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- PR-AUC
- Confusion Matrix
- Classification Report

### 6. BNPL Risk Index

A risk scoring system is developed using XGBoost prediction probabilities.

The predicted probability is converted into a BNPL Risk Index ranging from 0 to 100.

Users are categorized into different risk levels:

- Low
- Medium
- High
- Critical

### 7. Model Explainability

SHAP (SHapley Additive exPlanations) is used to:

- Identify the most influential features.
- Understand how features affect model predictions.
- Analyze individual user risk factors.
