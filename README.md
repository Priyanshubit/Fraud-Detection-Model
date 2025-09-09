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

## 🚀 Results  
- **High recall** for fraud detection (catching more fraudulent cases)  
- XGBoost performed best with **balanced precision & recall**  
- Identified key fraud indicators: transaction type, amount, balance inconsistencies  

## 🔑 Key Learnings  
- Importance of **feature engineering** in fraud detection  
- Handling **imbalanced data** significantly improves recall  
- Business validation of fraud rules (large transfers flagged automatically)  

## 🖼️ Visualizations  
📊 Fraud distribution, transaction types, correlation heatmaps, and feature importance plots are included in the `notebooks/` folder.  

## 🧰 Tech Stack  
- **Python** 🐍  
- **Pandas, Numpy** (Data wrangling)  
- **Matplotlib, Seaborn** (EDA & Visualization)  
- **Scikit-learn** (ML models & evaluation)  
- **XGBoost** (Boosted tree model)  
- **Imbalanced-learn** (SMOTE handling)  

## 📌 Future Scope  
- Deploy model using **Streamlit / Flask** 🌐  
- Real-time fraud detection pipeline with **Apache Kafka** ⚡  
- Further optimization with **Deep Learning (LSTM on sequential data)**  

---

✨ If you like this project, give it a ⭐ and check out my other work!  

