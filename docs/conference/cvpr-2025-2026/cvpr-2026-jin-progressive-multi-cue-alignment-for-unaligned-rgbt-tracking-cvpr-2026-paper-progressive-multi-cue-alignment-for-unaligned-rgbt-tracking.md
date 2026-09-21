---
title: Progressive Multi-cue Alignment for Unaligned RGBT Tracking
title_zh: 面向未对齐RGBT跟踪的渐进式多线索对齐
authors: "Jin, Jiandong, Li, Chenglong, Feng, Hao, Lu, Andong, Huang, Lili, Tang, Jin"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Jin_Progressive_Multi-cue_Alignment_for_Unaligned_RGBT_Tracking_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 8.0
evidence: 面向空间错位RGB与热红外的跨模态对齐
tldr: 该文研究未对齐RGB-T跟踪，即在空间错位的可见光与热红外视频中实现鲁棒目标定位，是RGB-T落地的重要挑战。现有方法同时求解全部跨模态对齐参数，难以适应不同错位程度且计算负担大。作者提出渐进式多线索对齐框架PMATrack，将对齐参数计算进行渐进式解耦。实验表明该方法在应对不同错位难度时更高效且更鲁棒。其未配准跨模态对齐思想对UAV RGB-T显著目标检测高度相关。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jin-progressive-multi-cue-alignment-for-unaligned-rgbt-tracking-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 2, \"index\": 1, \"width\": 4463, \"height\": 1256}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jin-progressive-multi-cue-alignment-for-unaligned-rgbt-tracking-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 2, \"index\": 2, \"width\": 3025, \"height\": 2594}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jin-progressive-multi-cue-alignment-for-unaligned-rgbt-tracking-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 4, \"index\": 3, \"width\": 6071, \"height\": 2111}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jin-progressive-multi-cue-alignment-for-unaligned-rgbt-tracking-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 5, \"index\": 4, \"width\": 3850, \"height\": 2188}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jin-progressive-multi-cue-alignment-for-unaligned-rgbt-tracking-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 8, \"index\": 5, \"width\": 3510, \"height\": 1953}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jin-progressive-multi-cue-alignment-for-unaligned-rgbt-tracking-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 8, \"index\": 6, \"width\": 2237, \"height\": 1152}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-jin-progressive-multi-cue-alignment-for-unaligned-rgbt-tracking-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 8, \"index\": 7, \"width\": 4373, \"height\": 2156}]"
motivation: 现有未对齐RGB-T跟踪同时求解全部对齐参数，难以适应不同错位程度且计算开销大。
method: 提出渐进式多线索对齐框架PMATrack，对跨模态对齐参数（空间位移与尺度变化）进行渐进解耦。
result: 实验显示该方法在不同错位难度下更鲁棒且计算更高效。
conclusion: 渐进式跨模态对齐有效缓解空间错位，对未配准RGB-T检测任务具有直接借鉴价值。
---

## Abstract
Unaligned RGBT tracking aims to achieve robust target localization across spatially misaligned RGB and thermal infrared (TIR) videos, a crucial challenge for deploying RGBT tracking in real-world scenarios. Existing methods often calculate all cross-modal alignment parameters (i.e., spatial shift and scale change) simultaneously, but suffer from two major limitations. 1) They are difficult to adapt to different degrees of unaligned difficulty during tracking. 2) They usually require complex models to handle challenging scenarios, resulting in a large computational burden. To overcome these limitations, we propose a novel Progressive Multi-cue Alignment framework called PMATrack, which disentangles the calculation of cross-modal alignment parameters in a progressive manner and dynamically selects appropriate cues to handle different challenges, thereby enabling robust and efficient unaligned RGBT tracking. In particular, PMATrack divides the cross-modal alignment parameter estimation into three stages to progressively perform center offset computation, scale transformation estimation, and global refinement. At each stage, we design a difficulty-aware router to adaptively select the appropriate alignment expert based on the cross-modal alignment complexity, thereby reducing computational redundancy. In addition, we build a high-quality video benchmark called MUART244 to facilitate the comprehensive evaluation of different unaligned RGBT tracking algorithms. Extensive experiments demonstrate the outstanding performance of PMATrack against existing state-of-the-art methods. The code and dataset will be available at https://github.com/NOP1224/Unaligned_RGBT_Tracking.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义

- **研究任务**：未对齐 RGBT 跟踪，即在空间错位的可见光（RGB）与热红外（TIR）视频中实现鲁棒目标定位。
- **背景痛点**：主流 RGBT 数据集通常经过昂贵的人工对齐，导致现有跟踪器默认模态间空间对应完美；但真实多传感器系统因安装偏移、视场差异等，原始跨模态图像存在显著空间错位。
- **现有方法局限**：
  - 同时估计全部跨模态对齐参数（空间位移与尺度变化），难以适应跟踪过程中不同错位难度；
  - 静态对齐架构通常依赖复杂模型处理困难场景，计算负担大。
- **整体含义**：论文提出渐进式多线索对齐框架 PMATrack，通过解耦对齐参数并动态选择合适线索，兼顾鲁棒性与效率，推动 RGBT 跟踪在真实未对齐场景中的部署。

## 2. 方法论

- **核心思想**：将对齐参数估计解耦为三个渐进阶段——中心偏移、尺度变换、全局精修，并在每个阶段根据场景复杂度自适应选择对齐专家。
- **渐进式对齐流程**：
  - 浅层利用几何线索预测中心偏移 \(P_{center}=[dx,dy]\)；
  - 中层结合几何与语义线索估计尺度变换 \(P_{scale}=[\Delta dx,\Delta dy,s_x,s_y]\) 并精修中心偏移；
  - 深层利用高层语义进行全局残差精修 \(P_{refine}=[\Delta dx,\Delta dy,\Delta s_x,\Delta s_y]\)。
  - 每阶段偏移由专家模块 \(E(\cdot)\) 预测：\(P_k=E([Z_V^i,X_V^i],[Z_I^i,X_I^i])\)。
- **难度感知多线索专家（DMAE）**：
  - **目标响应专家（TRE）**：计算模态特定目标响应图，引入最优传输矩阵建模跨模态显著性整体偏移结构，输出偏移 \(P_t\)；
  - **特征匹配专家（FME）**：对搜索区域特征做高低频分解，分别计算跨模态相关性并门控融合，经金字塔相关头预测偏移 \(P_c\)，应对遮挡或相似干扰；
  - **细节感知专家（DPE）**：使用 Tiny U-Net 提取多尺度细粒度信息，拼接后预测偏移 \(P_d\)，应对低质量或结构信息不足场景；
  - **路由器**：根据 \([X_V;X_I]\) 产生选择概率 \(r_e\)，最终偏移 \(P=\sum_e r_e P_e\)；
  - **成本惩罚专家选择损失**：\(L_{CPESL}=\sum_e r_e \ell_e+\lambda_{cost}\sum_e r_e c_e\)，平衡精度与计算成本，\(\lambda_{cost}=0.01\)。
- **变换引导跨模态可变形注意力（TCMDA）**：
  - 将每阶段预测偏移转为 3×3 单应矩阵 \(H\)，生成初始采样网格；
  - 目标点投影到源模态得到几何先验 \(\Delta H\)，再结合可学习局部偏移 \(\Delta L\) 与注意力权重，最终采样位置 \(G_{h,k}=p_t+\Delta H_h+\Delta L_{h,k}\)；
  - 对源特征采样并加权聚合，残差连接增强源模态表示，实现对齐引导融合。
- **训练与推理**：
  - 两阶段训练：第一阶段训练跟踪骨干（OSTrack 损失），第二阶段训练对齐网络与 TCMDA；
  - 损失包括平滑 L1 偏移损失、TRE 响应图 BCE 损失、CPESL 及跟踪损失；
  - 推理时采用模板-偏移对比更新（TOCU），维护动态单应矩阵，根据可靠性选择性更新，防止搜索区域丢失目标。

## 3. 实验设计

- **数据集与 Benchmark**：
  - 在 **LasHeR-Unaligned** 训练集上重训练所有跟踪器，并在其测试集及新构建的 **MUART244** 上评估。
  - **MUART244**：首个多平台未对齐 RGBT 跟踪数据集，含 143 个地面视角和 101 个空中视角序列对，共 244 对；无人工预对齐，双模态精确标注；覆盖 26 类目标、22 种挑战；分辨率从 \(1600\times1200/640\times480\) 到 \(3840\times2160/1280\times1024\)，相比 LasHeR-Unaligned 具有更大空间错位和更广目标尺寸比。
- **评价指标**：PR、NPR、SR，采用 OPE 协议。
- **对比方法**：
  - LasHeR-Unaligned：MANet、1MaCNet、CAT、FANet、ADRNet、MANet++、APFNet、DMCNet、ToMP、OSTrack、TBSI、ViPT、SDSTrack、UnTrack、BAT、GMMT、AFter、SUTrack、CAFormer、AINet、NAT 等。
  - MUART244：OSTrack、TBSI、ViPT、SDSTrack、UnTrack、BAT、GMMT、AFter、SUTrack、CAFormer、AINet 等。
- **实验类型**：SOTA 对比、模块消融、渐进策略消融、在线偏移预测必要性分析、挑战属性雷达图可视化、渐进对齐与专家选择可视化。

## 4. 资源与算力

- 论文明确说明：基于 PyTorch，使用 **单张 NVIDIA RTX 4090 GPU** 训练。
- 优化器 AdamW，权重衰减 \(1\times10^{-4}\)，batch size 16，学习率 \(1\times10^{-4}\)。
- 两阶段训练：分别 20 和 30 个 epoch，每 epoch 提供 60,000 个样本对。
- 参数初始化使用 DropMAE 预训练权重。
- **未明确说明**：总训练时长、总 GPU 小时、能耗、推理硬件配置及参数量等。
- 推理速度：表 1 中 PMATrack 为 28.0 FPS。

## 5. 实验数量与充分性

- **实验组数概览**：
  - 两个数据集上的大规模 SOTA 对比（LasHeR-Unaligned 表 1，MUART244 表 2）；
  - 模块消融（表 3）：Baseline、TRE、FME、DPE、TOCU 及全量组合；
  - 渐进策略消融（表 5）：Baseline、Only Center、Center+Scale、Center+Scale+Refinement；
  - 第一帧对齐对比（表 4）：5 个 SOTA 跟踪器使用初始帧偏移对齐后续帧；
  - 可视化分析：22 种挑战雷达图、渐进对齐过程、专家选择行为。
- **充分性评价**：
  - 覆盖两个数据集、多类 SOTA、多个模块消融和参数分析，整体较充分；
  - 所有跟踪器在相同训练集重训练，评估协议统一，公平性较好；
  - 但 MUART244 的详细统计与构建细节多在补充材料，正文信息有限；
  - 未报告超参数敏感性（如 \(\lambda_{cost}\) 变化影响）、统计显著性检验或误差棒；
  - 新数据集由作者构建，可能存在一定评估偏向风险。

## 6. 主要结论与发现

- PMATrack 在 LasHeR-Unaligned 上达到 PR 64.4%、NPR 58.7%、SR 50.6%，相比 AINet 分别提升 +3.0%、+3.0%、+2.3%；相比 NAT 提升 +6.3%、+6.4%、+5.8%。
- 在 MUART244 上达到 PR 62.7%、NPR 55.9%、SR 45.8%，相比 SUTrack 提升 +13.2%、+15.0%、+12.3%；相比 UnTrack 提升 +8.6%、+8.0%、+5.9%。
- 渐进式对齐策略有效：中心偏移带来明显增益，加入尺度变换和全局精修后性能持续提升。
- 难度感知专家选择有效：简单场景偏向轻量 TRE，遮挡或运动模糊时转向 FME 和 DPE。
- TOCU 动态偏移更新进一步提升时序稳定性，尤其在严重且动态变化的错位场景中。
- 在 MUART244 的 22 种挑战属性上，PMATrack 在大多数挑战下优于对比方法，在严重跨模态错位场景中增益尤为明显。

## 7. 优点

- **方法设计亮点**：
  - 将对齐参数解耦为三阶段，避免直接回归耦合的单应矩阵，符合由粗到细的感知逻辑；
  - 难度感知路由与成本惩罚损失，在精度与效率间取得平衡；
  - 三类专家分别针对简单、遮挡干扰、低质量细节场景，互补性强；
  - TCMDA 将几何先验与可变形注意力结合，减少直接对齐融合引入的噪声；
  - TOCU 在推理阶段动态维护偏移，增强跨帧稳定性。
- **实验与数据亮点**：
  - 构建 MUART244，填补多平台、大错位、多分辨率未对齐 RGBT 跟踪基准的空白；
  - 在多个数据集和大量 SOTA 方法上验证，消融实验较系统；
  - 提供挑战属性雷达图与可视化，增强可解释性。

## 8. 不足与局限

- **资源与效率**：
  - 仅报告单张 RTX 4090 训练，未给出总训练时长、参数量或推理硬件细节；
  - 28.0 FPS 低于部分对比方法（如 CAFormer 86.3 FPS、SUTrack 55 FPS），实时性优势并非绝对。
- **实验覆盖与公平性**：
  - MUART244 由作者构建，虽然标注精细，但可能存在数据集偏置；
  - 未与所有跨模态对齐专用方法全面对比（如 AMNet 等未在表中出现）；
  - 仅采用 OPE 协议，未报告其他评估协议或统计显著性；
  - 超参数 \(\lambda_{cost}\) 固定为 0.01，未分析其敏感性。
- **应用限制**：
  - 极端错位、模态缺失或严重遮挡下的鲁棒性仍需更广泛验证；
  - 渐进式多专家与 TCMDA 增加模型复杂度，部署到边缘设备可能受限；
  - 动态单应矩阵更新依赖可靠性判断，在快速运动或目标出视野时可能失效。

（完）
