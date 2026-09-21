---
title: "CoV-Align: Efficient Fine-grained Cross-Modal Alignment with Cohesive Visual Semantics Priority"
title_zh: CoV-Align：以凝聚视觉语义为先的高效细粒度跨模态对齐
authors: "Liu, Hengqi, Zhou, Wanting, Kong, Longteng, Feng, Fangxiang, Ren, Lei, Chen, Wei, Wang, Xiaojie"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Liu_CoV-Align_Efficient_Fine-grained_Cross-Modal_Alignment_with_Cohesive_Visual_Semantics_Priority_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 6.0
evidence: 以凝聚视觉语义为先的细粒度跨模态对齐
tldr: 现有跨模态对齐方法依赖文本引导聚合，存在冗余的图块-词相关性与高昂计算开销。本文提出CoV-Align框架，通过语义收敛注意力以无文本方式逐步聚合有意义的视觉图块，并设计融合可变形注意力的粗视觉语义特征提取器进行分组。实验表明该方法在实现高效细粒度对齐的同时取得优越性能。该工作为可见光与热红外的细粒度跨模态特征对齐提供了高效方案。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-cov-align-efficient-fine-grained-cross-modal-alignment-with-cohesive-visual-semantics-priority-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 2144, \"height\": 976}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-cov-align-efficient-fine-grained-cross-modal-alignment-with-cohesive-visual-semantics-priority-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 3, \"index\": 2, \"width\": 384, \"height\": 384}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-cov-align-efficient-fine-grained-cross-modal-alignment-with-cohesive-visual-semantics-priority-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 3, \"index\": 3, \"width\": 446, \"height\": 432}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-cov-align-efficient-fine-grained-cross-modal-alignment-with-cohesive-visual-semantics-priority-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 3, \"index\": 4, \"width\": 335, \"height\": 416}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-cov-align-efficient-fine-grained-cross-modal-alignment-with-cohesive-visual-semantics-priority-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 3, \"index\": 5, \"width\": 349, \"height\": 429}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-cov-align-efficient-fine-grained-cross-modal-alignment-with-cohesive-visual-semantics-priority-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 3, \"index\": 6, \"width\": 316, \"height\": 395}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-cov-align-efficient-fine-grained-cross-modal-alignment-with-cohesive-visual-semantics-priority-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 3, \"index\": 7, \"width\": 620, \"height\": 194}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-cov-align-efficient-fine-grained-cross-modal-alignment-with-cohesive-visual-semantics-priority-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 8, \"index\": 8, \"width\": 384, \"height\": 384}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-cov-align-efficient-fine-grained-cross-modal-alignment-with-cohesive-visual-semantics-priority-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 8, \"index\": 9, \"width\": 500, \"height\": 500}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-cov-align-efficient-fine-grained-cross-modal-alignment-with-cohesive-visual-semantics-priority-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 8, \"index\": 10, \"width\": 500, \"height\": 500}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-cov-align-efficient-fine-grained-cross-modal-alignment-with-cohesive-visual-semantics-priority-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 8, \"index\": 11, \"width\": 384, \"height\": 384}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-cov-align-efficient-fine-grained-cross-modal-alignment-with-cohesive-visual-semantics-priority-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 8, \"index\": 12, \"width\": 500, \"height\": 500}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-cov-align-efficient-fine-grained-cross-modal-alignment-with-cohesive-visual-semantics-priority-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 8, \"index\": 13, \"width\": 500, \"height\": 500}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-cov-align-efficient-fine-grained-cross-modal-alignment-with-cohesive-visual-semantics-priority-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 8, \"index\": 14, \"width\": 500, \"height\": 500}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-cov-align-efficient-fine-grained-cross-modal-alignment-with-cohesive-visual-semantics-priority-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 8, \"index\": 15, \"width\": 500, \"height\": 500}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-cov-align-efficient-fine-grained-cross-modal-alignment-with-cohesive-visual-semantics-priority-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 8, \"index\": 16, \"width\": 384, \"height\": 384}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-cov-align-efficient-fine-grained-cross-modal-alignment-with-cohesive-visual-semantics-priority-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 8, \"index\": 17, \"width\": 500, \"height\": 500}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-cov-align-efficient-fine-grained-cross-modal-alignment-with-cohesive-visual-semantics-priority-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 8, \"index\": 18, \"width\": 500, \"height\": 500}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-cov-align-efficient-fine-grained-cross-modal-alignment-with-cohesive-visual-semantics-priority-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 8, \"index\": 19, \"width\": 384, \"height\": 384}]"
motivation: 现有跨模态对齐依赖文本引导聚合，存在冗余图块-词相关性与高计算开销。
method: 提出语义收敛注意力与粗视觉语义特征提取器，以无文本方式聚合有意义视觉图块。
result: 实验表明方法在高效细粒度对齐上取得优越性能。
conclusion: 为细粒度跨模态特征对齐提供了高效新方案。
---

## Abstract
Cross-modal alignment aims to learn semantically consistent latent representations across diverse modalities. Prevailing methods rely on a text-guided aggregation paradigm to achieve fine-grained alignment, while they suffer from redundant patch-word correlations and high computational costs. To address these issues, we propose CoV-Align, an effective and efficient fine-grained cross-modal alignment framework with cohesive visual semantics priority. Through a semantically convergent attention mechanism, it progressively aggregates meaningful visual patches in a text-free manner. We design a coarse visual semantic feature extractor that integrates deformable attention and consistent assign attention to group patches with semantic consistency. A cohesive and discriminative feature optimization is presented to enhance intra-semantic cohesion and inter-semantic discriminability of visual region features, resulting in explicit improvements in cross-modal alignment. Extensive experiments demonstrate that CoV-Align achieves state-of-the-art performance on the Flickr30K and MS-COCO benchmarks. Notably, it delivers a 3-5xcomputational speedup compared to pioneer approaches, offering compelling advantages for large-scale multi-modal tasks.

---

## 论文详细总结（自动生成）

# CoV-Align 论文中文总结

## 1. 核心问题与整体含义（研究动机与背景）

- **研究领域**：跨模态对齐（图像—文本），是图像描述、视觉问答等多模态任务的基础问题，目标是学习跨模态语义一致的潜在表示。
- **现有范式演进**：
  - 粗粒度对齐（如 CLIP、VSE++）：对齐全局图像与整句文本，但难以捕捉局部细节。
  - 基于检测器的细粒度对齐（如 SCAN）：受限于检测器固定类别词表，不适合开放域任务。
  - 基于 Transformer 的 patch-word 对齐（如 FILIP）：单个图块缺乏完整语义，导致词匹配歧义。
  - 文本引导的区域-词对齐（如 LAPS、SPARC）：借助文本嵌入在语义层面聚合图块，性能领先。
- **核心痛点**：文本引导的聚合范式存在两个问题：
  1. **冗余的图块-词对齐**：每个文本查询与全部视觉图块计算权重，引入语义无关图块的噪声，稀释关键语义信息，损害检索精度。
  2. **高计算成本**：大规模检索（百万级图像）下重复聚合带来显著延迟与显存消耗，限制实际部署。
- **核心洞察**：问题根源在于"图块聚合阶段引入了文本信息"。若能在无文本引导下预先链接有意义的视觉语义（如"手""推""推车"），则无关区域无需参与交叉注意力计算。
- **整体含义**：论文提出 CoV-Align，以"凝聚视觉语义优先"实现无文本聚合的细粒度跨模态对齐，力求在精度与效率上取得双赢。

## 2. 方法论

### 2.1 核心思想
采用**无文本（text-free）聚合范式**：先由视觉侧独立生成语义凝聚的区域特征，再与词特征进行稀疏对齐。整体框架包含三个模块：粗视觉语义特征提取器（CVSFE）、凝聚与判别特征优化（CDFO）、稀疏区域-词对齐。

### 2.2 关键技术细节

- **Token 特征提取**：双编码器架构，ViT 提取图像图块特征 $F_v \in \mathbb{R}^{(N+1)\times d_v}$，Transformer 文本编码器提取词特征 $F_t \in \mathbb{R}^{L\times d_t}$。

- **粗视觉语义特征提取（CVSFE）**：
  - **可变形注意力（DAT）**：可学习的区域查询 $z_q$ 与参考点 $p_q$ 参与计算，每个查询只关注稀疏的、语义相关的空间位置，公式为多头的采样偏移加权聚合，兼顾语义聚合与计算效率。
  - **一致性分配注意力**：使用**共享投影矩阵 $W$** 约束注意力分布，强制跨注意力分布的一致性，缓解语义不相干区域间的虚假关联；注意力分数经 Softmax 归一化（温度 $\omega$）。
  - **动态掩码**：将注意力分数归一化到 [0,1] 后，剪除低于阈值 $\varepsilon$ 的图块（置零），得到掩码加权区域特征 $\hat{r}_q$。阈值决定每个区域的覆盖面积（实验共 8 个区域图）。

- **凝聚与判别特征优化（CDFO）**：针对注意力分散导致的**空间漂移**与区域重叠导致的**表示歧义**，设计两个互补约束：
  - **空间集中损失 $L_{conc}$**：计算区域中心 $c_q$（归一化注意力权重的坐标期望），惩罚偏离中心的注意力权重，使注意力分布空间紧凑。
  - **视觉对比损失 $L_{v2v}$**：以某区域特征自身为正样本、同图其他区域特征为负样本，经线性变换映射到文本嵌入空间，提升区域间判别性。

- **稀疏区域-词对齐**：
  - 计算区域-词相似度矩阵 $s_{ij}$（余弦相似度）。
  - 采用 **max-sum pooling**：每个区域（或词）仅保留跨全部词（或区域）的最大相似度，再平均得到图文关联因子 $S(I,T)$。
  - 使用双向对比损失 $L_{v2t}$、$L_{t2v}$ 最大化正对相似度、最小化负对相似度。

- **总损失**：$L_{total} = \frac{\vartheta_g}{2}(L_{t2v}+L_{v2t}) + \vartheta_v L_{v2v} + \vartheta_c L_{conc}$。

### 2.3 超参数设置
$\vartheta_g=1, \vartheta_v=1, \vartheta_c=0.5$；阈值 $\varepsilon=0.7$；区域数 $N_q=8$；训练 30 个 epoch，Adam 优化器，学习率 1e-4，权重衰减 1e-4，余弦退火，特征投影到 512 维共享空间。

## 3. 实验设计

- **数据集**：
  - **Flickr30K**：29,000 训练 / 1,014 验证 / 1,000 测试，每图 5 条描述。
  - **MS-COCO**：113,287 训练 / 5,000 验证 / 5,000 测试，结果报告为 5 折 1K 测试集均值与完整 5K 测试集。
- **评价指标**：Recall@K（R@1、R@5、R@10）及六项召回之和 RSUM，覆盖双向检索（图→文、文→图）。
- **Benchmark 与对比方法**：
  - 检测器类：TGDT、CHAN、HREM、NUIF（Faster R-CNN + BERT）。
  - Transformer 类：VSE++、SCAN、SGR、CHAN、LAPS、AVSE，覆盖 ViT-Base-224/384、Swin-Base-224/384 四种视觉骨干。
  - VLP 与 CLIP 变体：UNITER、VILT、CLIP、FG-CLIP、FineCLIP、SOHO、ALBEF、BLIP、LG-MGC、AGREE（CLIP-ViT-B/L 配置）。
  - 所有基线结果均直接取自原论文或在相同评测协议下复现，以保证公平性。
- **实验类型**：主检索实验、效率对比（FLOPs、参数量、GPU 显存、评测耗时）、消融实验（模块、损失、超参数）、可视化分析。

## 4. 资源与算力

- **论文未明确说明**所使用 GPU 的型号、数量及训练时长。
- 仅报告了效率相关指标：在 batch size 128 下，CoV-Align 的 #FLOPs 为 2289.22G，参数量 217.19M，训练显存占用 25G（对比 LAPS 的 2577.61G / 196.72M / 49G）。
- 因此，具体的硬件配置与训练成本无法从文中获知，这属于信息缺失。

## 5. 实验数量与充分性

- **主实验**：在 Flickr30K、MS-COCO 1K/5K 上跨 4~5 种视觉骨干与两类编码器配置进行对比，覆盖数十个基线模型，规模充分。
- **消融实验**（Flickr30K，ViT-Base-224 + BERT）：
  - 组件消融：基线 → +CVSFE → +视觉对比损失 → +空间集中损失，共 4 组。
  - 阈值 $\varepsilon$ 消融：0.0/0.3/0.5/0.7/0.9，共 5 组。
  - 区域数 $N_q$ 消融：4/8/12/16，共 4 组。
- **效率实验**：与 CLIP、CHAN、SCAN、LAPS 对比 FLOPs、参数量、显存，并在两数据集上对比评测时间。
- **可视化**：展示 4 组图文对的区域-词对齐效果。
- **充分性评估**：
  - 优点：实验覆盖多骨干、多数据集、多超参数，消融设计清晰，能逐项验证各模块贡献；对比结果声明来自原始论文或相同协议复现，公平性较好。
  - 局限：超参数 $\varepsilon$、$N_q$ 仅在 Flickr30K 上消融，未验证跨数据集泛化性；论文正文提及的部分细节（如共享投影矩阵设计）放在附录 B、损失系数放附录 A，正文中未充分展开。

## 6. 主要结论与发现

- CoV-Align 在 Flickr30K 与 MS-COCO 上达到 SOTA。相较代表性方法 LAPS，Flickr30K 上 RSUM 提升：ViT-224 **+8.7**、ViT-384 **+12.8**、Swin-224 **+5.0**、Swin-384 **+11.7**。
- 分辨率越高，相对 LAPS 的性能优势越大，说明独立区域聚合能更好地利用高分辨率注意力图。
- 集成到 CLIP 后（CLIP-ViT-Large）RSUM 达 491.9，优于 LG-MGC 的 465.3，并与 SOTA VLP 模型具有竞争力。
- **效率优势**：相比 LAPS 约 **3× 加速**（COCO 上 114.0s vs 442.2s）；FLOPs 降低 7–15%；训练显存 25G，比 LAPS 减少 49%。
- 消融表明：CVSFE 显著提升性能（R@1 从 70.4/59.4 提升至 73.9/62.1）；视觉对比损失提升类间判别性；空间集中损失进一步提升类内凝聚（R@1 再增 3.1/0.7）；最优阈值 $\varepsilon=0.7$、最优区域数 $N_q=8$。
- 可视化显示，模型对名词（如 "stop sign"）聚焦于对应物体区域，对动词（如 "is walking"、"is pushing"）能同时定位动作主体与相关区域，实现精确的视觉-语义关联。

## 7. 优点

- **范式创新**：首次提出无文本引导的图块聚合，从根源上解决冗余对齐与高计算成本问题，实现精度与效率的双赢。
- **模块设计精巧**：可变形注意力 + 一致性分配注意力（共享投影矩阵 + 动态掩码）协同生成语义一致的粗区域；两个互补损失（空间集中 + 视觉对比）分别解决空间漂移与区域重叠歧义。
- **效率优势显著**：FLOPs、显存、推理时间均优于细粒度同类方法，接近粗粒度 CLIP 的效率，利于大规模检索部署。
- **实验扎实**：多数据集、多骨干、多基线、多组消融，且对高分辨率场景展现出良好扩展性。
- **可视化直观**：验证了名词与动词的细粒度区域-词对齐能力。

## 8. 不足与局限

- **算力信息缺失**：未报告 GPU 型号、数量与训练时长，复现成本与可扩展性难以评估。
- **参数量略增**：CoV-Align 参数量 217.19M，高于对比方法的 196.72M，"参数效率"的表述相对保守。
- **超参数泛化性未验证**：$\varepsilon$、$N_q$ 仅在 Flickr30K 上消融，是否适用于其他数据集（如 MS-COCO、跨域场景）未知。
- **任务覆盖有限**：仅在图文检索任务上评估，未验证图像描述、VQA 等下游多模态任务。
- **关键细节置于附录**：共享投影矩阵有效性、损失系数选择等核心设计说明在正文中未充分展开，影响可读性与可复现性。
- **元数据与实际内容的偏差风险**：论文元数据标签提及 UAV/RGB-T 细粒度对齐应用，但正文实验并未涉及可见光-热红外或无人机场景，将该工作直接外推到这些领域缺乏实证支持。
- **无文本聚合的潜在风险**：区域划分完全依赖视觉侧，可能在文本强调的细粒度属性（颜色、数量等）上出现区域覆盖不足或错配，论文未对此类失败案例做定量分析。

（完）
