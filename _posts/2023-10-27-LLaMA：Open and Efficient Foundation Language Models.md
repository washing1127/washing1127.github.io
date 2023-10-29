---
title: 【DAILY READING】LLaMA：Open and Efficient Foundation Language Models
date: 2023-10-29 23:03:16 +0800
categories: [paper]
tags: [daily reading]
math: true
---


# Conclusion By Myself
This is a really clearly paper.
It introduces the LLaMA. 
LLaMA's **training** approach is similar to the methods described in [Brown et al., 2020](#);[Chowdhery et al., 2020](#), and is inspired by the [Chinchilla scaling laws](#).
Transformer is the base architecture of LLaMA. More specifically, it uses [RMSNorma normalizing function](#), replaces the ReLU non-linearity by the [SwiGLU Activation function](#), and use the [Rotary Positional Embeddings](#) instead of the absolute position embeddings.
LLaMAs are trained using the [AdamW optimizer](#), ant it also tried the optimize of models, such as use the inspiration from [Rabe and Staats](#) and the backward from [Dao et al.](#) to reduce the memory usage and runtime.
These papers above are readable for me.
# Abstract
We introduce LLaMA, a collection of foundation language models ranging from 7B to 65B parameters.
We train our models on trillions of tokens, and show that it is possible to train SOTA models using publicly available datasets exclusively, without resorting to proprietary and inaccessible datasets.
In particular, LLaMA-13B outperform GPT-3 (175B) on most benchmarks, and LLaMA-65B is competitive with the best models, Chinchilla-70B and PaLM-540B.
We release all our models to the research community.
# Key Points By AI
- LLMs trained on massive corpora of texts have shown their ability to perform new tasks from textual instructions or from a few examples
- We include two book corpora in our training datasets: the Gutenberg Project, which contains books that are in the public domain, and the Books3 section of ThePile, a publicly available dataset for training large language models
- While we have selected some of the standard benchmarks that are used by the language model community to indicate some of the issues with these models, these evaluations are not sufficient to fully understand the risks associated with these models
- We presented a series of language models that are released openly, and competitive with SOTA foundation models
- LLaMA-13B outperforms GPT-3 while being more than 10x smaller, and LLaMA-65B is competitive with Chinchilla-70B and PaLM-540B
- We observe that our model is significantly better at performing co-reference resolution for the "their/them/someone" pronouns than for the "her/her/she" and "his/him/he" pronouns
- We hope that releasing these models to the research community will accelerate the development of large language models, and help efforts to improve their robustness and mitigate known issues such as toxicity and bias
# File
[[2302.13971] LLaMA: Open and Efficient Foundation Language Models (arxiv.org)](https://arxiv.org/abs/2302.13971) 