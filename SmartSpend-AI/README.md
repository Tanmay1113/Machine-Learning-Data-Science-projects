# 💰 SmartSpend AI  
Personal Finance Analysis using Machine Learning & NLP

## 🔗 Dataset
Credit Card Transactions Dataset (Kaggle)  
https://www.kaggle.com/datasets/priyamchoksi/credit-card-transactions-dataset

---

## 🧠 Project Overview
SmartSpend AI is an end-to-end machine learning project that analyzes real-world credit card transactions to automatically categorize spending, detect unusual transactions, and forecast monthly expenses.

This project demonstrates practical applications of **NLP, anomaly detection, and time-series analysis** using real financial data.

---

## 🚀 Features

### 🔹 Transaction Categorization (NLP)
- Cleaned raw transaction descriptions
- Applied **TF-IDF Vectorization**
- Trained **Logistic Regression**
- Achieved **~98% classification accuracy**

### 🔹 Unusual Spending Detection
- Used **Isolation Forest (Unsupervised ML)**
- Features: transaction **Amount + Merchant Frequency**
- Detected rare and high-risk spending patterns

### 🔹 Monthly Expense Forecasting
- Aggregated monthly transaction amounts
- Predicted next month’s spending using regression
- Visualized monthly spending trends

---

## 🛠 Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn
- NLP (TF-IDF)
- Matplotlib
- Google Colab / Jupyter Notebook

---

## 📁 Dataset Columns Used
- `trans_date_trans_time` → Date  
- `merchant` → Transaction Description  
- `amt` → Amount  
- `category` → Spending Category  

Additional dataset columns were ignored for this project.

---

## 📊 Results
- **Transaction Categorization Accuracy:** ~98%
- **Unusual Transactions:** Successfully identified high-risk and rare spending
- **Forecasting:** Predicted next month’s total spending

---

## ▶️ How to Run

```bash
pip install pandas numpy scikit-learn matplotlib
python smartspend_ai.py
