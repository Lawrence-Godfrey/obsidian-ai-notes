A co-occurrence matrix captures the frequencies with which pairs of words appear together in a certain context. The "context" can be defined in various ways: it might be within a fixed window of $n$ words, within the same sentence, or some other scope.

For a simple example, consider the sentences:

1. "I love to eat apples."
2. "Apples are nutritious."
3. "I love nutritious food."

A co-occurrence matrix (with a window size of 1 word) might look something like:

| |I|love|to|eat|apples|are|nutritious|food|
|---|---|---|---|---|---|---|---|---|
|I|0|2|1|0|0|0|0|0|
|love|2|0|1|1|0|0|1|1|
|...|||||||||

Each entry (i, j) in the matrix indicates how often word i appears next to word j in the corpus.

This raw co-occurrence matrix can be used for various purposes:

- Semantic Analysis: Words that frequently appear together are likely related in meaning.
- Building embeddings: Techniques like [[GloVe]] leverage co-occurrence statistics to generate word embeddings.
