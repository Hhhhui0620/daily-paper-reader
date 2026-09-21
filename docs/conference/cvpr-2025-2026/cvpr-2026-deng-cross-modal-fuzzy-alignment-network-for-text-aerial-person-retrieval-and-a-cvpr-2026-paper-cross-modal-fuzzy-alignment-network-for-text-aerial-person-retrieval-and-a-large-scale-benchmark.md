---
title: Cross-modal Fuzzy Alignment Network for Text-Aerial Person Retrieval and A Large-scale Benchmark
title_zh: 面向文本-航拍行人检索的跨模态模糊对齐网络及大规模基准
authors: "Deng, Yifei, Li, Chenglong, Zhang, Yuyang, Hu, Guyue, Tang, Jin"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Deng_Cross-modal_Fuzzy_Alignment_Network_for_Text-Aerial_Person_Retrieval_and_A_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 5.0
evidence: 模糊逻辑量化可靠性实现跨模态细粒度对齐
tldr: 航拍图像因视角与飞行高度剧变导致视觉信息退化，使文本与图像的语义对齐十分困难。本文提出跨模态模糊对齐网络CFANet，利用模糊逻辑量化令牌级可靠性以实现细粒度对齐，并引入地面视角图像作为桥接缓解航拍与文本间的差距。实验在大规模基准上提升了检索对齐精度。其以可靠性量化驱动跨模态对齐的思路对不确定性感知对齐具有借鉴价值。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-deng-cross-modal-fuzzy-alignment-network-for-text-aerial-person-retrieval-and-a-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 1896, \"height\": 2040}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-deng-cross-modal-fuzzy-alignment-network-for-text-aerial-person-retrieval-and-a-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 4, \"index\": 2, \"width\": 4752, \"height\": 2136}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-deng-cross-modal-fuzzy-alignment-network-for-text-aerial-person-retrieval-and-a-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 6, \"index\": 3, \"width\": 6201, \"height\": 1371}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-deng-cross-modal-fuzzy-alignment-network-for-text-aerial-person-retrieval-and-a-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 6, \"index\": 4, \"width\": 1719, \"height\": 1158}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-deng-cross-modal-fuzzy-alignment-network-for-text-aerial-person-retrieval-and-a-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 8, \"index\": 5, \"width\": 1753, \"height\": 977}]"
motivation: 航拍图像因视角与飞行高度剧变导致视觉信息退化，与文本的语义对齐困难。
method: 提出跨模态模糊对齐网络CFANet，用模糊逻辑量化令牌级可靠性实现细粒度对齐，并引入地面图像作桥接。
result: 在大规模基准上提升了文本-航拍行人检索的对齐精度。
conclusion: 以可靠性量化缓解航拍跨模态对齐难题，具借鉴意义。
---

## Abstract
Text-aerial person retrieval aims to identify targets in UAV-captured images from eyewitness descriptions, supporting intelligent transportation and public security applications. Compared to ground-view text-image person retrieval, UAV-captured images often suffer from degraded visual information due to drastic variations in viewing angles and flight altitudes, making semantic alignment with textual descriptions very challenging. To address this issue, we propose a novel Cross-modal Fuzzy Alignment Network (CFANet), which quantifies the token-level reliability by fuzzy logic to achieve accurate fine-grained alignment and incorporates ground-view images as a bridge agent to further mitigate the gap between aerial images and text descriptions, for text-aerial person retrieval. In particular, we design the Fuzzy Token Alignment module that employs the fuzzy membership function to dynamically model token-level association strength and suppress the influence of unobservable or noisy tokens. It can alleviate the semantic inconsistencies caused by missing visual cues and significantly enhance the robustness of token-level semantic alignment. Moreover, to further mitigate the gap between aerial images and text descriptions, we design a Context-Aware Dynamic Alignment module to incorporates the ground-view agent as a bridge in text-aerial alignment and adaptively combine direct alignment and agent-assisted alignment to improve the robustness. In addition, we construct a large-scale benchmark dataset called AERI-PEDES by using a chain-of-thought to decompose text generation into attribute parsing, initial captioning, and refinement, thus boosting textual accuracy and semantic consistency. Experiments on AERI-PEDES and TBAPR demonstrate the superiority of our method. The code and dataset will be publicly released.

---

## 论文详细总结（自动生成）

# 论文总结：Cross-modal Fuzzy Alignment Network for Text-Aerial Person Retrieval and A Large-scale Benchmark

## 1. 核心问题与研究动机

- **任务背景**：文本-航拍行人检索（Text-Aerial Person Retrieval, TAPR）旨在根据目击者描述，从无人机（UAV）拍摄的图像中检索目标行人，服务于智能交通、公共安全与安防监控等应用。
- **核心挑战**：
  - 与地面固定摄像头不同，UAV 图像因**拍摄角度与飞行高度的剧烈变化**，导致外观、姿态、几何比例出现非线性畸变，视觉信息严重退化。
  - 查询文本通常来自目击者描述，包含**完整且细粒度**的行人属性；而航拍图像中的视觉线索往往**稀疏甚至部分缺失**（受高度、视角偏差、遮挡影响）。
  - 这种"可见性不一致"导致部分文本 token 找不到有效的视觉对应，从而引入**错误的跨模态对齐**。
- **整体含义**：论文首次系统性地将模糊逻辑引入 TAPR 任务，通过量化 token 级可靠性来抑制不可观测/噪声 token，并借助地面视角图像作为桥接，缓解航拍图像与文本之间的语义鸿沟。

## 2. 方法论

### 2.1 核心思想
提出 **Cross-Modal Fuzzy Alignment Network (CFANet)**，由两个模块组成：
- **Context-Aware Dynamic Alignment (CDA)**：在样本级动态平衡"直接对齐"与"桥接对齐"。
- **Fuzzy Token Alignment (FTA)**：在 token 级用模糊隶属度函数量化可靠性，实现鲁棒细粒度对齐。

整体流程：使用共享 CLIP 图像编码器提取航拍特征 $A$ 与地面特征 $G$，CLIP 文本编码器提取文本特征 $T$。

### 2.2 Context-Aware Dynamic Alignment (CDA)
- 计算每个样本的跨模态相似度差异：
  $$\Delta_i = \text{sim}(T_i^C, A_i^C) - \text{sim}(T_i^C, G_i^C)$$
- 通过 Sigmoid 映射为连续系数 $\alpha_i \in [0,1]$：
  $$\alpha_i = \frac{1}{1 + \exp(-k \cdot \Delta_i)}$$
  其中 $k$ 为敏感度超参数。$\alpha_i \to 1$ 时强调直接文本-航拍对齐；$\alpha_i \to 0$ 时强调经地面图像桥接的对齐。
- CDA 损失：
  $$L_{CDA} = \frac{1}{B}\sum_{i=1}^{B}\left[\alpha_i \cdot L_{direct}(T_i^C, A_i^C) + (1-\alpha_i) \cdot L_{bridge}(T_i^C, G_i^C, A_i^C)\right]$$
- 其中 $L_{direct} = \text{SDM}(T_i^C, A_i^C)$，$L_{bridge} = \text{SDM}(T_i^C, G_i^C) + \text{SDM}(\text{sg}(G_i^C), A_i^C)$，$\text{sg}(\cdot)$ 为停止梯度算子，防止地面特征被反向传播修改。
- 当无地面图像时，CDA 损失退化为标准 SDM 损失。

### 2.3 Fuzzy Token Alignment (FTA)
- 引入共享可学习查询 $Q \in \mathbb{R}^{K \times D}$，分别与图像、文本交互：
  $$Q_a = \text{CrossFormer}(Q, A, A), \quad Q_t = \text{CrossFormer}(Q, T, T)$$
- 以全局 class token 为语义参考，用 MLP 预测高斯尺度：$\log\sigma = \text{MLP}(A^C)$，$\sigma = \exp(\log\sigma)$。
- 计算每个查询 token 与 class token 的相似度 $r_j$，并映射为高斯隶属度：
  $$r_j = \frac{Q_a^{(j)\top} \cdot A^C}{\|Q_a^{(j)}\|_2 \|A^C\|_2}, \quad \mu_j^a = \exp\left(-\frac{(1-r_j)^2}{2\sigma^2}\right)$$
  文本模态 $\mu_j^t$ 类似计算。
- 通过模糊逻辑 AND 操作融合双模态隶属度（乘法形式作为可微软 AND）：
  $$\mu_j^{joint} = \mu_j^a \cdot \mu_j^t$$
- 用联合隶属度加权 token 级余弦相似度，得到样本级相似度：
  $$\text{sim}(Q_a, Q_t) = \frac{1}{K}\sum_{j=1}^{K} \mu_j^{joint} \cdot s_j$$
- 采用 SDM 损失计算最终模糊 token 对齐损失 $L_{FTA}$，其中相似度分布匹配项含温度参数 $\tau$ 与数值稳定项 $\epsilon$。

## 3. 实验设计

### 3.1 数据集与 Benchmark
- **AERI-PEDES（本文构建）**：
  - 包含 4,659 个身份、144,548 张行人图像，来源为三个航拍-地面行人重识别数据集。
  - 训练集：3,659 身份、112,672 张航拍图像、26,351 张地面图像、26,213 条生成描述。
  - 测试集：1,000 身份、5,525 张航拍图像、6,141 条**人工标注**描述。
  - 标题平均长度 38.6 词，最大 108 词；训练标题由 **Chain-of-Thought (CoT)** 框架生成（属性解析 → 初始标题 → 精炼），测试标题人工标注以保证真实性。
- **TBAPR**：首个 TAPR 基准，含 65,880 张行人图像，训练集 1,180 身份，测试集 529 身份。

### 3.2 评估指标
- Rank-1、Rank-5、Rank-10、mAP、RSum（Sum of Rank）。

### 3.3 对比方法
- IRRA (CVPR23)、APTM (MM23)、RDE (CVPR24)、CFAM (CVPR24)、NAM (CVPR24)、VFE (KBS25)、DM-Adapter (AAAI25)、LPNC / LPNC+Pretrain (TIFS25)、AEA-FIRM / AEA-FIRM+Pretrain (TCSVT25)、HAM (CVPR25)。

## 4. 资源与算力

- **GPU**：单张 **RTX 4090**。
- **训练配置**：Adam 优化器，60 个 epoch，初始学习率 $5 \times 10^{-6}$，余弦衰减，batch size 64。
- **输入尺寸**：图像统一 resize 至 $384 \times 128$；文本使用随机掩码增强。
- **FTA 查询**：4 个可学习的 512 维 token。
- **说明**：文中未明确提及训练总时长与显存占用细节。

## 5. 实验数量与充分性

- **主实验（2 个数据集）**：在 AERI-PEDES 与 TBAPR 上与 12 种 SOTA 方法对比（含无/有地面辅助两种设置）。
- **消融实验（AERI-PEDES）**：
  - Baseline、+CDA、+FTA、+CDA+FTA 共 4 组。
  - 不同桥接模态对比：None / Aerial / Ground 共 3 组。
- **参数敏感性分析**：
  - 可学习查询 token 数量（1–16）对 mAP 与 RSum 的影响。
  - CDA 中 $k$ 值（1, 2, 4, 8, 12, 16）的敏感性。
- **充分性评价**：
  - 实验覆盖两个数据集、多个 SOTA 方法、完整消融与参数分析，**整体较为充分**。
  - 对比方法来源年份跨度大（2023–2025），包含预训练与非预训练版本，**公平性较好**。
  - 但未报告多次运行的方差或统计显著性检验，且仅在单一 GPU 上训练，复现性验证有限。

## 6. 主要结论与发现

- **AERI-PEDES 上**：CFANet 在无地面辅助下即达到 Rank-1 45.06%、mAP 43.27%、RSum 182.80%；加入地面图像后达 Rank-1 47.16%、mAP 44.79%、RSum 186.65%，较此前最佳方法 RSum 提升近 6%。
- **TBAPR 上**：无地面辅助即达 Rank-1 49.15%、mAP 42.89%；加地面后 Rank-5 达 66.50%、RSum 189.03%，刷新 SoTA。
- **消融结论**：
  - CDA 显著提升（RSum +8.2%），能自适应平衡直接与桥接对齐。
  - FTA 单独带来 Rank-1/mAP/RSum 分别 +0.67%/+0.31%/+1.2%；叠加 CDA 后额外增益 +0.98%/+0.81%/+3.61%。
  - 桥接模态中 Ground 优于 Aerial，但差距不大，说明 CDA 可灵活使用不同桥接。
  - 查询 token 数为 4、$k=1$ 时性能最佳；过大 $k$ 使 Sigmoid 过陡，削弱细粒度调节能力。
- **数据集分析**：AERI-PEDES 的 CLIP 图文相似度分布比 CUHK-PEDES、RSTPReid 更宽，说明 CoT 生成的标题语义一致性更高。

## 7. 优点

- **方法创新**：
  - 首次将**模糊逻辑**系统引入 TAPR，用高斯隶属度量化 token 级可靠性，有效抑制不可观测/噪声 token。
  - 设计**地面图像桥接代理**，并通过可学习的动态门控自适应平衡直接与桥接对齐，思路新颖。
  - 停止梯度设计保证桥接对齐不污染地面表征，工程细节严谨。
- **数据贡献**：
  - 构建大规模 AERI-PEDES 基准（144K+ 图像、多源跨平台），训练用 CoT 生成、测试用人工标注，兼顾成本与真实性。
- **实验扎实**：
  - 两个数据集、12 种 SOTA 对比、完整消融与参数敏感性分析，结论可信。
  - 无地面辅助时仍超越所有对比方法，体现方法本身的鲁棒性。

## 8. 不足与局限

- **算力与复现**：仅单张 RTX 4090 训练，未报告训练时长、显存占用与多次运行方差，复现性与统计显著性证据不足。
- **地面图像依赖**：最佳性能仍依赖地面视角图像作为桥接；在实际部署中，地面图像未必总能获取（虽然作者指出可退化处理）。
- **数据集偏差风险**：
  - AERI-PEDES 由三个已有航拍-地面数据集拼接构建，可能存在场景/身份分布偏差。
  - 训练标题由 CoT 自动生成，可能仍存在属性遗漏或视觉幻觉；测试标题人工标注虽更真实，但规模有限（1,000 身份）。
- **应用限制**：
  - 方法针对航拍行人检索设计，是否可迁移至其他跨模态检索任务未验证。
  - 模糊隶属度中的高斯尺度 $\sigma$ 由 MLP 预测，其可解释性与稳定性缺乏深入分析。
  - 未讨论极端遮挡、低分辨率或夜间场景下的表现。
- **实验覆盖**：缺少与最新多模态大模型（MLLM）方法的直接对比；参数敏感性仅覆盖两个超参数。

（完）
