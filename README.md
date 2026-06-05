# Mobile Money Loan Eligibility and Loan Amount Prediction

## Hybrid Machine Learning Project: Supervised and Unsupervised Learning

This project develops a machine learning system for predicting mobile money loan eligibility, estimating the possible loan amount, and grouping customers into risk categories using clustering.

The project is inspired by mobile money credit services such as MoKash, where customer transaction behaviour can be used to support credit decision-making.

---

## Project Overview

Mobile money loan providers need reliable ways to decide whether a customer should receive a loan and how much should be offered. Poor loan decisions may cause financial losses when risky customers are approved, while very strict systems may reject good customers.

This project uses a hybrid machine learning approach:

- **Unsupervised learning** for customer segmentation and risk grouping.
- **Supervised classification** for predicting loan eligibility.
- **Supervised regression** for predicting the loan amount.

---

## Project Objectives

The main objectives of this project are:

1. To analyse mobile money transaction behaviour.
2. To group customers into risk categories using clustering.
3. To predict whether a customer is eligible for a loan.
4. To estimate the loan amount or loan limit for eligible customers.
5. To compare different machine learning models and select the best-performing ones.
6. To provide visual explanations using graphs, heatmaps, and model evaluation charts.

---

## Machine Learning Methods Used

### 1. Unsupervised Learning

Unsupervised learning is used to group customers based on transaction behaviour.

Models used:

- K-Means Clustering
- Gaussian Mixture Model
- Agglomerative Clustering

Evaluation metrics:

- Silhouette Score
- Calinski-Harabasz Score
- Davies-Bouldin Score

---

### 2. Supervised Classification

Classification is used to predict whether a customer is eligible for a loan.

Models used:

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- Support Vector Machine
- Gradient Boosting Classifier
- K-Nearest Neighbors / other comparison model

Evaluation metrics:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC Score
- Confusion Matrix
- ROC Curve

---

### 3. Supervised Regression

Regression is used to predict the loan amount for eligible customers.

Models used:

- Linear Regression
- Ridge Regression
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor
- Support Vector Regressor / other comparison model

Evaluation metrics:

- MAE
- RMSE
- R² Score
- Actual vs Predicted Plot
- Residual Plot

---

## Dataset

The project uses a mobile money transaction dataset with features such as:

- `step`
- `type`
- `amount`
- `nameOrig`
- `oldbalanceOrg`
- `newbalanceOrig`
- `nameDest`
- `oldbalanceDest`
- `newbalanceDest`

Fraud-related columns such as `isFraud` and `isFlaggedFraud` are removed because this project focuses on loan eligibility and loan amount prediction, not fraud detection.

---

## Feature Engineering

Several customer-level features were created from transaction records, including:

- Transaction count
- Average transaction amount
- Total transaction amount
- Maximum transaction amount
- Standard deviation of transaction amount
- Average old balance
- Average new balance
- Origin balance change
- Destination balance change
- Cash flow ratio
- Destination balance ratio
- Log-transformed amount
- Log-transformed cash flow ratio
- Transaction type ratios

These features help the model understand customer financial behaviour.

---

## Project Workflow

```text
1. Import required libraries
2. Load the mobile money dataset
3. Inspect dataset structure
4. Clean the dataset
5. Perform exploratory data analysis
6. Engineer customer-level features
7. Apply clustering for risk grouping
8. Profile clusters and assign risk labels
9. Create supervised learning targets
10. Train classification models
11. Train regression models
12. Compare model performance
13. Interpret feature importance
14. Make final customer loan prediction
