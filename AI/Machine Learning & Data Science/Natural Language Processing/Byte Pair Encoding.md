Byte Pair Encoding (BPE) is a data compression technique adapted for tokenisation in natural language processing. It works by iteratively replacing the most frequent pair of adjacent symbols (or bytes) with a new symbol, effectively building a vocabulary of subword units.
### In NLP, BPE is used to:
- **Handle out-of-vocabulary (OOV) words** by breaking them into known subword units.
- **Reduce vocabulary size** while maintaining the ability to represent any word. 
- **Improve generalisation** by allowing the model to learn common morphemes or frequent substrings.
### How it works in NLP:
1. Start with a corpus split into characters (e.g., `l o w e r`).
2. Count the frequency of all adjacent symbol pairs.
3. Merge the most frequent pair (e.g., `l o` → `lo`).
4. Repeat steps 2–3 for a predefined number of merges or until a desired vocabulary size is reached.

This leads to a tokenisation scheme where frequent words remain intact, and rare words are broken into meaningful subword components.