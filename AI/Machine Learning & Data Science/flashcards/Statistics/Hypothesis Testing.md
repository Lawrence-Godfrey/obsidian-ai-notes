#flashcards

What is hypothesis testing in statistics?
?
Hypothesis testing is a fundamental method in statistics used to determine if there is enough evidence in a sample of data to infer that a certain condition is true for the entire population.

What is the Null Hypothesis ($H_0$)?
?
The Null Hypothesis ($H_0$) is a statement of no effect or no difference, and it is the hypothesis that the researcher tries to disprove.

What is the Alternative Hypothesis ($H_1$ or $H_a$)?
?
The Alternative Hypothesis ($H_1$ or $H_a$) indicates the presence of an effect or a difference, which is what the researcher aims to prove.

Explain the relationship between Null and Alternative Hypotheses.
?
The Null Hypothesis and Alternative Hypothesis are mutually exclusive. The aim is to either reject or accept the Null Hypothesis.

What is a Type I Error ($\alpha$)?
?
A Type I Error is incorrectly rejecting the null hypothesis when it is true (false positive). It is generally considered worse than a Type II error.

What is a Type II Error ($\beta$)?
?
A Type II Error is failing to reject the null hypothesis when it is false (false negative).

What does the significance level ($\alpha$) represent in hypothesis testing?
?
The significance level ($\alpha$) represents the probability of rejecting the null hypothesis when it is actually true, and it indicates the greatest probability of Type I error that a researcher is willing to tolerate.

What are common values used for the significance level ($\alpha$)?
?
Common values for the significance level are $0.05$, $0.01$, and $0.10$.

What is a one-tailed test?
?
A one-tailed test tests the direction of the effect (either greater than or less than a certain value).

What is the difference between a right-tailed test and a left-tailed test?
?
A right-tailed test is used when the alternative hypothesis suggests that the mean of a sample will be greater than the mean of the population, while a left-tailed test indicates the mean will be less than the population mean.

Provide an example of when to use a left-tailed test.
?
If a school district wanted to investigate whether their new math curriculum leads to a decrease in average test scores (less than 70%), they would use a left-tailed test.

What is a Two-tailed test?
?
A two-tailed test tests for any effect, regardless of the direction (different from a certain value).

Define a test statistic.
?
A test statistic is a standardized value calculated from sample data during a hypothesis test that measures the degree of agreement between a sample statistic and the null hypothesis.

What is the Z-statistic used for?
?
The Z-statistic is used when the population variance is known and the sample size is large.

What formula is used to calculate a Z-statistic?
?
$$ z = \frac{\bar{x} - \mu}{\sigma / \sqrt{n}} $$.

When is the t-statistic used?
?
The t-statistic is used when the population variance is unknown and the sample size is small.

What formula is used to calculate a t-statistic?
?
$$ t = \frac{\bar{x} - \mu}{s / \sqrt{n}} $$.

What is the Chi-square statistic used for?
?
The Chi-square statistic is used for categorical data, calculated as $$ \chi^2 = \sum \frac{(O_i - E_i)^2}{E_i} $$.

How is the observed statistic defined?
?
The observed statistic is the actual calculated value from the sample data that is compared against a theoretical distribution to determine the p-value.

What does the p-value measure in hypothesis testing?
?
The p-value measures the probability of obtaining a test statistic at least as extreme as the one observed, assuming the null hypothesis ($H_0$) is true.

What are critical values in a hypothesis test?
?
Critical values are threshold values that define the boundaries of the acceptance region and the rejection region in a hypothesis test, determined by the chosen significance level ($\alpha$) and the sampling distribution of the test statistic.

What is the power of a statistical test?
?
The power of a statistical test is the probability that the test correctly rejects a false null hypothesis, thereby avoiding a Type II error.

How do you calculate the power of a test?
?
Power is calculated as $$\text{Power} = 1 - \beta$$, where $\beta$ is the probability of making a Type II error.

What is a paired t-test?
?
A paired t-test is a statistical method used to compare the means of two related groups, often used in 'before-and-after' studies.

What are the hypotheses in a paired t-test?
?
The Null Hypothesis ($H_0$): The mean difference between the paired observations is zero ($\mu_D = 0$). The Alternative Hypothesis ($H_1$): The mean difference is not zero ($\mu_D \neq 0$) for a two-tailed test.

What is the formula for the t statistic in a paired t-test?
?
$$ t = \frac{\bar{D} - \mu_{D}}{S_{D}/\sqrt{n}} $$, where $\bar{D}$ is the average of the differences, $S_{D}$ is the variance of the differences, $\mu_{D}$ is the population mean, and $n$ is the number of samples.

