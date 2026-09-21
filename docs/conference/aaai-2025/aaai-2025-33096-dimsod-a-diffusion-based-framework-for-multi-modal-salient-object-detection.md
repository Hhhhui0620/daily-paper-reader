---
title: "DiMSOD: A Diffusion-Based Framework for Multi-Modal Salient Object Detection"
authors: "Shuo Zhang, Jiaming Huang, Wenbing Tang, Yan Wu, Terrence Hu, Xiaogang Xu, Jing Liu"
date: 2025
pdf: "https://ojs.aaai.org/index.php/AAAI/article/download/33096/35251"
tags: ["query:uav-rgbt-sod"]
score: 6
source: AAAI-2025-Accepted
selection_source: long-range
publication_date: 2025
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
id: aaai-2025-33096
canonical_id: "work:92fd8405b6bf8e418fda2d60"
research_run_id: 20260921-e959361397be
research_mode: starter
reading_status: pending
---

## Abstract
Multi-modal salient object detection (SOD) through the integration of additional data such as depth or thermal information has become a significant task in computer vision during recent years. Traditionally, the challenges of identifying salient objects in RGB, RGB-D (Depth), and RGB-T (Thermal) images are tackled separately. However, without intricate cross-modal fusion strategies, such approaches struggle to effectively integrate multi-modal information, often resulting in poorly defined object edges or overconfident inaccurate predictions.
Recent studies have shown that designing a unified end-to-end framework to handle all three types of SOD tasks simultaneously is both necessary and difficult. To address this need, we propose a novel approach that treats multi-modal SOD as a conditional mask generation task utilizing diffusion models. 
We introduce DiMSOD, which enables the concurrent use of local (depth maps, thermal maps) and global controls (original images) within a unified model for progressive denoising and refined prediction. DiMSOD is efficient, only requiring fine-tuning of our newly introduced modules on the existing stable diffusion, which not only reduces the fine-tuning cost, making it more viable for practical use, but also enhances the integration of multi-modal conditional controls. Specifically, we have developed modules including SOD-ControlNet, Feature Adaptive Network (FAN), and Feature Injection Attention Network (FIAN) to enhance the model's performance. Extensive experiments demonstrate that DiMSOD efficiently detects salient objects across RGB, RGB-D, and RGB-T datasets, achieving superior performance compared to previous well-established methods.

## 专题评审

专题相关性评分：6/10。

涉及RGB-T显著目标检测，但未涉及UAV平台、未配准或不确定性感知对齐。

<!-- research-reading-pending -->
中文总结与全文内容待生成；当前仅提供原始论文元数据与摘要。
<!-- /research-reading-pending -->
