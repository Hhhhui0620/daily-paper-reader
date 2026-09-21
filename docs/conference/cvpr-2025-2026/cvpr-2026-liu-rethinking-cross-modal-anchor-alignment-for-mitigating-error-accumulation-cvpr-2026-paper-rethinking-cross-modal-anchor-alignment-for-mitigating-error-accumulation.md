---
title: Rethinking Cross-Modal Anchor Alignment for Mitigating Error Accumulation
title_zh: 重思跨模态锚点对齐以缓解误差累积
authors: "Liu, Bin, Sun, Wei, Wang, Qianqian, Feng, Wei, Chen, Yijie, Zhang, Haixi"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Liu_Rethinking_Cross-Modal_Anchor_Alignment_for_Mitigating_Error_Accumulation_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 5.0
evidence: 跨模态锚点对齐以缓解匹配误差累积
tldr: 针对跨模态匹配中噪声对应导致误差累积的问题，本文发现干净锚点对也会引发由模态不一致相关性导致的误差累积。为此提出几何-语义学习方法GSL，先利用傅里叶变换强化语义表示，减少非关键细粒度特征扰动带来的跨模态不一致，再结合几何学习缓解误差累积。实验验证了该方法在跨模态匹配中的有效性，为跨模态特征对齐提供新视角。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-rethinking-cross-modal-anchor-alignment-for-mitigating-error-accumulation-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 2, \"index\": 1, \"width\": 1185, \"height\": 1294}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-rethinking-cross-modal-anchor-alignment-for-mitigating-error-accumulation-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 2, \"index\": 2, \"width\": 1147, \"height\": 1296}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-rethinking-cross-modal-anchor-alignment-for-mitigating-error-accumulation-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 2, \"index\": 3, \"width\": 960, \"height\": 765}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-rethinking-cross-modal-anchor-alignment-for-mitigating-error-accumulation-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 3, \"index\": 4, \"width\": 5288, \"height\": 1444}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-rethinking-cross-modal-anchor-alignment-for-mitigating-error-accumulation-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 4, \"index\": 5, \"width\": 2851, \"height\": 1358}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-rethinking-cross-modal-anchor-alignment-for-mitigating-error-accumulation-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 4, \"index\": 6, \"width\": 1327, \"height\": 648}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-rethinking-cross-modal-anchor-alignment-for-mitigating-error-accumulation-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 5, \"index\": 7, \"width\": 4161, \"height\": 1169}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-rethinking-cross-modal-anchor-alignment-for-mitigating-error-accumulation-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 5, \"index\": 8, \"width\": 3365, \"height\": 1330}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-rethinking-cross-modal-anchor-alignment-for-mitigating-error-accumulation-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 8, \"index\": 9, \"width\": 1024, \"height\": 791}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-rethinking-cross-modal-anchor-alignment-for-mitigating-error-accumulation-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 8, \"index\": 10, \"width\": 3128, \"height\": 1707}]"
motivation: 跨模态匹配中误差累积严重，且干净锚点对也会引入模态不一致误差。
method: 提出几何-语义学习GSL，用傅里叶变换强化语义并缓解跨模态不一致。
result: 有效缓解了跨模态匹配中的误差累积问题。
conclusion: 从锚点对角度重新审视并改善了跨模态对齐。
---

## Abstract
Mitigating noisy correspondence in cross-modal matching poses a serious challenge due to the problem of error accumulation. Existing methods primarily attribute this accumulation to errors caused by noisy sample pairs. However, a novel source of error from clean sample pairs (also termed anchor pairs) is discovered in this paper. Such error accumulation is considered to arise from modality-inconsistent correlations. To address this issue, a novel method termed Geometric-Semantic Learning (GSL) is proposed. Firstly, GSL leverages the Fourier transform to emphasize semantic representations and reduce cross-modal inconsistencies caused by perturbations in non-critical fine-grained features, thereby alleviating the error accumulation problem. After that, a Geometry-Aware Label Correction (GALC) method is introduced to re-estimate soft correspondence labels by leveraging angular consistency between noisy sample pairs and anchor pairs across different modalities. Finally, a semantically constrained triplet loss is employed to regulate sample distances using semantic information, enabling robust separation of clean and noisy pairs during the training process. Extensive experiments on three benchmark datasets demonstrate that GSL consistently outperforms existing methods in retrieval accuracy.

---

## 论文详细总结（自动生成）

# 论文总结：Rethinking Cross-Modal Anchor Alignment for Mitigating Error Accumulation

## 1
