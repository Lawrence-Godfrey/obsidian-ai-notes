Using the Euclidean distance to calculate the similarity of two vectors can often be skewed by the relative magnitude of the vectors. In some cases we care more about the angle between the vectors, in which case using Cosine similarity can produce a more accurate metric.

The cosine of the angle between two vectors $\hat{v}$ and $\hat{w}$ is defined as:
$$
cos(\beta) = \frac{\hat{v}\cdot \hat{w}}{\parallel\hat{v}\parallel \parallel\hat{w}\parallel}
$$
If the two vectors are orthogonal, the cosine is 0, and if the vectors have the exact same direction, the cosine is 1.