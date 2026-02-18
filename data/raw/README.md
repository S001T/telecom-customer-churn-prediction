# Telecom Customer Churn Prediction

## Project Overview
This project aims to predict customer churn for a telecom company using machine learning models.  
Customer churn refers to whether a customer leaves the company or not.

The goal is:
- to identify high-risk customers,
- to understand key factors driving churn,
- and to compare different ML models.

---

## Dataset
The dataset contains information about 7,043 customers, including:
- Demographics (gender, senior citizen)
- Services (internet, security, streaming)
- Contract details
- Payment methods
- Charges and tenure

Target variable:
- `Churn` (1 = customer left, 0 = customer stayed)

---

## Data Preprocessing
Steps performed:

1. Converted `TotalCharges` to numeric and filled missing values.
2. Encoded target variable `Churn` to binary.
3. Binary encoding for Yes/No features.
4. One-hot encoding for categorical features.
5. Standardized numerical features:
   - `tenure`
   - `MonthlyCharges`
   - `TotalCharges`
6. Split data into train/test (80/20, stratified).

---

## Exploratory Data Analysis (EDA)
Key observations:
- Customers with **month-to-month contracts** churn more often.
- **Fiber optic users** have higher churn rate.
- Customers with **short tenure** are more likely to leave.
- Higher monthly charges correlate with higher churn.

---

## Models Used

### 1. Logistic Regression
A linear probabilistic model that estimates churn probability.

Used for:
- Interpretability
- Feature importance analysis

### 2. Decision Tree
Rule-based model using if-else conditions.

Used for:
- Visual explanation
- Business interpretability

### 3. Random Forest
Ensemble of multiple decision trees.

Used for:
- Best predictive performance
- Robustness

---

## Model Performance

| Model | ROC-AUC | Accuracy |
|------|--------|----------|
| Logistic Regression | ~0.84 | ~0.79 |
| Decision Tree | ~0.71 | ~0.80 |
| Random Forest | ~0.83 | ~0.79 |

---

## Key Features Influencing Churn

Consistently important across models:

- `tenure`
- `Contract type`
- `InternetService (Fiber optic)`
- `PaymentMethod (Electronic check)`
- `MonthlyCharges`

---

## Business Insights

High-risk customers:
- New customers (low tenure)
- Month-to-month contracts
- Fiber optic internet users
- Electronic check payment method

These customers should be prioritized for retention strategies.

---

## Conclusion

The project demonstrates a full ML pipeline:
- Data cleaning
- Feature engineering
- Model training
- Evaluation
- Business interpretation

The results provide both predictive power and actionable business insights.

