Random variables are used to quantify outcomes of a random phenomenon in terms of a numerical value. For example, we could assign the outcome of 10 coin flips to a variable $X$ by saying that it represents the number of heads. You can then have probabilities like $P(X=1)$, $P(X=2)$, etc. 
### Discrete vs Continuous
The example above represents the discrete case, where the variable takes on distinct values. There are also continuous random variables which can take on any value within a certain range or interval. For example, the height of a person in the general population can be considered as a continuous random variable, because it can take on any value between certain limits, say 3 feet to 7 feet.
### Distributions
#### Discrete
All discrete random variables can be modelled using a Probability Mass Function (PMF) , which assigns a probability to each possible outcome.
The variable must satisfy the following:
 - $p_{X}(x) \geq 0$
 - $\sum_{x}p_X(x)=1$
#### Continuous
Continuous random variables , on the other hand, can take on a potentially infinite number of values within a given range. Instead of a PMF, a continuous random variable is defined by a probability density function (PDF). On a PDF, the y-value represents the density of the probability rather than the actual probability. To get an actual probability, we take the integral of the PDF over a specific range.
The function needs to satisfy the following:
 - Must be defined for all numbers.
 - $f_{X}(x) \geq 0$
 - $\int_{-\infty}^{\infty}f_X(x)dx=1$ (i.e., the area under the curve must be 1)
