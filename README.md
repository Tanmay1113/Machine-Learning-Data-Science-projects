# Machine-Learning-Data-Science-projects

dataset Link = https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

Here is a **clean, professional, copy-paste ready README.md** for your **Real-Time Fraud Detection (FinTech)** project.
This is **resume + recruiter friendly**.

---

# 🏦 Real-Time Credit Card Fraud Detection System

## 📌 Problem Statement

Credit card fraud causes significant financial losses to banks and payment companies.
The challenge is detecting **rare fraudulent transactions (<1%)** in **real time**, while balancing:

* Catching as many frauds as possible (**high recall**)
* Avoiding unnecessary blocking of genuine users

---

## 🎯 Project Objective

Build a **real-time fraud detection system** that:

* Handles highly imbalanced data
* Prioritizes **recall** over accuracy
* Simulates live transaction processing
* Is deployable as an API for production use

---

## 🧠 Solution Overview

* Used **Random Forest** for fraud classification on tabular data
* Applied **SMOTE** to handle severe class imbalance
* Tuned decision threshold to improve fraud recall
* Simulated **real-time transaction streaming**
* Wrapped the model using **FastAPI** for production-ready inference

---

## 🛠️ Tech Stack

* **Language:** Python
* **Data Handling:** Pandas, NumPy
* **Machine Learning:** Scikit-learn
* **Imbalance Handling:** SMOTE (imbalanced-learn)
* **Model Deployment:** FastAPI
* **Model Persistence:** joblib

---

## 📂 Dataset

* **Source:** Kaggle – Credit Card Fraud Detection Dataset
* **Note:** Dataset not included due to large file size

Target Variable:

* `0` → Legit transaction
* `1` → Fraudulent transaction

---

## 📊 Model Performance

### 🔹 Baseline (Default Threshold = 0.5)

* Fraud Recall: **~76%**
* High precision but missed several fraud cases

### 🔹 Final Model (Threshold Tuned to 0.3)

* Fraud Recall: **~90%**
* Precision slightly reduced (acceptable trade-off)
* Better suited for real-world fraud detection

> **Accuracy is intentionally not used as a key metric due to extreme class imbalance.**

---

## ⏱️ Real-Time Simulation

* Transactions are processed **one by one**
* Each transaction is instantly classified as:

  * `BLOCK` (fraud)
  * `ALLOW` (legitimate)
* Mimics how payment systems work in production

---

## 🌐 API Deployment (FastAPI)

* Model inference is exposed via a REST API
* Accepts transaction features as input
* Returns fraud probability and decision

### Run Locally:

```bash
uvicorn fraud_detection_all_in_one:app --reload
```

> ⚠️ FastAPI server is not started inside Google Colab due to asyncio limitations.
> API logic is tested directly in Colab and deployed locally.

---

## 📁 Project Structure

```
Real-Time-Fraud-Detection/
├── fraud_detection_all_in_one.py
├── fraud_model.pkl
├── README.md
├── requirements.txt
```

---

## 🚀 Key Learnings

* Handling extreme class imbalance in financial data
* Importance of **recall vs precision trade-off**
* Threshold tuning for business-critical ML systems
* Real-time ML inference design
* Production-ready ML deployment concepts

---

## 💡 Future Improvements

* Isolation Forest for anomaly detection
* SHAP explanations for fraud decisions
* Cost-based evaluation (financial loss vs false positives)
* Dockerized deployment

---

## 👤 Author

**Tanmay Manoj Bhole**
B.Sc. IT | Data Science & Machine Learning Enthusiast

---

### ⭐ If you find this project useful, consider giving it a star!
