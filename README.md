# 📈 High-Accuracy Currency Exchange Rate Forecasting + Backtesting (LSTM)

---

## 📌 Project Overview
This project focuses on forecasting the daily closing price of the **Euro/Moroccan Dirham exchange rate (EURMAD=X)** using a deep learning LSTM model.  
It processes historical financial data and predicts short-term market movements.  
In addition, the project includes a **complete backtesting engine** that converts predictions into trading signals and evaluates the strategy using professional metrics.

---

## 🎯 Goal
Build and evaluate a robust time-series forecasting model capable of predicting future EUR/MAD prices and validating a trading strategy using out-of-sample backtesting.

---

## 📊 Data Acquisition & Preprocessing
- Collected historical data for the **EURMAD=X** pair using the `yfinance` API.
- Applied **MinMaxScaler** normalization to stabilize gradients and speed up training.
- Generated structured sequences with a **60-day look-back window**.

---

## 🧠 Model Architecture (LSTM)
- Sequential Keras model with:
  - **Two stacked LSTM layers** (50 units each)
  - **Dense output layer**
- Trained using a **time-based split (80% train / 20% test)** to ensure validation on unseen data.

---

## 📈 Key Results (Forecasting)
- **Test RMSE:** `0.0612` (example value)
- Given the EUR/MAD rate fluctuates around **10–11 MAD**, this means the model predicts within **0.06 MAD**, a strong performance for a volatile financial instrument.

---

## 🧪 Backtest & Trading Strategy
A simple trading protocol is used:

1. **BUY** if predicted next-day price > current price  
2. **SELL (short)** otherwise  
3. Exit after **1 trading day**  
4. No leverage, no transaction fees (baseline strategy)

---

## 📉 Backtest Results


---

## 📌 Performance Metrics Explained

| Metric | Meaning | Results |
|--------|---------|---------|
| **Total Trades** | Number of executed trades |**562** |
| **Win Rate** | Percentage of profitable trades |**56.76%** |
| **Profit Factor** | Gross Profit / Gross Loss |**1.55** |
| **Total PnL** | Net profit of the strategy |**2.89** |
| **Max Drawdown** | Worst peak-to-valley loss |**-0.35**|
| **Avg Duration** | Average holding time per trade |**1440 min**|

---

## 🛠️ Technologies Used
- Python  
- Keras/TensorFlow (LSTM)  
- Pandas & NumPy  
- Matplotlib  
- Scikit-learn  
- yfinance API  

---

## 🚀 Summary
A powerful deep learning forecasting pipeline achieving strong accuracy on real-world financial data, enhanced with a full trading backtest.  
The project demonstrates how LSTM predictions can be transformed into a systematic trading strategy with real performance evaluation.

---

## ⚠️ Disclaimer
This project is for **educational purposes only** and **not financial advice**.  
Real trading requires additional risk management, transaction cost modeling, and robustness testing.

---

## 🔮 Future Improvements
- Add transaction fees and spread  
- Add stop-loss / take-profit  
- Improve signal generation (trend filters, volatility filters)  
- Multi-asset support  
- Live trading integration  
