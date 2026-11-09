---
title: "Unified Group-Aware Influence Maximization with Generalized Deep Reinforcement Learning"
weight: 10
authors:
  - admin
  - "Yisheng Zhou"
  - "Yefeng Sun"
  - "Jianming Zhu"
  - "Weili Wu"
publication_types: ["article-journal"]
publication: "IEEE Transactions on Networking"
publication_short: "T-ON"
citation_details: "34, 6198–6213"
venue_metrics:
  - label: "CCF A 类（2026）"
    url: "https://kyc.lsu.edu.cn/_upload/article/files/20/77/2cbaa3754eb9aff9ed74cafed8ff/23a8de02-594c-445f-b084-69b0193c05b3.pdf#page=10"
date: "2026-07-13T00:00:00Z"
abstract: >-
  Influence maximization seeks a small seed set that maximizes the expected size of the diffusion cascade. Prior approaches perform well under standard independent-cascade and linear-threshold diffusion models but often ignore group structure and group interactions observed in real networks. This work introduces the Unified Group-aware Influence Propagation (UGIP) model, a generalized formulation that captures diverse group effects—such as echo-chamber bias and homophily—through a compact set of control parameters Θ, recovering both classical and group-aware diffusion behaviors as special cases. Under the UGIP model, we formalize the Group-aware Influence Maximization problem: given a network and Θ, select a budgeted seed set to maximize the expected spread ΣΘ(S). To address this problem, we propose the Unified Group-aware Double Deep Q-Network with Coupled Graph Neural Networks algorithm, an end-to-end deep reinforcement learning algorithm that learns seed-selection policies for Θ-parameterized UGIP instantiations and avoids Monte Carlo simulation during inference. Experiments on synthetic and real networks with overlapping communities show consistent gains over the group-agnostic learning baseline and competitive and often superior spread against reverse-influence-sampling methods and structural heuristics, with the clearest improvements in strong-community regimes and comparable selection time. Collectively, the UGIP model and the end-to-end learning algorithm constitute a ready-to-use solver for a broad spectrum of group-aware diffusion behaviors parameterized by Θ, delivering practical accuracy–efficiency trade-offs at inference without Monte Carlo simulation.
summary: "这项研究把回声室效应、同质性等群体现象纳入同一传播模型，并结合图神经网络和深度强化学习训练种子节点选择策略。训练好的策略在选点时无需运行蒙特卡洛模拟。"
hugoblox:
  ids:
    doi: 10.1109/TON.2026.3711960
featured: true
links:
  - type: custom
    label: "出版商全文"
    url: "https://ieeexplore.ieee.org/document/11603860"
    icon: hero/document-text
draft: false
---

{{< publication-details >}}
