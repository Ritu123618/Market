# 📈 Stock Price Trend Prediction using LSTM  

## 🔹 Overview  
This project predicts future stock prices using **historical data** and a **Long Short-Term Memory (LSTM)** deep learning model.  
It also integrates **technical indicators** such as Moving Average (MA) and Relative Strength Index (RSI) for better analysis.  

---

## 🔹 Features  
- Fetches historical stock price data using **Yahoo Finance API (yfinance)** or CSV data  
- Normalizes and prepares the dataset for LSTM  
- Builds and trains an LSTM neural network with **Keras**  
- Predicts and visualizes stock price trends  
- Plots **Moving Average** and **RSI** indicators alongside actual and predicted prices  

---

## 🔹 Tech Stack  
- **Python 3.x**  
- **Libraries:**  
  - yfinance (for data fetching)  
  - numpy, pandas, matplotlib  
  - scikit-learn (MinMaxScaler)  
  - keras (Sequential, LSTM, Dense)  

---

## 🔹 Workflow  
1. **Data Collection:**  
   - Download historical data using `yfinance`  
   - Fallback: Use CSV data when API isn’t accessible  

2. **Data Preprocessing:**  
   - Clean and normalize prices using `MinMaxScaler`  
   - Prepare data for time-series LSTM (look-back of 60 days)  

3. **Model Building:**  
   - LSTM layers with Dropout for regularization  
   - Dense output layer for predicting next-day close price  

4. **Model Training & Prediction:**  
   - Train on 80% of the data, validate on 20%  
   - Predict and compare actual vs predicted prices  

5. **Technical Indicators:**  
   - **14-day Moving Average (MA)**  
   - **14-day RSI** to detect overbought/oversold conditions  

6. **Visualization:**  
   - Plot actual vs predicted stock prices  
   - Overlay Moving Average  
   - Plot RSI separately with thresholds  

---

## 🔹 Outputs  
- Graphs comparing **actual and predicted prices**  
- Moving Average & RSI charts  
- Trained LSTM model weights (if saved)  

---

## 🔹 How to Run  
1. Install dependencies:  
   ```bash
   pip install yfinance keras scikit-learn matplotlib pandas numpy
