# Telco Customer Churn Prediction

## 1. Overview

This project focuses on predicting customer churn using machine learning techniques. The objective is to identify customers who are likely to leave a service so that businesses can take preventive actions.

The model is designed with a focus on **recall**, ensuring that the majority of churn customers are correctly identified.

---

## 2. Problem Statement

Customer churn leads to revenue loss for businesses. The goal of this project is to:

* Predict whether a customer will churn (Yes/No)
* Minimize false negatives (missed churn customers)
* Build a model aligned with business needs

---

## 3. Dataset Information

* Dataset: Telco Customer Churn
* Number of rows: 7043
* Number of features: 21 (before encoding)

### Target Variable

* `Churn`

  * Yes → 1
  * No → 0

---

## 4. Data Preprocessing

### 4.1 Data Cleaning

* Converted `TotalCharges` to numeric
* Handled hidden missing values using `errors='coerce'`
* Removed rows with missing values

### 4.2 Feature Engineering

* Dropped irrelevant column: `customerID`
* Applied one-hot encoding to categorical features
* Converted target variable to binary

### 4.3 Feature Scaling

* Applied Standardization to numerical features

---

## 5. Model Building

### 5.1 Train-Test Split

* Data split into training and testing sets

### 5.2 Models Used

* Logistic Regression
* Random Forest

### 5.3 Handling Class Imbalance

* Used `class_weight='balanced'` to improve performance on minority class

---

## 6. Model Evaluation

### Metrics Used

* Accuracy
* Precision
* Recall (primary focus)
* F1 Score

### Key Result

* Accuracy: ~73%
* Recall (Churn): ~79%

---

## 7. Model Optimization

### Threshold Tuning

* Adjusted classification threshold to improve recall
* Lower threshold helped capture more churn customers

### Visualization

* Confusion Matrix
* ROC Curve

---

## 8. Feature Importance

Top features influencing churn:

* Tenure
* Contract type
* Total charges
* Internet service
* Payment method

---

## 9. Final Model Selection

Logistic Regression was selected as the final model because it achieved higher recall compared to Random Forest and aligned better with the business objective.

---

## 10. Business Insights

* Customers with short tenure are at higher risk of churn
* Long-term contracts reduce churn probability
* Service type and payment method influence behavior

---

## 11. Limitations

* Model may produce false positives
* Limited dataset features
* Performance may vary on real-world data

---

## 12. Future Improvements

* Try advanced models (XGBoost, Gradient Boosting)
* Perform feature selection
* Deploy model using API
* Use larger or real-time datasets

---

## 13. Tech Stack

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib

---

## 14. How to Run

```bash
git clone <your-repository-link>
cd <repository-folder>
pip install -r requirements.txt
jupyter notebook
```

---

## 15. Author

Medha Jha
