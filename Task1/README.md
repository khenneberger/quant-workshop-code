# 📈 Natural Gas Price Forecasting – Multiple Approaches

This folder contains code for modeling and forecasting natural gas prices using **two distinct approaches**, developed as part of the Quantitative Workshop. The goal is to demonstrate different methods for time series analysis in the context of commodity price forecasting.

---

## 🧠 Problem Statement

Natural gas prices fluctuate over time due to seasonal demand, geopolitical factors, and supply dynamics. The challenge is to forecast future prices using statistical and mathematical models that capture both trend and seasonality.

---

## Approaches Implemented

### 1. **SARIMA Modeling (`pmdarima`-based)**
- Automatically detects seasonal trends and optimal hyperparameters
- Uses the `auto_arima` function to model the data
- Produces forecasts with 95% confidence intervals
- Ideal for more general-purpose and robust forecasting

### 2. **Sinusoidal Decomposition + Linear Regression**
- Decomposes prices into a long-term **linear trend** and a **yearly periodic component**
- Uses **bilinear regression** to fit a sine curve to seasonal effects
- Provides intuitive insight into cyclical patterns in energy prices
- Forecasts are made by combining linear and sinusoidal components

Each method has its own strengths:
- SARIMA is flexible and statistically grounded
- Sinusoidal + regression is interpretable and lightweight

---

## 📁 File Overview

- `forecasting_methods.py` – Combined Python script containing both forecasting methods and plotting routines
- `Nat_Gas.csv` – Historical natural gas price data (monthly)
- `README.md` – Project description and documentation

---

## ▶️ How to Run

Make sure required packages are installed:
```bash
pip install pandas numpy matplotlib pmdarima
