# TimeSeries
# Overview
As is known to all, San Francisco is one of the cities with the highest home price among the US. This project mainly aims to produce reliable forecasts of time series data utilizing median signal family home price data for San Francisco from 1996 to 2018, provided by Zillow datasets. Two prediction models for housing prices are build, simple time series forecast model and simple linear regression model. The performances of two models are compared.

# Time series forecasting
One of the most commonly used method for time-series forecasting, known as ARIMA is applied in the project. Before building the model, firstly we should take a look at the components of our time series data, trend, seasonality and noise. Based on the decomposition plots (Figure1), we can see that there is clearly an upward trend in the above plot. Also, the uniform seasonal change is clear. Non-uniform noise represents outliers and missing values.

Then, when looking to fit time series data with a seasonal ARIMA model, our first goal is to find the values of ARIMA(p,d,q)(P,D,Q)s that optimize a metric of interest. This issue is resolved by writing Python code to programmatically select the optimal parameter values for our ARIMA(p,d,q)(P,D,Q)s time series model. The output of the code suggests that SARIMAX (1, 1, 1)x(1, 1, 1, 12) yields the lowest AIC value of 4824.64. Therefore, this SARIMAX is considered to be optimal option out of all the models we have considered.
