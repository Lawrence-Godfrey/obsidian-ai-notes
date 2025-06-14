#flashcards

What is Maximum Likelihood Estimation (MLE)?
?
MLE is a method of estimating the parameters of a statistical model by maximizing the likelihood function, which measures how likely the observed data is for different parameter values.

What is the first step in performing MLE?
?
The first step is to specify the probability distribution that the data is assumed to follow, such as normal distribution or binomial distribution.

How is the likelihood function defined in MLE?
?
The likelihood function L(θ) is defined as L(θ) = ∏(i=1 to n) f(x_i; θ), where f(x_i; θ) is the probability density (or mass) function of the observed data point x_i given the parameter θ.

What is the purpose of the log-likelihood function in MLE?
?
The log-likelihood function, denoted as ℓ(θ), is used to simplify the calculations by taking the natural logarithm of the likelihood function, making it easier to work with.

What is the equation for the log-likelihood function?
?
ℓ(θ) = log L(θ) = ∑(i=1 to n) log f(x_i; θ).

What is the procedure to maximize the log-likelihood function?
?
To maximize the log-likelihood function, you need to find the parameter value(s) θ that satisfy the equation ∂ℓ(θ)/∂θ = 0 and confirm that this point is a maximum by checking the second derivative.

Why might one prefer to use the log-likelihood function instead of the likelihood function directly?
?
Using the log-likelihood function can help to transform products into sums, which are generally easier to differentiate and optimize.

What kind of statistical models can MLE be used for?
?
MLE can be used for various statistical models, as long as there is a defined probability distribution for the data being analyzed.

What do you check after finding a critical point when maximizing the log-likelihood function?
?
After finding a critical point, you should verify that the solution is a maximum by checking the second derivative or using other criteria.

Give an example of a probability distribution that might be specified in MLE.
?
Examples include the normal distribution, binomial distribution, Poisson distribution, or exponential distribution.

