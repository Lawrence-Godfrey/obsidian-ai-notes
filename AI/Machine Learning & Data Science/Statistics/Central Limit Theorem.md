The Central Limit Theorem (CLT) is a fundamental concept in statistics that states that when an adequately large number of independent, identically distributed random variables are added, their properly normalised sum tends toward a [[Normal Distribution]], regardless of the shape of the original distribution.

For example, if we sample 20 points from a uniform distribution, find the mean of the 20 samples, and then plot that on a histogram, over and over, the means in the histogram will slowly take the shape of a normal distribution. This is the same for any distribution.
## Rule of Thumb
There is a rule of thumb which states that the sample size must be at least 30 in order for CLT to work properly. 
## Practical Example
Consider a population with a mean $\mu = 100$ and standard deviation $\sigma = 15$, which is not normally distributed (it could be skewed or uniform).
1. **Draw a Sample**: Take a random sample of size $n = 50$.
2. **Sample Mean**: Calculate the sample mean $\bar{X}$.
3. **Repeat**: Repeat this process many times to get the sampling distribution of the sample mean.
According to the CLT, as the sample size $n$ becomes large, the distribution of $\bar{X}$ will approach a normal distribution with mean $\mu$ and standard deviation $\frac{\sigma}{\sqrt{n}}$.
## Use Cases
The CLT is useful because it allows us to use tools like [[Confidence Intervals]], [[Hypothesis Testing#Test Statistic|T-tests]], [[ANOVA]], etc., even when the original data does not follow a normal distribution.

