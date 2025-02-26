#flashcards

What does stationarity refer to in time-series data?
?
Stationarity refers to the assumption that the statistical properties of the data, such as mean, variance, and autocorrelation, are constant over time.

Why is stationarity important in time-series analysis?
?
Many statistical models and machine learning algorithms assume or require the time series data to be stationary before making predictions or extracting meaningful insights.

What is the Augmented Dickey-Fuller (ADF) test used for?
?
The ADF test is used to determine if a time series is stationary, where the null hypothesis is that the series is non-stationary.

What does differencing do in a time series dataset?
?
Differencing takes the difference between data at $t_{i}$ and $t_{i-1}$ and is used to achieve stationarity, removing the changing mean.

What is a downside of differencing in terms of variance and seasonality?
?
Differencing usually removes the changing mean but does not necessarily address changing variance or seasonality.

What is the effect of applying a log transformation to time series data?
?
The log transformation removes the change in variance but does not necessarily stabilize the mean over time.

How can you achieve a stationary dataset in both mean and variance?
?
By applying the log transformation first to stabilize the variance, and then differencing to stabilize the mean.

What is the null hypothesis in the ADF test?
?
The null hypothesis in the ADF test is that the series is non-stationary.

When analyzing time-series data, what should you do if the data is not stationary?
?
You can apply techniques like differencing, log transformation, or a combination of both to achieve stationarity.

Explain the process of combining log transformation and differencing.
?
First, apply the log transformation to stabilize variance, and then apply differencing to stabilize the mean.

