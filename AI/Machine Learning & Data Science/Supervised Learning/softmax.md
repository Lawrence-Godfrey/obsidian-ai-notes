The softmax activation function is commonly used in machine learning algorithms, particularly in multi-class classification problems. It is a type of activation function that takes in a vector of real numbers as input and transforms them into a probability distribution over the classes. I.e., it assigns probabilities to each class such that the sum of all probabilities is equal to 1.

If we have input vector $z$, the output of the softmax function would be
$$
\hat{y}_{i} = \frac{e^{z_{i}}}{\sum\limits_{j=1}^{V}e^{z_{j}}}
$$
