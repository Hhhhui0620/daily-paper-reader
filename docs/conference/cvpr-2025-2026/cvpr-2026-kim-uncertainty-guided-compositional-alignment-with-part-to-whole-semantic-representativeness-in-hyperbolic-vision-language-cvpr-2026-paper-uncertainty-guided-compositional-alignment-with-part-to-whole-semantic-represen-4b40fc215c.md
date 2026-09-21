---
title: Uncertainty-guided Compositional Alignment with Part-to-Whole Semantic Representativeness in Hyperbolic Vision-Language Models
title_zh: 双曲视觉语言模型中基于部分-整体语义代表性的不确定性引导组合对齐
authors: "Kim, Hayeon, Jang, Ji Ha, Kim, Junghun James, Chun, Se Young"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Kim_Uncertainty-guided_Compositional_Alignment_with_Part-to-Whole_Semantic_Representativeness_in_Hyperbolic_Vision-Language_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 5.0
evidence: 不确定性引导的多模态特征对齐
tldr: 双曲视觉语言模型虽能建模部分与整体关系，却未考虑各部分语义代表性存在差异。本文提出不确定性引导的组合对齐方法UNCHA，通过不确定性建模为不同部分赋予差异化权重。实验证明其提升了双曲视觉语言模型在组合场景下的对齐效果，其不确定性加权对齐思想可迁移至多模态特征融合任务。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 2, \"index\": 1, \"width\": 3072, \"height\": 5071}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 2, \"index\": 2, \"width\": 3072, \"height\": 5071}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 4, \"index\": 3, \"width\": 3675, \"height\": 2397}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 4, \"index\": 4, \"width\": 1198, \"height\": 772}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 4, \"index\": 5, \"width\": 3000, \"height\": 2400}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 4, \"index\": 6, \"width\": 763, \"height\": 871}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 4, \"index\": 7, \"width\": 926, \"height\": 1170}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 4, \"index\": 8, \"width\": 745, \"height\": 996}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 4, \"index\": 9, \"width\": 598, \"height\": 598}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 4, \"index\": 10, \"width\": 892, \"height\": 1312}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 4, \"index\": 11, \"width\": 840, \"height\": 735}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 4, \"index\": 12, \"width\": 876, \"height\": 1001}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 4, \"index\": 13, \"width\": 2961, \"height\": 1974}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 4, \"index\": 14, \"width\": 636, \"height\": 1279}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 4, \"index\": 15, \"width\": 552, \"height\": 552}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 4, \"index\": 16, \"width\": 703, \"height\": 680}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 4, \"index\": 17, \"width\": 709, \"height\": 856}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 4, \"index\": 18, \"width\": 636, \"height\": 1048}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 4, \"index\": 19, \"width\": 588, \"height\": 988}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-020.webp\", \"caption\": \"\", \"page\": 4, \"index\": 20, \"width\": 592, \"height\": 1140}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-021.webp\", \"caption\": \"\", \"page\": 4, \"index\": 21, \"width\": 761, \"height\": 1265}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-022.webp\", \"caption\": \"\", \"page\": 4, \"index\": 22, \"width\": 533, \"height\": 532}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-023.webp\", \"caption\": \"\", \"page\": 4, \"index\": 23, \"width\": 829, \"height\": 1503}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-024.webp\", \"caption\": \"\", \"page\": 4, \"index\": 24, \"width\": 5921, \"height\": 3947}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-025.webp\", \"caption\": \"\", \"page\": 4, \"index\": 25, \"width\": 724, \"height\": 673}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-026.webp\", \"caption\": \"\", \"page\": 4, \"index\": 26, \"width\": 718, \"height\": 1381}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-027.webp\", \"caption\": \"\", \"page\": 4, \"index\": 27, \"width\": 640, \"height\": 274}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-028.webp\", \"caption\": \"\", \"page\": 4, \"index\": 28, \"width\": 641, \"height\": 289}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-029.webp\", \"caption\": \"\", \"page\": 4, \"index\": 29, \"width\": 559, \"height\": 247}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-030.webp\", \"caption\": \"\", \"page\": 4, \"index\": 30, \"width\": 723, \"height\": 1264}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-031.webp\", \"caption\": \"\", \"page\": 4, \"index\": 31, \"width\": 662, \"height\": 1529}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-032.webp\", \"caption\": \"\", \"page\": 4, \"index\": 32, \"width\": 869, \"height\": 789}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-033.webp\", \"caption\": \"\", \"page\": 4, \"index\": 33, \"width\": 593, \"height\": 593}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-034.webp\", \"caption\": \"\", \"page\": 4, \"index\": 34, \"width\": 621, \"height\": 273}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-035.webp\", \"caption\": \"\", \"page\": 4, \"index\": 35, \"width\": 564, \"height\": 564}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-036.webp\", \"caption\": \"\", \"page\": 4, \"index\": 36, \"width\": 621, \"height\": 273}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-037.webp\", \"caption\": \"\", \"page\": 4, \"index\": 37, \"width\": 498, \"height\": 498}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-038.webp\", \"caption\": \"\", \"page\": 4, \"index\": 38, \"width\": 621, \"height\": 275}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-039.webp\", \"caption\": \"\", \"page\": 4, \"index\": 39, \"width\": 587, \"height\": 586}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-040.webp\", \"caption\": \"\", \"page\": 4, \"index\": 40, \"width\": 681, \"height\": 1528}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-041.webp\", \"caption\": \"\", \"page\": 4, \"index\": 41, \"width\": 594, \"height\": 594}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-042.webp\", \"caption\": \"\", \"page\": 5, \"index\": 42, \"width\": 2945, \"height\": 2812}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-043.webp\", \"caption\": \"\", \"page\": 5, \"index\": 43, \"width\": 576, \"height\": 579}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-044.webp\", \"caption\": \"\", \"page\": 5, \"index\": 44, \"width\": 526, \"height\": 529}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-045.webp\", \"caption\": \"\", \"page\": 6, \"index\": 45, \"width\": 2000, \"height\": 1000}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-046.webp\", \"caption\": \"\", \"page\": 6, \"index\": 46, \"width\": 512, \"height\": 512}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-047.webp\", \"caption\": \"\", \"page\": 6, \"index\": 47, \"width\": 2800, \"height\": 2000}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-048.webp\", \"caption\": \"\", \"page\": 8, \"index\": 48, \"width\": 1369, \"height\": 651}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-kim-uncertainty-guided-compositional-alignment-with-part-to-whole-semantic-representativeness-in-hyperbolic-vision-language-cvpr-2026-paper/fig-049.webp\", \"caption\": \"\", \"page\": 8, \"index\": 49, \"width\": 1369, \"height\": 651}]"
motivation: 现有双曲视觉语言模型未建模各部分对整体的语义代表性差异。
method: 提出不确定性引导的组合对齐UNCHA，用不确定性为部分-整体对齐赋予差异化权重。
result: 在组合场景下提升了对齐性能，验证不确定性加权的有效性。
conclusion: 其不确定性感知对齐思路可迁移至多模态特征融合。
---

## Abstract
While Vision-Language Models (VLMs) have achieved remarkable performance, their Euclidean embeddings remain limited in capturing hierarchical relationships such as part-to-whole or parent-child structures, and often face challenges in multi-object compositional scenarios. Hyperbolic VLMs mitigate this issue by better preserving hierarchical structures and modeling part-whole relations (i.e., whole scene and its part images) through entailment. However, existing approaches do not model that each part has a different level of semantic representativeness to the whole. We propose UNcertainty-guided Compositional Hyperbolic Alignment (UNCHA) for enhancing hyperbolic VLMs. UNCHA models part-to-whole semantic representativeness with hyperbolic uncertainty, by assigning lower uncertainty to more representative parts and higher uncertainty to less representative ones for the whole scene. This representativeness is then incorporated into the contrastive objective with uncertainty-guided weights. Finally, the uncertainty is further calibrated with an entailment loss regularized with entropy-based term. With the proposed losses, UNCHA learns hyperbolic embeddings with more accurate part-whole ordering, capturing the underlying compositional structure in an image and improving its understanding of complex multi-object scenes. UNCHA achieves state-of-the-art performance on zero-shot classification, retrieval, and multi-label classification benchmarks. Our code and models are available at: https://github.com/jeeit17/UNCHA.git.

---

## 论文详细总结（自动生成）

# UNCHA 论文总结

## 一、核心问题与整体含义

- **研究背景**：视觉语言模型（如 CLIP、ALIGN、ALBEF）在图像-文本匹配与零样本任务上表现优异，但受限于**欧氏几何**，难以有效刻画层级结构（部分-整体、父子关系），且在复杂多物体组合场景中存在偏置（文本编码器偏向句中首个物体，图像编码器偏向大物体）。
- **双曲几何优势**：双曲空间具有常负曲率与指数级体积增长，能以近乎无失真方式嵌入树状层级结构，因此 MERU、ATMG、HyCoCLIP 等工作将其引入 VLM，通过蕴含（entailment）关系建模跨模态与模态内的部分-整体关系。
- **核心缺口**：现有双曲 VLM 将各“部分”**一视同仁**，未建模每个部分对整体的语义代表性差异——如图中“街道/汽车”比“交通标志/模糊裁剪”更能代表整幅场景。若不加区分，会破坏多物体对齐、导致嵌入空间利用率低下甚至坍缩。
- **整体含义**：论文提出 **UNCHA（UNcertainty-guided Compositional Hyperbolic Alignment）**，用双曲不确定性量化部分-整体语义代表性，实现层级感知与组合式表征学习，提升复杂多物体场景理解。

## 二、方法论

### 核心思想
- 利用双曲半径（嵌入到原点的测地距离）作为语义抽象度/不确定性的代理：**越接近原点 → 越抽象 → 不确定性越高**；越远离原点 → 越具体 → 不确定性越低。
- 据此设计：对**更具代表性的部分赋予低不确定性**（在对比损失中权重更大），对**代表性弱的部分赋予高不确定性**（权重更小），并通过蕴含损失进行校准。

### 关键技术细节
- **双曲不确定性定义**（基于 Lorentz 模型）：
  - u(x) = log(1 + exp(−‖x‖₂))
  - 该式是双曲半径的平滑单调变换，可微且数值稳定。
- **不确定性引导对比损失**：
  - 基础相似度为负 Lorentz 距离，温度 τ 控制尺度。
  - 在全局-局部对比损失中，用逐元素自适应温度：
    - τ^I_un,i = exp(u(i_part_i)/2) · τ_gl
    - τ^T_un,i = exp(u(t_part_i)/2) · τ_gl
  - 不确定性越高 → 温度越大 → 对损失贡献越小。
  - 损失由三部分构成：不确定性引导的全局-局部对比损失 + 全局对比损失（温度 τ_g）+ 局部对比损失（温度 τ_l）。
- **分段连续蕴含损失**：
  - 原始 hinge 形式 L_orig = max(0, φ(p,q) − ηω(p))，一旦 q 落入 p 的蕴含锥内损失即归零，无法继续细粒度对齐。
  - 提出 Leaky-ReLU 式松弛：L*_ent(p,q) = max(0, φ(p,q) − ηω(p)) + α·φ(p,q)，即使 q 在锥内仍保留微小梯度。
- **不确定性校准损失（含熵正则）**：
  - L_cal_ent(p,q) = ⌊L*_ent(p,q)⌋ · e^(−u(p)) + u(p) + H(ũ(p))
  - 蕴含关系弱时 e^(−u(p)) 促使模型提高不确定性；u(p) 项防止为降低损失而盲目增大不确定性；熵项 H 保证不确定性分布多样、避免坍缩。
- **总损失**：L = L_con^un + λ_ent · L_ent^un，其中 L_ent^un 包含跨模态蕴含、模态内蕴含（权重 λ₁）与不确定性校准（权重 λ₂）。

### 算法流程概要
1. 用 Lorentz 模型编码图像/文本（全局与局部）嵌入；
2. 计算各部分嵌入的双曲不确定性 u；
3. 用 u 调制对比损失的温度，得到不确定性引导对比损失；
4. 用分段连续蕴含损失 + 校准项 + 熵正则，校准不确定性；
5. 联合优化，逐步强化部分-整体语义关系，形成更准确的双曲层级排序。

## 三、实验设计

### 训练数据与设置
- **训练集**：GRIT（Grounded Image-Text Pairs），含 **2050 万** 图文对与 **3590 万** 部分级标注。
- **批大小 768，总训练迭代 500,000**。
- 为公平比较，所有基线在**相同数据与训练配置**下复现，同时保留各自原实现中的优化设置。

### 评测任务与 Benchmark
- **零样本图像分类**：16 个数据集（ImageNet、CIFAR-10/100、SUN397、Caltech-101、STL-10、Food-101、CUB、Cars、Aircraft、Pets、Flowers、DTD、EuroSAT、RESISC45、Country211），指标 Top-1 准确率。
- **零样本检索**：COCO 验证集、Flickr30K 测试集，指标 R@1 / R@5（文本检索与图像检索）。
- **层级分类**：ImageNet，采用 HyCoCLIP 的层级指标 TIE(↓)、LCA(↓)、J(↑)、PH(↑)、RH(↑)。
- **零样本多标签分类**：MS-COCO、VOC，指标 mAP。
- **多物体表示与分类**：ComCo（真实物体组合）、SimCo（合成几何图形场景），2–5 个物体配置，mAP。
- **部分级对齐（难负例）**：基于 Densely Captioned Images 构建的基准，报告 All Pick5 与 All Hard Negs。

### 对比方法
- CLIP、MERU、ATMG、HyCoCLIP（均为双曲/欧氏 VLM 代表工作）。
- 架构规模：ViT-S/16 与 ViT-B/16。

## 四、资源与算力

- **论文正文未明确说明 GPU 型号、数量与训练时长**。仅给出批大小（768）与训练迭代数（500,000），以及训练数据规模（GRIT）。
- 致谢中提及获得“AI Computing Infrastructure Enhancement（GPU Rental Support）User Support Program”资助，暗示使用了外部 GPU 租赁资源，但**具体型号与数量未披露**。
- 这一点是复现性与算力成本评估上的信息缺口。

## 五、实验数量与充分性

- **实验规模**：
  - 零样本分类：16 个数据集 × 2 种骨干（ViT-S/ViT-B）；
  - 检索：2 个数据集 × 2 种骨干；
  - 层级分类：ImageNet 多项指标；
  - 多标签分类：VOC、COCO；
  - 多物体：ComCo、SimCo 各 4 种物体数配置；
  - 部分级对齐：All Pick5、All Hard Negs；
  - 消融实验：3 个变体（w/o uncertainty、w/o contrastive、w/o entropy）；
  - 分析实验：不确定性建模分析（图 4，与语义相似度的相关性 r = −0.739）、双曲嵌入半径分布可视化（图 5）。
- **充分性与客观性**：
  - 覆盖任务面广，兼顾通用分类、细粒度分类、检索、层级、多标签与组合场景，**整体较为充分**。
  - 基线在统一数据与配置下复现，**公平性较好**。
  - 消融实验验证了每个模块的必要性。
  - **不足**：消融仅在 ViT-S/16 上进行；部分数据集（如 CUB、Aircraft、EuroSAT）上并非全部指标最优，个别结果存在波动（如 ViT-S 上 CUB 12.5 低于 HyCoCLIP 14.7），论文未对这些下降作深入讨论。

## 六、主要结论与发现

- UNCHA 在零样本分类、检索、多标签分类与层级分类等基准上**达到 SOTA**，在 ViT-S 与 ViT-B 两种骨干下均稳定提升。
- 在多物体组合场景（ComCo、SimCo）与部分级难负例对齐（All Pick5、All Hard Negs）上提升显著，说明其**组合式理解能力更强**。
- 不确定性估计与语义代表性高度吻合：**部分与整体的语义相似度越高，不确定性越低**（相关系数 −0.739）。
- 双曲嵌入分析显示：相比 HyCoCLIP 嵌入集中在狭窄区域，UNCHA 的**部分嵌入更靠近原点、整体嵌入更远**，分布更分散、结构更清晰，说明更高效地利用了双曲空间。
- 消融表明不确定性建模、不确定性引导对比损失、熵正则三者均对性能有实质贡献。

## 七、优点

- **方法创新性强**：首次将“部分对整体的语义代表性差异”显式建模为双曲不确定性，并同时融入对比与蕴含两类损失，思想自然且与双曲几何属性高度契合。
- **数学设计细致**：
  - 分段连续蕴含损失（Leaky-ReLU 式松弛）解决了原 hinge 损失“锥内无梯度”的问题；
  - 校准损失中 e^(−u) 与 u 两项相互制衡，熵正则防止不确定性坍缩，设计合理。
- **实验覆盖广**：涵盖分类、检索、层级、多标签、多物体组合、部分级难负例等六类任务，16 个分类数据集，评估维度全面。
- **公平对比**：所有基线在同一训练数据与配置下复现，减少实现差异带来的偏差。
- **可解释性分析**：通过不确定性与语义相似度的负相关、嵌入半径分布可视化，直观验证了方法的有效性。
- **开源**：代码与模型已公开。

## 八、不足与局限

- **算力信息缺失**：未报告 GPU 型号、数量与训练时长，不利于成本评估与复现。
- **训练数据单一**：仅在 GRIT 上训练，未验证在其他大规模图文数据（如 LAION）上的泛化性。
- **部分结果非最优**：在 CUB、Aircraft、EuroSAT 等数据集上，UNCHA 未全面超过基线（如 ViT-S 上 CUB 低于 HyCoCLIP），论文未对失败案例作分析。
- **超参数依赖**：λ₁、λ₂、λ_ent、α、K、η 等超参数较多，敏感性分析未在正文充分展开（依赖补充材料）。
- **不确定性代理的合理性边界**：以双曲半径作为语义代表性代理依赖“抽象概念靠近原点”的假设，对某些类别（如抽象与具体混杂的场景）是否始终成立值得进一步验证。
- **应用限制**：方法基于 Lorentz 双曲模型与蕴含锥几何，迁移到其他几何/模型时需重新推导；对下游任务（如检测、分割）的适配尚未探索。
- **偏差风险**：GRIT 数据自身的分布偏差可能被不确定性建模放大，代表性弱的部分可能被持续低估。

（完）
