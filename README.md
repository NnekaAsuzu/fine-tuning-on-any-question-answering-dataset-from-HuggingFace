# Question Answering System with Fine-Tuned HuggingFace Model and Gradio Interface

## Overview

This project demonstrates how to perform fine-tuning on a question-answering dataset from HuggingFace and save the model. The saved model is then used to build a Gradio interface, which allows users to input a context and a question to receive the model's answer.

## Installation

To run the notebook, install the required libraries:

```bash
!pip install datasets evaluate transformers[sentencepiece]
!pip install accelerate
!apt install git-lfs
!pip install datasets
!pip install transformers datasets torch gradio

## Stanford Question Answering Dataset (SQuAD)

The Stanford Question Answering Dataset (SQuAD) is a popular dataset for machine reading comprehension tasks. It consists of questions posed by crowdworkers on a set of Wikipedia articles, where the answer to every question is a segment of text from the corresponding article.

The dataset is divided into two subsets: SQuAD1.1 and SQuAD2.0. SQuAD1.1 contains questions that can be answered based on the provided context, while SQuAD2.0 contains unanswerable questions as well.

In this project, we use the SQuAD dataset to fine-tune a HuggingFace model for question answering, and then use the fine-tuned model to build a Gradio interface for interactive question answering.

To download and load the SQuAD dataset, use the following code:

```python
from datasets import load_dataset

dataset = load_dataset("squad")


