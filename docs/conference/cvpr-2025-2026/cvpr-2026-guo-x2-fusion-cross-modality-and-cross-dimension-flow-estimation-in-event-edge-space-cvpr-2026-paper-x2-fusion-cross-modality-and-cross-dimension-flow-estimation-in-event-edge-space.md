---
title: "x^2-Fusion: Cross-Modality and Cross-Dimension Flow Estimation in Event Edge Space"
title_zh: x^2-Fusion：事件边缘空间中的跨模态与跨维度光流估计
authors: "Guo, Ruishan, Ruan, Ciyu, Wang, Haoyang, Gong, Zihang, Xu, Jingao, Chen, Xinlei"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Guo_x2-Fusion_Cross-Modality_and_Cross-Dimension_Flow_Estimation_in_Event_Edge_Space_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 5.0
evidence: 统一潜在空间解决跨传感器失配并融合多模态
tldr: 现有多模态光流方法多在异构特征空间各自为政，缺乏共享潜在空间导致跨传感器失配未解且融合复杂。本文提出x^2-Fusion，将事件相机提供的时空边缘信号视为内在边缘场作为统一潜在表示的锚点，把多模态融合重构为表示统一问题。该方法在2D光流与3D场景流估计中实现更简洁有效的跨模态融合。其统一潜在空间思路对失配条件下的多模态特征融合具有借鉴意义。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-guo-x2-fusion-cross-modality-and-cross-dimension-flow-estimation-in-event-edge-space-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 4, \"index\": 1, \"width\": 418, \"height\": 311}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-guo-x2-fusion-cross-modality-and-cross-dimension-flow-estimation-in-event-edge-space-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 5, \"index\": 2, \"width\": 2461, \"height\": 910}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-guo-x2-fusion-cross-modality-and-cross-dimension-flow-estimation-in-event-edge-space-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 7, \"index\": 3, \"width\": 3274, \"height\": 1600}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-guo-x2-fusion-cross-modality-and-cross-dimension-flow-estimation-in-event-edge-space-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 7, \"index\": 4, \"width\": 3342, \"height\": 1048}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-guo-x2-fusion-cross-modality-and-cross-dimension-flow-estimation-in-event-edge-space-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 8, \"index\": 5, \"width\": 3087, \"height\": 1363}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-guo-x2-fusion-cross-modality-and-cross-dimension-flow-estimation-in-event-edge-space-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 8, \"index\": 6, \"width\": 661, \"height\": 549}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-guo-x2-fusion-cross-modality-and-cross-dimension-flow-estimation-in-event-edge-space-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 8, \"index\": 7, \"width\": 600, \"height\": 498}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-guo-x2-fusion-cross-modality-and-cross-dimension-flow-estimation-in-event-edge-space-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 8, \"index\": 8, \"width\": 660, \"height\": 549}]"
motivation: 现有多模态光流方法在异构特征空间各自为政，跨传感器失配未被解决且融合复杂。
method: 提出x^2-Fusion，以事件边缘场作为统一潜在表示锚点，将多模态融合重构为表示统一问题。
result: 在2D光流与3D场景流估计中实现更简洁有效的跨模态融合。
conclusion: 为跨传感器失配下的多模态融合提供统一潜在空间思路。
---

## Abstract
Estimating dense 2D optical flow and 3D scene flow is essential for dynamic scene understanding. Recent work combines images, LiDAR, and event data to jointly predict 2D and 3D motion, yet most approaches operate in separate heterogeneous feature spaces. Without a shared latent space that all modalities can align to, these systems rely on multiple modality-specific blocks, leaving cross-sensor mismatches unresolved and making fusion unnecessarily complex. Event cameras naturally provide a spatiotemporal edge signal, which we can treat as an intrinsic edge field to anchor a unified latent representation, termed the Event Edge Space. Building on this idea, we introduce x^2-Fusion, which reframes multimodal fusion as representation unification: event-derived spatiotemporal edges define an edge-centric homogeneous space, and image and LiDAR features are explicitly aligned in this shared representation. Within this space, we perform reliability-aware adaptive fusion to estimate modality reliability and emphasize stable cues under degradation. We further employ cross-dimension contrast learning to tightly couple 2D optical flow with 3D scene flow. Extensive experiments on both synthetic and real benchmarks show that x^2-Fusion achieves state-of-the-art accuracy under standard conditions and delivers substantial improvements in challenging scenarios.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义

- **研究背景**：密集 2D 光流与 3D 场景流是动态场景理解的核心任务。近期工作尝试融合图像、LiDAR 和事件相机数据，以结合稠密表观、精确几何和高时间分辨率运动信息。
- **核心问题**：现有多模态方法通常让各模态停留在原生异构特征空间中进行融合，导致三类问题：
  - **高复杂度**：需要大量模态特定融合模块、逐对对齐、阶段式注意力等。
  - **信息侵蚀**：融合发生较晚，早期模态特定失真难以通过跨模态交互纠正。
  - **高脆弱性**：缺乏统一表示基础，在曝光极端、LiDAR 稀疏或漂移、运动模糊等退化下，模态间对齐容易崩溃。
- **整体含义**：论文提出 **Event Edge Space（EES，事件边缘空间）**，将事件相机提供的时空边缘信号作为统一潜在表示的锚点，把“多模态融合”重构为“表示统一”。其核心洞见是：
  - 边缘是跨模态、模态无关的结构线索；
  - 事件天然记录运动边缘，且与图像共享 2D 像素坐标，同时具有类似 LiDAR 的异步稀疏采样特性；
  - 因此事件可作为统一图像、LiDAR、事件特征的共享边缘中心空间。

## 2. 方法论

### 2.1 核心思想

- 构建一个 **edge-centric homogeneous latent space**，即事件边缘空间。
- 在该空间中：
  - 事件特征作为固定“边缘原型”；
  - 图像和 LiDAR 特征被显式对齐到事件原型；
  - 融合、可靠度估计和跨维度学习均在同一潜在空间内完成。

### 2.2 关键技术细节

- **事件边缘编码器预训练**
  - 将事件流在时空上体素化，输入稀疏 3D CNN，得到多尺度事件特征金字塔。
  - 定义事件边缘强度：
    - 对每个像素统计归一化事件活动量 \(\tilde{A}_E(x,y)\) 和归一化时间方差 \(\tilde{\sigma}_t(x,y)\)；
    - 组合为 \(e_E(x,y)=\tilde{A}_E(x,y)(1-\tilde{\sigma}_t(x,y))\)，越大表示运动边缘越强且时间越一致。
  - 自监督预训练：将时间窗分为前后两半，用前半事件体素预测后半未来边缘强度。
    - 损失为多尺度预测头输出与未来边缘强度之间的 L1 损失。
  - 预训练后冻结事件编码器，作为后续多模态训练中的稳定边缘
