---
title: Self-Supervised Spatial Correspondence Across Modalities
title_zh: 跨模态的自监督空间对应
authors: "Shrivastava, Ayush, Owens, Andrew"
date: 2025
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2025/papers/Shrivastava_Self-Supervised_Spatial_Correspondence_Across_Modalities_CVPR_2025_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 6.0
evidence: 无需空间对齐模态对的跨模态像素对应
tldr: 针对跨模态图像间寻找同一物理点像素对应困难的问题，本文提出自监督空间对应方法。模型扩展对比随机游走框架，同时学习跨模态与模态内匹配的循环一致特征表示，无需显式光度一致性假设，且可完全用无标签数据训练，不依赖任何空间对齐的多模态图像对。实验在几何与语义对应任务上验证了有效性，为未配准多模态对齐提供了通用工具。
source: CVPR-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 640, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 640, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 1920, \"height\": 1080}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-004.webp\", \"caption\": \"\", \"page\": 1, \"index\": 4, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-005.webp\", \"caption\": \"\", \"page\": 1, \"index\": 5, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-006.webp\", \"caption\": \"\", \"page\": 6, \"index\": 6, \"width\": 1214, \"height\": 924}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-007.webp\", \"caption\": \"\", \"page\": 6, \"index\": 7, \"width\": 1214, \"height\": 924}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-008.webp\", \"caption\": \"\", \"page\": 6, \"index\": 8, \"width\": 1120, \"height\": 426}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-009.webp\", \"caption\": \"\", \"page\": 6, \"index\": 9, \"width\": 1120, \"height\": 426}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-010.webp\", \"caption\": \"\", \"page\": 6, \"index\": 10, \"width\": 1120, \"height\": 426}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-011.webp\", \"caption\": \"\", \"page\": 7, \"index\": 11, \"width\": 1214, \"height\": 1214}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-012.webp\", \"caption\": \"\", \"page\": 7, \"index\": 12, \"width\": 1280, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-013.webp\", \"caption\": \"\", \"page\": 7, \"index\": 13, \"width\": 1214, \"height\": 1214}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-014.webp\", \"caption\": \"\", \"page\": 7, \"index\": 14, \"width\": 1214, \"height\": 1214}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-015.webp\", \"caption\": \"\", \"page\": 7, \"index\": 15, \"width\": 1214, \"height\": 1214}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-016.webp\", \"caption\": \"\", \"page\": 7, \"index\": 16, \"width\": 1280, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-017.webp\", \"caption\": \"\", \"page\": 7, \"index\": 17, \"width\": 1280, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-018.webp\", \"caption\": \"\", \"page\": 7, \"index\": 18, \"width\": 1280, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-019.webp\", \"caption\": \"\", \"page\": 7, \"index\": 19, \"width\": 1280, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-020.webp\", \"caption\": \"\", \"page\": 7, \"index\": 20, \"width\": 1280, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-021.webp\", \"caption\": \"\", \"page\": 8, \"index\": 21, \"width\": 1970, \"height\": 979}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-022.webp\", \"caption\": \"\", \"page\": 8, \"index\": 22, \"width\": 1970, \"height\": 979}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-023.webp\", \"caption\": \"\", \"page\": 8, \"index\": 23, \"width\": 1970, \"height\": 979}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-024.webp\", \"caption\": \"\", \"page\": 8, \"index\": 24, \"width\": 1970, \"height\": 979}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-025.webp\", \"caption\": \"\", \"page\": 8, \"index\": 25, \"width\": 1970, \"height\": 979}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-026.webp\", \"caption\": \"\", \"page\": 8, \"index\": 26, \"width\": 1970, \"height\": 979}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-027.webp\", \"caption\": \"\", \"page\": 8, \"index\": 27, \"width\": 1970, \"height\": 979}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-028.webp\", \"caption\": \"\", \"page\": 8, \"index\": 28, \"width\": 1970, \"height\": 979}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-029.webp\", \"caption\": \"\", \"page\": 8, \"index\": 29, \"width\": 1970, \"height\": 979}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-030.webp\", \"caption\": \"\", \"page\": 8, \"index\": 30, \"width\": 1970, \"height\": 979}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-031.webp\", \"caption\": \"\", \"page\": 8, \"index\": 31, \"width\": 1970, \"height\": 979}, {\"url\": \"assets/figures/cvpr-2025-accepted/cvpr-2025-shrivastava-self-supervised-spatial-correspondence-across-modalities-cvpr-2025-paper/fig-032.webp\", \"caption\": \"\", \"page\": 8, \"index\": 32, \"width\": 1970, \"height\": 979}]"
motivation: 跨模态像素对应缺乏对齐标注，且不同模态外观差异大。
method: 扩展对比随机游走，联合学习跨模态与模态内循环一致特征表示。
result: 无需空间对齐的多模态对即可训练，在几何与语义对应任务上有效。
conclusion: 为未配准跨模态对齐提供了无需对齐数据的自监督方案。
---

## Abstract
We present a method for finding cross-modal space-time correspondences. Given two images from different visual modalities, such as an RGB image and a depth map, our model identifies which pairs of pixels correspond to the same physical points in the scene. To solve this problem, we extend the contrastive random walk framework to simultaneously learn cycle-consistent feature representations for both cross-modal and intra-modal matching. The resulting model is simple and has no explicit photo-consistency assumptions. It can be trained entirely using unlabeled data, without the need for any spatially aligned multimodal image pairs. We evaluate our method on both geometric and semantic correspondence tasks. For geometric matching, we consider challenging tasks such as RGB-to-depth and RGB-to-thermal matching (and vice versa); for semantic matching, we evaluate on photo-sketch and cross-style image alignment. Our method achieves strong performance across all benchmarks.

---

## 论文详细总结（自动生成）

# 论文总结：Self-Supervised Spatial Correspondence Across Modalities

## 1. 核心问题与研究动机

- **核心问题**：当同一场景由不同视觉模态（RGB、深度、热成像、素描、不同风格图像）的相机采集时，如何确定两幅图像中哪些像素对应同一物理点，即跨模态像素级空间对应。
- **研究背景**：
  - 不同模态的像素记录的信息本质不同（如深度值 vs. 亮度值），无法用局部外观信息直接匹配。
  - 现有自监督方法多依赖**成对的多传感器数据**或**光度一致性假设**，而多模态数据中这些假设常被违反。
  - 跨模态预测（如单目深度估计）本身是极难问题，不能作为匹配的中间步骤。
- **整体含义**：本文提出一种**模态无关**的自监督方法，无需空间对齐的多模态图像对，也无需显式光度一致性假设，即可学习跨模态密集像素对应，为未配准多模态对齐提供通用工具。

## 2. 方法论

### 2.1 核心思想

- 扩展**对比随机游走（Contrastive Random Walk, CRW）** 框架至跨模态场景。
- 构建有向图：节点为各模态图像块，边连接跨模态图像块；训练网络为随机游走分配转移概率。
- 通过**循环一致性**训练：随机游走者从模态 A 的像素出发，经模态 B 再返回原点，最大化返回概率。

### 2.2 关键技术细节

- **模型架构**：
  - 基于**全局匹配随机游走（GMRW）** 模型 [32]，支持全对像素匹配。
  - 每个模态使用独立视觉编码器；共享 Transformer 主干（6 个自注意力/交叉注意力/前馈块）执行跨模态全局匹配。
  - 几何任务用 CNN 编码器；语义任务用 **DINOv2** 初始化并微调，利用其语义先验。

- **跨模态转移矩阵**：
  - 对特征 $F^{m_1}_t$ 与 $F^{m_2}_{t+k}$ 计算 $A^{m_1,m_2}_{t,t+k} = \text{softmax}(F^{m_1}_t (F^{m_2}_{t+k})^\top / \tau)$，$\tau = \sqrt{d}$。
  - 期望像素位移（光流）由转移矩阵与坐标网格计算得到。

- **损失函数**（总损失为三者加权和）：
  1. **跨模态循环一致性损失** $L_{\text{cross-crw}}$：在回文序列 $\{I^{m_1}_t, I^{m_2}_{t+k}, I^{m_1}_t\}$ 上，链式连接两个方向转移矩阵，用标签扭曲损失 [32] 防止捷径学习。
  2. **模态内循环一致性损失** $L_{\text{intra-crw}}$：对同模态的原始图像与增强裁剪图做随机游走，稳定训练、避免局部最优。
  3. **平滑损失** $L_{\text{smooth}}$：边缘感知的二阶导数惩罚，仅在 RGB 作为源图像时施加。

### 2.3 训练流程

- **三阶段训练**：
  1. 仅模态内 CRW（RGB-RGB、Depth-Depth / Thermal-Thermal）。
  2. 加入跨模态 CRW（RGB-Depth、Depth-RGB 等）。
  3. 加入平滑损失。
- 直接优化跨模态循环一致性会导致收敛到次优解，辅助模态内监督是关键。

## 3. 实验设计

### 3.1 数据集与场景

| 任务 | 数据集 | 训练/评估规模 |
|------|--------|--------------|
| RGB-Depth | NYU Depth V2 | 约 400K 无标签 RGB-D 帧；250 个视频片段，平均 688 条轨迹/片段 |
| RGB-Thermal | Thermal-IM（室内）、KAIST（室外） | Thermal-IM：783 序列；KAIST：320 序列；手动标注 100 对 RGB-Thermal 帧、1000 个评估点 |
| Photo-Sketch | PSC6K | 6,250 对标注；130K+ 训练对；评估集 8 关键点/对 |
| Cross-style | 自建基准（Flux 生成） | 10 种风格 × 10K 图像 = 100K 训练样本；500 测试图像，2,250 对比较 |

### 3.2 评估指标

- 几何匹配：TAP-Vid 的位置精度 $\langle \delta^x_{\text{avg}} \rangle$（阈值 1、2、4、8、16 的平均）。
- 语义匹配：PCK-5、PCK-10。

### 3.3 对比方法

- **几何匹配**：RAFT、GMFlow、Arar et al.、CycleGAN+GMFlow、ARFlow（含重训练版）、DIFT、SD-DINO。
- **语义匹配（Photo-Sketch）**：CNNGeo、DINOv2+NN、SD-DINO、WeakAlign、NC-Net、DCCNet、PMD、WarpC-Net、PSCNet。
- **跨风格匹配**：DINOv2+NN、DIFT、SD-DINO、GeoAwareSC（监督方法）。

## 4. 资源与算力

- **论文中未提及**具体的 GPU 型号、数量、训练时长等算力信息。
- 仅可从数据集规模（如 400K RGB-D 帧、100K 跨风格样本）和模型架构（CNN/DINOv2 + 6 层 Transformer）间接推测训练开销较大，但无明确说明。

## 5. 实验数量与充分性

- **实验组数**：
  - 4 个主要任务：RGB-Depth、RGB-Thermal、Photo-Sketch、Cross-style。
  - 消融实验（Table 2）：4 种损失组合 × 2 个数据集 × 2 个方向 = 16 组配置。
  - 与 7+ 种几何基线、9+ 种语义基线对比。
  - 定性结果覆盖全部 4 个任务（Figures 3–6）。
- **充分性与公平性**：
  - 覆盖几何与语义两大类别，跨 5 个数据集，实验较全面。
  - 消融实验清晰验证了模态内预训练、跨模态损失、平滑损失各自的贡献。
  - 对比方法包含监督与自监督方法，且对部分基线进行了重训练适配，较为公平。
  - **但**：所有任务均包含 RGB 模态，未测试完全不涉及 RGB 的模态对（如 depth-thermal 直接匹配）。

## 6. 主要结论与发现

- 跨模态像素对应可**完全通过无标签数据的循环一致性**学习，无需空间对齐的多模态图像对。
- 在 RGB-Depth 和 RGB-Thermal 几何匹配上**显著优于所有基线**（如 NYU Depth 跨模态精度 33.5/34.3 vs. 基线最高 16.2/16.6）。
- 在 Photo-Sketch 语义匹配上**与专用方法竞争**（PCK-5 53.61、PCK-10 82.20）。
- 在自建 Cross-style 基准上**超越所有基线**，包括监督方法 GeoAwareSC（PCK-5 69.26 vs. 68.30）。
- **模态内辅助监督是跨模态训练成功的关键**：仅用跨模态损失会导致训练不稳定和收敛差。

## 7. 优点

- **完全自监督**：无需任何标注或空间对齐的多模态配对，可利用大规模多模态视频数据。
- **模态无关**：不依赖手工设计的光度一致性或模态转换，同一框架适用于 RGB-Depth、RGB-Thermal、Photo-Sketch、跨风格等多种任务。
- **架构简洁**：基于现有 GMRW 框架扩展，引入模态内随机游走和平滑先验即可稳定训练。
- **实验全面**：覆盖几何与语义两大范式，消融实验设计清晰，定性结果丰富。
- **新基准贡献**：提出 RGB-Depth、RGB-Thermal 和 Cross-style 匹配的评估基准。

## 8. 不足与局限

- **模态覆盖有限**：仅验证 4 种域，且所有数据集均包含 RGB；未测试完全不涉及 RGB 的模态对（如 Depth-Thermal）。
- **依赖可匹配的视觉结构**：若模态缺乏共同可辨结构（如遮挡轮廓），匹配可能失败。
- **跨风格匹配存在失败案例**：如动物左右肢体混淆（Figure 6 右上）。
- **算力信息缺失**：未报告 GPU 型号、数量、训练时长，难以评估复现成本与效率。
- **训练阶段较多**：三阶段训练流程增加调参复杂度。
- **部分任务性能非最优**：Photo-Sketch 上 PCK-5 低于 PSCNet（53.61 vs. 57.92），仅 PCK-10 接近。

（完）
