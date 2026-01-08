## Project Title
Cardiovascular Disease Risk Prediction Using Logistic Regression.

## Introduction

Cardiovascular diseases (CVDs) remain one of the leading causes of death worldwide. According to the World Health Organization, approximately **12 million deaths occur globally each year due to heart-related diseases**, with a significant proportion occurring in developed countries.
Early identification of individuals at high risk of coronary heart disease (CHD) enables preventive interventions such as lifestyle modification and timely medical care. This project applies **predictive modelling techniques**, specifically **logistic regression**, to estimate a patient’s **10-year risk of coronary heart disease** using demographic, behavioural, and medical risk factors.

## Project Objective

The objectives of this project are to:
* Perform exploratory data analysis (EDA) to understand cardiovascular risk factors.
* Build a **logistic regression model** to predict 10-year CHD risk.
* Select the **most appropriate classification metric** for this healthcare problem.
* Determine the **optimal decision threshold** and justify its selection.
* Provide actionable insights based on model performance and feature importance.
* 
## Dataset Description

### Source
The dataset is publicly available on **Kaggle** and originates from an ongoing cardiovascular study conducted on residents of **Framingham, Massachusetts**.
Dataset link:
[https://www.kaggle.com/datasets/christofel04/cardiovascular-study-dataset-predict-heart-disea?select=train.csv](https://www.kaggle.com/datasets/christofel04/cardiovascular-study-dataset-predict-heart-disea?select=train.csv)

### Files Used
* **train.csv** – Primary dataset used for modelling
* **Module_4_sprint_4.ipynb** – Jupyter Notebook containing data cleaning, preprocessing, modelling, and evaluation

### Dataset Overview
* Number of records: 3,390
* Number of features: 15
* Target variable: 10-year risk of coronary heart disease (binary)

## Variables

### Demographic

* **Sex** – Male or Female
* **Age** – Patient age (continuous)

### Behavioural

* **Is_smoking** – Current smoker (Yes/No)
* **Cigs Per Day** – Average number of cigarettes smoked per day

### Medical History

* **BP Meds** – On blood pressure medication
* **Prevalent Stroke** – History of stroke
* **Prevalent Hyp** – Hypertension status
* **Diabetes** – Diabetes diagnosis

### Current Medical Measurements

* **Tot Chol** – Total cholesterol
* **Sys BP** – Systolic blood pressure
* **Dia BP** – Diastolic blood pressure
* **BMI** – Body Mass Index
* **Heart Rate** – Heart rate
* **Glucose** – Blood glucose level

### Target Variable

* **TenYearCHD** – 10-year risk of CHD
  * `1` = Yes
  * `0` = No

## Methodology

### 1. Data Cleaning & Preprocessing

* Handling missing values using appropriate imputation strategies.
* Encoding categorical variables.
* Feature scaling for numerical variables where required.
* Checking class imbalance in the target variable.

### 2. Exploratory Data Analysis (EDA)

* Distribution analysis of risk factors.
* Visualisation of relationships between predictors and CHD risk.
* Identification of key contributing variables.

### 3. Model Development

* Logistic regression selected due to:

  * Binary classification nature of the target variable.
  * Interpretability of coefficients in a healthcare context.
* Feature selection guided by domain relevance and statistical significance.

### 4. Model Evaluation

* Evaluation metrics considered:

  * Accuracy
  * Precision
  * Recall
  * F1-score
  * ROC-AUC
* **Primary metric selected:** ROC-AUC / Recall (depending on your notebook outcome), justified by the higher cost of false negatives in healthcare.

### 5. Threshold Optimisation

* The optimal classification threshold was determined using:

  * ROC curve analysis
  * Precision–Recall trade-offs
* The chosen threshold balances sensitivity and specificity, prioritising early detection of high-risk patients.

## Key Findings

* Age, systolic blood pressure, cholesterol level, smoking status, and diabetes were among the strongest predictors of CHD risk.
* Logistic regression provided an interpretable and effective baseline model.
* Adjusting the classification threshold improved the model’s ability to identify high-risk patients.
* Using recall-oriented evaluation ensures fewer high-risk patients are missed.

## Conclusion

This analysis demonstrates that logistic regression is a suitable and interpretable approach for predicting long-term coronary heart disease risk. By carefully selecting evaluation metrics and optimising the decision threshold, the model provides **clinically meaningful predictions** that support preventive healthcare decision-making.

Just tell me how you want to use it 👌
