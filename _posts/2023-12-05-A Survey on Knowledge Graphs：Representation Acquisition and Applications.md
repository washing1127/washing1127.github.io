---
title: 【DAILY READING】A Survey on Knowledge Graphs: Representation Acquisition and Applications
date: 2023-12-05 20:17:54 +0800
categories: [paper]
tags: [daily reading]
math: true
mermaid: true
---

# Overview
This paper introduces a comprehensive review of **knowledge graph**. There are four topics about KG, 1) *knowledge graph representation learning*, 2) *knowledge acquisition and completion*, 3) *temporal knowledge graph*, and 4) *knowledge-aware applications*.
# Knowledge-graph Representation Learning (KRL)
This is also known as *Knowledge Graph Embedding (KGE)*, there are four parts of it:
## Representation Space
The key issue of representation learning is to learn low-dimensional distributed embedding of entities and relations.
The embedding space should follow three conditions, i.e., differentiability, calculation possibility, and definability of a scoring function. There are several kinds of space following:
- Point-Wise Space
- Complex Vector Space
- Gaussian Distribution
- Manifold and Group

## Scoring Function
The scoring function is used to measure the plausibility of facts, also referred to as the energy function in the energy-based learning framework.
Energy-based learning aims to learn the energy function $\mathcal{E}_\theta(x)$ (parameterized by $\theta$ taking $x$ as input) and to make sure positive samples have higher scores than negative samples.
There are two typical types of scoring functions:
- distance-based
- similarity-based

## Encoding Models
There are several models that encode the interactions of entities and relations through specific model architectures, including:
- Linera/Bilinear Models
	Linear models formulate relations as a linear/bilinear mapping by projectiong head entities into a representation space close to tail entities.
- Factorization Models
	Factorization aims to decompose relational data into low-rank matrices for representation learning.
- Neural Networks
	Neural networks encode relational data with non-linear neural activation and more complex network structures by matching semantic similarity of entities and relations.
	Neural Networks Models include CNNs, RNNs, Transformers, and GNNs (Graph Neural Networks).

## Embedding with Auxiliary Information
Multi-modal embedding incorporates external information such as text descriptions, type constraints, relational paths, and visual information, with a knowledge graph itself to facilitate more effective knowledge representation.
## Summary
Developing a novel KRL model is to answer the following four questions:
1. which representation space to choose;
2. how to measure the plausibility of triplets in a specific space;
3. which encoding model to use for modeling relational interactions;
4. whether to utilize auxiliary information.

The most popularly used representation space is Euclidean point-based space by embedding entities in vector space and modeling interactions via vector, matrix, or tensor.
Other representation spaces, including complex vector space, Gaussian distribution, and manifold space and group, are also studied.
Manifold space has an advantage over pointwise Euclidean space by relaxing the point-wise embedding.
# Knowledge Acquisition
Knowledge acquisition aims to construct knowledge graphs from unstructured text and other structured or semi-structured sources, complete an existing knowledge graph, and discover and recognize entities and relations. There are three parts of it:
## Knowledge Graph Completion
Because of the nature of incompleteness of knowledge graphs, KGC is developed to add new triples to a knowledge graph.
Typical subtasks include link prediction, entity prediction, and relation prediction.
The steps of KGC are:
- Embedding-based Models
- Relation Path Reasoning
- RL-based Path Finding
- Rule-based Reasoning
- Meta Relational Learning
- Triple Classification

## Entity Discovery
Entity-based knowledge qcquisition can be distinguished into several fractionized tasks:
- Entity Recognition
- Entity Typing
- Entity Disambiguation
- Entity Alignment

## Relation Extraction
Relation extraction is a key task to build large-scale knowledge graphs automatically by extracting unknown relational facts from plain text and adding them into knowledge graphs. It include:
- Neural Relation Extraction
- Atteention Mechanism
- Graph Convolutional Networks
- Adverserial Training
- Reinforcement Learning
- Joint Entity and Relation Extraction

## Summary
Knowledge graph completion completes missing links between existing entities or infers entities given entity and relation queries.
Entity discovery acquires entity-oriented knowledge from text and fuses knowledge between knowledge graphs.
Relation extraction suffers from noisy patterns under the assumption of distant supervision, especially in text corpus of different domains.
# Temporal Knowledge Graph
The temporal information is of great importance because the structured knowledge only holds within a specific period, and the evolution of facts follows a time sequence. It includes four parts:
## Temporal Information Embedding
Temporal information is considered in temporal-aware embedding by extending triples into temporal quadruple as $(h,r,t,\tau)$, where $\tau$ provides additional temporal information about when the fact held.
## Entity Dynamics
To improve temporal scope inference, the contextual temporal profile model formulates the temporal scoping problem as state change detection and utilizes the context to learn state and state change vectors.
## Temporal Relational Dependency
There exists temporal dependencies in relational chains following the timeline, for example, *wasBornIn -> graduateFrom -> workAt -> diedIn*. There is a kind of time-aware embedding, a joint learning framework with temporal regularization, to incorporate temporal order and consistency information.
## Temporal Logical Reasoning
Logical rules are also studied for temporal reasoning. Markov logic network and probabilistic soft logic can be used for reasoning over uncertain temporal knowledge graphs.
Temporal close-path rules and learns the structure of rules from the knowledge graph stream for reasoning are also considered.
# Knowledge-aware Applications
Rich structured knowledge can be useful for AI applications.
The application of knowledge graphs includes two folds:
1. In-KG applications
	such as link prediction and named entity recognition;
2. Out-of-KG applications
	including relation extraction and more downstream knowledge-aware applications such as question answering and recommendation systems.

## Language Representation Learning
Language representation learning via self-supervised language model pretraining has become an integral component of many NLP systems.
Troditional language modeling does not exploit factual knowledge with eitieies frequently observed in the text corpus.
## Question Answering
Knowledge-graph-based question answering (KG-QA) answers natural language questions with facts from knowledge graphs.
Neural network-based approaches represent questions and answers in distributed semantic space, and some also conduct symbolic knowledge injection for commonsense reasoning.
## Recommender Systems
Integrating knowledge graphs as external information enables recommendation systems to have the ability of commonsense reasoning, with the potential to solve the sparsity issue and the cold start problem.
# Future Directions
Future directions are focus on these parts:
## Complex Reasoning
Numerical computing for knowledge representation and reasoning requires a continuous vector space to capture the semantic of entities and relations.
While embedding-based methods have a limitation on complex logical reasoning, two directions on the relational path and symbolic logic are worthy of being further explored.
## Unified Framework
Several representation learning models on knowledge graphs have been verifed as equivalence.
A unified understanding of knowledge representation and reasoning is less explored. An investigation towards unification in a way similar to the unified framework of graph networks, however, will be worthy of bridging the research gap.
## Interpretability
Interpretability of knowledge representation and injection is a vital issue for knowledge acquisition and real-world applications.
Preliminary efforts have been made for interpretability.
## Scalability
Scalability is crucial in large-scale knowledge graphs. There is a trade-off between computational efficiency and model expressiveness, with a limited number of works applied to more than 1 million entities.
Several embedding methods use simplification to reduce the computation cost, such as simplifying tensor products with circular correlation operation.
## Knowledge Aggregation
The aggregation of global knowledge is the core of knowledge-aware applications. For example, recommendation systems use a knowledge graph to model user-item interaction and text classification jointly to encode text and knowledge graph into a semantic space.
Most current knowledge aggregation methods design neural architectures such as attention mechanisms and GNNs.
## Automatic Construction and Dynamics
Current knowledge graphs rely highly on manual construction, which is labor-intensive and expensive. The widespread  applications of knowledge graphs on different cognitive intelligence fields require automatic knowledge graph construction  from large-scale unstructured content. 
Recent research mainly  works on semi-automatic construction under the supervision  of existing knowledge graphs. Facing the multimodality, heterogeneity, and large-scale application, automatic construction  is still of great challenge.