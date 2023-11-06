---
title: 【DAILY READING】GPT-Fathom：Benchmarking Large Language Models to Decipher the Evolutionary Path towards GPT-4 And Beyond
date: 2023-11-06 00:03:07 +0800
categories: [paper]
tags: [daily reading]
math: true
---


# Conclusion By Myself
This is a paper from ByteDance, it presented an open-source and reproducible evaluation suite for LLMs named GPT-Fathom.
# Abstract
With the rapid advancement of LLMs, there is a pressing need for a comprehensive evaluation suite to assess their capabilities and limitations.
Existing LLM leaderboards often reference scores reported in other papers without consistent settings and prompts, which may inadvertently encourage cherry-picking favored settings and prompts for better results.
In this work, we introduce GPT-Fathom, an open-source and reproducible LLM evaluation suite built on top of OpenAI Evals.
We systematically evaluate 10+ leading LLMs as well as OpenAI's legacy models on 20+ curated benchmarks across 7 capability categories, all under aligned settings.
Our retrospective study on OpenAI's earlier models offers valuable insights into the evolutionary path from GPT-3 to GPT-4.
Currently, the community is eager to know how GPT-3 progressively improves to GPT-4, including technical details like whether adding code data improves LLM's reasoning capability, which aspects of LLM capability can be improved by SFT and RLHF, how much is the alignment tax, etc.
Our analysis sheds light on many of these questions, aiming to improve the transparency of advanced LLMs.