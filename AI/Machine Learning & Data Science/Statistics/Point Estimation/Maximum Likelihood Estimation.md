Maximum Likelihood Estimation (MLE) is a method of estimating the parameters of a statistical model given observations. This is done by maximising the likelihood function, which measures how likely it is to observe the given data for different parameter values.

## Steps in MLE
1. **Specify the Probability Distribution**: 
   Identify the probability distribution that the data is assumed to follow. For example, normal distribution, binomial distribution, etc.
2. **Formulate the Likelihood Function**: 
   For a given set of observed data points $x_1, x_2, \ldots, x_n$​ and a probability distribution with parameter(s) $\theta$, the likelihood function $L(\theta)$ is defined as:
   $$
   L(\theta) = \prod_{i=1}^n f(x_i; \theta)
   $$
  
   where $f(x_i; \theta)$ is the probability density (or mass) function of the observed data point $x_i$ given the parameter $\theta$.
3. **Log-Likelihood Function**: 
   Often, it's easier to work with the natural logarithm of the likelihood function, known as the [[AI/Machine Learning & Data Science/Probability/Naïve Bayes#Log Likelihood|log-likelihood]] function $\ell(\theta)$: 
   $$
   \ell(\theta) = \log L(\theta) = \sum_{i=1}^n \log f(x_i; \theta)
   $$
4. **Maximise the Log-Likelihood Function**: 
   Find the parameter value(s) θ\thetaθ that maximise the log-likelihood function. This involves solving the equation:
   $$
   \frac{\partial \ell(\theta)}{\partial \theta} = 0
   $$
   
   and ensuring that the solution is a maximum by checking the second derivative (or using other criteria).