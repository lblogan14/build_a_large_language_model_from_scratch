# Chapter 1: Understanding Large Language Models

## Refresher on LLMs

General process of building an LLM involves two steps: **pretraining** and **fine-tuning**.
- **Pretraining**: The model is trained on a large corpus of text data to learn language patterns, grammar, and general knowledge. This step helps the model understand the structure and nuances of human language. The pretrained model is capable of text generation, completion, and basic comprehension tasks. It has limited few-shot learning capabilities.
- **Fine-tuning**: The pretrained model is further trained on a smaller, task-specific dataset to adapt it for particular applications, such as sentiment analysis, question answering, or translation. Fine-tuning enhances the model's performance on specific tasks by providing it with relevant examples and context. There are two main types of fine-tuning:
    - *Instruction Fine-tuning*: The model is trained on datasets that contain instructions and corresponding outputs, enabling it to follow user commands more effectively.
    - *Classification Fine-tuning*: The model is trained to categorize inputs into predefined classes, improving its ability to perform classification tasks.


The original transformer architecture consists of an encoder and a decoder.
- **Encoder**: The encoder module processes the input text and encodes it into a series of numerical representations (embeddings) that capture the meaning and context of the input.
- **Decoder**: The decoder module takes the encoded representations from the encoder and generates the output text, one token at a time, based on the learned patterns and context.

For BERT (Bidirectional Encoder Representations from Transformers), only the encoder part of the transformer architecture is used. BERT is designed for understanding the context of words in a sentence by looking at both the left and right context simultaneously. It is primarily used for tasks such as text classification, named entity recognition, and question answering.

For GPT (Generative Pre-trained Transformer), only the decoder part of the transformer architecture is used. GPT is designed for generating coherent and contextually relevant text by predicting the next word in a sequence based on the preceding words. It is primarily used for tasks such as text generation, completion, and conversational agents.



## Python Environment Setup
To set up the Python environment for this repository, follow these steps with `uv`:
1. **Create a new virtual environment**:
   ```bash
   uv venv .venv
   ```
2. **Activate the virtual environment**:
    - On Windows:
        ```bash
        .venv\Scripts\activate
        ```
    - On macOS/Linux:
        ```bash
        source .venv/bin/activate
        ```
3. **Install the required packages**:
    ```bash
    uv pip install -e .
    ```
    This command installs the current package listed in `pyproject.toml` in editable mode, allowing you to make changes to the code without reinstalling.
4. **Verify the installation**:
    ```bash
    uv pip list
    ```
5. **Deactivate the virtual environment when done**:
    ```bash
    deactivate
    ```

