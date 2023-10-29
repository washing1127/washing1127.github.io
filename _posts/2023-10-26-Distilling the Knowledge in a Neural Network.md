---
title: 【DAILY READING】Distilling the Knowledge in a Neural Network
date: 2023-10-29 20:15:01 +0800
categories: [paper]
tags: [daily reading]
math: true
---


# Conclusion By Myself
This paper introduced that it is helpful to train a little model with a big model. 
The specific method is train a big model with a lot of data and make it performance good. Then, we can train a little model with the same data but with an additional task that is beside the little model need to predict the real target of the features, and it also need to predict the *"soft target"* which is produced by the big model. More details, the soft target is the class probabilities produced by the big model.
# Abstract
A very simple way to improve the performance of almost any machine learning algorithm is to train many different models on the same data and then average their predictions.
Unfortunately, making predictions using a whole ensemble of models is cumbersome and may be too computationally expensive to allow deployment to a large number of users, especially if the individual models are large neural nets.
Caruana and his collaborators have shown that it is possible to compress the knowledge in an ensemble into a single model which is much easier to deploy and we develop this approach further using a different compression technique.
We achieve some surprising results on MNIST and we show that we can significantly improve the acoustic model of a heavily used commercial system by distilling the knowledge in an ensemble of models into a single model.
We also introduce a new type of ensemble composed of one or more full models and many specialist models which learn to distinguish fine-grained classes that the full models confuse.
Unlike a mixture of experts, these specialist models can be trained rapidly and in parallel.
# Key Points By AI
- Many insects have a larval form that is optimized for extracting energy and nutrients from the environment and a completely different adult form that is optimized for the very different requirements of traveling and reproduction
- We have found that using the original training set works well, especially if we add a small term to the objective function that encourages the small model to predict the true targets as well as matching the soft targets provided by the cumbersome model
- The Deep Neural Network produces a probability distribution over clusters of tri-phone states at each time and a decoder finds a path through the Hidden Markov Model states that is the best compromise between using high probability states and producing a transcription that is probable under the language model
- The ensemble gives a small improvement on the ultimate objective of Word Error Rate due to the mismatch in the objective function, bug again, the improvement in WER achieved by the ensemble is transferred to the distilled model
- For a deep acoustic model that is version of the one used by Android voice search, we have shown that nearly all of the improvement that is achieved by training an ensemble of deep neural nets can be distilled into a single neural net of the same size which is far easier to deploy
- For really big neural networks, it can be infeasible even to train a full ensemble, but we have shown that the performance of a single really big net that has been trained for a very long time can be significantly improved by learning a large number of specialist nets, each of which learns to discriminate between the classes in highly confusable cluster
# File
[[1503.02531] Distilling the Knowledge in a Neural Network (arxiv.org)](https://arxiv.org/abs/1503.02531) 