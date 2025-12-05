# High-Accuracy Currency Exchange Rate Forecasting using Deep Learning (LSTM)

## 📌 Project Overview
This project focuses on forecasting the daily closing price of the **Euro/Moroccan Dirham exchange rate (EURMAD=X)** using a deep learning LSTM model. The system processes five years of historical financial data and predicts short-term market movements with high accuracy.

---

## 🎯 Goal
Build and evaluate a robust time-series forecasting model capable of predicting future EUR/MAD prices for financial insight and trading support.

---

## 📊 Data Acquisition & Preprocessing
- Collected **5 years of historical data** for the EURMAD=X pair using the `yfinance` API.
- Applied **MinMaxScaler** normalization to stabilize gradients and speed up training.
- Generated structured sequences with a **60-day look-back window**, shaping the dataset into:



Compatible with recurrent neural network architectures.

---

## 🧠 Model Architecture (LSTM)
- Constructed a **Sequential Keras model** with:
- **Two stacked LSTM layers**, each with **50 units**
- LSTMs selected for their ability to retain and learn long-term patterns in noisy financial signals.
- Trained using a **time-based split (80% train / 20% test)** to ensure validation on unseen data.

<p align="center">
<img src="model_architecture.png" alt="LSTM Model Architecture" width="500"/>
</p>

---

## 📈 Key Results
- **Test RMSE:** `0.0612` on unseen market data
- Given the EUR/MAD rate fluctuates around **10–11 MAD**, this means the model predicts within **0.06 MAD**, a strong performance for a volatile financial instrument.

This result highlights:
- High predictive reliability  
- Strong applicability in **financial risk management** and **short-term trading strategies**

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
A powerful deep learning forecasting pipeline achieving strong accuracy on real-world financial data, demonstrating the effectiveness of LSTMs in time-series prediction tasks.
