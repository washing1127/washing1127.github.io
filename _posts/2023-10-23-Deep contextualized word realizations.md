---
title: 【DAILY READING】Deep contextualized word realizations
date: 2023-11-09 09:41:03 +0800
categories: [paper]
tags: [daily reading]
math: true
---


# Conclusion By Myself
The traditional technology of word representation is use an extra model to train a stable word vectors. ELMo can give a dynamic word representations by a language model. This LM is given by the architecture of biLSTM.
When we use this model, the word "apple" in "I'd like to eat apple." and "I like the products of apple." will give back in two different vectors.
# Abstract
We introduce a new type of *deep contextualized* word representation that models both:
1. complex characteristics of word use (e.g., syntax and semantics), and 
2. how these uses vary across linguistic contexts (i.e., to model polysemy).

Our word vectors are learned functions of the internal states of a deep bidirectional language model (biLM), which is pretrained on a large text corpus.
We show that these representations can be easily added to existing models and significantly improve the state of the art across six challenging NLP problems, including question answering, textual entailment and sentiment analysis.
We also present an analysis showing that exposing the deep internals of the pre-trained network is crucial, allowing downstream models to mix different types of semi-supervision signals.
# Key Points
- Pre-trained word representations are a key component in many neural language understanding models
- We use vectors derived from a bidirectional Long Short-Term Memory that is trained with a coupled language model objective on a large text corpus
- We show that the higher-level Long Short-Term Memory states capture context-dependent aspects of word meaning while lower-level states model aspects of syntax
- We show that similar signals are induced by the modified language model objective of our ELMo representations, and it can be very beneficial to learn models for downstream tasks that mix these different types of semi-supervision
- Question answering The Stanford Question Answering Dataset (SQuAD) contains 100k+ crowd sourced question-answer pairs where the answer is a span in a given Wikipedia paragraph
- We have introduced a general approach for learning high-quality deep context-dependent representations from bidirectional language model, and shown large improvements when applying ELMo to a broad range of NLP tasks
# File
[[1802.05365] Deep contextualized word representations (arxiv.org)](https://arxiv.org/abs/1802.05365) 