# AI-Powered Stock Trend Analysis Tool

## Overview

This project is a Python-based system designed to analyze and predict stock market trends using a combination of **technical indicators, machine learning, and sentiment analysis**. The tool collects historical stock market data, performs technical analysis, trains a predictive model, and visualizes the results through an interactive dashboard.

The system focuses on exploring **data-driven trading insights** using commonly used financial indicators and machine learning techniques.

---

## Key Features

### 1. Market Data Collection

- Fetches historical stock market data using the **Yahoo Finance API**.
- Supports analysis of stocks from **NSE and BSE exchanges**.
- Retrieves market data including:
  - Open price
  - High price
  - Low price
  - Close price
  - Volume

---

### 2. Technical Analysis

The system computes several widely used technical indicators:

- **Relative Strength Index (RSI)**
- **Moving Average Convergence Divergence (MACD)**
- **MACD Signal Line**
- **Bollinger Bands**

These indicators help identify:

- Market momentum
- Volatility
- Potential trend reversals

---

### 3. Trading Signal Detection

The project detects potential trading opportunities by identifying **local peaks and dips in stock prices**.

- **Local minimum → Buy signal**
- **Local maximum → Sell signal**

A sliding window algorithm is used to detect these price movements.

---

### 4. Machine Learning Price Prediction

The system includes a machine learning pipeline to predict future stock prices.

**Model Used**

- Random Forest Regressor

**Features Used**

- RSI
- MACD
- Signal Line
- Bollinger Band High
- Bollinger Band Low
- Sentiment Score

**ML Pipeline Components**

- Feature scaling using **StandardScaler**
- Hyperparameter tuning using **GridSearchCV**
- Train/test split for model evaluation

The model also generates **simulated predictions for the next 30 days**.

---

### 5. Sentiment Analysis

The project includes a lightweight sentiment analysis module.

Features:

- Dictionary-based sentiment scoring
- Lorentzian weighting function
- Sentiment classification:
  - Positive
  - Neutral
  - Negative

Sentiment scores are incorporated as an additional feature in the machine learning model.

---

### 6. Interactive Dashboard

An **interactive Streamlit dashboard** allows users to visualize analysis results.

Dashboard features include:

- Stock symbol input
- Date range selection
- Adjustable trading signal window
- Technical indicator visualization
- Buy/Sell signal markers
- Predicted stock price trends

Charts and visualizations are rendered using **Plotly**.

---

### Module Overview

**data_collection.py**

- Fetches historical stock data using the Yahoo Finance API.

**technical_analysis.py**

- Computes technical indicators such as RSI, MACD, and Bollinger Bands.

**trading_signals.py**

- Detects buy/sell signals using peak and dip detection.

**sentiment_analysis.py**

- Calculates sentiment scores from textual inputs.

**model_training.py**

- Trains the Random Forest regression model and generates predictions.

**dashboard.py**

- Implements the interactive Streamlit dashboard.

---

## Installation

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Running the Application

Run the main script:

```bash
python main.py
```

This will launch the **Streamlit dashboard**, where users can analyze stock data interactively.

---

## Example Workflow

1. Enter a stock symbol (example: `RELIANCE.NS`)
2. Select a date range for analysis
3. Adjust the trading signal detection window
4. Click **Analyze**

The system will then:

- Fetch historical market data
- Compute technical indicators
- Perform sentiment analysis
- Train the machine learning model
- Display trading signals and predictions

---

## Technologies Used

### Programming Language

- Python

### Libraries

- Pandas
- NumPy
- Scikit-learn
- TA (Technical Analysis Library)
- Streamlit
- Plotly
- yfinance

---

## Limitations

This project is intended for **educational and experimental purposes**.

Some limitations include:

- Sentiment analysis uses a small dictionary-based approach.
- Predictions rely on historical data and simplified assumptions.
- Future price simulations may not accurately reflect real-world market conditions.

---

## Future Improvements

Possible extensions for the project include:

- Integrating financial news APIs for real-time sentiment analysis
- Implementing deep learning models such as **LSTM** for time-series forecasting
- Adding portfolio optimization tools
- Implementing automated backtesting for trading strategies

---

## References

- Investopedia – Basics of Stock Market
- Screener.in – Stock Fundamentals
- Chartink – Stock Screener
- NSE India
- BSE India

**main.py**

- Installs dependencies and launches the application.
