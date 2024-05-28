In Natural Language Processing, autocorrect is the task of automatically correcting misspelled words or grammatically incorrect phrases in written text. This generally works by first identifying misspelled words, then finding similar words, and finally choosing the most likely correct word based on context.
1. Identifying misspelled words could be as simple as checking whether every word is a valid word in your vocabulary, or could be more complex, and take into consideration factors such as context, grammar, and language rules.
2. To find similar words you can use n-edit distance techniques to find every string that is n-edits from the misspelled word.
3. You can calculate the probability of each candidate word by dividing it's frequency in the corpus by the size of the vocabulary, or by using more advanced statistical techniques such as n-gram models.
### Minimum Edit Distance
Minimum edit distance is a technique used to compare the similarity between two strings. It calculates the minimum number of edits (deletions, additions, replacements of characters) needed to transform the one string into the other.
#### Levenshtein Distance
The algorithm for finding this distance uses a table where the rows $i$ correlate to the source word and the columns $j$ to the target word. Each element in the table represents the distance from $source[:i] \rightarrow target[:j]$. 

The algorithm calculates the distance $D$ at every position using the already calculated distances $D[i-1, j]$, $D[i, j-1]$ and $D[i-1, j-1]$:

![[Pasted image 20231008175523.png]]

![[Pasted image 20231008174942.png]]

![[Pasted image 20231008175718.png|center]]

