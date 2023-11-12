---
title: 【DAILY READING】大模型周报丨Table-GPT、3D-GPT、AgentTuning、MusicAgent等新工作重磅来袭
date: 2023-11-05 17:43:14 +0800
categories: [paper]
tags: [daily reading]
math: true
---


# Conclusion By Myself
This is an article from [AMiner](https://www.aminer.cn/) which is the web site I usually find the paper at. I read this article which is similar to a review for lazy.
This article introduced the more important 10 papers of LLMs this (2023-10-16/22) week. As the article says, the agent model may be a hot point in recent researches.
# Papers
1. AgentTuning: Enabling Generalized Agent Abilities for LLM
	This paper gives a method of AgentTuning, which can improve the agent ability of LLMs. It constructed by a lightweight instruction-tuning dataset contains high-quality interaction trajectories. And it employed a hybrid instruction-tuning strategy by combining AgentInstruct with open-source instructions from general domains. This method is used to instruction-tune the Llama 2 series, resulting in AgentLM.
2. CodeChain: Towards Modular Code Generation Through Chain of Self-revision with Representative Sub-modules
	This is a paper [we have read before](https://washing1127.github.io/posts/CodeChain：Towards-Modular-Code-Generation-Through-Chain-of-Self-revisions-with-Representative-Sub-modules). It introduced the CodeChain framework to induce LLMs can generate more modularize code by self-revisions. They did this in two steps, 1. Use CoT to prompt the LLM to get more modularized codes; 2. Clustering these codes, and use CoT again to ask the LLMs to generate answers by its previous output.
3. In-Context Pretraining: Language Modeling Beyond Document Boundaries
	This is also a paper [we have read before](https://washing1127.github.io/posts/In-Context-Pretraining：Language-Modeling-Beyond-Document-Boundaries). It give an opinion that if we feed more related data to model, then we can significantly enhance its performance across multiple aspects.
4. Self-RAG: Learning to Retrieve, Generated, and Critique through Self-Reflection
	This enhanced the Retrieval-Augmented Generation (RAG) method by self-reflection. This method trains a single arbitrary LM that adaptively retrieves passages on-demand, and generates and reflects on retrieved passages and its own generations using special tokens, called reflection tokens. Generation reflection tokens makes the LM controllable during the inference phase, enabling it to tailor its behavior to diverse task requirements.
5. Towards Graph Foundation Models: A Survey and Beyond
	This is a survey of Graph Foundation Models (GFMs). Respect to these foundation models researcher in the LLMs age.
6. MusicAgent: An AI Agent for Music Understanding and Generation with Large Language Models
	This is also an agent model, It collected tools from diverse sources, and then use LLMs decompose user requests into multiple sub-tasks and invoke corresponding music tools.
7. 3D-GPT: Procedural 3D Modeling with Large Language Models
	I think this can also be seen as a agent model. It use LLMs to generate the instructions of 3D model procedural. More specifically, it use LLMs to decompose the 3D model procedural into some accessible segments and appointing the apt agent for each task.
8. BitNet: Scaling 1-bit Transformers for Large Language Models
	This may be a paper of a littler transformer, it introduced BitLinear as nn.Linear in transformer. This architecture can significantly reduce the memory occupy and energy usage.
9. Llemma: An Open Language Model For Mathematics
	This is a LLM of mathematics. It pre-trained the Code Llama on the dataset Proof-Pile-2.
10. Table-GPT: Table-tuned GPT for Diverse Table Tasks
	Table-GPT is a model goals to enhancing language models' ability to understand tables and perform table tasks.

# File
[大模型周报丨Table-GPT、3D-GPT、AgentTuning、MusicAgent等新工作重磅来袭 - 热点 - 科研解读 - AMiner](https://www.aminer.cn/research_report/653739c57cb68b460f549f84) 