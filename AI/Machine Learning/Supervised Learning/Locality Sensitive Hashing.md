Locality Sensitive Hashing (LSH) is a method used for approximate [[K-Nearest Neighbours]] search, which allows for the efficient retrieval of similar items from large datasets. LSH works particularly well in high-dimensional spaces where traditional methods can be computationally prohibitive.

The fundamental idea behind LSH is to hash input items in such a way that similar items are more likely to be hashed to the same bucket, while dissimilar items are more likely to be hashed to different buckets.

### Multiple Planes
One way to do this is to create a set of planes which divide up your dataset. Each plane is described by it's normal vector $P$. Given a new vector $v$, you can calculate the dot product of that point with each plane, and use the sign of the product to indicate which side of the plane the point is on. 

$$
\begin{aligned}
P_{1}\cdot v = 3, h_{1}=1 \\

P_{2}\cdot v = -3, h_{1}=0 \\

P_{3}\cdot v = 3, h_{1}=1 \\
\end{aligned}
$$
![[Pasted image 20230911200819.png|centre]]

These signs (0 or 1) are then multiplied by exponentially increasing numbers and summed to produce a hash value.
$$
hash = 2^{0}\times h_{1}+2^{1}\times h_{2}+ 2^{2}\times h_{3}
$$

Formally:
$$
hash = \sum\limits_{i}^{H}2^{i}\times h_{i}
$$
