---
title: "M4-SAM: Multi-Modal Mixture-of-Experts with Memory-Augmented SAM for RGB-D Video Salient Object Detection"
title_zh: M4-SAM：面向RGB-D视频显著目标检测的记忆增强SAM多模态专家混合
authors: "Liu, Jiyuan, Lin, Jia, Zhou, Xiaofei, Cong, Runmin, Liu, Deyang, Liu, Zhi"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Liu_M4-SAM_Multi-Modal_Mixture-of-Experts_with_Memory-Augmented_SAM_for_RGB-D_Video_Salient_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 5.0
evidence: 多模态显著目标检测特征融合，但为RGB-D视频
tldr: 将SAM2扩展到RGB-D视频显著目标检测面临线性LoRA空间建模有限、多尺度特征利用不足与依赖显式提示等问题。本文提出M4-SAM，为SAM2注入模态相关PEFT、层次化特征融合与无提示记忆初始化。实验表明其在RGB-D视频显著目标检测上提升了分割性能。该工作为多模态显著目标检测中的基础模型适配提供有效方案，但其模态为深度而非热红外，且未涉及未配准对齐问题。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 4, \"index\": 1, \"width\": 438, \"height\": 346}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 4, \"index\": 2, \"width\": 768, \"height\": 202}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 4, \"index\": 3, \"width\": 432, \"height\": 342}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 4, \"index\": 4, \"width\": 520, \"height\": 260}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 4, \"index\": 5, \"width\": 552, \"height\": 263}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 4, \"index\": 6, \"width\": 580, \"height\": 268}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 4, \"index\": 7, \"width\": 628, \"height\": 268}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 4, \"index\": 8, \"width\": 532, \"height\": 268}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 4, \"index\": 9, \"width\": 792, \"height\": 272}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 4, \"index\": 10, \"width\": 792, \"height\": 832}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 4, \"index\": 11, \"width\": 792, \"height\": 280}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 4, \"index\": 12, \"width\": 792, \"height\": 280}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 4, \"index\": 13, \"width\": 822, \"height\": 658}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 4, \"index\": 14, \"width\": 560, \"height\": 256}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 7, \"index\": 15, \"width\": 613, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 7, \"index\": 16, \"width\": 613, \"height\": 346}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 7, \"index\": 17, \"width\": 613, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 7, \"index\": 18, \"width\": 612, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 7, \"index\": 19, \"width\": 612, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-020.webp\", \"caption\": \"\", \"page\": 7, \"index\": 20, \"width\": 612, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-021.webp\", \"caption\": \"\", \"page\": 7, \"index\": 21, \"width\": 613, \"height\": 346}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-022.webp\", \"caption\": \"\", \"page\": 7, \"index\": 22, \"width\": 612, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-023.webp\", \"caption\": \"\", \"page\": 7, \"index\": 23, \"width\": 613, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-024.webp\", \"caption\": \"\", \"page\": 7, \"index\": 24, \"width\": 613, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-025.webp\", \"caption\": \"\", \"page\": 7, \"index\": 25, \"width\": 613, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-026.webp\", \"caption\": \"\", \"page\": 7, \"index\": 26, \"width\": 613, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-027.webp\", \"caption\": \"\", \"page\": 7, \"index\": 27, \"width\": 612, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-028.webp\", \"caption\": \"\", \"page\": 7, \"index\": 28, \"width\": 612, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-029.webp\", \"caption\": \"\", \"page\": 7, \"index\": 29, \"width\": 612, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-030.webp\", \"caption\": \"\", \"page\": 7, \"index\": 30, \"width\": 613, \"height\": 346}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-031.webp\", \"caption\": \"\", \"page\": 7, \"index\": 31, \"width\": 612, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-032.webp\", \"caption\": \"\", \"page\": 7, \"index\": 32, \"width\": 613, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-033.webp\", \"caption\": \"\", \"page\": 7, \"index\": 33, \"width\": 613, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-034.webp\", \"caption\": \"\", \"page\": 7, \"index\": 34, \"width\": 613, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-035.webp\", \"caption\": \"\", \"page\": 7, \"index\": 35, \"width\": 613, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-036.webp\", \"caption\": \"\", \"page\": 7, \"index\": 36, \"width\": 613, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-037.webp\", \"caption\": \"\", \"page\": 7, \"index\": 37, \"width\": 613, \"height\": 346}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-038.webp\", \"caption\": \"\", \"page\": 7, \"index\": 38, \"width\": 613, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-039.webp\", \"caption\": \"\", \"page\": 7, \"index\": 39, \"width\": 613, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-040.webp\", \"caption\": \"\", \"page\": 7, \"index\": 40, \"width\": 612, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-041.webp\", \"caption\": \"\", \"page\": 7, \"index\": 41, \"width\": 613, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-042.webp\", \"caption\": \"\", \"page\": 7, \"index\": 42, \"width\": 613, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-043.webp\", \"caption\": \"\", \"page\": 7, \"index\": 43, \"width\": 613, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-044.webp\", \"caption\": \"\", \"page\": 7, \"index\": 44, \"width\": 613, \"height\": 346}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-045.webp\", \"caption\": \"\", \"page\": 7, \"index\": 45, \"width\": 613, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-046.webp\", \"caption\": \"\", \"page\": 7, \"index\": 46, \"width\": 613, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-047.webp\", \"caption\": \"\", \"page\": 7, \"index\": 47, \"width\": 612, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-048.webp\", \"caption\": \"\", \"page\": 7, \"index\": 48, \"width\": 613, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-049.webp\", \"caption\": \"\", \"page\": 7, \"index\": 49, \"width\": 612, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-050.webp\", \"caption\": \"\", \"page\": 7, \"index\": 50, \"width\": 642, \"height\": 362}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-051.webp\", \"caption\": \"\", \"page\": 7, \"index\": 51, \"width\": 640, \"height\": 360}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-052.webp\", \"caption\": \"\", \"page\": 7, \"index\": 52, \"width\": 642, \"height\": 362}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-053.webp\", \"caption\": \"\", \"page\": 7, \"index\": 53, \"width\": 642, \"height\": 360}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-054.webp\", \"caption\": \"\", \"page\": 7, \"index\": 54, \"width\": 642, \"height\": 362}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-055.webp\", \"caption\": \"\", \"page\": 7, \"index\": 55, \"width\": 642, \"height\": 362}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-056.webp\", \"caption\": \"\", \"page\": 7, \"index\": 56, \"width\": 642, \"height\": 362}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-057.webp\", \"caption\": \"\", \"page\": 7, \"index\": 57, \"width\": 640, \"height\": 362}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-058.webp\", \"caption\": \"\", \"page\": 7, \"index\": 58, \"width\": 642, \"height\": 362}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-059.webp\", \"caption\": \"\", \"page\": 7, \"index\": 59, \"width\": 612, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-060.webp\", \"caption\": \"\", \"page\": 7, \"index\": 60, \"width\": 642, \"height\": 362}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-061.webp\", \"caption\": \"\", \"page\": 7, \"index\": 61, \"width\": 640, \"height\": 360}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-062.webp\", \"caption\": \"\", \"page\": 7, \"index\": 62, \"width\": 642, \"height\": 362}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-063.webp\", \"caption\": \"\", \"page\": 7, \"index\": 63, \"width\": 640, \"height\": 362}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-064.webp\", \"caption\": \"\", \"page\": 7, \"index\": 64, \"width\": 642, \"height\": 360}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-065.webp\", \"caption\": \"\", \"page\": 7, \"index\": 65, \"width\": 642, \"height\": 362}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-066.webp\", \"caption\": \"\", \"page\": 7, \"index\": 66, \"width\": 642, \"height\": 362}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-067.webp\", \"caption\": \"\", \"page\": 7, \"index\": 67, \"width\": 612, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-068.webp\", \"caption\": \"\", \"page\": 7, \"index\": 68, \"width\": 613, \"height\": 346}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-069.webp\", \"caption\": \"\", \"page\": 7, \"index\": 69, \"width\": 612, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-m4-sam-multi-modal-mixture-of-experts-with-memory-augmented-sam-for-rgb-d-video-salient-cvpr-2026-paper/fig-070.webp\", \"caption\": \"\", \"page\": 7, \"index\": 70, \"width\": 613, \"height\": 345}]"
motivation: SAM2扩展到RGB-D视频显著目标检测面临LoRA空间建模不足、多尺度特征利用不充分与依赖显式提示等问题。
method: 提出M4-SAM，为SAM2注入模态相关PEFT、层次化特征融合与无提示记忆初始化。
result: 在RGB-D视频显著目标检测任务上提升了分割性能。
conclusion: 为多模态显著目标检测中基础模型适配提供有效方案。
---

## Abstract
The Segment Anything Model 2 (SAM2) has emerged as a foundation model for universal segmentation. Owing to its generalizable visual representations, SAM2 has been successfully applied to various downstream tasks. However, extending SAM2 to the RGB-D video salient object detection (RGB-D VSOD) task encounters three challenges including limited spatial modeling of linear LoRA, insufficient employment of SAM's multi-scale features, and dependence of initialization on explicit prompts. To address the issues, we present Multi-Modal Mixture-of-Experts with Memory-Augmented SAM (M4-SAM), which equips SAM2 with modality-related PEFT, hierarchical feature fusion, and prompt-free memory initialization. Firstly, we inject Modality-Aware MoE-LoRA, which employs convolutional experts to encode local spatial priors and introduces a modality dispatcher for efficient multi-modal fine-tuning, into SAM2's encoder. Secondly, we deploy Gated Multi-Level Feature Fusion, which hierarchically aggregates multi-scale encoder features with an adaptive gating mechanism, to balance spatial details and semantic context. Finally, to conduct zero-shot VSOD without manual prompts, we utilize a Pseudo-Guided Initialization, where a coarse mask is regarded as a pseudo prior and used to bootstrap the memory bank. Extensive experiments demonstrate that M4-SAM achieves the state-of-the-art performance across all evaluation metrics on three public RGB-D VSOD datasets.

---

## 论文详细总结（自动生成）

# M4-SAM 论文中文总结

## 1. 核心问题与整体含义（研究动机与背景）

- **任务背景**：RGB-D 视频显著目标检测（RGB-D VSOD）需要同时利用 RGB、深度和时序信息，在复杂背景、低光照、运动模糊、遮挡等场景中稳定分割显著目标。
- **现有问题**：传统 RGB-D VSOD 方法多依赖有限规模数据集训练，且常使用光流进行时序建模，难以捕捉长时依赖，泛化能力受限。
- **基础模型适配挑战**：SAM2 具备强大预训练表示和视频记忆机制，但直接用于 RGB-D VSOD 存在三大问题：
  - 线性 LoRA 仅做线性投影，缺乏局部空间先验和模态特定设计；
  - 现有 SAM 方法多只在解码器做简单加性多尺度融合，未充分利用编码器多尺度特征；
  - 基于记忆的方法通常依赖首帧人工提示（点、框、掩码）初始化，无法满足无提示 RGB-D VSOD 场景。
- **整体含义**：论文提出 M4-SAM，目标是以参数高效、无提示的方式将 SAM2 适配到 RGB-D 视频显著目标检测，兼顾多模态融合、层次特征利用和时序记忆初始化。

## 2. 方法论：核心思想、关键技术细节与流程

### 2.1 整体架构

- 将 SAM2 改造成 U 型结构：共享 Hiera 编码器处理 RGB 和深度输入，并注入 **Modality-Aware MoE-LoRA**。
- 编码器输出四级 RGB 特征和深度特征，经 **UIM + RFB** 融合为统一多模态编码器特征 `{X_i^E}`。
- 层次解码器逐步上采样并跳连融合，得到解码特征 `{X_i^D}`。
- 将中间层解码特征 `X_2^D` 与编码器多级特征送入 **Pseudo-Guided Temporal Memory**，与记忆库交互后输出最终预测，并用最新预测反向更新记忆库。

### 2.2 Modality-Aware MoE-LoRA

- 将传统 LoRA 的低秩线性分支改造为**卷积专家组**：
  - 3×3 卷积专家；
  - 5×5 卷积专家；
  - 深度可分离 + 逐点卷积专家。
- 通过轻量 MoE Gating 动态选择 top-K 专家并聚合，引入空间局部先验，适应密集预测任务。
- 设计三组专家：RGB 组、深度组、融合组；融合组参数在两个模态间共享。
- 引入 **Modality Dispatcher**：RGB 流激活 RGB + 融合组，深度流激活深度 + 融合组，使 RGB 和深度在统一编码器分支中处理，减少双编码器带来的内存开销。
- 前向形式可概括为：`h = W0x + BAx + BD(Ax)`，其中 `D(·)` 为模态调度器。
- 实现中秩 `r=4`，每组 3 个卷积专家，MoE Gating 选择 top-2 专家。

### 2.3 Gated Multi-Level Feature Fusion

- 将多级编码器特征拼接压缩为上下文表示 `X_c`，再通过空间注意力和通道注意力增强为 `X_e`。
- 使用门控权重 `G` 自适应平衡浅层特征 `X_1^E` 与增强特征 `X_e`，再经 FFN 得到融合编码表示 `\tilde{X}^E`。
- 最终与中间层解码特征 `X_2^D` 拼接为 `X_F`。
- 论文强调基础模型最后一层可能抑制局部空间信息，因此选择中间层解码特征 `X_2^D` 而非最终层参与融合。

### 2.4 Pseudo-Guided Temporal Memory

- 对当前帧融合特征 `X_F` 与记忆库中的历史 key/value 做交叉注意力，得到时序聚合特征 `\tilde{X}_F`。
- 记忆解码器结合空间特征、时序上下文和上一隐藏状态，生成预测掩码。
- 记忆库保存最近 `T` 帧的 key/value，并通过 ValueEncoder 在预测掩码引导下编码显著特征。
- **Pseudo-Guided Initialization**：首帧没有时序信息，使用解码器生成的粗掩码 `P_{c,0}^1` 作为伪先验初始化记忆库：
  - `\tilde{k}_{m,0} = Linear_k(X_{F,0})`
  - `\tilde{v}_{m,0} = Linear_v(X_{F,0} · P_{c,0}^1)`
- value 投影与后续 ValueEncoder 共享参数，保持特征空间一致，从而去除人工提示依赖。

### 2.5 损失函数

- 总损失：`L_total = L_pred + L_aux + L_moe`。
- `L_pred`：最终预测与 GT 的结构损失。
- `L_aux`：多级辅助监督，包括粗掩码损失和 Sobel 伪边缘监督的边缘图损失。
- `L_moe`：专家负载均衡正则，权重 `λ=10^-2`，防止专家坍缩。

## 3. 实验设计

- **数据集 / benchmark**：
  - **DViSal**：237 个 RGB-D 视频，7117 帧，室内外复杂光照。
  - **RDVS**：57 个 RGB-D 视频，4087 帧，复杂背景和多种物体运动。
  - **ViDSOD-100**：100 个 RGB-D 视频，9362 帧，包含尺度变化和快速运动。
- **评价指标**：
  - E-measure `E_ξ`、S-measure `S_α`、F-measure `F_β`、MAE `M`。
  - 前三者越高越好，MAE 越低越好。
- **对比方法**：共 13 个 SOTA 方法：
  - MFENet、PICRNet、STDNet、HRTransNet、ATFNet、DPA、DVSOD、DCTNet+、LSTA、MDSAM、SAM2-UNet、TransFlow、KAN-SAM。
- **定性对比场景**：
  - 快速运动：`biking_2`；
  - 复杂背景：`parkout_1`；
  - 低光室内：`DET_book01_indoor`。
- **消融实验**：
  - 深度输入必要性：Pseudo Copy、Pseudo Black、Actual Depth；
  - PEFT 策略：None、Adapter、LoRA、Conv-LoRA、Ours；
  - MoE Gating top-K：1、2、3；
  - Pseudo-Guided Temporal Memory：Baseline、+Mem、+Mem+Gated-MLF；
  - 解码器特征输入：`X_1^D`、`X_2^D`、二者组合；
  - 训练 clip 长度 `T`：2、4、6。
- **实现设置**：
  - 使用 SAM2.1 的 Hiera-L 编码器，SA-1B 预训练，冻结编码器，仅训练注入的 MoE-LoRA。
  - 输入尺寸 352×352，深度归一化并复制为 3 通道。
  - 训练 clip 长度 `T=4`。

## 4. 资源与算力

- 论文明确提到：
  - 使用 **2 张 NVIDIA RTX 4090（48GB）GPU**；
  - 训练 **50 epochs**；
  - 每张 GPU batch size 为 **4**；
  - 每段训练 clip 含 **T=4** 帧；
  - 整个训练过程可在 **5 小时内**完成。
- 优化器与学习率：
  - AdamW；
  - MoE-LoRA 学习率 `1×10^-4`；
  - 其他参数学习率 `1×10^-3`；
  - weight decay `5×10^-4`。
- 未明确说明的信息：
  - 总 GPU 小时数、推理延迟、吞吐量、参数量、FLOPs、能耗等均未报告；
  - 测试阶段算力开销未单独说明。

## 5. 实验数量与充分性

- 实验大致包括：
  - 3 个公开 RGB-D VSOD 数据集上的主实验；
  - 与 13 个 SOTA 方法的定量比较；
  - 代表性视频序列的定性比较；
  - 至少 6 组消融 / 分析实验（深度输入、PEFT 策略、top-K、时序记忆、解码器特征、clip 长度）。
- **充分性**：
  - 覆盖三个数据集和四个指标，主实验较全面；
  - 消融覆盖核心模块：MoE-LoRA、Gated-MLF、Pseudo-Guided Memory、深度模态、时序长度；
  - 对 SAM-based 方法进行了专门比较，说明性能并非仅来自 SAM2 骨干。
- **公平性与客观性**：
  - 使用公开 benchmark 和常用指标，比较对象包括近年 SOTA；
  - 但论文未提供统计显著性检验、误差棒或多次运行方差；
  - 未说明对比方法是否全部在同一训练协议下重训，因此绝对公平性仍有不确定性；
  - 深度输入消融中“Pseudo Copy / Black”是极端替代，不能完全代表真实深度质量变化。

## 6. 主要结论与发现

- M4-SAM 在三个公开 RGB-D VSOD 数据集上**所有评价指标均取得最佳性能**。
- 具体提升：
  - DViSal：E-measure 0.925，F-measure 0.828，相比第二优 KAN-SAM 分别提升 4.5% 和 5.7%；
  - RDVS：E-measure 0.927，超过第二优 DCTNet+ 2.0%；
  - ViDSOD-100：E-measure 0.936，MAE 0.016，相比 KAN-SAM 提升 2.6% 和 0.009。
- 与 SAM-based 方法相比，M4-SAM 平均 E-measure 提升约 6.9%、7.6%、2.9%。
- 消融表明：
  - 深度信息必要；
  - Modality-Aware MoE-LoRA 优于 Adapter、Lo
