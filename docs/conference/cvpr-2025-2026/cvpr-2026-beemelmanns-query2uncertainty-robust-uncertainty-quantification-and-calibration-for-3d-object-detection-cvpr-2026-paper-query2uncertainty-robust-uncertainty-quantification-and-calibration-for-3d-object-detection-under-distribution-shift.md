---
title: "Query2Uncertainty: Robust Uncertainty Quantification and Calibration for 3D Object Detection under Distribution Shift"
title_zh: Query2Uncertainty：分布偏移下三维目标检测的鲁棒不确定性量化与校准
authors: "Beemelmanns, Till, Nekrasov, Alexey, Vilceanu, Stefan, Steinhaus, Jonas, Woopen, Timo, Leibe, Bastian, Eckstein, Lutz"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Beemelmanns_Query2Uncertainty_Robust_Uncertainty_Quantification_and_Calibration_for_3D_Object_Detection_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 5.0
evidence: 基于查询特征密度进行不确定性量化与校准
tldr: 三维目标检测在分布偏移下置信度校准不佳，现有事后校准方法难以适应偏移场景。本文提出Query2Uncertainty，利用DETR类检测器潜在对象查询的密度感知特征，将事后校准器与特征密度耦合，从而动态调整模型置信度。实验表明该方法在分布偏移下显著改善了不确定性估计与校准质量。该工作为多模态与跨模态任务中的不确定性建模提供了可迁移的校准思路。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-beemelmanns-query2uncertainty-robust-uncertainty-quantification-and-calibration-for-3d-object-detection-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 756, \"height\": 426}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-beemelmanns-query2uncertainty-robust-uncertainty-quantification-and-calibration-for-3d-object-detection-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 756, \"height\": 426}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-beemelmanns-query2uncertainty-robust-uncertainty-quantification-and-calibration-for-3d-object-detection-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 3, \"index\": 3, \"width\": 2400, \"height\": 1200}]"
motivation: 三维检测器在分布偏移下校准较差，现有事后校准方法难以适应偏移场景。
method: 提出密度感知校准方法，将事后校准器与DETR式检测器潜在查询的特征密度耦合。
result: 实验表明方法在分布偏移下显著改善不确定性估计与校准质量。
conclusion: 为跨模态任务中的不确定性建模提供了可迁移的校准思路。
---

## Abstract
Reliable uncertainty estimation for 3D object detection is critical for deploying safe autonomous systems, yet modern detectors remain poorly calibrated, especially under distribution shifts. Although post-hoc calibration methods address this issue and provide improved calibration for in-distribution tests, they fail to adapt in distribution-shifted scenarios. In this work, we address this issue and introduce a density-aware calibration method that couples post-hoc calibrators with the feature density of latent object queries from DETR-style 3D object detectors. These queries form a compact, location and class-aware feature, ideal for density estimation, allowing our approach to adjust model confidences in distribution-shift scenarios. By fitting a density estimator on these query features, our approach jointly recalibrates both classification and bounding box regression uncertainties. On both a multi-view camera and LiDAR-based detector, our approach consistently outperforms standard post-hoc methods in both in-distribution and distribution-shifted scenarios. Code: https://tillbeemelmanns.github.io/query2uncertainty

---

## 论文详细总结（自动生成）

# Query2Uncertainty 论文总结

## 1. 核心问题与整体含义

- **研究动机**：3D 目标检测是自动驾驶与机器人感知的核心模块，其输出的 3D 框、类别和不确定性会被用于跟踪、融合、规划与避障。因此，可靠的不确定性估计对安全关键系统至关重要。
- **核心问题**：现代 DETR 式 3D 检测器通常存在**过度自信**问题，置信度无法真实反映预测正确概率。现有事后校准方法在**同分布（ID）**测试中有效，但在**分布偏移（distribution shift）**场景下会失效，因为它们假设测试数据与校准数据同分布，并对所有输入施加相同校正。
- **整体含义**：论文提出 **Query2Uncertainty**，利用 DETR 式 3D 检测器中潜在对象查询的特征密度，使事后校准器具备密度感知能力，从而在 ID 与分布偏移下同时校准**分类不确定性**和**边界框回归不确定性**。论文还建立了一个面向 3D 目标检测的不确定性量化评测基准。

## 2. 方法论

### 2.1 核心思想

- 在 DETR 式 3D 检测器中，最终解码器输出的对象查询 `z` 是紧凑、位置感知、类别感知的潜在特征，可视为对象假设的嵌入。
- 训练时缓存与真值匹配的 True Positive 查询特征，按类别拟合密度估计器。
- 测试时，若查询特征密度高，说明其接近训练分布，可保持较尖锐置信度；若密度低，说明可能遭遇分布偏移，应调低置信度或放大回归方差。
- 密度信号被注入经典事后校准器，形成 **DA-TS、DA-PS、DA-IR** 等密度感知校准方法。

### 2.2 概率化 Transformer 检测器

- 输入为多视图相机图像或 LiDAR 点云，经 backbone 与位置编码后作为 token 输入 DETR 式解码器。
- 可学习对象查询 `z0` 与 3D 特征交互，最终输出精炼
