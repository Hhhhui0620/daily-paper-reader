---
title: "Disentangle-then-Align: Non-Iterative Hybrid Multimodal Image Registration via Cross-Scale Feature Disentanglement"
title_zh: 先解耦再对齐：基于跨尺度特征解耦的非迭代混合多模态图像配准
authors: "Zhang, Chunlei, Xia, Jiahao, Xiao, Yun, Jiang, Bo, Zhang, Jian"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Zhang_Disentangle-then-Align_Non-Iterative_Hybrid_Multimodal_Image_Registration_via_Cross-Scale_Feature_Disentanglement_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 7.0
evidence: 处理全局错位与局部形变的混合多模态配准
tldr: 该文针对多模态图像配准中共享特征空间受模态私有信息泄漏、且多尺度框架仅支持单一变换类型的问题展开研究。作者将混合多模态配准建模为同时学习稳定共享特征空间与统一混合变换，并提出跨尺度特征解耦的非迭代对齐方法。实验表明该方法能同时应对全局错位与局部形变。该工作对未配准多模态图像的对齐具有直接的方法借鉴价值。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-disentangle-then-align-non-iterative-hybrid-multimodal-image-registration-via-cross-scale-feature-disentanglement-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 8, \"index\": 1, \"width\": 1716, \"height\": 968}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-disentangle-then-align-non-iterative-hybrid-multimodal-image-registration-via-cross-scale-feature-disentanglement-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 8, \"index\": 2, \"width\": 1364, \"height\": 1144}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-disentangle-then-align-non-iterative-hybrid-multimodal-image-registration-via-cross-scale-feature-disentanglement-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 8, \"index\": 3, \"width\": 1364, \"height\": 1144}]"
motivation: 多模态配准中共享特征易受模态私有信息泄漏影响，且单一变换类型难以兼顾全局与局部错位。
method: 将混合配准建模为联合学习稳定共享特征空间与统一混合变换，并进行跨尺度特征解耦。
result: 实验显示方法可同时处理全局错位与局部形变，配准精度更高。
conclusion: 稳定的共享特征空间与混合变换为未配准多模态对齐提供了有效途径。
---

## Abstract
Multimodal image registration is a fundamental task and a prerequisite for downstream cross-modal analysis. Despite recent progress in shared feature extraction and multi-scale architectures, two key limitations remain. First, some methods use disentanglement to learn shared features but mainly regularize the shared part, allowing modality-private cues to leak into the shared space. Second, most multi-scale frameworks support only a single transformation type, limiting their applicability when global misalignment and local deformation coexist. To address these issues, we formulate hybrid multimodal registration as jointly learning a stable shared feature space and a unified hybrid transformation. Based on this view, we propose HRNet, a Hybrid Registration Network that couples representation disentanglement with hybrid parameter prediction. A shared backbone with Modality-Specific Batch Normalization (MSBN) extracts multi-scale features, while a Cross-scale Disentanglement and Adaptive Projection (CDAP) module suppresses modality-private cues and projects shared features into a stable subspace for matching. Built on this shared space, a Hybrid Parameter Prediction Module (HPPM) performs non-iterative coarse-to-fine estimation of global rigid parameters and deformation fields, which are fused into a coherent deformation field. Extensive experiments on four multimodal datasets demonstrate state-of-the-art performance on rigid and non-rigid registration tasks. The code is available at the project website.

---

## 论文详细总结（自动生成）

# 论文总结：Disentangle-then-Align（HRNet）

## 1. 核心问题与研究动机

- **任务背景**：多模态图像配准是跨模态分析的基础前提。由于不同成像机制导致显著的跨模态外观差异（appearance gap），加之视角差异带来的几何错位，配准难度较大。
- **两大关键局限**：
  - **共享空间泄漏**：现有基于解耦的方法主要对共享部分施加正则化，缺乏对模态私有子空间边界与独立性的显式约束，导致模态私有线索（外观/噪声）回流到共享空间，干扰几何对应。
  - **单一变换类型**：多数多尺度框架只支持一种变换（纯刚性或纯非刚性）。刚性可校正全局错位但无法处理局部形变；非刚性适应局部变化但在大全局偏移下表现差且可能破坏结构完整性。
- **混合配准的现状问题**：已有混合方法多为"刚性阶段 + 非刚性阶段"的**串行级联**，存在两个弊端：(1) 两种变换在**不同表示空间**中估计，难以协调成统一的混合形变；(2) 阶段间耦合弱，后续预测会继承前序偏差，累积形变伪影。
- **整体含义**：论文将混合多模态配准重新建模为**联合学习一个稳定的共享特征空间 + 一个统一的混合变换**，提出"先解耦再对齐（disentangle-then-align）"的通用模板，实现非迭代、单次前向的混合配准。

## 2. 方法论（HRNet）

### 核心思想
HRNet 由三部分组成：**共享编码器（含 MSBN）→ CDAP 解耦模块 → HPPM 混合参数预测模块**。采用"先提取再解耦（extract-then-disentangle）"策略，确保刚性/非刚性预测始终在**同一共享特征空间**中进行。

### 关键技术细节

- **共享骨干 + 模态特定批归一化（MSBN）**：
  - 卷积权重跨模态共享以学习几何共性；BN 的均值、方差与仿射参数**按模态分别维护**，用于吸收外观/辐射差异。
  - 输出多尺度特征 $\{F_0,\dots,F_4\}$、$\{M_0,\dots,M_4\}$（共 5 个尺度）。

- **跨尺度解耦与自适应投影（CDAP）**：遵循 **Decompose → Gate → Project** 流水线。
  - **Decompose**：每个尺度用两个提取器将特征分解为共享分量 $F^s_i$/$M^s_i$（跨模态共享卷积权重）与私有分量 $F^p_i$/$M^p_i$。
  - **Gate**：采用**层间解耦注意力（ILDA）**，利用相邻尺度的语义构造 Query/Key/Value 三元组，做跨尺度注意力引导门控，计算门控系数 $\varepsilon^s_i$、$\varepsilon^p_i$，抑制私有信息泄漏：$\tilde{F}^s_i = \varepsilon^s_i \odot F^s_i - \varpi_i \varepsilon^p_i \odot F^p_i$（$\varpi_i \to 0$）。
  - **Project**：**动态共享子空间（DSS）** 投影，输入自适应地生成近似正交基 $W^s_i$，将共享特征投影到低维稳定子空间：$\hat{F}^s_i = \tilde{F}^s_i W^{s\top}_i$。

- **混合参数预测模块（HPPM）**：
  - 基于 **Mamba 状态空间架构**（RSSB 块，$q=2$）以低计算代价建模长程依赖。
  - **非迭代、由粗到细**：最粗尺度先预测全局刚性参数并编码为粗流场；后续尺度将上一尺度变换上采样并用于扭曲移动特征，逐尺度累积增量：$\omega_3 = \text{upsample}(\omega_4) + \omega^{\leftrightarrow}_3$。
  - **混合配准块（HRB）**：包含刚性头（全局平均池化 + 两层全连接，输出低维参数 $H$）与非刚性头（3×3 卷积堆叠，输出稠密形变场）。
  - 实现上共 5 个尺度：最粗 1 个做刚性，其余 4 个做非刚性细化，最终融合为**单一相干形变场**。

- **损失函数**：
  - 配准损失：$L_r$（刚性参数+重投影误差）、$L_n$（非刚性形变场+图像误差）、$L_s$（形变场平滑）。
  - 解耦损失：$L_{ccd}$（跨协方差去相关，降低共享-私有耦合）、$L_{bo}$（基正交性，避免子空间退化）、$L_{cs}$（跨尺度方向一致性）、$L_{tri}$（三元组损失，拉近跨模态共位特征、推开私有干扰）。
  - 总损失为各加权项之和。

## 3. 实验设计

- **数据集 / 场景**（4 个多模态数据集）：
  - **RGB–TIR**：TBBR 数据集（3000 训练 / 300 测试）。
  - **RGB–NIR**：RGB-NIR Scene 数据集（裁剪生成 3000 训练 / 300 测试）。
  - **RGB–IR** 与 **RGB–SAR**：MRSR 数据集（各 3500 训练，其余测试）。
- **评价指标（benchmark）**：重投影误差（RE）与归一化相关系数（NCC），遵循文献 [21,22]。
- **对比方法**：
  - 刚性任务：IHN、InMIRNet、RHWF、SCPNet、MCNet、MMRNet。
  - 非刚性任务：SuperFusion、InMIRNet、MMRNet、NBRNet、ADRNet。
- **训练设置**：图像统一 resize 至 256×256；刚性变换生成范围（旋转 ±20°、平移 ±15%、缩放 ±13%）；非刚性附加形变度 140、高斯平滑半径 35；采用**三阶段课程学习**（warmup 10% / mid 50% / late 40%）动态调整损失权重。

## 4. 资源与算力

- 论文明确提到：**PyTorch 实现，单张 NVIDIA L40 GPU 训练**。
- 优化器 Adam，学习率 1e-4，batch size 8，训练 100 epochs。
- **未明确说明**：GPU 数量（文中只提一张 L40）、总训练时长、参数量、FLOPs 等效率指标均未报告。

## 5. 实验数量与充分性

- **主要对比实验**：刚性任务（表 2）与非刚性任务（表 3），各在 4 个数据集上对比 5–6 个方法。
- **消融实验**：
  - 模块消融（MSBN、CDAP，表 4，在 RGB-TIR / RGB-SAR 上）。
  - 损失消融（逐步加入 $L_{ccd}$、$L_{bo}$、$L_{cs}$、$L_{tri}$，表 5）。
  - 参数选择（刚性/非刚性步数配比 $N_{rigid}$:$N_{nonrigid}$，表 6）。
  - 定性对比（图 4、图 5）；特征分布分析（CKA 图 6、t-SNE 图 7）。
- **充分性与公平性评估**：
  - **优点**：覆盖 4 个数据集 × 2 类任务 × 多种基线，消融维度较完整（模块、损失、超参），有定量+定性+特征可视化，实验较充分。
  - **可商榷点**：消融实验仅在 2 个数据集上进行（非全部 4 个）；未报告参数量/推理时间/显存等效率对比，无法判断 SOTA 是否以更高计算代价换取；训练数据由合成变换生成，与真实配准场景存在域差。

## 6. 主要结论与发现

- HRNet 在全部 4 个数据集、刚性与非刚性任务上均取得 **SOTA**（最低 RE、最高 NCC）。
- 刚性任务：相比强基线 MMRNet，RE 分别降低 **75.3%（RGB-NIR）、69.9%（RGB-TIR）、86.9%（RGB-IR）、55.3%（RGB-SAR）**，平均约 72% 相对提升。
- 非刚性任务：相比混合方法 ADRNet，RE 降低 61.2% / 62.5% / 66.9% / 23.3%；相比最强非混合基线 MMRNet 降低 56.7% / 23.4% / 73.9% / 17.0%。
- 消融表明：MSBN 在 RGB-TIR / RGB-SAR 上带来约 19.5% / 9.0% 的 RE 降低，CDAP 贡献 9.5% / 7.2%；四项解耦损失互补增益。
- 参数选择结论：**1 个刚性步 + 4 个非刚性步**（总步数 5）最优，说明一步刚性足以校正全局位姿，多步非刚性有利于局部细化。
- 特征分析：MSBN 使跨模态 CKA 更高（尤其在浅层）；CDAP 使共享分量跨模态高度重叠、私有分量彼此分离，证明泄漏被抑制。

## 7. 优点

- **统一框架创新**：将刚性与非刚性在**同一共享特征空间、同一非迭代粗到细流水线**中联合估计，克服串行级联的表示割裂与误差累积。
- **解耦更彻底**：不仅正则化共享部分，还通过 decompose-gate-project 显式约束私有子空间边界，并用三种结构化正则（去相关、正交基、跨尺度一致性）塑造共享空间。
- **轻量高效的长程建模**：引入 Mamba/SSM 结构，在低计算成本下捕获长程依赖。
- **工程可用性**：单次前向非迭代，代码开源；MSBN 引入的额外开销可忽略。
- **实验覆盖较广**：自然场景（RGB-TIR、RGB-NIR）与遥感场景（RGB-IR、RGB-SAR）兼顾，定量、定性、特征可视化多角度验证。

## 8. 不足与局限

- **效率指标缺失**：未报告参数量、FLOPs、推理速度、显存占用，难以评估相对于基线的实际部署成本。
- **消融覆盖不全**：模块与损失消融仅在 RGB-TIR / RGB-SAR 两个数据集上，未覆盖 RGB-NIR / RGB-IR。
- **训练数据依赖合成变换**：刚性与非刚性变换由人工参数生成（旋转/平移/缩放 + 形变度 140、高斯半径 35），与真实多模态配准中的复杂形变存在差距，可能带来域偏移风险。
- **算力说明不完整**：仅提及单张 L40，未说明训练时长与总计算量。
- **应用限制**：论文聚焦 2D 图像配准，未验证三维、多视角或任务感知场景；作者在结论中也承认这些是未来工作方向。
- **潜在偏差风险**：对比方法均在同一合成数据协议下评估，若某些基线原设计不针对此类数据，可能低估其真实能力。

（完）
