A Binomial Distribution is a specific type of probability distribution. It describes the number of successes in a fixed number of independent [[Bernoulli Distribution|Bernoulli]] trials (experiments with two possible outcomes: success or failure).

### Binomial Coefficient
The binomial coefficient refers to the number of ways in which a certain event can occur.
In general:
$${n \choose k} = \frac{n!}{k!(n-k)!}$$
Where:
- $n$ is the total number of trials.
- $k$ is the number of successful trials.

For example, in a coin toss experiment, $n \choose k$ represents the number of combinations of landing $k$ heads in $n$ coin tosses. The denominator essentially takes care of the cases where combination is actually the same. For example, `T T H H T` and `T T H H T` could be counted as 4 separate combinations if you flip the two tails or 2 heads around, but we want to count them as a single combination.

### Distribution
The [[Random Variables#Distributions|PMF]] of a Binomial Distribution gives the probability of obtaining exactly $k$ successes in $n$ trials:
$$P(X=k) = {n \choose k}p^{k}(1-p)^{n-k}$$
