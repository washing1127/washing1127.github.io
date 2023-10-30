---
title: 【DAILY READING】Deep Reinforcement Learning from Human Preferences
date: 2023-10-30 18:11:04 +0800
categories: [paper]
tags: [daily reading]
math: true
---


# Conclusion By Myself
This is a paper included in the class of RLHF. 
This paper published in 2017, it introduced a method of RL which is give two actions to a common human(non-expert), and then ask this human for prefer one.
This method makes the feedback from human be easier, so the training of the complex model becomes easier too.
Specifically, this paper desires to solve the follow problems:
1. enable us to solve tasks for which we can only recognize the desired behavior, but no necessarily demonstrate it
2. allows agents to be taught by non-expert users
3. scales to large problems
4. be economical with user feedback

# Abstract
For sophisticated reinforcement learning (RL) systems to interact usefully with real-world environments, we need to communicate complex goals to these systems. 
In this work, we explore goals defined in terms of (non-expert) human preferences between pairs of trajectory segments.
We show that this approach can effectively solve complex RL tasks without access to the reward function, including Atari games and simulated robot locomotion, while providing feedback on less than 1% of our agent's interactions with the environment.
This reduces the cost of human oversight far enough that it can be practically applied to SOTA RL systems.
To demonstrate the flexibility of our approach, we show that we can successfully train complex novel behaviors with about an hour of human time.
These behaviors and environments are considerably more complex than any which have been previously learned from human feedback.
# Key Points By AI
- Recent success in scaling reinforcement learning (RL) to large problems has been driven in domains that have a well-specified reward function
- The agent learns about the goal of the task only by asking a human which of two trajectory segments is better
- Feedback is provided by contractors who are given a 1-2 sentence description of each task before being asked to compare several hundred to several thousand pairs of trajectory segments for that task
- There is a large literature of preference elicitation and RL from unknown reward functions, we provide the first evidence that these techniques can be economically scaled up to SOTA RL systems
- Future work may be able to improve the efficiency of learning from human preferences, and expand the range of tasks to which it can be applied
- In the long run it would be desirable to make learning a task from human preferences no more difficult than learning it from a programmatic reward signal, ensuring that powerful RL systems can be applied in the service of complex human values rather than low-complexity goals

# File
[[1706.03741] Deep reinforcement learning from human preferences (arxiv.org)](https://arxiv.org/abs/1706.03741) 