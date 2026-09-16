# 📊 Banking Fraud Analytics Dataset

## Dataset Overview

This project uses a transaction-level banking fraud dataset containing:

- **1,000,000 transactions**
- **26 columns**
- Target variable: `is_fraud`

The dataset contains transaction, customer, behavioral, risk-indicator, geographic, and fraud-related information.

## Dataset Categories

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

## Target Variable

`is_fraud` is the binary target used to identify whether a transaction is classified as fraudulent.

It is used for:

- Fraud KPI analysis
- Fraud-rate analysis
- Customer-level risk analysis
- Fraud pattern analysis
- Machine Learning classification

## Data Preparation

The project performs data-quality checks and preparation before analysis, including:

- Missing-value checks
- Duplicate-record checks
- Duplicate transaction-ID checks
- Data-type validation
- Date conversion
- Time conversion
- Negative-value checks
- Binary indicator standardization
- Fraud-type standardization
- Feature engineering

The `hour_of_day` feature is created from transaction time for time-based fraud analysis.

## Privacy & Repository Note

The raw dataset is **not included in this GitHub repository** because of its large size.

This folder contains documentation about the dataset and its structure only.

## Usage

To reproduce the analysis, obtain the dataset separately and place it in the appropriate local data directory before running:

`banking_fraud_analytics.ipynb`

Do not commit sensitive, private, or restricted financial/customer data to a public repository.

## Project Context

The dataset is analyzed using Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, and Power BI as part of the Banking Fraud Analytics & Fraud Prediction project.
