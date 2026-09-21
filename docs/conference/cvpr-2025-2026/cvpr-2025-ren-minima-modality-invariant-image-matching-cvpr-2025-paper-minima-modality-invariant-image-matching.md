---
title: "MINIMA: Modality Invariant Image Matching"
title_zh: MINIMA：模态不变图像匹配
authors: "Ren, Jiangwei, Jiang, Xingyu, Li, Zizhuo, Liang, Dingkang, Zhou, Xin, Bai, Xiang"
date: 2025
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2025/papers/Ren_MINIMA_Modality_Invariant_Image_Matching_CVPR_2025_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 6.0
evidence: 处理模态鸿沟的统一跨模态图像匹配
tldr: 该文针对跨视角与跨模态图像匹配中由成像系统差异导致的模态鸿沟问题，指出现有方法泛化性不足。作者提出MINIMA统一匹配框架，通过构建可自由生成多模态、多场景且带精确匹配标签的大规模数据引擎，从数据规模扩展角度提升通用性能。实验显示其在多种跨模态匹配场景下取得更强泛化能力。该工作为可见光与热红外的跨模态对齐提供了可迁移的基础方法。
source: CVPR-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-ren-minima-modality-invariant-image-matching-cvpr-2025-paper/fig-001.webp\", \"caption\": \"\", \"page\": 2, \"index\": 1, \"width\": 480, \"height\": 384}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-ren-minima-modality-invariant-image-matching-cvpr-2025-paper/fig-002.webp\", \"caption\": \"\", \"page\": 2, \"index\": 2, \"width\": 480, \"height\": 465}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-ren-minima-modality-invariant-image-matching-cvpr-2025-paper/fig-003.webp\", \"caption\": \"\", \"page\": 4, \"index\": 3, \"width\": 1280, \"height\": 945}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-ren-minima-modality-invariant-image-matching-cvpr-2025-paper/fig-004.webp\", \"caption\": \"\", \"page\": 4, \"index\": 4, \"width\": 1280, \"height\": 945}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-ren-minima-modality-invariant-image-matching-cvpr-2025-paper/fig-005.webp\", \"caption\": \"\", \"page\": 4, \"index\": 5, \"width\": 1280, \"height\": 947}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-ren-minima-modality-invariant-image-matching-cvpr-2025-paper/fig-006.webp\", \"caption\": \"\", \"page\": 4, \"index\": 6, \"width\": 487, \"height\": 272}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-ren-minima-modality-invariant-image-matching-cvpr-2025-paper/fig-007.webp\", \"caption\": \"\", \"page\": 4, \"index\": 7, \"width\": 487, \"height\": 298}]"
motivation: 不同成像系统造成的模态鸿沟使跨模态图像匹配泛化困难，现有方法局限明显。
method: 提出统一跨模态匹配框架，并设计可生成多模态、多场景、带精确标签的大规模数据引擎。
result: 在多类跨模态匹配任务上表现出优于既有方法的泛化性能。
conclusion: 通过数据规模扩展可显著提升跨模态匹配的通用性，为跨模态对齐奠定基础。
---

## Abstract
Image matching for both cross-view and cross-modality plays a critical role in multimodal perception. In practice, the modality gap caused by different imaging systems/styles poses great challenges to the matching task. Existing works try to extract invariant features for specific modalities and train on limited datasets, showing poor generalization. In this paper, we present MINIMA, a unified image matching framework for multiple cross-modal cases. Without pursuing fancy modules, our MINIMA aims to enhance universal performance from the perspective of data scaling up. For such purpose, we propose a simple yet effective data engine that can freely produce a large dataset containing multiple modalities, rich scenarios, and accurate matching labels. Specifically, we scale up the modalities from cheap but rich RGB-only matching data, by means of generative models. Under this setting, the matching labels and rich diversity of the RGB dataset are well inherited by the generated multimodal data. Benefiting from this, we construct MD-syn, a new comprehensive dataset that fills the data gap for general multimodal image matching. With MD-syn, we can directly train any advanced matching pipeline on randomly selected modality pairs to obtain cross-modal ability. Extensive experiments on in-domain and zero-shot matching tasks, including 19 cross-modal cases, demonstrate that our MINIMA can significantly outperform the baselines and even surpass modality-specific methods. The dataset and code are available at https://github.com/LSXI7/MINIMA

---

## 论文详细总结（自动生成）

# MINIMA: Modality Invariant Image Matching 论文中文总结

## 1. 核心问题与整体含义
- **研究背景**：跨视角、跨模态图像匹配是多模态感知的基础任务，广泛用于图像融合、视觉定位/导航、目标检测/识别/跟踪等。
- **核心问题**：不同成像系统/风格造成显著“模态鸿沟”，例如 RGB-IR、RGB-Depth、RGB-Event、Optical-SAR 等，使同一模型难以统一处理多种跨模态匹配。
- **现有不足**：
  - 多数方法聚焦 RGB-only 匹配，跨模态数据集规模小、场景覆盖有限、模态种类少。
  - 跨模态匹配常依赖人工标注或相机标定生成近似标签，成本高、标签质量受限。
  - 已有跨模态方法多针对特定模态训练，泛化能力弱，难以统一适配多种跨模态场景。
- **论文含义**：作者提出 MINIMA，一个统一的跨模态图像匹配框架，核心不是设计复杂模块，而是通过“数据规模化”填补跨模态匹配的数据缺口，从而提升通用匹配性能和零样本泛化能力。

## 2. 方法论
- **核心思想**：从廉价且丰富的 RGB-only 匹配数据出发，利用生成模型扩展出大规模、多模态、多场景且带精确匹配标签的数据集，再训练/微调任意先进匹配 pipeline，获得跨模态能力。
- **数据引擎**：
  - **源数据**：选用 MegaDepth 的 RGB 多视角图像对，因其户外场景丰富、标签精确、常用于匹配模型预训练。
  - **引导数据**：使用公开对齐的真实跨模态图像对，如 LLVIP、M3FD 等，用于微调生成模型。
  - **生成模态**：共考虑 6 类目标模态，与 RGB 组合后形成 7 种模态：
    - Infrared：基于 StyleBooth，用 LoRA rank 256 微调，输入/输出统一 1024×1024。
    - Depth：直接使用 DepthAnything V2 large。
    - Event：按事件相机亮度变化模型模拟，随机设置对比阈值 \(C \in [0.05,0.5]\)、极性 \(p_k=\pm1\)，并加入随机轻微运动。
    - Normal：使用 DSINE 生成表面法向图。
    - Artistic：包括 oil paint 和 sketch，分别使用 Paint Transformer 与 Anime2Sketch。
  - **数据构造**：对每对 RGB 图像 \(\{A_0,B_0\}\)，生成多模态集合 \(A=\{A_i\}, B=\{B_i\}\)，构造 \(\{A_0,B_i\}\) 或 \(\{A_i,B_0\}\) 跨模态匹配对。
  - **规模**：MegaDepth 约 40M 图像对，扩展后得到约 480M 跨模态图像对，构成 **MD-syn** 数据集。
- **训练流程**：
  - **Stage 1 预训练**：在 RGB 多视角数据上预训练先进匹配模型至收敛，获得良好匹配先验。
  - **Stage 2 微调**：在随机选择的跨模态图像对上以小学习率微调，学习模态不变匹配能力。
  - 采用预训练+微调而非从头训练，因为跨模态数据方差大，从头训练难收敛；RGB 预训练可快速迁移。
- **基础模型**：选择稀疏、半密集、密集三类代表模型：
  - LightGlue → MINIMA LG
  - LoFTR → MINIMA LoFTR
  - RoMa → MINIMA RoMa
- **训练模态选择**：仅使用 RGB-IR、RGB-Depth、RGB-Normal 三类合成模态对训练，即可获得较好跨模态泛化。

## 3. 实验设计
- **数据集/场景**：
  - **MD-syn**：作者合成数据集，测试时每个跨模态 case 使用 1500 对图像，共 6 个跨模态 case。
  - **METU-VisTIR**：真实 RGB-IR 数据集，约 2590 对，带相机位姿。
  - **DIODE**：真实 RGB-Depth/Normal 数据集，约 27858 对全对齐图像。
  - **DSEC**：RGB-Event 视频数据集，选取 3 个序列生成约 100 对 RGB-Event 测试对。
  - **MMIM**：用于零样本评估，包括遥感领域 7 个跨模态 case 和医学领域 6 个跨模态 case。
  - 总计覆盖 **19 个跨模态 case**。
- **Benchmark/评价协议**：
  - 对双视图位姿数据：报告位姿误差 AUC，阈值 \(5^\circ,10^\circ,20^\circ\)。
  - 对单应性数据：报告四角点投影误差 AUC，阈值 \(3\text{px},5\text{px},10\text{px}\)。
  - 对齐图像对会施加合成单应性以模拟形变，再尝试恢复单应性。
  - 所有图像长边统一 resize 到 640；统一使用 RANSAC 作为鲁棒估计器；评估在单张 RTX 3090 上完成。
- **对比方法**：
  - **稀疏匹配**：SuperGlue、LightGlue、OmniGlue、GIM LG、ReDFeat，以及 RIFT、SRIT、LNIFT 等手工跨模态方法。
  - **半密集匹配**：LoFTR、ELoFTR、XoFTR、GIM LoFTR。
  - **密集匹配**：DKM、GIM DKM、RoMa。
  - 其中 XoFTR、ReDFeat 为跨模态方法，OmniGlue 以泛化能力著称。
- **实验类型**：
  - MD-syn 合成数据全结果。
  - 真实 RGB-IR 域内测试。
  - 真实 RGB-Depth 域内测试。
  - 医学、遥感、RGB-Event 零样本测试。
  - 消融实验。

## 4. 资源与算力
- **匹配模型训练**：使用 **4 张 RTX 3090 GPU**，LightGlue、LoFTR、RoMa 的 batch size 分别为 **32、8、12**。
- **生成模型微调**：StyleBooth 微调使用 **单张 GPU**，训练 **210k steps**，固定学习率 \(1\times10^{-4}\)，batch size 为 2，输入/输出分辨率 1024×1024。
- **评估**：所有精度和运行时实验在 **单张 RTX 3090** 上完成。
- **未明确说明**：论文未给出完整训练总时长、总 GPU 小时数、数据生成总耗时等细节。

## 5. 实验数量与充分性
- **实验数量**：
  - MD-syn
