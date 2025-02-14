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
### Contrastive Loss
Contrastive loss is used for tasks that involve finding similarity or dissimilarity between two instances, for example, in tasks such as face recognition or signature verification. The main idea behind contrastive loss is to minimise the distance between similar instances and maximise the distance between dissimilar instances.

The formula for contrastive loss is
$$
L = yd^{2} + (1-y)Max(0, m-d)^{2}
$$
Where $y$ is the labeled sample, which will be $1$ for the positive example and $0$ for the negative example. So for a positive example we will only consider the first part of the function, meaning your loss is directly correlated to the square of the Euclidean distance. For a negative sample, the loss is square of the distance from the margin $m$ (a hyperparameter which determines how strictly the model enforces the minimum distance between dissimilar pairs). 

We use a margin in contrastive loss for a few reasons:
1. It enforces a minimum distance for separation, rather than some arbitrary distance.
2. It avoids overfitting by reducing the importance of separating the points by some infinitely scaling distance.
3. Creates stability.
4. Allows for flexibility since you can tweak how strict the model is.