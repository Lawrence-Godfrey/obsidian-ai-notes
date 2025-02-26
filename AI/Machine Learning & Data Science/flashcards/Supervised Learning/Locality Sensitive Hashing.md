#flashcards

What is Locality Sensitive Hashing (LSH) used for?
?
LSH is used for approximate K-Nearest Neighbours search, enabling efficient retrieval of similar items from large datasets.

Why is LSH particularly advantageous in high-dimensional spaces?
?
Because traditional methods for searching nearest neighbours can be computationally prohibitive in high-dimensional spaces.

How does Locality Sensitive Hashing (LSH) work?
?
LSH hashes input items such that similar items are more likely to be hashed into the same bucket, while dissimilar items are more likely to be hashed into different buckets.

What is the role of planes in the LSH method?
?
Planes divide the dataset; each plane is associated with a normal vector that helps determine which side of the plane a point lies on.

How do you determine which side of a plane a point is on in LSH?
?
By calculating the dot product of the point with the plane's normal vector and checking the sign of the product.

Given the equations, what do the signs represent in the LSH process?
?
The signs (0 or 1) represent which side of each plane the point is located on.

What formula is used to produce the hash value in LSH?
?
hash = ∑(2^i × h_i) for i = 0 to H, where h_i are the signs associated with the planes.

Write the hash value calculation for three planes based on their respective signs.
?
hash = 2^0 × h_1 + 2^1 × h_2 + 2^2 × h_3.

What is the significance of using exponentially increasing numbers in the hash calculation?
?
Using exponentially increasing numbers helps to ensure that each bit in the final hash code has a distinct weight, which maximizes the uniqueness of the hash.

What is a potential application of LSH in data science?
?
LSH can be used in image retrieval systems, recommendation engines, and clustering tasks to quickly find similar items.

