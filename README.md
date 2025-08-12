# bank-customer-churn-prediction
Machine learning project for predicting bank customer churn using demographic and financial data. Includes exploratory data analysis, feature engineering, and model building with Decision Tree and Random Forest classifiers tuned via GridSearchCV.
# Bank Customer Churn Prediction

<p align="left">
  <img alt="Python" src="https://img.shields.io/badge/Python-3.x-blue">
  <img alt="Pandas" src="https://img.shields.io/badge/Pandas-Data%20Analysis-informational">
  <img alt="NumPy" src="https://img.shields.io/badge/NumPy-Linear%20Algebra-informational">
  <img alt="Matplotlib" src="https://img.shields.io/badge/Matplotlib-Visualization-informational">
  <img alt="Seaborn" src="https://img.shields.io/badge/Seaborn-Visualization-informational">
  <img alt="scikit-learn" src="https://img.shields.io/badge/scikit--learn-ML%20Models-orange">
  <img alt="License" src="https://img.shields.io/badge/License-MIT-green">
</p>

## 🛠 Tech Stack
- **Language:** Python  
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn  
- **Techniques:** EDA, Feature Engineering, Label Encoding, Normalization, Hyperparameter Tuning (GridSearchCV), Decision Tree, Random Forest  
- **Environment:** Jupyter Notebook

---

## 📌 Project Overview
A complete machine learning pipeline to predict **bank customer churn** using demographic and financial features.  
The goal is to surface actionable insights and build baseline models recruiters can quickly review and run.

---

## 📂 Dataset
- **Source:** Kaggle — *Churn for Bank Customers*  
- **Shape:** 10,000 rows × 14 columns  
- **Target:** `Churn` (1 = left, 0 = retained)  
- **Key Features:** Age, Geography, CreditScore, Tenure, Balance, NumOfProducts, HasCrCard, IsActiveMember, EstimatedSalary

> ⚠️ If you include the dataset in this repo, ensure the license permits redistribution. Otherwise, add instructions for downloading from Kaggle.

---

## 🔍 Exploratory Data Analysis — Highlights
- Highest churn rate in the **40–50** age band  
- **Germany** shows higher churn versus other regions  
- Churn spikes for **1** and **9** years of tenure  
- Customers with **3–4 products** churn more than those with 1–2  
- **Inactive members** are much more likely to churn

---

## ⚙️ Data Preprocessing
- Dropped non-informative IDs: `RowNumber`, `CustomerId`, `Surname`  
- No missing values in core features (per dataset)  
- Label-encoded: `Geography`, `Gender`  
- Normalized: `CreditScore`, `Balance`, `EstimatedSalary`

---

## 🤖 Models & Tuning
Two baseline models with **GridSearchCV**:
1. **Decision Tree Classifier**  
2. **Random Forest Classifier**

**Results (test set):**

| Model                    | Accuracy | Precision (Churn) | Recall (Churn) | F1 (Churn) |
|--------------------------|----------|-------------------|----------------|------------|
| Decision Tree            | 0.861    | 0.80              | 0.39           | 0.52       |
| Random Forest            | **0.868**| **0.82**          | 0.41           | 0.55       |

> Takeaway: Random Forest slightly outperforms Decision Tree and is the recommended baseline.

---

