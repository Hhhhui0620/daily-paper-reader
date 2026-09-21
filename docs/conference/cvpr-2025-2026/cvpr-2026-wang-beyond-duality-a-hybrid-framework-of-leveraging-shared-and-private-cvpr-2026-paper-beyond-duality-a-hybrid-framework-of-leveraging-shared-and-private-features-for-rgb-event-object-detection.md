---
title: "Beyond Duality: A Hybrid Framework of Leveraging Shared and Private Features for RGB-Event Object Detection"
title_zh: 超越二元：利用共享与私有特征的RGB-Event目标检测混合框架
authors: "Wang, Keyao, Liu, Shuai, Shi, Hengda, Shi, Lukui, Chen, Haiyong"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Wang_Beyond_Duality_A_Hybrid_Framework_of_Leveraging_Shared_and_Private_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 5.0
evidence: 面向多模态融合的共享与私有特征解耦
tldr: RGB-Event目标检测虽能兼顾清晰度与高速信息采集，但现有检测器未显式区分共享与私有特征，融合潜力未被充分挖掘。本文提出基于频域一致性的共享-私有特征解耦方法SPFD，通过FCFS模块分离两类特征并送入专门分支。实验表明该解耦策略提升了多模态检测性能，其融合思路对RGB-T等多模态任务具有借鉴意义。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-beyond-duality-a-hybrid-framework-of-leveraging-shared-and-private-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 3, \"index\": 1, \"width\": 640, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-beyond-duality-a-hybrid-framework-of-leveraging-shared-and-private-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 3, \"index\": 2, \"width\": 640, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-beyond-duality-a-hybrid-framework-of-leveraging-shared-and-private-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 3, \"index\": 3, \"width\": 640, \"height\": 480}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-beyond-duality-a-hybrid-framework-of-leveraging-shared-and-private-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 3, \"index\": 4, \"width\": 934, \"height\": 638}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-beyond-duality-a-hybrid-framework-of-leveraging-shared-and-private-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 3, \"index\": 5, \"width\": 935, \"height\": 639}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-beyond-duality-a-hybrid-framework-of-leveraging-shared-and-private-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 3, \"index\": 6, \"width\": 935, \"height\": 639}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-beyond-duality-a-hybrid-framework-of-leveraging-shared-and-private-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 3, \"index\": 7, \"width\": 508, \"height\": 932}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-beyond-duality-a-hybrid-framework-of-leveraging-shared-and-private-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 3, \"index\": 8, \"width\": 284, \"height\": 488}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-beyond-duality-a-hybrid-framework-of-leveraging-shared-and-private-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 8, \"index\": 9, \"width\": 1200, \"height\": 301}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-beyond-duality-a-hybrid-framework-of-leveraging-shared-and-private-cvpr-2026-paper/fig-010.webp\", \"caption\": \"\", \"page\": 8, \"index\": 10, \"width\": 1200, \"height\": 301}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-wang-beyond-duality-a-hybrid-framework-of-leveraging-shared-and-private-cvpr-2026-paper/fig-011.webp\", \"caption\": \"\", \"page\": 8, \"index\": 11, \"width\": 1200, \"height\": 299}]"
motivation: RGB-Event检测器未显式解耦共享与私有特征，融合特征潜力未被充分利用。
method: 提出频域一致性共享-私有特征解耦网络SPFD，用FCFS模块分离两类特征到专门分支。
result: 有效利用单模态特征，提升多模态目标检测性能。
conclusion: 其共享-私有解耦融合策略可迁移至RGB-T等多模态任务。
---

## Abstract
RGB-Event object detection is able to capture clear and detailed features of the target while maintaining high-speed information collection. It is suitable for high dynamic or harsh environments and has become a research hotspot in recent years. The existing RGB-Event object detectors all struggle to fully utilize the fusion features of two modalities, but do not explicitly disentangle shared vs. private features to dedicated branches. To fully tap into the potential of single features, we propose a frequency-domain coherence-based Shared and Private Features Decoupling method for RGB-Event object detection, SPFD network. First, we design a FCFS module to separate shared and private features by exploring the spectral energy distribution differences between dual modalities. Then, we design a TriAdapt Encoder to process the shared and private features, selectively emphasizing texture-rich RGB features in static regions and motion-sensitive event features in dynamic regions, thereby achieving a robust balance between spatial detail and temporal awareness. Finally, a TriInject Decoder is proposed to emphasize the most discriminative modality features dynamically. Experimental results on the DSEC-Det and PKU-DAVIS-SOD datasets demonstrate that our model achieves competitive performance with state-of-the-art methods.

---

## 论文详细总结（自动生成）

# 论文总结：Beyond Duality — 利用共享与私有特征的 RGB-Event 目标检测混合框架（SPFD）

## 1. 核心问题与整体含义

- **研究背景**：RGB-Event 目标检测融合 RGB 相机与事件相机两种模态，前者擅长捕捉纹理与静态细节，后者在高动态、低光照、高速运动等严苛场景下仍能保持快速响应，近年来成为多模态感知的研究热点，尤其在自动驾驶领域应用前景广阔。
- **核心问题**：现有 RGB-Event 检测器（如 FPN-Fusion、SOD-Former、SFNet、CAFR 等）大多对两模态特征进行**无差别融合**，未能显式地将"共享特征"（两模态语义一致部分）与"模态私有特征"（如低光照下事件流独有的运动信息、相对静止场景下 RGB 独有的纹理信息）解耦到专门分支。这种"一刀切"式融合导致对模态特有优势的挖掘不充分，尤其在某些模态失效或退化时性能受限。
- **整体含义**：论文主张从"二元融合"走向"共享-私有特征重组织"，在频域中显式分离两类特征，并分别服务于编码器与解码器，从而更充分地利用单模态潜力，提升检测在挑战性场景下的鲁棒性。

## 2. 方法论

### 2.1 核心思想

- 提出 **SPFD 网络**（frequency-domain coherence-based Shared and Private Features Decoupling），整体遵循 DETR 风格架构，包含三个关键组件：
  1. **FCFS 模块**：基于频域一致性分离共享与私有特征；
  2. **TriAdapt Encoder**：自适应交互共享与私有特征，生成记忆表示；
  3. **TriInject Decoder**：逐层注入模态私有特征以精修检测框。

### 2.2 关键技术细节

**（1）FCFS 模块（Frequency-domain Coherence-based Feature Separation）**

- **频谱统计**：对 RGB 特征 `x` 与事件特征 `y` 分别做二维 FFT，得到 `X = F(x)`、`Y = F(y)`；计算功率谱 `Sxx = |X|² + ε`、`Syy = |Y|² + ε` 与互谱 `Sxy = X·Y*`（`Y*` 为共轭）。
- **系数计算**：
  - **谱一致性** `γ² = |Sxy|² / (Sxx · Syy)`：衡量两模态在频域的线性相关程度。`γ²→1` 表示响应高度同步，对应共享语义；`γ²→0` 表示不相关，对应私有特征。
  - **强度平衡项** `η = √(Sxx·Syy) / (Sxx + Syy + ε)`：平衡两模态能量差异，抑制某一模态过度主导。
- **特征分离**：
  - 共享掩码 `Ms = σ((γ² · η − τ) / T)`，其中 `τ` 为一致性阈值（0.25），`T` 为温度因子（0.2）。
  - RGB 私有掩码 `Mr = (1−Ms) · |Sxx−Syy|/(Sxx+Syy+ε) · Sxx/(Sxx+Syy)`；
  - Event 私有掩码 `Me = (1−Ms) · |Sxx−Syy|/(Sxx+Syy+ε) · Syy/(Sxx+Syy)`。
  - 频域特征组合：`Zs = Ms ⊙ ½(X+Y)`，`Zr = Mr ⊙ X`，`Ze = Me ⊙ Y`，再经 IFFT 回到空域得到 `zs`、`zr`、`ze`。

**（2）TriAdapt Encoder**

- 每层含两个多尺度可变形注意力（MSDA）分支：以共享特征 `zs` 为 Query，分别以 RGB 私有特征 `zr` 与事件私有特征 `ze` 为 Value，得到 `U_r`、`U_e`。
- **自适应门控**：`Ū = ½(U_r + U_e)`，`G = σ(Wg·Ū)`；融合输出 `Õ = G ⊙ Wr·U_r + (1−G) ⊙ We·U_e`，再经 Norm 与 FFN 精修。
- 门控机制在空间与通道维度动态调节 RGB/事件贡献比例：纹理丰富区域偏向 RGB，高动态区域偏向 Event。

**（3）TriInject Decoder**

- 每层解码器接收多层级记忆特征 `M` 以及私有特征 `zr`、`ze`，先线性投影为 `V_r`、`V_e`。
- 引入可学习缩放系数 `γr`、`γe`，融合为 `V_f = M + γr·V_r + γe·V_e`。
- 以 `V_f` 作为 Value 与 Query 做跨注意力：`Q^(l+1) = D(Q^l, V_f^l)`，实现逐层非对称私有特征注入，使不同解码层分别侧重空间纹理或时序轮廓信息。

## 3. 实验设计

- **数据集**：
  - **DSEC-Det**：驾驶场景多模态基准，RGB 1440×1080、Event 640×480，含 8 个交通类别；消融实验使用原始标注，对比实验采用 SFNet 标注版本以保证公平性。
  - **PKU-DAVIS-SOD**：DAVIS346 事件相机采集，346×260 空间对齐 RGB 与事件流，含 87 万余个人工标注框，覆盖 car、pedestrian、cyclist 三类，包含正常、运动模糊、低光照三种条件。
- **评价指标**：标准 COCO 协议，主指标为 mAP、mAP₅₀、mAP₇₅。
- **对比方法**：
  - **Event-only**：RVT、SAST、S5-ViT、SMamba；
  - **RGB-only**：YOLOX、YOLOv11、MambaYOLO；
  - **RGB-Event 多模态**：FPN-fusion、SODFormer、EOLO、DAGr、SFNet、CAFR、ACGR。
- **主要结果**：DSEC-Det 上 56.7% mAP₅₀ / 34.6% mAP；PKU-DAVIS-SOD 上 62.4% mAP₅₀ / 32.0% mAP。相较 SOTA 分别提升 mAP +4.2%/+0.1%，mAP₅₀ +5.3%/+2.8%。

## 4. 资源与算力

- **GPU**：2 张 NVIDIA RTX 4090。
- **批大小**：每张 GPU 为 4。
- **主干网络**：ResNet-50。
- **训练配置**：100k 次迭代，初始学习率 1×10⁻⁴，在第 80k 次迭代衰减 10 倍。
- **超参数**：ε = 10⁻⁶，τ = 0.25，T = 0.2。
- **说明**：论文未明确给出单次训练的总时长（小时/天）以及总 GPU 时数，仅披露了硬件与迭代次数，因此无法精确核算算力开销。参数量方面，SPFD 为 78.6M，介于 SFNet（57.5M）与 SODFormer/CAFR（82M）之间。

## 5. 实验数量与充分性

- **对比实验**：在 2 个数据集上分别与 4 种事件方法、3 种 RGB 方法、7 种 RGB-Event 方法对比，覆盖面较广。
- **消融实验**：DSEC-Det 测试集上 4 组配置（基线、+FCFS、+FCFS+TA、+FCFS+TA+TD），逐步验证各模块贡献（47.3 → 47.9 → 49.0 → 49.2 mAP）。
- **有效性分析**：分别针对 FCFS（频域可视化对比）、TriAdapt Encoder（伪彩特征与门控图可视化，覆盖正常/低光照/静态三类场景）、TriInject Decoder（mAP 族对比，mAP +0.2%、mAP₇₅ +0.75%、mAP_s +0.16%、mAP₅₀ −0.15%）做了专门分析。
- **可视化分析**：与基线在遮挡、模糊场景下做定性对比。
- **充分性评估**：
  - **优点**：模块级消融与三类场景的可视化分析较为系统，且对比方法覆盖单模态与多模态主流工作，具备一定客观性。
  - **不足**：消融仅在 DSEC-Det 上进行，未在 PKU-DAVIS-SOD 上重复；PKU-DAVIS-SOD 上 mAP 仅领先 0.1%，优势微弱；未报告推理速度/FPS、显存占用等效率指标；未给出多随机种子或误差棒，统计显著性不明确。

## 6. 主要结论与发现

- SPFD 通过频域一致性显式解耦共享与私有特征，在 DSEC-Det 与 PKU-DAVIS-SOD 上均达到 SOTA 水平（34.6% mAP / 32.0% mAP）。
- 频域可视化表明：RGB 特征能量集中于低频，事件特征分布更宽；FCFS 分离后，共享特征保留中低频及方向一致成分，RGB 私有分支捕捉低频语义纹理，事件私有分支强化高频瞬时边缘（呈各向同性环状频谱）。
- TriAdapt Encoder 的门控图验证了其自适应能力：正常场景近场前景偏 RGB、远处小目标与运动目标偏 Event；低光照下偏向 Event，相对静止场景下偏向 RGB。
- TriInject Decoder 通过逐层注入私有特征，主要提升定位精度（mAP₇₅ 与 mAP_s 提升），mAP₅₀ 略有下降，说明其作用更偏向精细框回归。

## 7. 优点

- **思路新颖**：首次在 RGB-Event 检测中显式将特征解耦为"共享 + 两路私有"三条流，并分别服务于编码器与解码器，突破传统无差别融合范式。
- **频域建模有物理依据**：利用谱一致性 γ² 与强度平衡 η 构建可解释的分离掩码，而非纯数据驱动的注意力，分离过程具有频域物理解释性。
- **编码器-解码器协同设计**：TriAdapt 侧重特征选择与记忆构建，TriInject 侧重逐层私有信息注入，形成从空间显著性到时序敏感性的层级过渡。
- **实验较全面**：涵盖两类数据集、单模态与多模态对比、模块消融与多场景可视化，结论有据可依。
- **可复现性**：代码已开源（github.com/git-KeYw/SPFD）。

## 8. 不足与局限

- **极端退化场景鲁棒性不足**：论文自述当两模态同时严重退化（低对比度 APS 成像、噪声事件流、强运动模糊）时，跨模态一致性估计可靠性下降，共享-私有分离失效，检测精度下降；未来工作方向为提升一致性估计的鲁棒性。
- **数据集提升不均衡**：PKU-DAVIS-SOD 上 mAP 仅提升 0.1%，优势不显著，SOTA 领先幅度有限。
- **效率与部署信息缺失**：未报告推理延迟、FPS、显存占用等实用指标；参数量 78.6M 相对较大，实际部署成本未知。
- **实验覆盖的局限**：消融实验仅在 DSEC-Det 上进行，未跨数据集验证模块通用性；未进行多随机种子重复实验，缺乏统计显著性检验。
- **消融中的负向现象**：TriInject Decoder 使 mAP₅₀ 下降 0.15%，说明该模块对宽松 IoU 阈值下的检测并非全为正向增益，其适用边界未深入讨论。
- **主干与配置单一**：仅采用 ResNet-50 主干，未验证其他主干（如 Swin、ViT）下的泛化性；超参数 τ、T 的敏感性分析缺失。
- **应用限制**：主要面向自动驾驶等帧式 RGB-Event 检测设定，对其他多模态组合（如 RGB-T、RGB-D）的可迁移性仅停留在推测层面，未做实证。

（完）
