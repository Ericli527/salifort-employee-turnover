# Salifort Motors Employee Turnover Prediction

## Project Overview

This project analyses employee turnover at Salifort Motors and develops
machine-learning models to identify employees at risk of leaving.

I conducted exploratory data analysis, feature engineering and predictive
modelling using Logistic Regression, Random Forest and XGBoost.

## Model Results

The tuned Random Forest achieved:

- Accuracy: 98.6%
- Precision: 99.1%
- Recall: 92.4%
- F1-score: 95.6%
- ROC-AUC: 0.980
- PR-AUC: 0.963

Five-fold cross-validation produced an average F1-score of approximately
94.9%, supporting the model's generalisation performance.

## Key Findings

Employee turnover was strongly associated with factors including:

- Satisfaction level
- Time spent at the company
- Number of projects
- Last evaluation
- Average monthly working hours

These variables represent predictive associations and should not be
interpreted as causal effects.

## Business Application

The analysis could support HR in identifying patterns associated with
employee turnover and designing targeted retention strategies around
employee satisfaction, workload and career development.

## Tools

Python | pandas | scikit-learn | XGBoost | GridSearchCV |
Matplotlib | Seaborn | Jupyter Notebook

## Project Files

- Jupyter Notebook – full analysis and modelling
- Executive Summary – findings for business stakeholders
- HR & Board Presentation – presentation of results and recommendations

