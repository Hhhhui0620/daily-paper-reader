---
title: Multi-Modal Aerial-Ground Cross-View Place Recognition with Neural ODEs
title_zh: 基于神经常微分方程的多模态空地跨视角地点识别
authors: "Wang, Sijie, She, Rui, Kang, Qiyu, Li, Siqi, Li, Disheng, Geng, Tianyu, Yu, Shangshu, Tay, Wee Peng"
date: 2025
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2025/papers/Wang_Multi-Modal_Aerial-Ground_Cross-View_Place_Recognition_with_Neural_ODEs_CVPR_2025_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 5.0
evidence: 融合相机与激光雷达的多模态空地跨视角识别
tldr: 多模态地点识别多聚焦同视角匹配，地面视角描述子与航拍视角数据库匹配的跨视角场景仍待探索。本文提出AGPlace模型，融合相机与激光雷达等多模态地面传感器信息，借助神经ODE在流形上实现空地跨视角地点识别。实验表明该方法取得准确的跨视角识别性能。该工作为无人机航拍多模态感知与跨视角特征融合提供了方法参考。
source: CVPR-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-multi-modal-aerial-ground-cross-view-place-recognition-with-neural-odes-cvpr-2025-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 693, \"height\": 398}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-multi-modal-aerial-ground-cross-view-place-recognition-with-neural-odes-cvpr-2025-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 900, \"height\": 317}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-multi-modal-aerial-ground-cross-view-place-recognition-with-neural-odes-cvpr-2025-paper/fig-003.webp\", \"caption\": \"\", \"page\": 4, \"index\": 3, \"width\": 901, \"height\": 320}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-multi-modal-aerial-ground-cross-view-place-recognition-with-neural-odes-cvpr-2025-paper/fig-004.webp\", \"caption\": \"\", \"page\": 4, \"index\": 4, \"width\": 721, \"height\": 320}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-multi-modal-aerial-ground-cross-view-place-recognition-with-neural-odes-cvpr-2025-paper/fig-005.webp\", \"caption\": \"\", \"page\": 4, \"index\": 5, \"width\": 463, \"height\": 464}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-multi-modal-aerial-ground-cross-view-place-recognition-with-neural-odes-cvpr-2025-paper/fig-006.webp\", \"caption\": \"\", \"page\": 4, \"index\": 6, \"width\": 463, \"height\": 464}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-multi-modal-aerial-ground-cross-view-place-recognition-with-neural-odes-cvpr-2025-paper/fig-007.webp\", \"caption\": \"\", \"page\": 4, \"index\": 7, \"width\": 463, \"height\": 464}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-multi-modal-aerial-ground-cross-view-place-recognition-with-neural-odes-cvpr-2025-paper/fig-008.webp\", \"caption\": \"\", \"page\": 5, \"index\": 8, \"width\": 697, \"height\": 765}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-multi-modal-aerial-ground-cross-view-place-recognition-with-neural-odes-cvpr-2025-paper/fig-009.webp\", \"caption\": \"\", \"page\": 5, \"index\": 9, \"width\": 700, \"height\": 765}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-multi-modal-aerial-ground-cross-view-place-recognition-with-neural-odes-cvpr-2025-paper/fig-010.webp\", \"caption\": \"\", \"page\": 5, \"index\": 10, \"width\": 700, \"height\": 765}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-multi-modal-aerial-ground-cross-view-place-recognition-with-neural-odes-cvpr-2025-paper/fig-011.webp\", \"caption\": \"\", \"page\": 6, \"index\": 11, \"width\": 846, \"height\": 317}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-multi-modal-aerial-ground-cross-view-place-recognition-with-neural-odes-cvpr-2025-paper/fig-012.webp\", \"caption\": \"\", \"page\": 6, \"index\": 12, \"width\": 936, \"height\": 355}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-multi-modal-aerial-ground-cross-view-place-recognition-with-neural-odes-cvpr-2025-paper/fig-013.webp\", \"caption\": \"\", \"page\": 6, \"index\": 13, \"width\": 640, \"height\": 640}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-multi-modal-aerial-ground-cross-view-place-recognition-with-neural-odes-cvpr-2025-paper/fig-014.webp\", \"caption\": \"\", \"page\": 8, \"index\": 14, \"width\": 544, \"height\": 599}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-multi-modal-aerial-ground-cross-view-place-recognition-with-neural-odes-cvpr-2025-paper/fig-015.webp\", \"caption\": \"\", \"page\": 8, \"index\": 15, \"width\": 507, \"height\": 546}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-multi-modal-aerial-ground-cross-view-place-recognition-with-neural-odes-cvpr-2025-paper/fig-016.webp\", \"caption\": \"\", \"page\": 8, \"index\": 16, \"width\": 398, \"height\": 395}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-wang-multi-modal-aerial-ground-cross-view-place-recognition-with-neural-odes-cvpr-2025-paper/fig-017.webp\", \"caption\": \"\", \"page\": 8, \"index\": 17, \"width\": 398, \"height\": 395}]"
motivation: 多模态地点识别多聚焦同视角，地面与航拍视角匹配的跨视角场景仍待探索。
method: 提出AGPlace模型，融合相机与激光雷达信息，借助神经ODE在流形上实现跨视角识别。
result: 实验表明该方法取得准确的空地跨视角识别性能。
conclusion: 为航拍多模态感知与跨视角特征融合提供了参考。
---

## Abstract
Place recognition (PR) aims at retrieving the query place from a database and plays a crucial role in various applications, including navigation, autonomous driving, and augmented reality. While previous multi-modal PR works have mainly focused on the same-view scenario in which ground-view descriptors are matched with a database of ground-view descriptors during inference, the multi-modal cross-view scenario, in which ground-view descriptors are matched with aerial-view descriptors in a database, remains under-explored. We propose AGPlace, a model that effectively integrates information from multi-modal ground sensors (cameras and LiDARs) to achieve accurate aerial-ground PR. AGPlace achieves effective aerial-ground cross-view PR by leveraging a manifold-based neural ordinary differential equation (ODE) framework with a multi-domain alignment loss. It outperforms existing state-of-the-art cross-view PR models on large-scale datasets. As most existing PR models are designed for ground-ground PR, we adapt these baselines into our cross-view pipeline. Experiments demonstrate that this direct adaptation performs worse than our overall model architecture AGPlace. AGPlace represents a significant advancement in multi-modal aerial-ground PR, with promising implications for real-world applications.

---

## 论文详细总结（自动生成）

# 论文总结：Multi-Modal Aerial-Ground Cross-View Place Recognition with Neural ODEs

## 1. 核心问题与整体含义

- **研究背景**：地点识别（Place Recognition, PR）将定位视为检索任务，广泛应用于导航、自动驾驶、AR、SLAM 等。现有 PR 工作大多关注：
  - **单模态同视角**：图像-图像或点云-点云匹配；
  - **多模态同视角**：地面相机 + LiDAR 与地面数据库匹配；
  - **空地跨视角**：地面查询与航拍数据库匹配，但现有方法多局限于“地面图像 vs 航拍图像”的同模态跨视角。
- **核心问题**：如何利用地面多模态传感器（2D 相机图像 + 3D LiDAR 点云）作为查询，与航拍数据库（卫星 RGB 图像、道路语义图）进行跨视角地点识别。该场景对地面机器人定位很有价值，因为航拍地图覆盖广、采集效率高，且能提供丰富几何参考。
- **整体含义**：论文提出 **AGPlace**，通过流形上的神经常微分方程（Neural ODE）融合多模态信息，并设计多域对齐损失，实现多模态空地跨视角 PR。作者还构建了两个新基准数据集，证明 AGPlace 优于现有 SOTA 跨视角 PR 模型和多种多模态 PR 基线。

## 2. 方法论

- **核心思想**：
  - 采用 **两阶段融合**：先构建融合嵌入，再将融合嵌入注入各模态空间进行模态级融合。
  - 使用 **流形上的 Neural ODE** 描述融合状态演化，利用 ODE 解的非交叉性质保证不同地点的表示可区分。
  - 设计 **多视角多模态损失（MVMM loss）**，同时对齐航拍-航拍、地面-航拍、地面 2D-航拍、地面 3D-航拍特征。
- **问题形式化**：
  - 地面查询为图像 \(I_G\) 和点云 \(P_G\)，航拍数据库为 \(I_A\)。
  - 目标：学习地面模型 \(f_G\) 与航拍模型 \(f_A\)，使查询与正邻域内的航拍地点距离最小。
- **模态特征提取**：
  - 航拍侧使用现成 2D VPR 方法（如 ResNet-GeM）提取描述子。
  - 地面侧分别用 2D 和 3D backbone 提取多层级特征图 \(F_{2D}\)、\(F_{3D}\)。
- **阶段 1：融合嵌入构建**：
  - 从最后一个 block 向第一个 block 演化，即 \(L \to 1\)。
  - 每个 block 的状态初始化：
    - 若 \(l=L\)，初始状态为融合动量 \(m_l\)；
    - 否则，初始状态为 \(m_l + \gamma_{l+1}(T)\)。
  - 融合动量 \(m_l\) 由 2D/3D 池化特征经可学习流形 chart 函数 \(\phi_{2D}^l\)、\(\phi_{3D}^l\) 映射后相加得到。
  - 状态更新用 Neural ODE：\(\frac{d\gamma_l(t)}{dt}=f_{\theta_l}(\gamma_l(t))\)。
  - 最终融合嵌入为第一 block 的末状态 \(e_{\text{fuse}}=\gamma_1(T)\)。
  - 理论依据：ODE 解的非交叉性质表明，不同初始条件会产生不同轨迹，因此不同地点可得到不同融合状态。
- **阶段 2：模态级融合**：
  - 将融合嵌入通过 chart 函数 \(\psi_{\text{fuse},2D}\)、\(\psi_{\text{fuse},3D}\) 投影回 2D/3D 空间，得到 \(e_{2D}\)、\(e_{3D}\)。
  - 与最后 block 的原始模态特征图广播相加，经 decoder 和池化得到 \(e'_{2D}\)、\(e'_{3D}\)。
  - 最终地面场景描述子：\(e_G=\lambda'(e'_{2D}+e'_{3D})+\lambda_{\text{fuse}}e_{\text{fuse}}\)。
- **损失函数**：
  - **MVMM loss**：将 PR 视为二分类，正样本距离小、负样本距离大；同时对齐航拍-航拍、地面-航拍、地面 2D-航拍、地面 3D-航拍。
  - **Triplet loss**：相对引导，强制负样本距离大于正样本距离，并采用硬负样本挖掘。
  - 总损失：\(\ell=\alpha \ell_{\text{MVMM}}+\ell_{\text{tri}}\)。

## 3. 实验设计

- **数据集 / 场景**：
  - **KITTI360-AG**：基于 KITTI360，提供地面图像、点云、GNSS；7 个序列，前 85% 训练、后 15% 测试，测试包含已见和未见过区域。航拍数据通过 Google Maps Static API 下载，包括卫星图和道路图，约 75×75 m²。
  - **nuScenes-AG**：基于 nuScenes，使用官方 train/test split，包含多相机和 LiDAR，测试场景也覆盖已见/未见过区域。
  - **Oxford RobotCar**：公开多模态地面-地面 PR 基准，采用 MinkLoc++ 和 AdaFusion 两种 split，用于验证地面模型本身
