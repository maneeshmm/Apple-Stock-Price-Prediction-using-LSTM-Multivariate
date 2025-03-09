# Apple Stock Price Prediction Using LSTM (Multivariate)

## 1. Introduction

Stock market prediction is a challenging task due to the dynamic nature of financial markets. In this project, we use Long Short-Term Memory (LSTM), a type of Recurrent Neural Network (RNN), to predict Apple Inc.'s stock prices based on multiple features (Multivariate analysis). The primary objective is to develop a robust model that can predict future stock prices using historical data.

## 2. Data Preprocessing

The dataset used in this project is Apple Inc.'s historical stock data, which includes:

Date: The date of the recorded stock prices.

Open Price: The price of the stock at the market's opening.

High Price: The highest price the stock reached during the trading session.

Low Price: The lowest price the stock traded at during the session.

Close Price: The final price at which the stock was traded before the market closed.

Adj Close Price: The closing price adjusted for corporate actions like stock splits and dividends.

Volume: The number of shares traded during the day.

Data Cleaning & Transformation

Loading Data: The dataset is read using Pandas.

Handling Missing Values: The dataset is checked for missing values.

Date Conversion & Indexing: The Date column is converted to DateTime format and set as the index.

Sorting: The data is sorted chronologically.

Data Normalization: The MinMaxScaler from sklearn.preprocessing is used to normalize all numerical values to a range of [0,1] to enhance model efficiency.

## 3. Feature Engineering

To create meaningful features for training the model, we:

Use a sliding window technique to generate input sequences (time steps) for LSTM.

Define a method to create historical sequences of stock prices.

Split the dataset into training and testing sets (typically 80-20 split).

## 4. LSTM Model Architecture

LSTM Network Structure

A Sequential LSTM model is built using Keras, consisting of:

LSTM Layers: Three stacked LSTM layers with a specified number of units.

Dropout Layers: Dropout is applied to prevent overfitting.

Dense Output Layer: A fully connected Dense layer is added for prediction.

## 5. Model Training & Evaluation

Training Process

The model is compiled using an optimizer and a loss function.

The training is done for a specified number of epochs with batch size optimization.

The dataset is split into training (80%) and testing (20%).

Evaluation Metrics

The model's performance is evaluated using:

Mean Squared Error (MSE)

Root Mean Squared Error (RMSE)

Mean Absolute Percentage Error (MAPE)

## 6. Results & Visualization

The predicted vs actual stock prices are plotted to visualize model performance.

The error metrics are calculated to analyze the accuracy of predictions.

## 7. Conclusion

The LSTM model successfully captures patterns in Apple stock prices. However, model performance can be improved by:

Increasing training data.

Optimizing hyperparameters.

Experimenting with bidirectional LSTMs.

Incorporating external features like market indices, sentiment analysis, and news data.

This project demonstrates the potential of deep learning in financial forecasting and provides insights into multivariate time-series prediction using LSTM.
