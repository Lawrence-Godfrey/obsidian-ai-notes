#flashcards

What does Bayes' theorem allow you to calculate?
?
It allows you to find the probability of an event based on the probability of a related event.

State Bayes' theorem formula.
?
P(A|B) = \frac{P(B|A) \times P(A)}{P(B)}

What does the term P(A) represent in Bayes' theorem?
?
P(A) is the 'prior', for example, in spam classification, it represents the percentage of emails that are spam.

In the context of spam classification, what does P(B) signify?
?
P(B) is the overall probability of event B occurring, which could be represented in terms of the Law of Total Probability.

What is the Law of Total Probability?
?
It states that if A and its complement A^c form a complete partition of the sample space, then P(B) can be expressed as P(B) = P(B|A) * P(A) + P(B|A^c) * P(A^c).

In spam classification, what does P(A|B) represent?
?
P(A|B) represents the probability that the email is spam given that it contains the word 'lottery'.

What makes applying Bayes' theorem challenging in high-dimensional data?
?
The challenge arises because you have multiple events affecting the outcome, which requires extensive examples including all relevant features for accurate calculations.

What is Naïve Bayes?
?
Naïve Bayes is a simplified version of Bayes' Rule that assumes each feature in the dataset is independent.

Why is the assumption of independence in Naïve Bayes useful?
?
It simplifies the computation of probabilities in high-dimensional datasets by allowing isolation of features.

Can you explain how Bayes' theorem can be applied in real-world scenarios besides spam classification?
?
Bayes' theorem can be applied in various fields like medical diagnosis, risk assessment, and machine learning for predictive analytics.

