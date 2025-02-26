#flashcards

What is the main issue with using Euclidean distance for vector similarity?
?
Euclidean distance can be skewed by the relative magnitude of the vectors.

What similarity metric should be used when the angle between vectors is more important than their magnitude?
?
Cosine similarity.

What is the formula for cosine of the angle between two vectors \\(\hat{v}\) and \\(\hat{w}\\)?
?
\\(cos(\beta) = \frac{\hat{v} \cdot \hat{w}}{\parallel\hat{v}\parallel \parallel\hat{w}\parallel}\\.

What does a cosine similarity of 0 indicate about two vectors?
?
It indicates that the vectors are orthogonal (at a 90-degree angle to each other).

What does a cosine similarity of 1 indicate about two vectors?
?
It indicates that the vectors have the exact same direction.

Why is cosine similarity often preferred over Euclidean distance in text analysis?
?
Because it focuses on the angle between vectors rather than their magnitude, which is more relevant for comparing the orientation of text data.

What does the term 'dot product' refer to in the context of the cosine similarity formula?
?
The dot product is the numerator in the cosine similarity formula, representing the projection of one vector onto another.

How does cosine similarity range between vectors typically?
?
Cosine similarity ranges from -1 to 1, where -1 indicates opposite directions, 0 indicates orthogonality, and 1 indicates identical directions.

