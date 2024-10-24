A confidence interval (CI) is a range of values used to estimate a population parameter. It is derived from sample data and provides an interval within which the parameter is expected to lie with a certain level of confidence.
### Key Concepts
1. **Point Estimate**: A single value estimate of a population parameter (e.g., sample mean).
2. **Confidence Level**: The probability that the confidence interval contains the true parameter. Common levels are 90%, 95%, and 99%.
3. **Margin of Error**: The range above and below the point estimate within which the true parameter is expected to lie.
### Equation
For the Mean (when population standard deviation $\sigma$ is known):
$$
CI=\bar{x}\pm Z_{\alpha/2​}\frac{\sigma}{​\sqrt{n}}​
$$
Where
- $\bar{x}$ is the sample mean.
- $Z_{\alpha/2​}$ is the critical value from the [[AI/Machine Learning & Data Science/Probability/Distributions/Normal Distribution#Standard Normal Distribution|standard normal distribution]] for the desired confidence level.
- $\sigma$ is the population standard deviation.
- $n$ is the sample size.
- $\frac{\sigma}{​\sqrt{n}}$ is the margin of error.

This makes the assumption that:
 - Simple random samples are used (i.e., random, with each sample having an equal chance of being selected).
 - Sample sizes > 30 or population is approximately normal.
 - The population standard deviation is known.
 
The term $\frac{\sigma}{\sqrt{n}}$ is the same term used to calculate the standard deviation of the resulting distribution in the [[AI/Machine Learning & Data Science/Statistics/Central Limit Theorem|Central Limit Theorem]]. The confidence interval calculation essentially just uses the CLT with a scaling parameter $\alpha$ and applies it to a number of samples.

In reality, the population standard deviation is not always known, in which case we use the sample standard deviation $s$ instead. When the population standard deviation is unknown and we use the sample standard deviation, we need to use a [[T-Distribution]] instead of a z-distribution.

The equation becomes:
$$
CI=\bar{x}\pm t_{\alpha/2​}\frac{s}{​\sqrt{n}}​
$$
## Confidence Intervals for Proportions
Confidence intervals can also be used when proportions are being measured. For example, finding the proportion $\hat{p}$ of samples $x$ with some property over the entire sample set of size $n$.

$$
CI=\bar{x}\pm Z_{\alpha/2​}\sqrt{\frac{\hat{p}(1-\hat{p})}{​n}}
$$
