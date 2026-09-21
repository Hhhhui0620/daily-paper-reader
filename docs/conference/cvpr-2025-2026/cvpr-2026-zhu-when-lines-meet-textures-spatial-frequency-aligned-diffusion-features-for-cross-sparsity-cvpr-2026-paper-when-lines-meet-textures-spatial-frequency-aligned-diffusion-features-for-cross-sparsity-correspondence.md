---
title: "When Lines Meet Textures: Spatial-Frequency Aligned Diffusion Features for Cross-Sparsity Correspondence"
title_zh: 当线条遇见纹理：面向跨稀疏度对应的空频对齐扩散特征
authors: "Zhu, Mingrui, Wang, Fengzhi, Wei, Xin, Wang, Jun, Wang, Nannan, Gao, Xinbo"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Zhu_When_Lines_Meet_Textures_Spatial-Frequency_Aligned_Diffusion_Features_for_Cross-Sparsity_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 4.0
evidence: 双域对齐缓解跨模态空间错位的对应问题
tldr: 稀疏线条与富纹理图像之间的跨模态对应长期困难，本文指出其源于结构抽象带来的空间域错位与纹理密度差异造成的频域不一致。为此提出SFA-DIFT，学习空间-频率双域对齐的扩散特征，实现鲁棒的跨模态对应。实验表明该方法优于仅做空间对齐的既有方案。其双域对齐思路对未配准多模态特征融合具有迁移价值。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 591, \"height\": 296}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 591, \"height\": 300}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 591, \"height\": 296}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 1, \"index\": 4, \"width\": 591, \"height\": 296}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 1, \"index\": 5, \"width\": 591, \"height\": 296}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 1, \"index\": 6, \"width\": 591, \"height\": 296}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 7, \"index\": 7, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 7, \"index\": 8, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 7, \"index\": 9, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 7, \"index\": 10, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 7, \"index\": 11, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 7, \"index\": 12, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 7, \"index\": 13, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 7, \"index\": 14, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 7, \"index\": 15, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 7, \"index\": 16, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 7, \"index\": 17, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 7, \"index\": 18, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 7, \"index\": 19, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-020.webp\", \"caption\": \"\", \"page\": 7, \"index\": 20, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-021.webp\", \"caption\": \"\", \"page\": 7, \"index\": 21, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-022.webp\", \"caption\": \"\", \"page\": 7, \"index\": 22, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-023.webp\", \"caption\": \"\", \"page\": 7, \"index\": 23, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-024.webp\", \"caption\": \"\", \"page\": 7, \"index\": 24, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-025.webp\", \"caption\": \"\", \"page\": 7, \"index\": 25, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-026.webp\", \"caption\": \"\", \"page\": 7, \"index\": 26, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-027.webp\", \"caption\": \"\", \"page\": 7, \"index\": 27, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-028.webp\", \"caption\": \"\", \"page\": 7, \"index\": 28, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-029.webp\", \"caption\": \"\", \"page\": 7, \"index\": 29, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-030.webp\", \"caption\": \"\", \"page\": 7, \"index\": 30, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-031.webp\", \"caption\": \"\", \"page\": 7, \"index\": 31, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-032.webp\", \"caption\": \"\", \"page\": 7, \"index\": 32, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-033.webp\", \"caption\": \"\", \"page\": 7, \"index\": 33, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-034.webp\", \"caption\": \"\", \"page\": 7, \"index\": 34, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-035.webp\", \"caption\": \"\", \"page\": 7, \"index\": 35, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-036.webp\", \"caption\": \"\", \"page\": 7, \"index\": 36, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-037.webp\", \"caption\": \"\", \"page\": 7, \"index\": 37, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-038.webp\", \"caption\": \"\", \"page\": 7, \"index\": 38, \"width\": 538, \"height\": 269}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-039.webp\", \"caption\": \"\", \"page\": 7, \"index\": 39, \"width\": 551, \"height\": 275}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-040.webp\", \"caption\": \"\", \"page\": 7, \"index\": 40, \"width\": 551, \"height\": 275}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-041.webp\", \"caption\": \"\", \"page\": 7, \"index\": 41, \"width\": 551, \"height\": 275}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-zhu-when-lines-meet-textures-spatial-frequency-aligned-diffusion-features-for-cross-sparsity-cvpr-2026-paper/fig-042.webp\", \"caption\": \"\", \"page\": 7, \"index\": 42, \"width\": 550, \"height\": 275}]"
motivation: 稀疏线条与富纹理图像之间的跨模态对应存在空间错位与频域不一致两大鸿沟。
method: 提出SFA-DIFT，学习空间-频率双域对齐的扩散特征，实现鲁棒的跨模态对应。
result: 在跨稀疏度对应任务中优于仅做空间对齐的既有方法。
conclusion: 表明双域对齐对缓解跨模态空间错位具有通用价值。
---

## Abstract
Establishing accurate correspondence between sparse line representations and rich textured imagery remains a formidable challenge. While diffusion features excel in semantic correspondence, they struggle to bridge the fundamental gap between abstract sketches and texture-rich photographs. We identify two critical disparities: spatial domain misalignment from structural abstraction differences, and frequency domain inconsistencies from texture density variations. Based on this analysis, we propose SFA-DIFT, a novel approach that learns spatial-frequency aligned diffusion features for robust cross-modal correspondence. Unlike previous methods focusing solely on spatial alignment, our key innovation performs dual-domain alignment by learning unified clean diffusion features while strategically aggregating low-frequency components in the frequency domain. This comprehensive spatial-frequency alignment enables equitable understanding between sparse abstractions and rich textures. To validate our approach, we extend the existing sketch-photo correspondence dataset (PSC6K) by generating multi-style textured imagery, creating MS-PSC6K, a comprehensive correspondence benchmark. Extensive experiments demonstrate that SFA-DIFT achieves state-of-the-art performance, delivering substantial improvements with an average of 0.87% on PCK@1, 2.20% on PCK@5, and 0.95% on PCK@10 over previous best methods, validating the effectiveness and robustness of our dual-domain alignment approach. Codes are available on https://github.com/Mofr77/SFA-DIFT.

---

## 论文详细总结（自动生成）

# 论文总结：When Lines Meet Textures: Spatial-Frequency Aligned Diffusion Features for Cross-Sparsity Correspondence

## 1. 核心问题与整体含义

- **研究动机**：稀疏线条（草图/线稿）与富纹理图像（照片）之间的跨模态语义对应长期困难。人类可凭共享语义轻松建立对应，但算法难以跨越"视觉稀疏度鸿沟"。
- **两大核心差异**（论文的系统性分析）：
  - **空间域错位**：草图是认知选择性的稀疏抽象，只保留主轮廓，导致"稀疏性"（纹理区域无对应线条）与"错位"（线条位置偏离真实边界）。
  - **频域不一致**：照片能量广布于全频段；草图则表现为低频平台 + 高频尖峰 + 中频稀疏，造成跨模态频域对齐困难。
- **现有方法局限**：
  - 专用编码器因草图数据稀缺而泛化差；文本提示式学习无法解决特征分布差异。
  - Stable Diffusion 特征偏向纹理与外观，在纯线稿上出现"特征空洞"与噪声伪影。
  - CleanDIFT 虽通过去噪提升特征平滑度，但过度平滑削弱语义表达，且仍无法弥合跨模态频域差距。
- **整体含义**：有效的跨稀疏度对应需要**空间与频域的同时对齐**，为跨模态理解提供了新的分析框架。

## 2. 方法论：SFA-DIFT

### 核心思想
- 不同于以往仅做空间对齐的方法，SFA-DIFT 执行**双域对齐**：
  1. **Unified Clean Diffusion Feature Learning**：通过参数高效 LoRA 微调，将两模态映射到共享语义子空间，解决空间错位。
  2. **Low-Frequency Feature Aggregation (LoFFA)**：基于小波变换聚合低频分量，解决频域不匹配。

### 关键技术细节

**阶段一：Unified CleanDIFT**
- 在预训练 CleanDIFT 的 U-Net 所有线性投影层注入 LoRA，仅训练低秩矩阵 A、B：
  - `W' = W + ΔW`，其中 `ΔW = αBA`，秩 `r ≪ d`。
- **Teacher-Student 双路径训练**：
  - Teacher 路径：干净草图 `x0` 加噪得 `xt`，用冻结 SD 模型提取目标特征 `F_target`。
  - Student 路径：干净草图 `x0` 以固定时间步 `t' = 261` 输入 LoRA 增强模型，得到 `F_pred`。
  - 引入**时间步条件化的点向投影头**，输出 `F_proj`。
  - 统一文本提示 "a photo of a [class]"。
- **损失函数**：负余弦相似度
  - `L_ada = E[ -Σ_k cos(F_proj^(k), F_target^(k)) ]`
  - 通过全时间步采样，学习时间不变、跨模态统一的干净扩散特征。

**阶段二：LoFFA 模块**
- 输入：Unified CleanDIFT 与 DINOv2 提取的 L 层多尺度特征。
- 处理流程（每层）：
  1. 卷积降维 + AdaIN 将图像特征分布对齐到草图分布。
  2. **LoFE（低频增强）**：
     - 两级 DWT 分解，得到二级低频分量 `F_LL^(2)` 与各级高频分量。
     - Sigmoid 门控调制：`F̃_LL^(2) = F_LL^(2) ⊙ (1 + M)`，M 为可学习注意力掩码。
     - 通过可学习权重的 IDWT 重建，结合高低频分量。
     - 残差连接：`F_out = F_in + β(H(F_in) - F_in)`。
  3. 再次 AdaIN + 卷积得到精炼特征。
- **自适应加权求和**：`F̂ = Σ_l ω_l F'_l`，ω_l 为可学习标量。

**训练目标**
- `L_CL`：CLIP 式对称对比损失，拉近对应关键点、推远非对应点。
- `L_Dense`：稠密匹配损失，通过 Soft-Argmax 可微地预测目标位置，并加入高斯噪声正则。
- 总损失：`L = L_CL + L_Dense`。

## 3. 实验设计

### 数据集与 Benchmark
- **PSC6K**：1250 张照片，125 类，每类 5 张草图，15 万人工标注关键点。
- **MS-PSC6K**（论文提出）：在 PSC6K 基础上生成 5 种风格纹理图像（Abstract、Baroque、Realism、Post-Impressionism、Neo-Impressionism），共 7500 张纹理图，构成多风格对应基准。
- **Sketchy**：62500 张草图、125 类，用于将 CleanDIFT 微调为 Unified CleanDIFT。

### 评价指标
- **PCK@1 / @5 / @10**（α = 0.01 / 0.05 / 0.1，基于目标边界框尺寸）。
- **Robustness Ratio (RR)**（论文提出）：衡量纹理扰动前后性能比值，`RR > 1` 表示偏向多样风格而非照片。

### 对比方法
- 零样本方法：SD、CLIP、DINOv2-ViT-B/14、DINOv3-ViT-B/16、SD+DINO、Fuse2Match、CleanDIFT+DINO、Self-Sup、SketchFusion。
- 监督方法：GMRW-SC、Self-Sup‡、SketchFusion‡、CleanDIFT+DINO‡。
- 覆盖 PSC6K 主实验与 MS-PSC6K 五风格实验。

## 4. 资源与算力

- **论文未明确说明**所使用的 GPU 型号、数量、训练时长或总计算量。
- 仅提到推理效率：**平均每次对应估计耗时 0.8 秒**，作者在 Limitation 中承认扩散特征推理效率存在固有局限。
- 因此无法从文中评估训练成本与可复现性所需的算力门槛。

## 5. 实验数量与充分性

### 实验组数概览
- **主实验（PSC6K）**：1 组，对比约 10 种方法。
- **多风格实验（MS-PSC6K）**：覆盖 5 种风格，对比约 11 种方法。
- **鲁棒性实验（RR）**：1 组，覆盖多种方法。
- **消融实验**：1 组，包含 CleanDIFT、Unified CleanDIFT、Unified CleanDIFT+DINOv2、Unified CleanDIFT+Conv、LoFFA w/o AdaIN、LoFE→Conv、DWT&IDWT→Conv、Single DWT&IDWT、SFA-DIFT full 等 9 个变体。
- **可视化分析**：t-SNE 跨模态聚类、PCA 特征图、Fourier 频谱分析、定性对应结果。

### 充分性与公平性评估
- **优点**：
  - 对比方法覆盖零样本与监督两类，且包含最新 SOTA（如 DINOv3、SketchFusion、Fuse2Match）。
  - 消融验证了 AdaIN、LoFE、DWT/IDWT、两级分解等各组件的必要性。
  - 引入 RR 指标缓解绝对性能下降不可比的问题。
- **不足**：
  - 消融仅在平均指标上报告，未分别列出 PSC6K 与 MS-PSC6K 的结果，可能掩盖数据集间差异。
  - 缺少跨数据集迁移实验（如 PSC6K 训练、其他数据集测试）。
  - 未报告训练/推理效率与参数量对比，难以评估实际部署成本。
  - MS-PSC6K 由生成式方法构造，风格分布可能与真实艺术图像存在偏差。
  - 摘要中"平均提升 0.87% PCK@1、2.20% PCK@5、0.95% PCK@10"与单数据集表格数值（如 PSC6K 的 0.37%、2.63%、1.71%）口径不完全一致，需注意解读。

## 6. 主要结论与发现

- **SFA-DIFT 达到 SOTA**：
  - PSC6K：PCK@1 = 9.81%，PCK@5 = 72.94%，PCK@10 = 92.70%。
  - MS-PSC6K 五风格平均：PCK@1 = 8.70%，PCK@5 = 69.21%，PCK@10 = 91.02%。
- **双域对齐有效**：Unified CleanDIFT 先建立空间一致特征，LoFFA 再聚合共享低频、抑制模态特有高频噪声，使频谱能量集中于低-中频并锐化空间边界。
- **t-SNE 验证**：SFA-DIFT 按语义类别聚类而非模态类型聚类，SD 则呈现明显的模态判别性聚类。
- **鲁棒性发现**：Unified CleanDIFT 的 RR 接近 1.0，表明对纹理变化具有真正的不变性；完整 SFA-DIFT 的 RR 略降至 0.87，作者解释为高方差纹理干扰与结构线索竞争所致。
- **现有方法在风格多样化数据上退化严重**：直接迁移预训练权重或在 MS-PSC6K 上重训练均导致性能下降甚至不收敛。

## 7. 优点

- **问题分析系统深入**：从空间与频域两个视角量化并可视化跨稀疏度鸿沟，为方法设计提供清晰依据。
- **双域对齐思路新颖**：首次将低频小波聚合与 CleanDIFT 统一特征学习结合，超越单纯空间对齐。
- **参数高效**：LoRA 仅更新低秩矩阵，保留 SD 对纹理图像的理解；LoFFA 为轻量模块。
- **基准与指标贡献**：提出 MS-PSC6K 多风格基准与 RR 鲁棒性指标，利于后续公平比较。
- **模块化设计**：两阶段解耦，便于分析各组件贡献；消融实验验证了 AdaIN、LoFE、DWT 深度等的必要性。
- **可视化充分**：PCA 特征图、频谱分析、t-SNE 与定性对应结果共同支撑结论。

## 8. 不足与局限

- **推理效率低**：平均 0.8 秒/次对应估计，依赖扩散模型，难以满足实时应用；作者将其列为未来工作。
- **算力信息缺失**：未报告 GPU 型号、数量、训练时长，影响可复现性与成本评估。
- **数据依赖与偏差风险**：
  - LoFFA 训练依赖关键点标注，标注成本高。
  - MS-PSC6K 由生成模型构造多风格纹理，可能无法完全代表真实艺术风格分布。
- **实验覆盖有限**：
  - 仅在草图-照片跨稀疏度场景验证，未扩展到其他跨模态/跨稀疏度任务。
  - 消融用平均指标，未分数据集报告，可能掩盖差异。
  - 缺少与基线在参数量、训练时间、显存占用上的对比。
- **指标解释需谨慎**：完整模型 RR 略低于 Unified CleanDIFT，说明风格扰动下仍有性能损失；摘要平均提升与单数据集表格数值口径不完全一致。
- **应用限制**：当前方法面向语义对应估计

，而非生成、编辑或检索等下游任务；若迁移到草图检索、图像编辑、跨模态定位等场景，仍需重新设计监督信号与匹配头。此外，LoFFA 依赖 AdaIN 将图像特征分布对齐到草图分布，当模态角色反转、多对多匹配或存在遮挡/裁剪变化时，其稳定性仍待验证。
- **失败模式分析不足**：论文展示了成功定性结果，但 PCK@1 仍仅约 10%，说明细粒度对应仍有大量失败。文中未系统量化失败模式，例如细长结构、重复纹理、语义歧义区域、背景干扰与草图夸张变形对匹配的影响。
- **超参数与训练细节透明度有限**：固定时间步 `t' = 261`、LoRA 秩、LoFFA 层数、小波基选择、损失权重等关键超参缺乏敏感性分析，可能影响复现与泛化判断。
- **伦理与版权风险**：MS-PSC6K 通过生成式风格化构造，可能继承生成模型的风格偏差与版权争议；草图-照片对应数据也涉及原始图像授权、艺术家署名与用户隐私等问题，论文未展开讨论。

## 9. 总结性判断

- **核心贡献**：该论文将“跨稀疏度对应”从单纯的空间特征匹配问题，提升为**空间-频域双域对齐**问题，并通过 Unified CleanDIFT 与 LoFFA 给出参数高效、模块化的实现路径。其价值不限于草图-照片匹配，也为其他稀疏-稠密跨模态对应任务提供了频域分析视角。
- **方法有效性**：主实验、多风格实验、消融与可视化共同表明，先统一干净扩散特征、再聚合低频共享信息，确实能缓解特征空洞、模态聚类与频域错配问题，并在多个指标上达到 SOTA。
- **现实约束**：扩散特征推理成本、关键点标注依赖、生成式 benchmark 偏差以及算力报告缺失，仍是其走向大规模实时应用与公平复现的主要障碍。
- **未来方向**：可探索将扩散特征蒸馏到轻量编码器、引入无关键点自监督对应、构建更真实的艺术风格基准，并将双域对齐思想扩展到检索、编辑、定位等下游任务。

（完）
