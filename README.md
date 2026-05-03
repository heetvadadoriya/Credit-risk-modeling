# 📊 Credit Risk Modeling – Bank GoodCredit

## 🚀 Overview
This project builds an end-to-end machine learning pipeline to predict customer credit default risk and support better lending decisions.

---

## 🎯 Business Objective
- Identify high-risk customers before credit approval  
- Reduce financial losses due to defaults  
- Improve credit portfolio quality  

---

## 📂 Dataset
The dataset consists of:
- Customer Account Data (payment behavior, balances)
- Customer Enquiry Data (credit enquiry patterns)
- Customer Demographics (customer-level attributes)

Target Variable:
- **Bad_label** (0 = Good, 1 = Default)

---

## ⚙️ Workflow

### 1. Data Preprocessing
- Removed high-missing columns (>70%)
- Handled missing values (median/mode)
- Dropped irrelevant fields (customer_no)

### 2. Feature Engineering
- account_age_days  
- days_since_last_payment  
- days_since_enquiry  
- payment_duration  

### 3. Handling Imbalance
- Applied SMOTE and class weighting  

### 4. Modeling
- Logistic Regression (baseline)
- Random Forest (final model)
- XGBoost (comparison)

---

## 📈 Model Performance

| Model | ROC-AUC | Gini |
|------|--------|------|
| Logistic Regression | Low | Negative |
| Random Forest | **0.63** | **0.26 (Best)** |
| XGBoost | 0.61 | 0.23 |

---

## 📊 Decile Analysis
- Validates model’s ability to rank customers by risk  
- Higher deciles contain higher default rates  

---

## 💼 Business Impact
- Enables identification of high-risk customers  
- Supports better credit approval decisions  
- Reduces potential default losses  

---

## 🛠️ Tech Stack
- Python (Pandas, NumPy)
- Scikit-learn
- XGBoost
- Power BI

---

## 🚀 How to Run

```bash
pip install -r requirements.txt
