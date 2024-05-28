In a **Term-Document Matrix (TDM)** or **Document-Term Matrix (DTM)**:
- **Rows** represent terms (words or sometimes phrases).
- **Columns** represent documents.
- **Entries** in the matrix indicate the frequency (or sometimes weighted frequency) of a term in a particular document.

For example, consider you have the following three documents:

1. "I love apples."
2. "Apples are sweet."
3. "I love sweet food."

A simple Term-Document Matrix might look something like:

| |Doc1|Doc2|Doc3|
|---|---|---|---|
|I|1|0|1|
|love|1|0|1|
|apples|1|1|0|
|are|0|1|0|
|sweet|0|1|1|
|food|0|0|1|

In this matrix:

- A row represents a term.
- A column represents a document.
- The value at a given cell (term, document) represents the frequency of that term in the document.

A common enhancement to raw frequencies in a TDM is the use of **TF-IDF ([[Term Frequency-Inverse Document Frequency]])**. TF-IDF weighs terms by their importance, giving higher weights to terms that are frequent in a specific document but not across many documents in the corpus.