---
title: Bridging the Modality Gap in Compositional Zero-Shot Learning via Sparse Alignment and Unimodal Memory Bank
title_zh: 通过稀疏对齐与单模态记忆库弥合组合零样本学习中的模态鸿沟
authors: "Zhang, Yang, Chi, Zhixiang, Yan, Xudong, Wang, Yang, Feng, Songhe"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Zhang_Bridging_the_Modality_Gap_in_Compositional_Zero-Shot_Learning_via_Sparse_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 4.0
evidence: 稀疏跨模态对齐以弥合模态鸿沟
tldr: 该文针对组合零样本学习中CLIP跨模态对齐忽视模态鸿沟的问题展开研究。作者提出SAM方法，通过稀疏对齐将文本表示直接关联到语义相关的视觉图块，并引入单模态记忆库缓解信息不平衡。实验表明该方法能有效弥合模态鸿沟并提升组合识别性能。其跨模态对齐思想有一定参考价值，但任务与UAV RGB-T显著目标检测差异较大。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 2, \"index\": 1, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 3, \"index\": 2, \"width\": 1200, \"height\": 392}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 4, \"index\": 3, \"width\": 1280, \"height\": 800}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 4, \"index\": 4, \"width\": 789, \"height\": 730}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 4, \"index\": 5, \"width\": 765, \"height\": 593}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 4, \"index\": 6, \"width\": 781, \"height\": 593}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 4, \"index\": 7, \"width\": 767, \"height\": 600}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 4, \"index\": 8, \"width\": 921, \"height\": 593}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 4, \"index\": 9, \"width\": 1280, \"height\": 560}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 4, \"index\": 10, \"width\": 1280, \"height\": 733}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 4, \"index\": 11, \"width\": 1280, \"height\": 266}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 4, \"index\": 12, \"width\": 1140, \"height\": 836}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 4, \"index\": 13, \"width\": 1280, \"height\": 883}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 4, \"index\": 14, \"width\": 1124, \"height\": 836}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 4, \"index\": 15, \"width\": 1280, \"height\": 381}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 4, \"index\": 16, \"width\": 1280, \"height\": 392}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 4, \"index\": 17, \"width\": 1280, \"height\": 386}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 4, \"index\": 18, \"width\": 1280, \"height\": 357}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 4, \"index\": 19, \"width\": 1280, \"height\": 348}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-020.webp\", \"caption\": \"\", \"page\": 4, \"index\": 20, \"width\": 1280, \"height\": 352}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-021.webp\", \"caption\": \"\", \"page\": 4, \"index\": 21, \"width\": 751, \"height\": 800}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-022.webp\", \"caption\": \"\", \"page\": 4, \"index\": 22, \"width\": 697, \"height\": 800}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-023.webp\", \"caption\": \"\", \"page\": 4, \"index\": 23, \"width\": 730, \"height\": 800}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-024.webp\", \"caption\": \"\", \"page\": 4, \"index\": 24, \"width\": 879, \"height\": 859}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-025.webp\", \"caption\": \"\", \"page\": 4, \"index\": 25, \"width\": 825, \"height\": 859}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-026.webp\", \"caption\": \"\", \"page\": 4, \"index\": 26, \"width\": 858, \"height\": 859}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-027.webp\", \"caption\": \"\", \"page\": 4, \"index\": 27, \"width\": 1280, \"height\": 800}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-028.webp\", \"caption\": \"\", \"page\": 4, \"index\": 28, \"width\": 1280, \"height\": 383}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-029.webp\", \"caption\": \"\", \"page\": 4, \"index\": 29, \"width\": 1280, \"height\": 349}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-030.webp\", \"caption\": \"\", \"page\": 4, \"index\": 30, \"width\": 1280, \"height\": 359}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-031.webp\", \"caption\": \"\", \"page\": 4, \"index\": 31, \"width\": 1214, \"height\": 862}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-032.webp\", \"caption\": \"\", \"page\": 4, \"index\": 32, \"width\": 380, \"height\": 380}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-033.webp\", \"caption\": \"\", \"page\": 5, \"index\": 33, \"width\": 1200, \"height\": 380}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-034.webp\", \"caption\": \"\", \"page\": 5, \"index\": 34, \"width\": 1200, \"height\": 380}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-035.webp\", \"caption\": \"\", \"page\": 8, \"index\": 35, \"width\": 1350, \"height\": 600}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-036.webp\", \"caption\": \"\", \"page\": 8, \"index\": 36, \"width\": 1350, \"height\": 600}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-037.webp\", \"caption\": \"\", \"page\": 8, \"index\": 37, \"width\": 1350, \"height\": 600}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-038.webp\", \"caption\": \"\", \"page\": 8, \"index\": 38, \"width\": 1350, \"height\": 600}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-039.webp\", \"caption\": \"\", \"page\": 8, \"index\": 39, \"width\": 1350, \"height\": 600}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-040.webp\", \"caption\": \"\", \"page\": 8, \"index\": 40, \"width\": 527, \"height\": 317}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhang-bridging-the-modality-gap-in-compositional-zero-shot-learning-via-sparse-cvpr-2026-paper/fig-041.webp\", \"caption\": \"\", \"page\": 8, \"index\": 41, \"width\": 1776, \"height\": 4060}]"
motivation: 现有组合零样本学习依赖CLIP跨模态对齐，却忽视训练数据信息不平衡带来的模态鸿沟。
method: 提出稀疏对齐将文本表示关联到语义相关视觉图块，并引入单模态记忆库。
result: 实验证明该方法可有效弥合模态鸿沟并提升未见组合的识别表现。
conclusion: 稀疏对齐思路对跨模态对齐有启发，但任务目标与RGB-T显著检测不同。
---

## Abstract
Compositional Zero-Shot Learning (CZSL) aims to recognize unseen attribute-object compositions with learned primitives (attribute and object) knowledge from seen compositions. While previous approaches gain their notable performance through the powerful cross-modal alignment of CLIP, they often overlook the modality gap, an inherent constraint stemming from information-imbalanced training data. In this work, we propose SAM, a novel \underline \text S parse \underline \text A lignment and Unimoal \underline \text M emory Bank to effectively bridging modality gap for CZSL. Specifically, we conduct sparse alignment that links textual representations directly to their semantically pertinent visual patches. This direct linking serves to prune redundant visual data and counter the information imbalance in image-text pairs. Subsequently, with the sparsely aligned visual information as its guidance, the visual adaptive condensation module adaptively fuses these critical cues into a unified representation. Finally, we introduce a dynamically updated memory bank that stores samples from both seen and unseen compositions. This bank serves a dual purpose: it bypasses the modality gap through visual-only classification and concurrently strengthens generalization to unseen compositions. Experiments on three benchmarks demonstrate that our method gains significant improvements over CLIP-based methods under closed-world and open-world settings.

---

## 论文详细总结（自动生成）

# 论文总结：通过稀疏对齐与单模态记忆库弥合组合零样本学习中的模态鸿沟

## 1. 论文的核心问题与整体含义（研究动机与背景）

- **任务背景**：组合零样本学习（Compositional Zero-Shot Learning, CZSL）要求模型在仅见过部分属性–对象组合（如 white swan、black cat）的情况下，识别未见过的组合（如 black swan），核心挑战在于对属性与对象原语的解耦与重组。
- **现状与痛点**：当前主流方法依赖 CLIP 强大的跨模态对齐能力，并在此基础上探索增强视觉–文本对齐、原语解耦、优先级校准和语义挖掘等技术。然而，这些方法普遍**忽视了一个根本性限制——模态鸿沟（modality gap）**。
- **模态鸿沟的成因**：论文指出，模态鸿沟的根本原因在于**训练数据中的信息不平衡**。图像通常编码丰富的细节信息，而文本标注往往只描述显著目标，导致匹配对之间的监督信号被削弱。在 CZSL 这类细粒度任务中，显著属性极易被周围上下文污染。
- **核心问题**：如何在 CZSL 任务中，通过有原则地减少冗余视觉信息、恢复图文信息平衡，从而弥合模态鸿沟并提升未见组合的识别性能。
- **整体含义**：该工作将模态鸿沟的成因分析从对比损失、温度参数等表层因素，追溯到信息不平衡这一更深层机制，并据此设计了一个三阶段框架 SAM，在闭世界与开世界两种设定下均取得显著提升。

## 2. 论文提出的方法论

### 核心思想
不再依赖 CLIP 的全局 `[CLS]` token 作为视觉表示，而是通过**稀疏对齐（Sparse Alignment, SA）** 将文本表示直接关联到语义最相关的视觉图块（patch），抑制冗余视觉信息；再通过**视觉自适应凝聚（Visual Adaptive Condensation, VAC）** 以稀疏对齐信号为引导，自适应地融合关键视觉线索；最后通过**动态更新的单模态记忆库**在纯视觉模态内完成分类，从根本上绕过模态鸿沟。

### 关键技术细节与算法流程

**Stage I：稀疏对齐（Sparse Alignment, SA）**
- 给定 CLIP 视觉编码器输出的 token 序列 `V = [v_CLS, v_1, ..., v_L]`，对每个已见组合的文本表示 `t_c`，计算其与所有视觉 token 的相似度，并取最大值：
  - `s_c = max_{l=1}^{L+1} S_{l,c}`，其中 `S = V · T_c^T`
- 该操作保留每个文本表示语义最相关的 patch，形成稀疏对齐。
- 组合分类概率：`p_sa(c_i|x) = exp(s_i/τ) / Σ_k exp(s_k/τ)`
- 属性与对象原语采用相同形式，基础损失为 `L_base = L_c + L_a + L_o`。
- 论文通过实验证明，降低 patch token 的贡献会显著降低性能，说明 `[CLS]` token 引入了过量视觉信息；同时约 25% 的 patch 表现出高类别特异性激活，且大多数样本中最高响应 token 来自 patch 而非 `[CLS]`。

**Stage II：视觉自适应凝聚（Visual Adaptive Condensation, VAC）**
- 引入一个可学习的 query embedding `q ∈ R^{1×D}`，通过 K 个处理块（含多头交叉注意力与 FFN）动态聚合所有 token 中的语义重要信息，得到凝聚表示 `v_q`。
- VAC 预测：`p_vac(c_i|x) = exp(v_q · t_i^c/τ) / Σ_k exp(v_q · t_k^c/τ)`
- 基础损失：`L_base^vac = L_c^vac + L_a^vac + L_o^vac`
- **蒸馏目标**：以 SA 的预测分布作为软标签，通过 KL 散度约束 VAC：
  - `L_kl = - (1/|D_tr|) Σ_x p_vac log(p_vac / p_sa)`
- 总体损失：`L_vac = (1-α) · L_base^vac + α · L_kl`

**Stage III：动态更新记忆库**
- 构建记忆库 `B ∈ R^{|C|×N×D}`，每个组合存储 N 个高置信度凝聚视觉表示。
- 更新规则：当 VAC 预测置信度高（熵 `H(p_vac) < T_{i,j}`）且预测类别为 i 时，用当前样本替换该组合中熵最高的存储样本。
- 推理时，对每个测试样本 `v_q`，从记忆库中检索各组合原型 `p_i = softmax((v_q · B_{i,:}^T)/τ_mb) · B_{i,:}`，得到记忆库预测 `p_mb(c_i|x)`。
- 初始时将文本表示插入记忆库，以支持无视觉样本的未见组合推理；更新与预测均为训练无关方式，不引入显著计算开销。

**最终推理融合**
- `p̂(c|x) = β · p̄_sa(c|x) + (1-β) · (p̄_vac(c|x) + γ · p_mb(c|x))`
- 其中 `p̄(c|x) = p(c|x) + p(a|x) · p(o|x)`，即组合预测与属性、对象原语预测的融合。

## 3. 实验设计

- **数据集**：三个 CZSL 标准基准——UT-Zappos、MIT-States、C-GQA。
- **评估设定**：
  - **闭世界（closed-world）**：仅考虑数据集中的已知组合。
  - **开世界（open-world）**：测试集包含所有可能的属性–对象组合（C = A × O），更具挑战性。
- **评估指标**：已见准确率（S）、未见准确率（U）、调和平均（HM）、AUC。
- **对比方法**：CLIP、CoOp、CSP、DFSP、PLID、CDS、Troika、LogiCzsl、ClusPro 等 9 种 SOTA 方法。
- **骨干网络**：预训练 CLIP ViT-L/14，视觉编码器采用 LoRA 微调。
- **消融实验**：
  - 主成分消融：Baseline → +L_base（SA）→ +L_qbase（VAC）→ +L_kl（蒸馏）→ +Memory Bank → +Dynamically Update。
  - 模态鸿沟与 AUC 关系分析（RMG 与 AUC 的对应趋势）。
  - 稀疏对齐中不同操作（Mean / Attention / Linear / Max）的对比。
  - 将 SA 即插即用地集成到 SOTA 方法 Troika 中验证通用性。
- **可视化分析**：注意力可视化（VAC vs. Baseline）、成功与失败案例分析。

## 4. 资源与算力

- 论文中**未明确提及**所使用的 GPU 型号、数量、训练时长或总计算量。
- 仅提及采用预训练 CLIP ViT-L/14 作为骨干，并使用 LoRA 进行视觉编码器微调，详细实验设置置于补充材料 §A 中。
- 因此，关于训练成本与算力开销，正文无法给出具体量化信息。

## 5. 实验数量与充分性

- **实验组数概览**：
  - 闭世界设定：3 个数据集 × 9 种对比方法 + 本方法。
  - 开世界设定：3 个数据集 × 9 种对比方法 + 本方法。
  - 消融实验：6 个递进配置 × 3 个数据集 × 4 个指标。
  - 模态鸿沟分析：3 个配置（Base / +SA / +VAC）× 3 个数据集。
  - 稀疏对齐操作对比：4 种操作 × 2 个数据集。
  - 即插即用验证：Troika 与 Troika+SA 在 2 个数据集上的对比。
  - 定性结果与注意力可视化。
- **充分性评价**：
  - 实验覆盖三个主流基准、两种评估设定，对比方法涵盖 2021–2025 年的代表性工作，**覆盖面较为充分**。
  - 消融实验逐级递进，清晰展示了各模块的边际贡献。
  - 额外验证了 SA 作为即插即用模块对 Troika 的增益，增强了结论的**泛化性与公平性**。
  - 但缺少对超参数（如 α、β、γ、N、T）的敏感性分析，正文中部分细节依赖补充材料。

## 6. 论文的主要结论与发现

- **核心发现**：模态鸿沟与信息不平衡密切相关；适度减少视觉信息（如随机丢弃 patch token）即可带来 AUC 提升与 RMG 下降，但丢弃率过高会损害性能。
- **方法有效性**：SAM 在闭世界设定下于三个数据集上取得最佳 AUC（50.0 / 24.0 / 16.2）和 HM（62.0 / 40.8 / 34.8）；开世界设定下同样取得 SOTA 的 AUC 与 HM（42.3 / 9.4 / 4.6）。
- **模块贡献**：SA 建立信息平衡训练范式，VAC 在 SA 引导下自适应恢复关键视觉信息，记忆库通过纯视觉分类绕过模态鸿沟，动态更新进一步提升已见与未见的准确率。
- **模态鸿沟与性能的关系**：随着 SA 和 VAC 的引入，RMG 持续下降而 AUC 持续上升，验证了两者之间的负相关关系。
- **稀疏对齐的通用性**：SA 不引入额外可学习参数，可即插即用地集成到 Troika 中，在 C-GQA 上将 AUC 从 12.4 提升至 13.1，在 UT-Zappos 上从 41.7 提升至 43.1。

## 7. 优点

- **问题定位深刻**：将模态鸿沟的成因从对比损失、温度参数等表层因素追溯到信息不平衡这一更深层机制，视角新颖。
- **方法论系统完整**：三阶段框架设计环环相扣——SA 减少冗余、VAC 补偿信息损失、记忆库绕过模态鸿沟，逻辑自洽。
- **稀疏对齐设计巧妙**：利用 CLIP 输出端的 patch token 而非仅依赖 `[CLS]`，通过 max 操作实现无参数的稀疏对齐，简洁有效且可即插即用。
- **蒸馏机制合理**：以 SA 的软标签指导 VAC，既保留了信息平衡的优势，又补偿了稀疏化可能带来的信息损失。
- **记忆库设计实用**：训练无关的动态更新机制，在不显著增加推理成本的前提下，同时提升已见与未见组合的识别性能。
- **实验全面**：闭世界与开世界双设定、三个基准、多种消融、即插即用验证与可视化分析，论证链条完整。

## 8. 不足与局限

- **算力信息缺失**：论文未报告 GPU 型号、数量、训练时长等算力开销，难以评估方法的实际部署成本与可复现性。
- **超参数敏感性分析不足**：α、β、γ、N、T、τ_mb 等关键超参数的选取依据与敏感性分析在正文中未充分展开。
- **失败案例的局限性**：失败案例多源于语义相似性（如 red vs. maroon、suede vs. sheepskin），说明方法在细粒度语义区分上仍有提升空间。
- **记忆库的潜在偏差风险**：动态更新依赖模型自身预测的置信度，若模型在未见组合上产生高置信度错误预测，可能污染记忆库，论文未对此风险做深入讨论。
- **任务适用性受限**：该方法针对 CZSL 的图文对齐任务设计，与 RGB-T 显著目标检测等任务差异较大，跨任务迁移能力有待验证。
- **MIT-States 表现相对较弱**：论文指出该数据集噪声样本较多导致模态鸿沟较大，方法在该数据集上的增益相对有限。

（完）
