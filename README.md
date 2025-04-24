 # 📊 Quantitative Modeling & Risk Assessment — Project Overview

This repository contains a series of four tasks that explore various **quantitative modeling** strategies in the context of finance and risk management. Each task builds on practical machine learning and data science methods to solve real-world problems in loan analysis, commodity trading, and credit risk modeling.

---

## 🚀 Project Goals

- Simulate and value financial contracts under real-world constraints
- Model credit risk using classification techniques
- Compare modeling strategies using industry-relevant evaluation metrics
- Apply advanced feature engineering techniques like quantization for risk segmentation

---

## 🧩 Task Summaries

### 🔹 **Task 1 — Time Series Forecasting: Natural Gas Prices**
**Concepts:** SARIMA modeling, sinusoidal + linear trend decomposition  
**Goal:** Forecast future natural gas prices using:
- **SARIMA**: Automatically detects seasonal trends and outputs a statistical forecast
- **Custom sinusoidal regression**: Decomposes historical price into a linear trend and a seasonal sinusoidal component  
**Evaluation:** Forecast visualization, smoothed trends, and extrapolation

---

### 🔹 **Task 2 — Storage Contract Valuation**
**Concepts:** Simulation modeling, storage capacity constraints, cash flow analysis  
**Goal:** Price a gas storage contract by modeling:
- Injection and withdrawal behavior across dates
- Capacity and operational constraints
- Cash inflows and outflows based on market prices  
**Output:** Net contract value (profit/loss) calculated from trading decisions

---

### 🔹 **Task 3 — Credit Default Classification**
**Concepts:** Logistic regression, decision trees, XGBoost, ROC AUC, expected loss  
**Goal:** Predict the probability of loan default using various models:
- Logistic Regression (baseline)
- Decision Tree (nonlinear baseline)
- XGBoost (ensemble model)  
**Evaluation:** Accuracy, AUC, Expected Loss  

---

### 🔹 **Task 4 — Quantization of FICO Scores for Risk Modeling**
**Concepts:** Feature quantization, bucketization, log-likelihood optimization  
**Goal:** Compare the effect of quantizing FICO scores using:
- **Mean Squared Error (MSE)** based binning
- **Log-likelihood-based** bucketing (dynamic, risk-driven)  
**Method:** Add quantized buckets to the feature set, retrain logistic regression  
**Evaluation:** Accuracy, Confusion Matrix, Classification Report

---

## 🛠 Methods/Libraries Used

- **Python** (NumPy, Pandas, Scikit-learn, XGBoost)
- **Time Series Modeling** (`pmdarima`)
- **Logistic Regression / Decision Trees / Boosting**
- **Quantization techniques** for feature engineering
- **Model Evaluation Metrics**: Accuracy, ROC AUC, Expected Loss, Confusion Matrix


