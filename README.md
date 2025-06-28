# 💳 Anomaly Detection in Financial Transactions

This project implements machine learning models to detect **anomalies (fraudulent or irregular transactions)** in synthetic financial transaction data. The goal is to identify risky behavior for applications in **audit risk assessment**, **compliance monitoring**, and **fraud prevention**.


---

## 🧠 Problem Statement

In financial systems, fraudulent or risky transactions are rare but costly. This project applies both **unsupervised** and **supervised** learning techniques to:

* Detect abnormal patterns
* Reduce false positives
* Improve audit efficiency

---

## 🧪 Dataset

A synthetic dataset was generated using Python libraries like `faker` to simulate real-world features:

* `amount` (transaction value)
* `device_type` (Mobile, POS, Web, etc.)
* `transaction_type` (Withdrawal, Transfer, Purchase)
* `hour`, `day_of_week` (temporal features)
* `is_anomaly` (target label)

Class balance: \~3% anomalies, 97% normal

---

## 🔍 Exploratory Data Analysis (EDA)

* Univariate and bivariate distributions
* Class imbalance visualization
* Boxplots and histograms for `amount`
* Frequency plots for device/time patterns

---

## 🧪 Models Trained

### ✅ 1. Isolation Forest (Unsupervised)

* Trained with expected contamination (3%)
* Very high recall on anomalies

**Performance:**

```
Precision: 0.59
Recall:    1.00
F1-Score:  0.74
Accuracy:  98%
ROC AUC:   0.989
```

**Confusion Matrix:**

```
[[1898   42]
 [   0   60]]
```

---

### ✅ 2. Logistic Regression (Supervised)

* Trained on labeled dataset
* Extremely high performance due to clean data

**Performance:**

```
Accuracy:  100%
Precision: 1.00
Recall:    1.00
F1-Score:  1.00
ROC AUC:   1.00
```

---

## 🛠️ Tech Stack

* Python
* pandas, scikit-learn, seaborn, matplotlib
* Streamlit (optional for dashboard)
* Faker (synthetic data)

---

## 🚀 How to Run the Project

### ▶️ Run the Notebook

```bash
jupyter notebook notebooks/eda_and_modeling.ipynb
```

## 💡 Future Improvements

* Add user-based features (e.g., transaction velocity)
* Try Autoencoders and XGBoost
* Build alert system & dashboard for audit teams
* Deploy as a REST API

---

## 🙋 Author

Kealeboga Khumalo — Final year BSc Mathematics & Computer Science student passionate about Data Science and Financial Applications.

---
