The Normal Distribution, or Gaussian Distribution, is a continuous probability distribution that has a bell-shaped curve. It is one of the most important and widely used statistical distributions due to its properties and natural occurrence in different phenomena. 

In a Normal Distribution, the data tends to be centered around the mean, forming a bell-shaped curve where approximately 68% of values fall within one standard deviation of the mean, about 95% fall within two standard deviations, and roughly 99% fall within three standard deviations.

The Normal Distribution is modelled by $N(\mu, \sigma^2)$, where $\mu$ is the [[AI/Machine Learning & Data Science/Probability/Basics#Expected Value|mean or expectation]] of the distribution (and also its [[AI/Machine Learning & Data Science/Probability/Basics#Median|median]] and [[AI/Machine Learning & Data Science/Probability/Basics#Mode|mode]]), and $\sigma^2$ is its [[AI/Machine Learning & Data Science/Probability/Basics#Variance|variance]]. The formula for the PDF of the Normal Distribution is then:
$$
f(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-(x-\mu)^2 / 2\sigma^2}
$$
### Standard Normal Distribution
The Standard Normal Distribution, also known as the Z-distribution, is a special case of the normal distribution where the mean $\mu$ is zero and the standard deviation $\sigma$ is one. The PDF formula can be modified if this is the case:
$$
f(z) = \frac{1}{\sqrt{2\pi}} e^{-z^2 / 2}
$$
A distribution can be standardised by subtracting the mean and dividing by the standard deviation. The new distribution can be used to derive the Z-score of a datapoint and compare it to different distributions.
## Sum of Gaussians
In general, if you have independent Gaussian distributions $X \sim N(\mu_{X}, \sigma^2_{X})$ and $Y \sim N(\mu_{Y}, \sigma^2_{Y})$, then the sum $W \sim N(a\mu_{X} + b\mu_{Y}, a^{2}\sigma^{2_{X}}+ b^{2}\sigma^2_{X})$.