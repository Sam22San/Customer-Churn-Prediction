# Customer Churn Prediction

As part of my Master’s degree in Data Science at the Faculty of Graduate Studies for Statistical Research (FGSSR) – Cairo University, during my complementary semester in the Practical Machine Learning course, taught and supervised by Dr. Nermeen and teaching assistant Salma.
This project is the final assignment for the Machine Learning course.

---

## Project Overview

This project aims to build a predictive system that identifies customers likely to churn (leave a subscription service) and supports businesses in designing intelligent retention strategies using machine learning. By analyzing customer data, the system helps reduce churn and improve customer loyalty.

---

## Team Members

- Nourhan Khaled  
- Fatimah Ehab  
- Hend Labib  
- Mona Elgoba  
- Mayar Mustafa  

---

## Dataset Description

**Target Variable:**  
- `Churn` — customers who left within the last month.

**Features:**  
- Services: phone, multiple lines, internet, online security, online backup, device protection, tech support, streaming TV/movies  
- Account info: tenure, contract, payment method, paperless billing, monthly charges, total charges  
- Demographics: gender, age range, partners, dependents

---

## Exploratory Data Analysis (EDA)

- Imbalanced data with fewer churners  
- Tenure distribution is bimodal (early churn or loyal customers)  
- Monthly charges skewed right (mostly low-cost plans)

---

## Project Pipeline

- **Data Preprocessing:**  
  - Handled missing values and duplicates  
  - Encoded categorical variables (OneHotEncoder)  
  - Scaled numeric features using RobustScaler and MinMaxScaler  
  - Feature selection based on correlation and model relevance:  
    - Dropped `gender` and `phone_service` (weak correlation)  
    - Excluded `total_charges` for linear models to avoid redundancy; retained for tree-based models

- **Imbalance Handling:** SMOTE oversampling during training  
- **Models Trained:** Logistic Regression, XGBoost, LightGBM, Stacking Classifier  
- **Evaluation:** Precision, Recall, F1-Score  
- **Deployment:** Gradio app with LLM-powered personalized retention offers

## Deployment

Try the system live through Gradio (link provided in the notebook or deployment instructions).

---
