---
title: "PROMO‐Orchard: A Robust Semantic‐Enhanced Framework for Dual‐Robot Simultaneous Localization and Mapping Merging in Orchard"
weight: 110
authors:
  - "Yefeng Sun"
  - admin
  - "Liang Gong"
  - "Bishu Gao"
  - "Jinghan Cai"
  - "Yanming Li"
  - "Chengliang Liu"
author_notes:
  - ""
  - ""
  - "Corresponding author"
  - ""
  - ""
  - ""
  - ""
date: "2026-08-14T00:00:00Z"
publication_types: ["article-journal"]
publication: "Journal of Field Robotics"
publication_short: "JFR"
hugoblox:
  ids:
    doi: 10.1002/rob.70323
abstract: >-
  Agricultural robots are increasingly used to improve orchard productivity and reduce labor dependence, yet collaborative orchard mapping remains difficult because dense canopy degrades GNSS reliability, repetitive row geometry induces structural aliasing, and long-duration operation over large orchard blocks causes mergeable overlap to emerge only after extended traversal, thereby destabilizing generic registration pipelines. In this work, we formulate orchard map merging as an operation-time progressive submap association and registration problem for a dual-robot field setting and propose PROMO-Orchard, an orchard-aware semantic map-merging framework. The framework integrates four tightly coupled components: class-dependent voxelization with persistent orchard-prior extraction, Orchard-AKS for operation-aware submap scheduling, Sem-OREOS for semantic-enhanced overlap retrieval and merge triggering, and Sem-GICP for class-weighted semantic refinement with orchard structural regularization. Together, these components turn semantic map merging into an operation-time, orchard-aware process rather than a generic post-hoc registration step. Field experiments in three representative orchard settings, namely I-Tunnel, U-Tunnel, and Long-Duration, show that the proposed method consistently suppresses row aliasing and maintains semantically coherent shared maps under in-row overlap, headland U-turning, and delayed-overlap operation. Compared with Segregator and a semantic-ablation variant, the proposed framework reduces ICP error by 78–94% while maintaining FPMR above 91% across all scenarios, and achieves clear improvements in semantic fidelity, boundary continuity, and structural consistency. These results support the conclusion that reliable orchard map merging requires not only semantic cues, but their structured integration with orchard-specific priors, thereby providing a practical basis for collaborative orchard mapping and downstream robotic operations such as navigation, canopy management, harvesting, and logistics. While the present study experimentally validates the dual-robot case, the proposed progressive pairwise merging formulation provides the system-level basis for future extension to larger multi-robot orchard teams.
tags: []
featured: false
links:
  - type: custom
    label: "Full Text"
    url: "https://onlinelibrary.wiley.com/doi/full/10.1002/rob.70323"
    icon: hero/document-text
draft: false
---

**Article type:** Research Article.
