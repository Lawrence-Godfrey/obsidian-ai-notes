#flashcards

What is the key assumption of the Naïve Bayes algorithm regarding features?
?
Features are conditionally independent given the class label.

What does Bayes' theorem calculate in the context of Naïve Bayes?
?
It calculates the probability of a class C given an instance with features F1, F2, ..., Fn.

How does Naïve Bayes simplify the calculation of probabilities for features?
?
It assumes that the joint probability of features given the class can be decomposed into the product of individual probabilities of each feature given the class.

What is the role of Laplacian smoothing in Naïve Bayes?
?
It prevents the occurrence of zero probabilities for unseen features in the test data.

What is the formula for probability with Laplacian smoothing?
?
P(F|C) = (Number of times F appears in C + α) / (Total number of words in C + α × Number of unique words) where α is the smoothing parameter.

What are the components of log likelihood in Naïve Bayes?
?
The log likelihood consists of the log prior and the sum of log probabilities of features given the classes.

How can Naïve Bayes lead to underflow issues when calculating probabilities?
?
Because the product of many small probabilities can result in very small numbers that exceed floating-point precision.

What assumption about class sizes does Naïve Bayes make?
?
Naïve Bayes assumes that the sizes of the classes are relatively equal.

What decision does Naïve Bayes make in binary classification?
?
It compares P(C1|F) and P(C2|F) and classifies the instance into the class with the higher probability.

What is the potential limitation of Naïve Bayes regarding the relationship between features?
?
It assumes that the features are unrelated, which may not hold true in real-world scenarios.

