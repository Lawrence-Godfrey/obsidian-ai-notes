#flashcards

What is the primary purpose of the softmax activation function?
?
To transform a vector of real numbers into a probability distribution over classes, particularly in multi-class classification problems.

How does the softmax function ensure that the output is a valid probability distribution?
?
It assigns probabilities to each class such that the sum of all probabilities is equal to 1.

What is the formula for the output of the softmax function given input vector z?
?
The output is given by \( \hat{y}_{i} = \frac{e^{z_{i}}}{\sum\limits_{j=1}^{V}e^{z_{j}}} \) for each class i.

In the softmax function, what does the variable V represent?
?
V represents the total number of classes.

What type of problems is the softmax activation function commonly used in?
?
In multi-class classification problems.

Why do we use the exponential function in the softmax calculation?
?
The exponential function ensures that all outputs are positive and amplifies the differences between input values.

Can you explain what happens to the output of the softmax function if one input value is significantly larger than the others?
?
The output for the class corresponding to the largest input will approach 1, while the outputs for the other classes will approach 0.

What are some limitations of the softmax function?
?
Softmax is not suitable for multi-label classification and can be sensitive to outlier values due to the exponential calculation.

How is the softmax function typically applied in a neural network's output layer?
?
It is used as the activation function in the output layer to produce class probabilities from the final layer's raw output logits.

