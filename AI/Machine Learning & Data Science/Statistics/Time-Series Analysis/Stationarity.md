In time-series data, stationarity refers to the assumption that the statistical properties of the data such as mean, variance, and autocorrelation are constant over time. Many statistical models and machine learning algorithms assume or require the time series data to be stationary before making predictions or extracting meaningful insights.
## Stationarity Test
There are more quantitative techniques to determine if the data is stationary, rather than visual analysis. 
The most famous method is the [[Augmented Dickey-Fuller (ADF) test]]. This is a statistical hypothesis test where the null hypothesis is the series is non-stationary (also known as the unit root test).
## Differencing
Differencing (i.e., taking the difference between the data at $t_{i}$ and $t_{i-1}$) is often used to achieve stationarity in a time series dataset. However, this usually removes the changing mean, but not necessarily the changing variance or seasonality, if present.
## Log Transform
Using the log-transform of the data, on the other hand, removes the change in variance, but not necessarily the change in mean over time.
## Log + Difference Transform
Combining these approaches can lead to a stationary dataset in both mean and variance. Always apply the log transformation first to stabilize the variance, then follow up with differencing to stabilize the mean.

