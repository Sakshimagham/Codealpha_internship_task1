# Codealpha_internship_task1

Stock Price Prediction using LSTM

📌 Project Overview

This project aims to predict stock prices using Long Short-Term Memory (LSTM), a type of recurrent neural network (RNN) that is well-suited for time series forecasting. We leverage historical stock market data, preprocess it, train an LSTM model, and predict future stock prices.


📊 Dataset

The stock data is retrieved using the yfinance library, which provides historical price data including:

Date: Trading date (index)

Open: Opening price of the stock

High: Highest price of the day

Low: Lowest price of the day

Close: Closing price of the stock

Adj Close: Adjusted closing price (considering stock splits/dividends)

Volume: Number of shares traded


📅 Data Range

Start Date: January 1, 2024
End Date: Latest Available Date (Dynamic)


🛠️ Technologies Used

yfinance: Fetches stock data.

tensorflow: Loads machine learning models.

pandas: Handles data manipulation.

datetime: Manages date-related operations.

sklearn.preprocessing.MinMaxScaler: Normalizes stock prices.

numpy: Handles numerical operations.

Sequential, LSTM, Dense, Dropout: TensorFlow layers for LSTM model creation.

matplotlib.pyplot: Used for data visualization.


🚀 Implementation Steps

1️⃣ Data Collection

- Retrieve stock market data using yfinance.download()

2️⃣ Data Preprocessing

- Normalize data using MinMaxScaler to scale values between 0 and 1
- Split dataset into 80% training and 20% testing
- Create input-output sequences for LSTM (using the past 60 days to predict the next day)
- Convert sequences into NumPy arrays and reshape for LSTM input

3️⃣ Model Building

- Construct a sequential LSTM model with:
- Two LSTM layers (50 units each)
- Dropout layers (to prevent overfitting)
- Dense output layer (predicting stock price)
- Compile using Adam optimizer and Mean Squared Error (MSE) loss
- Train the model for 50 epochs with batch size 32

4️⃣ Prediction & Forecasting

- Use the trained model to predict stock prices
- Forecast the next 30 days of stock prices
- Convert predictions back to original scale using inverse_transform()


Plot actual vs. predicted stock prices

📈 Results & Visualization :

The predicted prices are plotted against actual stock prices.

Future stock prices for 30 business days are forecasted.

