---
title: 【DAILY READING】iTransformer：Inverted Transformer Are Effective for Time Series Forecasting
date: 2023-10-29 20:15:17 +0800
categories: [paper]
tags: [daily reading]
math: true
---


# Conclusion By Myself
Honestly, this paper is not so clear to me. So I came back to this article [Transformer王者归来！](https://mp.weixin.qq.com/s/74AXbvgtpgtlCbqeM1GRgg) where introduced the paper to me.
This is a specific aspect of transformer on time series, or we can say it is a model for future forecasting. This paper is purpose to deal with the problem of linear forecasting models are overtaking the transformer architecture models. 
It gives an opinion that the transformers now is underdeveloped, and it introduces a iTransformer model which is simply inverting the duties of the attentions mechanism and the feed-forward network.
More detailed, it changes the representations on layer-normal, feed-forward, and attention. But it is not able to be understood for me now. OK, it is still too naive for me on AI. Let's read more, study more.
# Abstract
The recent boom of linear forecasting models questions the ongoing passion for architectural modifications of Transformer-based forecasters.
These forecasters leverage Transformers to model the global dependencies over temporal tokens of time series, with each formed by multiple variates of the same timestamp.
However, Transformer is challenged in forecasting series with large lookback windows due to performance degradation and computation explosion.
Besides, the unified embedding for each temporal token fuses multiple variates with potentially unaligned timestamps and distinct physical measurements, which may fail in learning variate-centric representations and result in meaningless attention maps.
In this work, we reflect on the competent duties of Transformer components and repurpose the Transformer architecture without any adaptation on the basic components.
We propose iTransformer that simply **inverts the duties of the attention mechanism and the feed-forward network**.
Specifically, the time points of individual series are embedded into variate tokens which are utilized by the attention mechanism to capture multivariate correlations; meanwhile, the feed-forward is applied for each variate token to learn nonlinear representations.
The iTransformer model achieves consistent state-of-the-art on several real-world datasets, which further empowers the Transformer family with promoted performance, generalization ability across different variates, and better utilization of **arbitrary lookback windows**, making it a nice alternative as the fundamental backbone of time series forecasting.
# File
[[2310.06625] iTransformer: Inverted Transformers Are Effective for Time Series Forecasting (arxiv.org)](https://arxiv.org/abs/2310.06625) 