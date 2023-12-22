One way to represent a word in your vocabulary as a vector is to use one-hot vectors. One-hot vectors are binary vectors where all elements are zero except for one element, set to one, which corresponds to a particular word.

**Pros**: 
 - Simple
 - No implied ordering
**Cons**:
 - Huge vectors, scaling with vocabulary size
 - No embedded meaning; can't compare words meaningfully.