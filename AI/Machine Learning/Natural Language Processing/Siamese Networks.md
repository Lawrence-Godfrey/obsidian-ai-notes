Siamese networks are a type of neural network architecture that is specifically designed for comparing and recognising similarities between inputs. 

One possible architecture using [[Long-Short Term Memory networks|LSTMs]] is shown below. The same weights can be used for both models. Essentially it is only the input that changes.
![[Pasted image 20231222160048.png]]

# Loss Function
Calculating the loss for a particular sample usually uses triplet inputs, e.g., 3 different sentences. One input is an anchor, one is a positive sample, i.e., has the same meaning/is similar to the anchor, and one is a negative sample, i.e., is not similar. 

The similarity is then the similarity of the anchor and negative outputs minus the similarity of the anchor and positive outputs:
$$
Loss = s(A, N) - s(A, P)
$$

The loss will be high if the 