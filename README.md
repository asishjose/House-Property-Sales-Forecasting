# 🏡 House Property Sales Forecasting (2007–2019)

This project focuses on forecasting house property sales prices using various **time series forecasting models** and comparing their performance to find the most accurate one.

---

## 📊 Dataset Overview

- **Period:** 2007–2019  
- **Columns:** `saledate`, `price`, `type`, `bedrooms`, `postcode`  
- **Frequency:** Monthly (aggregated mean prices)
- **Focus:** Forecasting property **price trends** for houses and units.

---

## 🧠 Models Compared

| Model | MAE | RMSE |
|-------|-----|------|
| **LSTM** | 21647.49 | 30541.72 |
| **Holt-Winters** | 29163.23 | 35255.13 |
| **Prophet** | 29307.63 | 35375.60 |
| **SARIMA** | 28740.88 | 36464.43 |
| **ARIMA** | 63067.00 | 69375.22 |

---

## 🏁 Conclusion

Among all models, **LSTM** achieved the lowest MAE and RMSE, showing its superior ability to capture complex nonlinear relationships and temporal dependencies in property sales data.  
Traditional statistical models (Holt-Winters, SARIMA, Prophet) also performed well but lagged slightly behind the deep learning approach.

---

## ⚙️ Setup & Requirements

```bash
pip install -r requirements.txt
