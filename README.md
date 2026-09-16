 # 🏦 Banking Fraud Analytics & Fraud Prediction

An end-to-end Banking Fraud Analytics and Fraud Prediction project using Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn and Power BI.

The project analyzes 1,000,000 banking transactions to identify fraud patterns, customer-level risk, unusual transaction behavior and potential risk signals.

## 📌 Business Problem

Banks process a very large number of transactions every day. Manually identifying suspicious transactions and unusual customer behavior is difficult.

This project uses transaction data to understand:

- Where fraud is occurring
- Which transaction characteristics are associated with higher fraud activity
- How fraud varies across customers and business dimensions
- Which transactions show unusual behavior
- How analytics and machine learning can support fraud monitoring

## 🎯 Objectives

- Perform data understanding and quality checks
- Clean and prepare transaction data
- Calculate fraud KPIs
- Analyze customer-level fraud behavior
- Detect unusual transactions using the 3-Sigma method
- Analyze fraud by country, city, merchant, payment method and device
- Analyze fraud by transaction time and risk indicators
- Create business-focused visualizations
- Generate actionable business recommendations
- Build a Logistic Regression fraud prediction model
- Evaluate the classification model
- Present insights through a Power BI dashboard

## 📊 Dataset

Dataset size: 1,000,000 rows × 26 columns

Target variable: `is_fraud`

### Main data categories

#### Transaction

- `transaction_id`
- `transaction_date`
- `transaction_time`
- `transaction_amount`

#### Customer

- `customer_id`
- `customer_age`
- `credit_score`
- `account_age_years`
- `account_balance`

#### Behavior

- `distance_from_home_km`
- `num_prev_transactions`
- `transaction_freq_monthly`
- `time_since_last_txn_hrs`
- `failed_attempts`

#### Risk indicators

- `is_international`
- `is_weekend`
- `is_night_transaction`
- `pin_changed_recently`

#### Fraud

- `is_fraud`
- `fraud_type`

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Data analysis |
| Pandas | Data manipulation |
| NumPy | Numerical analysis |
| Matplotlib | Visualization |
| Seaborn | Statistical visualization |
| Scikit-learn | Machine learning |
| Jupyter Notebook | Analysis environment |
| Power BI | Interactive dashboard |

## 🔄 End-to-End Workflow

Data Loading → Data Understanding → Data Quality Checks → Data Cleaning → Fraud KPI Analysis → Customer Risk Analysis → 3-Sigma Outlier Analysis → Fraud Pattern Analysis → Visualization → Business Insights → Business Recommendations → Machine Learning Prediction

# 1. Data Loading & Initial Inspection

The banking transaction dataset was loaded using Pandas.

Initial inspection included:

- Dataset shape
- First records
- Random sample
- Last records
- Data types
- Statistical summary
- Unique values

# 2. Data Cleaning

Before analysis, the dataset was checked for data-quality issues.

### Missing Values

Missing values were identified using column-wise null counts.

### Duplicate Records

Both complete duplicate rows and duplicate transaction IDs were checked.

Repeated categorical values such as country, merchant category and payment method were not treated as duplicate records.

### Data Types

Data types were reviewed before analysis.

### Negative Values

Numerical columns were checked for unexpected negative values.

### Date & Time Conversion

`transaction_date` was converted to datetime.

`transaction_time` was converted using the expected time format.

An additional feature was created:

`hour_of_day`

This feature was later used for hourly fraud analysis.

### Binary Columns

The following binary fields were cleaned into numeric 0/1 values:

- `is_weekend`
- `is_night_transaction`
- `is_international`
- `pin_changed_recently`
- `is_fraud`

### Fraud Type Cleaning

Missing fraud types were replaced with `No Fraud`.

Non-fraud transactions were also assigned `No Fraud` to maintain consistent labeling.

# 3. Outlier Handling Strategy

Outliers were not automatically removed.

In fraud analytics, an unusual transaction can itself be an important signal.

Therefore, unusual observations were analyzed separately using the 3-Sigma method.

Lower Limit = Mean - 3 × Standard Deviation

Upper Limit = Mean + 3 × Standard Deviation

A statistical outlier does not automatically mean fraud.

# 4. Customer Risk Analysis

Customer-level aggregation was performed using:

- Total transactions
- Total transaction amount
- Average transaction amount
- Fraud transaction count
- Fraud rate

This helps identify customers with repeated fraudulent activity or unusual transaction behavior.

The analysis also considers transaction volume so that a high fraud rate based on very few transactions is not interpreted in isolation.

# 5. 3-Sigma Outlier Analysis

The 3-Sigma method was applied to selected behavioral variables.

### Variables analyzed

- Transaction Amount
- Distance from Home
- Transaction Frequency
- Previous Transactions

For each variable, unusual observations were compared with normal observations using fraud rate.

### Business Interpretation

The purpose was not simply to remove outliers.

Instead, the analysis asks:

> Do statistically unusual transactions show different fraud behavior from normal transactions?

This makes the outlier analysis relevant to fraud detection.

# 6. Fraud Pattern Analysis

Fraud rate was analyzed across multiple business dimensions.

### Merchant Category

Fraud rates were calculated for each merchant category.

Observed higher-rate categories included:

- ATM Withdrawal — ~8.74%
- Jewelry — ~8.70%
- Crypto Exchange — ~8.65%

### Payment Method

Fraud rates were compared across payment methods.

Observed values included:

- Cheque — ~5.67%
- Credit Card — ~5.60%
- Bank Transfer — ~5.51%
- Crypto — ~5.50%
- Mobile Payment — ~5.49%
- Debit Card — ~5.46%

### Country

Fraud rates were calculated for each country.

The highest observed country-level rate was:

- Brazil — ~5.67%

Country-level rates were otherwise relatively close.

### City

City-level fraud rates were calculated and the top cities were examined for potential geographic patterns.

### Device Type

Fraud rates were compared across device types.

### Fraud Type

Fraudulent transactions were filtered using `is_fraud = 1` and their fraud-type distribution was analyzed.

# 7. Fraud by Transaction Hour

The `hour_of_day` feature was created from transaction time.

Fraud rate was calculated for every hour.

### Key Finding

The highest observed hourly fraud rate was approximately:

**6 AM — ~8.07%**

Several midnight and early-morning hours also showed elevated fraud rates.

Transaction time can therefore be used as one additional risk signal.

# 8. Night, International & Weekend Analysis

## 🌙 Night Transactions

| Transaction Type | Fraud Rate |
|---|---:|
| Non-Night | ~4.07% |
| Night | ~7.96% |

Night transactions showed substantially higher fraud activity in this dataset.

## ✈️ International Transactions

| Transaction Type | Fraud Rate |
|---|---:|
| Non-International | ~4.76% |
| International | ~9.86% |

International transactions showed approximately 2× higher fraud activity than non-international transactions in this dataset.

## 📅 Weekend Transactions

| Transaction Type | Fraud Rate |
|---|---:|
| Non-Weekend | ~5.51% |
| Weekend | ~5.57% |

The difference is very small, suggesting that weekend status alone provides limited fraud-detection value in this dataset.

# 9. Fraud KPIs

The project calculates key fraud-monitoring metrics:

- Total Transactions
- Fraud Transactions
- Non-Fraud Transactions
- Fraud Rate
- Total Fraud Amount
- Average Fraud Transaction Amount
- Fraud Customers

These KPIs provide an overall view of fraud activity.

# 10. Data Visualization

The notebook contains business-focused visualizations including:

- Fraud vs Non-Fraud Transactions
- Top Countries by Fraud Rate
- Top Merchant Categories by Fraud Rate
- Fraud Rate by Hour
- Fraud Type Distribution
- Transaction Amount: Fraud vs Non-Fraud
- Distance from Home: Fraud vs Non-Fraud

# 11. Key Business Insights

## 1. International Transactions

International transactions had approximately 9.86% fraud, compared with 4.76% for non-international transactions.

**Business implication:** International transactions can receive additional verification or risk scoring, especially when combined with other suspicious signals.

## 2. Night Transactions

Night transactions had approximately 7.96% fraud, compared with 4.07% for non-night transactions.

**Business implication:** Time-based monitoring can be combined with transaction amount, location and customer behavior.

## 3. High-Risk Merchant Categories

ATM Withdrawal, Jewelry and Crypto Exchange showed the highest observed merchant-level fraud rates.

**Business implication:** These categories can receive enhanced monitoring when multiple risk indicators are present.

## 4. Early-Morning Activity

The highest observed hourly fraud rate was approximately 8.07% at 6 AM.

**Business implication:** Transaction time can be used as one component of a risk-based monitoring system.

## 5. Payment Method

Cheque and Credit Card showed the highest observed payment-method fraud rates, but the differences were relatively small.

**Business implication:** Payment method should not be used as a standalone fraud rule.

## 6. Weekend Status

Weekend and non-weekend fraud rates were very similar.

**Business implication:** Weekend status should be combined with stronger risk indicators.

## 7. Customer-Level Monitoring

Customer-level fraud frequency, fraud rate and transaction volume can be used together to identify repeated suspicious behavior.

# 12. Risk-Based Fraud Monitoring

The analysis supports a multi-signal approach rather than relying on a single attribute.

High Transaction Amount + International Transaction + Night Transaction + High-Risk Merchant + Failed Attempts + Unusual Customer Behavior

↓

Higher Priority for Review

The purpose is to prioritize suspicious transactions for further investigation.

# 13. Business Recommendations

## 1. International Transaction Monitoring

Apply additional verification or risk scoring to international transactions.

## 2. High-Risk Merchant Monitoring

Prioritize monitoring for ATM Withdrawal, Jewelry and Crypto Exchange transactions when other risk indicators are also present.

## 3. Time-Based Monitoring

Increase monitoring during higher-risk hours identified through hourly analysis.

## 4. Customer-Level Risk Monitoring

Monitor repeated fraud activity while considering transaction volume.

## 5. Unusual Behavior Detection

Use 3-Sigma analysis as an additional signal for unusual transaction behavior.

## 6. Multiple Risk Signals

Combine transaction amount, international status, night activity, merchant category, failed attempts and customer behavior.

## 7. ML as Decision Support

Use the machine learning model as an additional risk-scoring layer rather than as the only decision-making mechanism.

# 14. Machine Learning — Fraud Prediction

A Logistic Regression classification model was built to estimate whether a transaction is fraudulent.

### Selected Features

- `transaction_amount`
- `hour_of_day`
- `distance_from_home_km`
- `num_prev_transactions`
- `transaction_freq_monthly`
- `failed_attempts`
- `account_balance`
- `is_weekend`
- `is_night_transaction`
- `is_international`
- `pin_changed_recently`

### Target

`is_fraud`

### Train-Test Split

- 80% training data
- 20% testing data
- `random_state = 42`
- Stratified split

### Model

Logistic Regression

Configured with:

- `max_iter = 1000`
- `class_weight = "balanced"`

# 15. Model Evaluation

The model was evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Classification Report
- Confusion Matrix

For fraud detection, Accuracy should not be considered alone.

Precision and Recall are particularly important because both false positives and missed fraud have business consequences.

Actual model metric values should be taken from the executed notebook output rather than assumed.

# 16. Power BI Dashboard

The cleaned dataset can be exported for Power BI:

```python
df_transactions.to_csv(
    "bank_fraud_cleaned.csv",
    index=False
)
