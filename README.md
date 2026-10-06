# Customer Churn Intelligence Platform

## Overview

An end-to-end customer churn intelligence project combining machine learning, explainable AI, customer segmentation, risk scoring, and Power BI business intelligence.

The project focuses on identifying customers with elevated churn probability, understanding factors associated with observed churn, and supporting customer-risk prioritization.

## Business Problem

This project answers:

- Which customers have elevated churn probability?
- What characteristics are associated with observed churn?
- Which machine learning approach performs best?
- How can churn predictions be converted into useful business intelligence?

## Project Workflow

Data Cleaning
→ Exploratory Data Analysis
→ Feature Preparation
→ Model Comparison
→ XGBoost
→ Churn Probability
→ Risk Classification
→ SHAP Explainability
→ Customer Segmentation
→ Power BI Dashboard

## Dataset

IBM Telco Customer Churn dataset.

- 7,043 customer records
- 21 original variables
- Target: Churn
- Numerical and categorical customer attributes

Data preparation included numeric conversion, missing-value handling, duplicate checks, categorical encoding, feature scaling, and stratified train/test splitting.

The Power BI dashboard uses the 1,409-customer test set generated during model evaluation.

## Machine Learning

Models evaluated:

- Logistic Regression
- Random Forest
- XGBoost

The final pipeline uses XGBoost to estimate customer churn probability.

Evaluation includes:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- PR-AUC
- Threshold analysis

## Explainable AI

SHAP is used to understand model behavior at both global and individual-customer levels.

Power BI Key Influencers is also used to explore statistical associations with observed churn.

These relationships should not be interpreted as causal effects.

## Risk Scoring

Customers are classified using predicted churn probability:

| Probability | Risk |
|---|---|
| 0–30% | Low |
| 30–60% | Medium |
| 60–100% | High |

Risk levels are intended for prioritization and do not represent guaranteed churn outcomes.

## Customer Segmentation

K-Means clustering was applied using:

- Tenure
- Monthly Charges
- Total Charges

Four customer segments were identified for additional customer profiling.

## Power BI Dashboard

The dashboard contains four pages:

### Executive Summary
Overall churn metrics, risk distribution, churn patterns, filters, and customer risk exploration.

### Churn Intelligence
Key Influencers analysis for characteristics associated with observed churn.

### Customer Detail
Customer-level drill-through containing churn probability, risk level, contract, tenure, charges, service information, and churn status.

### Risk Analysis
Interactive risk-threshold analysis for identifying customers above a selected probability threshold.

## Interactive Features

- Risk-level filtering
- Contract filtering
- Internet-service filtering
- Customer drill-through
- Dynamic risk-threshold analysis
- Customer-level risk exploration

## Technology Stack

Python | Pandas | NumPy | Scikit-learn | XGBoost | SHAP | K-Means | Power BI | Google Colab | GitHub

## Repository Structure

customer-churn-intelligence/

- app/
- dashboard/
- data/
- models/
- notebooks/
- src/
- tests/
- README.md

## Limitations

- The dataset is a static customer snapshot.
- This project focuses on churn classification and risk prioritization rather than 30/60/90-day forecasting.
- Predicted probabilities are not guaranteed outcomes.
- Observational relationships do not establish causality.
- Retention effectiveness was not experimentally measured.
- External factors such as competitor pricing and customer satisfaction are not included.

## Future Improvements

- Real-time customer data
- Automated model retraining
- Model monitoring
- Customer lifetime value analysis
- CRM integration
- Automated retention recommendations
- Temporal churn modeling using longitudinal data

## Project Objective

The goal was to demonstrate an end-to-end data science workflow:

Data → Analysis → Prediction → Evaluation → Explanation → Segmentation → Risk → Business Intelligence
