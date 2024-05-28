In supervised learning, loss functions are used to measure the error or deviation between the predicted output and the actual target output.
### Frobenius Norm
The Frobenius norm of a matrix is a measure of the overall magnitude of the matrix. 
$$
\parallel A \parallel_{F} = \sqrt{\sum\limits_{i=1}^{m}\sum\limits_{j=1}^{n}|a_{ij}|^2}
$$
This can be used to calculate the loss between your training data $X$ and your target output $Y$. For example:
$$
Loss = \parallel X\Theta - Y \parallel_F
$$
Where $\Theta$ are the parameters of your model.
Often the loss will be calculated as the square of the Frobenius norm divided by $m$ (the number of examples) which makes calculating the derivative easier. This doesn't change the outcome when minimising the loss. The derivative of the squared Frobenius norm is then:
$$
\frac{d}{d\Theta}Loss = \frac{2}{m}(X^T(X\Theta - Y))
$$
### Cross-Entropy Loss
For two discrete probability distributions, $p$ (true distribution) and $q$ (predicted distribution), the cross-entropy is defined as: 
$$
		H(p, q) = -\sum\limits_{i}p(i) log q(i)
$$
Cross-entropy loss is commonly used in classification problems in machine learning, especially in neural networks. The true distribution typically has a probability of 1 for the correct class and 0 for all other classes (in the case of one-hot encoded labels), and the predicted distribution is the model's estimated probabilities for each class. The loss measures how well the predicted probabilities match the true labels.

### Triplet Loss
Triplet loss is a loss function often used for models which compare similarity between inputs, and uses an anchor, negative and positive sample to compute loss.

The loss is then the similarity of the anchor and negative outputs minus the similarity of the anchor and positive outputs:
$$
Loss = s(A, N) - s(A, P)
$$

The loss will be high if the similarity between the anchor and negative is high, and the similarity between the anchor and positive is low, and will be low if the similarity between the anchor and negative is low, and the similarity between the anchor and positive is high.

We can add a hyperparameter, the alpha margin $\alpha$, which essentially makes the loss a bit stricter. The loss will then be:
$$
Loss = \begin{equation} \left\{ \begin{aligned} & 0; \text{if diff + } \alpha \leq 0  \\ & diff + \alpha; \text{ if diff + } \alpha \gt 0  \end{aligned} \right. \end{equation}
$$
