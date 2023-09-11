### Stop Words and Punctuation
Stop words, like _and_, _is_, _are_, _at_, etc. as well as punctuation can often be removed before training a model since they don't provide much information for certain tasks. There are also certain tokens specific to certain domains which can be removed, like @'s in a tweet or urls.
### Stemming
Stemming is the process of reducing a word to its root or base form. For example, __tuning__ can be reduced to the form __tun__. This can help a model more easily learn the underlying meaning of words by treating different forms of the same word as identical.
### Normalising Case
Normalising the case of all words, i.e. lowercasing them, can help models learn relationships between words more easily.

