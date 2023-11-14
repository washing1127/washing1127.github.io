---
title: 【DAILY READING】Efficient Estimation of Word Representations in Vector Space
date: 2023-10-29 20:15:27 +0800
categories: [paper]
tags: [daily reading]
math: true
mermaid: true
---


# Conclusion By Myself
This paper introduced two model architectures to deal with the problems when computing the word vectors. The two architectures are CBOW and skip-gram. Specifically, the CBOW is predicts the word in the middle by using the words around it. Conversely, the skip-gram is uses the middle word to predict other words around.
This paper is seen as the first word embedding model nowadays.
# Abstract
We propose two novel model architectures for computing continuous vector representations of words from very large data sets.
The quality of these representations is measured in a **word similarity** task, and the results are compared to the previously best performing techniques based on different types of neural networks.
We observe large improvements in **accuracy** at much lower computational cost, i.e. it takes less than a day to learn high quality word vectors from a 1.6 billion words data set.
Furthermore, we show that these vectors provide state-of-the-art performance on our test set for measuring **syntactic and semantic** word similarities.
# Key Points By AI
- Many current NLP systems and techniques tread words as atomic units - there is no notion of similarity between worlds, as these are represented as indices in a vocabulary.
- An examples is the popular N-gram model used for statistical language modeling - today it is possible to train N-grams on virtually all available data.
- We focus on distributed representations of words learned by neural networks, as it was previously shown that they perform significantly better than Latent Semantic Analysis for preserving linear regularities among words; Latent Dirichlet Allocation becomes computationally very expensive on large data sets.
- In this paper we studied the quality of vector representations of words derived by various models on a collection of syntactic and semantic language tasks.
- The neural network based word vectors were previously applied to many other NLP tasks, for example sentiment analysis and paraphrase detection.
- It can be expected that these applications can benefit from the model architectures described in this paper.
# File
[[1301.3781] Efficient Estimation of Word Representations in Vector Space (arxiv.org)](https://arxiv.org/abs/1301.3781) 