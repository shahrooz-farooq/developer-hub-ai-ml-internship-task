# Task 2: Stock Price Prediction

## Task Objective
The objective of this task is to predict the closing price of Apple (AAPL) stock using machine learning regression model. The model learns from historical stock data (Open, High, Low, Volume) to forecast future closing prices.

## Dataset Used
- **Dataset Name**: Apple (AAPL) Historical Stock Data
- **Source**: Yahoo Finance (via yfinance library)
- **Time Period**: January 1, 2022 to January 1, 2025
- **Data Frequency**: Daily OHLC (Open, High, Low, Close) prices and Volume
- **Total Samples**: Approximately 755 trading days

### Features Used:
- **Input Features (X)**:
  - Open: Opening price of the stock
  - High: Highest price during the day
  - Low: Lowest price during the day
  - Volume: Number of shares traded
  
- **Target Variable (y)**:
  - Close: Closing price of the stock (what we predict)

## Data Preparation
1. Downloaded Apple stock data from Yahoo Finance API
2. Selected features: Open, High, Low, Volume as inputs
3. Target: Close price as output
4. Split data: 80% training (604 days) and 20% testing (151 days)
5. Random state set to 42 for reproducibility

## Model Applied
**Linear Regression**
- **Type**: Supervised Learning, Regression
- **Algorithm**: Ordinary Least Squares (OLS)
- **Why Linear Regression**: Simple baseline model to understand linear relationships between stock features and closing price

## Model Training
- Trained on 80% of historical data (2022-2024)
- Tested on remaining 20% of data
- Model learns the linear relationship between OHLC features and closing price

## Results
- **Predictions**: Model generates closing price predictions for test data (151 days)
- **Visualization**: Actual vs Predicted closing prices plotted for visual comparison
- **Pattern**: Graph shows how closely predicted prices match actual market prices

## Key Findings
1. Linear Regression provides a baseline prediction model for stock prices
2. Stock closing price shows linear relationship with Open, High, Low prices and Volume
3. The model captures general trends in stock price movements
4. For more accurate predictions, consider:
   - Technical indicators (RSI, MACD, Moving Averages)
   - Sentiment analysis from news and social media
   - External factors (market conditions, economic indicators)
   - Advanced models (LSTM, Prophet, Ensemble methods)

## Limitations
- Linear Regression assumes linear relationships which may not capture complex stock market dynamics
- Stock prices are influenced by external factors not captured in OHLC data
- Past performance does not guarantee future results
- Model should not be used for real trading decisions without further validation

## Libraries Used
- **yfinance**: Download stock data from Yahoo Finance
- **sklearn.model_selection**: Train-test split for data partitioning
- **sklearn.linear_model**: Linear Regression model
- **matplotlib**: Visualization of predictions

## Files in This Task
- `task2_stock_price_prediction.py`: Main Python script for stock price prediction

## How to Run
```bash
python task2_stock_price_prediction.py
```

## Output
- Actual vs Predicted stock prices plotted in a line graph
- Visual comparison shows model's prediction accuracy on test data
