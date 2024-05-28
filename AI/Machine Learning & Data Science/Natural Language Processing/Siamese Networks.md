Siamese networks are a type of neural network architecture that is specifically designed for comparing and recognising similarities between inputs. 

One possible architecture using [[Long-Short Term Memory networks|LSTMs]] is shown below. The same weights can be used for both models. Essentially it is only the input that changes.
![[Pasted image 20231222160048.png]]

## Loss Function
Calculating the loss for a particular sample usually uses triplet inputs, e.g., 3 different sentences. One input is an anchor, one is a positive sample, i.e., has the same meaning/is similar to the anchor, and one is a negative sample, i.e., is not similar. This is known as [[Loss Functions#Triplet Loss|Triplet Loss]].

## Computing Cost
To compute the cost of a batch of training examples you can build two batches of samples, where each sample in the first batch corresponds to (is similar to/has same meaning) a sample in the second batch. 

You then have your anchor (the sample in batch 1), positive sample (the corresponding sample in batch 2) and a number of negative samples (all the other samples in batch 2), provided there are no duplicates in batch 1. 

Once the similarity scores have been calculated for all the samples, you can create a matrix of scores like the one below, where all the scores on the diagonal should be close to 1, and all non-diagonals should be close to -1:

![[Pasted image 20231222162718.png|center]]

We now have the positive similarities, and a number of negatives for each sample. Our loss function only caters for a single negative similarity, so we need a way to squash the negative similarities into a single number. 

We can either take the mean of the negative scores, known as the mean negative, or take the closest negative (0.3 in the example above for the first sample).


