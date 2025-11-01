# 🏡 House Property Sales Forecasting (2007–2019)

This project focuses on **forecasting house property sales prices** using multiple **time series forecasting models** and comparing their performance to determine the most efficient one.

---

## 📊 Dataset Overview

- **Period:** 2007–2019  
- **Columns:** `saledate`, `price`, `type`, `bedrooms`, `postcode`  
- **Type:** Monthly aggregated time series  
- **Description:**  
  The dataset contains monthly house and unit sale prices across different postcodes, with varying bedroom counts.  
  It represents long-term housing price trends, seasonal variations, and economic influences in the property market.

---

## 🎯 Project Objective

To build, evaluate, and compare different **time series models** for forecasting property sales prices and identify the best performing method based on accuracy metrics.

---

## 🧠 Models Implemented

| Model | MAE | RMSE |
|:------|----:|----:|
| **LSTM** | 21647.49 | 30541.72 |
| **Holt-Winters** | 29163.23 | 35255.13 |
| **Prophet** | 29307.63 | 35375.60 |
| **SARIMA** | 28740.88 | 36464.43 |
| **ARIMA** | 63067.00 | 69375.22 |

---

## 🧩 Methodology

1. **Data Preprocessing**
   - Converted `saledate` to datetime and sorted in ascending order.  
   - Resampled to monthly frequency and aggregated using mean prices.  
   - Handled missing values using interpolation and forward fill.  
   - Split data chronologically (80% train, 20% test).

2. **Model Training & Forecasting**
   - Built univariate forecasting models:
     - ARIMA
     - SARIMA
     - Holt-Winters (Exponential Smoothing)
     - Prophet
     - LSTM (Deep Learning)
   - Each model was trained on the training period and evaluated on the test period.

3. **Evaluation Metrics**
   - **MAE (Mean Absolute Error)**
   - **RMSE (Root Mean Squared Error)**  
   - Consistent test split used across models for fair comparison.

---

## 📈 Insights & Findings

- The dataset showed **strong seasonality and trend** patterns across years.  
- **LSTM** outperformed all other models with the lowest MAE and RMSE, effectively capturing nonlinear and long-term dependencies.  
- **Traditional models** (Holt-Winters, SARIMA, Prophet) provided interpretable and stable forecasts, suitable for explainable forecasting tasks.  
- **ARIMA** underperformed due to its limited handling of seasonality and complex patterns.

---

## 🏁 Conclusion

The **LSTM model** demonstrated the best forecasting accuracy, proving the strength of deep learning methods for modeling complex, nonlinear time series data in the real-estate domain.  
However, simpler statistical models like **Holt-Winters** and **Prophet** still offer strong performance with easier interpretability and faster computation.

---

## ⚙️ Setup & Requirements

Install dependencies before running the notebooks:

```bash
pip install -r requirements.txt
