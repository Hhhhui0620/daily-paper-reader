---
title: "THE MORE, THE MERRIER: CONTRASTIVE FUSION FOR HIGHER-ORDER MULTIMODAL ALIGNMENT"
title_zh: 越多越好：面向高阶多模态对齐的对比融合
authors: "Koutoupis, Stefanos, Zervou, Michaela Areti, Kontras, Konstantinos, De Vos, Maarten, Tsakalides, Panagiotis, Tsagkatakis, Grigorios"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Koutoupis_THE_MORE_THE_MERRIER_CONTRASTIVE_FUSION_FOR_HIGHER-ORDER_MULTIMODAL_ALIGNMENT_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 6.0
evidence: 对比融合将多模态及其融合组合对齐到统一空间
tldr: 现有多模态对齐方法大多局限于两两模态配对，难以同时保留成对关系与高阶交互，限制了下游单模态任务表现。本文提出对比融合框架ConFu，将各模态及其融合组合联合嵌入统一表示空间并施加对齐约束，在传统成对对比目标上扩展出高阶对齐机制。实验表明该框架在多模态与单模态任务上均取得更优表现。该工作为可见光与热红外等跨模态特征对齐提供了可迁移的高阶对齐思路。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-koutoupis-the-more-the-merrier-contrastive-fusion-for-higher-order-multimodal-alignment-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 1020, \"height\": 483}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-koutoupis-the-more-the-merrier-contrastive-fusion-for-higher-order-multimodal-alignment-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 3, \"index\": 2, \"width\": 1012, \"height\": 684}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-koutoupis-the-more-the-merrier-contrastive-fusion-for-higher-order-multimodal-alignment-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 4, \"index\": 3, \"width\": 984, \"height\": 583}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-koutoupis-the-more-the-merrier-contrastive-fusion-for-higher-order-multimodal-alignment-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 7, \"index\": 4, \"width\": 1735, \"height\": 992}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-koutoupis-the-more-the-merrier-contrastive-fusion-for-higher-order-multimodal-alignment-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 7, \"index\": 5, \"width\": 898, \"height\": 678}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-koutoupis-the-more-the-merrier-contrastive-fusion-for-higher-order-multimodal-alignment-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 7, \"index\": 6, \"width\": 1735, \"height\": 1165}]"
motivation: 现有多模态对齐方法多以两两配对为主，忽视或难以保留成对关系，限制单模态任务表现。
method: 提出对比融合框架ConFu，将各模态及其融合组合联合嵌入统一表示空间，扩展成对对比目标。
result: 实验表明该框架在多模态对齐与单模态任务上均取得更优表现。
conclusion: 为高阶多模态对齐提供了兼顾成对关系的新范式。
---

## Abstract
Learning joint representations across multiple modalities remains a central challenge in multimodal machine learning. Prevailing approaches predominantly operate in pairwise settings, aligning two modalities at a time. While some recent methods aim to capture higher-order interactions among multiple modalities, they often overlook or insufficiently preserve pairwise relationships, limiting their effectiveness on single-modality tasks. In this work, we introduce Contrastive Fusion (ConFu), a framework that jointly embeds both individual modalities and their fused combinations into a unified representation space, where modalities and their fused counterparts are aligned. ConFu extends traditional pairwise contrastive objectives with an additional fused-modality contrastive term, encouraging the joint embedding of modality pairs with a third modality. This formulation enables ConFu to capture higher-order dependencies, such as XOR-like relationships, that cannot be recovered through pairwise alignment alone, while still maintaining strong pairwise correspondence. We evaluate ConFu on synthetic and real-world multimodal benchmarks, assessing its ability to exploit cross-modal complementarity, capture higher-order dependencies, and scale with increasing multimodal complexity. Across these settings, ConFu demonstrates competitive performance on retrieval and classification tasks, while supporting unified one-to-one and two-to-one retrieval within a single contrastive framework. We release our code and dataset at https://github.com/estafons/confu.

---

## 论文详细总结（自动生成）

# 论文总结：ConFu —— 面向高阶多模态对齐的对比融合

## 1. 核心问题与研究动机

- **背景**：多模态联合表示学习是核心难题。以 CLIP、ALIGN 为代表的对比学习框架证明了配对模态（如图像–文本）对齐能带来强大的零样本迁移与检索能力。
- **核心痛点一：成对局限**。现有主流方法本质上是**成对（pairwise, 1→1）**的，只能捕捉两个模态之间的相关性，忽略三个及以上模态交互时产生的**高阶依赖（higher-order dependencies）**。
- **核心痛点二：模态竞争**。多模态模型常出现“模态竞争”现象，强模态（如视觉）会压制弱模态（如音频），导致联合表示偏向单一信息源。
- **核心痛点三：高阶方法牺牲成对关系**。Symile、TRIANGLE、GRAM 等近期高阶方法虽然建模了多模态联合依赖，但往往忽视或难以保留成对关系，且在推理时要求所有模态齐全，无法支持标准的单模态（1→1）检索。
- **研究问题**：能否在一个统一的对比学习框架内，既捕捉成对对齐，又建模高阶协同依赖？
- **整体意义**：论文提出 **ConFu（Contrastive Fusion）**，把单模态与融合模态统一嵌入同一表示空间，在单一目标下兼顾 1→1 与 2→1 对齐，为跨模态（如可见光–热红外等）高阶对齐提供了可迁移思路。

## 2. 方法论

### 核心思想
- 对 M=3 个模态，不仅对齐两两模态，还把**任意两个模态的融合表示**与**第三个模态**对齐，从而在统一空间中同时最大化成对与高阶依赖。
- 理论上，该目标等价于最大化三变量**总相关（Total Correlation, TC）**的对比下界。

### 关键技术细节
- **编码与投影**：每个模态 $X_i$ 经模态专属编码器 $f_{\theta_i}$ 和投影器 $p_{\phi_i}$ 映射到共享隐空间 $Z$：$z_i = p_{\phi_i}(f_{\theta_i}(X_i))$。
- **成对对比目标（1→1）**：对每对模态 $(X_i, X_j)$ 用 InfoNCE 下界估计互信息 $I(X_i;X_j)$，密度比 $s_{\omega_{ij}}$ 实现为温度缩放的**点积相似度**。三个成对项求和得到 $L_{pair}$。
- **高阶对比目标（2→1）**：用融合网络 $g_{\psi_{ij}}$（实验中为**浅层 MLP**）将两个模态编码特征融合为 $z_{ij}$，再与剩余模态 $X_k$ 用 InfoNCE 对齐，估计 $I(X_k; X_i, X_j)$，三个三元组项求和得到 $L_{fused}$。
- **总损失**：$L = (1-\lambda)L_{pair} + \lambda L_{fused}$，$\lambda \in [0,1]$ 平衡成对与高阶监督。

### 理论推导
- 总相关分解为链式形式 $TC = I(X_1;X_2) + I(X_3;X_1,X_2)$，对所有 6 种排列取平均得对称形式。
- 将各互信息的 InfoNCE 下界代入，得到 TC 的可处理下界：最大化 TC ⇔ 最小化所有成对与高阶 InfoNCE 损失（当 critic 足够表达且 N→∞ 时下界趋紧）。
- **与 Symile/GRAM/TRIANGLE 的区别**：后者用单一联合对齐目标（多线性相似度 / 平行体体积 / 三角形面积），不区分成对与高阶；ConFu 在**损失层面做因子分解**，可独立控制两类监督，并支持任意模态子集推理。

### 动机示例（XOR 任务）
- 三个二值变量中 $x_3 = (x_1 \oplus x_2)$，成对互信息为零，只有建模联合交互才能解。ConFu 与 Symile 能解，Trimodal pairwise CLIP 停留在随机水平（~3%），GRAM/TRIANGLE 低于 15%。

## 3. 实验设计

### 数据集 / 场景
- **合成数据**：XOR 合成任务（验证高阶依赖捕捉能力）。
- **AV-MNIST**：加噪音频频谱 + 退化 MNIST 图像 + 由标签模板生成文本。
- **情感计算基准**（MultiBench）：MOSI、UR-FUNNY、MUStARD（文本、音频、视频三模态情感理解）。
- **细粒度鸟类分类**：SSW60、VB100（真实视频–音频对，用于下游评估）。
- **自建数据集 Bird-MML**：15 万（149,681）图像–音频–文本三元组，覆盖 150 个物种；图像来自 iNaturalist，音频来自 Xeno-Canto（10 秒片段），文本由 InstructBLIP2 图像描述 + 音频元数据 + Wikipedia 摘要经 gemma-2-2b-it 融合生成；约 43% 物种存在音频复用。

### Benchmark 与评估设置
- 零样本分类（zero-shot）、1→1 与 2→1 检索（Recall@10）、线性探针分类（few-shot 与全量）、多帧（8 帧平均）与单帧协议。
- 额外的**噪声诱导分布偏移**测试（仅对视觉加高斯噪声，SNR≈20dB，测试时施加）。

### 对比方法
- Bi-modal CLIP（标准两模态对比损失）、Tri-modal CLIP（Tri-CLIP，所有模态两两对比）。
- 高阶方法：Symile（总相关）、TRIANGLE（三角形面积相似度）、GRAM（Gramian 体积）。

## 4. 资源与算力

- **论文正文未明确说明**所使用的 GPU 型号、数量、训练时长或总计算量。
- 仅提及融合网络 $g$ 为**小规模浅层 MLP**，额外计算开销轻量；附录（B.1 关于 λ 的分析、B.2 XOR 细节、D.1 数据生成流程等）被多次引用，但提取文本中未包含具体算力信息。
- 因此，**算力配置与训练成本无法从现有文本中确认**。

## 5. 实验数量与充分性

- **实验组数概览**：
  - 合成 XOR 任务 1 组（含不同协同参数 $\hat{p}$ 的扫描）。
  - 零样本分类：AV-MNIST（表 1）、SSW60/VB100（表 4、表 5，含 19 帧采样统计）。
  - 检索实验：MOSI/UR-FUNNY/MUStARD 上的 1→1 与 2→1（表 2，覆盖多组 query→target）。
  - 线性探针分类（表 3）与 few-shot 曲线（图 4）。
  - 消融/分析：模态重叠与模态竞争分析（图 5）、噪声诱导分布偏移（表 6）、λ 影响（附录 B.1）、部分模态掩码（附录 B.3）、额外噪声实验（附录 B.4）、对齐项剪枝（附录 E）。
- **充分性与公平性**：
  - 覆盖合成 + 真实、多领域（生物多样性、情感、多媒体）、多任务（分类、检索、线性探针），**较为全面**。
  - 所有结果均为 **5 次运行均值±标准差**，统计规范。
  - 与 CLIP / Tri-CLIP / Symile / GRAM / TRIANGLE 等代表性基线对比，**比较对象合理**。
  - **潜在不充分之处**：缺少与其他高阶方法在更多模态数（>3）下的对比；Bird-MML 为合成对齐数据集，可能引入生成偏差。

## 6. 主要结论与发现

- ConFu 在合成 XOR 任务上成功捕捉高阶协同信息，而 pairwise CLIP 与几何类方法失败。
- AV-MNIST 零样本分类中取得最佳（A+V 融合 71.2%，较最强单模态提升约 8%）；即便只用视觉也比单模态基线高约 1.5%，说明多模态训练反哺单模态表示。
- 情感基准上：1→1 与 2→1 检索在多数设置下排名第一或第二；UR-FUNNY、MUStARD 上 2→1 优于 1→1，说明双模态查询提供更丰富线索；线性探针在 UR-FUNNY 上最高。
- 鸟类细粒度任务：SSW60 多帧设置达 71.4%（最佳），证明双模态互补有效；VB100 音频信息弱（~4%）时融合仍接近视觉基线（18.15% vs 20.69%），展现对干扰模态的鲁棒性。
- 噪声诱导分布偏移下 ConFu 达 45.4%，明显优于所有基线（Symile 40.9%，TRIANGLE/GRAM 甚至低于单模态基线）。
- 模态重叠分析显示约 5% 样本仅靠融合才能正确预测，验证融合捕获了单模态之外的互补信息。

## 7. 优点

- **统一性**：单一对比框架内同时支持 1→1 与 2→1 检索，无需为不同任务训练不同模型。
- **架构无关**：仅需在编码器之上添加轻量 MLP 融合层，不修改编码器结构，额外开销小。
- **理论支撑扎实**：从总相关分解出发，严格推导出对比下界，将成对与高阶依赖在损失层面因子化，可独立调节。
- **鲁棒性突出**：在模态退化、噪声分布偏移、弱模态场景下均优于高阶基线。
- **附带数据贡献**：构建并开源 Bird-MML 数据集，填补了图像–音频–文本三元组多模态预训练资源的空白，并给出伦理声明。

## 8. 不足与局限

- **算力信息缺失**：正文未报告 GPU 型号、数量与训练时长，可复现性与成本评估受限。
- **模态数受限**：实验主要围绕 3 模态展开，虽声称可扩展至任意模态数，但随模态数增加计算需求上升，缺乏 >3 模态的实证。
- **依赖全模态对齐训练**：当前要求训练时所有模态齐全，无法直接处理部分缺失模态；作者提出伪配对构造等作为未来方向。
- **合成数据偏差**：Bird-MML 中图像、音频、文本为人工配对，约 43% 物种音频复用，文本由 LLM 生成可能含事实噪声，存在生成偏差风险。
- **个别任务非最优**：MOSI 的 2→1 融合略低于成对基线（作者归因于冗余信息导致的捷径学习，需借助部分模态掩码缓解）；MUStARD 线性探针未取得最佳。
- **模态竞争仍存在**：图 5 显示视觉主导现象明显，纯音频贡献仅约 2%，融合虽有效但未根本解决竞争问题。
- **应用限制**：数据仅限非商业研究用途；情感/生物识别等场景的实际部署需谨慎评估。

（完）
