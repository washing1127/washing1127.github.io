---
title: 【PAPER】Augmented Language Models：a Survey
date: 2023-10-29 20:15:39 +0800
categories: [paper]
tags: [daily reading]
math: true
---


# Conclusion By Myself
# Table of Contents
## Abstract
This survey reviews works in which language models (LMs) are augmented with **reasoning skills** and the **ability to use tools**.
The former is defined as decomposing a potentially complex task into simpler subtasks while the latter consists in calling external modules such as a code interpreter.
LMs can leverage these augmentations separately or in combination via heuristics, or learn to do so from demonstrations. 
While adhering to a standard missing tokens prediction objective, such augmented LMs can use various, possibly non-parametric external modules to expand their context processing ability, thus departing from the pure language modeling paradigm. 
We therefore refer to them as *Augmented Language Models (ALMs)*. 
The missing token objective allows ALMs to learn to reason, use tools, and even act, while still performing standard natural language tasks and even outperforming most regular LMs on several benchmarks. 
In this work, after reviewing current advance in ALMs, we conclude that *this new research direction has the potential to address common limitations of traditional LMs such as interpretability, consistency, and scalability issues*.
## 1 Introduction: motivation for the survey and definitions
### 1.1 Motivation
- more reading
	- [ ] Evaluating large language models trained on code | copilot
	- [ ] Neural text generation with unlikelihood training. In International Conference on Learning Representations | hallucinations
- fundamental defect of today's LLMs
	1. a single parametric model
	2. a limited context
- external things can integrate into LLMs
	1. external documents
	2. external data sources
	3. external tools
- definitions in this survey
	- Reasoning: reasoning is decomposing a potentially complex task into simpler subtasks the LM can solve more easily by itself or using tools.
	- Tool: a tool is an external module that is typically called using a rule or a special token and whose output is included in the ALM's context.
	- Act: we will sometimes denote the call of a tool by an ALM as an action, even if it does not have an external effect.

#### Why jointly discussing reasoning and tools
#### Why jointly discussing tools and actions
### 1.2 Our classification
## 2 Reasoning
### 2.1 Eliciting reasoning with prompting
elicitive prompts encourage LMs to solve tasks by following intermediate steps before predicting the output/answer.
#### Few-shot setting
- [ ] Chain of thought prompting elicits reasoning in large language models. | Chain-of-Thought
- [ ] Measuring and narrowing the compositionality gap in language models | self-ask
- [ ] Webshop: Towards scalable real-world web interaction with grounded language agents. | ReAct
#### Zero-shot setting
few-shot provides examples of the task at hand, zero-shot conditions the LM on a single prompt that is not an example.
- [ ] Large language models are zero-shot reasoners. | think step by step
### 2.2 Recursive prompting
### 2.3 Explicitly teaching language models to reason
all works also show that small scale instruction-finetuned models can perform better than un-finetuned large scale models, especially in the tasks where instruction following is important
### 2.4 Comparison and limitations of abstract reasoning
overall, reasoning can be seen as decomposing a problem into a sequence of sub-problems either iteratively or recursively.
- [ ] Hypertree proof search for neural theorem proving. | example of other reasoning structures such as trees could be considered
## 3 Using Tools and Act
The possibility to easily include tools and actions in the form of special tokens is a convenient feature of language modeling coupled with transformers.
### 3.1 Calling another model
#### Iterative LM calling
- [ ] Re3: Generating longer stories with recursive reprompting and revision. | seems interesting
- [ ] Diffusion-lm improves controllable text generation. | a model can denoising sequence of Gaussian vectors into word vectors
- [ ] Peer: A collaborative language model. | a model can call itself repeatedly
#### Leveraging other modalities
- [ ] Flamingo: a visual language model for few-shot learning.
- [ ] Socratic models: Composing zero-shot multimodal reasoning with language | a modular framework allows models exchange information with each other and acquire new multimodal capabilities without additional finetuning
### 3.2 Information retrieval
#### 3.2.1 Retrieval-augmented language models
##### Dense and sparse retrievers
both types of retrievers assess the relevance of a document to an information-seeking query. this can be done by:
	1. checking for precise term overlap, or
	2. computing the semantic similarity across related concepts.
##### Conditioning LMs on retrieved documents
##### Chain-of-thought prompting and retrievers
#### 3.2.2 Querying search engines
In general, reasoning can improve decision making by making better inferences and predictions, while the ability to use external tools can improve reasoning by gathering additional information from knowledge bases or environments
#### 3.2.3 Searching and navigating the web
- [ ] Webgpt: Browser-assisted question-answering with human feedback. | a LM-based agent, can search the internet, navigate webpages, follow links, and cite sources
### 3.3 Computing via Symbolic Modules and Code Interpreters
### 3.4 Acting on the virtual and physical world
#### Controlling Virtual Agents
#### Controlling Physical Robots
## 4 Learning to reason, use tools, and act
### 4.1 Supervision
#### Few-shot prompting
#### Fine-tuning
#### Prompt pre-training
#### Bootstrapping
### 4.2 Reinforcement learning
#### Hard-coded reward functions
#### Human feedback
- RLHFs:
	- [ ] Tamer: Training an agent manually via evaluative reinforcement.
	- [ ] Interactive learning from policy-dependent human feedback.
	- [ ] Deep reinforcement learning from human preferences.
	- [ ] Deep tamer: Interactive agent shaping in high-dimensional state spaces.
### 4.3 Limitations and future directions
## 5 Discussion
### Moving away from language modeling
### A tradeoff between memorizing and querying tools
### Generalizing the non-parametric framework
### A path towards autonomous machine intelligence
- [ ] A path towards autonomous machine intelligence | LeCnn's 
### Augmented Language Models benefits
#### Truthfulness
#### Estimating and reducing uncertainty
#### Interpretability
#### Enhanced capabilities
### Ethical concerns
# File
[[2302.07842] Augmented Language Models: a Survey (arxiv.org)](https://arxiv.org/abs/2302.07842)