The **Chain Rule** (also known as the **General Product Rule**) in probability provides a way to find the joint probability of a sequence of interdependent events. Formally, if we have a set of $n$ events $A_{1}, A_{2}, \ldots, A_{n}$, the chain rule allows us to express their joint probability as a product of conditional and marginal probabilities:
$$P(A_{1}, A_{2}, \ldots, A_{n}) = P(A_{1}) \times P(A_{2}|A_{1}) \times P(A_{3}|A_{1}, A_{2}) \times \ldots \times P(A_{n}|A_{1}, A_{2}, \ldots A_{n-1})$$
Where:
- $P(A_{1})$ is the probability of even $A_{1}$ occurring.
- $P(A_{2}|A_{1})$ is the probability of event $A_{2}$ occurring given $A_{1}$ has occurred. 
- $P(A_{3}|A_{1}, A_{2})$ is the probability of event \(A_3\) occurring given that \(A_1\) and \(A_2\) have occurred.
- $P(A_{n}|A_{1}, A_{2}, \ldots A_{n-1})$ is the probability of event \(A_n\) occurring given that all the preceding events have occurred.