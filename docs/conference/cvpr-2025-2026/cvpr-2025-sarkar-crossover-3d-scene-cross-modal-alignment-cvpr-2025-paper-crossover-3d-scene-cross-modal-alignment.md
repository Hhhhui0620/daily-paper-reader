---
title: "CrossOver: 3D Scene Cross-Modal Alignment"
title_zh: CrossOver：三维场景跨模态对齐
authors: "Sarkar, Sayan Deb, Miksik, Ondrej, Pollefeys, Marc, Barath, Daniel, Armeni, Iro"
date: 2025
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2025/papers/Sarkar_CrossOver_3D_Scene_Cross-Modal_Alignment_CVPR_2025_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 6.0
evidence: 松弛约束下的灵活场景级跨模态对齐
tldr: 该文指出多模态三维理解常假设数据完整且模态间严格对齐，难以适应现实。作者提出CrossOver框架，通过松弛约束的场景级模态对齐学习统一的模态无关嵌入空间，无需显式物体语义。方法采用维度特定编码器与多阶段训练流程，产生涌现式跨模态行为。实验表明其支持鲁棒的场景检索与物体理解。其松弛对齐思路对未配准多模态融合有借鉴意义。
source: CVPR-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 1191, \"height\": 839}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 1047, \"height\": 874}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 1049, \"height\": 271}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-004.webp\", \"caption\": \"\", \"page\": 1, \"index\": 4, \"width\": 339, \"height\": 510}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-005.webp\", \"caption\": \"\", \"page\": 1, \"index\": 5, \"width\": 1917, \"height\": 370}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-006.webp\", \"caption\": \"\", \"page\": 1, \"index\": 6, \"width\": 2198, \"height\": 348}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-007.webp\", \"caption\": \"\", \"page\": 1, \"index\": 7, \"width\": 1220, \"height\": 382}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-008.webp\", \"caption\": \"\", \"page\": 1, \"index\": 8, \"width\": 673, \"height\": 390}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-009.webp\", \"caption\": \"\", \"page\": 1, \"index\": 9, \"width\": 411, \"height\": 323}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-010.webp\", \"caption\": \"\", \"page\": 3, \"index\": 10, \"width\": 841, \"height\": 754}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-011.webp\", \"caption\": \"\", \"page\": 3, \"index\": 11, \"width\": 583, \"height\": 243}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-012.webp\", \"caption\": \"\", \"page\": 3, \"index\": 12, \"width\": 640, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-013.webp\", \"caption\": \"\", \"page\": 3, \"index\": 13, \"width\": 640, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-014.webp\", \"caption\": \"\", \"page\": 3, \"index\": 14, \"width\": 640, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-015.webp\", \"caption\": \"\", \"page\": 3, \"index\": 15, \"width\": 640, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-016.webp\", \"caption\": \"\", \"page\": 3, \"index\": 16, \"width\": 653, \"height\": 422}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-017.webp\", \"caption\": \"\", \"page\": 3, \"index\": 17, \"width\": 549, \"height\": 243}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-018.webp\", \"caption\": \"\", \"page\": 3, \"index\": 18, \"width\": 547, \"height\": 300}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-019.webp\", \"caption\": \"\", \"page\": 3, \"index\": 19, \"width\": 1200, \"height\": 343}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-020.webp\", \"caption\": \"\", \"page\": 3, \"index\": 20, \"width\": 697, \"height\": 245}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-021.webp\", \"caption\": \"\", \"page\": 3, \"index\": 21, \"width\": 796, \"height\": 375}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-022.webp\", \"caption\": \"\", \"page\": 3, \"index\": 22, \"width\": 742, \"height\": 1465}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-023.webp\", \"caption\": \"\", \"page\": 3, \"index\": 23, \"width\": 372, \"height\": 677}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-024.webp\", \"caption\": \"\", \"page\": 3, \"index\": 24, \"width\": 545, \"height\": 332}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-025.webp\", \"caption\": \"\", \"page\": 3, \"index\": 25, \"width\": 677, \"height\": 249}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-026.webp\", \"caption\": \"\", \"page\": 3, \"index\": 26, \"width\": 372, \"height\": 402}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-027.webp\", \"caption\": \"\", \"page\": 3, \"index\": 27, \"width\": 779, \"height\": 322}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-028.webp\", \"caption\": \"\", \"page\": 3, \"index\": 28, \"width\": 698, \"height\": 943}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-029.webp\", \"caption\": \"\", \"page\": 3, \"index\": 29, \"width\": 578, \"height\": 243}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-030.webp\", \"caption\": \"\", \"page\": 3, \"index\": 30, \"width\": 1200, \"height\": 797}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-031.webp\", \"caption\": \"\", \"page\": 3, \"index\": 31, \"width\": 470, \"height\": 1305}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-032.webp\", \"caption\": \"\", \"page\": 3, \"index\": 32, \"width\": 381, \"height\": 930}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-033.webp\", \"caption\": \"\", \"page\": 3, \"index\": 33, \"width\": 819, \"height\": 637}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-034.webp\", \"caption\": \"\", \"page\": 5, \"index\": 34, \"width\": 854, \"height\": 875}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-035.webp\", \"caption\": \"\", \"page\": 6, \"index\": 35, \"width\": 1200, \"height\": 650}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-036.webp\", \"caption\": \"\", \"page\": 6, \"index\": 36, \"width\": 6093, \"height\": 3298}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-037.webp\", \"caption\": \"\", \"page\": 6, \"index\": 37, \"width\": 549, \"height\": 879}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-038.webp\", \"caption\": \"\", \"page\": 6, \"index\": 38, \"width\": 479, \"height\": 350}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-039.webp\", \"caption\": \"\", \"page\": 6, \"index\": 39, \"width\": 290, \"height\": 415}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-040.webp\", \"caption\": \"\", \"page\": 6, \"index\": 40, \"width\": 440, \"height\": 766}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-041.webp\", \"caption\": \"\", \"page\": 6, \"index\": 41, \"width\": 353, \"height\": 350}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-sarkar-crossover-3d-scene-cross-modal-alignment-cvpr-2025-paper/fig-042.webp\", \"caption\": \"\", \"page\": 8, \"index\": 42, \"width\": 10707, \"height\": 2574}]"
motivation: 现有多模态三维理解假设数据完整且模态严格对齐，难以应对现实中的缺失与未对齐。
method: 提出场景级跨模态对齐框架，用维度特定编码器与多阶段训练学习模态无关嵌入。
result: 实验表明该方法支持鲁棒的场景检索与物体理解。
conclusion: 松弛约束下的跨模态对齐可提升鲁棒性，为未配准多模态融合提供思路。
---

## Abstract
Multi-modal 3D object understanding has gained significant attention, yet current approaches often assume complete data availability and rigid alignment across all modalities. We present CrossOver, a novel framework for cross-modal 3D scene understanding via flexible, scene-level modality alignment. Unlike traditional methods that require aligned modality data for every object instance, CrossOver learns a unified, modality-agnostic embedding space for scenes by aligning modalities -- RGB images, point clouds, CAD models, floorplans, and text descriptions -- with relaxed constraints and without explicit object semantics. Leveraging dimensionality-specific encoders, a multi-stage training pipeline, and emergent cross-modal behaviors, CrossOver supports robust scene retrieval and object localization, even with missing modalities. Evaluations on ScanNet and 3RScan datasets show its superior performance across diverse metrics, highlighting CrossOver's adaptability for real-world applications in 3D scene understanding.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义
- **研究动机**：现有多模态 3D 理解方法通常假设数据完整、模态间严格对齐，并要求每个物体实例在所有模态中都有对应数据。这在真实场景中往往不成立，例如点云缺失、图像遮挡、CAD 模型与真实场景实例不一致、跨模态实例分割难以统一等。
- **核心问题**：如何在缺少完整模态配对、没有显式物体语义或 3D 场景图的条件下，实现 3D 场景级跨模态对齐与理解。
- **整体含义**：论文提出 **CrossOver**，将 RGB 图像、点云、CAD 网格、floorplan、文本描述五种模态映射到统一的、模态无关的嵌入空间。目标不是只做物体级匹配，而是支持场景级跨模态检索、实例定位与缺失模态下的鲁棒推理。

## 2. 方法论
### 2.1 核心思想
- 学习一个 **统一的模态无关场景嵌入空间**，使同一 3D 场景在不同模态下的表示彼此接近。
- 采用 **松弛约束**：训练时不要求所有模态同时存在，也不要求跨模态实例语义完全一致；推理时无需语义实例分割或显式 3D 场景图。
- 以图像模态 `I` 作为训练时的基础锚模态，将其他模态对齐到图像特征空间，从而产生涌现式跨模态行为。

### 2.2 模态定义
- `I`：RGB 多视图图像。
- `P`：真实重建点云。
- `M`：CAD 网格 / mesh。
- `R`：文本描述 / object referrals。
- `F`：栅格化 floorplan。

### 2.3 三阶段 / 三层结构
1. **实例级多模态交互**
   - 1D 文本编码：使用 BLIP 编码 object referrals，如“椅子在灯前面”，对每个实例的多个 referral 做平均池化。
   - 2D 图像编码：对每个实例选可见性最高的 top-K 视图，生成多级 bounding box，用 DinoV2 提取 crop 的 CLS token，再平均池化。
   - 3D 点云 / 网格编码：点云和 mesh 用预训练 I2PMAE 编码；点云实例拼接 3D 位置，并通过 spatial-attention transformer 建模实例间空间关系。mesh 不假设与场景几何对齐，因此不编码位置和空间关系。
   - 对比损失：将 `P/M/R` 对齐到 `I`，形式为  
     `L_Oi = L(f_Ii, f_Pi) + L(f_Ii, f_Mi) + L(f_Ii, f_Ri)`。

2. **场景级多模态交互**
   - 对同一场景内各实例特征按模态做平均池化，得到场景级 `f_R, f_I, f_P, f_M`。
   - 使用可学习注意力权重进行加权融合，得到统一场景嵌入 `F_S`：  
     `F_S = Σ_q [ exp(w_q) / Σ_j exp(w_j) · f_q ]`。
   - 再通过 MLP 投影到最终表示空间。

3. **统一维度编码器**
   - 为避免推理时依赖跨模态一致的语义实例信息，设计 1D、2D、3D 三类编码器直接处理原始数据。
   - 1D：每场景随机采样约 10 条 referral，用文本编码器形成 `F_1D`。
   - 2D：RGB 与 floorplan 共享同一个 DinoV2 编码器权重；RGB 选约 10 个关键帧，拼接 CLS 与 patch 聚合特征，平均池化得到 `F_2D`。
   - 3D：使用 Minkowski Engine 稀疏卷积网络，将点云体素化后输出 `F_3D`。
   - 训练损失：  
     `L_s = αL(F_S, F_1D) + βL(F_S, F_2D) + γL(F_S, F_3D)`，  
     总损失 `L = L_s + Σ_Oi L_Oi`。

### 2.4 损失与推理
- 使用类似 ImageBind 的对称对比损失 InfoNCE，温度 `τ` 可学习。
- 对不可用模态对，直接 mask 对应损失项，从而支持不完整模态训练。
- 推理时，将查询模态编码到共享空间，在目标模态数据库中做最近邻检索，可完成跨模态实例检索和跨模态场景检索。

## 3. 实验设计
### 3.1 数据集与场景
- **ScanNet**：RGB-D 视频数据集，包含 250 万视图、1500 多个室内场景，提供图像、点云、相机位姿、实例语义分割等。
- **3RScan**：室内重扫描数据集，包含 1428 个 RGB-D 序列、478 个室内场景，支持时序重定位和物体移动后的重扫描。
- **辅助数据**：
  - object referrals 来自 SceneVerse。
  - ScanNet 上的 CAD mesh 和 floorplan 来自 Scan2CAD / ShapeNet。

### 3.2 评测任务与 benchmark
- **跨模态实例检索**：同一场景内，给定某实例的一种模态，检索其另一种模态。
- **场景级匹配召回**：R@25%、R@50%、R@75%，衡量场景内实例匹配比例。
- **跨模态场景检索**：
  - scene matching recall：检索完全相同的场景。
  - scene category recall：检索同类场景。
  - temporal recall：检索不同时间采集的同一场景。
  - intra-category recall：在单类别数据库中检索特定场景。
- **时序实例匹配**：在 3RScan 上评估物体移动 / 重排后的实例匹配。
- **缺失模态实验**：用非重叠数据分别训练 `I→P` 和 `I→M`，测试涌现出的 `P→M` 匹配能力。

### 3.3 对比方法
- 多模态预训练方法：**ULIP-2**、**PointBind**。
- 自身基线：**Instance Baseline (Ours)**，
