# E-Commerce Fraud Detection System

# a. Problem statement
This project focuses on detecting fraudulent e-commerce transactions using multiple machine learning classification models. The goal is to compare different algorithms and evaluate their effectiveness in identifying fraud.
The project also includes a Streamlit web application that allows users to upload a dataset and evaluate model performance interactively.

## b. Dataset description
The dataset used contains historical e-commerce transaction records with a binary target variable indicating whether a transaction is fraudulent.
Some columns that are not useful for prediction (such as transaction ID and addresses) were removed during preprocessing.

- Number of instances: 23,634
- Number of features: 15
- Target variable: Is Fraudulent
  - 0 → Valid transaction
  - 1 → Fraud transaction

### Feature Types:
- Numerical features: Transaction amount, account age, transaction frequency, etc.
- Categorical features: Payment method, product category, customer location, device used

Categorical features were label-encoded, and irrelevant identifier columns were removed during preprocessing.

---

## c. Models used:

The following machine learning models were implemented:

- Logistic Regression
- Decision Tree
- K-Nearest Neighbors (KNN)
- Naive Bayes
- Random Forest
- XGBoost

All models are implemented as Python source files (`.py`) as required.

### Evaluation Metrics:
- Accuracy
- AUC Score
- Precision
- Recall
- F1 Score
- Matthews Correlation Coefficient (MCC)

---

## Comparison Table with the evaluation metrics calculated for all the models as below:

| ML Model | Accuracy | AUC | Precision | Recall | F1 Score | MCC |
|--------|---------|-----|----------|--------|----------|-----|
| Logistic Regression | 0.9534 | 0.7777 | 0.8497 | 0.1203 | 0.2108 | 0.3095 |
| Decision Tree | 0.9794 | 0.923 | 0.7694 | 0.8601 | 0.8122 | 0.8028 |
| KNN | 0.9551 | 0.885 | 0.832 | 0.1661 | 0.2769 | 0.3599 |
| Naive Bayes | 0.9419 | 0.7732 | 0.3898 | 0.2185 | 0.28 | 0.2638 |
| Random Forest(Ensemble) | 0.9905 | 0.9807 | 0.9845 | 0.8298 | 0.9005 | 0.8992 |
| XGBoost(Ensemble) | 0.9737 | 0.942 | 0.9439 | 0.5229 | 0.673 | 0.6919 |


---

##  Observations on the performance of each model on the chosen dataset.

| ML Model | Observation |
|--------|------------|
| Logistic Regression | Gave high accuracy but missed many fraud cases, as shown by its very low recall. |
| Decision Tree | Picked up more fraud cases than most models but overall performance was weaker and less reliable. |
| kNN | Showed good accuracy, but struggled badly to identify fraud cases, leading to low recall and F1 score. |
| Naive Bayes | Performed decently overall but made simplifying assumptions that limited its ability to detect fraud accurately. |
| Random Forest(Ensemble)  | Balanced performance well with strong AUC and MCC, showing better handling of complex patterns. |
| XGBoost(Ensemble)  | Delivered the most consistent and effective results, especially in identifying fraud, making it the best overall model. |
