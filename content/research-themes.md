---
title: Research Themes
date: 2026-06-04
lastmod: 2026-11-10
summary: How good is an algorithm’s solution when the optimum is hard to compute? How do stochastic gradients affect training? In a network, how do interactions between groups change which node an agent should select next?
---

Jialing Dai translates practical questions into objectives and constraints, analyzes the guarantees an algorithm can offer, and uses data to test model assumptions and algorithm performance.

## Combinatorial Optimization and Algorithm Theory

Which discrete optimization problems admit efficient approximations under a budget constraint? In her work on intergroup debate, the objective of maximizing net influence is non-submodular. She and her collaborators bounded it above and below with submodular functions and used sampling to obtain a data-dependent approximation guarantee. She also studies what guarantees are possible when each decision involves a choice among several labels. [Paper on intergroup debate]({{< relref "publications/ins-2024-intergroup-debate" >}})

## Optimization for Machine Learning

She is interested in nonconvex optimization when training deep networks. When gradients are estimated from small batches of examples, how does the resulting noise affect training stability and convergence speed for different optimizers?

## Reinforcement Learning and Agent Decision-Making

When choosing seed nodes one at a time, the value of the next node depends on those already selected. She and her collaborators used graph neural networks to represent the network and deep reinforcement learning to train a selection policy. They compared the learned policy with sampling algorithms and structural heuristics on both synthetic and real networks. [Paper on group-aware seed selection]({{< relref "publications/ton-ug-dcgnn" >}})

## Network Science and Social Computing

How do group discussions change individual preferences and, in turn, the spread of opinions? She and her collaborators studied group polarization in real-world data and incorporated changes in preferences into a diffusion model. Her interests also include rumor containment and information provenance. In work on tracing AI-generated content, she and her collaborators modeled checkpoint selection as a coverage problem across multiple scenarios. [Paper on group polarization]({{< relref "publications/ins-2022-polarization" >}}) · [Paper on content provenance]({{< relref "publications/aaim-2026-checkpoint-cover" >}})
