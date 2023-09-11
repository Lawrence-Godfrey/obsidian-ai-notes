In natural language processing, feature extraction refers to the process of transforming raw text data into a format that can be understood and analysed by machine learning algorithms.

### Vocabulary Vectors
Using vocabulary vectors is a very simple approach to representing a word or phrase as a vector, where the size of the vector is the size of your vocabulary, and you extract the embedding for a phrase by setting each corresponding element in the vector to a 1.
#### Problems with Sparse Representations
As your vocabulary size becomes larger, your vector becomes more and more sparse (a larger portion of the vector are zeros) which can have an effect on the efficiency and performance of various natural language processing tasks. 
### Feature Extraction with Frequencies
If you have a set of examples of phrases split into different classes, you can generate frequency vectors for each class by incrementing the count for every time a word shows up in the class. This results in $k$ vectors of size $v$, where $k$ is the number of classes and $v$ is the size of your vocabulary.
Then, given a new example, you can generate a feature vector $X$ by summing up the corresponding frequencies of every word in your different classes. An example can then be classified by how frequently it's words show up in a given class. 
$$X_{m}= [1, \sum\limits_wfreqs(w,0),\sum\limits_{w}freqs(w,1)...\sum\limits_{w}freqs(w,k)]$$
Where $freqs(w,k)$ is the frequency of word $w$ in class $k$.
