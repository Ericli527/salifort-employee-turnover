# Salifort Motors Employee Turnover Prediction

## Project Overview

This project analyses employee turnover at Salifort Motors and develops machine-learning models to identify employees at risk of leaving.

The objective was not only to build an accurate predictive model, but also to translate workforce data into actionable insights that could help HR understand potential drivers of turnover and support more proactive retention strategies.

> **Key Finding:** Employee turnover was strongly associated with factors including satisfaction level, time spent at the company, number of projects, evaluation scores and working hours. The final Random Forest model achieved a **95.6% F1-score and 92.4% recall** for employees who left.

---

## Business Problem

Employee turnover can create significant recruitment, training and productivity costs. This project addresses three key questions:

- Which factors are most associated with employee turnover?
- Can machine learning accurately identify employees at higher risk of leaving?
- How can HR translate these insights into more proactive retention strategies?

The aim is to move from simply understanding historical turnover toward using workforce analytics as a decision-support tool.

---

## Approach

I conducted the project in Python using an end-to-end data analytics and machine-learning workflow:

1. **Data cleaning and validation** – examined the dataset for missing values, duplicates, outliers and data-quality issues.
2. **Exploratory data analysis** – investigated relationships between employee characteristics and turnover.
3. **Feature engineering** – prepared numerical and categorical variables for modelling.
4. **Logistic Regression** – established an interpretable baseline classification model.
5. **Random Forest** – developed an ensemble model and tuned its hyperparameters using GridSearchCV.
6. **XGBoost** – built a boosting model for comparison.
7. **Model evaluation and validation** – compared accuracy, precision, recall and F1-score, followed by cross-validation and ROC-AUC/PR-AUC evaluation.
8. **Business interpretation** – translated model findings into recommendations for HR and senior stakeholders.

---

## Key Findings

The analysis identified several important factors associated with employee turnover:

- **Satisfaction level** was one of the strongest predictors of whether an employee would leave.
- **Time spent at the company** and **number of projects** were also highly important predictors.
- **Evaluation scores** and **average monthly working hours** contributed useful information to the models.
- Turnover patterns also differed across factors such as **salary level** and **promotion history**.

These relationships should be treated as indicators for further investigation rather than evidence that individual factors directly cause employees to leave.

---

## Model Performance

Three classification models were evaluated:

| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| Logistic Regression | 83.4% | 50.2% | 20.5% | 29.1% |
| **Random Forest** | **98.6%** | **99.1%** | 92.4% | **95.6%** |
| XGBoost | 98.3% | 97.1% | **92.6%** | 94.8% |

The tuned **Random Forest** was selected as the final model because it achieved the strongest overall balance of performance across the evaluation metrics.

Its confusion matrix on the test set showed:

- **460** employees who left were correctly identified.
- **38** employees who left were missed.
- Only **4** employees who stayed were incorrectly classified as leaving.

### Model Validation

Additional validation was conducted to assess whether the model generalised beyond the test set:

- **Training F1-score:** 96.5%
- **Test F1-score:** 95.6%
- **5-fold cross-validation F1-score:** 94.9% ± 1.3%
- **ROC-AUC:** 0.980
- **PR-AUC:** 0.963

The consistency between training, test and cross-validation performance suggests that the model generalises well, with no substantial evidence of overfitting.

---

## Business Recommendations

The results suggest that Salifort Motors could use workforce analytics to support a more proactive employee-retention strategy.

HR could use the model as an **early-warning decision-support tool** to identify workforce groups that may warrant further investigation. Particular attention could be given to patterns involving employee satisfaction, workload, project allocation, tenure and career progression.

Rather than automatically acting on individual predictions, model outputs should be combined with employee feedback, HR expertise and managerial judgement. The identified factors should be treated as signals for investigation rather than assumed causes of employee turnover.

---

## Next Steps

Potential extensions of the project include:

- Monitor model performance as new employee data becomes available.
- Explore probability thresholds depending on the relative cost of false positives and false negatives.
- Incorporate additional employee-related variables that may improve predictive performance.
- Use explainability techniques such as SHAP to understand individual predictions.
- Investigate employee segments with elevated predicted turnover risk.
- Evaluate whether retention initiatives reduce turnover over time.

Because the model concerns employees, predictions should be used responsibly and should **not be the sole basis for employment or HR decisions**.

---

## Repository Contents

- `salifort_employee_turnover_analysis.ipynb` – Full exploratory analysis, feature engineering, modelling and model evaluation.
- `salifort_employee_turnover_executive_summary.pdf` – Executive summary of the project's findings and business recommendations.
- `salifort_employee_turnover_presentation.pptx` – Presentation of the analysis for HR and senior stakeholders.

---

## Tools & Skills

### Data Analysis
- Python
- pandas
- NumPy
- Exploratory Data Analysis
- Data Cleaning
- Data Visualisation

### Machine Learning
- Logistic Regression
- Random Forest
- XGBoost
- GridSearchCV
- Cross-validation
- Feature Importance
- Classification Metrics
- ROC-AUC / PR-AUC

### Libraries
- pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn
- XGBoost

### Business & Analytical Skills
- HR Analytics
- Employee Turnover Analysis
- Predictive Modelling
- Model Evaluation
- Translating analytical findings into business recommendations
- Communicating results to non-technical stakeholders

---

## Project Context

This project was completed as part of the **Google Advanced Data Analytics Professional Certificate** capstone project using the Salifort Motors employee dataset.

I developed the analysis from exploratory data analysis through predictive modelling and business interpretation, including comparison of Logistic Regression, tuned Random Forest and XGBoost models, followed by additional model validation and stakeholder-focused recommendations.

---

## Author

**Eric Li**

MSc Mathematical Finance | Data Analytics & Machine Learning

Interested in applying data analytics, machine learning and quantitative methods to real-world business and financial problems.
