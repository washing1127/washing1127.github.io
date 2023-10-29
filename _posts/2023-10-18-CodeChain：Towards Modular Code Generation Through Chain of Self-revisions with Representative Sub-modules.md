---
title: 【PAPER】CodeChain：Towards Modular Code Generation Through Chain of Self-revisions with Representative Sub-modules
date: 2023-10-29 20:15:49 +0800
categories: [paper]
tags: [daily reading]
math: true
---


# Conclusion By Myself
LLMs lack of the ability to write modularized code to solve complex task. This paper introduced a way of inference to solve this problem.
Concretely in two step:
1. Use "chain-of-thought(CoT)" to prompt the LLM to get more modularized codes.
2. Self-revisions by two inner step:
	1. Clustering these code.
	2. Use CoT prompt again and ask the llm to generate answer by its previous output.
# Abstract
Large Language Models (LLMs) have already become quite proficient at solving simpler programming tasks like those in HumanEval or MBPP benchmarks.
However, solving more complex and competitive programming tasks is still quite challenging for these models - possible due to their tendency to generate solutions as monolithic code blocks instead of decomposing them into logical sub-tasks and sub-modules. On the other hand, experienced programmers instinctively write modularized code with abstraction for solving complex tasks, often reusing previously developed modules.
To address this gap, we propose CodeChain, a novel framework for **inference** that elicits modularized code generation through a **chain of self-revisions**, each being guided by some representative sub-modules generated in previous iterations.
Concretely, CodeChain first instructs the LLM to generate modularized codes through **chain-of-thought prompting**. Then it applies a chain of self-revisions by iterating the two steps:
	- **extracting and clustering** the generated sub-modules and selecting the cluster representatives as the more generic and re-usable implementations
	- **augmenting the original chain-of-thought prompt** with these selected module-implementations and instructing the LLM to re-generate new modularized solutions.
We find that by naturally encouraging the LLM to reuse the previously developed and verified sub-modules, CodeChain can significantly boost both modularity as well as correctness of the generated solutions, achieving relative pass@1 improvements of 35% on APPS and 76% on CodeContents.
It is shown to be effective on both OpenAI LLMs as well as open-sourced LLMs like WizardCoder. We also conduct comprehensive ablation studies with different methods of prompting, number of clusters, model sizes, program qualities, etc., to provide useful insights that underpin CodeChain's success.
# Key Points By AI
1. The long-term goal of artificial intelligence is to develop executable and functionally correct computer programs to solve complex problems.
2. Large pre-trained language models (LLMs) have made unprecedented progress in recent years and have expanded to learning large-scale code data.
3. Current state-of-the-art models cannot compare with skilled developers in highly complex programming tasks because their generation methods are too simple.
4. Most methods using LLMs adopt a simple generation approach, where the model usually generates code solutions as a single overall code block.
5. Another limitation is that the model generates a large number of solutions independently, hoping that one of them will pass all private test cases.
6. Recent research has proposed a method of subsampling output, providing the model with problem descriptions and public test cases as input.
7. Experienced developers will try to modify and reuse code developed previously until they are satisfied.
8. Some recent works have addressed this issue, for example, using LLM for self-correction, improving generated solutions through feedback such as compiler error messages, test results, and natural language explanations.
9. These methods only use independent feedback from each solution, ignoring the potential collective insights of all generated samples or their subcomponents.
10. Inspired by the problem-solving process, we propose CodeChain, a novel reasoning framework to improve code generation in LLMs through a chain of self-correcting submodules.
11. In CodeChain, we first introduce chain-of-thought prompts to indicate that the LLM should decompose solutions into modular paragraphs, each representing an abstract function for advanced logical subtasks.
12. To exploit modularity in the program, we further improve the generation process through a series of self-corrections, each based on a set of sampled submodules.
13. We first extract the submodules found in the generated program and group them into clusters, where we sample the central submodules and treat them as reusable code parts for self-correction.
14. Then, we expand the original chain-of-thought prompts through these selected submodules and instruct the LLM to generate new modular solutions.
15. In this way, the LLM can gain collective insights from the modular components of all past generated samples to improve its future generations, imitating the problem-solving process of experienced developers.
16. Experimental results show that CodeChain can significantly improve the performance of LLMs and achieve state-of-the-art performance on challenging code tasks in APPS and CodeContests.
17. CodeChain has improved the average pass@1 performance on APPS by over 35%, and on CodeContests by over 76%. We have also observed continuous improvements for both OpenAI LLM and open-source LLMs (such as WizardCoder).
18. We have also conducted comprehensive ablation studies, including analyzing single-step and multi-step revisions, feedback types, and cluster numbers, to gain useful insights into success of CodeChain.
19. Our work is closely related to the research of large-scale Transformer-based language models (LLMs).
20. Originally designed for natural language processing, these models have been expanded to learn large-scale code data and are skilled at understanding the context of programming languages and generating outputs.
21. More directly related is recent work aimed at improving code generation quality through output feedback, which introduced a simple filtering method by only selecting output samples that passed public test cases.
22. Some related work aims to improve generation quality through iterative self-revision, which uses the test results of public test cases as feedback for the model to revise its code.
# File
[[2310.08992] CodeChain: Towards Modular Code Generation Through Chain of Self-revisions with Representative Sub-modules (arxiv.org)](https://arxiv.org/abs/2310.08992)
