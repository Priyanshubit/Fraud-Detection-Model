
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

## 📊 Final Workflow Summary

The fraud detection workflow was designed to handle a highly imbalanced dataset and optimize model performance while maintaining interpretability. The process began with data cleaning and feature engineering, including the creation of amount_capped, amount_log, and is_amount_outlier to address extreme transaction values and skewed distributions. Outliers were carefully analyzed and transformed rather than removed to preserve meaningful patterns in fraud behavior.

Next, the dataset was split into training and testing sets using stratified sampling to maintain the original class distribution. Given the severe class imbalance (fraud cases were <0.1% of all transactions), SMOTE (Synthetic Minority Over-sampling Technique) was applied to the training set to generate synthetic fraud examples, ensuring the model could learn fraud patterns effectively.

Categorical variables, specifically type, were encoded numerically, and the data was prepared for tree-based modeling, requiring no scaling. An XGBoost classifier was trained on the balanced dataset, taking advantage of its ability to handle large-scale imbalanced datasets and complex non-linear relationships.

Following training, model evaluation was performed using ROC-AUC, confusion matrices, precision, recall, and F1-score. Threshold tuning was then conducted to optimize the classification threshold (~0.9985) for maximizing the F1-score, striking a balance between minimizing false positives and maintaining high fraud detection rates. Comparison of the default vs. tuned thresholds highlighted the importance of this step, as false positives decreased drastically while retaining strong recall.

Finally, feature importance analysis revealed that the most predictive feature was newbalanceOrig, indicating that changes in the sender’s balance after a transaction are the primary signal for fraud detection, followed by oldbalanceOrg and transaction type. The workflow ensures a robust, explainable, and high-performing model suitable for deployment in real-world fraud detection systems.

## 📌 Future Scope  
- Deploy model using **Streamlit / Flask** 🌐  
- Real-time fraud detection pipeline with **Apache Kafka** ⚡  
- Further optimization with **Deep Learning (LSTM on sequential data)**  

---

✨ If you like this project, give it a ⭐ and check out my other work!  

