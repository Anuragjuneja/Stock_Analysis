# Stock Price Prediction,Trend Analysis and Portfolio Optimization

## Project Overview
This project focuses on developing an LSTM-based model to predict stock prices and analyze market trends. The model leverages historical data to forecast future stock prices and assesses the accuracy of trend predictions across different stocks. Additionally, it aids in constructing a less risky portfolio by minimizing variance.

## Features
- **Data Loading:** Load Data from Yahoo Finance.
- **Data Preprocessing:** Scales and reshapes stock data for LSTM input.
- **Model Training:** Trains an LSTM model on historical stock data.
- **Prediction:** Predicts future stock prices and trends.
- **Trend Matching:** Compares predicted trends with actual trends and counts matching trends.
- **Visualization:** Plots the actual vs. predicted stock prices.
- **Portfolio Optimization:** Returns optimized portfolio including few specific stocks

## Main Libraries Used
- Python 3.x
- NumPy
- Pandas
- Scikit-learn
- TensorFlow / Keras
- Matplotlib
- Joblib
- Tabulate

## Data Collection
The data for this project is collected from  Yahoo Finance.

## Model Training and Prediction

### Data Preprocessing:
- Each stock's closing prices are normalized using `MinMaxScaler`.
- Data is split into training (95%) and testing (5%) sets.

### Model Architecture:
- The LSTM model consists of two LSTM layers with 128 and 64 units respectively.
- The model is trained to predict the next day's closing price based on the past 100 days of data.

### Prediction:
- After training, the model is tested on the test data, and predictions are generated.
- The root mean square error (RMSE) is calculated to evaluate the performance.

### Saving Models:
- The trained model and the scalers are saved for future use.

## Trend Analysis
For each stock, the project analyzes the trends (whether the price goes up or down) of the actual and predicted prices:

### Trend Calculation:
- The trends for both actual and predicted prices are calculated using the difference between consecutive days.

### Trend Matching:
- The project compares the trends for the last 50 days and counts how many times the predicted trend matches the actual trend.

## Portfolio Optimization
In addition to stock price prediction, this project also includes portfolio optimization. The goal is to minimize risk (variance) while achieving a user-defined return threshold. The optimization is performed on the following stocks:
- TCS
- NESTLEIND
- TITAN
- ASTRAL
- TATAPOWER
- SUZLON
- HINDPETRO
- HDFCBANK
- INFY
- ULTRACEMCO
- MAHLIFE
- ADANIGREEN
The optimization ensures that the sum of weights equals 1 and that all weights are non-negative, aiming for an optimal balance between risk and return.
## Results
For each stock, the project outputs:
- The RMSE of the model.
- A plot of the actual vs. predicted prices.
- The number of matching trends for the last 50 days.
- The next day's predicted price.
- Optimized Portfolio of above shares


