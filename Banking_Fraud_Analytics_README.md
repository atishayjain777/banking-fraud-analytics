# 🏦 Banking Fraud Analytics & Fraud Prediction

An end-to-end **Banking Fraud Analytics and Fraud Prediction** project using **Python, Statistical Analysis, Machine Learning, and Power BI** to analyze transaction-level fraud patterns, identify customer risk, investigate unusual behavior, and generate business-focused insights.

The project analyzes **1,000,000 banking transactions across 26 columns** covering transaction details, customer information, behavioral attributes, risk indicators, merchant categories, payment methods, geography, and fraud labels.

---

## 📌 Table of Contents

1. [Project Overview](#-project-overview)
2. [Business Problem](#-business-problem)
3. [Business Objectives](#-business-objectives)
4. [Dataset](#-dataset)
5. [Feature Categories](#-feature-categories)
6. [Tech Stack](#-tech-stack)
7. [End-to-End Workflow](#-end-to-end-workflow)
8. [Data Loading & Initial Inspection](#1--data-loading--initial-inspection)
9. [Data Quality & Cleaning](#2--data-quality--cleaning)
10. [Feature Engineering](#3--feature-engineering)
11. [Exploratory Data Analysis](#4--exploratory-data-analysis)
12. [Fraud KPI Analysis](#5--fraud-kpi-analysis)
13. [3-Sigma Outlier Analysis](#6--3-sigma-outlier-analysis)
14. [Customer-Level Risk Analysis](#7--customer-level-risk-analysis)
15. [Fraud Pattern Analysis](#8--fraud-pattern-analysis)
16. [Geographical Analysis](#9--geographical-analysis)
17. [Transaction Timing Analysis](#10--transaction-timing-analysis)
18. [Risk Indicator Analysis](#11--risk-indicator-analysis)
19. [Key Business Findings](#12--key-business-findings)
20. [Fraud Risk Signals](#13--fraud-risk-signals)
21. [Machine Learning](#14--machine-learning)
22. [Model Evaluation](#15--model-evaluation)
23. [Power BI Dashboard](#16--power-bi-dashboard)
24. [Business Recommendations](#17--business-recommendations)
25. [Analytical Value](#18--analytical-value)
26. [Limitations](#19--limitations)
27. [Future Improvements](#20--future-improvements)
28. [Project Structure](#21--project-structure)
29. [How to Run](#22--how-to-run)
30. [Requirements](#23--requirements)
31. [Skills Demonstrated](#24--skills-demonstrated)
32. [Resume Project Description](#25--resume-project-description)
33. [Project Takeaways](#26--project-takeaways)
34. [Conclusion](#27--conclusion)

---

## 📌 Project Overview

Financial institutions process a very large number of transactions every day.

Because transaction volumes are high, manually reviewing every transaction for suspicious behavior is not practical. Fraud patterns can also vary by customer, merchant category, payment method, location, transaction time, and behavioral characteristics.

This project applies a complete analytical workflow to understand those patterns.

The project moves from:

```text
Raw Transaction Data
        ↓
Data Loading
        ↓
Data Quality & Cleaning
        ↓
Feature Engineering
        ↓
Exploratory Data Analysis
        ↓
Fraud KPI Analysis
        ↓
3-Sigma Outlier Analysis
        ↓
Customer Risk Analysis
        ↓
Fraud Pattern Analysis
        ↓
Business Insights
        ↓
Machine Learning
        ↓
Power BI Dashboard
        ↓
Business Recommendations
```

The analysis focuses on identifying **observed relationships and risk signals** rather than treating any single characteristic as proof of fraud.

---

## 📌 Business Problem

Banks and financial institutions need to monitor a large number of transactions while identifying potentially suspicious activity.

A useful fraud analytics process should answer questions such as:

- Where is fraud occurring?
- Which merchant categories show higher observed fraud rates?
- Which payment methods show different fraud activity?
- Does transaction timing provide a useful risk signal?
- How does fraud vary between international and non-international transactions?
- Is night-time activity associated with different fraud rates?
- How does fraud vary across customers?
- Which transactions are statistically unusual?
- Can multiple transaction characteristics be used to predict fraud?
- How can analytical findings be communicated to business users?

This project addresses these questions through data analytics, statistical analysis, machine learning, and business intelligence.

---

# 🎯 Business Objectives

The project was developed to:

1. Understand a large banking transaction dataset.
2. Validate the structure and quality of the raw data.
3. Clean and prepare transaction-level data.
4. Create useful analytical features.
5. Calculate fraud-related KPIs.
6. Analyze fraud across multiple business dimensions.
7. Analyze customer-level fraud behavior.
8. Identify unusual observations using the 3-Sigma method.
9. Analyze fraud by merchant category.
10. Analyze fraud by payment method.
11. Analyze fraud across geography.
12. Analyze fraud by transaction hour.
13. Compare night and non-night transactions.
14. Compare international and non-international transactions.
15. Compare weekend and non-weekend transactions.
16. Investigate behavioral risk indicators.
17. Identify potential fraud risk signals.
18. Build a Logistic Regression classification model.
19. Evaluate the model using multiple classification metrics.
20. Build an interactive Power BI dashboard.
21. Convert analytical findings into business recommendations.

---

# 📊 Dataset

## Dataset Size

| Attribute | Value |
|---|---:|
| Total Transactions | 1,000,000 |
| Total Columns | 26 |
| Target Variable | `is_fraud` |

The dataset contains transaction-level banking information along with customer, behavioral, risk, and fraud-related attributes.

## 🎯 Target Variable

The main target variable is:

`is_fraud`

It identifies whether a transaction is classified as fraudulent.

The target variable was used for:

- Fraud KPI calculations
- Fraud-rate analysis
- Customer risk analysis
- Pattern analysis
- Machine Learning classification

---

# 🧾 Feature Categories

## Transaction Information

| Feature | Description |
|---|---|
| `transaction_id` | Unique transaction identifier |
| `transaction_date` | Transaction date |
| `transaction_time` | Transaction time |
| `transaction_amount` | Transaction value |
| `merchant_category` | Merchant/business category |
| `payment_method` | Payment method used |

## Customer Information

| Feature | Description |
|---|---|
| `customer_id` | Customer identifier |
| `customer_age` | Customer age |
| `credit_score` | Customer credit score |
| `account_age_years` | Age of customer account |
| `account_balance` | Account balance |

## Behavioral Information

| Feature | Description |
|---|---|
| `distance_from_home_km` | Distance of transaction from home |
| `num_prev_transactions` | Number of previous transactions |
| `transaction_freq_monthly` | Monthly transaction frequency |
| `time_since_last_txn_hrs` | Time since previous transaction |
| `failed_attempts` | Failed transaction or authentication attempts |

## Risk Indicators

| Feature | Description |
|---|---|
| `is_international` | Indicates an international transaction |
| `is_weekend` | Indicates weekend activity |
| `is_night_transaction` | Indicates night-time activity |
| `pin_changed_recently` | Indicates a recent PIN change |

## Fraud Information

| Feature | Description |
|---|---|
| `is_fraud` | Fraud classification target |
| `fraud_type` | Fraud category/type |

---

# 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Data analysis and Machine Learning |
| Pandas | Data manipulation and transformation |
| NumPy | Numerical analysis |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Scikit-learn | Machine Learning |
| Jupyter Notebook | Analytical environment |
| Power BI | Interactive dashboard and reporting |

---

# 🔄 End-to-End Workflow

```text
1. Data Loading
        ↓
2. Data Quality & Cleaning
        ↓
3. Feature Engineering
        ↓
4. Exploratory Data Analysis
        ↓
5. Fraud KPI Analysis
        ↓
6. 3-Sigma Outlier Analysis
        ↓
7. Customer-Level Risk Analysis
        ↓
8. Fraud Pattern Analysis
        ↓
9. Geographical Analysis
        ↓
10. Transaction Timing Analysis
        ↓
11. Risk Indicator Analysis
        ↓
12. Business Findings
        ↓
13. Machine Learning
        ↓
14. Model Evaluation
        ↓
15. Power BI Dashboard
        ↓
16. Business Recommendations
        ↓
17. Conclusion
```

---

# 1. 📥 Data Loading & Initial Inspection

The first stage was to load the banking transaction dataset into the Python environment using Pandas.

The purpose of this stage was to establish a reliable starting point for the complete analytical workflow.

The loaded dataset contained:

- **1,000,000 transactions**
- **26 columns**
- Transaction information
- Customer information
- Behavioral information
- Risk indicators
- Fraud labels

## Initial Dataset Inspection

The following checks were performed:

- Dataset shape
- Column names
- First records
- Random sample
- Last records
- Data types
- Statistical summary
- Unique values
- Missing values

These checks helped establish the structure of the raw dataset before transformation.

## Why Data Loading Matters

Data loading is the foundation of the analysis.

Before performing fraud analysis, it is necessary to confirm that:

- The expected dataset has been loaded.
- The number of records is correct.
- Required columns are available.
- Variables have reasonable data types.
- The target variable is present.
- Potential quality issues are visible.

Only after this initial inspection was the dataset taken into the cleaning stage.

---

# 2. 🧹 Data Quality & Cleaning

Before performing statistical analysis or Machine Learning, the dataset was checked for data-quality issues.

The goal was to make the data consistent and suitable for downstream analysis.

## Missing Value Analysis

Missing values were reviewed using column-level null checks.

Particular attention was given to:

- Transaction fields
- Customer fields
- Behavioral fields
- Risk indicators
- Fraud fields

Missing values in `fraud_type` were handled consistently so that non-fraud observations could be represented as `No Fraud`.

## Duplicate Record Checks

Duplicate records were investigated at two levels:

1. Complete duplicate rows
2. Duplicate transaction IDs

Repeated values in categorical columns were not automatically treated as duplicate records.

For example, many transactions can legitimately have the same:

- Country
- Merchant category
- Payment method

Therefore, categorical repetition alone does not indicate a duplicate transaction.

## Data Type Validation

Data types were reviewed before analysis.

This was particularly important for:

- Dates
- Times
- Numerical variables
- Binary indicators
- Categorical variables

Correct data types are required for accurate aggregation, visualization, statistical calculations, and Machine Learning.

## Date Conversion

The `transaction_date` field was converted to a datetime-compatible format.

This enables date-based analysis and consistent reporting.

## Time Conversion

The `transaction_time` field was converted using the expected time format.

This made it possible to extract transaction-hour information.

## Negative Value Checks

Numerical fields were checked for unexpected negative values.

This validation step helps identify potential data-entry or data-quality problems before statistical analysis.

## Binary Column Standardization

The following binary indicators were standardized into numeric `0/1` representations:

- `is_weekend`
- `is_night_transaction`
- `is_international`
- `pin_changed_recently`
- `is_fraud`

Using consistent binary values makes grouping, aggregation, visualization, and model preparation easier.

## Fraud Type Standardization

The `fraud_type` field was standardized.

Missing fraud types and non-fraud transactions were represented consistently as:

`No Fraud`

## Cleaning Outcome

After quality checks and transformations, the dataset was prepared for:

- Feature engineering
- Exploratory analysis
- Fraud KPI calculations
- Customer-level aggregation
- Statistical analysis
- Machine Learning
- Power BI reporting

---

# 3. ⚙️ Feature Engineering

Feature engineering was used to create analytical variables from existing transaction data.

The main engineered feature documented in the project was:

`hour_of_day`

## Hour of Day

The transaction time was transformed into an hourly representation.

```text
Transaction Time
       ↓
Extract Hour
       ↓
hour_of_day
       ↓
Fraud Rate by Hour
```

This feature was later used in:

- Exploratory Data Analysis
- Fraud pattern analysis
- Risk indicator analysis
- Machine Learning

## Why Feature Engineering Matters

Raw transaction time is less convenient for grouped fraud analysis.

Converting time into `hour_of_day` makes it possible to compare:

- Morning activity
- Afternoon activity
- Evening activity
- Late-night activity
- Early-morning activity

Feature engineering therefore converts raw fields into variables that are more useful for analysis.

---

# 4. 🔎 Exploratory Data Analysis

Exploratory Data Analysis was performed to understand the distribution and behavior of transaction data before drawing business conclusions.

The EDA focused on:

- Transaction amounts
- Customer attributes
- Behavioral variables
- Merchant categories
- Payment methods
- Geographic information
- Transaction timing
- Fraud indicators

## Transaction Amount Analysis

Transaction amounts were examined to understand:

- Distribution
- Central tendency
- Spread
- Potentially unusual values
- Relationship with fraud

Transaction amount was also included in the later outlier analysis and Machine Learning feature set.

## Customer Attribute Analysis

Customer-level variables were examined to understand the population represented by the dataset.

Relevant attributes included:

- Age
- Credit score
- Account age
- Account balance

These variables were also considered as potential inputs for customer risk analysis and fraud prediction.

## Behavioral Variable Analysis

Behavioral characteristics were reviewed, including:

- Distance from home
- Previous transaction count
- Monthly transaction frequency
- Time since previous transaction
- Failed attempts

These variables provide context about how a transaction compares with historical or behavioral patterns.

## Categorical Analysis

Categorical fields were explored to understand fraud variation across:

- Merchant categories
- Payment methods
- Countries
- Fraud types

---

# 5. 📊 Fraud KPI Analysis

Fraud KPIs were calculated to establish an overall view of fraud activity.

| KPI | Purpose |
|---|---|
| Total Transactions | Overall transaction volume |
| Fraud Transactions | Number of fraudulent transactions |
| Non-Fraud Transactions | Number of non-fraud transactions |
| Fraud Rate | Proportion of transactions classified as fraud |
| Total Fraud Amount | Total transaction value associated with fraud |
| Average Fraud Transaction Amount | Average value of fraudulent transactions |
| Fraud Customers | Number of customers associated with fraud |

## Fraud Rate

Fraud rate provides a normalized measure of fraud activity.

```text
Fraud Rate
=
Fraud Transactions
-------------------
Total Transactions
× 100
```

This metric was used to compare fraud activity across business dimensions.

## Why KPIs Matter

A fraud dashboard should not only show individual transactions.

Decision-makers also need summary indicators that answer:

- How many transactions occurred?
- How many were classified as fraud?
- What percentage were fraudulent?
- What amount was associated with fraud?
- How many customers were affected?

These KPIs form the foundation of the Power BI dashboard.

---

# 6. 📐 3-Sigma Outlier Analysis

The project used the **3-Sigma method** to investigate unusual transaction behavior.

The analysis focused on:

- Transaction amount
- Distance from home
- Transaction frequency
- Number of previous transactions

## 3-Sigma Concept

The boundaries were defined as:

```text
Lower Bound = Mean - 3 × Standard Deviation

Upper Bound = Mean + 3 × Standard Deviation
```

Observations outside these limits were treated as statistically unusual for investigation.

## Why Outliers Were Not Automatically Removed

Outliers were not automatically removed.

In fraud analytics, unusual transactions can contain valuable information.

An unusually high:

- Transaction amount
- Distance from home
- Transaction frequency
- Previous transaction count

may represent legitimate behavior or potentially suspicious behavior.

Removing such records automatically could therefore remove useful fraud signals.

## Outlier vs Fraud

A statistical outlier is not automatically a fraudulent transaction.

The project compared the fraud behavior of:

- Normal observations
- Statistical outliers

The purpose was to investigate whether unusual behavior showed different fraud activity.

## Business Interpretation

```text
Transaction
     ↓
Statistical Check
     ↓
Normal / Unusual
     ↓
Combine With Other Signals
     ↓
Risk Investigation
```

---

# 7. 👤 Customer-Level Risk Analysis

Fraud analysis was also performed at the customer level.

A single transaction does not always provide enough information to understand customer behavior.

Customer-level aggregation provides a broader view.

## Customer-Level Metrics

The analysis included:

- Total transactions
- Total transaction amount
- Average transaction amount
- Fraud transaction count
- Fraud rate

## Customer Transaction Volume

Total transaction count helps identify customers with high transaction activity.

High transaction volume alone is not evidence of fraud, but it provides context when combined with other indicators.

## Total Transaction Amount

The total amount provides an overview of monetary activity associated with each customer.

## Average Transaction Amount

Average transaction amount provides additional behavioral context.

It helps distinguish customers who generally perform:

- Small-value transactions
- Medium-value transactions
- Higher-value transactions

## Customer Fraud Count

Fraud transaction count indicates how many transactions associated with a customer were classified as fraudulent.

## Customer Fraud Rate

Fraud rate provides a normalized customer-level measure, which is useful when customers have different transaction volumes.

## Customer Risk Monitoring

A practical monitoring approach can combine:

```text
Transaction Frequency
        +
Transaction Amount
        +
Fraud History
        +
Behavioral Signals
        +
Risk Indicators
```

---

# 8. 🔍 Fraud Pattern Analysis

Fraud activity was analyzed across multiple transaction dimensions.

The major dimensions included:

- Merchant category
- Payment method
- Country
- Transaction hour
- Night activity
- International activity
- Weekend activity
- Fraud type

---

# 9. 🏪 Merchant Category Analysis

Merchant categories were compared using fraud rate.

Selected categories with higher observed fraud rates included:

| Merchant Category | Observed Fraud Rate |
|---|---:|
| ATM Withdrawal | ~8.74% |
| Jewelry | ~8.70% |
| Crypto Exchange | ~8.65% |

These values describe observed fraud rates in this dataset.

## Merchant Risk Interpretation

Merchant category can be useful as one component of fraud monitoring.

However:

- A high category-level fraud rate does not mean every transaction in that category is fraudulent.
- Merchant category should not be used as a standalone fraud rule.
- Additional transaction and customer signals should be considered.

---

# 10. 💳 Payment Method Analysis

Fraud activity was compared across payment methods.

| Payment Method | Observed Fraud Rate |
|---|---:|
| Cheque | ~5.67% |
| Credit Card | ~5.60% |
| Bank Transfer | ~5.51% |
| Crypto | ~5.50% |
| Mobile Payment | ~5.49% |
| Debit Card | ~5.46% |

## Payment Method Interpretation

Payment method can be useful as a contextual variable.

The observed rates were relatively close, so payment method alone should not be treated as an automatic fraud rule.

It can instead be combined with:

- Transaction amount
- Location
- Timing
- Customer history
- International status
- Other behavioral indicators

---

# 11. 🌍 Geographical Analysis

Fraud rates were analyzed geographically using available location information.

The analysis considered:

- Country
- City
- Other available geographic dimensions

## Country-Level Analysis

Brazil showed the highest observed fraud rate among the analyzed countries at approximately:

**5.67%**

This is an observed dataset result and should not be interpreted as a general statement about fraud risk in Brazil outside this dataset.

## Geographic Risk Monitoring

Geographical analysis can help investigate:

- Unusual transaction locations
- Cross-border activity
- Location changes
- Geographic concentration of fraud

Geographic information should be interpreted together with other transaction and customer characteristics.

---

# 12. ⏰ Transaction Timing Analysis

Transaction timing was analyzed using the engineered `hour_of_day` feature.

## Hourly Fraud Analysis

The highest observed hourly fraud rate occurred around:

**6 AM — approximately 8.07%**

Midnight and early-morning periods also showed elevated observed activity.

## Why Time Matters

Transaction time can provide additional behavioral context.

A transaction may become more relevant for investigation when its timing differs substantially from a customer's normal activity.

Time should therefore be considered as one component of a broader risk-monitoring framework.

---

# 13. 🌙 Night vs Non-Night Analysis

Transactions were divided into:

- Night transactions
- Non-night transactions

| Transaction Type | Observed Fraud Rate |
|---|---:|
| Non-Night | ~4.07% |
| Night | ~7.96% |

The observed fraud rate was substantially higher among night transactions in this dataset.

## Business Interpretation

Night-time activity can be used as an additional risk signal.

A monitoring system could consider:

```text
Night Transaction
       +
Unusual Amount
       +
Unusual Location
       +
Other Behavioral Signals
```

rather than flagging every night transaction.

---

# 14. 🌐 International vs Non-International Analysis

Transactions were compared based on international status.

| Transaction Type | Observed Fraud Rate |
|---|---:|
| Non-International | ~4.76% |
| International | ~9.86% |

International transactions showed approximately twice the observed fraud rate of non-international transactions in this dataset.

## Business Interpretation

International status represents an important contextual risk indicator in this analysis.

It can be combined with:

- Transaction location
- Transaction amount
- Customer behavior
- Transaction timing
- Merchant category
- Historical transaction patterns

The result should be treated as a risk signal rather than an automatic fraud decision.

---

# 15. 📅 Weekend vs Non-Weekend Analysis

Weekend transactions were compared with non-weekend transactions.

| Transaction Period | Observed Fraud Rate |
|---|---:|
| Non-Weekend | ~5.51% |
| Weekend | ~5.57% |

The difference was small.

## Business Interpretation

Weekend status alone does not provide a strong separation in this dataset.

This supports the broader principle that fraud monitoring should use multiple signals rather than relying on one simple rule.

---

# 16. 🚨 Risk Indicator Analysis

The project investigated multiple variables that may provide useful fraud-monitoring signals.

These included:

- International transaction status
- Night transaction status
- Weekend status
- Recent PIN change
- Failed attempts
- Transaction distance
- Transaction frequency
- Previous transaction count
- Transaction amount
- Transaction timing

## Risk Signal Framework

```text
                 Transaction
                      |
        +-------------+-------------+
        |             |             |
      Amount        Timing       Location
        |             |             |
        +-------------+-------------+
                      |
                 Behavior
                      |
        +-------------+-------------+
        |             |             |
   Frequency    Previous Txns   Failed Attempts
                      |
                 Risk Indicators
                      |
          +-----------+-----------+
          |                       |
    International              Night
          |                       |
          +-----------+-----------+
                      |
                Risk Assessment
```

This approach provides a more complete view than using a single variable.

---

# 17. 📌 Key Business Findings

## Finding 1 — International Transactions

International transactions showed an observed fraud rate of approximately **9.86%**, compared with approximately **4.76%** for non-international transactions.

This represents one of the larger observed differences in the analysis.

## Finding 2 — Night Transactions

Night transactions showed an observed fraud rate of approximately **7.96%**, compared with approximately **4.07%** for non-night transactions.

This indicates that transaction timing can provide an additional risk signal.

## Finding 3 — Merchant Categories

Selected merchant categories showed relatively higher observed fraud rates:

- ATM Withdrawal — ~8.74%
- Jewelry — ~8.70%
- Crypto Exchange — ~8.65%

## Finding 4 — Payment Methods

Payment-method fraud rates were relatively close in the observed results.

Cheque had an observed rate of approximately **5.67%**, while Debit Card was approximately **5.46%**.

## Finding 5 — Transaction Hour

The highest observed hourly fraud rate was approximately **8.07% at 6 AM**.

Midnight and early-morning periods also showed elevated observed fraud activity.

## Finding 6 — Weekend Activity

Weekend and non-weekend fraud rates were very similar:

- Non-weekend — ~5.51%
- Weekend — ~5.57%

## Finding 7 — Statistical Outliers

3-Sigma analysis identified statistically unusual observations across selected numerical variables.

These observations were not automatically removed because unusual behavior can be analytically valuable in fraud detection.

---

# 18. 🚨 Fraud Risk Signals

Based on the observed analysis, several variables can be considered useful contextual risk signals.

Higher observed fraud activity was associated with:

- International transactions
- Night transactions
- Selected merchant categories
- Certain transaction hours
- Unusual transaction behavior

## Multi-Signal Monitoring

A practical fraud-monitoring approach should combine signals.

```text
International
      +
Night Transaction
      +
Unusual Transaction Amount
      +
Unusual Distance
      +
Failed Attempts
      +
Recent PIN Change
      ↓
Higher Investigation Priority
```

This is a conceptual monitoring framework rather than a fixed fraud rule.

---

# 19. 🤖 Machine Learning

Machine Learning was introduced to move from descriptive analytics toward transaction-level fraud classification.

The selected model was:

**Logistic Regression**

## Machine Learning Objective

The objective was to predict:

`is_fraud`

using transaction, behavioral, customer, and risk-related features.

## Selected Features

The model used:

- Transaction amount
- Hour of day
- Distance from home
- Number of previous transactions
- Transaction frequency
- Failed attempts
- Account balance
- Weekend indicator
- Night indicator
- International indicator
- Recent PIN change

## Train-Test Split

The dataset was divided into:

- **80% training data**
- **20% testing data**

A `random_state` of **42** was used for reproducibility.

The split used stratification to preserve target-class distribution.

## Class Imbalance Handling

The Logistic Regression configuration used balanced class weights to give additional consideration to the minority class during training.

## Logistic Regression Configuration

The documented configuration included:

- Logistic Regression
- `class_weight = balanced`
- `max_iter = 1000`
- Stratified train-test split
- Random state = 42

## Why Logistic Regression

Logistic Regression provides a practical and interpretable baseline for binary classification.

It can help establish whether the selected transaction and behavioral features contain useful predictive information.

---

# 20. 📏 Model Evaluation

The model was evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Classification Report
- Confusion Matrix

## Accuracy

Accuracy measures the proportion of total predictions that were correct.

However, accuracy alone may not be sufficient for fraud classification when classes are imbalanced.

## Precision

Precision measures how many transactions predicted as fraud were actually fraudulent.

## Recall

Recall measures how many actual fraudulent transactions were successfully identified.

## F1 Score

F1 Score combines precision and recall into a single harmonic-mean metric.

## ROC-AUC

ROC-AUC evaluates the model's ability to distinguish fraud from non-fraud across classification thresholds.

## Confusion Matrix

```text
                 Predicted
              Non-Fraud   Fraud

Actual
Non-Fraud       TN          FP

Fraud           FN          TP
```

Where:

- **TN** = True Negative
- **FP** = False Positive
- **FN** = False Negative
- **TP** = True Positive

## Model Metric Note

Actual numerical model metrics should be taken from the executed notebook output.

This README intentionally does not invent or assume model performance values.

---

# 21. 📊 Power BI Dashboard

Power BI was used to transform the analytical results into an interactive business-facing dashboard.

The cleaned dataset was prepared for reporting after the Python analysis.

## Dashboard Objectives

The dashboard was designed to help users:

- Monitor overall fraud KPIs
- Analyze fraud by country
- Compare merchant categories
- Compare payment methods
- Analyze hourly fraud activity
- Compare night and day activity
- Compare international and domestic activity
- Explore fraud types
- Filter the analysis interactively

## Dashboard KPIs

The main dashboard KPIs included:

- Total Transactions
- Fraud Transactions
- Fraud Rate
- Fraud Amount

## Dashboard Analysis

### Fraud Rate by Country

Shows how observed fraud rates vary geographically.

### Fraud Rate by Merchant Category

Shows which merchant categories have higher or lower observed fraud rates.

### Fraud Rate by Payment Method

Allows comparison of fraud activity across payment methods.

### Fraud Rate by Hour

Shows how fraud activity varies throughout the day.

### Night vs Day

Compares observed fraud rates between night and non-night transactions.

### International vs Domestic

Compares international and non-international transaction activity.

### Fraud Type Distribution

Provides visibility into different fraud categories.

## Dashboard Filters

Interactive filters included:

- Country
- Merchant Category
- Payment Method
- Device Type
- Fraud Type
- Transaction Date

## Dashboard Business Value

The Power BI dashboard converts analytical results into a business-friendly monitoring interface.

```text
Overall KPIs
     ↓
Geographic Analysis
     ↓
Merchant Analysis
     ↓
Payment Analysis
     ↓
Time Analysis
     ↓
Risk Indicator Analysis
     ↓
Fraud Type Analysis


### Dashboard Preview

![Banking Fraud Dashboard](images/fraud_analysis_dashboard.png)

🔗 **[Download Power BI Dashboard (.pbix)](https://drive.google.com/file/d/1YE8fwWl10vPgTajP403kDgtzrCy52JI_/view?usp=sharing)**
```

---

# 22. 💡 Business Recommendations

## Recommendation 1 — Monitor International Transactions

International transactions showed a higher observed fraud rate in this dataset.

Additional attention can be given to international activity when combined with other risk signals.

## Recommendation 2 — Add Time-Based Risk Signals

Night and early-morning transaction activity showed elevated observed fraud rates.

Transaction time can therefore be incorporated into risk scoring or investigation prioritization.

## Recommendation 3 — Monitor High-Observed-Risk Merchant Categories

Merchant categories such as ATM Withdrawal, Jewelry, and Crypto Exchange showed higher observed fraud rates.

These categories can receive additional analytical monitoring.

## Recommendation 4 — Use Multi-Signal Risk Detection

Fraud monitoring should combine multiple indicators rather than relying on one rule.

Potential signals include:

- Transaction amount
- International status
- Night status
- Distance from home
- Failed attempts
- Transaction frequency
- Previous transactions
- Recent PIN change
- Merchant category
- Transaction timing

## Recommendation 5 — Use Customer-Level Monitoring

Repeated fraud classifications or unusual customer behavior can be monitored at the customer level.

## Recommendation 6 — Investigate Statistical Outliers

Statistical outliers should not automatically be removed.

Instead, they can be investigated alongside fraud labels and other risk indicators.

## Recommendation 7 — Use Machine Learning as Decision Support

The Logistic Regression model can support transaction-level classification.

A production fraud system would combine Machine Learning with business rules, monitoring, threshold optimization, human investigation, and model performance monitoring.

---

# 23. 📈 Analytical Value

This project demonstrates a complete transition from raw data to business intelligence.

```text
Raw Transactions
       ↓
Clean Data
       ↓
Analytical Features
       ↓
Fraud KPIs
       ↓
Statistical Analysis
       ↓
Customer Risk Analysis
       ↓
Fraud Pattern Analysis
       ↓
Machine Learning
       ↓
Power BI Reporting
       ↓
Business Recommendations
```

## Data Analytics Value

The project demonstrates:

- Data validation
- Data cleaning
- Feature engineering
- Exploratory Data Analysis
- KPI development
- Fraud analysis
- Customer-level analysis
- Statistical analysis
- Outlier analysis
- Business insight generation

## Machine Learning Value

The project demonstrates:

- Feature selection
- Target definition
- Train-test splitting
- Stratified sampling
- Logistic Regression
- Class imbalance handling
- Classification metrics
- Confusion matrix analysis

## Business Intelligence Value

The project demonstrates:

- KPI reporting
- Interactive filtering
- Business visualization
- Fraud monitoring
- Risk analysis
- Data storytelling

---

# 24. ⚠️ Limitations

## Dataset Dependency

The findings are based on the available transaction dataset and may not represent every banking environment.

## Correlation vs Causation

The analysis identifies observed relationships and differences. It does not establish that a particular characteristic causes fraud.

## Fraud Rate Interpretation

A higher fraud rate for a category does not mean every transaction in that category is fraudulent.

## Outlier Interpretation

A statistical outlier is not automatically fraudulent.

## Weekend Analysis

Weekend and non-weekend fraud rates were very similar in the observed dataset.

## Machine Learning Limitation

Logistic Regression was used as the baseline classification model.

A production system would require broader model comparison, validation, tuning, and monitoring.

## Production Limitation

This is an analytical and Machine Learning portfolio project, not a production-ready real-time banking fraud system.

It does not implement:

- Real-time transaction scoring
- Real-time alert delivery
- Production APIs
- Automated model retraining
- Production model monitoring
- Live banking-system integration

---

# 25. 🚀 Future Improvements

## Advanced Machine Learning Models

Future experiments can include:

- Random Forest
- Gradient Boosting
- XGBoost
- Other classification algorithms

Models can then be compared using consistent evaluation metrics.

## Hyperparameter Tuning

Future versions can use:

- Cross-validation
- Grid search
- Randomized search
- Threshold optimization

## Feature Importance

Additional analysis can identify which variables contribute most strongly to fraud predictions.

## Advanced Fraud Scoring

Instead of simple fraud/non-fraud classification, a future system can generate a continuous risk score.

```text
Transaction
     ↓
Feature Extraction
     ↓
Risk Model
     ↓
Fraud Probability / Risk Score
     ↓
Investigation Priority
```

## Automated ETL Pipeline

The workflow can be converted into:

```text
Data Source
    ↓
ETL
    ↓
Data Validation
    ↓
Cleaning
    ↓
Feature Engineering
    ↓
Model Scoring
    ↓
Database / Warehouse
    ↓
Power BI
```

## Database Integration

The cleaned data can be stored in:

- Relational databases
- Data warehouses
- Analytical storage systems

## Real-Time Fraud Detection

A future production-oriented implementation could support:

- Real-time transaction ingestion
- Real-time feature generation
- Model scoring
- Fraud alerts
- Investigation queues

## Power BI Enhancements

The dashboard can be extended with:

- Drill-through pages
- Additional KPIs
- Detailed customer profiles
- Risk-score distribution
- Time trends
- Advanced tooltips
- Scheduled refresh
- Role-based reporting

---

# 26. 📁 Project Structure

```text
banking-fraud-analytics/
│
├── README.md
├── banking_fraud_analytics.ipynb
├── banking_fraud_dashboard.pbix
├── requirements.txt
│
├── images/
│   └── fraud_analysis_dashboard.png
│
└── data/
    └── README.md
```

## File Description

| File | Purpose |
|---|---|
| `README.md` | Project documentation |
| `banking_fraud_analytics.ipynb` | Complete Python analysis and Machine Learning workflow |
| `banking_fraud_dashboard.pbix` | Power BI dashboard |
| `requirements.txt` | Python dependencies |
| `images/` | Dashboard/project images |
| `data/README.md` | Dataset documentation |

The large raw dataset is not included directly in the repository.

---

# 27. ▶️ How to Run

## Step 1 — Clone or Download the Repository

Download the project repository to your local machine.

## Step 2 — Install Python

Use a suitable Python environment for running the notebook.

## Step 3 — Install Dependencies

Install the packages listed in:

`requirements.txt`

## Step 4 — Open Jupyter Notebook

Open:

`banking_fraud_analytics.ipynb`

## Step 5 — Run the Notebook

Run the notebook sequentially to reproduce:

- Data loading
- Data inspection
- Data quality checks
- Data cleaning
- Feature engineering
- EDA
- Fraud KPI analysis
- Customer risk analysis
- 3-Sigma analysis
- Fraud pattern analysis
- Visualization
- Machine Learning
- Model evaluation

## Step 6 — Open Power BI

Open:

`banking_fraud_dashboard.pbix`

Refresh the data source if required and explore the interactive dashboard.

---

# 28. 📦 Requirements

```text
pandas
numpy
matplotlib
seaborn
scikit-learn
jupyter
```

---

# 29. 🧠 Skills Demonstrated

## Data Analytics

- Data Loading
- Data Validation
- Data Cleaning
- Data Transformation
- Exploratory Data Analysis
- KPI Analysis
- Fraud Analytics
- Customer Risk Analysis
- Statistical Analysis
- Outlier Analysis
- Feature Engineering
- Business Analysis
- Business Insights
- Data Storytelling

## Python

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Machine Learning

- Feature Selection
- Target Definition
- Train-Test Split
- Stratified Sampling
- Class Imbalance Handling
- Logistic Regression
- Binary Classification
- Precision
- Recall
- F1 Score
- ROC-AUC
- Classification Report
- Confusion Matrix

## Power BI

- KPI Development
- Interactive Dashboard
- Fraud Monitoring
- Risk Analysis
- Business Visualization
- Interactive Filters
- Data Storytelling

---

# 30. 📄 Resume Project Description

### Banking Fraud Analytics & Fraud Prediction

**Python | Pandas | NumPy | Matplotlib | Seaborn | Scikit-learn | Power BI | Machine Learning**

- Analyzed **1M+ banking transactions** to identify fraud patterns across merchant categories, payment methods, geography, transaction timing, and customer behavior.
- Identified elevated observed fraud activity in **international transactions (~9.86% vs ~4.76% non-international)**, **night transactions (~7.96% vs ~4.07% non-night)**, and selected merchant categories including **ATM Withdrawal (~8.74%)**.
- Applied **3-Sigma statistical analysis** to investigate unusual transaction behavior and developed a **Logistic Regression fraud classification model** evaluated using Precision, Recall, F1-score, ROC-AUC, classification report, and confusion matrix.
- Built an interactive **Power BI fraud-monitoring dashboard** with KPI reporting, country, merchant, payment method, hourly, transaction-type, and fraud-type analysis.

---

# 31. 📌 Project Takeaways

## Technical Takeaways

- Worked with **1,000,000 transaction records**.
- Performed structured data-quality checks.
- Cleaned and transformed transaction data.
- Converted date and time fields.
- Standardized binary indicators.
- Created an hourly analytical feature.
- Developed fraud KPIs.
- Performed customer-level aggregation.
- Applied 3-Sigma statistical analysis.
- Analyzed fraud across multiple business dimensions.
- Developed a Logistic Regression classification model.
- Evaluated the model using multiple classification metrics.
- Created an interactive Power BI dashboard.

## Business Takeaways

The analysis identified several observed patterns:

- International transactions showed higher observed fraud activity.
- Night transactions showed higher observed fraud activity.
- Selected merchant categories showed higher observed fraud rates.
- Transaction timing provided an additional risk signal.
- Customer-level behavior can support repeated-risk monitoring.
- Statistical outliers can be investigated as unusual behavior.
- Multiple risk signals can be combined to prioritize investigation.

---

# 32. 🎯 Overall Project Outcome

The project demonstrates how a large transaction dataset can be transformed into a structured fraud analytics solution.

The complete process combines:

```text
Data
 ↓
Cleaning
 ↓
Feature Engineering
 ↓
Exploration
 ↓
KPIs
 ↓
Statistical Analysis
 ↓
Customer Analysis
 ↓
Fraud Pattern Analysis
 ↓
Machine Learning
 ↓
Power BI
 ↓
Business Insights
```

The result is a portfolio project demonstrating practical experience across:

- Python Data Analytics
- Statistical Analysis
- Fraud Analytics
- Machine Learning
- Power BI
- Business Intelligence
- Data Storytelling

---

# 33. 📝 Conclusion

This project demonstrates an end-to-end **Banking Fraud Analytics and Fraud Prediction workflow**, starting from raw transaction data and progressing through data preparation, statistical analysis, customer-level analysis, Machine Learning, and Power BI reporting.

The analysis combined:

- Data Loading
- Data Quality Checks
- Data Cleaning
- Feature Engineering
- Exploratory Data Analysis
- Fraud KPI Analysis
- Customer Risk Analysis
- 3-Sigma Statistical Analysis
- Fraud Pattern Analysis
- Geographical Analysis
- Transaction Timing Analysis
- Risk Indicator Analysis
- Logistic Regression
- Model Evaluation
- Power BI Dashboard
- Business Recommendations

The strongest observed differences in the dataset were associated with **international transactions, night transactions, selected merchant categories, and certain transaction hours**.

International transactions showed an observed fraud rate of approximately **9.86%**, compared with approximately **4.76%** for non-international transactions. Night transactions showed approximately **7.96%**, compared with approximately **4.07%** for non-night transactions.

The analysis also identified higher observed fraud rates in selected merchant categories such as **ATM Withdrawal (~8.74%)**, **Jewelry (~8.70%)**, and **Crypto Exchange (~8.65%)**.

The project does not treat these characteristics as automatic proof of fraud. Instead, they are interpreted as **potential risk signals** that can be combined with customer behavior, transaction characteristics, location, timing, and other indicators.

The Machine Learning component extends the project from descriptive analysis toward fraud classification using Logistic Regression. The model was evaluated using Precision, Recall, F1 Score, ROC-AUC, classification report, and confusion matrix.

Finally, the Power BI dashboard converts the analytical results into an interactive business reporting layer, allowing users to explore fraud KPIs and patterns across geography, merchants, payment methods, transaction timing, transaction types, and fraud categories.

Overall, the project demonstrates a complete analytics pipeline:

```text
Raw Banking Transactions
        ↓
Data Preparation
        ↓
Statistical & Exploratory Analysis
        ↓
Fraud Risk Analysis
        ↓
Machine Learning
        ↓
Business Intelligence
        ↓
Actionable Insights
```

This project demonstrates practical **Data Analytics, Statistical Analysis, Machine Learning, Business Intelligence, and Data Storytelling** skills applied to a banking fraud use case.
