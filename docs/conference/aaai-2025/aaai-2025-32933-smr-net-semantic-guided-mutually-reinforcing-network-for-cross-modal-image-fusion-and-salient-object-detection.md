---
title: "SMR-Net: Semantic-Guided Mutually Reinforcing Network for Cross-Modal Image Fusion and Salient Object Detection"
authors: "Guobao Xiao, Xinyu Liu, Zebin Lin, Rui Ming"
date: 2025
pdf: "https://ojs.aaai.org/index.php/AAAI/article/download/32933/35088"
tags: ["query:uav-rgbt-sod"]
score: 6
source: AAAI-2025-Accepted
selection_source: long-range
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
id: aaai-2025-32933
canonical_id: "work:2580fc1104cf0e3bbe9c48fa"
research_run_id: 20260921-e959361397be
research_mode: starter
reading_status: pending
---

## Abstract
This paper introduces a lightweight Semantic-guided Mutually Reinforcing network (SMR-Net) for the tasks of cross-modal image fusion and salient object detection (SOD). The core concept of SMR-Net is to leverage semantics for directing the mutual reinforcing between image fusion and SOD. Specifically, a Progressive Cross-modal Interaction (PCI) image fusion subnetwork is designed to exploit local interactions via convolution operations and extend to global interactions utilizing spatial and channel attention mechanisms. Subsequently, a cross-modal Bit-Plane Slicing-based SOD subnetwork (BPS) is developed by incorporating the fused image as a third modality. This component employs bit-plane slicing and the deformable convolution technique to effectively extract irregular semantic information embedded in fusion features. The refined semantic information then guides the feature extraction process of the source modalities in a reweighted fashion. By cascading these two subnetworks, BPS leverages final semantic results to direct PCI towards focusing more on semantic information. Ultimately, through this semantic-guided mutual enhancement process, SMR-Net excels in both producing high-quality fused images and achieving effective salient object detection. Our extensive experiments on image fusion and SOD tasks convincingly demonstrate the superiority of our network over existing state-of-the-art alternatives without introducing noticeable computational costs. Compared to nearest competitors, our method demonstrates a stronger generalization ability with 26% fewer parameters.

## 专题评审

专题相关性评分：6/10。

该文研究跨模态图像融合与显著目标检测的语义引导互增强，属于实质邻近，但未涉及UAV平台、未配准图像或不确定性感知对齐。

<!-- research-reading-pending -->
中文总结与全文内容待生成；当前仅提供原始论文元数据与摘要。
<!-- /research-reading-pending -->
