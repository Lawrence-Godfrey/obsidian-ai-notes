Naïve Bayes is a classification algorithm based on [[Bayes' Rule]]. It's called "naïve" because it makes a significant assumption: it assumes that the features used to describe instances are conditionally independent given the class label. In simpler terms, each feature is assumed to independently contribute to the class label without being influenced by any other feature.

Given:

- A data set with instances described by features $F_{1}, F_{2}, ... F_{n}$.
- Each instance belongs to a certain class $C$.

The goal of Naïve Bayes is to find the probability of a class $C$ given an instance with features $F_{1}, F_{2}, ... F_{n}$.

Using Bayes' theorem:

$P(C∣F_1​,F_2​,...F_n​)=\frac{P(F_1​,F_2​,...F_n​∣C)×P(C)}{P(F_1​,F_2​,...F_n​)}​$

The naïve assumption comes into play for the term $P(F_1​,F_2​,...F_n​∣C)$. Instead of computing the joint probability of all features given the class, which can be complex and computationally expensive, the Naïve Bayes classifier assumes each feature is independent of the others given the class. Therefore:

$$
P(F_1​,F_2​,...F_n​∣C) = P(F_1​∣C)×P(F_2​∣C)×...×P(F_n​∣C)
$$

The class that maximises $$P(F_1​∣C)×P(F_2​∣C)×...×P(F_{n}​∣C) \times P(C)$$ is chosen as the predicted class.

### Naïve Bayes Inference Rule for Binary Classification
Given two classes $C_{1}$ and $C_{2}$, the Naïve Bayes inference rule compares $P(C_{1}|F)$ and $P(C_{2}|F)$ and classify the instance into the class with the higher probability.

Concretely, if 
$$
\frac{P(C_{1})}{P(C_{2})}\prod_{i=1}^{n}\frac{P(F_{i}|C_{1})}{P(F_{i}|C_{2})} \geq 1
$$
Then we classify the instance as being part of $C_{1}$.

### Laplacian Smoothing
When encountering examples in the test data which were not present in the training data, these can result in zero probabilities. Since we multiply all our probabilities together in Naïve Bayes, this results in the entire probability being zero. 

Laplacian smoothing (or additive smoothing) can counteract this problem. The basic idea is to pretend we've seen every word a few more times than we actually have. Formally, for a given feature $F$ and class $C$:
$$
P(F∣C)=\frac{\text{Number of times t appears in }C+α}{\text{Total number of words in }C+α×\text{Number of unique words}}​
$$
Where:
 - $\alpha$ is the smoothing parameter (often set to 1).
 - The denominator $α×\text{Number of unique words}$ ensures that our probabilities still sum up to 1.

Essentially we add $\alpha$ to the count of every feature for each class so that no feature has a probability of zero.

### Log Likelihood
Sometimes the product of probabilities can be so small that they risk underflow. To counteract this we can take the log of our product:
$$
log\left(\frac{P(C_{1})}{P(C_{2})}\prod_{i=1}^{n}\frac{P(F_{i}|C_{1})}{P(F_{i}|C_{2})}\right) = log\left(\frac{P(C_{1})}{P(C_{2})}\right)+ \sum\limits_{i=1}^{n} log\left(\frac{P(F_{i}|C_{1})}{P(F_{i}|C_{2})}\right)
$$
Where $log\left(\frac{P(C_{1})}{P(C_{2})}\right)$ is known as the "log prior"
and $\sum\limits_{i=1}^{n} log\left(\frac{P(F_{i}|C_{1})}{P(F_{i}|C_{2})}\right)$ is known as the "log likelihood".
In this case we predict based on the log being above 0.

### Assumptions
Naïve Bayes assumes that the features in an instance are unrelated, but this is not always the case. For example in the sentence "It's cold and snowy in ...", Naïve Bayes might assign the same probability to the next word being "Winter" as it does to "Summer".

Naïve Bayes also assumes that the size of the classes are relatively equal, which is not always the case.