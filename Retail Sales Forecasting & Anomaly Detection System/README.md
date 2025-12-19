# Retail Sales Forecasting & Anomaly Detection System

## 📌 Overview

This project focuses on forecasts weekly retail sales and detects abnormal sales behavior using Machine Learning. The solution is designed to support **business decision-making** such as demand planning, inventory management, and operational monitoring.

The project uses historical Walmart sales data and applies **time-aware modeling**, **feature engineering**, **model comparison**, and **anomaly detection** to deliver actionable insights.

---

## 🎯 Business Problem

Retail businesses need accurate demand forecasts to:

* Plan inventory efficiently
* Reduce stock-outs and overstocking
* Anticipate seasonal and holiday-driven demand
* Detect abnormal sales patterns caused by supply or demand shocks

This project addresses these challenges by building a robust ML-based forecasting pipeline.

---

## 🗂️ Project Structure

```
Retail-Sales-Forecasting/
│
├── forecasting_wizard.py   # Complete end-to-end ML pipeline (single file)
├── walmart_sales.csv       # Dataset
├── README.md               # Project documentation
```

The project is intentionally kept **simple and clean** to reflect real-world ML workflows.

---

## 📊 Dataset

**Source:** Walmart Sales Dataset (Kaggle)

### Columns Used

* `Store` – Store identifier
* `Date` – Weekly sales date
* `Weekly_Sales` – Target variable
* `Holiday_Flag` – Indicates holiday week
* `Temperature` – Weather factor
* `Fuel_Price` – Economic indicator
* `CPI` – Inflation metric
* `Unemployment` – Economic health indicator

These features help model **seasonal, economic, and store-level demand patterns**.

---

## ⚙️ Tech Stack

* **Language:** Python
* **Libraries:** pandas, numpy, matplotlib
* **Machine Learning:** scikit-learn
* **Models:** Linear Regression, Random Forest
* **Anomaly Detection:** Isolation Forest

---

## 🧠 Methodology

### 1. Data Preparation

* Parsed and sorted time-series data
* Created time-based features (Year, Month, Week)
* Encoded categorical store information

### 2. Modeling Strategy

* Used **time-aware train-test split** (no shuffling) to avoid data leakage
* Built a **baseline Linear Regression** model
* Improved performance using **Random Forest** to capture non-linear patterns

### 3. Evaluation Metrics

* **MAE (Mean Absolute Error)**
* **RMSE (Root Mean Squared Error)**

### 4. Anomaly Detection

* Implemented **Isolation Forest** to identify abnormal sales weeks
* Helps detect operational or demand-related issues

---

## 📈 Results

| Model             | MAE          | RMSE         |
| ----------------- | ------------ | ------------ |
| Linear Regression | ~421,000     | ~513,000     |
| Random Forest     | **~105,000** | **~191,000** |

✔ Random Forest reduced forecasting error by **~75%**, making it suitable for real-world deployment.

---

## 🏪 Store-Level Forecasting

* Built store-wise forecasting models
* Enabled location-specific demand planning
* Demonstrated scalability across multiple stores

---

## 🚨 Anomaly Detection Output

* Flagged weeks with abnormal sales behavior
* Useful for identifying:

  * Supply chain disruptions
  * Unexpected demand drops or spikes

---

## 📌 Key Business Insights

* Holiday weeks significantly impact sales volume
* Economic indicators (CPI, unemployment) influence demand
* Random Forest effectively captures complex sales patterns

---

## ▶️ How to Run

1. Clone the repository
2. Install required libraries
3. Place `walmart_sales.csv` in the project directory
4. Run:

```bash
python forecasting_wizard.py
```

## 🚀 Future Enhancements

* Streamlit dashboard for business users
* Automated retraining pipeline
* Integration with real-time sales data
