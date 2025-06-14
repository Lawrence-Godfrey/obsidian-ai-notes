#flashcards

What is a joint distribution?
?
A joint distribution combines multiple random variables into a single distribution, representing the likelihood of all variables occurring simultaneously.

Define marginal distribution in the context of joint distribution.
?
The marginal distribution of a joint distribution refers to the probability distribution of a single random variable within the joint distribution.

How is the marginal distribution P(A) calculated for discrete variables?
?
P(A) = ∑ P(A, B) over all B.

How is the marginal distribution P(A) calculated for continuous variables?
?
P(A) = ∫ P(A, B) dB.

What is a conditional distribution?
?
A conditional distribution is the distribution of a single variable given the value of another variable, derived from a joint distribution.

How is the conditional probability P(A|B) calculated?
?
P(A|B) = P(A, B) / P(B).

What is the formula for conditional probability involving continuous variables?
?
P(A|B) = P(A, B) / ∫ P(A, B) dB.

What is covariance and how is it calculated?
?
Covariance describes the degree to which two or more variables move together; calculated as Cov(X, Y) = E[ (X - μx)(Y - μy) ] = E[XY] - E[X]E[Y].

What is a covariance matrix?
?
The covariance matrix shows the covariance and variance of different random variables involved in a joint distribution.

Write the structure of a covariance matrix for two variables X and Y.
?
Cov(X, Y) = [[Var(X), Cov(X, Y)], [Cov(Y, X), Var(Y)]]

What is the correlation coefficient?
?
The correlation coefficient is a standardized version of covariance, used to measure the strength of the relationship between two variables.

What is the formula for the correlation coefficient ρ(X, Y)?
?
ρ(X, Y) = Cov(X, Y) / √(Var(X) * Var(Y)).

What is the range of values for the correlation coefficient?
?
The correlation coefficient ranges from -1 to 1.

