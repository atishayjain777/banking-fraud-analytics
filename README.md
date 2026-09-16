# 🏦 Banking Fraud Analytics & Fraud Prediction

An end-to-end **Banking Fraud Analytics and Fraud Prediction** project using **Python, Statistical Analysis, Machine Learning, and Power BI** to analyze transaction-level fraud patterns, identify customer risk, and generate business-focused insights.

The project analyzes **1,000,000 banking transactions across 26 columns** covering transaction details, customer behavior, geography, merchant categories, payment methods, and fraud indicators.

---

## 📌 Project Overview

Financial institutions process a large number of transactions every day. Identifying suspicious transactions manually can be difficult because fraud patterns may vary across customers, locations, transaction types, merchant categories, payment methods, and transaction times.

This project uses data analytics and machine learning to investigate transaction behavior and identify potential fraud risk signals.

### The analysis focuses on:

- Fraud transaction patterns
- Customer-level fraud behavior
- Merchant category risk
- Payment method patterns
- Geographic patterns
- Transaction timing
- Night-time activity
- International transactions
- Weekend activity
- Unusual transaction behavior
- Machine Learning-based fraud prediction
- Interactive Power BI reporting

---

# 🎯 Business Objectives

The project was developed to:

1. Understand and validate a large banking transaction dataset.
2. Perform data quality checks.
3. Clean and prepare transaction data.
4. Create fraud-related KPIs.
5. Analyze fraud across multiple business dimensions.
6. Analyze customer-level fraud behavior.
7. Identify unusual transactions using the 3-Sigma method.
8. Analyze fraud across merchant categories and payment methods.
9. Analyze geographical and device-related patterns.
10. Analyze fraud by transaction hour.
11. Compare night and non-night transactions.
12. Compare international and non-international transactions.
13. Compare weekend and non-weekend transactions.
14. Identify important fraud risk signals.
15. Build a Logistic Regression fraud prediction model.
16. Evaluate the Machine Learning model using multiple metrics.
17. Build an interactive Power BI dashboard.
18. Translate analytical findings into business recommendations.

---

# 📊 Dataset

## Dataset Size

- **1,000,000 rows**
- **26 columns**
- Target variable: `is_fraud`

## Data Categories

### Transaction Information

- `transaction_id`
- `transaction_date`
- `transaction_time`
- `transaction_amount`
- `merchant_category`
- `payment_method`

### Customer Information

- `customer_id`
- `customer_age`
- `credit_score`
- `account_age_years`
- `account_balance`

### Behavioral Information

- `distance_from_home_km`
- `num_prev_transactions`
- `transaction_freq_monthly`
- `time_since_last_txn_hrs`
- `failed_attempts`

### Risk Indicators

- `is_international`
- `is_weekend`
- `is_night_transaction`
- `pin_changed_recently`

### Fraud Information

- `is_fraud`
- `fraud_type`

---

# 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Data analysis and processing |
| Pandas | Data manipulation |
| NumPy | Numerical analysis |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Scikit-learn | Machine Learning |
| Jupyter Notebook | Analysis environment |
| Power BI | Interactive dashboard |

---

# 🔄 Project Workflow

The project follows a complete end-to-end data analytics workflow:

```text
📥 Data Loading
      ↓
🧹 Data Quality & Cleaning
      ↓
⚙️ Feature Engineering
      ↓
🔎 Exploratory Data Analysis (EDA)
      ↓
📐 3-Sigma Outlier Analysis
      ↓
👤 Customer Analysis
      ↓
🚨 Fraud Analysis
      ↓
🤖 Machine Learning
      ↓
📊 Power BI Dashboard
      ↓
💡 Business Insights & Recommendations
