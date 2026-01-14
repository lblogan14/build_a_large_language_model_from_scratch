# Chapter 7: Fine-Tuning to Follow Instructions

In this chapter, we will explore how to fine-tune the pretrained GPT model to follow instructions using instruction-following datasets.

## 7.1 Introduction to Instruction Fine-Tuning

The **instruction fine-tuning** is also known as *supervised instruction fine-tuning*. It involves training a language model on a diverse set of tasks using specific instructions to improve its ability to understand and execute tasks described in natural language prompts. This process helps the model generalize better across various tasks and respond more accurately to user queries.

## 7.2 Preparing a Dataset for Supervised Instruction Fine-Tuning

Switch to [`main.ipynb`](./main/main.ipynb) to implement data loading and preprocessing steps for the instruction-following dataset, ensuring that the data is in the correct format for training the model.