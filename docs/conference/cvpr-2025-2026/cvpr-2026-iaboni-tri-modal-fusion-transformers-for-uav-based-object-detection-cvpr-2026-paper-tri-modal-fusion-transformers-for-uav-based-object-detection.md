---
title: Tri-Modal Fusion Transformers for UAV-based Object Detection
title_zh: 面向无人机目标检测的三模态融合Transformer
authors: "Iaboni, Craig, Abichandani, Pramod"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Iaboni_Tri-Modal_Fusion_Transformers_for_UAV-based_Object_Detection_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 7.0
evidence: 无人机目标检测融合RGB、热红外与事件多模态
tldr: 无人机目标检测在低光与运动模糊下RGB线索失效，热红外与事件模态可提供互补信息。本文提出三模态融合Transformer，以双流层次化结构处理RGB、热红外与事件数据，并在编码器中引入模态感知门控交换与双向令牌交换模块实现分辨率保持的融合。该框架在复杂场景下提升了检测鲁棒性，首次系统研究三模态统一检测器，为无人机多模态感知提供新框架。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-iaboni-tri-modal-fusion-transformers-for-uav-based-object-detection-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 2, \"index\": 1, \"width\": 1369, \"height\": 644}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-iaboni-tri-modal-fusion-transformers-for-uav-based-object-detection-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 3, \"index\": 2, \"width\": 733, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-iaboni-tri-modal-fusion-transformers-for-uav-based-object-detection-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 5, \"index\": 3, \"width\": 4138, \"height\": 1397}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-iaboni-tri-modal-fusion-transformers-for-uav-based-object-detection-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 8, \"index\": 4, \"width\": 1092, \"height\": 1080}]"
motivation: 无人机目标检测在光照变化与运动模糊下RGB线索失效，需融合热红外与事件模态提升鲁棒性。
method: 提出处理RGB、热红外与事件三模态的双流层次化视觉Transformer，含模态感知门控交换与双向令牌交换模块。
result: 在无人机检测任务中实现分辨率保持的多模态融合，提升低光等复杂场景下的检测鲁棒性。
conclusion: 首次系统研究三模态统一检测器，为无人机多模态感知提供新框架。
---

## Abstract
Reliable UAV object detection requires robustness to illumination changes, motion blur, and scene dynamics that suppress RGB cues. Thermal long-wave infrared (LWIR) sensing preserves contrast in low light, and event cameras retain microsecond-level temporal edges, but integrating all three modalities in a unified detector has not been systematically studied. We present a tri-modal framework that processes RGB, thermal, and event data with a dual-stream hierarchical vision transformer. At selected encoder depths, a Modality-Aware Gated Exchange (MAGE) applies inter-sensor channel and spatial gating, and a Bidirectional Token Exchange (BiTE) module performs bidirectional token-level attention with depthwise-pointwise refinement, producing resolution-preserving fused maps for a standard feature pyramid and two-stage detector. We introduce a 10,489-frame UAV dataset with synchronized and pre-aligned RGB-thermal-event streams and 24,223 annotated vehicles across day and night flights. Through 61 controlled ablations, we evaluate fusion placement, mechanism (baseline MAGE+BiTE, CSSA, GAFF), modality subsets, and backbone capacity. Tri-modal fusion improves over all dual-modal baselines, with fusion depth having a significant effect and a lightweight CSSA variant recovering most of the benefit at minimal cost. This work provides the first systematic benchmark and modular backbone for tri-modal UAV-based object detection.

---

## 论文详细总结（自动生成）

# 论文总结：Tri-Modal Fusion Transformers for UAV-based Object Detection

## 1. 核心问题与整体含义
- **研究动机**：无人机目标检测常面临光照突变、运动模糊、平台动态、热杂波等挑战，单一 RGB 模态在低光、模糊场景下容易失效；热红外 LWIR 在低光下保留对比度，事件相机提供微秒级时序边缘信息，但三者存在噪声、空间对齐、时间密度和语义可靠性差异。
- **核心问题**：现有检测器多基于 RGB 或 RGB–热红外、RGB–事件等双模态，缺乏对 RGB、热红外、事件三模态统一检测器的系统研究，也缺少同步、预对齐的三模态 UAV 基准数据集。
- **整体含义**：论文将三模态融合视为架构设计空间，提出可插拔、分辨率保持的融合骨干，并构建首个三模态 UAV 检测基准，系统评估融合位置、融合机制、模态组合与骨干容量。

## 2. 方法论
- **核心思想**：采用双流层次化视觉 Transformer，将 RGB 作为
