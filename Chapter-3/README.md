# Chapter 3: Coding Attention Mechanism

This chapter covers the implementation of the attention mechanism, which is a core component of transformer-based large language models (LLMs). The attention mechanism allows the model to focus on different parts of the input sequence when generating each token in the output sequence, enabling it to capture long-range dependencies and contextual relationships in the data.

## 3.1 The Problem with Modeling Long Sequences

Traditional encoder-decoder RNNs and LSTMs struggle to model long sequences due to issues like vanishing gradients and limited memory capacity. The attention mechanism addresses these challenges by allowing the model to dynamically weigh the importance of different tokens in the input sequence, regardless of their distance from the current token being processed.

## 3.2 Capturing Data Dependencies with Attention Mechanisms

Self-attention in transformers is a mechanism that allows each position in the input sequence to consider the relevancy of all other positions in the same sequence when computing the representation of a sequence.

## 3.3 Attending to Different Parts of the Input with Self-Attention

"Self"-attention refers to the mechanism where the model attends to different parts of the same input sequence to compute a representation for each token. It assesses and learns the inner relationships and dependencies between various parts of the input data itself, such as words in a sentence or pixels in an image.

Contrast to traditional "cross"-attention mechanisms, where the focus is on the relationships between elements of **two** different sequences, such as in sequence-to-sequence models where the attention is applied between an input sequence (like a source sentence) and an output sequence (like a target sentence).

### 3.3.1 A Simple Self-Attention Mechanism without Trainable Weights

Switch to [`main.ipynb`](./main/main.ipynb) to see the implementation of a simple self-attention mechanism without trainable weights.

### 3.3.2 Computing Attention Weights for All Input Tokens

Switch to [`main.ipynb`](./main/main.ipynb) to see the implementation of computing attention weights for all input tokens.

## 3.4 Implementing Self-Attention with Trainable Weights

Switch to [`main.ipynb`](./main/main.ipynb) to see the implementation of self-attention with trainable weights.