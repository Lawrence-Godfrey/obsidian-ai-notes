### Principle Component Analysis (PCA)
**Goal**: Reduce data from $n$ dimensions to $k$ dimensions where $n\gt k$. 
Find $k$ vectors which we can project the data onto to minimise the projection error. 
Can speed up learning and reduce memory requirements.

#### PCA is not Linear Regression
![[Pasted image 20230828165021.png | center]]

#### Preprocessing
Features should be normalised before applying PCA:
$$\mu_{j} = \frac{1}{m}\sum\limits_{i=1}^{m}x_{j}^{i} $$
Replace each $x_{j}$ with $x_{j} - \mu_{j}$. 
If features are on different scales, also apply [[feature scaling]].

#### Algorithm
 1. Compute "Covariance" matrix $$\Sigma = \frac{1}{m}\sum\limits_{i=1}^{n} (x^{i})(x^i)^{T} $$ where $x^{i}$ is a $n\times 1$ matrix, or simply $$\Sigma = \frac{1}{m}XX^T$$
 2. Compute the eigenvectors of $\Sigma$ (singular value decomposition).
 3. Sort the eigenvalues in descending order and rearrange the corresponding eigenvectors. The first principal component corresponds to the eigenvector associated with the largest eigenvalue, the second principal component to the second-largest eigenvalue, and so on.
 4. Finally, to transform the original data into the new $k$-dimensional space, use $$X_{new}= XW$$ where $W$ are the chosen eigenvectors.

#### Choosing $k$
Choose $k$ to be the smallest value so that 99% of variance is maintained, i.e., the average squared projection error over the total variation in data is $\leq 0.01$ 

#### Notes
 - It is possible to reconstruct the data in the original dimensionality if the principle components are kept, although it will obviously be an approximation of the original dataset.
 - PCA should **not** be used to prevent [[Overfitting & Underfitting|overfitting]].
 - Only use PCA if actually needed, not as a standard in your pipeline.
