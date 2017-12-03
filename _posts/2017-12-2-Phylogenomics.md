---
layout: post
title: Phylogenomics
---

Phylogenetics is the study of the evolutionary history and relationships among organisms.

Two Phylogeny Problems :
#### Small Phylogeny Problems :

**Given**:
- a set of characters at the leaves (extant species)
- a set of states for each character
- the cost of transition from each state to every other, and the topology of the phylogenetic tree.

**Find**: A labeling for each internal node that minimizes the overall
cost of transitions.

Three methods to solve as below
  - [Fitch's Algorithm](https://swetakum.github.io/Fitch's-Algortihm/)
  - Sankoff's Algorithm
  - Maximum Likelihood

#### Large Phylogeny Problems

**Given**:
- a set of characters at the leaves (extant species)
- a set of states for each character
- the cost of transition from each state to every other

**Find**: A tree topology and labeling for each internal node that
minimizes the overall cost (over all trees and internal states)
