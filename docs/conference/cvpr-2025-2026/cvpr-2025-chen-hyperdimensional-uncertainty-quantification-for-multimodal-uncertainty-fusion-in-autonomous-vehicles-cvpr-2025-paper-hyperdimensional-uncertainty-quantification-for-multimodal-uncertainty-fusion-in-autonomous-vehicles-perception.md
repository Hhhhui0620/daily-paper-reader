---
title: Hyperdimensional Uncertainty Quantification for Multimodal Uncertainty Fusion in Autonomous Vehicles Perception
title_zh: 面向自动驾驶感知多模态不确定性融合的超维不确定性量化
authors: "Chen, Luke, Wang, Junyao, Mortlock, Trier, Khargonekar, Pramod, Al Faruque, Mohammad Abdullah"
date: 2025
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2025/papers/Chen_Hyperdimensional_Uncertainty_Quantification_for_Multimodal_Uncertainty_Fusion_in_Autonomous_Vehicles_CVPR_2025_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 7.0
evidence: 多模态融合中的特征级认知不确定性
tldr: 现有多模态不确定性量化多停留在任务级输出层面，未考虑特征融合中的认知不确定性，且贝叶斯方法计算开销大。本文提出HyperDUM，一种基于超维计算的确定性不确定性量化方法，可高效估计特征级认知不确定性。实验表明其在自动驾驶感知的多模态融合中兼顾精度与效率，为多模态不确定性感知融合提供了可迁移思路。
source: CVPR-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-chen-hyperdimensional-uncertainty-quantification-for-multimodal-uncertainty-fusion-in-autonomous-vehicles-cvpr-2025-paper/fig-001.webp\", \"caption\": \"\", \"page\": 3, \"index\": 1, \"width\": 2627, \"height\": 901}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-chen-hyperdimensional-uncertainty-quantification-for-multimodal-uncertainty-fusion-in-autonomous-vehicles-cvpr-2025-paper/fig-002.webp\", \"caption\": \"\", \"page\": 6, \"index\": 2, \"width\": 4400, \"height\": 1870}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-chen-hyperdimensional-uncertainty-quantification-for-multimodal-uncertainty-fusion-in-autonomous-vehicles-cvpr-2025-paper/fig-003.webp\", \"caption\": \"\", \"page\": 7, \"index\": 3, \"width\": 1988, \"height\": 1190}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-chen-hyperdimensional-uncertainty-quantification-for-multimodal-uncertainty-fusion-in-autonomous-vehicles-cvpr-2025-paper/fig-004.webp\", \"caption\": \"\", \"page\": 8, \"index\": 4, \"width\": 2294, \"height\": 1162}]"
motivation: 现有方法未量化多模态特征融合层的认知不确定性，且贝叶斯方法计算开销高。
method: 提出确定性方法HyperDUM，利用超维计算高效量化特征级认知不确定性。
result: 在多模态融合中兼顾效率与可靠性，提升感知系统稳健性。
conclusion: 为多模态不确定性感知融合提供了高效可部署的方案。
---

## Abstract
Uncertainty Quantification (UQ) is crucial for ensuring the reliability of machine learning models deployed in real-world autonomous systems. However, existing approaches typically quantify task-level output prediction uncertainty without considering epistemic uncertainty at the multimodal feature fusion level, leading to sub-optimal outcomes. Additionally, popular uncertainty quantification methods, e.g., Bayesian approximations, remain challenging to deploy in practice due to high computational costs in training and inference. In this paper, we propose HyperDUM, a novel deterministic uncertainty method (DUM) that efficiently quantifies feature-level epistemic uncertainty by leveraging hyperdimensional computing. Our method captures the channel and spatial uncertainties through channel and patch -wise projection and bundling techniques respectively. Multimodal sensor features are then adaptively weighted to mitigate uncertainty propagation and improve feature fusion. Our evaluations show that HyperDUM on average outperforms the state-of-the-art (SOTA) algorithms by up to 2.01%/1.27% in 3D Object Detection and up to 1.29% improvement over baselines in semantic segmentation tasks under various types of uncertainties. Notably, HyperDUM requires 2.36x less Floating Point Operations and up to 38.30x less parameters than SOTA methods, providing an efficient solution for real-world autonomous systems.

---

## 论文详细总结（自动生成）

# 面向自动驾驶感知多模态不确定性融合的超维不确定性量化（HyperDUM）论文总结

## 1. 核心问题与整体含义
- **研究动机**：自动驾驶感知系统需要在真实世界中可靠运行，但相机、LiDAR、Radar 等模态在不同天气、光照、遮挡、传感器噪声和 corner case 下鲁棒性不同。若不能量化各模态特征的不确定性，不确定信息会在多模态融合中传播，导致过度自信预测和性能下降。
- **现有问题**：
  - 常见 UQ 方法多关注任务级输出预测不确定性，较少建模多模态特征融合层的认知不确定性（epistemic uncertainty）。
  - 贝叶斯近似、深度集成、MC dropout 等方法训练/推理开销大，难以满足实时自动驾驶约束。
  - Conformal Prediction 多提供任务级区间，难以捕捉中间特征不确定性；Posterior Networks 等依赖高质量数据估计后验。
  - 确定性不确定性方法（DUM）有单次前向高效估计的潜力，但尚未充分用于多模态特征级不确定性融合。
- **整体含义**：论文提出 **HyperDUM**，一种基于超维计算（Hyperdimensional Computing / VSA）的确定性不确定性量化方法，在特征融合前估计各模态的通道级和空间级认知不确定性，并据此自适应加权多模态特征，以提升 3D 目标检测和语义分割的鲁棒性、校准性与计算效率。

## 2. 方法论
- **总体框架**：
  - 输入多模态样本 \(x=\{x_1,\dots,x_M\}\)，各模态编码器 \(f_m\) 提取特征 \(z_m=f_m(x_m)\)。
  - 在每个编码器后插入不确定性量化模块 \(U_m(z_m)\)，输出不确定性 \(u_m\)。
  - 通过可学习不确定性加权模块 \(\Omega(z_m,u_m)\) 得到不确定性感知特征 \(\hat z_m\)，再送入融合模块 \(F(\hat z_i,\hat z_j)\)，最后任务头输出检测框/类别或分割标签。
  - 核心思想：在融合前抑制高不确定性模态特征的负面影响，减少不确定性跨模态传播。
- **超维计算基础**：
  - VSA/HDC 将输入映射到高维超向量空间 \(H\in\mathbb{R}^d\)，常用操作包括相似度 \(\delta(\cdot,\cdot)\)、bundling（逐元素相加）、binding（逐元素相乘）。
  - 对同标签样本的超向量进行 bundling，可形成超维原型：\(H_l^m=\bigoplus_{i:y_i=l}\phi_m(z_i^m)\)。
  - 不确定性定义为新样本超向量与各原型之间的相似度集合：\(U_m=\bigcup_{l=1}^L\{\delta(H_z^m,H_l^m)\}\)。
- **HyperDUM 的两个关键设计**：
  - **通道级投影与捆绑 CPB**：对潜在特征 \(z\in\mathbb{R}^{C\times H\times W}\) 先空间池化到 \(\mathbb{R}^C\)，用投影矩阵 \(\Phi^{d\times C}\) 保留通道维，得到 \(H_z\in\mathbb{R}^{d\times C}\)；再按通道进行 bundling，形成通道级原型，并输出 \(C\times L\) 个相似度，以刻画每个通道的不确定性。
  - **块级投影与捆绑 PPB**：将空间维度切成 \(P\) 个 patch，每个 patch 池化后投影到超维空间，得到 patch 级超向量；按 patch 进行 bundling，形成 patch 级原型，并输出 \(P\times L\) 个相似度，以保留细粒度空间不确定性。
