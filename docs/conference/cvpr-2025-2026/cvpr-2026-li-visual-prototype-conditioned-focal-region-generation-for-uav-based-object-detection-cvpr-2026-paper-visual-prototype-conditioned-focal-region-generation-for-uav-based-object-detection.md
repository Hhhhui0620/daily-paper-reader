---
title: Visual Prototype Conditioned Focal Region Generation for UAV-Based Object Detection
title_zh: 面向UAV目标检测的视觉原型条件聚焦区域生成
authors: "Li, Wenhao, Wu, Zimeng, Wu, Yu, Fu, Zehua, Chen, Jiaxin"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Li_Visual_Prototype_Conditioned_Focal_Region_Generation_for_UAV-Based_Object_Detection_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 4.0
evidence: 基于UAV的目标检测影像
tldr: UAV目标检测在动态场景与标注有限条件下十分困难，现有布局到图像生成方法在小目标边界附近易产生伪影。本文提出UAVGen框架，设计视觉原型条件扩散模型为每类构建代表性实例以生成聚焦区域图像。实验表明其提升了UAV目标检测精度，为航拍视觉感知提供了数据增强思路，但不涉及多模态融合。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 7, \"index\": 2, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 7, \"index\": 3, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 7, \"index\": 4, \"width\": 1360, \"height\": 765}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 7, \"index\": 5, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 7, \"index\": 6, \"width\": 960, \"height\": 540}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 7, \"index\": 7, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 7, \"index\": 8, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 7, \"index\": 9, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 7, \"index\": 10, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 7, \"index\": 11, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 7, \"index\": 12, \"width\": 1360, \"height\": 765}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 7, \"index\": 13, \"width\": 1360, \"height\": 765}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 7, \"index\": 14, \"width\": 1360, \"height\": 765}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 7, \"index\": 15, \"width\": 1360, \"height\": 765}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 7, \"index\": 16, \"width\": 1360, \"height\": 765}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 8, \"index\": 17, \"width\": 1826, \"height\": 1748}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 8, \"index\": 18, \"width\": 4178, \"height\": 4009}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 8, \"index\": 19, \"width\": 3284, \"height\": 3127}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-visual-prototype-conditioned-focal-region-generation-for-uav-based-object-detection-cvpr-2026-paper/fig-020.webp\", \"caption\": \"\", \"page\": 8, \"index\": 20, \"width\": 3222, \"height\": 3120}]"
motivation: UAV检测标注有限，布局到图像生成在小目标边界易产生伪影。
method: 提出UAVGen框架，用视觉原型条件扩散模型为每类构建代表性实例生成聚焦区域。
result: 合成图像提升UAV目标检测精度，缓解标注不足。
conclusion: 为航拍视觉感知提供数据增强思路，但不涉及多模态融合。
---

## Abstract
Unmanned aerial vehicle (UAV) based object detection is a critical but challenging task, when applied in dynamically changing scenarios with limited annotated training data. Layout-to-image generation approaches have proved effective in promoting detection accuracy by synthesizing labeled images based on diffusion models. However, they suffer from frequently producing artifacts, especially near layout boundaries of tiny objects, thus substantially limiting their performance. To address these issues, we propose UAVGen, a novel layout-to-image generation framework tailored for UAV-based object detection. Specifically, UAVGen designs a Visual Prototype Conditioned Diffusion Model (VPC-DM) that constructs representative instances for each class and integrates them into latent embeddings for high-fidelity object generation. Moreover, a Focal Region Enhanced Data Pipeline (FRE-DP) is introduced to emphasize object-concentrated foreground regions in synthesis, combined with a label refinement to correct missing, extra and misaligned generations. Extensive experimental results demonstrate that our method significantly outperforms state-of-the-art approaches, and consistently promotes accuracy when integrated with distinct detectors. The source code is available at https://github.com/Sirius-Li/UAVGen.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义

- **研究背景**：UAV 航拍目标检测在农业、交通监控、灾害救援等场景有实际价值，但受飞行高度、固定视角、动态环境和小目标密集重叠影响，高质量标注数据稀缺，导致检测器鲁棒性与泛化能力受限。
- **核心问题**：现有基于扩散模型的 layout-to-image 数据增强方法在通用检测中有效，但在 UAV 场景中效果有限，主要原因是：
  - UAV 目标小且重叠，布局条件质量低，边界附近易产生伪影；
  - 目标在空间上高度不均，扩散模型在低信息背景区域浪费容量；
  - 生成图像与真实标注不一致，出现漏生成、多生成和标签错位，引入标签噪声。
- **整体含义**：论文提出 **UAVGen**，一个面向 UAV 目标检测的扩散驱动数据合成框架，目标是通过高质量视觉原型条件、聚焦区域生成和标签精炼，提高合成数据保真度与标注一致性，从而增强 UAV 检测器训练。作者称这是首个面向 UAV 检测器训练的数据合成方法。

## 2. 方法论

- **总体框架**：给定真实 UAV 检测数据集 D_real = {(I_real, L_real)}，训练扩散模型 Gθ，以布局 L_real 和辅助条件 C 生成合成图像 I_syn = Gθ(L_real, C)，形成 D_syn，再与 D_real 联合训练检测器。UAVGen 在此基础上加入 **VPC-DM** 和 **FRE-DP**。

- **VPC-DM：视觉原型条件扩散模型**
  - **双准则视觉原型选择**：
    - 用预训练检测器 D(·) 在 D_real 上检测目标，按类别分组，得到检测框和置信度。
    - 视觉空间准则：保留与真实框 IoU ≥ τ_det 且置信度 s_i ≥ 类别置信分布 α 分位数的候选。
    - 潜空间准则：用 VAE 编码候选区域，计算其与类中心 μ_c 的 L2 距离，仅保留距离小于 τ_lat 的候选，构成类别视觉原型集合 P_c。
  - **多源条件编码**：
    - 对布局中每个目标区域，从对应类别原型集合中采样视觉原型，按目标框位置和尺度放置到空白画布。
    - 对每个区域画布用 VAE 编码，再通过 3D 卷积融合为视觉原型增强的布局嵌入 v_i。
    - 文本条件包括全局 prompt “An aerial image with {c1}, {c2}, ...”，以及对象级 prompt “An aerial image of {cj}”。
    - 对象级文本嵌入与 Fourier 位置嵌入拼接，经 MLP 和 gated attention 聚合，得到细粒度布局嵌入 e_fi。
  - **条件注入与训练**：
    - 视觉原型布局嵌入 v_i 和细粒度文本嵌入 e_fi 通过 ControlNet 注入，得到条件特征 C_i。
    - 全局文本嵌入 e_gi 与 C_i 共同引导去噪网络 εθ。
    - 使用前景感知重加权损失 L_layout，对目标区域像素赋予更高权重，背景区域权重为 1，以增强目标区域生成质量。

- **FRE-DP：聚焦区域增强数据管线**
  - **区域数据合成**：
    - 计算每个真实框中心点，用 K-means 聚类得到 K 个聚类中心。
    - 对每个中心，在候选区域中求解最大化完整包含真实框数量的聚焦区域 B_k。
    - 裁剪目标密集的聚焦区域，构建 D_real_dense，用于训练和生成。
    - 生成聚焦区域图像后，再合并回原始图像分辨率，形成 D_syn_dense，用于检测器训练。
  - **标签精炼**：
    - 用预训练检测器对合成图像预测，并与真实布局做 IoU 匹配。
    - 处理三类不一致：
      - **漏生成**：删除未匹配且低置信度的真实标签；
      - **多生成**：将高置信度的额外预测作为新标签加入；
      - **标签错位**：当预测置信度高于阈值时，用预测框替换原标签。
    - 最终得到精炼数据集 D_ref，用于检测器训练。阈值 α、β、γ 根据检测器精度设置。

## 3. 实验设计

- **数据集与场景**：
  - **VisDrone**：UAV 视角基准，6,471 训练、548 验证、1,580 测试图像，10 类，包含行人、车辆等。
  - **UAVDT**：UAV 检测与跟踪基准，24,143 训练、16,592 测试图像，来自 UAV 视频。
  - 两数据集均包含小目标、尺度变化、密集目标、遮挡和动态场景。
- **评价指标**：
  - **FID**：衡量生成图像质量。
  - **AP**：mAP、AP_50、AP_75、AP_s、AP_m、AP_l，按 MS COCO 尺寸划分。
- **对比方法**：
  - Real only：仅真实数据训练。
  - CopyPaste。
  - GLIGEN。
  - GeoDiffusion。
  - AeroGen。
  - 检测器：GFL-ResNet50 训练 12 epochs；RemDet-X 作为 SOTA UAV 检测器。
- **生成数据规模**：
  - VisDrone：生成 18,649 个 patch，合并为 738 张完整图像。
  - UAVDT：生成 29,403 个 patch，合并为 9,802 张完整图像。
  - 对比方法按标准实践生成与训练集同规模数据：VisDrone 6,474 张，UAVDT 24,143 张。
  - CopyPaste 复现时合成 7,258 张图像，用 DeepLabV3 ResNet101 推断 mask，与真实数据混合训练 GFL。

## 4. 资源与算力

- 论文明确提到：
  - 基于 **FLUX** 模型；
  - 学习率 **1e-5**；
  - 训练 **60K iterations**；
  - batch size **8**；
  - 使用 **1 张 NVIDIA A800 GPU**；
  - 训练和生成分辨率 **512×512**；
  - 扩散模型、文本编码器、VAE 编码器使用预训练 FLUX 权重并冻结，其余参数微调；
  - 视觉原型选择和标签精炼使用 **Faster R-CNN**。
- 未明确说明：
  - 总训练时长；
  - 推理/生成总耗时；
  - 模型参数量；
  - 能耗或成本；
  - 多次运行方差。

## 5. 实验数量与充分性

- 主要实验包括：
  - **Table 1**：VisDrone 和 UAVDT 上的 FID 与 AP 对比，涵盖 Real only、CopyPaste、GLIGEN、GeoDiffusion、AeroGen、UAVGen。
  - **Table 2**：在 VisDrone 上增强 RemDet-X 的对比。
  - **Table 3**：消融 VPC-DM 中的视觉原型 VP、布局嵌入 LE，以及 FRE-DP 中的聚焦区域 FR、标签精炼 LR。
  - **Table 4**：聚焦区域分辨率消融，比较 1024、512、256。
  - **Fig. 3**：VisDrone 上各类别 mAP 对比。
  - **Fig.
