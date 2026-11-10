---
title: Research Themes
date: 2026-06-04
lastmod: 2026-11-10
hide_date: true
reading_time: false
summary: Dai studies how closely an algorithm can approximate the best possible solution. She is also interested in the design and convergence of optimizers for deep learning. In social networks, her work connects the choice of seed nodes with the way groups discuss and share information.
---

Jialing Dai builds mathematical models of decision problems, derives guarantees for the algorithms that solve them, and tests both the models and the algorithms against data.

## Combinatorial Optimization and Algorithm Theory

Dai studies [polynomial-time approximation algorithms for orthant-submodular maximization]({{< relref "publications/or-2026-orthant-submodular" >}}). This work is under review at the *SIAM Journal on Computing* (SICOMP). In a [manuscript under review at ICLR 2027]({{< relref "publications/iclr-2027-refined-label-comparisons" >}}), she and her collaborators study how to compare candidate labels when maximizing a non-monotone k-submodular function under constraints.

In a model of intergroup debate, how should a few participants be chosen to introduce a message so that its net influence is as large as possible? The objective is non-submodular. She and her collaborators used submodular upper and lower bounds to obtain a data-dependent approximation guarantee. They also developed sampling algorithms for settings where different messages compete. [Study of intergroup debate]({{< relref "publications/ins-2024-intergroup-debate" >}})

## Optimization for Machine Learning

Her interests include algorithm design and convergence in stochastic and nonconvex optimization. For deep learning, she is particularly interested in how the choice of optimizer affects training stability and convergence.

## Reinforcement Learning and Agent Decision-Making

Once a few seed nodes are in place, which additional node will help a message reach the most people? Dai and her collaborators used graph neural networks to represent how nodes are connected and deep reinforcement learning to choose each new seed in light of earlier choices. They tested the learned policy against sampling methods and heuristics based on network structure, using both synthetic and real networks. [Study of group-aware seed selection]({{< relref "publications/ton-ug-dcgnn" >}})

## Network Science and Social Computing

People sometimes leave a group discussion with more extreme views than they held going in. Dai and her collaborators studied this form of polarization in real-world data and modeled how changing preferences affect the spread of opinions. [Study of group polarization]({{< relref "publications/ins-2022-polarization" >}})

She is also interested in containing rumors and tracing information to its source. For AI-generated content, she and her collaborators formulated a coverage problem to determine where to place checkpoints so that the same set works across several possible scenarios. [Study of content provenance]({{< relref "publications/aaim-2026-checkpoint-cover" >}})
