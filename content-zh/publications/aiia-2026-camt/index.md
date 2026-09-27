---
title: "CaMT: Class-aware Multi-level Training Distillation for Lightweight Semantic Segmentation in Apple Orchard"
weight: 70
authors:
  - "Yefeng Sun"
  - admin
  - "Liang Gong"
  - "Bishu Gao"
  - "Gengjie Lin"
  - "Jiayu Chen"
  - "Yanming Li"
  - "Chengliang Liu"
author_notes:
  - ""
  - ""
  - "通讯作者"
  - ""
  - ""
  - ""
  - ""
  - ""
publication_types: ["article-journal"]
publication: "Artificial Intelligence in Agriculture"
publication_short: "AIIA"
date: "2026-08-20T00:00:00Z"
hugoblox:
  ids:
    doi: 10.1016/j.aiia.2026.08.001
abstract: >-
  Accurate semantic understanding of orchard environments is essential for enabling agricultural robots to perform navigation, monitoring, and autonomous operations under limited onboard computation. However, lightweight semantic segmentation models often suffer from severe performance degradation in apple orchards due to class imbalance, repetitive tree-row structures, thin objects, strong illumination variations, occlusions, and visually similar categories. To address these challenges, we propose CaMT, a Class-aware Multi-level Training Distillation framework for lightweight semantic segmentation in apple orchards. CaMT transfers structured knowledge from a high-capacity teacher to lightweight student models through four complementary components: reliable hard-region class-balanced logit distillation, reliable hard-region guided multi-level feature distillation, cross-class prototype-relation distillation, and teacher-guided boundary distillation. To quantitatively evaluate the proposed method, we construct a finely annotated apple orchard dataset covering spring and autumn, two typical operational seasons, and conduct experiments on four different lightweight student models. Experiments on four lightweight student architectures demonstrate that CaMT consistently outperforms standard supervised training, MDKD, and Zhao et al. On average, CaMT improves mean Intersection over Union by 3.47 percentage points over the non-distilled baseline, 2.65 percentage points over MDKD, and 2.24 percentage points over Zhao et al., while introducing no additional inference-time parameters or FLOPs. Additional ablation, condition-wise, failure-case, and deployment-efficiency analyses further examine the component necessity, environmental adaptability, limitations, and practical deployment potential of CaMT. These results show that CaMT provides an effective training strategy with deployment potential for lightweight orchard semantic segmentation under resource-constrained agricultural robotic perception settings.
tags: []
featured: false
links:
  - type: custom
    label: "出版商全文"
    url: "https://www.sciencedirect.com/science/article/pii/S2589721726000863"
    icon: hero/document-text
projects: []
slides: ""
draft: false
---
