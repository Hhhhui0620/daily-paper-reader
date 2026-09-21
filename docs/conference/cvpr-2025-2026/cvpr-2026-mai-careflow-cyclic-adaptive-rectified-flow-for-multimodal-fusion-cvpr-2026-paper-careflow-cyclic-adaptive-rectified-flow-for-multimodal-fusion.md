---
title: "CaReFlow: Cyclic Adaptive Rectified Flow for Multimodal Fusion"
title_zh: CaReFlow：面向多模态融合的循环自适应整流流
authors: "Mai, Sijie, Han, Shiqin"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Mai_CaReFlow_Cyclic_Adaptive_Rectified_Flow_for_Multimodal_Fusion_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 6.0
evidence: 用整流流进行模态分布映射以缩小融合中的模态鸿沟
tldr: 模态鸿沟严重制约多模态融合效果，现有扩散与对抗方法多关注一对一映射，未让源模态数据点观察目标模态的全局分布。本文提出循环自适应整流流CaReFlow，利用整流流的直线轨迹与一对多映射策略进行模态分布映射。实验表明该方法有效缩小模态差距并提升融合性能。该工作为跨模态特征对齐与失配融合提供了分布层面的新工具。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-mai-careflow-cyclic-adaptive-rectified-flow-for-multimodal-fusion-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 2573, \"height\": 2099}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-mai-careflow-cyclic-adaptive-rectified-flow-for-multimodal-fusion-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 1196, \"height\": 1352}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-mai-careflow-cyclic-adaptive-rectified-flow-for-multimodal-fusion-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 2, \"index\": 3, \"width\": 1969, \"height\": 1078}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-mai-careflow-cyclic-adaptive-rectified-flow-for-multimodal-fusion-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 4, \"index\": 4, \"width\": 1946, \"height\": 1121}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-mai-careflow-cyclic-adaptive-rectified-flow-for-multimodal-fusion-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 6, \"index\": 5, \"width\": 2234, \"height\": 1517}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-mai-careflow-cyclic-adaptive-rectified-flow-for-multimodal-fusion-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 6, \"index\": 6, \"width\": 2234, \"height\": 1601}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-mai-careflow-cyclic-adaptive-rectified-flow-for-multimodal-fusion-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 7, \"index\": 7, \"width\": 2573, \"height\": 2029}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-mai-careflow-cyclic-adaptive-rectified-flow-for-multimodal-fusion-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 7, \"index\": 8, \"width\": 2078, \"height\": 1684}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-mai-careflow-cyclic-adaptive-rectified-flow-for-multimodal-fusion-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 7, \"index\": 9, \"width\": 2573, \"height\": 2029}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-mai-careflow-cyclic-adaptive-rectified-flow-for-multimodal-fusion-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 7, \"index\": 10, \"width\": 2573, \"height\": 2029}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-mai-careflow-cyclic-adaptive-rectified-flow-for-multimodal-fusion-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 7, \"index\": 11, \"width\": 2573, \"height\": 2029}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-mai-careflow-cyclic-adaptive-rectified-flow-for-multimodal-fusion-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 8, \"index\": 12, \"width\": 2158, \"height\": 1342}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-mai-careflow-cyclic-adaptive-rectified-flow-for-multimodal-fusion-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 8, \"index\": 13, \"width\": 2150, \"height\": 1344}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-mai-careflow-cyclic-adaptive-rectified-flow-for-multimodal-fusion-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 8, \"index\": 14, \"width\": 2160, \"height\": 1346}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-mai-careflow-cyclic-adaptive-rectified-flow-for-multimodal-fusion-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 8, \"index\": 15, \"width\": 2160, \"height\": 1346}]"
motivation: 模态鸿沟制约多模态融合，现有方法多为一对一映射，未利用目标模态全局分布信息。
method: 扩展整流流进行模态分布映射，采用一对多映射策略让源模态数据点观察目标分布。
result: 实验表明方法有效缩小模态差距并提升融合性能。
conclusion: 为跨模态对齐与失配融合提供了分布层面的新工具。
---

## Abstract
Modality gap significantly restricts the effectiveness of multimodal fusion. Previous methods often use techniques such as diffusion models and adversarial learning to reduce the modality gap, but they typically focus on one-to-one alignment without exposing the data points of the source modality to the global distribution information of the target modality. To this end, leveraging the characteristic of rectified flow that can map one distribution to another via a straight trajectory, we extend rectified flow for modality distribution mapping. Specifically, we leverage the `one-to-many mapping' strategy in rectified flow that allows each data point of the source modality to observe the overall target distribution. This also alleviates the issue of insufficient paired data within each sample, enabling a more robust distribution transformation. Moreover, to achieve more accurate distribution mapping and address the ambiguous flow directions in one-to-many mapping, we design `adaptive relaxed alignment', enforcing stricter alignment for modality pairs belonging to the same sample, while applying relaxed mapping for pairs not belonging to the same sample or category. Additionally, to prevent information loss during distribution mapping, we introduce `cyclic rectified flow' to ensure the transferred features can be translated back to the original features, allowing multimodal representations to learn sufficient modality-specific information. After distribution alignment, our approach achieves very competitive results on multiple tasks of multimodal affective computing even with a simple fusion method, and visualizations verify that it can effectively reduce the modality gap.

---

## 论文详细总结（自动生成）

# CaReFlow 论文结构化总结

## 1. 核心问题与整体含义（研究动机与背景）

- **模态鸿沟（modality gap）**：由于模态异质性（视觉/声学/语言）与特征提取器差异，不同模态的特征在空间中落在互不对齐的区域，严重制约多模态融合效果。
- **现实后果**：论文图 1 显示，朴素多模态模型（特征拼接 + MLP）在 CMU-MOSI 上甚至**不如纯语言单模态模型**，说明直接融合无法建模跨模态复杂依赖，泛化能力差。
- **现有方法的局限**：
  - 对比学习、多模态 Transformer、GAN、扩散模型等多聚焦于**样本内一对一映射**；
  - 未让源模态数据点接触目标模态的**全局分布信息**，难以学到整体、鲁棒的模态对齐；
  - 受限于每个样本内可用的模态配对数量不足；
  - 扩散模型推理慢，递归式整流流训练计算代价高。
- **整体含义**：论文将 MAC（多模态情感计算）中的模态鸿沟问题**重新表述为分布映射任务**，首次把整流流（rectified flow）引入该领域，为跨模态对齐提供了分布层面的新工具。

## 2. 方法论

### 2.1 核心思想
- 利用整流流"以近似直线轨迹将一个分布映射到另一个分布"的特性，将视觉、声学模态的分布映射到语言模态分布（语言被视为主导模态）。
- 在潜特征空间操作，降低运行时间并使分布映射更易实现。
- 提出 **CaReFlow = 一对多映射 + 自适应松弛对齐 + 循环整流流**。

### 2.2 关键技术细节

- **整流流基础**：定义插值 $X^t_{m_1,m_2}=(1-t)X_{m_1}+tX_{m_2}$，学习漂移力（速度场）$V_{m_1,m_2}$，通过最小二乘回归让 $V$ 逼近方向 $(X_{m_2}-X_{m_1})$；推理时用欧拉步解 ODE，从源分布转移到目标分布。
- **一对多映射**：训练时除样本内配对外，随机采样大量**跨样本**模态对，使每个源数据点能"看到"目标模态的整体分布，缓解配对数据不足，实现更鲁棒的分布变换。
- **自适应松弛对齐**（解决一对多映射中的流向歧义）：
  - 损失改为带 margin 的 hinge 形式：$\max(\|V_{m_1,m_2}(X^t,t)-(X_{m_2}-X_{m_1})\|^2-\eta_{m_1,m_2},\ 0)$；
  - margin 设定：同一样本 $\eta=0$（严格对齐）；不同样本同类别 $\eta=\epsilon$（松弛）；不同类别 $\eta=\epsilon+\|y_i-y_j\|^2$（更松弛）；
  - 效果：既保留全局分布视野，又引导模型关注相关性更高的目标点，**无需递归多轮训练**即可获得良好对齐。
- **循环整流流**（防止源模态信息丢失）：
  - 构造反向整流流，把前向输出 $X_{m_1,m_2}$ 映射回原始特征 $X_{m_1}$；
  - 仅在同一样本内构造配对；对 $X_{m_1}$ 做 detach、对 $X_{m_1,m_2}$ 不做 detach，使反向损失能反哺前向流，促使前向变换保留模态特有信息。
- **实现细节**：
  - 用 2 个欧拉步（$dt=0.5$）生成 $X_{m,l}$，推理时**不使用目标模态特征**，形成源→目标的因果信息流；
  - 时间嵌入采用 Transformer 式正弦/余弦函数（无额外可学习参数），与特征拼接后经简单 MLP 输出速度场。
- **总优化目标**：主任务损失 + 前向整流流损失（权重 $\alpha_f$）+ 反向损失（权重 $\alpha_b$）；融合与预测仅用简单特征拼接 + MLP。

## 3. 实验设计

- **数据集 / 场景**（共 5 个，覆盖 3 类任务）：
  - 多模态情感分析（MSA）：CMU-MOSI、CMU-MOSEI、CH-SIMS-v2；
  - 多模态幽默检测（MHD）：UR-FUNNY；
  - 多模态讽刺检测（MSD）：MUStARD。
- **Benchmark 与指标**：以公开基准数据集与标准指标为准，包括 Acc7 / Acc5 / Acc3 / Acc2、F1、MAE、Corr。
- **对比方法**：
  - 主任务基线：Self-MM、C-MIB、DMD、DEVA、AtCAF、EMOE、Multimodal Boosting、ITHP、DLF、MISA、MAG-BERT、MMIM、AV-MC、KuDA、MulT、DMD+SuCI、MAG-XLNet、MCL、MGCL、MULOT、MIL、MO-Sarcation 等；
  - 分布对齐方法（同架构公平对比）：ARGF（GAN）、Deep CCA、CLGSI（对比学习）、MulT、Diffusion Bridge（扩散）；
  - 融合方法对比：Tensor Fusion、Graph Fusion、Low-rank Modality Fusion、CubeMLP 与默认简单融合。
- **消融实验**（4 组）：去掉分布对齐、去掉循环信息流、去掉自适应松弛对齐、去掉一对多映射。
- **其他分析**：4 个关键超参（样本比 $\beta$、欧拉步数 $1/dt$、$\alpha_f$、$\alpha_b$）的敏感性分析；t-SNE 单模态分布可视化；参数量对比。

## 4. 资源与算力

- **论文正文未报告**具体 GPU 型号、数量、训练时长或显存占用等算力信息，仅在实验附录承诺提供实验设置（正文受篇幅限制未展开）。
- 可间接获得的信息：
  - 仅报告了**模型参数量**对比（CaReFlow 约 185.38M，与 ARGF、Deep CCA、CLGSI、MulT、Diffusion Bridge 同量级）；
  - 强调在潜空间操作可显著降低运行时间，且通过自适应松弛对齐**避免递归多轮训练**、仅需 2 个欧拉步，从而降低计算成本。
- 因此，关于训练/推理的实际算力开销，**该总结无法给出确切结论**，属论文未充分披露的部分。

## 5. 实验数量与充分性

- **实验规模**：5 个数据集 × 多类任务 + 4 组消融 + 2 组横向对比（分布对齐方法、融合方法）+ 4 个超参敏感性分析 + t-SNE 可视化，整体实验量较充分。
- **充分性**：
  - 跨 MSA/MHD/MSD 三类任务验证泛化性，覆盖面较好；
  - 消融逐项验证了四个核心组件的贡献，逻辑清晰；
  - 超参分析显示方法在较宽取值范围内稳定优于基线，鲁棒性有说服力。
- **公平性**：
  - 与分布对齐方法的对比在**同一主干架构**下重实现，参数规模相近，声称提升不是来自参数量增加；
  - 但部分对比结果标注来自原论文（†），与自跑结果混用，存在评测协议差异的潜在风险；
  - 在部分指标上优势有限（如 CMU-MOSEI Acc7 为 55.7，与 CLGSI 持平；CH-SIMS-v2 部分指标与 Tensor Fusion 融合后差距不大），说明提升并非在所有设定下都显著。
- **客观性**：结论有消融与可视化支撑，论证链条较完整；但可视化以定性为主，缺少模态鸿沟的定量度量（如分布距离指标）。

## 6. 主要结论与发现

- 在 CMU-MOSI 上，Acc7/Acc2 超过 SOTA 基线 DLF 1 分以上；在 CMU-MOSEI 上取得 Acc2、F1、MAE、Corr 最佳；在 CH-SIMS-v2 上**所有指标全面超越**基线（Acc5 提升 4 分以上）。
- 在 UR-FUNNY 与 MUStARD 上分别超过最佳基线 AtCAF 约 3 分、MO-Sarcation 约 2.5 分，验证跨任务泛化性。
- 消融显示：**一对多映射贡献最大**（去除后 Acc2 下降约 3 分），循环信息流与自适应松弛对齐同样关键；去掉分布对齐后模型退化为普通多模态模型，性能明显下降。
- t-SNE 可视化表明：相比 ARGF、CLGSI、Diffusion Bridge 与 DLF，CaReFlow 更显著地缩小了模态间特征距离（论文指出前几类方法因主任务权重更高，分布对齐优化不足）。
- 即使使用简单拼接 + MLP 融合，CaReFlow 仍达 SOTA；换成 Tensor Fusion 等更强融合可进一步提升，说明方法与融合机制解耦。

## 7. 优点

- **问题重述有新意**：首次将模态鸿沟建模为分布映射问题并引入整流流，视角不同于主流对比学习/对抗/扩散路线。
- **三点设计针对性强**：一对多映射解决配对不足与全局分布视野缺失；自适应松弛对齐用标签距离调节对齐强度，同时缓解一对多的流向歧义并免去递归训练；循环整流流保证信息不丢失，兼顾对齐与模态特有信息保留。
- **效率友好**：仅 2 个欧拉步、无需多轮递归训练、潜空间操作、推理时无需目标模态特征（因果信息流）。
- **即插即用**：与融合机制解耦，可搭配多种融合网络；参数量与主流对齐方法相当，提升不依赖参数量堆叠。
- **实验较为扎实**：5 个数据集、3 类任务、逐组件消融、超参鲁棒性分析与可视化证据形成较完整证据链。

## 8. 不足与局限

- **算力信息缺失**：未报告 GPU 型号/数量/训练时长与推理延迟，实际部署成本难以评估；虽声称高效，但缺少与扩散方法的时延定量对比。
- **任务与模态覆盖有限**：仅在视频三模态（语言/视觉/声学）的 MAC 任务上验证，未涉及图像-文本、遥感-可见光等模态组合，跨域泛化性未知。
- **"语言为主导模态"假设**：方法默认将视觉/声学映射到语言分布，在语言非主导或模态缺失、噪声严重的场景下适用性存疑。
- **评测公平性风险**：部分基线结果引自原论文（†），与自实现结果混排；分布对齐基线在统一架构下重实现，可能受实现细节影响。
- **定量证据不足**：模态鸿沟缩小主要靠 t-SNE 定性展示，缺少分布距离（如 MMD、CKA）等量化指标；部分数据集上的领先幅度较小。
- **超参依赖**：$\beta$、$\alpha_f$、$\alpha_b$ 需调参，论文自身也指出精细调参（如 $\beta=7$）可进一步提升，说明默认设置非最优。
- **计算开销**：跨样本一对多采样引入额外配对构造与训练开销，论文未给出训练时间对比。

（完）
