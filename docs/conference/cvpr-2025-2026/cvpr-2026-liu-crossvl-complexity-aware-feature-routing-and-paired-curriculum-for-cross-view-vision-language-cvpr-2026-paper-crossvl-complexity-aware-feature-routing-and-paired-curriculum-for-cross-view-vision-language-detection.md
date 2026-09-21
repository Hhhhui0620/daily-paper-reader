---
title: "CrossVL: Complexity-Aware Feature Routing and Paired Curriculum for Cross-View Vision-Language Detection"
title_zh: CrossVL：面向跨视角视觉语言检测的复杂度感知特征路由与成对课程
authors: "Liu, Zhipeng, Luo, Chunbo"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Liu_CrossVL_Complexity-Aware_Feature_Routing_and_Paired_Curriculum_for_Cross-View_Vision-Language_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 5.0
evidence: 跨视角航拍与地面图像及复杂度感知多模态特征路由
tldr: 视觉语言模型在地面与航拍视角差异大的跨视角场景下性能严重退化，固定融合机制难以应对尺度与布局差异。本文提出CrossVL框架，通过复杂度感知路径聚合根据多模态统计估计场景复杂度并路由视觉特征，结合成对课程学习提升检测能力。实验表明该方法在跨视角检测任务上取得更优效果。该工作为无人机航拍多模态感知中的特征路由与融合提供了借鉴。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crossvl-complexity-aware-feature-routing-and-paired-curriculum-for-cross-view-vision-language-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 1248, \"height\": 936}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crossvl-complexity-aware-feature-routing-and-paired-curriculum-for-cross-view-vision-language-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 4, \"index\": 2, \"width\": 4428, \"height\": 2624}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-liu-crossvl-complexity-aware-feature-routing-and-paired-curriculum-for-cross-view-vision-language-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 8, \"index\": 3, \"width\": 2351, \"height\": 1449}]"
motivation: 视觉语言模型在地面与航拍视角差异大的场景下性能退化，固定融合机制难以应对。
method: 提出复杂度感知路径聚合与成对课程学习，依据多模态统计估计复杂度并路由视觉特征。
result: 实验表明方法在跨视角检测任务上取得更优效果。
conclusion: 为航拍多模态感知中的特征路由与融合提供了借鉴。
---

## Abstract
Vision-language models (VLMs) enable text-guided object detection but degrade severely under cross-view scenarios where ground and aerial viewpoints differ in altitude, scale, and spatial layout. These geometric changes introduce systematic complexity variations between viewpoints, e.g., ground view images contain dense and highly occluded structures, while aerial images are sparse and globally organized. Fixed VLM fusion mechanisms cannot handle this discrepancy. We propose CrossVL, a framework combining Complexity-Aware Pathway Aggregation (CPA) and Paired Curriculum Learning (PCL) for enhanced cross-view detection for VLM. CPA estimates scene complexity from multimodal statistics and routes visual features through multiple pathways to obtain view-specific representations. PCL leverages semantic consistency of synchronized ground-aerial pairs to provide stable early supervision and then gradually shifts toward randomized sampling. On MAVREC, CrossVL improves Florence-2's aerial mAP from 58.66% to 61.03% and reduces the ground-aerial performance gap from 8.63pp to 6.65pp, while also achieving a 3.3x reduction in variance across random seeds. CPA provides stable complexity-aware feature aggregation, and PCL enhances optimization dynamics. Together, they demonstrate that coordinated architectural and training adaptations are crucial for robust cross-view VLM detection.

---

## 论文详细总结（自动生成）

# CrossVL 论文中文总结

## 1. 核心问题与整体含义（研究动机与背景）

- **研究背景**：视觉语言模型（VLM）已能通过文本引导实现开放词汇目标检测，但在**跨视角场景**（地面视角与航拍视角）下性能严重退化。二者在高度、尺度、空间布局上存在系统性差异，导致检测性能大幅下降。
- **几何鸿沟（Geometry Gap）**：地面图像中目标更少但更大、覆盖度高、空间聚集紧密；航拍图像中目标更多、尺度更小、空间分布更广、视野更大。这种差异是**几何/空间变化**，而非单纯外观变化（如合成到真实、昼夜变化），因此传统特征对齐策略基本无效。
- **复杂度失衡**：地面场景需要细粒度处理以应对密集目标交互，航拍场景则更依赖全局上下文推理。常规 VLM 融合机制对所有场景采用统一处理，导致表示次优与训练不稳定。
- **未充分利用的成对结构**：MAVREC 等跨视角数据集提供同步的地面–航拍图像对，二者虽空间不重叠但具有相似的物体类别与上下文线索（语义一致性），现有方法却将两视角视为独立样本，浪费了这一监督信号。
- **整体含义**：本文提出 CrossVL，通过**架构适配（CPA）+ 训练策略适配（PCL）**协同应对几何变化引起的复杂度失衡，证明跨视角检测需要针对几何变化而非外观变化专门设计。

## 2. 方法论

### 2.1 核心思想
- 将跨视角检测的挑战归结为**几何诱导的场景复杂度失衡**，通过复杂度感知的特征路由与渐进式跨视角课程学习，在**不增加推理成本**的前提下提升 VLM 的跨视角鲁棒性与训练稳定性。

### 2.2 关键技术细节

**（1）复杂度感知路径聚合（CPA）**

- **复杂度估计**：从多模态特征统计量出发，计算视觉特征均值 μ(V)、标准差 σ(V)、最大值 max(V) 及文本特征均值 μ(T)、标准差 σ(T)，经两层 ReLU MLP（g_φ）与 Softmax 得到三维复杂度向量 **c = [c_s, c_m, c_d] ∈ R³**，分别对应稀疏、中等、密集复杂度。特征方差高通常指示密集地面场景，方差低反映稀疏航拍布局。
- **多粒度路径**：
  - **稀疏路径**：通过可学习注意力 A_s(V) = Softmax(Q_s K_sᵀ/√d) 进行显著 token 选择，适合空间孤立、全局分布的航拍场景。
  - **中等路径**：将特征图划分为固定空间区域，做自适应池化后经可学习跨区域交叉注意力进行区域级聚合，捕捉中程空间依赖，适合地面场景。
  - **密集路径**：全自注意力 + 全局平均池化，建模密集地面场景中的复杂交互。
- **复杂度条件融合**：V_fused = Σ_{p∈{s,m,d}} w_p V_p，其中 w = Softmax(h_ψ([V_s; V_m; V_d; c]))，融合权重同时依赖路径特征与复杂度分数。
- **训练动态**：早期复杂度估计器输出近似均匀分布，随后逐步特化——航拍图像稀疏路径主导、地面图像密集路径激活，中等路径提供平滑过渡。
- **优化与正则**：
  - 辅助视觉–语言对齐损失：**L_align = ||V_fused − T_aligned||²₂**，提供对视角噪声不敏感的稳定训练信号。
  - 路由熵正则：**L_reg = −Σ_p w_p log w_p**，促进路径选择的置信度与非均匀性，防止坍缩到单一通路。
- **轻量化**：仅增加 Florence-2-base 约 **2.5% 参数**，且**仅在训练阶段使用**，推理时零额外计算与延迟。

**（2）成对课程学习（PCL）**

- **动机**：同步地面–航拍对虽空间不重叠，但共享环境条件（天气、光照、时段）与场景上下文，形成稳定的场景级语义锚点。
- **采样调度**：成对采样概率 p_pair(t) 分三阶段——
  - t ∈ [0, T₁)：p_pair = 1（完全成对采样）；
  - t ∈ [T₁, T₂)：线性衰减（按概率混合成对与独立采样）；
  - t ∈ [T₂, T]：p_pair = 0（完全随机采样）。
- **参数设置**：T₁、T₂ 经验设为总训练时长的约 1/3 与 2/3；补充材料显示对调度变化鲁棒（测试 mAP 波动 <2pp）。
- **与 CPA 的互相正则化**：早期成对训练为 CPA 提供稳定复杂度分布；CPA 的复杂度感知表示又防止课程调度引发优化不稳定，二者协同增益超过各自独立贡献之和。

### 2.3 算法流程（文字描述）
1. 输入同步地面–航拍图像对及 COCO 风格标注，转换为 Florence-2 文本格式（⟨OD⟩ 提示 + 归一化坐标至 [0,1000]）。
2. 训练时 CPA 对编码器/解码器中间特征进行复杂度估计，路由至稀疏/中等/密集三路径，加权融合后经共享对齐器投影。
3. 以 VLM 检测损失 + L_align + L_reg 联合优化；PCL 按调度控制采样来源。
4. 推理时移除 CPA，仅保留原 Florence-2 解码流程，无额外开销。

## 3. 实验设计

- **数据集 / 场景**：MAVREC（当前最大的跨视角检测 benchmark），包含 **8,605 对**训练、**538** 验证、**1,614** 测试样本；覆盖北欧城市与乡村环境，10 类目标（tram、bicycle、van、truck、bus、person、car、other、streetlight、traffic light）；地面–航拍同步采集，航拍高度 25–45 m。
- **Benchmark**：MAVREC 的航拍验证集与测试集（默认报告航拍结果）。
- **对比方法**：
  - **视觉单模态基线**（遵循 MAVREC 协议）：DETR、Deformable-DETR、Deformable-DETR*（COCO 预训练）、YOLO-NAS-L、YOLOv7。
  - **视觉–语言基线**：Florence-2-base（随机混合地面与航拍图像训练，无跨视角适配）。
  - 另评估 LoRA（r=16, α=32）微调作为对比。
- **评估指标**：COCO 风格 mAP（IoU 0.50–0.95 步长 0.05）、mAP₅₀、mAP₇₅、mAP_S、mAP_M；NMS IoU 阈值 0.5；Florence-2 不输出置信度，所有预测等权。
- **评估协议**：严格 **val-only 检查点选择**（不接触测试集），3 个随机种子（42、123、789），报告均值与方差。

## 4. 资源与算力

- **GPU**：单张 **NVIDIA RTX 5090**。
- **训练配置**：Florence-2-base（230M 参数）为主干；batch size 8，梯度累积 2 步（有效 batch size 16）；AdamW 优化器，学习率 1×10⁻⁶，weight decay 0.01，500 步 warmup，cosine 调度；FP16 混合精度；训练 **10 个 epoch**。
- **说明**：论文明确给出了上述单卡训练设置；未提及多卡并行或总训练时长（小时数）的细节。

## 5. 实验数量与充分性

- **主要实验组数**：
  - 主结果对比（Table 1）：基线 vs. +CPA vs. +Curriculum vs. +Both，含验证/测试两套指标与 5 个评估维度。
  - 路径架构消融（Table 2）：基线 vs. 单路径变体 vs. 完整 CPA（三路径 + 复杂度路由）。
  - 跨视角鲁棒性（Table 3）：地面/航拍 mAP 与 gap，验证与测试集。
  - 训练稳定性分析（Figure 3）：3 个随机种子的逐 seed 测试 mAP 分布。
  - 路由行为验证：密集路径分数与目标数相关性 r=0.986（p<0.001），稀疏路径 r=−0.988（p<0.001）。
  - 额外对比：LoRA 微调（24.17% 测试 mAP）。
  - 补充材料：T₁、T₂ 调度敏感性分析。
- **充分性与客观性评价**：
  - **优点**：采用严格的 val-only 检查点选择 + 3 seed 均值/方差报告，避免测试集泄漏；消融覆盖路径数量与课程调度；跨视角 gap 与稳定性分析维度较全面。
  - **局限**：所有实验仅在 MAVREC 单一数据集上完成，未跨数据集验证；3 个 seed 数量偏少，对极端失败案例（如 seed 123）的统计推断能力有限；复杂度估计器与路由行为的分析以相关性为主，缺少因果性验证。

## 6. 主要结论与发现

- **性能提升**：CrossVL 将 Florence-2-base 的航拍测试 mAP 从 **58.66% 提升至 61.03%**（+2.37pp），验证 mAP 从 63.73% 提升至 65.35%。
- **跨视角一致性**：地面–航拍测试集性能差距从 **8.63pp 缩小至 6.65pp**，验证集差距从 5.71pp 缩小至 3.73pp。
- **训练稳定性**：随机种子间方差较单独课程学习**降低 3.3×**（±1.50 vs. ±4.97 std）；课程学习单独使用时 seed 123 出现灾难性失败（49.77% mAP），加入 CPA 后恢复至 62.34%。
- **超加性协同**：组合方法验证提升（+1.62pp）超过两组件独立贡献之和（+0.76pp + 0.64pp = +1.40pp），证实互相正则化效应。
- **尺度互补**：CPA 对中等目标提升显著（+10.4pp mAP_M），课程学习改善小目标检测（+1.69pp mAP_S），组合模型继承两者优势。
- **路由有效性**：CPA 路径选择与场景目标数高度相关，证明其成功捕捉了从稀疏航拍到密集地面的复杂度梯度。
- **VLM 优势**：视觉–语言模型显著优于视觉单模态基线（Florence-2 58.66% vs. YOLOv7 31.9% 测试 mAP）；LoRA 微调（24.17%）远低于全量微调，说明跨视角几何鸿沟需要充分参数更新。

## 7. 优点

- **问题定位精准**：明确区分"几何变化"与"外观变化"，将跨视角检测挑战定义为复杂度失衡，区别于常规域适应。
- **架构与训练协同设计**：CPA 解决"特征如何被处理"，PCL 控制"模型看到什么跨视角关系"，二者形成互相正则化，组合效果超加性。
- **轻量且推理零成本**：CPA 仅增加 2.5% 参数且只在训练时启用，兼容实时/资源受限部署。
- **评估协议严谨**：val-only 检查点选择 + 多 seed 均值/方差报告，避免测试集过拟合，提升结果可复现性。
- **路由行为可解释**：通过相关性分析定量验证路径特化，而非仅报告最终指标。
- **诚实报告负面结果**：明确指出课程学习单独使用时的不稳定性与灾难性失败，增强了结论可信度。

## 8. 不足与局限

- **课程学习独立不稳定**：单独使用 PCL 时对随机初始化敏感，seed 123 出现 49.77% vs. 61.59% 的灾难性差距，需依赖 CPA 才能缓解，限制了其独立实用性。
- **复杂度估计过于简单**：仅使用均值、方差、最大值等统计特征，可能在非几何因素（极端光照、传感器噪声）主导特征方差时失效，泛化性存疑。
- **数据集覆盖有限**：仅在 MAVREC 单一数据集上验证，未测试卫星–街景、室内–室外等其他跨视角场景；MAVREC 地域集中于北欧，存在地理偏差风险。
- **实验规模偏小**：仅 3 个随机种子

- **实验规模偏小**：仅 3 个随机种子，统计效力有限；未报告置信区间或显著性检验，难以判断性能提升是否稳健。此外，未在多个数据集或跨域设置下验证，泛化性证据不足。
- **复杂度估计与路由的可解释性有限**：尽管相关性分析显示路径选择与目标数高度相关，但复杂度向量仅由均值、方差、最大值等低阶统计量导出，缺乏对语义类别、遮挡关系或空间布局的显式建模；在极端光照、运动模糊或传感器噪声导致方差异常时，可能产生错误路由。
- **架构设计缺乏充分消融**：三路径的粒度划分、区域池化尺寸、注意力头数等关键超参数未系统消融，无法确定当前配置是否为最优；也未与更简单的动态路由机制（如 MoE）对比。
- **课程学习策略对比不足**：仅验证了成对采样概率的三阶段调度，未与自步学习、难度感知采样等课程学习变体比较，也未分析成对样本语义一致性的量化指标。
- **训练开销未充分报告**：虽然推理零额外成本，但训练阶段 CPA 引入的额外参数、计算量与显存占用未量化；未报告总训练时长、能耗或与基线的训练成本对比。
- **评估维度局限**：仅报告 COCO mAP 系列指标，缺少推理速度（FPS）、模型参数量、FLOPs 等效率指标；未分析不同目标尺度、遮挡程度下的细粒度性能。
- **基线覆盖有限**：未与专门的跨视角/跨域检测方法（如域对抗训练、特征解耦、几何对齐）对比，仅对比通用检测器与 LoRA，难以凸显方法在跨视角领域的相对优势。
- **可复现性细节**：论文未提及代码/模型是否开源，部分超参数（如 MLP 隐藏层维度、对齐器结构）描述不够具体，可能影响复现。

## 9. 总体评价与启示

- CrossVL 的核心贡献在于将跨视角检测的几何鸿沟重新表述为**场景复杂度失衡**，并通过训练时动态路由与成对课程学习实现轻量适配。其“训练时增强、推理时归零”的设计对实际部署友好，超加性协同效应也提供了架构与训练策略联合设计的范例。
- 未来方向包括：引入更丰富的复杂度表征（如目标密度图、语义布局）；将 CPA 扩展到视频或时序跨视角场景；在更多跨视角数据集（卫星–街景、无人机–地面）上验证；探索与在线课程学习、自监督预训练的结合；以及提供更严格的统计检验与效率分析。

（完）
