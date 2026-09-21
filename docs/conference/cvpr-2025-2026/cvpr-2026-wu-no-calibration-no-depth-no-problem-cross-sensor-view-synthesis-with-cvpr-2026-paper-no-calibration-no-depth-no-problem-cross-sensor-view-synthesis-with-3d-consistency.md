---
title: "No Calibration, No Depth, No Problem: Cross-Sensor View Synthesis with 3D Consistency"
title_zh: 无标定、无深度也无所畏惧：具有三维一致性的跨传感器视图合成
authors: "Wu, Cho-Ying, Huang, Zixun, Huang, Xinyu, Ren, Liu"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Wu_No_Calibration_No_Depth_No_Problem_Cross-Sensor_View_Synthesis_with_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 7.0
evidence: 无需标定获取对齐RGB-X数据，处理未配准模态对
tldr: 针对RGB-X多模态研究普遍假设已存在对齐数据、而实际标定代价高昂的问题，本文首次系统研究跨传感器视图合成。方法采用匹配-稠密化-整合流程，先用RGB-X图像匹配与引导点稠密化，再以置信度感知稠密化和自匹配过滤提升视图合成，最后用3D高斯泼溅整合。实验表明无需三维先验即可获得更好对齐数据，为多模态融合缓解配准负担。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-no-calibration-no-depth-no-problem-cross-sensor-view-synthesis-with-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 3000, \"height\": 888}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-no-calibration-no-depth-no-problem-cross-sensor-view-synthesis-with-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 2, \"index\": 2, \"width\": 1428, \"height\": 456}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-no-calibration-no-depth-no-problem-cross-sensor-view-synthesis-with-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 4, \"index\": 3, \"width\": 3952, \"height\": 1176}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-no-calibration-no-depth-no-problem-cross-sensor-view-synthesis-with-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 5, \"index\": 4, \"width\": 2974, \"height\": 1566}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-no-calibration-no-depth-no-problem-cross-sensor-view-synthesis-with-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 6, \"index\": 5, \"width\": 3030, \"height\": 960}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-no-calibration-no-depth-no-problem-cross-sensor-view-synthesis-with-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 6, \"index\": 6, \"width\": 1428, \"height\": 1200}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wu-no-calibration-no-depth-no-problem-cross-sensor-view-synthesis-with-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 7, \"index\": 7, \"width\": 3006, \"height\": 1188}]"
motivation: 多模态融合研究假设已存在对齐的RGB-X数据，但实际标定需要巨大工程代价。
method: 提出匹配-稠密化-整合流程，结合置信度感知稠密化、自匹配过滤与三维高斯泼溅。
result: 无需三维先验即可实现更优的跨传感器视图合成与对齐。
conclusion: 为未配准多模态数据获取提供了低成本、无需标定的解决方案。
---

## Abstract
We present the first study of cross-sensor view synthesis across different modalities. We examine a practical, fundamental, yet widely overlooked problem: getting aligned RGB-X data, where most RGB-X prior work assumes such pairs exist and focuses on modality fusion, but it empirically requires huge engineering effort in calibration. We propose a match-densify-consolidate method. First, we perform RGB-X image matching followed by guided point densification. Using the proposed confidence-aware densification and self-matching filtering, we attain better view synthesis and later consolidate them in 3D Gaussian Splatting (3DGS). Our method uses no 3D priors for X-sensor and only assumes nearly no-cost COLMAP for RGB. We aim to remove the cumbersome calibration for various RGB-X sensors and advance the popularity of cross-sensor learning by a scalable solution that breaks through the bottleneck in large-scale real-world RGB-X data collection.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **核心问题**：如何在没有繁琐传感器标定、没有 X 模态深度/位姿/内参等 3D 先验的情况下，获得与 RGB 视图像素级对齐的 RGB-X 数据。
- **背景动机**：
  - 大量 RGB-X 多模态研究默认已经存在对齐好的 RGB-X 数据，主要关注融合、分割、检测等任务。
  - 现实中，不同传感器（热红外、NIR、SAR 等）的配对与对齐通常依赖复杂标定：内参测量、时间同步、相对位姿估计、度量深度获取等。
  - 传统 3D 重投影流程误差会逐级传播，且难以解决传感器位移造成的遮挡问题。
  - COLMAP 等 SfM 方法主要适用于 RGB，在低纹理 X 模态或 RGB-X 场景中常失败。
  - 跨模态匹配方法虽可估计单应矩阵或位姿，但单应变换假设平面结构，无法处理真实 3D 视差，前景/背景层会出现明显错位。
- **整体含义**：论文首次系统研究“跨传感器视图合成”这一被忽视但基础的问题，提出无需 X 传感器 3D 先验、仅需低成本 RGB COLMAP 的可扩展框架，以缓解 RGB-X 数据采集和对齐瓶颈，推动跨传感器学习。

## 2. 论文提出的方法论

- **核心思想**：采用“匹配—稠密化—整合”（match-densify-consolidate）流程：
  1. 跨模态图像匹配获得稀疏/半稠密 RGB-X 对应点；
  2. 将 X 关键点累积到 RGB 视图，形成稀疏 X 图；
  3. 用 RGB 引导的稠密化网络生成稠密 X 图；
  4. 通过置信度感知融合、自匹配过滤和再稠密化提升质量；
  5. 最后用 RGB-X 3DGS 在 RGB 视图上做 3D 一致性整合。

- **关键技术细节**：
  - **RGB-X 匹配与 X 图累积**：
    - 使用跨模态匹配器在 RGB 图 \(I\) 和 X 图 \(X\) 间建立对应点，并带有置信度 \(c\)。
    - 将 \(N\) 帧 X 关键点按 RGB 坐标累积，形成半稠密 X 图 \(X_m\)。
    - 对未匹配区域设为 void。
  - **区域采样 Area Sampling**：
    - 用 GroundedSAM 分割天空、地面、墙面、草地等低纹理/复杂区域。
    - 在对应单应变换后的 X 图中均匀采样，但仅采样这些区域和 void 区域的 5% 点，避免单应误差过度影响后续稠密化。
  - **置信度感知稠密化与融合 CADF**：
    - 稠密化网络 \(D\) 以 RGB 图和稀疏 X 图为输入，输出稠密 X 图。
    - 将图像匹配置信度 \(c\) 聚合成置信图 \(C_m\)，融入 DySPN 递归细化：
      \[
      L^{t+1}=(1-C_sC_m)\sum_r\sum_{(a,b)}w_{r,a,b}*L^t_{a,b}+C_sC_mX_m
      \]
      从而降低可能错误关键点的贡献，聚焦高置信点。
    - 使用多级置信度阈值 \(\delta=0.15,0.3,0.5\)，得到多级 X 图，再用融合模块 \(F\) 融合，抑制噪声、去模糊、锐化边缘。
    - \(F\) 用自监督损失训练，包括 SigLIP2 图像特征余弦相似度损失和 RGB-X 自匹配损失。
  - **自匹配过滤 Self-Matching Filtering**：
    - 利用匹配器 patch 特征计算 RGB-X 相似矩阵：
      \[
      A=\frac{F_IF_X^\top}{\tau}
      \]
    - 理想情况下 \(A\) 应为对角矩阵。
    - 训练时用损失 \(L_{sim}\) 最大化对角项、最小化非对角项。
    - 推理时用 \(q=Q_{50}(A)/Q_{99}(A)\) 衡量自匹配集中度，按 \((1-q)\) 分位数剔除低相似 patch。
  - **精细阶段再稠密化**：
    - 在过滤后的 X 图上
