# Fraud-Detection-Model
This project focuses on proactive fraud detection for a financial company using Machine Learning models.  I worked with a large-scale dataset (6.3M+ transactions, 470MB) to identify fraudulent patterns in CASH-OUT &amp; TRANSFER transactions.  


# 🚨 Fraud Detection in Financial Transactions  

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)  
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-yellow?logo=pandas)  
![Scikit-Learn](https://img.shields.io/badge/ScikitLearn-ML-orange?logo=scikit-learn)  
![XGBoost](https://img.shields.io/badge/XGBoost-Model-green)  
![Status](https://img.shields.io/badge/Status-Completed-success)  

## 📌 Project Overview  
This project focuses on **proactive fraud detection** for a financial company using **Machine Learning models**.  
We worked with a **large-scale dataset (6.3M+ transactions, 470MB)** to identify fraudulent patterns in **CASH-OUT & TRANSFER** transactions.  

## 📊 Dataset Details  
- **Steps:** Time unit (1 step = 1 hour, 744 steps = 30 days)  
- **Type:** CASH-IN, CASH-OUT, DEBIT, PAYMENT, TRANSFER  
- **Amount:** Transaction amount in local currency  
- **Balance Features:** Old & new balances for sender/receiver  
- **Fraud Flags:**  
  - `isFraud` → Fraudulent transactions (target)  
  - `isFlaggedFraud` → Transactions flagged over 200k  

📁 Dataset Source: Provided by [Accredian Case Study]  

## 🛠️ Workflow  
1. **Data Cleaning** 🧹  
   - Handled missing values & outliers  
   - Checked multicollinearity & removed redundant features  

2. **Exploratory Data Analysis (EDA)** 📈  
   - Identified fraud patterns  
   - Created new features like **balance errors**  

3. **Data Preprocessing** ⚙️  
   - Label encoding categorical features  
   - Handling class imbalance with **SMOTE**  

4. **Model Development** 🤖  
   - Logistic Regression  
   - Random Forest  
   - XGBoost (best performance)  

5. **Model Evaluation** ✅  
   - Metrics: **Precision, Recall, F1-score, ROC-AUC**  
   - Tuned thresholds to maximize **fraud recall**  

