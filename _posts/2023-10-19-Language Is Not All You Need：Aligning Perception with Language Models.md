---
title: 【DAILY READING】Language Is Not All You Need：Aligning Perception with Language Models
date: 2023-11-09 09:40:19 +0800
categories: [paper]
tags: [daily reading]
math: true
mermaid: true
---


# Conclusion By Myself
This paper introduced a Multimodal LLM, which combine image tasks and text tasks together.
It use CLIP ViT-L/14 model to representing the pic, and use a transformer based model MAGNETO to do the language model work.
The final result shows that going from LLMs to MLLMs enables new capabilities and opportunities.
There are three conclusion in this paper by authors:
- From LLMs to MLLMs:
	- enable LLMs to get knowledge beyond text description.
	- opens a new task door to LLMs.
	- unified various APIs.
- Language models as general-purpose interface
- New capabilities of MLLMs:
	- zero- and few-shot
	- nonverbal reasoning
	- multi-turn interactions

# Abstract
A big convergence of language, multimodal perception, action, and world modeling is a key step toward artificial general intelligence.
In this work, we introduce *KOSMOS-1*, a Multimodal Large Language Model (MLLM) that can perceive general modalities, learn in context (i.e., few-shot), and follow instructions (i.e., zero-shot).
Specifically, we train KOSMOS-1 from scratch on web-scale multimodal corpora, including arbitrarily interleaved text and images, image-caption pairs, and text data.
We evaluate various settings, including zero-shot, few-shot, and multimodal chain-of-thought prompting, on a wide range of tasks without any gradient updates of finetuning.
Experimental results show that KOSMOS-1 achieves impressive performance on
1. language understanding, generation, and even **OCR-free NLP** (directly fed with document images)
2. perception-language tasks, including **multimodal dialogue, image captioning, visual question answering**
3. vision tasks, such as image recognition with descriptions (specifying **classification via text instructions**).

We also show that **MLLMs can benefit from cross-modal transfer**, i.e., transfer knowledge from language to multimodal, and from multimodal to language.
In addition, we introduce a dataset of Raven IQ test, which diagnoses the **nonverbal reasoning** capability of MLLMs.

# Key Points By AI
- From LLMs to Multimodal Large Language Model (MLLM)
- Large Language Models (LLMs) have successfully served as general purpose interface across various natural language tasks.
- There is still large performance gap between the current model and the average level of adults, KOSMOS-1 demonstrates the potential of MLLMs to perform zero-shot nonverbal reasoning by aligning perception with language models.
- Multimodal Chain-of-Thought Prompting allows large language models to generate a series of reasoning steps and decompose a multi-step problem into intermediate steps.
- We observe that providing descriptions in context can significantly improve the accuracy of image classification.

# File
[[2302.14045] Language Is Not All You Need: Aligning Perception with Language Models (arxiv.org)](https://arxiv.org/abs/2302.14045)
