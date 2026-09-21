---
title: Distribution-Aligned Multimodal Fusion for Robust Object Detection
title_zh: 面向鲁棒目标检测的分布对齐多模态融合
authors: "Hao, Xiaohui, Pu, Yanglin, Wang, Yongjun, She, Rui"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Hao_Distribution-Aligned_Multimodal_Fusion_for_Robust_Object_Detection_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 6.0
evidence: RGB-红外多模态融合与特征对齐用于鲁棒检测
tldr: 针对RGB-红外多模态目标检测在训练退化类型有限时泛化困难的问题，本文提出分布对齐框架。核心思想是将融合特征对齐到预训练检测器表现最优的分布，而非适应训练特有退化，仅训练轻量融合模块并冻结检测器，从而利用红外互补信息减少分布偏移。实验在三个基准上取得领先结果且训练快四倍，为多模态特征融合与对齐提供了有效思路。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-hao-distribution-aligned-multimodal-fusion-for-robust-object-detection-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 426, \"height\": 350}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-hao-distribution-aligned-multimodal-fusion-for-robust-object-detection-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 451, \"height\": 350}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-hao-distribution-aligned-multimodal-fusion-for-robust-object-detection-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 451, \"height\": 355}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-hao-distribution-aligned-multimodal-fusion-for-robust-object-detection-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 1, \"index\": 4, \"width\": 426, \"height\": 356}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-hao-distribution-aligned-multimodal-fusion-for-robust-object-detection-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 3, \"index\": 5, \"width\": 1992, \"height\": 1196}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-hao-distribution-aligned-multimodal-fusion-for-robust-object-detection-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 6, \"index\": 6, \"width\": 1359, \"height\": 1019}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-hao-distribution-aligned-multimodal-fusion-for-robust-object-detection-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 6, \"index\": 7, \"width\": 1359, \"height\": 1087}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-hao-distribution-aligned-multimodal-fusion-for-robust-object-detection-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 6, \"index\": 8, \"width\": 1359, \"height\": 1137}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-hao-distribution-aligned-multimodal-fusion-for-robust-object-detection-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 6, \"index\": 9, \"width\": 1359, \"height\": 1087}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-hao-distribution-aligned-multimodal-fusion-for-robust-object-detection-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 7, \"index\": 10, \"width\": 1976, \"height\": 1511}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-hao-distribution-aligned-multimodal-fusion-for-robust-object-detection-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 7, \"index\": 11, \"width\": 2572, \"height\": 1645}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-hao-distribution-aligned-multimodal-fusion-for-robust-object-detection-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 7, \"index\": 12, \"width\": 2454, \"height\": 1804}]"
motivation: RGB-红外检测在训练数据退化类型有限时存在严重的跨退化泛化问题。
method: 冻结预训练检测器，仅训练轻量融合模块，将融合特征对齐到预训练分布。
result: 在三个基准上取得领先结果，训练速度提升约四倍。
conclusion: 证明对齐预训练分布可有效提升多模态检测鲁棒性。
---

## Abstract
Cross-degradation generalization remains a critical challenge for RGB-infrared multimodal object detection, especially when training data covers limited degradation types. This paper presents a distribution alignment framework with a key insight: aligning fused features to the pretrained distribution where the frozen detector performs optimally, rather than adapting to training-specific degradations. By freezing the pretrained detector and training only a lightweight fusion module, our approach leverages complementary infrared information to reduce distribution shift while maintaining computational efficiency. The method achieves state-of-the-art results on three benchmarks with 4x faster training. Critically, we demonstrate that aligning to the pretrained distribution substantially outperforms aligning to training degradations when generalizing to unseen scenarios.

---

## 论文详细总结（自动生成）

# 论文总结：面向鲁棒目标检测的分布对齐多模态融合

## 1. 核心问题与整体含义（研究动机与背景）

- **研究背景**：RGB-红外（RGB-IR）多模态目标检测在自动驾驶、安防监控等安全关键场景中至关重要。RGB 相机在过曝、欠曝、夜间等挑战性光照条件下性能严重退化，而红外相机对光照变化不敏感，可提供互补信息。
- **核心问题**：现有融合方法在极端场景下仍面临重大挑战——当**训练数据仅覆盖有限退化类型**时，模型难以泛化到**未见过的退化类型**（如仅用"过曝"数据训练，却需应对夜间、模糊等场景）。
- **关键洞察**：作者发现，多模态融合的**优化目标选择至关重要**。现有方法隐式地让模型去拟合训练数据分布（可能包含退化特定模式），导致对训练退化过拟合；而本文主张应显式地将融合特征**对齐到预训练检测器表现最优的"正常分布"** $P_{normal}$，而非适应训练特有的退化分布。
- **整体含义**：论文证明了对齐预训练分布比对齐训练退化分布能带来显著更好的跨退化泛化能力，同时通过冻结检测器、仅训练轻量融合模块，将训练时间从 14–17 小时降至 3.5 小时。

## 2. 方法论

### 2.1 核心思想
- 将多模态融合问题建模为**分布偏移修正**问题：退化场景下 RGB 特征偏离预训练分布 $P_{normal}$，导致冻结检测器决策边界失效。利用红外互补信息，学习一个融合函数 $\mathcal{M}$，使融合特征 $P_{fused} = P(\mathcal{M}(F_{rgb}, F_{ir}))$ 尽可能接近 $P_{normal}$。
- **对齐目标三选一**：(1) 端到端适配检测器；(2) 对齐到训练退化分布 $P_{degraded}$；(3) **对齐到正常分布 $P_{normal}$（本文选择）**。基于迁移学习理论，当训练退化类型有限时，对齐 $P_{normal}$ 泛化更好。

### 2.2 关键技术细节

**两阶段流程**：

- **Stage 1（离线）——预训练分布建模**：
  - 用冻结的 ViT 编码器提取正常验证集（5k 图像，亮度 ∈ [0.3, 0.7]、对比度 > 0.4）的 [CLS] token 特征。
  - 用 **GMM（高斯混合模型）** 建模 $P_{normal}$，K 个分量，参数 $\{w_k, \mu_k, \Sigma_k\}$ 经 EM 算法估计，采用对角协方差将参数量从 $O(Kd^2)$ 降至 $O(Kd)$。
  - 用 k-means++ 初始化均值，BIC 选择 K（默认 K=8），最多 100 次迭代，tol=1e-4。
  - 梯度公式：$\nabla_{F_{cls}} \log p_{normal}(F_{cls}) = \sum_k \gamma_k(F_{cls}) \Sigma_k^{-1}(\mu_k - F_{cls})$，将特征拉向最近的 GMM 分量。

- **Stage 2（在线）——融合训练**：
  - 冻结整个检测器（ViT 编码器 + DETR 解码器，共 86M 参数），仅训练融合模块（13M 参数）。
  - 损失函数：$\mathcal{L} = \mathbb{E}[-\log p_{normal}(F_{cls}^{rect}) + \lambda \mathcal{L}_{det}(H(F_{rect}), Y)]$，其中 λ=0.5 平衡对齐损失与检测损失。

**融合模块架构**（输入 RGB/IR patch token 特征 $F \in \mathbb{R}^{N \times d}$，N=197，d=768）：
1. **跨模态注意力**：8 头交叉注意力（每头 dk=96），带残差连接，双向增强（RGB 查询 IR，IR 查询 RGB）。
2. **自适应 Token 门控**：拼接增强特征后，经 MLP（Linear 2d→d→2d）+ Sigmoid 生成通道级门控，动态加权模态贡献。
3. **特征融合**：MLP（Linear 2d→4d→d）投影回原维度，输出 $F_{rect} \in \mathbb{R}^{N \times d}$。

## 3. 实验设计

### 3.1 数据集与场景
- **LLVIP**：15,488 对，行人检测。
- **FLIR**：10,228 对，车辆检测。
- **DroneVehicle**：28,439 对，无人机航拍。
- 评估指标：IoU=0.5 下的 mAP，并分别评估正常 vs. 挑战场景（过曝、欠曝、夜间）。

### 3.2 Benchmark 与对比方法
- 统一在 **ViT-Base + DETR** 检测器上实现所有方法以保证公平。
- 对比方法涵盖：
  - **简单基线**：Concat、Add。
  - **注意力方法**：CBAM、SENet、MMTM。
  - **SOTA 端到端方法**：CFT、ICAFusion、CALNet、C2Former、M2FNet、CFMW。
  - **先进融合方法**：CrossFormer、LRAFNet、RSDet。
- 报告 3 次运行的均值 ± 标准差，并做 p<0.01 显著性检验。

### 3.3 主要实验组
- 主性能对比（表 1，三个数据集）。
- 挑战场景细分（表 2，LLVIP 过曝/欠曝/夜间）。
- 对齐目标对比（表 3，仅用过曝训练，测试夜间/模糊）。
- 跨退化泛化（表 4，过曝训练，测试欠曝/夜间/模糊）。
- 组件消融（表 5）。
- 端到端对比（表 6）。
- 对齐指标量化（表 7，Wasserstein 距离、负对数似然）。
- t-SNE 特征可视化（图 5）与逐维度分布分析（图 6）。
- 训练动态曲线（图 4）。

## 4. 资源与算力

- **硬件**：AMD EPYC 7532 CPU、**NVIDIA RTX 4090 GPU（24GB）**、2TB SSD。
- **训练配置**：AdamW 优化器（lr=1e-4，wd=1e-4），30 epochs，batch size 8，λ=0.5。
- **训练时长**：本文方法 **3.5 小时**，对比 SOTA 端到端方法 14–17 小时，先进融合方法约 4 小时。
- **GMM 拟合开销**：一次性约 10 分钟，相对训练时间可忽略。
- **模型规模**：融合模块 13M 可训练参数（跨模态注意力 4.7M、自适应门控 2.4M、融合 MLP 7.1M），冻结检测器 86M 参数。
- **说明**：文中未明确提及使用的 GPU 数量，仅提及单张 RTX 4090；也未说明是否使用多卡并行训练。

## 5. 实验数量与充分性

- **实验组数**：约 7 类主要实验（3 个数据集主实验、场景细分、对齐目标对比、跨退化泛化、组件消融、E2E 对比、对齐量化验证），加上可视化分析（t-SNE、逐维度分布）。
- **充分性评价**：
  - **优点**：覆盖 3 个不同域的数据集（行人/车辆/航拍），验证了方法的通用性；对齐目标对比实验设计巧妙，直接验证了核心假设；消融实验逐步添加组件，清晰展示各模块贡献；对齐指标（W2、-log p）与 mAP 的相关性分析提供了定量证据。
  - **公平性**：所有对比方法统一在相同 ViT-Base + DETR 检测器上实现，参数计数和训练时间在同一设置下测量，3 次运行报告均值 ± 标准差并做显著性检验，较为客观。
  - **潜在不足**：GMM 的 K 值选择、正常样本的筛选标准（亮度/对比度阈值）可能对结果有影响，但文中未提供这些超参数的敏感性分析；跨退化实验仅在"过曝训练"这一种设定下进行，其他训练退化类型（如夜间、模糊）是否同样成立未验证。

## 6. 主要结论与发现

- **核心结论**：**对齐目标的选择决定了泛化能力**。对齐到预训练分布 $P_{normal}$ 在未见退化场景上显著优于对齐到训练退化分布 $P_{degraded}$ 或端到端训练。
- **性能表现**：在 LLVIP（98.1%）、FLIR（79.5%）、DroneVehicle（57.8%）三个基准上均达到 SOTA，且训练时间从 14–17 小时降至 3.5 小时（快约 4 倍）。
- **场景分析**：改进在**挑战场景（过曝/欠曝）上最为显著**，而正常场景提升较小；夜间场景因红外热特征稳定，提升相对较小。
- **机制解释**：对齐 $P_{degraded}$ 在 epoch 15 左右出现平台期，表明对有限退化模式过拟合；对齐 $P_{normal}$ 收敛更一致，最终对齐损失最低。
- **对齐验证**：t-SNE 和逐维度分析显示融合特征被拉回 $P_{normal}$；约 10% 特征未能完美对齐，但检测性能已显著提升，说明减少分布散度足以改善泛化。

## 7. 优点

- **洞察深刻**：明确指出现有方法隐式拟合训练退化分布的缺陷，提出"对齐预训练分布"这一简洁而有效的设计原则，具有理论依据（迁移学习）。
- **方法简洁高效**：冻结 86M 检测器、仅训练 13M 融合模块，训练时间减少约 4 倍，且无需重新设计检测器架构。
- **GMM 建模设计合理**：对角协方差降低参数量，闭合梯度便于优化，K 个分量可捕获多模态场景结构。
- **实验设计严谨**：对齐目标对比实验直接验证核心假设；跨退化泛化实验（过曝训练→夜间/模糊测试）设计巧妙；统一 backbone 保证公平对比。
- **可解释性强**：通过 t-SNE、逐维度分布、Wasserstein 距离等多角度可视化对齐效果。
- **模块化设计**：方法可与更强预训练检测器或替代分布模型结合，具有良好的扩展性。

## 8. 不足与局限

- **依赖预训练检测器质量**：方法假设预训练检测器在正常场景下表现良好，若预训练模型本身质量不足，对齐效果受限。
- **GMM 假设的局限**：假设特征分布可用 GMM 近似，当分布高度复杂或多峰非高斯时可能不准确。
- **极端退化场景**：当所有模态同时严重退化时，互补信息有限，方法效果可能下降。
- **实验覆盖**：
  - 跨退化实验仅在"过曝训练"设定下验证，未涵盖其他训练退化类型。
  - 未提供 GMM 超参数（K 值、正常样本筛选阈值）的敏感性分析。
- **算力说明不完整**：未明确 GPU 使用数量，难以准确评估总计算资源。
- **应用限制**：GMM 需针对每个目标域重新离线拟合（约 10 分钟），跨域部署时需额外开销。
- **偏差风险**：正常样本的亮度/对比度筛选标准可能引入人为偏差，"正常"的定义与预训练分布之间的差距未充分讨论。

（完）
