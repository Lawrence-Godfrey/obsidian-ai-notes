Given the target number of clusters $K$ and your dataset $x^{i}\in \mathbb{R}^{n}$ 
 1. Randomly initialise cluster centroids $u_{1}, u_{2}, ..., u_{K} \in \mathbb{R}^{n}$
 2. Repeat the following:
	 1. For each sample, add the sample to the nearest cluster.
	 2. For each cluster, update the centroid location to be the mean of all points in that cluster.

Note that $K < m$.

#### Random Initialisation
One way to randomly initialise your centroid locations is to randomly pick $K$ training examples and initialise your centroids at those random sample locations.

#### Local Optima 
The K-means algorithm can get stuck in local optima:

![[Pasted image 20230828164510.png | center]]

Can try running K-means on the dataset a number of times with different random initialisations and use the one with the lowest cost.

For a clustering algorithm which doesn't require a preconfigured number of clusters, see [[DBSCAN]].