# bnpl-risk-analysis
Overview

This project focuses on analyzing and predicting repayment risks among Buy Now Pay Later (BNPL) users using Machine Learning techniques.

The project aims to identify users who are likely to experience late payments or payment defaults, segment users based on their behavior, and understand the key factors influencing repayment risks.

The analysis combines classification, clustering, feature engineering, and model explainability to provide a more comprehensive understanding of BNPL user behavior.

Objectives

Analyze BNPL user characteristics and repayment behavior.

Predict the probability of payment default.

Segment users into different behavioral and risk-based personas.

Develop a BNPL Risk Index to measure individual user risk.

Identify important features influencing repayment predictions using SHAP.

Dataset

The project uses the bnpl_dataset_v2.csv dataset.

Some of the features used in the analysis include:

Feature

Description

customer_age

Customer age

annual_income

Annual customer income

credit_score

Customer credit score

purchase_amount

BNPL transaction amount

checkout_time_seconds

Checkout duration

purchase_category

Purchase category

bnpl_provider

BNPL service provider

repayment_status

Original repayment status

Note: The dataset is not included in this repository. You need to provide the dataset separately to run the notebook.

Technologies & Libraries

Python

Pandas & NumPy

Matplotlib & Seaborn

Scikit-learn

XGBoost

SHAP

Project Workflow

1. Data Exploration & Cleaning

Load and inspect the dataset.

Identify missing values.

Standardize column names.

Remove duplicate records.

Convert numerical columns into appropriate data types.

2. Feature Engineering

Create additional features to improve model performance, including:

Purchase-to-income ratio.

Income-to-purchase ratio.

Log transformations.

Credit score risk indicators.

Purchase and income risk flags.

Age and credit score categories.

Risk pressure score.

3. Target Encoding

The original repayment_status is converted into a binary classification target:

Label

Meaning

0

Paid on time

1

Late payment / Default

4. User Segmentation with K-Means

K-Means clustering is used to divide BNPL users into four personas based on their characteristics and repayment risk:

Responsible User

Promo Hunter

Frequent Borrower

High Risk Borrower

5. Classification Models

Three classification algorithms are implemented and compared:

Logistic Regression

Random Forest

XGBoost

XGBoost is further optimized using class imbalance handling and threshold tuning.

6. Model Evaluation

The models are evaluated using:

Accuracy

Balanced Accuracy

Precision

Recall

F1-Score

ROC-AUC

PR-AUC

Confusion Matrix

Classification Report

Threshold tuning is performed to find a suitable classification threshold based on the F2-score.

7. BNPL Risk Index

A risk scoring system is developed using XGBoost prediction probabilities.

The predicted probability is converted into a BNPL Risk Index ranging from 0 to 100.

Users are categorized into four risk levels:

Risk Level

Description

Low

Low repayment risk

Medium

Moderate repayment risk

High

High repayment risk

Critical

Very high repayment risk

8. Model Explainability with SHAP

SHAP (SHapley Additive exPlanations) is used to:

Identify the most influential features.

Understand how features affect model predictions.

Analyze the top risk factors for individual users.
