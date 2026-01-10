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

In the original transformer architecture, the self-attention mechanism is also called *scaled dot-product attention*.

As discussed earlier, we want to compute context vectors as weighted sums over the input vectors specific to a certain input element, but now we will introduce trainable weight matrices which are updated during model training.

### 3.4.1 Computing the Attention Weights Step-by-Step

Switch to [`main.ipynb`](./main/main.ipynb) to see the implementation of computing the attention weights step-by-step.

### 3.4.2 Implementing a Compact Self-Attention Class

Switch to [`main.ipynb`](./main/main.ipynb) to see the implementation of a compact self-attention class.

## 3.5 Hiding Future Words with Causal Attention

Causal attention, also known as *masked attention*, is a mechanism used in transformer models to ensure that the prediction for a given token only depends on the tokens that come before it in the sequence. It restricts a model to only consider previous and current inputs in a sequence when processing any given token when computing attention scores. (This is contrast to the standard self-attention mechanism, which allows access to the entire input sequence at once.)

### 3.5.1 Applying a Causal Attention Mask

Switch to [`main.ipynb`](./main/main.ipynb) to see the implementation of applying a causal attention mask.

### 3.5.2 Masking Additional Attention Weights with Dropout

Switch to [`main.ipynb`](./main/main.ipynb) to see the implementation of masking additional attention weights with dropout.

### 3.5.3 Implementing a Compact Causal Attention Class

Switch to [`main.ipynb`](./main/main.ipynb) to see the implementation of a compact causal attention class.

## 3.6 Extending Single-Head Attention to Multi-Head Attention

**Multi-head** refers to dividing the attention mechanism into multiple "heads", each operating independently on different subspaces of the input data. This allows the model to capture a richer set of relationships and dependencies by attending to information from multiple perspectives simultaneously.

In this context, a single causal attention module can be considered single-head attention, where there is only one set of attention weights processing the input sequentially. Multi-head attention, on the other hand, involves multiple causal attention modules (or heads) that operate in parallel, each with its own set of attention weights. The outputs from these heads are then concatenated and linearly transformed to produce the final output.

### 3.6.1 Stacking Multiple Single-Head Attention Layers

Switch to [`main.ipynb`](./main/main.ipynb) to see the implementation of stacking multiple single-head attention layers.

### 3.6.2 Implementing Multi-Head Attention with Weight Splits

Switch to [`main.ipynb`](./main/main.ipynb) to see the implementation of multi-head attention with weight splits.