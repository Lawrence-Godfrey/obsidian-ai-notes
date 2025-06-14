#flashcards

What are stop words?
?
Stop words are common words such as 'and', 'is', 'are', 'at', etc. that can often be removed before training a model as they don't provide much information for certain tasks.

Give examples of specific tokens that might be removed for certain domains.
?
Tokens like @'s in tweets and URLs can be removed.

What is stemming in the context of natural language processing?
?
Stemming is the process of reducing a word to its root or base form, such as reducing 'tuning' to 'tun'.

How does stemming help in model training?
?
Stemming allows a model to learn the underlying meaning of words more easily by treating different forms of the same word as identical.

What does normalising case mean?
?
Normalising case refers to the process of converting all words to lowercase to help models learn relationships between words more easily.

What is the purpose of creating a symbol to represent numbers in a dataset?
?
Creating a symbol like '<NUMBER>' to represent any number can help standardize the representation of numerical data in the corpus.

What is a specific example of a special number that can be handled differently?
?
Special numbers like 3.14159 can be left as is or assigned their own separate symbol.

Why might punctuation be collapsed when preparing data for a model?
?
Collapsing sequences of the same punctuation into one, such as reducing '!!!' to '!', can reduce noise and improve model training efficiency.

What is the goal when removing stop words and punctuation in data preparation?
?
The goal is to focus on the words and tokens that carry more meaningful information for the specific task at hand.

Can you mention a situation where it might not be appropriate to remove stop words?
?
In tasks such as sentiment analysis or certain NLP applications, stop words can carry important contextual information and might not be removed.

