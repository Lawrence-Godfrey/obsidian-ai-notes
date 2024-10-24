A joint distribution combines multiple random variables into a single distribution, representing the likelihood of all variables occurring simultaneously.
## Marginal Distribution
The marginal distribution of a joint distribution refers to the probability distribution of a single random variable within the joint distribution. This is useful when we are interested in understanding the behaviour or characteristics of one variable without considering the effect of other variables. To get the marginal distribution $P (A)$, one must sum or integrate over all possible outcomes of the other variable in the joint distribution. 

$$
P(A) = \sum_{B} P(A, B)
$$

or in the case of continuous variables:

$$
P(A) = \int P(A, B) dB
$$

## Conditional Distribution
The conditional distribution is another way to extract information from a joint distribution. Similar to a marginal distribution, a conditional distribution aims to extract information about a single variable in a joint distribution. However, in a conditional distribution, the focus is on the distribution of a single variable given the value of another variable. There is a caveat when applying this formula, since simply taking a slice of the distribution results in a distribution which does not sum to 1. Therefore, the distribution is normalised by the row sum. 

$$
P(A|B) = \frac{P(A, B)}{P(B)}
$$

or in the case of continuous variables:

$$
P(A|B) = \frac{P(A, B)}{\int P(A, B) dB}
$$

This formula illustrates that the conditional probability of A given B is simply the joint probability of A and B divided by the marginal probability of B.
## Covariance
The covariance of a joint distribution describes the degree to which two or more variables move together or vary in relation to each other. It can be obtained by first standardising or centring the data (i.e., making the mean = 0 and variance = 1 for each variable) and then calculating the expectation (or average value) of the products of these standardised variables.

$$
Cov(X, Y) = E[ (X - μx) (Y - μy) ] =  E[XY] - E [X]E[Y] 
$$

![[Pasted image 20240608112153.png|centered]]

### Covariance Matrix
The covariance matrix of a joint distribution shows the covariance and variance of the different random variables involved. It's useful in understanding and interpreting the relationships between these variables.

$$
Cov(X, Y) = 
\begin{bmatrix}
Var(X) & Cov(X, Y)\\
Cov(Y, X) & Var(Y)
\end{bmatrix}
$$

Each entry in the covariance matrix represents the covariance between two variables.
### Correlation Coefficient 
The magnitude of covariance doesn't necessarily reflect the strength of a relationship between two variables. For this the correlation coefficient is used, which is a standardised version of covariance. 

$$
\rho(X, Y) = \frac{Cov(X, Y)}{\sqrt{Var(X)Var(Y)}}
$$

The correlation coefficient, also known as Pearson's correlation coefficient, ranges from -1 to 1.