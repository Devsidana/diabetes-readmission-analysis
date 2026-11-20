# Diabetes 130-US Hospitals — Readmission Analysis

## Project Overview

This project analyzes the Diabetes 130-US Hospitals dataset (1999–2008) to explore patterns associated with hospital readmission among diabetic patients.

The project uses Python for data cleaning, exploratory data analysis, visualization, feature preparation, and a basic machine learning classification model to predict readmission within 30 days.

## Project Objectives

* Understand and clean hospital admission data.
* Explore patient demographics, hospitalization, diagnoses, and treatment patterns.
* Analyze factors associated with hospital readmission.
* Build a classification model to predict readmission within 30 days.
* Evaluate model performance.
* Communicate findings through visualizations, insights, and recommendations.

## Tools & Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* JupyterLab

## Dataset

**Dataset:** Diabetes 130-US Hospitals for Years 1999–2008

**Source:** UCI Machine Learning Repository

The dataset contains 101,766 hospital encounter records from 130 US hospitals and integrated delivery networks.

It includes demographic information, hospitalization details, diagnoses, laboratory tests, medications, and readmission outcomes.

**Dataset source:** https://archive.ics.uci.edu/dataset/296/diabetes-130-us-hospitals-for-years-1999-2008

## Project Workflow

1. Data Loading
2. Data Understanding
3. Data Cleaning
4. Missing Value Analysis
5. Exploratory Data Analysis (EDA)
6. Feature Preparation
7. Train-Test Splitting
8. Data Preprocessing
9. Logistic Regression
10. Model Evaluation
11. Business Insights
12. Recommendations and Conclusion

## Target Variable

A binary target variable named `readmitted_30d` was created.

* **1:** Patient was readmitted within 30 days.
* **0:** Patient was not readmitted within 30 days. This includes the original `NO` and `>30` categories.

The positive class represents approximately 11.16% of hospital encounters.

## Machine Learning Model

**Algorithm:** Logistic Regression

The dataset was divided into training and testing sets using GroupShuffleSplit at the patient level to prevent the same patient from appearing in both sets.

The model used:

* Numerical preprocessing: Median imputation and StandardScaler.
* Categorical preprocessing: Missing-value imputation and OneHotEncoder.
* Class weighting: `balanced` to account for class imbalance.

## Model Evaluation Results

| Evaluation Metric | Result |
| ----------------- | -----: |
| Accuracy          | 65.64% |
| Precision         | 16.70% |
| Recall            | 55.65% |
| F1-score          | 25.69% |
| ROC-AUC           |  0.656 |

The model identified approximately 55.65% of actual readmissions within 30 days. However, its low precision indicates a considerable number of false-positive predictions.

Overall, the model showed limited predictive performance and would require further validation and improvement before any practical application.

## Key Business Insights

* Approximately 11.16% of encounters resulted in readmission within 30 days.
* Readmission patterns varied across patient and hospitalization characteristics.
* Previous inpatient and emergency visits showed associations with 30-day readmission.
* The analysis highlighted the importance of examining hospital utilization and discharge-related patterns.

## Business Recommendations

* Review hospital encounters involving patients with previous inpatient and emergency visits.
* Examine discharge planning and post-discharge follow-up processes.
* Monitor readmission patterns across patient groups.
* Further validate predictive models before considering operational use.

## Project Limitations

* The dataset contains historical records from 1999–2008.
* The target classes are imbalanced.
* The Logistic Regression model achieved relatively low precision and limited ROC-AUC.
* The analysis identifies associations, not causal relationships.
* The findings may not represent current healthcare practices or other populations.

## Conclusion

This project provided practical experience in data cleaning, exploratory data analysis, visualization, feature engineering, machine learning, and model evaluation.

It explored patterns associated with hospital readmission and demonstrated how analytical findings can be translated into business insights and recommendations.

The results also highlighted the limitations of predictive modelling and the importance of careful evaluation before applying models in real-world healthcare settings.

## Author

**Diabetes Readmission Analysis Project**
