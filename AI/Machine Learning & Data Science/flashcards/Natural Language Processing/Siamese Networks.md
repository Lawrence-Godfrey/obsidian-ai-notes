#flashcards

What are Siamese networks primarily designed for?
?
They are designed for comparing and recognizing similarities between inputs.

What type of neural network can be used in a Siamese network architecture?
?
Long-Short Term Memory networks (LSTMs).

In the context of Siamese networks, what does 'triplet inputs' refer to?
?
It refers to using three different sentences: an anchor, a positive sample that is similar to the anchor, and a negative sample that is not similar.

What is the triplet loss function used for?
?
It is used to calculate the loss for a particular sample based on the anchor, positive sample, and negative sample.

How do you compute the cost of training examples in Siamese networks?
?
By building two batches of samples where each sample in the first batch corresponds to a similar sample in the second batch.

What should the scores on the diagonal of the similarity matrix be close to?
?
Close to 1.

What should the scores on the non-diagonal of the similarity matrix be close to?
?
Close to -1.

How can negative similarities be consolidated into a single number?
?
By taking the mean of the negative scores or taking the closest negative score.

What is the significance of using the same weights for both models in a Siamese network?
?
It ensures that the comparison between inputs is consistent, as only the input changes.

What is a similarity score matrix in the context of Siamese networks?
?
It is a matrix that contains calculated similarity scores for all samples, where diagonal elements represent positive similarities and non-diagonal elements represent negative similarities.

