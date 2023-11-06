---
title: 【DAILY READING】CodeFusion：A Pre-trained Diffusion Model for Code Generation
date: 2023-11-05 17:44:58 +0800
categories: [paper]
tags: [daily reading]
math: true
---


# Conclusion By Myself
This paper introduces CodeFusion, which is a pre-trained diffusion model for code generation. It combines an encoder-decoder architecture with a diffusion process.
In more detail, there are three parts in it. Encoder (E), Denoiser (N) and Decoder (D).
A sentence is fed to encoder, and it will be mapped into continuous representation, then this representation will be used by the diffusion models as an additional condition for denoising random Gaussian noise input. Next, the denoised embeddings will be fed into a transformer decoder to obtain probability distributions over code tokens. Finally, the token will be mapped into code by a fully connected layer.
# Abstract
Imagine a developer who can only change their last line of code -- how often would they have to start writing a function from scratch before it is correct? 
Auto-regressive models for code generation from natural language have a similar limitation: they do not easily allow reconsidering earlier tokens generated.
We introduce CODEFUSION, a pre-trained diffusion code generation model that address this limitation by iteratively denoising a complete program conditioned on the encoded natural language.
We evaluate CODEFUSION on the task of natural language to code generation for Bash, Python and Microsoft Excel condition formatting (CF) rules.
Experiments show that CODEFUSION (75M parameters) performs on par with SOTA auto-regressive systems (350M-175B parameters) in top-1 accuracy and outperforms them in top-3 and top-5 accuracy, due to its better balance in diversity versus quality.
# Architecture
![image.png](https://washing-pic-1302390349.cos.ap-beijing.myqcloud.com/obsidian/pic/202311051741572.png?imageSlim)
# File
[[2310.17680] CodeFusion: A Pre-trained Diffusion Model for Code Generation (arxiv.org)](https://arxiv.org/abs/2310.17680) 