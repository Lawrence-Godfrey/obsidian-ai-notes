#flashcards

What is the main goal of Principal Component Analysis (PCA)?
?
To reduce data from n dimensions to k dimensions where n > k, while minimizing projection error.

What is the first step in the PCA algorithm?
?
Compute the covariance matrix using Sigma = (1/m) * sum(x^i * (x^i)^T).

Why is data normalization necessary before applying PCA?
?
Normalization ensures that features with different scales do not disproportionately influence the results of PCA.

What determines the choice of k in PCA?
?
k should be chosen to maintain at least 99% of the variance in the data.

How does t-SNE differ from PCA?
?
t-SNE is a non-linear dimensionality reduction technique designed for visualization, while PCA is a linear method.

What is the probabilistic approach used by t-SNE?
?
t-SNE converts high-dimensional distances into conditional probabilities to represent similarities, and minimizes the divergence between the high-dimensional and low-dimensional distributions.

What is the significance of the perplexity parameter in t-SNE?
?
Perplexity influences how much attention is paid to local versus global structures in the data during visualization.

Why is t-SNE considered non-deterministic?
?
Because it can yield different results upon multiple runs due to random initialization of low-dimensional embeddings.

What should one avoid when using PCA regarding overfitting and underfitting?
?
PCA should not be used as a method to prevent overfitting or underfitting.

Can PCA reconstruct the original data?
?
Yes, but it will be an approximation based on the principal components retained.

What is a characteristic visual outcome of t-SNE?
?
t-SNE often produces visually appealing plots that reveal clusters of similar data points.

How is t-SNE computationally intensive compared to PCA?
?
t-SNE can require more computational resources, especially on large datasets, due to its probabilistic nature and optimization process.

