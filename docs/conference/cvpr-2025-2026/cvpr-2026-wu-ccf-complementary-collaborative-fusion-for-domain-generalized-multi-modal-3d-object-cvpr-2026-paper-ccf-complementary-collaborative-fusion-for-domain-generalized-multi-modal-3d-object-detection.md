---
title: "CCF: Complementary Collaborative Fusion for Domain Generalized Multi-Modal 3D Object Detection"
title_zh: CCF：面向域泛化多模态三维目标检测的互补协同融合
authors: "Wu, Yuchen, Wang, Kun, Pan, Yining, Zhao, Na"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Wu_CCF_Complementary_Collaborative_Fusion_for_Domain_Generalized_Multi-Modal_3D_Object_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 4.0
evidence: 单一模态退化下的鲁棒多模态融合
tldr: 多模态融合在跨域部署时性能显著下降，夜间或雨天等场景下单一模态严重退化且激光雷达分支主导检测。本文面向双分支提案级检测器提出互补协同融合CCF，通过查询解耦损失、互补融合等组件为各模态提供独立监督并平衡贡献。实验证明该方法在跨域条件下取得更鲁棒的检测性能。该工作为模态退化与失配情形下的鲁棒融合提供了可借鉴的策略。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 1056, \"height\": 384}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 1056, \"height\": 384}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 2450, \"height\": 1050}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 1, \"index\": 4, \"width\": 2424, \"height\": 978}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 4, \"index\": 5, \"width\": 732, \"height\": 1093}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 4, \"index\": 6, \"width\": 1056, \"height\": 384}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 4, \"index\": 7, \"width\": 1056, \"height\": 384}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 4, \"index\": 8, \"width\": 1056, \"height\": 384}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 4, \"index\": 9, \"width\": 1056, \"height\": 384}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 4, \"index\": 10, \"width\": 1056, \"height\": 384}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 4, \"index\": 11, \"width\": 2400, \"height\": 1200}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 4, \"index\": 12, \"width\": 567, \"height\": 263}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 4, \"index\": 13, \"width\": 539, \"height\": 326}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 4, \"index\": 14, \"width\": 539, \"height\": 263}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 4, \"index\": 15, \"width\": 500, \"height\": 250}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 4, \"index\": 16, \"width\": 509, \"height\": 282}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 4, \"index\": 17, \"width\": 1056, \"height\": 384}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 5, \"index\": 18, \"width\": 541, \"height\": 264}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 5, \"index\": 19, \"width\": 449, \"height\": 280}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-020.webp\", \"caption\": \"\", \"page\": 5, \"index\": 20, \"width\": 468, \"height\": 467}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-021.webp\", \"caption\": \"\", \"page\": 5, \"index\": 21, \"width\": 482, \"height\": 280}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-022.webp\", \"caption\": \"\", \"page\": 8, \"index\": 22, \"width\": 1395, \"height\": 826}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-023.webp\", \"caption\": \"\", \"page\": 8, \"index\": 23, \"width\": 1395, \"height\": 826}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-024.webp\", \"caption\": \"\", \"page\": 8, \"index\": 24, \"width\": 1395, \"height\": 826}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-025.webp\", \"caption\": \"\", \"page\": 8, \"index\": 25, \"width\": 1395, \"height\": 826}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-026.webp\", \"caption\": \"\", \"page\": 8, \"index\": 26, \"width\": 1395, \"height\": 826}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-027.webp\", \"caption\": \"\", \"page\": 8, \"index\": 27, \"width\": 1395, \"height\": 826}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-028.webp\", \"caption\": \"\", \"page\": 8, \"index\": 28, \"width\": 1395, \"height\": 826}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-029.webp\", \"caption\": \"\", \"page\": 8, \"index\": 29, \"width\": 1395, \"height\": 826}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-ccf-complementary-collaborative-fusion-for-domain-generalized-multi-modal-3d-object-cvpr-2026-paper/fig-030.webp\", \"caption\": \"\", \"page\": 8, \"index\": 30, \"width\": 1395, \"height\": 826}]"
motivation: 多模态融合在跨域部署时性能大幅下降，挑战场景下单一模态退化且存在分支主导问题。
method: 提出查询解耦损失与互补协同融合等组件，为二维、三维及融合分支提供独立监督。
result: 在跨域实验中取得更鲁棒的多模态三维检测性能。
conclusion: 为模态退化与失配场景下的鲁棒融合提供了新方案。
---

## Abstract
Multi-modal fusion has emerged as a promising paradigm for accurate 3D object detection. However, performance degrades substantially when deployed in target domains different from training. In this work, focusing on dual-branch proposal-level detectors, we identify two factors that limit robust cross-domain generalization: 1) in challenging domains such as rain or nighttime, one modality may undergo severe degradation; 2) the LiDAR branch often dominates the detection process, leading to systematic underutilization of visual cues and vulnerability when point clouds are compromised. To address these challenges, we propose three components. First, Query-Decoupled Loss provides independent supervision for 2D-only, 3D-only, and fused queries, rebalancing gradient flow across modalities. Second, LiDAR-Guided Depth Prior augments 2D queries with instance-aware geometric priors through probabilistic fusion of image-predicted and LiDAR-derived depth distributions, improving their spatial initialization. Third, Complementary Cross-Modal Masking applies complementary spatial masks to the image and point cloud, encouraging queries from both modalities to compete within the fused decoder and thereby promoting adaptive fusion. Extensive experiments demonstrate substantial gains over state-of-the-art baselines while preserving source-domain performance. Code and models are publicly available at https://github.com/IMPL-Lab/CCF.git.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义

- **研究背景**：多模态 3D 目标检测融合 LiDAR 几何信息与相机语义信息，在标准 benchmark 上表现优异，但跨域部署时性能显著下降。真实环境中雨、夜、地理迁移等域偏移会导致传感器退化。
- **核心问题**：论文聚焦**双分支、提案级（proposal-level）多模态 3D 检测器**，指出跨域鲁棒性受两个因素限制：
  - 挑战域中某一模态可能严重退化，例如雨天 LiDAR 点稀疏、夜间图像质量下降；
  - LiDAR 分支在检测过程中占主导，视觉线索被系统性低利用，导致点云受损时整体性能脆弱。
- **整体含义**：作者将问题归结为**模态不平衡**，具体表现为 2D 查询监督不足、深度初始化不准、融合阶段 3D 查询主导。CCF 的目标是在域泛化设定下提升相机与 LiDAR 的平衡利用，同时保持源域性能。

## 2. 方法论：核心思想与关键技术

- **总体框架**：CCF 建立在 MV2DFusion 类双分支提案级融合框架上。2D 检测器生成图像提案，3D 检测器生成 LiDAR 提案，再转换为查询并由 Transformer 解码器融合。
- **核心思想**：从**监督、初始化、融合竞争**三个环节缓解模态不平衡。

### 2.1 Query Decoupled Loss（查询解耦损失）

- 问题：标准 Hungarian matching 中 3D 查询主导匹配，2D 查询获得监督极少。论文统计源域平均每样本匹配 9.375 个 3D 查询，但仅 0.25 个 2D 查询，比例约 37.5:1。
- 方法：使用三个**并行、权重共享**的解码器分支：
  - 2D-only 分支：只解码 2D 查询；
  - 3D-only 分支：只解码 3D 查询；
  - fused 分支：解码拼接后的 2D+3D 查询。
- 三个分支分别进行 Hungarian matching 和损失计算：
  - \( \mathcal{L}_{total} = \mathcal{L}_{2d} + \mathcal{L}_{3d} + \mathcal{L}_{fused} \)
  - 每项包含分类损失与框回归损失：\( \mathcal{L}_{(\cdot)} = \mathcal{L}_{cls} + \mathcal{L}_{box} \)
- 作用：避免 2D 查询在融合分支中“搭便车”依赖 3D 查询信息；推理时只使用 fused 分支，因此不增加推理计算量。

### 2.2 LiDAR-Guided Depth Prior（LiDAR 引导深度先验）

- 问题：2D 查询的 3D 定位依赖图像深度预测，域偏移下误差增大。论文报告源域深度 MAE 为 1.78 m，Rain 为 3.01 m，Night 为 2.27 m，Boston 为 2.55 m。
- 方法：对每个 2D 提案融合两种深度分布：
  - 图像分支输出学习到的深度分布 \(d_{2d} \in \mathbb{R}^D\)；
  - LiDAR 分支收集 2D 提案对应 3D 视锥内点，离散化为深度直方图 \(d_{3d}\)；若无视锥内点，则用均匀分布。
- 自适应融合：轻量置信网络预测实例级权重 \( \lambda_i \in [0,1] \)，在 log 空间进行 Product-of-Experts 式融合：
  - \( d_{fused}^i = \sigma(\lambda_i \cdot \log(d_{2d}^i) + (1-\lambda_i) \cdot \log(d_{3d}^i)) \)
- 融合后的期望深度用于初始化对应 2D 查询的 3D 参考点，提升其空间定位质量。

### 2.3 Complementary Cross-Modal Masking（互补跨模态掩码）

- 动机：真实域偏移中两模态退化往往不对称，例如雨天 LiDAR 受损而图像仍可提供语义，夜间图像退化而 LiDAR 仍提供几何。
- 方法：在图像平面生成空间掩码 \(M \in \{0,1\}^{H \times W}\)，将图像中被掩码像素置零；同时将 LiDAR 点投影到图像平面，只保留落在**互补区域**的点。投影公式为：
  - \( [u_i, v_i, 1]^\top \propto K(Rp_i + t) \)
- 掩码生成采用 GridMask，并使用课程学习，使掩码概率从 0 线性增加到 \(p=0.7\)。
- 作用：模拟局部模态退化，迫使融合解码器中来自两模态的查询相互竞争，促进自适应融合，而非固定依赖 LiDAR。

## 3. 实验设计

- **数据集 / 场景**：
  - 基于 **nuScenes** 构建域泛化 benchmark。
  - 源域：226 个新加坡晴天白天场景。
  - 目标域：Rain（27 场景）、Night（15 场景）、Boston（77 场景），分别覆盖天气、光照、地理迁移。
- **评价指标**：
  - mAP，在 10 个类别上平均；
  - NDS，nuScenes Detection Score，综合 mAP 与平移、尺度、方向、速度、属性误差。
- **实现配置**：
  - 基于 MV2DFusion，3D 提案生成器为 ISFusion，2D 提案生成器为 Faster R-CNN；
  - 6 层融合解码器；
  - 深度先验使用 D=25 个深度 bin，3 层 MLP 置信网络；
  - 互补掩码使用 GridMask，课程掩码概率从 0 到 0.7。
- **训练流程**：
  - Stage 1：2D 与 3D 提案生成器仅在源域预训练。2D 检测器使用源域 3D 标注投影得到的 2D 框训练，避免使用可能含目标域的 nuImages 预训练权重。
  - Stage 2：冻结 3D 提案生成器，训练融合解码器 24 epochs，batch size 16，AdamW，初始学习率 \(4 \times 10^{-4}\)，weight decay 0.01，cosine annealing。
- **对比方法**：
  - 主表对比 FSDv2、CMT、MOAD、MEFormer、ISFusion、MoME，以及自身 baseline。
  - Oracle 表还对比 BEVDet、PETR、CenterPoint、TransFusion-L、TransFusion、BEVFusion、GraphBEV、MV2DFusion 等。
- **主要结果**：
  - CCF 源域 mAP/NDS 为 68.2/65.9，基本保持源域性能。
  - 目标域 mAP/NDS：Rain 44.7/52.5，Night 44.2/45.3，Boston 50.6/56.8；平均 46.5/51.5。
  - 相对 baseline，mAP 提升：Rain +2.8，Night +1.3，Boston +3.2。
  - Oracle 设定下，All/Rain/Night 达到 73.6/74.2、72.9/74.5、46.9/48.3 mAP/NDS。

## 4. 资源与算力

- 论文**未明确说明**使用的 GPU 型号、数量、总训练时长或总计算量。
- 仅报告了训练相关超参数：Stage 2 训练 24 epochs、batch size 16、AdamW、初始学习率 \(4 \times 10^{-4}\)、weight decay 0.01、cosine annealing。
- 因此无法从论文文本判断实际算力开销与复现成本。

## 5. 实验数量与充分性

- **实验组数概览**：
  - 主跨域对比表：源域 + Rain/Night/Boston 三个目标域，多个基线方法。
  - Oracle 表：在 nuScenes 标准训练划分上训练，对比大量 2D/3D/多模态方法。
  - 组件消融表：Query Decoupled Loss、LiDAR-Guided Depth Prior、Complementary Cross-Modal Masking 的组合，共 8 组配置。
  - 掩码策略消融表：6 种变体，包括 Image GridMask、Modal Mask、Consistent GridMask、Complementary GridMask、Complementary RandomMask、加课程学习的 Complementary GridMask。
  - 还有 pilot study：2D 提案质量分析、监督匹配统计、深度误差分析，以及定性可视化。
- **充分性评价**：
  - 实验覆盖了多目标域、多基线、组件消融、掩码设计消融和 Oracle 上限分析，整体较充分。
  - 公平性方面，作者强调所有方法使用相同数据划分、训练流程和评价协议；两阶段训练避免目标域数据泄漏，2D 检测器不使用可能含目标域的 nuImages 预训练权重。
  - 但 Night 域只有 15 个场景，且部分类别缺失，虽然仍按 10 类报告，统计稳定性可能有限。
  - 未报告多次随机种子运行的均值/方差或显著性检验，因此结果稳定性证据有限。

## 6. 主要结论与发现

- 双分支提案级多模态检测器存在明显**模态不平衡
