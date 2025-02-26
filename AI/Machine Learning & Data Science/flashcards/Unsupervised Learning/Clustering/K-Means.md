#flashcards

What is the first step in initializing the K-means algorithm?
?
Randomly initialise cluster centroids u_1, u_2, ..., u_K in R^n.

What do you do after randomly initializing the cluster centroids in K-means?
?
Repeat the process of assigning samples to the nearest cluster and updating the centroid location.

In K-means, how is the centroid for each cluster updated?
?
The centroid is updated to be the mean of all points in that cluster.

What is a common method for randomly initializing cluster centroids in K-means?
?
Randomly pick K training examples and set the centroids at those sample locations.

What issue can K-means face regarding the clustering results?
?
K-means can get stuck in local optima.

How can you try to avoid local optima in K-means?
?
Run K-means multiple times with different random initialisations and use the one with the lowest cost.

What is the limitation on K in the K-means algorithm?
?
K must be less than m, where m is the number of samples in the dataset.

What is an alternative clustering algorithm that does not require a predefined number of clusters?
?
DBSCAN.

What is the significance of the variable K in the K-means algorithm?
?
K represents the target number of clusters for the dataset.

Describe what K-means does in the assignment step.
?
For each sample, K-means assigns the sample to the nearest cluster.

