## Population and Sample
In statistics, **population** refers to the entire group of individuals or objects that you are interested in studying, while **sample** refers to a subset of the population that is selected for the study.

Some rules about selecting a sample:
1. Sample randomly, not selectively: Random sampling is a basic principle in statistical analysis.
2. Samples should be independent: E.g., your second sample shouldn't exclude individuals because they were in your first sample.
3. Samples should be identically distributed: This means that each sample or observation should come from the same probability distribution.
The last 2 rules is often referred to as i.i.d, e.g., the samples should be i.i.d.

In machine learning, a dataset is essentially a sample of a population. For example, if you're training a cat classifier, your dataset will not include every possible image of a cat, but should include a representative sample. The same rules apply to these datasets.

## Sample Mean & Variance
When estimating the population mean $\mu$ you can use a number of sample means $\bar{x}_{1}, \bar{x}_{2}, ... \bar{x}_{n}$ from separate independent samples. 
Similarly, you can calculate the sample variance $s^{2}$ of a sample using it's mean $\bar{x}$:
$$
s^{2} = \frac{1}{n-1} \sum_{i=1}^n (x_i - \bar{x})^2
$$
Where $x_i$ are the observations, $\bar{x}$ is the sample mean, and $n$ is the number of observations in the sample.
## Law of Large Numbers
The Law of Large Numbers is a fundamental principle in probability and statistics that describes how the average of a sample is likely to come close to the average of the overall population as the sample size increases, as long as the samples follow [[AI/Machine Learning & Data Science/Statistics/Basics#Population and Sample|these rules]].
