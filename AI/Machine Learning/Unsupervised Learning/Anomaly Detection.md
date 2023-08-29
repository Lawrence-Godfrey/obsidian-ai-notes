### Gaussian (Normal) Distribution
If $x \in \mathbb{R}$ is a distributed Gaussian with mean $\mu$ and variance $\sigma ^{2}$ (square of standard deviation) then the data can be modelled with a Gaussian distribution $$p(x;\mu, \sigma) = \frac{1}{\sqrt{2\pi} \sigma} exp(-\frac{(x-\mu)^{2}}{2\sigma^2})$$
If $x\in \mathbb{R}^n$ calculate $p(x_i)$ for every dimension. $p(x)$ is then the product of all the probabilities.
$$p(x) = \prod_{i=1}^{n}p(x_i;\mu_i, \sigma_i)$$

#### Multivariate Gaussian Distribution
The previous method might not work well for certain datasets where the features are not mutually exclusive.
![[Pasted image 20230828172559.png | center]]

Rather model $p(x)$ all at once. $\mu$ is now a matrix in $\mathbb{R}^n$ and $\Sigma$ is a matrix in $\mathbb{R}^{n\times n}$. This automatically captures correlations between features.

#### Notes
 - While labels aren't required to fit a Gaussian model, they are useful for evaluating the [[Performance Metrics | performance]] of the model.
 - If raw dataset is not Gaussian, it can be mapped to a Gaussian distribution![[Pasted image 20230828172228.png | center]]