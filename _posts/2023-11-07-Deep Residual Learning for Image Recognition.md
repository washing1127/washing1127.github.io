---
title: 【DAILY READING】Deep Residual Learning for Image Recognition
date: 2023-11-12 20:17:54 +0800
categories: [paper]
tags: [daily reading]
math: true
mermaid: true
---


# Abstraction
Deeper neural networks are more difficult to train. We present a residual learning framework to ease the training of networks that are substantially deeper than those used previously.
We explicitly reformulate the layers as learning residual functions with reference to the layer inputs, instead of learning unreferenced functions.
We provide comprehensive empirical evidence showing that these residual networks are easier to optimize, and can gain accuracy from considerably increased depth. 
On the ImageNet dataset we evaluate residual nets with a depth of up to 152 layers---8x deeper than VGG nets but still having lower complexity. 
An ensemble of these residual nets achieves 3.57% error on the ImageNet test set. 
This result won the 1st place on the ILSVRC 2015 classification task. We also present analysis on CIFAR-10 with 100 and 1000 layers.  
The depth of representations is of central importance for many visual recognition tasks.
Solely due to our extremely deep representations, we obtain a 28% relative improvement on the COCO object detection dataset. 
Deep residual nets are foundations of our submissions to ILSVRC & COCO 2015 competitions, where we also won the 1st places on the tasks of ImageNet detection, ImageNet localization, COCO detection, and COCO segmentation.
# Questions Before Read
## 1. Why it Works
If one hypothesizes that multiple nonlinear layers can asymptotically approximate complicated functions, then it is equivalent to hypothesize that they can asymptotically approximate the residual function, i.e., $\mathcal H(x)-x$. 
## 2. How the Back Propagation Works
The BP is same as the normal Networks.
# Conclusion By Myself
Theoretically, deeper a Network is, better performance it will have. Because when it is necessary, the added layers will be *identity mapping* layers ($f(x)=x$).
But there are evidences show that when a network be extremely deep, it will become worse than a shallow form. This is not caused by overfitting, because the training errors are higher too.
This paper introduced a *Residual Networks (ResNets)* to prevent this problem.
Traditional Networks are form in $y=\sigma(\mathcal H(x))$, where $\mathcal H(x)$ are several Networks layers, i.e., $W^{h2}(W^{h1}(x))$. This is indeed a value changed $x$. So, there is a function $\mathcal F(x) = \mathcal H(x) - x$ called the residual of $\mathcal H(x)$. Then we can present $\mathcal H(x)$ as $\mathcal F(x) + x$.
This method are 1) easy to implement, 2) little parameters when deep, 3) easy for optimize, and 4) can reduce a good performance.
1) is because it just add some *shortcut connections* into the networks, these connections add either extra parameter nor computational complexity.
2) is because the *Bottleneck Architectures*. It use a 3 layers of ($1\times 1$, $3\times3$ and $1\times1$) instead of 2 ($3\times3$, $3\times3$).
3) is because the residual connection makes the gradients more distinctness.
4) is because it changes the target to optimize from $\mathcal H(x)$ to $\mathcal F(x)$. This can lead the model walk out of the early satisfy of gradient.

There are three options of shortcuts, (A) identity, and zero-padding when dimensions increasing; (B) identity, and projection when dimensions increasing; (C) all are projections. Where the performance of B is little better than A, and C is marginal better than B. So this paper choose A for research mainly.
ResNets can make the deep networks have a enough learn, but can also lead to a overfitting when it is very very deep.
# File
[[1512.03385] Deep Residual Learning for Image Recognition (arxiv.org)](https://arxiv.org/abs/1512.03385) 