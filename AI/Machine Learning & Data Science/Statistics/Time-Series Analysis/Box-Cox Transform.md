The **Box-Cox transform** is a statistical technique used to stabilise variance (see [[Stationarity]]) and make data more closely resemble a [[AI/Machine Learning & Data Science/Probability/Distributions/Normal Distribution|Normal Distribution]], which is often required for certain statistical models and tests. It transforms non-normal dependent variables into a normal shape by applying a power transformation.

The Box-Cox transformation is defined as:

$$y(\lambda) = \begin{cases} \frac{y^{\lambda} - 1}{\lambda}, & \text{if } \lambda \neq 0, \\ \log(y), & \text{if } \lambda = 0. \end{cases}​$$
where:
- $y$ is the original data,
- $\lambda$ is the transformation parameter that determines the nature of the transformation.

### Key Points:
1. **Parameter $\lambda$**:
    - The parameter $\lambda$ controls the transformation. The value of $\lambda$ is typically chosen by maximising the likelihood of a model (e.g., maximising the log-likelihood in a regression setting).
    - Common values of $\lambda$:
        - $\lambda = 1: No transformation (linear),
        - $\lambda = 0$: Logarithmic transformation,
        - $\lambda = 0.5$: Square root transformation,
        - $\lambda = -1$: Reciprocal transformation.
2. **Purpose**:
    - The primary aim of the Box-Cox transformation is to make the data distribution more normal (Gaussian), which is often a requirement for many statistical tests and models (like linear regression).
    - It can also be used to stabilise variance, which can improve the performance of certain models.
3. **Limitations**:
    - It only works on positive data since the log transformation (used when $\lambda = 0$) is undefined for zero or negative values.

In practice, the **optimal value of $\lambda$** is typically estimated from the data to achieve the best possible transformation.