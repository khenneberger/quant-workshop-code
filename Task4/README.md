# 🧮 Task 4: Quantization Strategies for Credit Default Prediction

This task explores the impact of feature quantization—specifically for **FICO scores**—on the performance of logistic regression models used to predict **loan default**. The task compares two quantization strategies: **Mean Squared Error (MSE)** and a custom **Log-Likelihood-based** bucketing approach.

---

## 🎯 Objective

To evaluate how different FICO score bucketing techniques affect model performance in a loan default classification problem. The project compares:

- Model performance with **MSE-based quantization**
- Model performance with **Log-Likelihood optimized quantization**

---

## 📋 Instructions

1. **Load the dataset** (`Loan_Data.csv`) and select input features:
   - `credit_lines_outstanding`
   - `loan_amt_outstanding`
   - `total_debt_outstanding`
   - `income`
   - `years_employed`

2. **Define the target variable**:  
   `default` (binary outcome: 1 for default, 0 for no default)

3. **Quantize the FICO score** using two approaches:
   - **MSE Quantization**: Split the range of scores into equally spaced bins.
   - **Log-Likelihood Quantization**: Dynamically determine bucket boundaries to maximize classification signal based on likelihood of default.

4. **Train separate logistic regression models** for each method using scikit-learn:
   - Use the original features + quantized FICO bucket as inputs.
   - Evaluate using accuracy, confusion matrix, and classification report.

---

## ⚙️ Implementation Summary

### 1. MSE Quantization
- Divides the FICO score range into `n` equally spaced bins.
- Maps each applicant to a discrete bucket.
- Adds `fico_buckets_mse` as a categorical input to the model.

### 2. Log-Likelihood Quantization
- Dynamically builds FICO buckets based on maximizing the likelihood of default within each bin.
- Uses a recursive, bucket-splitting process.
- Produces `fico_buckets_ll`, a more risk-calibrated input feature.

---

## 📊 Evaluation Metrics

Each model is evaluated using:
- **Accuracy**: Overall correctness of predictions
- **Confusion Matrix**: Breakdown of true/false positives and negatives
- **Classification Report**: Includes precision, recall, and F1-score

These metrics provide insight into how effective the quantization methods are in segmenting credit risk.

---

## 🛠 Dependencies

```bash
pip install pandas numpy scikit-learn
 
