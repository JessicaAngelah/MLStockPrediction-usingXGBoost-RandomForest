# 📈 Machine Learning Model for ANTAM Stock Price Prediction

This project builds a **machine learning–based stock price prediction model** for **PT Aneka Tambang Tbk (ANTM.JK)** using historical market data and technical indicators.  
The goal is to **predict the next trading day’s closing price** and compare the performance of two popular machine learning models:

- 🌲 Random Forest Regressor  
- 🚀 XGBoost Regressor  

The project is implemented in **Python** using a **Jupyter Notebook** and is suitable for academic assignments, portfolios, and learning purposes.

---

## 📂 Project Structure

MLmodelForANTAM.ipynb # Main notebook containing data processing, modeling, and evaluation
README.md # Project documentation


---

## 📊 Data Source

- **Ticker:** `ANTM.JK`
- **Data Provider:** Yahoo Finance (`yfinance`)
- **Time Range:** January 2022 – Present
- **Frequency:** Daily closing prices

No API keys are required.

---

## ⚙️ Libraries & Frameworks

The following Python libraries are used:

- `yfinance` – stock market data retrieval  
- `pandas`, `numpy` – data manipulation  
- `matplotlib` – data visualization  
- `scikit-learn` – machine learning models & evaluation  
- `ta` – technical indicators  
- `xgboost` – gradient boosting model  

---

## 🧠 Feature Engineering (How the Model Understands the Market)

Instead of predicting prices blindly, the model uses **technical indicators** to capture market behavior:

| Feature | Description |
|------|------------|
| SMA_5 | 5-day Simple Moving Average (short-term trend) |
| SMA_10 | 10-day Simple Moving Average (medium-term trend) |
| Volatility | Rolling standard deviation of returns (risk level) |
| RSI | Relative Strength Index (momentum indicator) |

These features help the model understand **trend, momentum, and volatility**.

---

## 🎯 Target Variable

- **Target:** Next trading day’s closing price  
- Created by shifting the closing price by one day forward.

---

## 🧪 Train–Test Split

- **80% Training data**
- **20% Testing data**
- Data is **not shuffled** to preserve time-series order.

---

## 🌲 Random Forest Model

Random Forest is an ensemble learning method that combines multiple decision trees to reduce overfitting and capture nonlinear patterns in stock price movements.

### Evaluation Metric:
- **Mean Absolute Error (MAE)**

Example result:
MAE ≈ 927 IDR


**Interpretation:**  
On average, the Random Forest model’s predictions differ from the actual ANTAM stock price by approximately **927 Indonesian Rupiah**.

---

## 🚀 XGBoost Model

XGBoost (Extreme Gradient Boosting) improves upon traditional ensemble models by sequentially correcting errors from previous trees, making it well-suited for structured financial data.

### Evaluation Metric:
- **Mean Absolute Error (MAE)**

Example result:
MAE ≈ 944 IDR


---

## 📈 Model Comparison

Both models are evaluated using the same test dataset and compared visually:

- Actual closing prices  
- Random Forest predictions  
- XGBoost predictions  

This allows an intuitive understanding of how closely each model tracks real market movements.

---

## 📉 Visualization

The notebook includes:
- Actual vs Predicted price plots
- Side-by-side comparison between Random Forest and XGBoost

These visualizations help interpret model performance beyond numeric metrics.

---

## 📌 Key Findings

- Random Forest achieved slightly lower MAE than XGBoost on this dataset.
- Both models demonstrate reasonable short-term predictive capability.
- Tree-based models are effective, interpretable, and easy to train for daily stock prediction tasks.

---

## ⚠️ Disclaimer

This project is for **educational purposes only**.  
It does **not constitute financial advice** and should not be used for real trading decisions without further validation, risk management, and transaction cost considerations.

---

## 🚀 Future Improvements

Potential extensions include:
- Buy/Sell signal optimization
- Backtesting with transaction costs
- Additional technical indicators
- Hyperparameter tuning
- Comparison with deep learning models (e.g., LSTM)

---

## 👩‍💻 Author

Developed as a learning and portfolio project using Python and machine learning techniques.
