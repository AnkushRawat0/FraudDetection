# Credit Card Fraud Detection using Machine Learning

## Project Overview

Credit card fraud is a major challenge in the financial industry, leading to significant monetary losses and security concerns. The objective of this project is to build a machine learning model capable of identifying fraudulent transactions based on transaction behavior and risk-related features.

The project covers the complete machine learning workflow including data preprocessing, exploratory data analysis (EDA), feature engineering, model training, evaluation, and feature importance analysis.

---

## Dataset

**Dataset:** Credit Card Fraud Detection Dataset

### Dataset Information

* Total Records: 10,000
* Target Variable: `is_fraud`
* Problem Type: Binary Classification
* Fraud Class: 1
* Legitimate Class: 0

### Features

* amount
* transaction_hour
* merchant_category
* foreign_transaction
* location_mismatch
* device_trust_score
* velocity_last_24h
* cardholder_age
* transaction_channel
* is_fraud

---

## Data Preprocessing

The following preprocessing steps were performed:

* Checked for missing values
* Checked for duplicate records
* Performed One-Hot Encoding on categorical variables
* Split data into training and testing sets
* Applied Standard Scaling
* Prepared data for machine learning models

---

## Exploratory Data Analysis (EDA)

Exploratory Data Analysis was conducted to understand fraud patterns and feature relationships.

### Class Distribution

The dataset is highly imbalanced, with legitimate transactions significantly outnumbering fraudulent transactions.

### Transaction Amount Analysis

Fraudulent transactions showed different spending behavior compared to legitimate transactions, with several high-value outliers observed.

### Transaction Hour Analysis

Transaction timing was found to be an important indicator of fraudulent activity. Certain hours showed a higher concentration of fraud cases.

### Device Trust Score Analysis

Lower device trust scores were strongly associated with fraudulent transactions.

### Foreign Transaction Analysis

Foreign transactions exhibited a higher fraud rate compared to domestic transactions.

### Location Mismatch Analysis

Transactions with location mismatches were more likely to be fraudulent.

### Transaction Velocity Analysis

Higher transaction velocity within the previous 24 hours was associated with increased fraud risk.

### Correlation Analysis

A correlation heatmap was generated to understand relationships between features and identify potential patterns.

---

## Machine Learning Models

### Logistic Regression

Logistic Regression was used as a baseline model for comparison.

### Random Forest Classifier

Random Forest was implemented to capture complex non-linear relationships and improve fraud detection performance.

---

## Model Performance

| Model               | Accuracy | Precision | Recall | F1 Score |
| ------------------- | -------- | --------- | ------ | -------- |
| Logistic Regression | 99.25%   | 85.71%    | 60.00% | 70.59%   |
| Random Forest       | 99.70%   | 100.00%   | 80.00% | 88.89%   |

---

## Feature Importance Analysis

Feature importance extracted from the Random Forest model revealed the following key predictors of fraud:

1. device_trust_score
2. transaction_hour
3. velocity_last_24h
4. foreign_transaction
5. amount
6. location_mismatch

These features contributed most significantly to fraud detection decisions.

---

## Key Insights

* Device trust score was the strongest predictor of fraud.
* Fraudulent transactions frequently occurred during unusual hours.
* High transaction velocity was associated with suspicious activity.
* Foreign transactions carried a higher fraud risk.
* Merchant category had relatively low predictive importance.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* Jupyter Notebook

---

## Future Improvements

* Hyperparameter tuning
* ROC-AUC optimization
* XGBoost implementation
* SMOTE for class imbalance handling
* Model deployment using FastAPI
* Interactive dashboard development

---

## Conclusion

This project demonstrates an end-to-end machine learning workflow for fraud detection. Random Forest significantly outperformed Logistic Regression, achieving 99.70% accuracy, 100% precision, and 80% recall. Feature importance analysis highlighted behavioral and risk-based indicators as the most effective predictors of fraudulent transactions.
