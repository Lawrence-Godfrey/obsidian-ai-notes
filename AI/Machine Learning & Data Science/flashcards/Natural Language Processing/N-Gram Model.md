#flashcards

What is an N-gram?
?
An N-gram is a sequence of N consecutive words or characters within a given text.

Provide an example of bi-grams from the sentence 'I love to eat ice cream'.
?
The bi-grams are 'I love', 'love to', 'to eat', 'eat ice', and 'ice cream'.

How do you calculate the probability of a word given an N-gram?
?
The probability is calculated as P(w_n|w_{n-N+1}^{n-1}) = C(w_{n-N+1}^{n-1}, w_n) / C(w_{n-N+1}^{n-1}), where C is the count function.

What is the significance of the row sum in an N-gram probability table?
?
The row sum is used to normalize the counts by dividing each cell by the sum of the row to find the probabilities.

What is the Chain Rule in the context of N-grams?
?
The Chain Rule calculates the probability of a sequence of words as the conditional probability of each word given the previous words.

How does the Markov assumption simplify probability calculations in N-grams?
?
The Markov assumption allows us to approximate probabilities using only the previous word instead of all previous words.

What tokens are added at the start and end of sequences for N-gram models?
?
Start tokens (e.g., '<s>') are added to the start and an end token (e.g., '</s>') is added to the end.

What does the term Out of Vocabulary (OOV) refer to?
?
OOV refers to words in a corpus that are not in the vocabulary used by the model.

How does Laplacian Smoothing work?
?
Laplacian Smoothing adds 1 to the numerator and V (the vocabulary size) to the denominator to handle unseen N-grams.

What is 'Stupid' Backoff smoothing?
?
'Stupid' Backoff uses smaller N-grams multiplied by a constant when larger N-grams are not found.

What are the parameters in the 'Stupid' Backoff formula?
?
The parameters λ1, λ2, λ3 are coefficients such that the sum of all λ equals 1.

What problem does adding start and end tokens solve in N-gram models?
?
It allows for the calculation of probabilities at the beginning and end of sequences, and helps with the variable-length sequence problem.

Why should OOV handling be used sparingly with a certain token like <UNK>?
?
Using <UNK> too much can artificially inflate the model's performance by assuming high probabilities for sequences of <UNK>.

Describe Add-K smoothing. What advantage does it offer over Laplacian smoothing?
?
Add-K smoothing generalizes Laplacian smoothing by allowing the addition of a constant K instead of just 1, which can provide better results for larger corpuses.

How does the N-gram model handle unseen N-grams?
?
Unseen N-grams are managed using smoothing techniques like Laplacian Smoothing or 'Stupid' Backoff.

