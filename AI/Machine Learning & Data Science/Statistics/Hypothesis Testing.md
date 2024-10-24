Hypothesis testing is a fundamental method in statistics used to determine if there is enough evidence in a sample of data to infer that a certain condition is true for the entire population.
## Null Hypothesis 
The Null Hypothesis ($H_0$​) is statement of no effect or no difference. It is the hypothesis that the researcher tries to disprove.
## Alternative Hypothesis
The Alternative Hypothesis ($H_1$ or $H_a$​) is a statement that indicates the presence of an effect or a difference. It is what the researcher wants to prove.

The Null Hypothesis and Alternative Hypothesis are mutually exclusive.
The aim is to either reject or accept the Null Hypothesis.
## Type I Error ($\alpha$)
Incorrectly rejecting the null hypothesis when it is true (false positive). Generally worse than a type II error.
## Type II Error ($\beta$)
Failing to reject the null hypothesis when it is false (false negative).
## Significance Level ($\alpha$):
The probability of rejecting the null hypothesis when it is actually true (Type I error). Essentially the greatest probability of type I error you are willing to tolerate in your model. $\alpha = 0$ would mean having no type I error, i.e., no false positives (high precision, low recall).
Commonly used values are $0.05$, $0.01$, and $0.10$.
## One-tailed test
Tests the direction of the effect (greater than or less than a certain value).
### Right-tailed vs Left tailed
There are two categories of one-tailed tests, namely, the right-tailed test and the left-tailed test. A right-tailed test is used when the alternative hypothesis suggests that the mean of a sample will be greater than the mean of the population. A left-tailed test simply tests the opposite. 

For example, if a school district wanted to investigate whether their new math curriculum has led to a decrease in average test scores (<70%), they would use a left-tailed test, where $H_0$ states that the mean $\mu$ is equal to the average test score before the new curriculum ($H_{0}: \mu = 60$), and $H_{1}$ states that the mean $\mu$ is less than the average test score before the new curriculum ($H_{1} : \mu < 60$). Note that the hypothesis are formulated using the population mean, not sample mean.

![[Pasted image 20240720131107.png]]
In the diagram above the test statistic is calculated using the Z-statistic equation, and is 1.837 (the value of the y-axis when x=68.442). The value 0.0332 is the p-value, and is simply the probability of $\bar{X}$ being above 
## Two-tailed test
Tests for any effect, regardless of the direction (different from a certain value).
## Test Statistic
A test statistic is a standardised value calculated from sample data during a hypothesis test. It measures the degree of agreement between a sample statistic and the null hypothesis.
### Types
 - [[AI/Machine Learning & Data Science/Probability/Distributions/Normal Distribution#Standard Normal Distribution|Z-statistic]]: Used when population variance is known and the sample size is large. 
   $$z = \frac{\bar{x} - \mu}{\sigma / \sqrt{n}}$$
   
- [[T-Distribution|t-statistic]]: Used when population variance is unknown and the sample size is small. $$t = \frac{\bar{x} - \mu}{s / \sqrt{n}}$$
 - [[AI/Machine Learning & Data Science/Probability/Distributions/Chi-Squared Distribution|Chi-square statistic]]: Used for categorical data. $$\chi^2 = \sum \frac{(O_i - E_i)^2}{E_i}$$
- **Example**: If you are testing whether the mean height of students differs from a specified value, the test statistic helps determine how far the sample mean deviates from this value under the null hypothesis.
## Observed Statistic
The observed statistic is the actual calculated value from the sample data. It is the value that you compare against a theoretical distribution to determine the p-value.

 - **Example**: In a t-test, after calculating the t-statistic using sample data, the observed t-statistic is the specific numerical value obtained. This value is then compared to the critical t-value to decide whether to reject the null hypothesis.
## P-Value 
The p-value is a measure used in statistical hypothesis testing to help determine the significance of the observed results. It quantifies the probability of obtaining a test statistic at least as extreme as the one observed, assuming that the null hypothesis (H0H_0H0​) is true.
![[Pasted image 20240720131318.png|centered]]

## Critical Values
Critical values are the threshold values that define the boundaries of the acceptance region and the rejection region in a statistical hypothesis test. They are determined based on the chosen significance level ($\alpha$) and the sampling distribution of the test statistic. 
![[Pasted image 20240721134953.png|centered]]

## Power of the Test
The power of a statistical test is the probability that the test correctly rejects a false null hypothesis (i.e., it avoids a Type II error). It measures the test's ability to detect an effect when there is one.

The power of the test is given by:
$$\text{Power} = 1 - \beta$$
where $\beta$ is the probability of making a Type II error (failing to reject a false null hypothesis). 
- A higher power means a greater chance of detecting an effect when it exists.
- Power is used to determine the sample size needed for a study to reliably detect an effect.
## Paired t-Test
A paired t-test is a statistical method used to compare the means of two related groups. It is often used in "before-and-after" studies, or when the same subjects are measured under two different conditions. 

The paired t-test evaluates whether the mean difference between paired observations is significantly different from zero.
- **Dependent Samples**: The observations in each pair must be related (e.g., measurements from the same subject).
- **Normal Distribution**: The differences between the paired observations should be approximately normally distributed.
- **Continuous Data**: The data should be continuous.
#### Hypotheses
- **Null Hypothesis ($H_0$)**: The mean difference between the paired observations is zero ($\mu_D = 0$).
- **Alternative Hypothesis ($H_1$​ or $H_a$​)**: The mean difference between the paired observations is not zero ($\mu_D \neq 0$) for a two-tailed test, or greater than/less than zero for a one-tailed test.

The observed statistic can be calculated based on the sample mean and sample variance of the differences:
$$
t = \frac{\bar{D} - \mu_{D}}{S_{D}/\sqrt{n}}
$$
Where
 - $\bar{D}$ is the average of the differences in corresponding samples in the two groups.
 - $S_{D}$ is the variance of the differences. 
 - $\mu_{D}$ is the population mean (0 if your $H_{0}$ is that there was no change).
 - $n$ is the number of samples.
