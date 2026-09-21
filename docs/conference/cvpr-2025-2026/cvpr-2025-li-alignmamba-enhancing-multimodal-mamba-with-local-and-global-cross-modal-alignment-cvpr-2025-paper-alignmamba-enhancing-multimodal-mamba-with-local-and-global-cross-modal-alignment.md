---
title: "AlignMamba: Enhancing Multimodal Mamba with Local and Global Cross-modal Alignment"
title_zh: AlignMamba：以局部与全局跨模态对齐增强多模态Mamba
authors: "Li, Yan, Xing, Yifei, Lan, Xiangyuan, Li, Xin, Chen, Haifeng, Jiang, Dongmei"
date: 2025
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2025/papers/Li_AlignMamba_Enhancing_Multimodal_Mamba_with_Local_and_Global_Cross-modal_Alignment_CVPR_2025_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 7.0
evidence: 面向融合的局部与全局跨模态对齐
tldr: 跨模态对齐对多模态表征融合至关重要，但Transformer计算代价高，Mamba的顺序扫描又难以全面建模跨模态关系。本文提出AlignMamba，基于最优传输设计局部跨模态对齐模块并结合全局对齐实现高效融合。实验表明其在效率与效果上均具优势，为可见光-热红外等多模态对齐任务提供了可迁移的骨干方法。
source: CVPR-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-li-alignmamba-enhancing-multimodal-mamba-with-local-and-global-cross-modal-alignment-cvpr-2025-paper/fig-001.webp\", \"caption\": \"\", \"page\": 2, \"index\": 1, \"width\": 1432, \"height\": 802}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-li-alignmamba-enhancing-multimodal-mamba-with-local-and-global-cross-modal-alignment-cvpr-2025-paper/fig-002.webp\", \"caption\": \"\", \"page\": 7, \"index\": 2, \"width\": 3053, \"height\": 1163}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-li-alignmamba-enhancing-multimodal-mamba-with-local-and-global-cross-modal-alignment-cvpr-2025-paper/fig-003.webp\", \"caption\": \"\", \"page\": 7, \"index\": 3, \"width\": 3095, \"height\": 1169}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-li-alignmamba-enhancing-multimodal-mamba-with-local-and-global-cross-modal-alignment-cvpr-2025-paper/fig-004.webp\", \"caption\": \"\", \"page\": 8, \"index\": 4, \"width\": 1745, \"height\": 325}]"
motivation: Transformer跨模态对齐计算代价高，Mamba顺序扫描难以全面建模跨模态关系。
method: 提出AlignMamba，基于最优传输设计局部跨模态对齐并辅以全局对齐实现高效融合。
result: 在效率与效果上均优于现有方法，验证了对齐模块的有效性。
conclusion: 为多模态特征对齐与融合提供了可迁移的高效骨干。
---

## Abstract
Cross-modal alignment is crucial for multimodal representation fusion due to the inherent heterogeneity between modalities. While Transformer-based methods have shown promising results in modeling inter-modal relationships, their quadratic computational complexity limits their applicability to long-sequence or large-scale data. Although recent Mamba-based approaches achieve linear complexity, their sequential scanning mechanism poses fundamental challenges in comprehensively modeling cross-modal relationships. To address this limitation, we propose AlignMamba, an efficient and effective method for multimodal fusion. Specifically, grounded in Optimal Transport, we introduce a local cross-modal alignment module that explicitly learns token-level correspondences between different modalities. Moreover, we propose a global cross-modal alignment loss based on Maximum Mean Discrepancy to implicitly enforce the consistency between different modal distributions. Finally, the unimodal representations after local and global alignment are passed to the Mamba backbone for further cross-modal interaction and multimodal fusion. Extensive experiments on complete and incomplete multimodal fusion tasks demonstrate the effectiveness and efficiency of the proposed method. For instance, on the CMU-MOSI dataset, AlignMamba improves classification accuracy by 0.9%, reduces GPU memory usage by 20.3%, and decreases inference time by 83.3%.

---

## 论文详细总结（自动生成）

# AlignMamba 论文总结

## 1. 核心问题与整体含义

- **研究背景**：多模态表征融合（音频、视频、语言）是视觉-语言理解、音视频分析等任务的基础，但模态间的固有异质性（统计特性与特征分布差异）使跨模态对齐与融合成为核心挑战。
- **现有方法的局限**：
  - **Transformer 类方法**（单流/多流）虽能建模跨模态关系，但注意力机制的二次复杂度使其难以处理长序列或大规模数据。
  - **Mamba 类方法**（基于状态空间模型 SSM）具备线性复杂度，但其**顺序扫描机制**难以全面建模跨模态关系，尤其对未被扫描到的 token 难以建立对应关系，导致对齐信息缺失、融合表征质量受限。
- **论文含义**：作者提出 **AlignMamba**，通过引入局部与全局双重跨模态对齐信息来增强多模态 Mamba，在保持线性效率的同时提升融合效果，兼顾“有效性”与“效率”。

## 2. 方法论

### 2.1 核心思想
- 在对特征送入 Mamba 主干之前，先对单模态特征做**双重对齐**：
  - **局部对齐**：基于最优传输（OT），显式学习 token 级跨模态对应关系。
  - **全局对齐**：基于最大均值差异（MMD），隐式约束不同模态的分布一致性。
- 对齐后的特征再经 Mamba 主干做跨模态交互与融合，形成“先对齐、后融合”的范式。

### 2.2 关键技术细节

**（1）基于 OT 的局部跨模态对齐**
- 将各模态特征序列（音频 $X_a$、视频 $X_v$、语言 $X_l$）视为离散分布，求解传输矩阵 $M$ 以最小化传输代价。
- 代价矩阵采用**余弦距离**：$C(i,j)=1-\frac{X_i\cdot X_j}{\|X_i\|\|X_j\|}$，兼顾角度关系与数值稳定性。
- 为降低计算开销，采用**松弛形式**（去除 incoming 和约束），仅保留 outgoing 归一化约束，使解退化为“每个源 token 匹配代价最小的目标 token”，即 $M(i,j)=1/T_v$（当 $j$ 为最小代价目标），否则为 0。
- 对齐后特征由传输矩阵转置与原始特征相乘得到：$\tilde{X}_v=M_{v2l}^\top X_v$，$\tilde{X}_a=M_{a2l}^\top X_a$，从而将音视频对齐到语言模态的序列长度。

**（2）基于 MMD 的全局跨模态对齐**
- 使用高斯核 $k(x,y)=\exp(-\|x-y\|_2^2/2\sigma^2)$，在再生核希尔伯特空间（RKHS）中计算模态分布差异。
- 全局对齐损失为各对齐模态与语言模态之间 MMD 平方距离之和：
  $\mathcal{L}_{align}=\text{MMD}^2(\tilde{X}_v,X_l)+\text{MMD}^2(\tilde{X}_a,X_l)$。

**（3）Mamba 融合与优化**
- 采用**时间优先的交错扫描策略**构建统一序列：$X_{mm}=[\tilde{X}_a^1,\tilde{X}_v^1,X_l^1,\tilde{X}_a^2,\tilde{X}_v^2,X_l^2,\dots]$，使同一时刻的多模态特征被顺序处理，便于选择性扫描捕获模态内与模态间依赖。
- 总损失：$\mathcal{L}=\mathcal{L}_{task}+\lambda\mathcal{L}_{align}$，端到端联合优化，$\lambda$ 为平衡超参数。

## 3. 实验设计

- **数据集/场景**：
  - **CMU-MOSI** 与 **CMU-MOSEI**，均为视频片段，含视觉（面部表情）、声学（语音）、文本（转写）三模态，标注 -3 到 +3 的情感分数，二分类为正面/负面。
  - 两类场景：**完整多模态融合**（训练与推理时所有模态可用）与**不完整多模态融合**（推理时部分模态缺失，缺失率 MR 为 10%–70%）。
- **评价指标**：二分类准确率（Accuracy）与二分类 F1。
- **对比方法**：
  - 完整融合：LSTM 类（ICCN、MISA、MMIM）、跨模态 Transformer 类（MulT、Self-MM、DMD）、对比学习类（HyCon、ConFEDE、MTMD）等，共 14 个基线。
  - 不完整融合：模态恢复类（MCTN、MMIN、GCNet、IMDer）与非恢复类（DCCA、DCCAE）。
  - 效率对比：单流与多流 Transformer。
- **Benchmark**：以 CMU-MOSI/MOSEI 上的准确率/F1 为效果基准，以 GPU 显存、推理时间、FLOPs 为效率基准。

## 4. 资源与算力

- **论文文本中未明确说明**所使用的 GPU 型号、数量、训练时长或总训练算力。
- 仅提及效率实验中所有对比方法在“相同条件下”运行，并统计了 50 次推理的平均时间，但未给出具体硬件配置与训练成本。**这是一个信息缺口**。

## 5. 实验数量与充分性

- **实验规模**：
  - 2 个数据集 × 2 类场景（完整/不完整）× 7 种缺失率。
  - 效率分析 3 项（显存、推理时间、FLOPs），覆盖多种序列长度。
  - 消融实验 3 组：组件分析（去局部/去全局/两者都去）、融合方式对比（单流/多流 Mamba）、模态消融（去音频/去视频/去语言）。
  - 进一步分析：A-distance 量化模态差异、OT 传输计划定性可视化。
- **充分性与公平性**：
  - 整体实验较充分，覆盖效果、效率、消融、对齐可解释性多个维度。
  - 与大量 SOTA 方法对比，且效率实验在统一条件下进行，公平性较好。
  - 但消融/超参分析相对有限（如 $\lambda$、核带宽 $\sigma$ 的敏感性未系统探讨），且仅在情感分析任务上验证。

## 6. 主要结论与发现

- **效果**：AlignMamba 在两个数据集上均取得最优效果。CMU-MOSI 准确率 86.9%（较前方法提升 0.9%），CMU-MOSEI 86.6%。
- **不完整融合**：在 MOSI 上平均准确率 79.9%，较前方法提升 1.2%；且随缺失率上升性能下降更小（MOSI 仅降 11.9%，优于 MMIN 的 19.0% 和 IMDer 的 13.0%），鲁棒性更强。
- **效率**：处理 6.4k token 时显存仅 8.53 GB，较单流/多流 Transformer 分别降低 20.3% 和 58.0%；推理时间 6.05s，分别降低 83.3% 和 87.6%；FLOPs 仅 46.7G，较单流降低 54%、较多流降低 77%。
- **对齐有效性**：A-distance 显著下降（如 MOSI 上音频-语言从 1.68 降至 1.59），说明双重对齐有效缩小模态差距。
- **消融结论**：局部 OT 对齐比全局 MMD 对齐贡献更大（MOSI 上去除分别降 2.3% 和 1.1%）；朴素单流/多流 Mamba 均不如本方法，说明 Mamba 原生扫描不足以完成有效跨模态融合；语言模态最关键，移除后性能大幅下降。

## 7. 优点

- **问题定位清晰**：明确指出 Mamba 顺序扫描在跨模态对齐上的结构性缺陷，动机具有说服力。
- **方法设计互补**：局部 OT（显式 token 级对应）+ 全局 MMD（隐式分布一致性），从不同粒度形成互补，且 OT 传输矩阵具有可解释性。
- **效率与效果兼顾**：在保持线性复杂度的同时刷新 SOTA，显存、时间、FLOPs 均显著优于 Transformer 基线。
- **验证场景全面**：同时覆盖完整与不完整融合，并系统评估效率、消融、模态差异与可解释性。
- **工程可迁移性**：时间优先交错扫描与双重对齐机制较通用，可迁移至其他多模态对齐/融合任务。

## 8. 不足与局限

- **任务覆盖有限**：实验仅在 CMU-MOSI/MOSEI 两个情感分析数据集上验证，缺少视觉-语言、跨模态检索、多模态检测等更广泛任务的验证，泛化性存疑。
- **算力信息缺失**：未报告 GPU 型号、数量、训练时长，难以评估训练成本与可复现性。
- **超参与松弛策略未充分探讨**：$\lambda$、高斯核带宽 $\sigma$ 的敏感性未做分析；OT 的松弛形式去除了 incoming 约束，可能损失部分双向对齐信息。
- **不完整融合的模拟偏差**：缺失模态实验采用人工设置缺失率，可能无法完全反映真实场景中模态缺失的随机性与相关性。
- **对比基线时效性**：未与更多近期 Mamba 类多模态方法（如其他 2024–2025 年工作）进行系统对比，Mamba 内部比较主要限于单流/多流简单变体。
- **理论分析较浅**：MMD 与 OT 结合的理论互补性更多是直觉论证，缺少更深入的理论保证或收敛性分析。

（完）
