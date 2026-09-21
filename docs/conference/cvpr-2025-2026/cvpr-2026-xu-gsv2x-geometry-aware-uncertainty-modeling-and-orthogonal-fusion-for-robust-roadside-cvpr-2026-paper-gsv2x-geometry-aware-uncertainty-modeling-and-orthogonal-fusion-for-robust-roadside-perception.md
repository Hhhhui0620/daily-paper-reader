---
title: "GSV2X: Geometry-Aware Uncertainty Modeling and Orthogonal Fusion for Robust Roadside Perception"
title_zh: GSV2X：面向鲁棒路侧感知的几何感知不确定性建模与正交融合
authors: "Xu, Jianqiang, Pei, Gensheng, Liu, Huafeng, Yao, Yazhou"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Xu_GSV2X_Geometry-Aware_Uncertainty_Modeling_and_Orthogonal_Fusion_for_Robust_Roadside_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 6.0
evidence: 几何感知不确定性建模与抗错位融合
tldr: 该文针对多视角路侧感知中相机与激光雷达融合受几何错位和标定误差影响的问题，提出GSV2X融合框架。方法将二维图像特征提升到BEV空间并以三维高斯分布建模空间不确定性，结合相机几何引导的可学习扰动，同时设计正交融合模块增强模态协同。实验表明该方法对错位与标定误差具有更强鲁棒性。其不确定性建模与抗错位融合思路对未配准多模态检测具有借鉴意义。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 8, \"index\": 1, \"width\": 1015, \"height\": 634}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 8, \"index\": 2, \"width\": 1015, \"height\": 634}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 8, \"index\": 3, \"width\": 1015, \"height\": 634}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 8, \"index\": 4, \"width\": 1015, \"height\": 634}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 8, \"index\": 5, \"width\": 1015, \"height\": 634}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 8, \"index\": 6, \"width\": 1015, \"height\": 634}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 8, \"index\": 7, \"width\": 1015, \"height\": 634}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 8, \"index\": 8, \"width\": 1380, \"height\": 1030}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 8, \"index\": 9, \"width\": 1380, \"height\": 1030}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 8, \"index\": 10, \"width\": 1015, \"height\": 634}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 8, \"index\": 11, \"width\": 1015, \"height\": 634}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 8, \"index\": 12, \"width\": 1015, \"height\": 634}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 8, \"index\": 13, \"width\": 1015, \"height\": 634}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 8, \"index\": 14, \"width\": 1015, \"height\": 634}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 8, \"index\": 15, \"width\": 1015, \"height\": 634}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 8, \"index\": 16, \"width\": 1015, \"height\": 634}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 8, \"index\": 17, \"width\": 1015, \"height\": 634}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 8, \"index\": 18, \"width\": 1380, \"height\": 1030}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 8, \"index\": 19, \"width\": 1380, \"height\": 1030}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-xu-gsv2x-geometry-aware-uncertainty-modeling-and-orthogonal-fusion-for-robust-roadside-cvpr-2026-paper/fig-020.webp\", \"caption\": \"\", \"page\": 8, \"index\": 20, \"width\": 1015, \"height\": 634}]"
motivation: 路侧多视角感知中相机与激光雷达融合常受几何错位与标定误差干扰，亟需鲁棒融合方案。
method: 将二维图像特征提升至BEV空间并用三维高斯分布建模空间不确定性，同时设计正交融合模块增强模态协同。
result: 在受错位与标定误差影响的场景中，所提方法展现出更强的鲁棒性与融合性能。
conclusion: 不确定性建模结合正交融合可有效缓解几何错位问题，为跨模态对齐提供可迁移思路。
---

## Abstract
Reliable 3D perception from multi-view roadside sensors hinges on the robust fusion of camera and LiDAR data, a task complicated by geometric misalignments and sensor calibration errors. This paper presents GSV2X, a fusion framework that tackles these challenges through two core contributions. First, to achieve robustness against spatial uncertainty, we lift 2D image features into a unified Bird's-Eye-View (BEV) space by representing them as 3D Gaussian distributions. By incorporating learnable perturbations guided by camera geometry, our model explicitly accounts for potential calibration inaccuracies. Second, to maximize the synergy between modalities, we propose a new orthogonal fusion module. This module employs constrained attention to enforce orthogonality between camera and LiDAR features, effectively disentangling redundant information and promoting the learning of complementary representations. Extensive experiments on the challenging RCooper dataset demonstrate that GSV2X sets a new state-of-the-art in multi-view roadside perception and exhibits remarkable robustness in complex, real-world scenarios.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义
- **研究动机**：路侧感知系统（RPS）通常部署在固定位置，可提供全局视角，但多视角相机与 LiDAR 融合在实际部署中极易受**几何错位、标定误差、深度估计误差**影响。
- **核心问题**：
  - **空间不确定性**：将 2D 图像特征投影到统一 BEV 空间依赖精确标定，微小误差会导致特征错位、鬼影、跟踪不稳定和漏检。
  - **模态不平衡/冗余**：相机特征稠密、LiDAR 特征稀疏但几何精确，简单拼接或相加容易造成相机模态主导，削弱 LiDAR 的几何贡献。
- **整体含义**：论文提出 **GSV2X**，试图通过概率化 BEV 表示与正交融合，提升多视角路侧 3D 感知在真实复杂场景中的鲁棒性，并在 RCooper、DAIR-V2X-I 上验证其有效性与泛化能力。

## 2. 方法论
- **核心思想**：不再将每个像素确定性投影为单个 3D 点，而是表示为 **3D 高斯分布**，以吸收深度与标定不确定性；融合阶段不追求简单相似对齐，而是用**正交正则**促进相机与 LiDAR 的互补性。
- **概率
