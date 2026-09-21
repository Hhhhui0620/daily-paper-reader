---
title: "CRFT: Consistent-Recurrent Feature Flow Transformer for Cross-Modal Image Registration"
title_zh: CRFT：用于跨模态图像配准的一致循环特征流Transformer
authors: "Liu, Xuecong, Ding, Mengzhu, Sun, Zixuan, Li, Zhang, Teng, Xichao"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Liu_CRFT_Consistent-Recurrent_Feature_Flow_Transformer_for_Cross-Modal_Image_Registration_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 7.0
evidence: 跨模态图像配准处理未对齐模态对
tldr: 针对跨模态图像因成像差异难以精确配准的问题，本文提出一致循环特征流Transformer（CRFT）。方法在Transformer中学习模态无关的特征流表示，通过由粗到细的多尺度相关与层次特征融合，并用迭代差异引导注意力与空间几何变换循环优化流场。实验表明该方法能稳健建立跨模态全局与局部对应关系。其贡献在于为未配准的多模态图像提供了统一的特征对齐与配准框架。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 4, \"index\": 1, \"width\": 693, \"height\": 524}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 4, \"index\": 2, \"width\": 712, \"height\": 516}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 4, \"index\": 3, \"width\": 959, \"height\": 960}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 6, \"index\": 4, \"width\": 1209, \"height\": 642}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 7, \"index\": 5, \"width\": 1369, \"height\": 690}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 7, \"index\": 6, \"width\": 1368, \"height\": 686}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 7, \"index\": 7, \"width\": 1369, \"height\": 680}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 7, \"index\": 8, \"width\": 1369, \"height\": 684}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 7, \"index\": 9, \"width\": 1368, \"height\": 686}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 7, \"index\": 10, \"width\": 1368, \"height\": 686}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 7, \"index\": 11, \"width\": 1369, \"height\": 686}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 7, \"index\": 12, \"width\": 1369, \"height\": 682}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 7, \"index\": 13, \"width\": 1369, \"height\": 683}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 7, \"index\": 14, \"width\": 1369, \"height\": 685}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 7, \"index\": 15, \"width\": 1369, \"height\": 682}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 7, \"index\": 16, \"width\": 1369, \"height\": 682}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 7, \"index\": 17, \"width\": 1370, \"height\": 684}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 7, \"index\": 18, \"width\": 1369, \"height\": 682}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 7, \"index\": 19, \"width\": 1370, \"height\": 682}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-020.webp\", \"caption\": \"\", \"page\": 7, \"index\": 20, \"width\": 1369, \"height\": 682}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-021.webp\", \"caption\": \"\", \"page\": 7, \"index\": 21, \"width\": 1022, \"height\": 510}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-022.webp\", \"caption\": \"\", \"page\": 7, \"index\": 22, \"width\": 1022, \"height\": 510}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-023.webp\", \"caption\": \"\", \"page\": 7, \"index\": 23, \"width\": 1019, \"height\": 505}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-024.webp\", \"caption\": \"\", \"page\": 7, \"index\": 24, \"width\": 1021, \"height\": 506}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-025.webp\", \"caption\": \"\", \"page\": 7, \"index\": 25, \"width\": 1328, \"height\": 850}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-026.webp\", \"caption\": \"\", \"page\": 7, \"index\": 26, \"width\": 1327, \"height\": 852}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crft-consistent-recurrent-feature-flow-transformer-for-cross-modal-image-registration-cvpr-2026-paper/fig-027.webp\", \"caption\": \"\", \"page\": 8, \"index\": 27, \"width\": 1320, \"height\": 852}]"
motivation: 跨模态图像存在显著外观与几何差异，难以建立精确的空间对应关系。
method: 提出由粗到细的特征流Transformer，联合进行特征对齐与光流估计，并用迭代差异引导注意力循环优化。
result: 多尺度相关与层次融合提升了全局对应与局部细节配准精度。
conclusion: 为未配准多模态图像提供了稳健的统一配准与特征对齐框架。
---

## Abstract
We present Consistent-Recurrent Feature Flow Transformer (CRFT), a unified coarse-to-fine framework based on feature flow learning for robust cross-modal image registration. CRFT learns a modality-independent feature flow representation within a transformer-based architecture that jointly performs feature alignment and flow estimation. The coarse stage establishes global correspondences through multi-scale feature correlation, while the fine stage refines local details via hierarchical feature fusion and adaptive spatial reasoning. To enhance geometric adaptability, an iterative discrepancy-guided attention mechanism with a Spatial Geometric Transform (SGT) recurrently refines the flow field, progressively capturing subtle spatial inconsistencies and enforcing feature-level consistency. This design enables accurate alignment under large affine and scale variations while maintaining structural coherence across modalities. Extensive experiments on diverse cross-modal datasets demonstrate that CRFT consistently outperforms state-of-the-art registration methods in both accuracy and robustness. Beyond registration, CRFT provides a generalizable paradigm for multimodal spatial correspondence, offering broad applicability to remote sensing, autonomous navigation, and medical imaging. Code and datasets are publicly available at https://github.com/NEU-Liuxuecong/CRFT.

---

## 论文详细总结（自动生成）

# CRFT 论文中文总结

## 1. 核心问题与研究动机

- **研究背景**：跨模态图像配准（如光学–SAR、可见光–红外）是计算机视觉中的基础问题，支撑三维重建、视觉定位、自主导航、遥感分析等应用。
- **核心挑战**：
  - 不同成像机制（光学/SAR/红外/多光谱）导致严重的非线性外观差异和特征分布不一致；
  - 相机运动、尺度变化、视角差异带来复杂几何变换，使像素级对齐困难；
  - 传统基于手工特征或强度驱动的方法对旋转、尺度、仿射变化敏感，在强非线性强度偏移或低纹理条件下失效；
  - 主流光流模型（RAFT、GMFlow 等）依赖光度一致性假设，在模态鸿沟下容易崩溃。
- **整体含义**：论文提出 CRFT，将跨模态配准统一建模为**可学习的、模态无关的特征流估计任务**，在 Transformer 架构中联合进行特征对齐与流估计，实现从全局结构到局部细节的鲁棒配准，并为多模态空间对应提供通用范式。

## 2. 方法论

### 核心思想
- 统一的**由粗到细（coarse-to-fine）**框架，学习模态无关的特征流表示，避免依赖光度一致性。
- 通过多尺度相关性建立全局对应，再通过层次特征融合与迭代差异引导注意力精化局部流场。

### 关键技术细节

- **粗尺度流估计（1/8 分辨率）**
  - 共享 ResNet 编码器在 1/2、1/4、1/8 三个尺度提取特征，粗匹配在 1/8 尺度进行以获取对光谱/辐射差异不敏感的高层结构。
  - 引入 Transformer 块（自注意力 SA + 交叉注意力 CA）：SA 稳定像素–上下文嵌入，CA 显式对齐模态相关特征。
  - 全局相关计算：对特征做线性投影与归一化后，计算相关性并通过 softmax 得到匹配概率，进而加权得到粗对应与粗流（式 1–5）。

- **细尺度流精化**
  - 多尺度局部特征聚合：在 1/4 和 1/2 特征图上分别用 5×5、3×3 窗口建立跨尺度对应路径。
  - 层次注意力精化：先用窗口自注意力增强局部几何一致性，再用交叉注意力对齐模态响应，逐级注入高频细节。

- **差异引导流优化（DGFO，核心创新）**
  - **FSFT**：用轻量 MLP（两层线性 + GELU）将细尺度特征投影到同质特征空间，降低模态外观差异。
  - **迭代流程**：每次迭代用当前流通过 **SGT（空间几何变换）** 对 B 模态特征做 warp，计算特征差异 ΔF，取反作为可靠性线索 F_attn = 1 − ΔF。
  - 以 F_attn 生成 Query/Key，当前流作为 Value，在局部邻域内做注意力聚合得到 T′；再经 CNN 编码器估计残差流 ΔT，更新 T^{i+1} = T′ + ΔT。
  - **局部流聚合与置信度平滑**：CENet 预测置信图，选取最高置信流并做加权平滑，最后上采样至全分辨率。

- **损失函数**
  - 粗尺度流损失 L_c（下采样 GT 的 L1）。
  - 迭代细尺度损失 L_f：每次迭代独立 L1 监督，按几何衰减权重 γ^{N−i}（γ=0.9）聚合，使后期更精确预测获得更大权重。
  - 总损失 L_total = λ_c L_c + λ_f L_f。

## 3. 实验设计

- **数据集 / 场景**
  - **OSdataset**：2673 对光学–SAR 配准图像，划分 2011/238/424（训练/验证/测试）。
  - **RoadScene**：221 对可见光–红外道路场景图像，划分 176/23/22。
  - 图像统一缩放至 512×512；训练时随机裁剪 64×64 patch，并施加随机缩放 [0.9,1.1]、旋转 [−45°,45°]、最多 30 像素平移。

- **评估指标（Benchmark）**
  - **AEPE**（平均端点误差，越低越好）。
  - **CMR**（正确匹配率），阈值 τ = 3、1、0.7 px，并绘制 0.1–5 px 的 CMR 曲线。

- **对比方法**（覆盖三大类共 10 种）
  - 稀疏/手工方法：HOWP、LNIFT、MSG、RIFT2。
  - 半稠密方法：XoFTR（+Flow）。
  - 稠密/光流方法：ADRNet、GMFlow、RAFT、GDROS。
  - 所有基线均经微调以保证公平比较。

- **消融实验**：以 XoFTR 为基线，逐步加入 L1 损失、粗流估计（FE）、迭代差异引导优化（IDGO）、迭代损失（IL），共 5 组配置。

## 4. 资源与算力

- **GPU**：单张 RTX 4090。
- **训练时长**：OSdataset 约 4.0 小时，RoadScene 约 0.65 小时，端到端训练。
- **模型规模**：11.96M 参数，11.47 GFLOPs，推理速度 0.033 s/pair。
- **DGFO 开销**：每迭代仅增加 0.93M 参数、1.90 GFLOPs、0.10 ms。
- **说明**：文中未明确提及使用的 GPU 数量（仅提及 RTX 4090），也未给出完整训练轮数等超参细节。

## 5. 实验数量与充分性

- **实验组数**：
  - 2 个数据集上的完整定量对比（表 1、表 2）。
  - CMR 曲线对比（图 5）。
  - 定性可视化对比（图 3、图 4）。
  - 1 组 5 配置的消融实验（表 3、图 6）。
  - 效率分析（参数量、FLOPs、耗时）。
- **充分性评价**：
  - **优点**：覆盖光学–SAR 与可见光–红外两类典型跨模态场景；基线涵盖手工、稀疏、半稠密、稠密四类，比较维度较全面；消融逐模块验证贡献，逻辑清晰。
  - **不足**：数据集数量偏少（仅 2 个），RoadScene 测试集仅 22 对，统计代表性有限；消融实验为控制基线失败而将旋转限制在 30°（主实验为 45°），与主实验设定不完全一致；未见跨数据集泛化实验或对更大尺度/更多模态的验证。

## 6. 主要结论与发现

- CRFT 在两个数据集上均取得最优 AEPE 与最高严格阈值 CMR。
  - **OSdataset**：AEPE 0.65（唯一亚像素结果），较次优 XoFTR+Flow（1.13）提升 42.5%；CMR@0.7px 达 89.9%，为 ADRNet 的 4.36 倍、GDROS 的 2.53 倍、XoFTR+Flow 的 2.15 倍。
  - **RoadScene**：AEPE 2.37，较 ADRNet（4.72）提升 49.8%，较 GMFlow（12.02）提升 80.3%；CMR@1px 为 18.2%，领先 RAFT（14.1%）与 ADRNet（9.4%）。
- 手工特征方法与光流基线在跨模态强差异下严重退化（严格阈值下 CMR 常降至 0）。
- 消融表明：IDGO 是亚像素精度的关键（CMR@0.7px 从 73.3% 提升至 88.9%），迭代损失 IL 进一步提升后期精化稳定性（最终 93.1%）。
- 结论：CRFT 在全局结构一致性与局部精细精度之间取得更优平衡，为多模态空间对应提供可扩展方案。

## 7. 优点

- **方法层面**：
  - 明确摆脱光流的光度一致性假设，学习模态无关的特征流，思路新颖且针对性强。
  - 差异引导注意力 + SGT 的迭代循环优化，能显式利用特征差异驱动几何校正，适合非线性与仿射变形。
  - 粗到细 + 多尺度窗口聚合设计，兼顾全局结构稳定与局部高频细节。
  - DGFO 模块轻量（每迭代仅 0.93M 参数），整体效率较高（0.033 s/pair）。
- **实验层面**：
  - 基线覆盖四类方法，且均经微调，公平性较好。
  - 采用 AEPE + 多阈值 CMR + CMR 曲线，评估维度较完整。
  - 消融逐步叠加，清晰量化每个模块贡献。
  - 代码与数据集公开，可复现性较好。

## 8. 不足与局限

- **实验覆盖**：
  - 仅 2 个数据集，RoadScene 规模小（221 对，测试 22 对），统计结论稳健性存疑。
  - 缺少医学影像、多光谱等其他模态的验证，与摘要中“广泛适用性”的宣称尚有差距。
  - 未报告跨数据集/跨模态泛化实验。
- **偏差风险**：
  - 消融实验旋转设定（30°）与主实验（45°）不一致，可能影响结论可比性。
  - 初始化自 XoFTR 预训练权重，性能增益部分可能来自预训练，文中未做从头训练对照。
- **资源信息不完整**：未说明 GPU 数量、训练轮数、随机种子等细节。
- **应用限制**：
  - 主要面向遥感/道路场景的成对配准，对极端大视角、非刚性形变、遮挡场景的鲁棒性未充分讨论。
  - 依赖像素级对齐的 GT 流监督，实际中获取此类标注成本较高。
  - 迭代次数 N、损失权重 λ_c/λ_f、γ 等超参的敏感性分析缺失。

（完）
