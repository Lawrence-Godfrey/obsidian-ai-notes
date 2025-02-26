#flashcards

What is the task of autocorrect in Natural Language Processing?
?
Automatically correcting misspelled words or grammatically incorrect phrases in written text.

What are the steps involved in autocorrect?
?
1. Identify misspelled words. 2. Find similar words. 3. Choose the most likely correct word based on context.

How can misspelled words be identified?
?
By checking if each word is valid in the vocabulary or considering context, grammar, and language rules.

What technique can be used to find similar words to a misspelled word?
?
n-edit distance techniques.

How can the probability of a candidate word be calculated in autocorrect?
?
By dividing its frequency in the corpus by the size of the vocabulary or using advanced statistical techniques such as n-gram models.

What is minimum edit distance?
?
A technique used to compare the similarity between two strings by calculating the minimum number of edits needed to transform one string into another.

What is Levenshtein Distance?
?
An algorithm for finding the minimum edit distance that uses a table to calculate distances between substrings of the source and target words.

In the Levenshtein Distance algorithm, what do the rows and columns of the table represent?
?
Rows correlate to the source word and columns correlate to the target word.

How is distance D calculated in the Levenshtein Distance algorithm?
?
Using already calculated distances D[i-1, j], D[i, j-1], and D[i-1, j-1].

What are the types of edits considered in calculating minimum edit distance?
?
Deletions, additions, and replacements of characters.

