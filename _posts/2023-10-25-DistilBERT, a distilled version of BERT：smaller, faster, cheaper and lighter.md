---
title: 【PAPER】DistilBERT, a distilled version of BERT：smaller, faster, cheaper and lighter
date: 2023-10-29 20:15:11 +0800
categories: [paper]
tags: [daily reading]
math: true
---


# Conclusion By Myself
This paper is about distilling BERT model. It is not so hard to read, but because the lacking of the distilling knowledge, I still can not clearly know what it said, Aha.
It introduces "a triple loss", "cosine-distance losses", I don't what it is, and the paper says nothing about it either. (May it said, but I missed it.)
But this gives a light that distilling can indeed help me with the problems in my real work now. Let's do more research.
# Abstract
As Transfer Learning from large-scale pre-trained models becomes more prevalent in Natural Language Processing (NLP), operating these large models in on-the-edge and/or under constrained computational training or inference budgets remain challenging.
In this work, we propose a method to pre-train a smaller general-purpose language representation model, called DistilBERT, which can then be fine-tuned with good performances on a wide range of tasks like its larger counterparts.
While most prior work investigated the use of distillation for building task-specific models, we leverage knowledge distillation during the pre-training phase and show that it is possible to reduce the size of a BERT model by 40%, while retaining 97% of its language understanding capabilities and being 60% faster.
To leverage the inductive biases learned by larger models during pre-training, we introduce a triple loss combining language modeling, distillation and cosine-distance losses.
Our smaller, faster and lighter model is cheaper to pre-train and we demonstrate its capabilities for on-device computations in a proof-of-concept experiment and a comparative on-device study.
# Key Points By AI
- This report introduces the recent rise of transfer learning in the field of natural language processing and the application of large-scale pre-trained language models in NLP tasks. These models typically have hundreds of billions of parameters, and current pre-trained model research indicates that training larger models still improves the performance of downstream tasks. However, this trend has also brought several concerns, including the environmental burden and the increasing computational and memory requirements.
- To address these concerns, this paper introduces a method for training smaller language models using knowledge distillation. This method improves the performance of inference time while requiring less computational training budget. Our general pre-trained model can be used for multiple downstream tasks and retains the flexibility of a large model. We also demonstrate that our compressed model can be run on edge devices, such as mobile devices.
- We use the triple loss method to train a 40% smaller knowledge distillation version of the Transformer, and ourselves train a larger Transformer language model. The method enables us to achieve similar performance on multiple downstream tasks while reducing inference time by 60%. Further ablation study shows that all triple loss components are key factors to achieve optimal performance. We also make the training code and weights public to allow other to experiment with the model.
- Finally, we evaluate the performance of DistilBERT in general language understanding tasks and downstream tasks, and the results show that it performs well on some tasks. We further investigate the performance of DistilBERT in several downstream tasks, including a classification task and a question answering task. On the SQuAD, DistilBERT only trails the full BERT model by 3.5 percentage points.
- This paper introduces DistilBERT, a general language model based on BERT pre-training that is 40% smaller and 60% faster than BERT. By analyzing the ablation study, we find that knowledge distillation can successfully train a general language model and DistilBERT has potential for edge applications.
# File
[[1910.01108] DistilBERT, a distilled version of BERT: smaller, faster, cheaper and lighter (arxiv.org)](https://arxiv.org/abs/1910.01108) 