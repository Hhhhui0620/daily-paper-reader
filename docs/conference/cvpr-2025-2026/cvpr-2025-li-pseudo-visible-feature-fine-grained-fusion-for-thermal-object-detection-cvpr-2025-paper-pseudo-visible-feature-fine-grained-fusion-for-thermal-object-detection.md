---
title: Pseudo Visible Feature Fine-Grained Fusion for Thermal Object Detection
title_zh: 伪可见特征细粒度融合用于热红外目标检测
authors: "Li, Ting, Ye, Mao, Wu, Tianwen, Li, Nianxin, Li, Shuaifeng, Tang, Song, Ji, Luping"
date: 2025
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2025/papers/Li_Pseudo_Visible_Feature_Fine-Grained_Fusion_for_Thermal_Object_Detection_CVPR_2025_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 7.0
evidence: 可见光与热红外的跨模态特征融合
tldr: 热红外目标检测常借助热转可见光模型与跨模态聚合，但现有融合未能充分利用可见光互补信息。本文提出伪可见特征细粒度融合方法PFGF，以多层级热特征与伪可见潜在特征构建图结构进行细粒度聚合。实验表明该方法更充分地挖掘可见光互补线索，提升了热红外检测性能，为可见光-热红外跨模态融合提供了新思路。
source: CVPR-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-li-pseudo-visible-feature-fine-grained-fusion-for-thermal-object-detection-cvpr-2025-paper/fig-001.webp\", \"caption\": \"\", \"page\": 8, \"index\": 1, \"width\": 407, \"height\": 301}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-li-pseudo-visible-feature-fine-grained-fusion-for-thermal-object-detection-cvpr-2025-paper/fig-002.webp\", \"caption\": \"\", \"page\": 8, \"index\": 2, \"width\": 407, \"height\": 301}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-li-pseudo-visible-feature-fine-grained-fusion-for-thermal-object-detection-cvpr-2025-paper/fig-003.webp\", \"caption\": \"\", \"page\": 8, \"index\": 3, \"width\": 407, \"height\": 302}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-li-pseudo-visible-feature-fine-grained-fusion-for-thermal-object-detection-cvpr-2025-paper/fig-004.webp\", \"caption\": \"\", \"page\": 8, \"index\": 4, \"width\": 406, \"height\": 302}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-li-pseudo-visible-feature-fine-grained-fusion-for-thermal-object-detection-cvpr-2025-paper/fig-005.webp\", \"caption\": \"\", \"page\": 8, \"index\": 5, \"width\": 406, \"height\": 301}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-li-pseudo-visible-feature-fine-grained-fusion-for-thermal-object-detection-cvpr-2025-paper/fig-006.webp\", \"caption\": \"\", \"page\": 8, \"index\": 6, \"width\": 407, \"height\": 302}]"
motivation: 现有热转可见光加跨模态聚合的融合方式未能充分利用可见光互补信息。
method: 提出伪可见特征细粒度融合PFGF，以热特征与伪可见潜在特征构图进行跨模态聚合。
result: 更充分挖掘可见光互补线索，提升热红外目标检测性能。
conclusion: 为可见光与热红外的细粒度跨模态融合提供了有效方案。
---

## Abstract
Thermal object detection is a critical task in various fields, such as surveillance and autonomous driving. Current state-of-the-art (SOTA) models always leverage a prior Thermal-To-Visible (T2V) translation model to obtain visible spectrum information, followed by a cross-modality aggregation module to fuse information from both modalities. However, this fusion approach does not fully exploit the complementary visible spectrum information beneficial for thermal detection. To address this issue, we propose a novel cross-modal fusion method called Pseudo Visible Feature Fine-Grained Fusion (PFGF). Specifically, a graph is constructed with nodes generated from multi-level thermal features and pseudo-visual latent features produced by the T2V model. Each level of features corresponds to a subgraph. An Inter-Mamba block is proposed to perform cross-modality fusion between nodes at the lowest level; while a Cascade Knowledge Integration (CKI) strategy is used to fuse low-level fused information to high-level subgraphs in a cascade manner. After several iterations of graph node updating, each subgraph outputs an aggregated feature to the detection head respectively. Unlike previous cross-modal fusion methods, our approach explicitly models high-level relationships between cross-modal data, effectively fusing different granularity information. Experimental results demonstrate that our method achieves SOTA detection performance. Code is available at https://github.com/liting1018/PFGF.

---

## 论文详细总结（自动生成）

# 论文总结：Pseudo Visible Feature Fine-Grained Fusion for Thermal Object Detection

## 1. 核心问题与整体含义
- **研究背景**：热红外目标检测在 surveillance、自动驾驶、低照度/隐私敏感场景中很重要。可见光图像在夜间、雾雪等条件下退化，热红外更稳健，但白天纹理细节不足。
- **现有路线**：多光谱检测需要成对可见光-热红外图像用于训练和推理，硬件成本与配准要求高；可见知识辅助路线希望训练时利用可见光知识，测试时仅输入热红外图像。
- **核心问题**：当前 SOTA 常用 Thermal
