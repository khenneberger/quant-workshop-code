# 🧾 Task 3: Credit Default Risk Modeling and Comparison

This task focuses on building and comparing classification models to predict the probability of loan default using historical financial data. The models are evaluated on their predictive performance and their utility in estimating financial risk.

---

## 🎯 Objective

The goal of this project is to:
- Predict the **probability of default (PD)** for loan applicants
- Use the PD to calculate **expected financial loss**
- Compare multiple modeling approaches to identify the most effective strategy

---

## 📋 Instructions

1. **Input Data**: Load the dataset `Loan_Data.csv`, which contains financial and employment information for loan applicants, along with a binary target indicating default (`default = 1`).

2. **Feature Selection**: Use the following predictors:
   - `credit_lines_outstanding`
   - `loan_amt_outstanding`
   - `total_debt_outstanding`
   - `income`
   - `years_employed`
   - `fico_score`

3. **Model Training**:
   - Split the dataset into training and testing sets (80/20).
   - Train three models: Logistic Regression, Decision Tree, and XGBoost.

4. **Evaluation Metrics**:
   - **Accuracy**: Percentage of correct predictions
   - **ROC AUC**: Area under the ROC curve, indicating how well the model ranks positive instances
   - **Expected Loss**: Calculated using the formula:  
     \[
     \text{Expected Loss} = \text{PD} \times \text{Exposure} \times (1 - \text{Recovery Rate})
     \]

5. **Model Comparison**:
   - Evaluate all three models on the same test set.
   - Compare based on accuracy, AUC, and expected loss.

---

## ⚙️ Implementation Overview

- **Logistic Regression**: Baseline linear model for classification.
- **Decision Tree Classifier**: Nonlinear model capturing feature interactions.
- **XGBoost Classifier**: Gradient boosting ensemble that provides superior predictive power.

---

## 📈 Results and Observations

- All three models perform reasonably well on the task.
- **XGBoost** achieved the best results in terms of ROC AUC and expected loss.
- ROC AUC is more important than raw accuracy for this application, since the ability to rank defaulters accurately is critical to minimizing financial risk.

---

## 🛠 Dependencies

Install required libraries using:

```bash
pip install pandas scikit-learn xgboost
 
