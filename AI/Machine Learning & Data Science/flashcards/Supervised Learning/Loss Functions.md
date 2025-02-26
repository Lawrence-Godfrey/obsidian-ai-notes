#flashcards

What is the purpose of loss functions in supervised learning?
?
Loss functions measure the error or deviation between the predicted output and the actual target output.

Define the Frobenius norm of a matrix.
?
The Frobenius norm is defined as \( \parallel A \parallel_{F} = \sqrt{\sum\limits_{i=1}^{m}\sum\limits_{j=1}^{n}|a_{ij}|^2} \), which measures the overall magnitude of the matrix.

How is the loss calculated using the Frobenius norm?
?
Loss is calculated as \( Loss = \parallel X\Theta - Y \parallel_F \), where \( \Theta \) are the parameters of the model.

What modification is often made to the loss calculation using the Frobenius norm, and why?
?
The loss is often calculated as the square of the Frobenius norm divided by \( m \) (the number of examples) to simplify the derivative calculation, but it does not change the outcome when minimizing the loss.

What is the derivative of the squared Frobenius norm loss?
?
The derivative is given by \( \frac{d}{d\Theta}Loss = \frac{2}{m}(X^T(X\Theta - Y)) \).

What is the formula for Cross-Entropy Loss?
?
Cross-Entropy Loss is defined as: \( H(p, q) = -\sum\limits_{i}p(i) \log q(i) \).

In what scenarios is cross-entropy loss commonly used?
?
It is commonly used in classification problems in machine learning, especially in neural networks.

How does symmetric cross-entropy differ from normal cross-entropy?
?
Symmetric cross-entropy calculates the average of two cross-entropy losses in both directions, making it useful for complex models.

What is the formula for symmetric cross-entropy loss?
?
The formula is given by: \( H(p, q)_{sym} = \frac{1}{2}(H(p, q) + H(q, p)) \).

What is contrastive loss used for?
?
Contrastive loss is used to find similarity or dissimilarity between two instances in tasks such as face recognition or signature verification.

What is the formula for contrastive loss?
?
The formula is \( L = yd^{2} + (1-y)Max(0, m-d)^{2} \).

What challenges does contrastive loss face?
?
It faces issues with 'hard negatives' and 'hard positives', making it difficult for the model to distinguish between labeled similar or dissimilar samples.

What does triplet loss improve upon compared to contrastive loss?
?
Triplet loss prioritizes the distance between the positive and negative samples rather than just the anchor, addressing the issues of hard samples encountered with contrastive loss.

What is the formula for triplet loss?
?
The formula is \( L = Max(0, d_{AP} - d_{AN} + m) \).

What is triplet mining?
?
Triplet mining aims to choose hard examples when training on triplets, making the model more robust and utilizing the data more effectively.

What does the margin \( m \) represent in contrastive and triplet loss?
?
The margin \( m \) determines the minimum distance that similar and dissimilar samples should maintain from each other.

