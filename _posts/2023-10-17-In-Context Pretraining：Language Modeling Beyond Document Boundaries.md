---
title: 【PAPER】In-Context Pretraining：Language Modeling Beyond Document Boundaries
date: 2023-10-29 20:15:59 +0800
categories: [paper]
tags: [daily reading]
math: true
---


# Conclusion By Myself
Feed more related data to model at once can significantly enhance its performance across multiple aspects.
Use the cosine similarity to determine the similarity between any two documents: $s(d_i,d_j)=\cos(\rm E\it(d_i),\rm E\it(d_j))$.
Formulate the graph traversal problem as a *maximum traveling salesman problem*, and use greedy algorithms to solve it.
# Abstract
Large language models (LMs) are currently trained to predict tokens given document prefixes, enabling them to directly perform long-form generation and prompting-style tasks which can be reduced to document completion.
Existing pretraining pipelines train LMs by concatenating random sets of short documents to create input contexts but the prior documents provide no signal for predicting the next document. 
We instead present In-Context Pretraining, a new approach where language models are pretrained on a sequence of related documents, thereby explicitly encouraging them to read and reason across document boundaries.
We can do In-Context Pretraining by simply changing the document ordering so that each context contains related document sorting problem is challenging. 
There are billions of documents and we would like to sort to maximize contextual similarity for every document without repeating any data.
To do this, we introduce approximate algorithms for finding related documents with efficient nearest neighbor search and constructing coherent input contexts with a graph traversal algorithm.
Our experiments show In-Context Pretraining offers a simple and scalable approach to significantly enhance LMs' performance: we see notable improvements in tasks that require more complex contextual reasoning, including in-context learning (+8%), reading comprehension (+15%), faithfulness to previous contexts (+16%), long-context reasoning (+5%), and retrieval augmentation (+9%).
# Key Points By AI
1. Large-scale language models predict tokens based on context and are widely applied to various tasks.
2. Existing LMs have difficulty understanding complex context, such as accurately following instructions or performing poorly in context learning.
3. The IN-CONTEXT PRETRAINING method is proposed, which creates a coherent input context by combining related documents, allowing LMs to access long relevant contexts and provide pre-training signals beyond document boundaries.
4. IN-CONTEXT PRETRAINING only changes the document order and can be intergraded into the existing pre-training process.
5. Existing pre-training methods connect random documents together, but this method cannot provide more learning signals for LMs.
6. IN-CONTEXT PRETRAINING generates a more coherent input context by connecting semantically related documents.
7. IN-CONTEXT PRETRAINING consists of two steps:
	1. Finding relevant documents in the pre-training corpus.
	2. Using these relevant documents to construct the input context.
8. To find relevant documents, a retrieval model links documents in the pre-training corpus, and retrieval scores are used to eliminate approximate duplicate documents.
9. The IN-CONTENT PRETRAINING method demonstrates strong language modeling and downstream task performance on all model scales, such as context learning, reading comprehension, and long context reasoning.
10. The improvements brought about by IN-CONTEXT PRETRAINING include: an average increase of 8% in context learning across 8 datasets; an average improvement of 15% in reading comprehension tasks; output results that are more faithful to the previous context (+16%); a 5% improvement in long context reasoning; and a 9% gain in retrieval enhancement when using external knowledge from sources like Wikipedia.
11. The results show that by simply changing the order of the pre-training documents, IN-CONTEXT PRETRAINING provides a scalable and simple method to significantly enhance understanding and reasoning about the entire context.
# File
[[2310.10638] In-Context Pretraining: Language Modeling Beyond Document Boundaries (arxiv.org)](https://arxiv.org/abs/2310.10638)
