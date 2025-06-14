Bayes' rule (or Bayes' theorem) is a fundamental concept in the theory of probability and provides a way to find the probability of an event based on the probability of a related event. It's an extension of [[Conditional Probability]] and is particularly useful when dealing with prior and updated knowledge.

The theorem is stated as:
$$
P(A|B) = \frac{P(B|A)\times P(A)}{P(B)}
$$
Where
 - $P(A)$ is the "prior", e.g., in spam classification, the prior is the percentage of emails which are spam.
 - $B$ is the "event", e.g., in spam classification, the event might be that the email contains the word "lottery".
 - $P(A|B)$ is the "posterior", e.g., in spam classification, this would be the probability that the email is spam given that it contains the word "lottery".

The denominator $P(B)$ can be rewritten in terms of the **Law of Total Probability**. Specifically, if we assume that $A$ and its complement $A^c$ (where $A^c$ means "not $A$") form a complete partition of the sample space, we can express $P(B)$ as:

$$P(B) = P(B|A) \cdot P(A) + P(B|A^c) \cdot P(A^c)$$

Using Baye's rule can become difficult when you have high-dimensional data because you essentially have a number of events which can affect the outcome. For example, what if you weren't only looking at the presence of the word "lottery", but also "won", "prize", etc. You would then need in your dataset examples which contain all of these words, otherwise your $P(B|A)$ would be 0. To solve this, you can utilise the concept of [[Naïve Bayes]], a simplified version of Bayes' Rule, which assumes that each feature in your dataset is independent.