#flashcards

What is batch gradient descent?
?
Batch gradient descent requires the entire dataset to compute the cost function, meaning every iteration of gradient descent uses insights from the whole dataset.

How does stochastic gradient descent differ from batch gradient descent?
?
Stochastic gradient descent computes the cost on a single sample at a time, rather than the entire dataset.

What is the potential issue with stochastic gradient descent?
?
In stochastic gradient descent, the cost may not decrease on every iteration; it can bounce around a point and may never hit the true minimum.

How can we visualize the performance of stochastic gradient descent?
?
To visualize the learning curve, average the last $x$ costs over the iterations and plot that average.

What is mini-batch gradient descent?
?
Mini-batch gradient descent uses $b$ samples in each iteration, striking a balance between the efficiency of batch and stochastic gradient descent.

What is online learning in the context of machine learning?
?
Online learning allows models to continuously update as new samples stream in, often associated with stochastic gradient descent.

What is the purpose of map-reduce in training machine learning models?
?
Map-reduce parallelizes training by splitting the dataset into batches, distributing them to multiple machines that compute gradients, and then combining these gradients to update model weights.

Why would one shuffle the dataset in stochastic gradient descent?
?
Shuffling the dataset before each epoch helps ensure that the samples are presented in a different order, which can lead to better convergence properties.

What is the typical outcome of stochastic gradient descent in terms of cost function trends?
?
While the cost function may not decrease steadily, the general trend should still be downward.

What is the significance of using $b$ samples in mini-batch gradient descent?
?
Using $b$ samples allows mini-batch gradient descent to reduce the variance of the updates and can improve convergence speed while maintaining the advantages of both approaches.

