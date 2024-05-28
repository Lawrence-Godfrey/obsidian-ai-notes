Decision trees do not generalise well since a small change in the features of a sample can completely change the resulting tree, i.e., they are very sensitive to samples in the data. Random Forest is a supervised learning algorithm which builds an array (forest) of random decision trees.

For each tree, a new dataset is created, which is randomly sampled from the original dataset. These datasets also only have a subset of the features of the original dataset (normally the log or square root of the number of original features), again, randomly sampled. A new decision tree is then trained on each tree. When inference is done, the sample is passed through each tree, and the prediction which is the most common is chosen.

The random sampling and feature selection reduces the sensitivity of the overall model to the dataset, and helps it generalise. 

![[Pasted image 20240301085625.png]]