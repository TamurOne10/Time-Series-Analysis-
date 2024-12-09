Time Series Analysis of Alibaba Stock Price
Project Overview
This project performs time series analysis on Alibaba's stock price, specifically focusing on the "Adj Close" column from historical stock data. We use a variety of statistical and machine learning techniques to explore trends, seasonality, and predict future stock prices. The analysis includes data visualization, stationarity testing, autocorrelation, seasonal decomposition, and forecasting using ARIMA and SARIMA models.

Data Description
The dataset used in this analysis contains daily stock price data for Alibaba (BABA) from January 2020 to April 2024, with the following columns:

Date: Date of the stock price entry.
Open: Opening price for the day.
High: Highest price reached during the day.
Low: Lowest price reached during the day.
Close: Closing price for the day.
Adj Close: Adjusted closing price (taking into account stock splits and dividends).
Volume: The number of shares traded during the day.
Libraries Used
pandas: Data manipulation and analysis.
numpy: Mathematical operations.
matplotlib: Data visualization.
seaborn: Statistical data visualization.
statsmodels: Statistical models and time series analysis.
ac and pacf plots: Autocorrelation and partial autocorrelation for model selection.
Steps in the Analysis
Data Loading and Preprocessing:

The dataset is loaded using pandas.read_csv().
We check for missing values and data types using df.isnull().sum() and df.info().
Stationarity Check:

We perform an Augmented Dickey-Fuller (ADF) test to check if the stock price data is stationary.
If the data is not stationary, we use seasonal decomposition to remove trends and seasonality.
Seasonal Decomposition:

The time series is decomposed into trend, seasonality, and residuals using seasonal_decompose() from statsmodels.
Autocorrelation and Partial Autocorrelation:

Autocorrelation and partial autocorrelation plots are generated using plot_acf() and plot_pacf() to determine appropriate values for AR (Auto-Regressive) and MA (Moving Average) terms in ARIMA models.
ARIMA and SARIMA Modeling:

ARIMA and SARIMA models are fitted to the data. We use the SARIMAX model from statsmodels for forecasting. The model is chosen based on autocorrelation plots and stationarity of the data.
Predictions for future stock prices are made, and the results are plotted alongside the actual data.
Model Evaluation and Visualization:

The forecasted stock prices are plotted with the actual stock prices to visually evaluate the model's performance.
Key Results
The dataset is found to be non-stationary based on the ADF test.
After performing seasonal decomposition and differencing, the stationarity issue is addressed.
The SARIMAX model with parameters (p=1, d=3, q=2) is fitted to the data, and forecasted values are plotted.
Requirements
To run this project, you need the following libraries:

pandas
numpy
matplotlib
seaborn
statsmodels
You can install them via pip:

bash
Copy code
pip install pandas numpy matplotlib seaborn statsmodels
Conclusion
This project demonstrates the process of time series analysis on Alibaba stock price data, including model selection and forecasting. The SARIMAX model provides valuable insights into future stock price trends, which can be used for trading strategies or financial analysis.
