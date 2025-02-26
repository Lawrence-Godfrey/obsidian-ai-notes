#flashcards

What is the main difference between a univariate and a multivariate Gaussian distribution?
?
The univariate Gaussian distribution is defined for one-dimensional space, while the multivariate Gaussian distribution generalizes this concept to higher dimensions, associating each point in n-dimensional space with a probability.

What are the two key parameters that define a multivariate Gaussian distribution?
?
The two key parameters are the mean vector (μ) and the covariance matrix (Σ).

What does the mean vector (μ) represent in a multivariate Gaussian distribution?
?
The mean vector (μ) is an n-dimensional vector where each element represents the mean of a particular dimension.

What information does the covariance matrix (Σ) contain in a multivariate Gaussian distribution?
?
The covariance matrix (Σ) is an n x n matrix that contains the variances and covariances of the variables in the distribution.

Why might a normal distribution be unsuitable for certain datasets?
?
A normal distribution might not work well for datasets where the features are not mutually exclusive.

How does modeling p(x) for a multivariate Gaussian distribution capture feature relationships?
?
By using a mean vector as a matrix in ℝ^n and a covariance matrix in ℝ^{n×n}, the model can automatically capture correlations between features.

What additional information can help evaluate the performance of a Gaussian model?
?
Labels are not required to fit a Gaussian model, but they are useful for evaluating the performance of the model.

What can be done if a raw dataset is not Gaussian distributed?
?
If a raw dataset is not Gaussian, it can be mapped to a Gaussian distribution.

