**Time-series decomposition** is a technique used to break down a time series into its underlying components, making it easier to analyse and understand patterns over time (See [[Stationarity]]). The basic idea is to decompose the time series into three key components:

1. **Trend (T)**: The long-term movement or direction in the data.
2. **Seasonality (S)**: Short-term regular patterns or cycles in the data that repeat at fixed intervals (e.g., monthly, quarterly, or yearly).
3. **Residual or Noise (R)**: The remaining part of the series after removing the trend and seasonality, representing random variation or irregular patterns.
## Additive vs. Multiplicative Decomposition:
- **Additive Model**: Assumes that the components add together to form the observed data: $$Y_t = T_t + S_t + R_t$$This model works best when the seasonal fluctuations and the residual noise remain relatively constant over time, meaning that both trend and seasonality have an additive nature.
- **Multiplicative Model**: Assumes that the components multiply together to form the observed data:
   $$Y_t = T_t \times S_t \times R_t$$
   This model is better suited when the seasonal effects or trend grow or shrink proportionally with the level of the time series. For example, if the seasonal variations get larger as the series trends upwards, the multiplicative model is a better fit.
## Converting Additive to Multiplicative and Vice Versa:
- You can convert a **multiplicative** model to an **additive** one by applying a logarithmic transformation. This is because: $$\log(Y_t) = \log(T_t \times S_t \times R_t) = \log(T_t) + \log(S_t) + \log(R_t)$$In this form, the components are now additive, and standard techniques for additive decomposition can be used. A [[Box-Cox Transform]] can also be used on a multiplicative model to remove the non-stationarity in the variance, which accomplishes the same thing.
## How it Works
The following is the classical/fundamental approach to decomposition:
1. Compute the trend component, $T$, using a moving/rolling average.
2. De-Trend the series ($Y-T$ for additive models, $\frac{Y}{T}$ for multiplicative models.
3. Compute the seasonal component, $S$, by taking the average of the de-trended series of each season.
4. The residual component, $R$, is calculated as $R = Y - T - S$ for additive models and $R= \frac{Y}{TS}$ for multiplicative models. 
