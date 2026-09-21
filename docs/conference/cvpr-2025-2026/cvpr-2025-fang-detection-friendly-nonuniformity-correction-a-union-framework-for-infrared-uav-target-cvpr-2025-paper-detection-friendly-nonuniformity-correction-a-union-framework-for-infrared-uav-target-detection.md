---
title: "Detection-Friendly Nonuniformity Correction: A Union Framework for Infrared UAV Target Detection"
title_zh: 面向检测的红外非均匀性校正：红外无人机目标检测的联合框架
authors: "Fang, Houzhang, Wang, Xiaolin, Li, Zengyang, Wang, Lu, Li, Qingshan, Chang, Yi, Yan, Luxin"
date: 2025
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2025/papers/Fang_Detection-Friendly_Nonuniformity_Correction_A_Union_Framework_for_Infrared_UAV_Target_CVPR_2025_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 4.0
evidence: 面向目标检测的红外无人机图像
tldr: 该文针对红外无人机图像受温度相关低频非均匀性影响、对比度下降而难以检测目标的问题展开研究。现有方法通常将红外非均匀性校正作为检测的预处理步骤，导致性能次优。作者提出端到端联合框架UniCD，同时处理非均匀性校正与UAV目标检测并增强有利于检测的信息。实验表明该框架在非均匀条件下取得更优检测效果。该工作面向UAV红外感知，但未涉及RGB-T跨模态对齐。
source: CVPR-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-001.webp\", \"caption\": \"\", \"page\": 7, \"index\": 1, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-002.webp\", \"caption\": \"\", \"page\": 7, \"index\": 2, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-003.webp\", \"caption\": \"\", \"page\": 7, \"index\": 3, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-004.webp\", \"caption\": \"\", \"page\": 7, \"index\": 4, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-005.webp\", \"caption\": \"\", \"page\": 7, \"index\": 5, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-006.webp\", \"caption\": \"\", \"page\": 7, \"index\": 6, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-007.webp\", \"caption\": \"\", \"page\": 7, \"index\": 7, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-008.webp\", \"caption\": \"\", \"page\": 7, \"index\": 8, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-009.webp\", \"caption\": \"\", \"page\": 7, \"index\": 9, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-010.webp\", \"caption\": \"\", \"page\": 7, \"index\": 10, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-011.webp\", \"caption\": \"\", \"page\": 7, \"index\": 11, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-012.webp\", \"caption\": \"\", \"page\": 7, \"index\": 12, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-013.webp\", \"caption\": \"\", \"page\": 7, \"index\": 13, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-014.webp\", \"caption\": \"\", \"page\": 7, \"index\": 14, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-015.webp\", \"caption\": \"\", \"page\": 7, \"index\": 15, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-016.webp\", \"caption\": \"\", \"page\": 7, \"index\": 16, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-017.webp\", \"caption\": \"\", \"page\": 7, \"index\": 17, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-018.webp\", \"caption\": \"\", \"page\": 7, \"index\": 18, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-019.webp\", \"caption\": \"\", \"page\": 7, \"index\": 19, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-020.webp\", \"caption\": \"\", \"page\": 7, \"index\": 20, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-021.webp\", \"caption\": \"\", \"page\": 7, \"index\": 21, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-022.webp\", \"caption\": \"\", \"page\": 7, \"index\": 22, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-023.webp\", \"caption\": \"\", \"page\": 7, \"index\": 23, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-024.webp\", \"caption\": \"\", \"page\": 7, \"index\": 24, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-025.webp\", \"caption\": \"\", \"page\": 7, \"index\": 25, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-026.webp\", \"caption\": \"\", \"page\": 7, \"index\": 26, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-027.webp\", \"caption\": \"\", \"page\": 7, \"index\": 27, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-028.webp\", \"caption\": \"\", \"page\": 7, \"index\": 28, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-029.webp\", \"caption\": \"\", \"page\": 7, \"index\": 29, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-030.webp\", \"caption\": \"\", \"page\": 7, \"index\": 30, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-031.webp\", \"caption\": \"\", \"page\": 7, \"index\": 31, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-032.webp\", \"caption\": \"\", \"page\": 7, \"index\": 32, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-033.webp\", \"caption\": \"\", \"page\": 7, \"index\": 33, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-034.webp\", \"caption\": \"\", \"page\": 7, \"index\": 34, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-035.webp\", \"caption\": \"\", \"page\": 7, \"index\": 35, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-036.webp\", \"caption\": \"\", \"page\": 7, \"index\": 36, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-037.webp\", \"caption\": \"\", \"page\": 8, \"index\": 37, \"width\": 401, \"height\": 332}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-038.webp\", \"caption\": \"\", \"page\": 8, \"index\": 38, \"width\": 535, \"height\": 370}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-039.webp\", \"caption\": \"\", \"page\": 8, \"index\": 39, \"width\": 535, \"height\": 370}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-040.webp\", \"caption\": \"\", \"page\": 8, \"index\": 40, \"width\": 3220, \"height\": 1029}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-fang-detection-friendly-nonuniformity-correction-a-union-framework-for-infrared-uav-target-cvpr-2025-paper/fig-041.webp\", \"caption\": \"\", \"page\": 8, \"index\": 41, \"width\": 640, \"height\": 512}]"
motivation: 红外无人机图像受非均匀性影响对比度降低，将校正作为预处理会导致检测性能次优。
method: 提出端到端联合框架UniCD，同时进行红外非均匀性校正与UAV目标检测。
result: 在非均匀条件下实现更优的无人机目标检测效果。
conclusion: 校正与检测联合优化有益于UAV红外感知，但缺乏跨模态对齐与RGB-T融合内容。
---

## Abstract
Infrared unmanned aerial vehicle (UAV) images captured using thermal detectors are often affected by temperature-dependent low-frequency nonuniformity, which significantly reduces the contrast of the images. Detecting UAV targets under nonuniform conditions is crucial in UAV surveillance applications. Existing methods typically treat infrared nonuniformity correction (NUC) as a preprocessing step for detection, which leads to suboptimal performance. Balancing the two tasks while enhancing detection-beneficial information remains challenging. In this paper, we present a detection-friendly union framework, termed UniCD, that simultaneously addresses both infrared NUC and UAV target detection tasks in an end-to-end manner. We first model NUC as a small number of parameter estimation problem jointly driven by priors and data to generate detection-conducive images. Then, we incorporate a new auxiliary loss with target mask supervision into the backbone of the infrared UAV target detection network to strengthen target features while suppressing the background. To better balance correction and detection, we introduce a detection-guided self-supervised loss to reduce feature discrepancies between the two tasks, thereby enhancing detection robustness to varying nonuniformity levels. Additionally, we construct a new benchmark composed of 50,000 infrared images in various nonuniformity types, multi-scale UAV targets and rich backgrounds with target annotations, called IRBFD. Extensive experiments on IRBFD demonstrate that our UniCD is a robust union framework for NUC and UAV target detection while achieving real-time processing capabilities. Dataset can be available at https://github.com/IVPLaboratory/UniCD.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **研究背景**：红外热探测器拍摄的无人机（UAV）图像常受温度相关低频非均匀性影响，即“偏置场”（bias field）导致图像对比度下降；同时红外 UAV 目标本身特征弱、背景复杂，非均匀性进一步加剧检测难度。
- **核心问题**：现有方法通常把红外非均匀性校正（NUC）当作检测前的预处理步骤，或将校正与检测分开处理，导致两个任务目标不一致，检测性能次优；如何在统一框架中同时提升校正质量和检测精度仍是挑战。
- **整体含义**：论文提出面向检测的联合框架 **UniCD**，首次尝试在端到端框架中同时处理红外 NUC 与红外 UAV 目标检测，并构建大规模基准 **IRBFD**，推动非均匀条件下红外 UAV 感知研究。

## 2. 论文提出的方法论

### 核心思想

- 将非均匀性校正建模为**少量多项式系数估计问题**，由先验和数据共同驱动，使用轻量网络预测偏置场参数。
- 将校正模块与红外 UAV 检测网络融合，通过辅助损失和自监督损失平衡低层校正任务与高层检测任务。
- 检测网络以 DANet 为基线，不显著增加结构复杂度，而是通过损失设计增强目标特征、抑制背景。

### 关键技术细节

- **退化模型**：红外退化图像表示为  
  \(Y = C + B\)，其中 \(Y\) 为退化图像，\(C\) 为清晰图像，\(B\) 为偏置场；校正图像 \(R = Y - B\)。
- **偏置场建模**：利用偏置场空间平滑特性，用三阶二元多项式建模：
  \[
  B(x_i,y_j)=\sum_{t=0}^{D}\sum_{s=0}^{D-t} a_{t,s}x_i^t y_j^s
  \]
  其中 \(D=3\)，\(a\) 为多项式系数。网络目标为预测系数 \(\hat{a}\)。
- **轻量 NUC 网络**：
  - 输入退化图像 \(Y\) 先下采样 2 倍；
  - 使用 **GBFE**（全局偏置场编码器，含两层 Swin Transformer，隐藏通道 16）和 **LBFE**（局部偏置场编码器，两个串联空间注意力模块）提取全局和局部特征；
  - 特征融合后经 5 个 \(3\times3\) 卷积层和全连接层预测系数 \(\hat{a}\)。
- **NUC 损失**：预训练 NUC 模块，最小化预测系数与真实系数差异：
  \[
  L_{cor}=\frac{1}{N}\|\hat{a}-a\|_2^2
  \]
  文中称 MAE，但公式为 L2 形式。
- **检测器辅助损失 TEBS**：
  - 将 GT 边界框转为二值目标掩码 \(M\)，目标区域为 1，背景为 0；
  - 在检测 backbone 四个阶段的特征图 \(F_i\) 上计算交叉熵损失：
    \[
    L_{TEBS}=\frac{1}{4}\sum_{i=1}^{4}L_{CE}(M,F_i)
    \]
  - 检测总损失：
    \[
    L_{det}=L_{cls}+L_{reg}+\lambda L_{TEBS}
    \]
    前 20 epoch \(\lambda=1\)，之后降为 0.01。
- **偏置鲁棒损失 BR**：
  - 联合训练时，将清晰图像 \(C\) 和校正图像 \(R\) 同时输入检测 backbone；
  - 对四个阶段特征计算余弦相似度，并定义：
    \[
    L_{BR}=\frac{1}{4}\sum_{i=1}^{4}\left(1-\text{CosSim}(F_C^{(i)},F_R^{(i)})\right)
    \]
  - 联合训练损失：
    \[
    L_{uni}=L_{det}+L_{BR}
  \]
- **整体流程**：先预训练 NUC 模块，再与检测网络端到端联合训练；校正模块可插拔，可集成到现有检测器中。

## 3. 实验设计

- **数据集 / 场景**：
  - 构建 **IRBFD** 基准，共 **50,000** 张红外图像，尺寸 **640×512**。
  - **IRBFD-syn**：30,000 张合成非均匀红外 UAV 图像，提供成对退化图像与清晰图像，用于训练和校正评估。
  - **IRBFD-real**：20,000 张真实非均匀红外 UAV 图像，用于验证真实场景泛化。
  - 场景包括密集云、建筑、森林、城市、海面等；目标距离 50 m 至 2 km，存在多尺度变化；无人机类型包括 DJI Inspire、Matrice、Phantom、Mavic、Mini 系列；所有目标位置人工标注。
- **Benchmark**：IRBFD 是论文提出的新基准，训练/验证/测试在 IRBFD-syn 上按 8:1:1 划分；在合成集训练，并直接在真实集上验证泛化。
- **对比方法**：
  - **直接检测**：Deformable DETR、DINO、DAGNet、LESPS、MSHNet、YOLO11L。
  - **先校正后检测**：传统 NUC 方法 Liu、Shi、AHBC；深度学习 NUC 方法 DMRN、TV-DIP；检测器包括 YOLO11L、DAGNet 等。
  - **联合方法**：UniCD。
- **评价指标**：
  - NUC：PSNR、SSIM。
  - 检测：Precision、Recall。
  - 实时性：FPS。
  - 真实集校正效果：SCRG，用于衡量校正后目标可检测性提升。
- **实验类型**：
  - 合成集和真实集定量比较；
  - P-R 曲线比较；
  - 定性可视化对比，包括建筑、山坡、云层等场景；
  - 消融实验：多项式阶数、LBFE/GBFE 模块、TEBS 损失、BR 损失、真实集有效性、不同非均匀性水平、NUC 模块可插拔性。

## 4. 资源与算力

- 文中明确说明实验在 **NVIDIA RTX 4090** 上进行，环境为 **CUDA 12.4** 和 **PyTorch 1.7**。
- 优化器为 Adam，学习率 0.001，训练 50 epoch，权重衰减 \(10^{-4}\)，batch size 为 4。
- 数据增强仅使用随机水平翻转。
- **未明确说明**：GPU 数量、总训练时长、能耗、显存占用、嵌入式部署实测等。因此算力报告不够完整。
- 模型轻量性方面，NUC 模块在 \(640\times512\) 图像上约 **0.3966M 参数、1.6809G FLOPs**，实时性达到 **32 FPS**。

## 5. 实验数量与充分性

- 论文包含约 **9 个主要表格** 和多个定性图、P-R 曲线：
  - 表 1：合成集 IRBFD-syn 上与多种直接检测、先校正后检测方法对比；
  - 表 2：真实集 IRBFD-real 上与多种方法对比；
  - 表 3：多项式阶数消融；
  - 表 4：LBFE/GBFE 模块消融；
  - 表 5：TEBS 损失消融；
  - 表 6：BR 损失与 Direct/Separate/Union 策略消融；
  - 表 7：真实集有效性消融；
  - 表 8：不同非均匀性强度泛化；
  - 表 9：NUC 模块与现有检测器结合的可扩展性。
- **充分性**：
  - 对自建 IRBFD 基准覆盖较全面，包含合成与真实、定量与定性、模块与损失消融。
  - 对比方法涵盖传统 NUC、深度学习 NUC、CNN 检测器和 Transformer 检测器。
- **客观与公平性**：
  - 使用统一数据集和指标，消融较系统。
  - 但真实集缺乏成对清晰图像，校正质量主要依赖 SCRG 和下游检测间接评估。
  - 部分对比方法是“校正方法 + 检测器”的组合，未必都针对联合任务重新调优，公平性存在一定限制。
  - 检测指标以 Precision/Recall 为主，缺少 mAP/AP 等更全面的目标检测指标。

## 6. 论文的主要结论与发现

- UniCD 能在端到端框架中同时完成红外非均匀性校正和 UAV 目标检测，并优于现有“先校正后检测”组合方法。
- 在 IRBFD-syn 上，UniCD 达到 **PSNR 31.961、SSIM 0.9827、Precision 0.999、Recall 0.822、32 FPS**。
- 在 IRBFD-real 上，UniCD 达到 **SCRG 1.286、Precision 0.994、Recall 0.901**，显示较好真实场景泛化。
- TEBS 损失能增强目标特征、抑制背景，提高检测召回；BR 损失能缓解校正与检测任务冲突，提高检测鲁棒性。
- NUC 模块具有可插拔性，可提升 YOLO11L、DAGNet、LESPS、MSHNet 等现有检测器在红外退化图像上的检测性能。
- 三阶多项式在精度、复杂度和冗余之间取得最佳平衡；GBFE + LBFE 组合显著提升校正性能且保持较高
