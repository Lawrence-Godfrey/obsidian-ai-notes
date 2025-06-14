#flashcards

What is the main principle behind Isolation Forests?
?
Anomalies can be isolated with fewer random partitions than normal points.

How does Isolation Forest detect anomalies?
?
By constructing a forest of random trees that isolate each sample, where shorter paths from root to terminal node suggest anomalies.

What are the first steps in the Isolation Forest algorithm?
?
1. Random Subsampling: Select a subset of data. 2. Tree Construction: Recursively divide the data using random features and split values.

What is the significance of path length in Isolation Forest?
?
The path length from the root to the terminal node indicates normalcy; shorter paths suggest an anomaly.

How is the anomaly score calculated in Isolation Forest?
?
By normalizing the path length of a data point over all trees in the forest using the formula: s(x, n) = 2 * c(n) / E(h(x)).

What does an anomaly score closer to 1 indicate?
?
It indicates a stronger anomaly.

What are some advantages of using Isolation Forest?
?
Efficiency, Scalability, Effectiveness.

What is the purpose of the area under the ROC curve in relation to Isolation Forest?
?
It is a performance metric for evaluating the efficiency of anomaly detection across various threshold settings.

What is a method used to interpret the economic contributions of features in Isolation Forest?
?
SHAP (Shapley Additive exPlanations) values.

What does the c(n) represent in the anomaly score calculation?
?
The average path length in an unsuccessful search in a binary search tree (BST), which serves as a normalization factor.

