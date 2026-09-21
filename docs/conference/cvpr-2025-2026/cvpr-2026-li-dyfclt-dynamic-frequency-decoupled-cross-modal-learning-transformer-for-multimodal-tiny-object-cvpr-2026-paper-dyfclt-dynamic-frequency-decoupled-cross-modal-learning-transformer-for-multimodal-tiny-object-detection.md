---
title: "DyFCLT: Dynamic Frequency-Decoupled Cross-Modal Learning Transformer for Multimodal Tiny Object Detection"
title_zh: DyFCLT：面向多模态微小目标检测的动态频率解耦跨模态学习Transformer
authors: "Li, Chaolang, Dai, Pengwen, Li, Jingyu, Yao, Siyuan, Jiang, Yuchen, Zheng, Zhuoran"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Li_DyFCLT_Dynamic_Frequency-Decoupled_Cross-Modal_Learning_Transformer_for_Multimodal_Tiny_Object_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 7.0
evidence: RGBT跨模态频率学习
tldr: 多模态微小目标检测因目标表征弱与跨模态干扰而困难，现有频域方法多局限于可见光模态，忽视RGB与红外的互补频率线索。本文提出动态频率解耦跨模态学习Transformer，DyFCLT，通过频率特性分析解耦并融合双模态中高频成分。实验表明其在RGBT微小目标检测上取得提升，为跨模态频率融合提供了新思路。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-dyfclt-dynamic-frequency-decoupled-cross-modal-learning-transformer-for-multimodal-tiny-object-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-dyfclt-dynamic-frequency-decoupled-cross-modal-learning-transformer-for-multimodal-tiny-object-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-dyfclt-dynamic-frequency-decoupled-cross-modal-learning-transformer-for-multimodal-tiny-object-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 8, \"index\": 3, \"width\": 403, \"height\": 322}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-dyfclt-dynamic-frequency-decoupled-cross-modal-learning-transformer-for-multimodal-tiny-object-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 8, \"index\": 4, \"width\": 403, \"height\": 322}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-dyfclt-dynamic-frequency-decoupled-cross-modal-learning-transformer-for-multimodal-tiny-object-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 8, \"index\": 5, \"width\": 403, \"height\": 322}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-dyfclt-dynamic-frequency-decoupled-cross-modal-learning-transformer-for-multimodal-tiny-object-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 8, \"index\": 6, \"width\": 403, \"height\": 322}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-dyfclt-dynamic-frequency-decoupled-cross-modal-learning-transformer-for-multimodal-tiny-object-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 8, \"index\": 7, \"width\": 403, \"height\": 322}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-dyfclt-dynamic-frequency-decoupled-cross-modal-learning-transformer-for-multimodal-tiny-object-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 8, \"index\": 8, \"width\": 403, \"height\": 322}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-dyfclt-dynamic-frequency-decoupled-cross-modal-learning-transformer-for-multimodal-tiny-object-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 8, \"index\": 9, \"width\": 403, \"height\": 322}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-dyfclt-dynamic-frequency-decoupled-cross-modal-learning-transformer-for-multimodal-tiny-object-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 8, \"index\": 10, \"width\": 403, \"height\": 322}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-dyfclt-dynamic-frequency-decoupled-cross-modal-learning-transformer-for-multimodal-tiny-object-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 8, \"index\": 11, \"width\": 403, \"height\": 322}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-dyfclt-dynamic-frequency-decoupled-cross-modal-learning-transformer-for-multimodal-tiny-object-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 8, \"index\": 12, \"width\": 403, \"height\": 322}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-dyfclt-dynamic-frequency-decoupled-cross-modal-learning-transformer-for-multimodal-tiny-object-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 8, \"index\": 13, \"width\": 640, \"height\": 415}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-dyfclt-dynamic-frequency-decoupled-cross-modal-learning-transformer-for-multimodal-tiny-object-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 8, \"index\": 14, \"width\": 640, \"height\": 415}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-dyfclt-dynamic-frequency-decoupled-cross-modal-learning-transformer-for-multimodal-tiny-object-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 8, \"index\": 15, \"width\": 640, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-dyfclt-dynamic-frequency-decoupled-cross-modal-learning-transformer-for-multimodal-tiny-object-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 8, \"index\": 16, \"width\": 640, \"height\": 512}]"
motivation: 多模态微小目标检测表征弱且跨模态干扰大，频域方法忽视跨模态频率线索。
method: 提出DyFCLT，基于频率特性分析动态解耦并融合RGB与红外的中高频跨模态成分。
result: 在RGBT微小目标检测上取得性能提升，验证频率解耦融合有效。
conclusion: 为多模态跨频率融合提供了新思路。
---

## Abstract
Multimodal tiny object detection plays a critical role in real-world applications, yet remains highly challenging due to weak target representations and complex cross-modal interference. Existing frequency-domain methods for tiny object detection are still largely limited to the visible modality and overlook complementary cross-modal frequency cues in multimodal scenes. In this paper, we investigate cross-modal frequency learning for RGBT tiny object detection. Through frequency characteristic analysis, we find that tiny objects in both RGB and infrared modalities contain richer mid- and high-frequency components as object size decreases. Motivated by this observation, we propose a Dynamic Frequency-Decoupled Cross-Modal Learning Transformer (DyFCLT). Specifically, DyFCLT introduces a Dynamic Frequency-Band Decoupled Cross-Modal Attention (DFCA) mechanism to perform fine-grained cross-modal interaction across dynamic frequency sub-bands, and a Selective Smoothing Enhancement (SSE) module to suppress background noise and enhance foreground responses during multi-scale fusion. Extensive experiments on two RGBT tiny object detection benchmarks and one general-scale benchmark demonstrate that DyFCLT achieves state-of-the-art performance with strong generalization across different scales and scenes.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义

- **研究背景**：微小目标检测（TOD）在自动驾驶、视频监控、灾害救援等场景中具有重要价值，但仅依赖可见光模态时，受动态光照、遮挡、复杂背景等影响，微小目标表征往往非常弱。
- **核心问题**：多模态可见光-红外（RGBT）微小目标检测仍很困难，主要挑战是目标表征弱、跨模态干扰强。现有频域方法多局限于可见光模态，或简单假设“红外以低频为主、RGB以高频细节为主”，缺乏对 RGBT 场景下不同尺度目标频率特性的系统分析。
- **关键观察**：作者在 RGBT-Tiny 上做径向频率分解，将归一化频谱划分为低、中、高频带。结果显示：随着目标尺寸减小，RGB 和红外模态中的中、高频能量占比都增加；即使红外通常以低频为主，微小目标仍包含丰富的多频带信息。
- **整体含义**：论文主张应充分挖掘跨模态、跨频带的互补频率线索，同时抑制复杂背景噪声。为此提出 DyFCLT，为 RGBT 微小目标检测提供“动态频带解耦 + 跨模态频率交互 + 选择性平滑增强”的新思路。

## 2. 方法论

### 2.1 总体架构

- 输入一对可见光图像 \(I_{vis}\) 和红外图像 \(I_{ir}\)。
- 使用模态特定特征提取器（ResNet50）分别提取多尺度特征 \(\{F^l_{vis}\}\) 和 \(\{F^l_{ir}\}\)。
- 核心融合模块为 DyFCLT，包含两个协同组件：
  - **DFCA**：Dynamic Frequency-Band Decoupled Cross-Modal Attention，动态频带解耦跨模态注意力。
  - **SSE**：Selective Smoothing Enhancement，选择性平滑增强。
- 融合后的多尺度特征送入基于可变形注意力的 Transformer 解码器和检测头，输出检测结果。
- 默认以红外分支为例说明，可见光分支操作相同。

### 2.2 DFCA：动态频带解耦跨模态注意力

- **Q/K/V 生成**：第 \(l\) 层特征 \(F^l_{vis}\) 和 \(F^l_{ir}\) 经 \(1\times1\) 逐点卷积和 \(3\times3\) 深度卷积，分别生成 query、key、value 特征 \(F^l_q,F^l_k,F^l_v\)。
- **频率带分解 FBD**：
  - 对 Q/K/V 做 FFT，并用径向二值掩码 \(M_b\) 隔离不同频带。
  - 掩码定义为：若径向频率 \(\sqrt{u^2+v^2}\) 落在第 \(b\) 个频带 \([k_b,k_{b+1})\) 内，则保留，否则为 0。
  - 归一化频率范围为 \([0,1/2]\)，\(k_0=0\)，\(k_B=1/2\)。
  - 频带边界可学习，以内边界累加正增量的方式保证单调性；初始化采用倍频程方案，例如 \(B=3\) 时为 \(\{0,1/8,1/4,1/2\}\)。
  - 论文设置 \(B=3\)，即低、中、高频三个频带。
- **Band-Wise Frequency Attention**：
  - 对每个频带，在频域计算 query 与 key 的共轭逐元素乘积，再经 IFFT 得到跨模态相关权重 \(A^l_b\)。
  - 用 \(3\times3\) 卷积和 sigmoid 激活调制该权重，再乘以 value 的 IFFT 结果，得到该频带的跨模态响应 \(R^l_b\)。
  - 将所有频带的 \(R^l_b\) 聚合，经 LayerNorm 和线性投影，
