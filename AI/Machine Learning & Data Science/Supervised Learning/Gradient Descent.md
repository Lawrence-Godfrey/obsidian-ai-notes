### Batch Gradient Descent
Cost function requires the entire dataset. Therefore every iteration of gradient descent requires insight into the whole dataset.

### Stochastic Gradient Descent
Stochastic gradient descent computes the cost on a single sample from the dataset at a time. For a single epoch, loop through the entire dataset and calculate the cost for each sample, and update the weights accordingly. Randomly shuffle the dataset before each epoch.

Can result in the cost not decreasing on every iteration, but the general trend should still be downwards. The cost might never hit the true minimum, and may just bounce around that point. If plotting the learning curve, average the last $x$ costs and plot that instead. 

### Mini-Batch Gradient Descent
Use $b$ samples in each iteration.

### Online Learning
Can continuously update model as samples stream in (Stochastic).

### Map-Reduce
Map-reduce is a method to parallelise your training. Machine 1 splits the dataset into $b$ batches and sends each batch to a separate machine which calculates the gradient using that batch. Machine 1 then combines the gradients again and updates the weights of the model.
