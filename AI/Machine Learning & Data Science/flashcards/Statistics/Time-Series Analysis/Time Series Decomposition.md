#flashcards

What is time-series decomposition?
?
Time-series decomposition is a technique used to break down a time series into its underlying components: trend, seasonality, and residual noise, making it easier to analyze and understand patterns over time.

What are the three key components of time-series decomposition?
?
1. Trend (T): Long-term movement or direction in data. 2. Seasonality (S): Short-term regular patterns that repeat at fixed intervals. 3. Residual (R): The remaining part of the series after removing trend and seasonality, representing random variations.

What is the difference between additive and multiplicative decomposition models?
?
In an additive model, the components add together to form the observed data (Y_t = T_t + S_t + R_t). In a multiplicative model, the components multiply together (Y_t = T_t × S_t × R_t). Additive is used when variations are constant, while multiplicative is used when they grow or shrink proportionally with the level of the time series.

When would you use an additive decomposition model?
?
An additive decomposition model is suitable when the seasonal fluctuations and the residual noise remain relatively constant over time, indicating that both trend and seasonality have an additive nature.

When is a multiplicative decomposition model more appropriate?
?
A multiplicative decomposition model is more appropriate when the seasonal effects or trend fluctuate proportionally with the level of the time series, such as when seasonal variations increase as the series trends upward.

How can you convert a multiplicative model to an additive model?
?
You can convert a multiplicative model to an additive one by applying a logarithmic transformation, as it changes the multiplication of components into an addition: log(Y_t) = log(T_t) + log(S_t) + log(R_t).

What is the first step in the classical approach to time-series decomposition?
?
The first step is to compute the trend component, T, using a moving or rolling average.

How do you de-trend a series in an additive model?
?
In an additive model, you de-trend the series by subtracting the trend component from the original series: Y - T.

Describe the process of computing the seasonal component in time-series decomposition.
?
The seasonal component, S, is computed by taking the average of the de-trended series for each season.

What formula is used to calculate the residual component in an additive decomposition model?
?
In an additive model, the residual component R is calculated as R = Y - T - S.

What is an alternative transformation to logarithmic transformation for converting multiplicative models to additive models?
?
A Box-Cox transformation can also be used on a multiplicative model to remove non-stationarity in variance and achieve an additive form.

