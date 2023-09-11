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

Often the loss will be calculated as the square of the Frobenius norm, since we don't really care about the number itself, we just want to minimise it. The derivative of the squared Frobenius norm is then:
$$
\frac{d}{d\Theta}Loss = \frac{2}{m}(X^T(X\Theta - Y))
$$
