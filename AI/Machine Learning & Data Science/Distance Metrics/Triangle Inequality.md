The **triangle inequality** is a fundamental concept in mathematics, particularly in vector spaces and norms. It states that for any vectors xxx and yyy in a normed space:

$$||x + y|| \leq ||x|| + ||y||$$

 - This means that the length of the sum of two vectors is at most the sum of the lengths of the vectors. 
 - Geometrically, it’s like saying “the shortest path between two points is a straight line”.

This is important because many algorithms assume the [[Breakdown of Common Metrics|distance function]] you use satisfies this property (but not all do).

When approximate methods or optimisations (KD-Trees, Ball Trees) are used, the triangle inequality becomes important.
- It's used to prune/skip nodes and trees in the search space.

[[Euclidean Distance vs Cosine Similarity|Cosine distance]] does not satisfy the triangle inequality and therefore is not a "proper" metric. 
- [[HNSW]] only works with cosine distance because it uses a graph-traversal heuristic, not geometric pruning. 

