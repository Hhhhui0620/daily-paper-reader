---
title: "3M-TI: High-Quality Mobile Thermal Imaging via Calibration-free Multi-Camera Cross-Modal Diffusion"
title_zh: 3M-TI：基于免标定多相机跨模态扩散的高质量移动热成像
authors: "Chen, Minchong, Yuan, Xiaoyun, Wan, Junzhe, Zhang, Jianing, Zhang, Jun"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Chen_3M-TI_High-Quality_Mobile_Thermal_Imaging_via_Calibration-free_Multi-Camera_Cross-Modal_Diffusion_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 6.0
evidence: 免标定跨模态扩散避免依赖精确热红外与可见光配准
tldr: 移动平台热红外传感器受体积限制，成像分辨率与纹理质量低，现有RGB引导超分方法依赖精确且繁琐的跨相机标定。本文提出免标定的多相机跨模态扩散框架3M-TI，在扩散UNet中引入跨模态自注意力模块替代原自注意力，实现无需配准的热成像增强。实验表明该方法在移动热成像任务上取得更优效果。该工作对未配准可见光与热红外图像对的跨模态处理具有重要借鉴价值。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 492, \"height\": 1237}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 1, \"index\": 4, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 1, \"index\": 5, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 1, \"index\": 6, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 1, \"index\": 7, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 6, \"index\": 8, \"width\": 4395, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 6, \"index\": 9, \"width\": 4395, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 6, \"index\": 10, \"width\": 4395, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 6, \"index\": 11, \"width\": 4395, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 6, \"index\": 12, \"width\": 4395, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 6, \"index\": 13, \"width\": 4395, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 7, \"index\": 14, \"width\": 4166, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 7, \"index\": 15, \"width\": 4166, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 7, \"index\": 16, \"width\": 4166, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 7, \"index\": 17, \"width\": 4166, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 7, \"index\": 18, \"width\": 4166, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 7, \"index\": 19, \"width\": 4166, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-020.webp\", \"caption\": \"\", \"page\": 8, \"index\": 20, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-021.webp\", \"caption\": \"\", \"page\": 8, \"index\": 21, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-022.webp\", \"caption\": \"\", \"page\": 8, \"index\": 22, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-023.webp\", \"caption\": \"\", \"page\": 8, \"index\": 23, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-024.webp\", \"caption\": \"\", \"page\": 8, \"index\": 24, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-025.webp\", \"caption\": \"\", \"page\": 8, \"index\": 25, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-026.webp\", \"caption\": \"\", \"page\": 8, \"index\": 26, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-027.webp\", \"caption\": \"\", \"page\": 8, \"index\": 27, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-028.webp\", \"caption\": \"\", \"page\": 8, \"index\": 28, \"width\": 355, \"height\": 354}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-029.webp\", \"caption\": \"\", \"page\": 8, \"index\": 29, \"width\": 355, \"height\": 354}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-030.webp\", \"caption\": \"\", \"page\": 8, \"index\": 30, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-031.webp\", \"caption\": \"\", \"page\": 8, \"index\": 31, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-032.webp\", \"caption\": \"\", \"page\": 8, \"index\": 32, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-033.webp\", \"caption\": \"\", \"page\": 8, \"index\": 33, \"width\": 355, \"height\": 355}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-034.webp\", \"caption\": \"\", \"page\": 8, \"index\": 34, \"width\": 355, \"height\": 355}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-035.webp\", \"caption\": \"\", \"page\": 8, \"index\": 35, \"width\": 354, \"height\": 355}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-036.webp\", \"caption\": \"\", \"page\": 8, \"index\": 36, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-037.webp\", \"caption\": \"\", \"page\": 8, \"index\": 37, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-038.webp\", \"caption\": \"\", \"page\": 8, \"index\": 38, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-039.webp\", \"caption\": \"\", \"page\": 8, \"index\": 39, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-040.webp\", \"caption\": \"\", \"page\": 8, \"index\": 40, \"width\": 355, \"height\": 355}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-041.webp\", \"caption\": \"\", \"page\": 8, \"index\": 41, \"width\": 355, \"height\": 354}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-042.webp\", \"caption\": \"\", \"page\": 8, \"index\": 42, \"width\": 354, \"height\": 355}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-chen-3m-ti-high-quality-mobile-thermal-imaging-via-calibration-free-multi-camera-cross-modal-diffusion-cvpr-2026-paper/fig-043.webp\", \"caption\": \"\", \"page\": 8, \"index\": 43, \"width\": 512, \"height\": 512}]"
motivation: 移动热红外成像分辨率与纹理受限，现有RGB引导方法依赖精确跨相机标定，鲁棒性差。
method: 提出免标定多相机跨模态扩散框架，在扩散UNet中引入跨模态自注意力模块。
result: 实验表明该方法在移动热成像任务上取得更优效果。
conclusion: 为未配准可见光与热红外图像对的跨模态处理提供了新思路。
---

## Abstract
The miniaturization of thermal sensors for mobile platforms inherently limits their spatial resolution and textural fidelity, leading to blurry and less informative images. Existing thermal super-resolution (SR) methods can be grouped into single-image and RGB-guided approaches: the former struggles to recover fine structures from limited information, while the latter relies on accurate and laborious cross-camera calibration, which hinders practical deployment and robustness. Here, we propose 3M-TI, a calibration-free Multi-camera cross-Modality diffusion framework for Mobile Thermal Imaging. At its core, 3M-TI integrates a cross-modal self-attention module (CSM) into the diffusion UNet, replacing the original self-attention layers to adaptively align thermal and RGB features throughout the denoising process, without requiring explicit camera calibration. This design enables the diffusion network to leverage its generative prior to enhance spatial resolution, structural fidelity, and texture detail in the super-resolved thermal images. Extensive evaluations on real-world mobile thermal cameras and public benchmarks validate our superior performance, achieving state-of-the-art results in both visual quality and quantitative metrics. More importantly, the thermal images enhanced by 3M-TI lead to substantial gains in critical downstream tasks like object detection and segmentation, underscoring its practical value for robust mobile thermal perception systems.

---

## 论文详细总结（自动生成）

# 3M-TI 论文深度总结

## 一、核心问题与整体含义（研究动机与背景）

- **硬件瓶颈**：移动平台热红外传感器因小型化需求导致孔径缩小，空间分辨率与纹理细节严重受限；热辐射波长较长限制了最小像元尺寸，红外传感器成本高昂也制约了像素数量。结果是移动端热图像普遍模糊、信息量低。
- **现有方法的两条路线及其缺陷**：
  - **单图像热超分（Single-image SR）**：仅依赖低分辨率热图自身信息，在严重退化或大倍率放大时难以恢复高频细节，且热图像大规模数据集匮乏，训练与泛化困难。
  - **RGB 引导热超分（RGB-guided SR）**：利用跨模态线索增强重建，但热与 RGB 成像原理差异大，直接融合易引入不真实细节；更关键的是，现有方法普遍依赖像素级对齐的 RGB-热红外图像对，需要繁琐且精确的跨相机标定，严重限制实际部署的鲁棒性与可扩展性。
- **整体含义**：论文旨在实现**免标定（calibration-free）**、**免同步（synchronization-free）** 的移动热成像增强，使消费级智能手机搭配低成本热模块即可获得高质量热图像，并直接惠及下游感知任务（目标检测、语义分割）。

## 二、方法论：核心思想与关键技术细节

### 2.1 整体框架（3M-TI Framework）

- 输入：低分辨率热图像（64×64）+ 未标定的高分辨率 RGB 参考图（512×512）。
- 骨干：基于一步扩散模型 **SD-Turbo**，兼顾效率与生成质量。
- 流程：
  1. 冻结的 VAE 编码器将热图与 RGB 图分别编码为隐空间表示；
  2. 在扩散 UNet 中引入**跨模态自注意力模块（CSM）** 替换原始自注意力层；
  3. 训练时对 RGB 施加**错位增强（Misalignment Augmentation）**；
  4. 通过零初始化卷积的**跳跃连接**将编码器 4 个下采样块的特征传递至对应解码器上采样块，增强结构一致性；
  5. 使用 **RAM（Recognize Anything Model）** 从 RGB 图生成文本提示，弥补低分辨率热图语义提取的不足；
  6. 采用 **LoRA** 对 UNet 和 VAE 解码器进行低秩微调。

### 2.2 跨模态自注意力模块（CSM）

- 核心思想：复用预训练扩散 UNet 中的 Transformer 块，将其改造为跨模态对应与融合模块，**无需显式相机标定**。
- 具体操作：
  - 将 RGB 与热隐变量拼接为张量 $\{z^0_{RGB}, z^0_{th}\} \in \mathbb{R}^{B \times M \times C \times H \times W}$，其中 $M=2$（可扩展至多张 RGB）。
  - 在非 Transformer 块中，将图像数量维度 $M$ 折叠进 batch 维度，使 RGB 与热图独立处理。
  - 在 Transformer 块内，进行两次张量重排：进入前 reshape 为 $\mathbb{R}^{B \times (M \times H \times W) \times C}$，将每个像素视为 token，两模态所有像素合并为长度 $M \times H \times W$ 的单一序列；自注意力在此序列上计算所有 RGB 与热像素间的成对依赖关系，自然学习跨模态对应并整合互补线索；块结束后再 reshape 回 $\mathbb{R}^{(B \times M) \times C \times H \times W}$。
  - 输出阶段，精炼后的热隐变量与 VAE 编码器初始隐变量通过零初始化跳跃连接合并，生成最终高保真热图像。
- **关键优势**：CSM 不引入额外参数，可高效配合 LoRA 微调。

### 2.3 错位增强策略（Misalignment Augmentation）

- 现实问题：多相机配置下存在相机视差（随场景深度与基线变化）和时间不同步（由物体运动与采集延迟决定）。
- 做法：对 RGB 图像施加受控空间变换——平移、缩放、旋转、透视变形，参数选取反映手持与多相机场景的典型偏差。
- 目的：鼓励 CSM 学习鲁棒的跨模态对应关系，弥合受限训练数据与多样部署环境之间的差距，避免过拟合到特定标定配置。

### 2.4 实际多相机系统

- 热模块：HIKVISION P09（成本低于 100 美元），原生分辨率 96×96（本文 resize 至 64×64），FOV 50°×50°，像元间距 12 μm。
- RGB 模块：小米 15 主摄（OV50H 传感器），分辨率 4096×3072，等效焦距 23 mm，FOV 74°×59°。
- 连接方式：Type-C 接口。

### 2.5 损失函数

$$\mathcal{L} = \mathcal{L}_2 + \lambda \cdot \mathcal{L}_{LPIPS}, \quad \lambda = 1$$

## 三、实验设计

### 3.1 数据集与场景

- **公开数据集**：IRVI、LLVIP、M³FD、PBVS 2025 TISR Challenge Track 2。
  - 训练集：10,922 对图像（IRVI 3,200 + LLVIP 3,200 + M³FD 3,822 + PBVS 2025 700）。
  - 测试集：1,176 对图像（IRVI 300 + LLVIP 300 + M³FD 376 + PBVS 2025 200）。
  - 原始数据集为严格对齐图像对，测试集额外施加受控空间变换以模拟视差与时间偏移；热图中心裁剪为方形并 resize 至 64×64，添加高斯噪声模拟真实传感器噪声；RGB 同步裁剪并 resize 至 512×512。
- **智能手机数据集**：自建系统采集 300 对图像，覆盖 100 个多样场景（200 组夜间 + 100 组白天）。

### 3.2 Benchmark 与评估指标

- **参考指标**：PSNR、SSIM（重建保真度）、LPIPS（感知质量）。
- **无参考指标**：MUSIQ、MANIQA（整体图像质量）。
- **下游任务**：开放词汇目标检测与语义分割，使用预训练 Grounded-SAM 零样本推理，所有方法使用相同文本提示。

### 3.3 对比方法（7 个基线）

| 方法 | 类型 |
|---|---|
| CoReFusion | RGB 引导超分（UNet 双编码器 + 对比损失） |
| CoRPLE | 轮廓波残差 + 提示学习红外增强 |
| SwinFuSR | Swin Transformer 骨干 + RGB 引导 |
| SwinPaste | SwinFuSR 增强变体（数据混合 + 多尺度监督） |
| SeeSR | 扩散超分（无语义参考引导） |
| OSEDiff | 一步扩散超分 |
| DifIISR | 红外专用扩散超分 |

- 公平性处理：除 DifIISR（训练代码不可用，直接评估）外，所有基线均用公开代码在自建数据集上重训练。

## 四、资源与算力

- **GPU**：单张 NVIDIA A800（80 GB）。
- **训练时长**：约 4 小时（8,000 次迭代）。
- **优化器**：Adam，学习率 $2 \times 10^{-5}$，batch size = 4。
- **LoRA 秩**：UNet 为 16，VAE 解码器为 4。
- **说明**：论文明确给出了 GPU 型号、数量与训练时长，算力信息较为透明。但未报告推理延迟、显存占用等部署相关指标。

## 五、实验数量与充分性

- **实验组数概览**：
  1. 公开数据集定量对比（表 1，8 个方法 + 2 个消融变体）；
  2. 真实手机数据集无参考评估（表 2，6 个方法）；
  3. 下游目标检测（表 3，含 GT 热图、参考 RGB、SwinPaste、SeeSR、3M-TI 共 5 组）；
  4. 下游语义分割（图 6 定性展示）；
  5. 消融实验（表 4，共 8 个配置：w/o Reference、w/o RAM prompt、w/o Augmentation、w/o Skip、w/ Self-Attn、w/ Feature Concat、w/ Cross-Attn、w/ All）；
  6. 融合策略对比（CSM vs. 原始自注意力 vs. 特征拼接 vs. 标准交叉注意力）。
- **充分性与客观性评估**：
  - **优点**：覆盖公开数据集与真实移动系统双场景，定量与定性结合，含下游任务验证与多组件消融，对比方法涵盖非扩散、Transformer 与扩散三类代表性工作，基线重训练保证公平。
  - **局限**：下游检测仅在 LLVIP 和 M³FD 两个有标注数据集上进行；分割任务以定性展示为主，缺少定量指标；未报告多次运行的方差或统计显著性检验。

## 六、主要结论与发现

- **定量结果**：3M-TI 在感知指标上全面领先——LPIPS 0.1787、MANIQA 0.4443、MUSIQ 36.66，均为最优；在保真度指标上（PSNR 30.09、SSIM 0.8610）优于 OSEDiff、SeeSR、DifIISR、SwinFuSR、SwinPaste，但略低于 CoRPLE（PSNR 30.47）和 CoReFusion w/ Augment（30.30）。
- **定性结果**：非扩散方法虽 PSNR/SSIM 较高但过度平滑、丢失高频结构；OSEDiff 和 SeeSR 能合成高频内容但与 GT 不一致；3M-TI 能忠实迁移 RGB 中的几何细节（建筑、道路标线、窗户、电线、树枝、电线杆等），轮廓自然。
- **真实手机数据集**：3M-TI 在 MUSIQ（30.62）和 MANIQA（0.3589）上最优，对未标定、未同步的真实采集对表现出强鲁棒性，甚至能从被光斑严重退化的 RGB 参考中恢复栏杆结构。
- **下游任务增益**：
  - 目标检测：3M-TI 的 F1 0.4724、IoU 0.3427，优于参考 RGB（0.4643/0.3359），接近 GT 热图（0.4887/0.3494），显著优于 SwinPaste 与 SeeSR。
  - 语义分割：3M-TI 生成更准确连贯的分割图，在低光场景下甚至优于 RGB 参考。
- **消融结论**：RGB 参考、错位增强、跳跃连接、RAM 语义提示各有贡献；CSM 优于原始自注意力、特征拼接和标准交叉注意力，因其同时捕获**跨模态（RGB-热）引导**与**模态内（热-热）结构依赖**。

## 七、优点

- **问题切入精准**：直击 RGB 引导热超分对精确标定的依赖这一实际部署痛点，提出免标定、免同步方案，具有明确的应用价值。
- **方法设计巧妙**：
  - 在 VAE 隐空间而非像素空间进行跨模态对齐，利用连续解耦表示实现鲁棒对应，避免显式配准；
  - CSM 通过 token 重排复用预训练自注意力层，**不引入额外参数**，计算高效；
  - 错位增强策略简单有效，无需物理仿真即可模拟真实视差与时间偏移；
  - 一步扩散（SD-Turbo）+ LoRA 微调，训练成本低（单卡 4 小时）。
- **验证体系完整**：公开数据集 + 自建真实手机系统双验证，定量 + 定性 + 下游任务（检测、分割）多维度评估，消融实验覆盖全部关键组件。
- **实际可行性**：硬件成本低于 100 美元，训练与推理开销可控，具备移动端部署潜力。

## 八、不足与局限

- **数据集规模与多样性有限**：训练集仅约 1.1 万对图像，相比 RGB 领域的数据规模偏小；测试集 1,176 对，且错位增强为人工合成变换，可能无法完全覆盖真实世界的复杂退化模式。
- **定量指标并非全面领先**：PSNR/SSIM 上不及 CoRPLE 和 CoReFusion w/ Augment，说明在像素级保真度上仍有提升空间；论文更强调感知质量，但未深入讨论保真度与感知质量的权衡机制。
- **下游分割任务缺乏定量评估**：语义分割仅以定性图展示，未报告 mIoU 等量化指标，说服力弱于检测任务。
- **对 RGB 参考的依赖**：方法本质上仍需要 RGB 图像作为引导，在 RGB 也失效的极端场景（如完全无光、RGB 被遮挡）下可能受限；论文未讨论 RGB 质量极差时的性能边界。
- **实时性与部署细节缺失**：未报告推理延迟、模型参数量、显存占用等移动端部署关键指标；"移动"更多体现在采集端而非计算端。
- **基线覆盖的公平性**：DifIISR 因训练代码不可用未在自建数据集上重训练，可能影响对比的完全公平性；CoRPLE 等方法的超参调优细节未充分披露。
- **泛化性验证范围**：仅验证了一款热模块（HIKVISION P09）和一款手机（小米 15），跨硬件平台的泛化能力有待进一步验证。

（完）
