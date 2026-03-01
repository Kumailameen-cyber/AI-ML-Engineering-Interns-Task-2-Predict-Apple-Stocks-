# 📈 Stock Price Prediction using Machine Learning

A machine learning project that predicts the next day's closing stock price using historical data fetched from Yahoo Finance.

---

## 📌 Objective

Use historical stock market data to predict the **next day's closing price** using Linear Regression and Random Forest models.

---

## 📂 Dataset

- **Source:** Yahoo Finance via `yfinance` Python library
- **Stock:** Apple Inc. (`AAPL`) — changeable to any ticker
- **Period:** January 2022 – January 2024
- **Features Used:**

| Feature | Description |
|---------|-------------|
| Open | Opening price of the day |
| High | Highest price of the day |
| Low | Lowest price of the day |
| Volume | Number of shares traded |
| Prev_Close | Previous day's closing price |
| Prev_Close_2 | Closing price 2 days ago |
| Prev_Close_3 | Closing price 3 days ago |
| MA_5 | 5-day moving average |
| MA_10 | 10-day moving average |
| Daily_Change | Difference between Close and Open |
| High_Low_Gap | Difference between High and Low |

---

## 🛠️ Libraries Required

```bash
pip install yfinance scikit-learn matplotlib pandas numpy
```

---

## 🚀 How to Run

1. Open the notebook in **Google Colab** or **Jupyter Notebook**
2. Run all cells from top to bottom
3. To change the stock, edit this line:

```python
ticker = "AAPL"   # Change to TSLA, GOOGL, MSFT etc.
```

---

## 🤖 Models Used

### 1. Linear Regression
- Simple baseline model
- Fits a straight line through the feature space
- Fast training, interpretable results

### 2. Random Forest Regressor
- Ensemble of 200 decision trees
- Handles non-linear relationships better
- More accurate than Linear Regression for stock data

```python
RandomForestRegressor(
    n_estimators=200,
    max_depth=10,
    min_samples_split=5,
    random_state=42
)
```

---

## 📊 Evaluation Metrics

| Metric | Description |
|--------|-------------|
| MAE | Mean Absolute Error — average dollar error |
| RMSE | Root Mean Squared Error — penalizes large errors |
| R² | How well the model fits the data (1.0 = perfect) |
| Avg $ Error | Average dollar difference from real price |

---

## 📉 Output Plots

1. **Actual vs Predicted Closing Price** — Line chart comparing real prices against both model predictions over time
2. **Feature Importance Chart** — Bar chart showing which features the Random Forest relied on most

---

## 📁 Project Structure

```
stock-price-prediction/
│
├── stock_prediction.ipynb   # Main Colab notebook
├── README.md                # Project documentation
```

---

## ⚠️ Disclaimer

This project is for **educational purposes only**. Stock price predictions made by this model should **not** be used for real financial decisions. Stock markets are influenced by many unpredictable factors not captured in historical price data alone.

---

## 👨‍💻 Skills Demonstrated

- Time series data handling
- Feature engineering
- Regression modeling (Linear + Random Forest)
- Data fetching using APIs (yfinance)
- Model evaluation and comparison
- Data visualization with Matplotlib

---

## 📚 References

- [yfinance Documentation](https://pypi.org/project/yfinance/)
- [scikit-learn Documentation](https://scikit-learn.org/)
- [Yahoo Finance](https://finance.yahoo.com/)
