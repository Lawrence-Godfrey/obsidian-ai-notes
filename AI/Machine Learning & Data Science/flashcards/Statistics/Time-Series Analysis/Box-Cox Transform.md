#flashcards

What is the Box-Cox transformation used for?
?
To stabilize variance and make data resemble a Normal Distribution, which is often required for statistical models and tests.

How is the Box-Cox transformation defined mathematically?
?
y(λ) = (y^λ - 1) / λ if λ ≠ 0; log(y) if λ = 0.

What does the parameter λ in the Box-Cox transformation control?
?
The nature of the transformation applied to the data.

What is the Box-Cox transformation result for λ = 1?
?
No transformation (linear).

What common transformation does λ = 0 correspond to in Box-Cox?
?
Logarithmic transformation.

What is the effect of applying the Box-Cox transformation?
?
It makes the data distribution more normal (Gaussian) and can also stabilize variance.

What is a key limitation of the Box-Cox transformation?
?
It only works on positive data since log(0) is undefined and log is undefined for negative values.

How is the optimal value of λ typically determined?
?
By maximizing the likelihood of a model, often through maximizing log-likelihood in regression.

What is an example of a transformation when λ = 0.5?
?
Square root transformation.

Why is normality important in statistical modeling?
?
Many statistical tests and models, like linear regression, assume that the underlying distribution of the data is normal.

