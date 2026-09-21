---
title: "VT-Intrinsic: Physics-Based Decomposition of Reflectance and Shading using a Single Visible-Thermal Image Pair"
title_zh: VT-Intrinsic：使用单对可见光-热图像进行反射率与光照的物理分解
authors: "Yuan, Zeqing, Ramanagopal, Mani, Sankaranarayanan, Aswin C., Narasimhan, Srinivasa G."
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Yuan_VT-Intrinsic_Physics-Based_Decomposition_of_Reflectance_and_Shading_using_a_Single_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 4.0
evidence: 使用单对可见光-热图像做分解，非显著性检测
tldr: 针对真实场景缺乏反射率与光照真值数据的问题，本文提出基于物理的可见光-热图像对内在分解方法。利用未被反射的光被吸收并以热量被热像仪捕获的原理，将可见光与热图像强度的序关系与光照、反射率序关系关联，从而对优化网络进行稠密自监督以恢复光照与反射率。实验用已知反射率进行定量评估，展示了可见光-热信息融合的物理建模价值，但与显著性检测任务不同。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 3124, \"height\": 2431}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 1, \"index\": 2, \"width\": 2199, \"height\": 464}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 1, \"index\": 3, \"width\": 2094, \"height\": 463}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 1, \"index\": 4, \"width\": 941, \"height\": 464}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 1, \"index\": 5, \"width\": 649, \"height\": 464}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 1, \"index\": 6, \"width\": 344, \"height\": 464}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 1, \"index\": 7, \"width\": 695, \"height\": 464}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 1, \"index\": 8, \"width\": 484, \"height\": 463}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 1, \"index\": 9, \"width\": 484, \"height\": 462}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 1, \"index\": 10, \"width\": 1222, \"height\": 463}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 1, \"index\": 11, \"width\": 4631, \"height\": 2139}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-012.webp\", \"caption\": \"\", \"page\": 1, \"index\": 12, \"width\": 4651, \"height\": 2139}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-013.webp\", \"caption\": \"\", \"page\": 1, \"index\": 13, \"width\": 613, \"height\": 485}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-014.webp\", \"caption\": \"\", \"page\": 1, \"index\": 14, \"width\": 3026, \"height\": 2402}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-015.webp\", \"caption\": \"\", \"page\": 1, \"index\": 15, \"width\": 1364, \"height\": 463}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-016.webp\", \"caption\": \"\", \"page\": 1, \"index\": 16, \"width\": 1481, \"height\": 463}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-017.webp\", \"caption\": \"\", \"page\": 1, \"index\": 17, \"width\": 613, \"height\": 485}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-018.webp\", \"caption\": \"\", \"page\": 1, \"index\": 18, \"width\": 1860, \"height\": 463}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-019.webp\", \"caption\": \"\", \"page\": 1, \"index\": 19, \"width\": 1778, \"height\": 463}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-020.webp\", \"caption\": \"\", \"page\": 1, \"index\": 20, \"width\": 613, \"height\": 485}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-021.webp\", \"caption\": \"\", \"page\": 1, \"index\": 21, \"width\": 1269, \"height\": 464}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-022.webp\", \"caption\": \"\", \"page\": 1, \"index\": 22, \"width\": 828, \"height\": 309}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-023.webp\", \"caption\": \"\", \"page\": 1, \"index\": 23, \"width\": 574, \"height\": 345}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-024.webp\", \"caption\": \"\", \"page\": 1, \"index\": 24, \"width\": 3026, \"height\": 2402}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-025.webp\", \"caption\": \"\", \"page\": 1, \"index\": 25, \"width\": 707, \"height\": 463}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-026.webp\", \"caption\": \"\", \"page\": 1, \"index\": 26, \"width\": 919, \"height\": 464}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-027.webp\", \"caption\": \"\", \"page\": 1, \"index\": 27, \"width\": 326, \"height\": 464}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-028.webp\", \"caption\": \"\", \"page\": 1, \"index\": 28, \"width\": 385, \"height\": 464}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-029.webp\", \"caption\": \"\", \"page\": 1, \"index\": 29, \"width\": 1013, \"height\": 464}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-030.webp\", \"caption\": \"\", \"page\": 1, \"index\": 30, \"width\": 1329, \"height\": 464}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-031.webp\", \"caption\": \"\", \"page\": 1, \"index\": 31, \"width\": 1163, \"height\": 464}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-032.webp\", \"caption\": \"\", \"page\": 1, \"index\": 32, \"width\": 1111, \"height\": 463}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-033.webp\", \"caption\": \"\", \"page\": 1, \"index\": 33, \"width\": 623, \"height\": 495}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-034.webp\", \"caption\": \"\", \"page\": 1, \"index\": 34, \"width\": 485, \"height\": 464}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-035.webp\", \"caption\": \"\", \"page\": 1, \"index\": 35, \"width\": 1411, \"height\": 464}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-036.webp\", \"caption\": \"\", \"page\": 1, \"index\": 36, \"width\": 1188, \"height\": 939}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-037.webp\", \"caption\": \"\", \"page\": 1, \"index\": 37, \"width\": 2727, \"height\": 464}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-038.webp\", \"caption\": \"\", \"page\": 3, \"index\": 38, \"width\": 1705, \"height\": 2534}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-039.webp\", \"caption\": \"\", \"page\": 3, \"index\": 39, \"width\": 1705, \"height\": 2805}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-040.webp\", \"caption\": \"\", \"page\": 5, \"index\": 40, \"width\": 2217, \"height\": 1247}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-041.webp\", \"caption\": \"\", \"page\": 8, \"index\": 41, \"width\": 400, \"height\": 316}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-042.webp\", \"caption\": \"\", \"page\": 8, \"index\": 42, \"width\": 400, \"height\": 316}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-043.webp\", \"caption\": \"\", \"page\": 8, \"index\": 43, \"width\": 400, \"height\": 316}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-044.webp\", \"caption\": \"\", \"page\": 8, \"index\": 44, \"width\": 400, \"height\": 316}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-045.webp\", \"caption\": \"\", \"page\": 8, \"index\": 45, \"width\": 400, \"height\": 305}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-046.webp\", \"caption\": \"\", \"page\": 8, \"index\": 46, \"width\": 400, \"height\": 305}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-047.webp\", \"caption\": \"\", \"page\": 8, \"index\": 47, \"width\": 400, \"height\": 304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-048.webp\", \"caption\": \"\", \"page\": 8, \"index\": 48, \"width\": 400, \"height\": 304}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-049.webp\", \"caption\": \"\", \"page\": 8, \"index\": 49, \"width\": 400, \"height\": 313}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-050.webp\", \"caption\": \"\", \"page\": 8, \"index\": 50, \"width\": 400, \"height\": 313}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-051.webp\", \"caption\": \"\", \"page\": 8, \"index\": 51, \"width\": 400, \"height\": 313}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-yuan-vt-intrinsic-physics-based-decomposition-of-reflectance-and-shading-using-a-single-cvpr-2026-paper/fig-052.webp\", \"caption\": \"\", \"page\": 8, \"index\": 52, \"width\": 400, \"height\": 313}]"
motivation: 真实场景缺乏反射率与光照的真值数据，内在分解困难。
method: 利用可见光-热强度序关系建立物理约束，稠密自监督优化网络恢复光照与反射率。
result: 在已知反射率数据上完成定量评估，验证了物理建模的有效性。
conclusion: 展示了可见光-热图像对在内在分解中的物理建模潜力。
---

## Abstract
Decomposing a scene into its reflectance and shading is a challenge due to the lack of extensive ground-truth data for real-world scenes. We introduce a novel physics-based approach for intrinsic image decomposition using a pair of visible and thermal images. We leverage the principle that light not reflected from an opaque surface is absorbed and detected as heat by a thermal camera. This allows us to relate the ordinalities (or relative magnitudes) between visible and thermal image intensities to the ordinalities of shading and reflectance. The ordinalities enable dense self-supervision of an optimizing neural network to recover shading and reflectance. We perform quantitative evaluations with known reflectance and shading under natural and artificial lighting, and qualitative experiments across diverse scenes. The results demonstrate superior performance over both physics-based and recent learning-based methods, providing a path toward scalable real-world data curation with supervision.

---

## 论文详细总结（自动生成）

# VT-Intrinsic 论文中文总结

## 1. 核心问题与研究动机

- **问题定位**：内在图像分解（Intrinsic Image Decomposition, IID）旨在将图像分解为**反射率（albedo）**与**光照/明暗（shading）**，是图形学（重着色、重打光、合成）与视觉（识别、跟踪）的基础任务。
- **核心痛点**：真实场景的反射率与光照真值**几乎无法采集**（需专用设备与受控流程），因此现有方法要么依赖合成数据（存在 sim-to-real 差距），要么依赖统计先验（易过平滑、幻觉化）。
- **关键观察**：对于不透明表面，**未被反射的光被吸收并转化为热**，可被长波红外（8–14 µm）热像仪捕获。因此：
  - 低反射率区域（可见光下暗）在热图中偏亮；
  - 光照变化在可见光与热图中同向变亮。
- **整体含义**：本文提出仅用**单张热图像**作为辅助模态，通过可见光–热强度之间的**序关系（ordinality）**建立物理约束，实现无需真值、无需学习先验的稠密自监督分解，并为真实世界数据监督的可扩展采集提供路径。

## 2. 方法论

### 2.1 核心思想
- 利用"反射光 = 可见图像"与"吸收光 = 热源"的互补关系，将可见–热强度序关系映射为 albedo / shading 序关系。
- 不估计吸收热量 H，而是直接使用热图像强度 It 作为代理，避免辐射标定、光照控制与视频采集。

### 2.2 物理建模与公式推导
- 可见成像（Lambertian）：`Iv(x) = g·ρ(x)·η(x)`（ρ 为反射率，η 为辐照度，g 为增益常数）。
- 热源强度：`H = (1 − ρ)·η`。
- **局部（边缘）约束**：对两者求梯度并利用"边缘主导项"假设得：
  - Albedo 边缘（∇η→0）：`sign(∇Iv) = −sign(∇H)`（可见与热梯度反向）；
  - Shading 边缘（∇ρ→0）：`sign(∇Iv) = sign(∇H)`（同向）。
- **非局部（点对）约束**：
  - 命题 1（Albedo 序）：若 `Iv(xi) < Iv(xj)` 且 `H(xi) > H(xj)`，则 `ρ(xi) < ρ(xj)`；
  - 命题 2（Shading 序）：若 `Iv(xi) < Iv(xj)` 且 `H(xi) < H(xj)`，则 `η(xi) < η(xj)`。
- **含不可见光扩展**：`H = (β − ρv)·η`，其中 `β = 1 + (1 − ρi)·li/lv`。由于红外反射率变化远小于可见光，β 在局部近似常数，序关系仍成立。
- **热图与热强度关系**：由热传导方程在稳态下推导得 `H = c1·It − c2·ΔIt − c3`，在局部区域内 c1、c2、c3 近似常数，故 **It 的序关系与 H 一致（命题 3）**，可将上述约束直接替换为热图像强度。

### 2.3 损失函数与优化流程
- **边缘损失 Ledge**：先用可见–热梯度的余弦相似度对边缘分类（A=albedo 主导，S=shading 主导），再惩罚 shading 主导边缘处的 albedo 梯度、albedo 主导边缘处的 shading 梯度。
- **点对损失 Lord**：用 Poisson 盘采样生成随机点对，依归一化强度差 δIv、δIt 标注为 S+/S−/A+/A−，使用**带 margin 的 hinge 损失**约束估计值的序关系。
- **正则化**：采用 **Double-DIP（DDIP）**，即两个随机初始化、冻结输入噪声的编码–解码网络（带跳连）分别参数化 albedo（3 通道，sigmoid 约束到 [0,1]³）与 shading（单通道，加非负惩罚），利用网络结构先验进行正则化。
- **总目标**：`L = ‖ρ̂·η̂ − Iv‖² + λ1·Ledge + λ2·Lord`。热图像仅参与边缘与点对损失，重建损失作用于 3 通道可见图像。

## 3. 实验设计

- **数据集 / 场景**：
  - 自建 **VT-Intrinsic 数据集**：600 对可见–热图像，涵盖公园、学校、教堂、广场、博物馆、街道等静态户外场景。
  - **颜色图表（Color Chart）**：在白色 LED、白炽灯、日光三种光照下拍摄，提供已知反射率。
  - **JoLHT-Video 数据集**：4 个颜色图表场景 + 1 个 Painted-Mask 场景，含线光源强光照变化。
  - **MIT-Intrinsics**：通过仿真理想热图像进行补充验证。
- **成像系统**：FLIR Boson 热像仪（512×640，50 mK NEDT）与 IDS UI-3130 彩色相机（600×800）通过金二色镜共光路；远景采用并排 + 单应对齐；20 张曝光包围图合成 HDR，5 帧平均降噪。
- **Benchmark / 指标**：使用**尺度不变均方误差（si-MSE）** 评价 albedo 与 shading。
- **对比方法**：
  - 优化类：RGB-Retinex、Opt-LocalSmooth；
  - 学习类：IntrinsicDiffusion、RGB$X、Intrinsic-v2、Intrinsic-v1、CRefNet；
  - 物理类：NIR-Priors（需 NIR 图）、JoLHT-Video（需受控光照下的瞬态热视频）。

## 4. 资源与算力

- **论文未明确说明**所使用的 GPU 型号、数量、训练时长或显存消耗等信息。
- 仅可知方法基于随机初始化网络的**逐场景优化（Double-DIP）**，属于无需大规模预训练的优化框架，但具体算力开销未在正文中量化披露。

## 5. 实验数量与充分性

- **序关系验证（3 类）**：
  - 多材质 patch 序关系：CUReT 20 个 patch + 常见物体，专家标注 865 条序关系，日光下准确率 98.59%、白光 LED 下 96.82%；
  - 真实场景点对序关系：100 个场景，专家标注 1063 对，总体准确率 98.95%（albedo 96.96%，shading 99.62%）；
  - 光谱统计验证：USGS 427 种材质 + ASTM-G173 太阳光谱，90,951 个材质对中 94.2% 序关系成立。
- **定量分解实验**：3 种光照下的颜色图表 + JoLHT-Video 的 4 组颜色图表与 Painted-Mask（Tab. 1）。
- **定性实验**：VT-Intrinsic 多样场景对比（约 5 类代表性案例）+ JoLHT-Video 场景。
- **补充实验**：MIT-Intrinsics 仿真、消融研究、序关系信息量仿真、低光/非平衡热条件分析。
- **充分性与公平性评价**：
  - 优点：序关系理论经过专家标注与光谱数据库**双重统计验证**，验证维度较全面；对比方法覆盖三类主流范式，定量/定性结合。
  - 局限：定量评估主要基于颜色图表等受控场景，真实复杂场景以定性为主；VT-Intrinsic 数据集规模（600 对）与场景多样性仍有限；未给出统计显著性检验或多次运行的方差。

## 6. 主要结论与发现

- 单张稳态热图像足以提供**可靠的 albedo / shading 序关系约束**，无需视频、辐射标定或光照控制。
- 在颜色图表与 JoLHT-Video 数据集上，本方法**优于所有学习类基线**（尽管不使用任何预训练先验），且性能**接近需要瞬态热视频与受控光照的 JoLHT-Video**。
- 在复杂真实场景中，本方法能有效去除投影阴影（如栏杆、灯笼阴影）、分离 albedo 纹理与 shading（如犀牛雕像、棋盘格），并正确处理类 Adelson 棋盘阴影错觉场景；学习类基线则常出现过平滑或纹理泄漏/幻觉。
- 序关系理论在日光与白炽灯等含红外分量的光源下依然稳健。

## 7. 优点

- **物理建模扎实**：从 Lambertian 成像与热传导方程出发，完整推导从可见–热序关系到 albedo / shading 序关系的链条，并给出含不可见光、热图代理的严格扩展与命题。
- **无需真值、无需预训练**：仅依赖单张热图与随机初始化网络的 Double-DIP 参数化，避免 sim-to-real 差距与统计先验导致的幻觉。
- **工程可行性高**：单张稳态热图即可，数秒内可达热平衡，避免了 JoLHT-Video 的视频采集、主动光照控制与辐射标定要求。
- **验证体系互补**：理论序关系同时用专家标注与光谱数据库统计验证，可信度较高。
- **数据集贡献**：发布 600 对高质量真实可见–热图像，提供稠密伪真值序关系，可监督学习方法。

## 8. 不足与局限

- **物理假设限制**：假设以漫反射为主、热量主要来自光吸收、无多重彩色光照；金属、透明物体、镜面会违反成像模型；发动机、人体、热风、火等非光吸收热源不被建模。
- **传感器限制**：依赖低成本的微测辐射热计热像仪，SNR 与分辨率低于可见光相机；弱光照、阴天或动态场景下性能下降。
- **实验覆盖偏差**：定量评估集中于颜色图表等受控场景；户外复杂场景以定性为主，缺乏真实 albedo / shading 真值；VT-Intrinsic 规模与多样性有限。
- **对比公平性细节**：部分基线（如 NIR-Priors、JoLHT-Video）在部分设置下标注为 N/A 或不可用，跨方法比较在可用性上并不完全对齐。
- **算力与可复现性**：未披露算力开销、训练时长与超参数敏感性，复现成本不明确。
- **应用边界**：需可见光与热像仪严格配准，实际部署中对齐误差、时间同步（动态场景）可能影响效果。

（完）
