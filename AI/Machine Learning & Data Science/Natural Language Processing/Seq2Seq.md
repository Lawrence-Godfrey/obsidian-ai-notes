Seq2Seq, short for Sequence-to-Sequence, is a class of models used in natural language processing tasks such as machine translation, text summarisation, and chatbot development, and use a encoder-decoder structure to take an input sequence and produce a variable length output sequence.

The original Seq2Seq model was introduced in "Sequence to Sequence Learning with Neural Networks," authored by Ilya Sutskever, Oriol Vinyals, and Quoc V. Le, and published in 2014.
### Architecture 
Seq2Seq consists of two main components: an encoder and a decoder. The encoder processes the input sequence and compresses the information into a context vector, often a single fixed-length vector at the end of the encoding phase. The decoder then generates the output sequence from this vector.
### Context Vector
This is a critical part of the Seq2Seq model. The encoder transforms the input sequence into this context vector, which ideally captures its semantic essence. The quality of this vector significantly impacts the model's performance.
### Drawbacks
Since the model had a fixed context vector (hidden state) it decreased in performance on longer contexts. This was largely fixed with the introduction of [[Attention]], a mechanism that allows the model to dynamically focus on different parts of the input sequence.