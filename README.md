# Timeseries-Assigment-

Time series analysis is a statistical technique that deals with time series data, or trend analysis.  Time series data means that data is in a series of  particular time periods or intervals.  The data is considered in three types:

Time series data: A set of observations on the values that a variable takes at different times.

Cross-sectional data: Data of one or more variables, collected at the same point in time.

Pooled data: A combination of time series data and cross-sectional data.


# ARIMA:

ARIMA stands for autoregressive integrated moving average.  This method is also known as the Box-Jenkins method.

Identification of ARIMA parameters:

* Autoregressive component: AR stands for autoregressive.  Autoregressive paratmeter is denoted by p.  When p =0, it means that there is no auto-correlation in the series.  When p=1, it means that the series auto-correlation is till one lag.

* Integrated: In ARIMA time series analysis, integrated is denoted by d.  Integration is the inverse of differencing.  When d=0, it means the series is stationary and we do not need to take the difference of it.  When d=1, it means that the series is not stationary and to make it stationary, we need to take the first difference.  When d=2, it means that the series has been differenced twice.  Usually, more than two time difference is not reliable.

* Moving average component: MA stands for moving the average, which is denoted by q.  In ARIMA, moving average q=1 means that it is an error term and there is auto-correlation with one lag.



In order to test whether or not the series and their error term is auto correlated, we usually use W-D test, ACF, and PACF.


* Decomposition: Refers to separating a time series into trend, seasonal effects, and remaining variabilityAssumptions:

* Stationarity: The first assumption is that the series are stationary.  Essentially, this means that the series are normally distributed and the mean and variance are constant over a long time period.

* Uncorrelated random error: We assume that the error term is randomly distributed and the mean and variance are constant over a time period.  The Durbin-Watson test is the standard test for correlated errors.

* No outliers: We assume that there is no outlier in the series.  Outliers may affect conclusions strongly and can be misleading.

* Random shocks (a random error component): If shocks are present, they are assumed to be randomly distributed with a mean of 0 and a constant variance.


# Auto Regressive Moving Average(ARMA) Models


ARMA model is simply the merger between AR(p) and MA(q) models:


* AR(p) models try to explain the momentum and mean reversion effects often observed in trading markets (market participant effects).

* MA(q) models try to capture the shock effects observed in the white noise terms. These shock effects could be thought of as unexpected events affecting the observation process e.g. Surprise earnings, wars, attacks, etc.

ARMA model attempts to capture both of these aspects when modelling financial time series. ARMA model does not take into account volatility clustering, a key empirical phenomena of many financial time series which we will discuss later.
ARMA(1,1) model is:


x(t) = a*x(t-1) + b*e(t-1) + e(t)
is e(t) white noise with E[e(t)] = 0

An ARMA model will often require fewer parameters than an AR(p) or MA(q) model alone. That is, it is redundant in its parameters.
