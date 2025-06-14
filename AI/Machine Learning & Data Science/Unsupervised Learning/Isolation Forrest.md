Isolation Forest is an anomaly detection algorithm which uses a number of trees to detect outliers in a dataset. See [[Random Forest]].

The principle behind Isolation Forests is that anomalies can be isolated with fewer random partitions than normal points. The algorithm exploits this property by constructing a forest of random trees, where each tree attempts to isolate every sample. The path length from the root node to the terminal node (where a sample is isolated) serves as a measure of normalcy; shorter paths suggest an anomaly.
![[Pasted image 20240529195430.png|centered]]
### Algorithm Steps
1. **Random Subsampling**: 
	- The algorithm begins by randomly selecting a subset of the data to ensure efficiency and to mitigate the curse of dimensionality. This subset is used to construct each tree in the forest.
2. **Tree Construction**:
	- For each tree, the algorithm recursively divides the data by randomly selecting a feature and then randomly selecting a split value between the minimum and maximum values of the selected feature.
    - This process of splitting continues until the node contains only one sample (isolation), or until it reaches a predefined limit (to prevent overfitting on the training data).
3. **Path Length Calculation**:
    - Once the forest is constructed, the path length for each point in the dataset is calculated. The path length is the number of edges from the root node to the terminal node.
    - Anomalies are expected to have shorter path lengths on average, as they are easier to isolate than normal points.
4. **Anomaly Score**:
    - The algorithm then calculates an anomaly score based on the path lengths. A shorter path length results in a higher anomaly score.
    - The anomaly score is normalised to be between 0 and 1, where scores closer to 1 indicate anomalies.
### Mathematical Formulation
The anomaly score $z = s(x,n)$ for a data point $x$ in a forest of $n$ trees is defined as:
$$
s(x, n) = 2 \frac{c(n)}{E(h(x))}
$$
where $E(h(x))$ is the average path length of $x$ over all trees in the forest, and $c(n)$ is the average path length in an unsuccessful search in a binary search tree (BST), which serves as a normalisation factor. This score quantifies the extent to which a data point is considered an outlier, with values closer to 1 indicating a strong anomaly.
### Advantages
- **Efficiency**: Isolation Forests are highly efficient, especially with large datasets, due to the sub-sampling step and the nature of tree construction.
- **Scalability**: The algorithm scales well with the number of dimensions and samples, making it suitable for high-dimensional data.
- **Effectiveness**: It generally outperforms other anomaly detection methods, especially in datasets where anomalies are substantially different from normal observations.

### Evaluation
The [[Area Under ROC Curve]] is a commonly used performance metric for measuring the efficiency of isolation forest in anomaly detection due to its ability to evaluate the model's performance across various threshold settings.

### Explainability
[[SHAP (Shapley Additive exPlanations) values]] can be used to understand the contribution of each feature to the anomaly score, thereby providing some interpretability to the Isolation Forest model.

![[Pasted image 20240529205912.png|centered]]