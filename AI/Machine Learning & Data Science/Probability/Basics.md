### Addition Rule
#### Disjoint (Mutually Exclusive) Events
•	Events $A$ and $B$ are disjoint if they cannot happen at the same time, i.e., $A \cap B = \emptyset$.
•	The addition rule for disjoint events is:
$P(A \cup B) = P(A) + P(B)$
#### Joint (Not Mutually Exclusive) Events
•	Events $A$ and $B$ can happen at the same time.
•	The addition rule for joint events is:
$P(A \cup B) = P(A) + P(B) - P(A \cap B)$
### Multiplication Rule
For independent events $A$ and $B$:
$P(A \cap B) = P(A) \times P(B)$
For dependent events, the [[Conditional Probability]] rule applies:
$P(A\cap B) = P(A) \times P(B | A)$
### Complementary Rule
The probability of the complement of an event $A$:
$P(A^c) = 1 - P(A)$
## Central Tendency
Central tendency is a statistical measure that defines the center point or typical value of a dataset.
### Expected Value
The Expected value, or mean, of a distribution is a measure of the "central tendency" or average value of the distribution. It is essentially a weighted average of the possible outcomes of the distribution, where each outcome is weighted by its probability.
In the example below, the Expected Value $E(X)$ of a random variable $X$ is calculated as
$$
E(X) = \sum x_i \cdot P(x_{i}) = \frac{3}{10}\cdot0 + \frac{2}{10}\cdot1 + \frac{4}{10}\cdot2 + \frac{1}{10}\cdot3 +  = 1.3
$$
Where $x_i$ represents each possible outcome of the random variable and $P(x_i)$ is the [[Random Variables#Distributions|probability mass function]] of that variable.

![[Pasted image 20240601085919.png|centered]]

For continuous random variables the formula would be 
$$
E(X) = \int x \cdot f(x) dx
$$
where $f(x)$ is the [[Random Variables#Distributions|probability density function]] of the random variable $X$.
#### Linearity of Expectation
If the given random variables are the output of a function, then in general
$$
E(aX + b) = aE(X) + b
$$
This is known as the Linearity of Expectation, and simplifies the calculation of the expected value of linear transformations of a random variable. For example, if you know $E(X)$, you can easily compute $E(aX + b)$ without having to go back to the original distribution of $X$.
#### Sum of Expectations
The Sum of Expectation property says that the expected value of the sum of two or more random variables is equal to the sum of their individual expected values, regardless of whether the random variables are dependent or not.
$$
E(X+Y) = E(X) + E(Y)
$$
This property can be extended to any number of random variables.
#### Variance
The variance of a distribution can be calculated as 
$$
Var(X) = E[(X - E[X])^2] = E[X^2] - (E[X])^2
$$
Essentially the average of the square of deviations. The absolute value of deviations $|X-E[X]|$ could be used, but has some undesirable mathematical properties, such as not being differentiable at zero.
##### Properties
$$
Var(aX + b) = a^2 * Var(X)
$$
#### Standar Deviation
The variance of a distribution has one inconvenience, which is that the units are all squared. Standard deviation uses the square root of variance to solve this. 
### Median
The Median of a distribution is the numerical value separating the higher half of a data sample or probability distribution from the lower half. It can be calculated using
$$
Median(X) = \frac{n+1}{2}
$$
where $n$ is the number of observations for discrete data, or
$$
Median(X) = \int_{-\infty}^{x} f(t) dt = 0.
$$
for continuous data.

Use the median instead of the mean or mode when you have a skewed distribution or outliers that could influence the results.
### Mode
The Mode of a distribution is the value that appears most frequently in a data set. It can be calculated using 
$$
Mode(X) = \max_{x_i} P(x_i)
$$
where $x_i$ are the possible outcomes and $P(x_i)$ is the [[Random Variables#Distributions|probability mass function]] for discrete data.

There can be multiple modes of a distribution, and these modes are classified into three types: unimodal, bimodal and multimodal.

Use the mode instead of the mean or median when you are dealing with nominal data (categorical data) or when the most frequently occurring value is more significant.