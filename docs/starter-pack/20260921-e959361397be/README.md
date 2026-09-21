<div class="dpr-topic-result-actions"><button type="button" data-topic-copy="docs/starter-pack/20260921-e959361397be/papers.md">复制论文清单</button> <a href="docs/starter-pack/20260921-e959361397be/papers.md" download data-no-router>下载 Markdown</a> <a href="docs/starter-pack/20260921-e959361397be/papers.json" download data-no-router>下载 JSON</a> <button type="button" data-topic-continue="20260921-e959361397be">继续生成阅读内容</button></div>

# uav-rgbt-sod · 入门导读

> 本导读基于所列论文的标题、摘要和已有速览，不代表已阅读全部全文。近期窗口不是完整领域史；检索不保证覆盖全部相关论文。模型导读需结合原文核验。

检索窗口：arXiv &#91;2025-09-21, 2026-09-21&#41;；会议 &#91;2024-09-21, 2026-09-21&#41;（UTC，结束日不含）

## 方向概览

本导读聚焦面向无人机平台的未配准RGB-T显著目标检测中的不确定性感知跨模态对齐问题。研究问题可概括为：当可见光与热红外图像因传感器视差、平台振动、视角变化和尺度差异而存在空间未配准，且各模态可靠性随光照、运动模糊、噪声和传感器伪影动态变化时，如何显式建模跨模态对齐可靠性与模态不确定性，并据此进行鲁棒的特征对齐与融合，从而提升显著目标检测性能。输入论文显示，相关研究已从早期依赖人工配准数据转向直接处理未配准图像对，并出现三类主要思路：一是显式空间对齐与语义约束，如薄板样条、可变形对齐、仿射配准和图结构校准；二是可靠性或不确定性引导的融合与专家路由，如空间可靠性图、证据融合、熵引导门控和频谱可靠性描述子；三是借助基础模型、扩散模型和状态空间模型提升边界与结构恢复能力。评测方面，输入中出现的基准包括UVT20K、VT821、VT1000、VT5000、VT-IMAG、MBU、DroneVehicle、DVMA、FLIR、M3FD、VEDAI、LLVIP、MFNet、PST900、MVSeg和CART等，但多数论文未提供统一协议下的横向对比，且部分数据集面向检测或分割而非SOD，跨任务可比性有限。主要局限包括：未配准SOD专用基准仍较少，不确定性建模多停留在启发式可靠性而非严格概率校准，部分证据仅来自摘要且缺少可复现实验细节。

依据：[Breaking Alignment Barriers: TPS-Driven Semantic Correlation Learning for Alignment-Free RGB-T Salient Object Detection](/20250921-20260920/2512.21856v1)；[Alignment-Free RGB-T Salient Object Detection: A Large-Scale Dataset and Progressive Correlation Network](/conference/aaai-2025/aaai-2025-32838-alignment-free-rgb-t-salient-object-detection-a-large-scale-dataset-and-progressive-correlation-network)；[LER-YOLO: Reliability-Aware Expert Routing for Misaligned RGB-Infrared UAV Detection](/20250921-20260920/2605.20667v1)；[RA-SOD: Reliability-Aware RGB-T Salient Object Detection under Modality Degradation](/20250921-20260920/2609.12622v1)；[Graph-based Semantic Calibration Network for Unaligned UAV RGBT Image Semantic Segmentation and A Large-scale Benchmark](/20250921-20260920/2604.26893v2)；[RSONet: Region-guided Selective Optimization Network for RGB-T Salient Object Detection](/20250921-20260920/2603.12685v1)；[GAAT: Geometry-Aware Alignment Transformer for Multimodal UAV Perception](/20250921-20260920/2608.27971v2)；[SAMSOD: Rethinking SAM Optimization for RGB-T Salient Object Detection](/20250921-20260920/2510.03689v1)；[HyPSAM: Hybrid Prompt-driven Segment Anything Model for RGB-Thermal Salient Object Detection](/20250921-20260920/2509.18738v1)；[DiMSOD: A Diffusion-Based Framework for Multi-Modal Salient Object Detection](/conference/aaai-2025/aaai-2025-33096-dimsod-a-diffusion-based-framework-for-multi-modal-salient-object-detection)；[Bridging Severe Cross-Modal Misalignment: End-to-End Visible-Infrared Object Detection via Explicit Feature-Domain Affine Registration](/20250921-20260920/2608.10680v1)；[Uncertainty-Aware Multimodal Anti-UAV Detection via Evidential Fusion and Conflict-Discounted Belief Aggregation](/20250921-20260920/2608.29235v1)；[EGM-Det: Entropy-Guided Multimodal Adaptive Fusion for UAV RGB-IR Object Detection](/20250921-20260920/2608.11685v1)；[MSTF-Net: A UAV-Oriented Multi-Spectral Video Segmentation Method via Modality-Robust, Scale-Adaptive, and Consistent Fusion](/20250921-20260920/2607.15628v1)；[Progressive Pixel-Neighborhood Deformable Cross-Attention for Multispectral Object Detection](/20250921-20260920/2606.24092v1)；[SMR-Net: Semantic-Guided Mutually Reinforcing Network for Cross-Modal Image Fusion and Salient Object Detection](/conference/aaai-2025/aaai-2025-32933-smr-net-semantic-guided-mutually-reinforcing-network-for-cross-modal-image-fusion-and-salient-object-detection)；[DGSSM: Diffusion guided state-space models for multimodal salient object detection](/20250921-20260920/2604.17585v1)；[Small Target Detection Based on Mask-Enhanced Attention Fusion of Visible and Infrared Remote Sensing Images](/20250921-20260920/2603.06925v1)；[Bridging Multimodal Fusion and Expert Routing via Spectral Reliability Descriptors for Robust Object Detection](/20250921-20260920/2606.01173v2)；[S&#36;^3&#36;AM: A Single-Stream SAM with Reliability-Calibrated Frequency Adapter for Multi-modal Salient Object Detection](/20250921-20260920/2608.17475v1)；[Frequency-Guided Fusion For RGB-Thermal Semantic Segmentation](/20250921-20260920/2605.26273v1)；[FreDFT: Frequency Domain Fusion Transformer for Visible-Infrared Object Detection](/20250921-20260920/2511.10046v2)；[CRFT: Consistent-Recurrent Feature Flow Transformer for Cross-Modal Image Registration](/20250921-20260920/2604.05689v1)

## 子方向一：未配准RGB-T显著目标检测的显式空间对齐方法

该子方向直接处理可见光与热红外图像对之间的空间未配准问题，核心思路是在特征域或图像域显式估计空间变换或对应关系，以减轻视差、平台振动和视角偏移对融合的干扰。TPS-SCL提出薄板样条对齐模块与语义相关约束，面向真实未配准图像对，并采用双流MobileViT与Mamba扫描机制控制参数量。PCNet在显式对齐基础上建模模态内与模态间相关性，并配套构建大规模未配准RGB-T SOD数据集UVT20K，包含两万图像对、407个场景和1256个类别，标注包括显著掩码、涂鸦、边界和挑战属性。GSCNet面向未配准UAV RGBT语义分割，设计特征解耦与对齐模块，在共享子空间进行可变形对齐，并构建URTF基准，含超过25000图像对和61个语义类别。GAAT提出几何感知对齐Transformer，通过syncPATC学习块中心一致性并输出token置信度、查询中心和子token偏移等几何先验，再以MG-Sparse-MMA在可靠区域进行稀疏融合。CRFT则从跨模态图像配准角度提出一致循环特征流Transformer，采用由粗到细框架和迭代差异引导注意力进行流场细化。这些工作共同表明，显式对齐有助于抑制未配准带来的伪影传播，但多数方法在SOD任务上的直接验证仍有限，且部分基准面向分割或配准而非SOD。

依据：[Breaking Alignment Barriers: TPS-Driven Semantic Correlation Learning for Alignment-Free RGB-T Salient Object Detection](/20250921-20260920/2512.21856v1)；[Alignment-Free RGB-T Salient Object Detection: A Large-Scale Dataset and Progressive Correlation Network](/conference/aaai-2025/aaai-2025-32838-alignment-free-rgb-t-salient-object-detection-a-large-scale-dataset-and-progressive-correlation-network)；[Graph-based Semantic Calibration Network for Unaligned UAV RGBT Image Semantic Segmentation and A Large-scale Benchmark](/20250921-20260920/2604.26893v2)；[GAAT: Geometry-Aware Alignment Transformer for Multimodal UAV Perception](/20250921-20260920/2608.27971v2)；[CRFT: Consistent-Recurrent Feature Flow Transformer for Cross-Modal Image Registration](/20250921-20260920/2604.05689v1)

## 子方向二：不确定性感知与可靠性引导的跨模态融合

该子方向强调在融合前或融合中评估局部跨模态对应与模态证据的可靠性，避免不可靠对齐或退化模态误导检测头。LER-YOLO提出不确定性感知目标对齐模块，将可见光特征重采样至红外参考并估计空间可靠性图，再由可靠性引导稀疏专家混合融合模块自适应选择RGB主导、红外主导和交互融合专家。RA-SOD显式建模模态可靠性，引入可靠性条件表示、不确定性引导双流细化与像素级模态竞争机制，面向低照度、运动模糊、噪声和热红外对比度压缩等退化场景。EGM-Det从输入强度、局部熵和跨模态差异导出浅层熵先验，引导局部偏移对齐与空间通道门控融合，并以跨模态蒸馏正则化融合门。Bridging Multimodal Fusion and Expert Routing提出无参数七维频谱可靠性描述子，驱动频谱可靠性融合与可靠性条件专家路由。Uncertainty-Aware Multimodal Anti-UAV Detection通过折扣信念融合将模态间冲突转化为不确定性质量，并按较低不确定性选择边界框。这些方法显示可靠性信号可同时服务于对齐、融合与后融合条件计算，但部分证据来自检测或分类任务，直接迁移到SOD仍需验证。

依据：[LER-YOLO: Reliability-Aware Expert Routing for Misaligned RGB-Infrared UAV Detection](/20250921-20260920/2605.20667v1)；[RA-SOD: Reliability-Aware RGB-T Salient Object Detection under Modality Degradation](/20250921-20260920/2609.12622v1)；[EGM-Det: Entropy-Guided Multimodal Adaptive Fusion for UAV RGB-IR Object Detection](/20250921-20260920/2608.11685v1)；[Bridging Multimodal Fusion and Expert Routing via Spectral Reliability Descriptors for Robust Object Detection](/20250921-20260920/2606.01173v2)；[Uncertainty-Aware Multimodal Anti-UAV Detection via Evidential Fusion and Conflict-Discounted Belief Aggregation](/20250921-20260920/2608.29235v1)

## 子方向三：面向未配准与模态不一致的鲁棒融合架构

该子方向关注融合架构本身对未配准、模态不一致和背景干扰的鲁棒性，常结合可变形卷积、注意力、图推理、频域分解和状态空间模型。RSONet针对RGB与热红外显著区域不一致问题，设计区域引导阶段与显著性生成阶段，通过相似度分数进行选择性优化融合，并引入密集细节增强与互交互语义模块。MSTF-Net面向UAV多光谱视频分割，提出模态空间互补抑制增强模块和多尺度时序跨模态语义一致性模块，以应对模态融合困境和时序变化。PNAFusion提出渐进像素邻域可变形交叉注意力，将交互集中在对齐最相关的局部邻域，并通过自适应可变形对齐捕获非线性空间对应。SMR-Net以语义引导图像融合与SOD相互增强，利用位平面切片和可变形卷积提取不规则语义信息。DGSSM将多模态SOD建模为渐进去噪过程，结合扩散结构先验与多尺度状态空间编码。S3AM采用单流SAM与可靠性校准频率适配器，通过频率专家混合和双门校准控制辅助高频注入。这些架构在多个基准上报告了竞争力，但输入摘要中未提供统一的未配准SOD评测协议。

依据：[RSONet: Region-guided Selective Optimization Network for RGB-T Salient Object Detection](/20250921-20260920/2603.12685v1)；[MSTF-Net: A UAV-Oriented Multi-Spectral Video Segmentation Method via Modality-Robust, Scale-Adaptive, and Consistent Fusion](/20250921-20260920/2607.15628v1)；[Progressive Pixel-Neighborhood Deformable Cross-Attention for Multispectral Object Detection](/20250921-20260920/2606.24092v1)；[SMR-Net: Semantic-Guided Mutually Reinforcing Network for Cross-Modal Image Fusion and Salient Object Detection](/conference/aaai-2025/aaai-2025-32933-smr-net-semantic-guided-mutually-reinforcing-network-for-cross-modal-image-fusion-and-salient-object-detection)；[DGSSM: Diffusion guided state-space models for multimodal salient object detection](/20250921-20260920/2604.17585v1)；[S&#36;^3&#36;AM: A Single-Stream SAM with Reliability-Calibrated Frequency Adapter for Multi-modal Salient Object Detection](/20250921-20260920/2608.17475v1)

## 子方向四：基础模型、扩散模型与参数高效适配

该子方向探索如何将大规模预训练模型适配到RGB-T SOD，以缓解数据稀缺并提升边界与泛化能力。SAMSOD指出RGB-T SOD中SAM微调存在两模态收敛不平衡和高低激活梯度差异问题，提出单模态监督增强非主导模态学习，并用梯度去冲突降低冲突梯度影响，同时以解耦适配器分别掩码高激活和低激活神经元。HyPSAM提出混合提示驱动SAM，先用动态融合网络生成高质量初始显著图作为视觉提示，再以即插即用细化网络结合文本、掩码和框提示引导SAM细化。DiMSOD将多模态SOD视为条件掩码生成任务，在稳定扩散上仅微调新引入模块，统一处理RGB、RGB-D和RGB-T。DGSSM同样利用扩散结构先验，但以状态空间模型进行多尺度编码和迭代细化。S3AM则强调单流SAM避免双流冗余，并以可靠性校准频率适配器控制辅助频率注入。这些工作显示基础模型适配是活跃方向，但输入中多数方法未专门针对未配准UAV场景设计对齐机制。

依据：[SAMSOD: Rethinking SAM Optimization for RGB-T Salient Object Detection](/20250921-20260920/2510.03689v1)；[HyPSAM: Hybrid Prompt-driven Segment Anything Model for RGB-Thermal Salient Object Detection](/20250921-20260920/2509.18738v1)；[DiMSOD: A Diffusion-Based Framework for Multi-Modal Salient Object Detection](/conference/aaai-2025/aaai-2025-33096-dimsod-a-diffusion-based-framework-for-multi-modal-salient-object-detection)；[DGSSM: Diffusion guided state-space models for multimodal salient object detection](/20250921-20260920/2604.17585v1)；[S&#36;^3&#36;AM: A Single-Stream SAM with Reliability-Calibrated Frequency Adapter for Multi-modal Salient Object Detection](/20250921-20260920/2608.17475v1)

## 子方向五：频域、多尺度与轻量化融合

该子方向从频域分解、多尺度交互和轻量化设计角度提升跨模态融合效率与细节恢复。Frequency-Guided Fusion for RGB-Thermal Semantic Segmentation在早期阶段用高斯滤波将红外特征分解为低频和高频分量，并以置信门控残差与RGB融合，晚期阶段用跨模态注意力和多尺度深度可分离卷积。FreDFT提出多模态频域注意力与频域前馈层，并构建跨模态全局建模模块和局部特征增强模块。ESM-YOLO+提出掩码增强注意力融合模块，通过可学习空间掩码和空间注意力在像素级融合可见光与红外特征，以缓解跨模态未配准和尺度异质性。S3AM的可靠性校准频率适配器同样属于频域可靠性控制思路。这些方法在检测或分割基准上报告了参数与精度优势，但面向未配准RGB-T SOD的频域对齐证据仍不足。

依据：[Frequency-Guided Fusion For RGB-Thermal Semantic Segmentation](/20250921-20260920/2605.26273v1)；[FreDFT: Frequency Domain Fusion Transformer for Visible-Infrared Object Detection](/20250921-20260920/2511.10046v2)；[Small Target Detection Based on Mask-Enhanced Attention Fusion of Visible and Infrared Remote Sensing Images](/20250921-20260920/2603.06925v1)；[S&#36;^3&#36;AM: A Single-Stream SAM with Reliability-Calibrated Frequency Adapter for Multi-modal Salient Object Detection](/20250921-20260920/2608.17475v1)

## 评测基准与实验设置

输入论文涉及的评测资源可归纳为三类。第一类是未配准或弱配准RGB-T SOD基准：UVT20K包含20000图像对、407场景和1256类别，标注显著掩码、涂鸦、边界和挑战属性；PCNet在未配准、弱配准和已配准数据集上进行了实验。第二类是已配准RGB-T SOD常用基准：VT821、VT1000、VT5000和VT-IMAG被RA-SOD用于验证；HyPSAM在三个公开数据集上实验；SAMSOD在RGB-T SOD基准及涂鸦监督、RGB-D SOD和RGB-D轨道表面缺陷检测上验证泛化性。第三类是检测、分割或配准基准：MBU用于LER-YOLO，DroneVehicle、DVMA、FLIR、M3FD、VEDAI、LLVIP用于检测方法，MFNet和PST900用于RGB-T语义分割，MVSeg和CART用于多光谱视频分割，URTF用于未配准UAV RGBT语义分割。需要明确说明：输入摘要未提供统一的未配准SOD评测协议、跨论文共享的数据划分或统计显著性检验，因此无法据此判断各方法在未配准UAV RGB-T SOD上的严格优劣。

依据：[Alignment-Free RGB-T Salient Object Detection: A Large-Scale Dataset and Progressive Correlation Network](/conference/aaai-2025/aaai-2025-32838-alignment-free-rgb-t-salient-object-detection-a-large-scale-dataset-and-progressive-correlation-network)；[RA-SOD: Reliability-Aware RGB-T Salient Object Detection under Modality Degradation](/20250921-20260920/2609.12622v1)；[HyPSAM: Hybrid Prompt-driven Segment Anything Model for RGB-Thermal Salient Object Detection](/20250921-20260920/2509.18738v1)；[SAMSOD: Rethinking SAM Optimization for RGB-T Salient Object Detection](/20250921-20260920/2510.03689v1)；[LER-YOLO: Reliability-Aware Expert Routing for Misaligned RGB-Infrared UAV Detection](/20250921-20260920/2605.20667v1)；[Bridging Severe Cross-Modal Misalignment: End-to-End Visible-Infrared Object Detection via Explicit Feature-Domain Affine Registration](/20250921-20260920/2608.10680v1)；[Progressive Pixel-Neighborhood Deformable Cross-Attention for Multispectral Object Detection](/20250921-20260920/2606.24092v1)；[Frequency-Guided Fusion For RGB-Thermal Semantic Segmentation](/20250921-20260920/2605.26273v1)；[MSTF-Net: A UAV-Oriented Multi-Spectral Video Segmentation Method via Modality-Robust, Scale-Adaptive, and Consistent Fusion](/20250921-20260920/2607.15628v1)；[Graph-based Semantic Calibration Network for Unaligned UAV RGBT Image Semantic Segmentation and A Large-scale Benchmark](/20250921-20260920/2604.26893v2)

## 进展与局限

从输入论文看，该方向的主要进展包括：第一，研究重心从已配准数据向真实未配准图像对迁移，出现UVT20K、URTF、DVMA等面向未配准或严重错位的基准；第二，对齐机制从隐式特征适应扩展到显式薄板样条、可变形对齐、仿射配准和特征流学习；第三，可靠性建模从简单注意力扩展到空间可靠性图、证据不确定性、熵先验、频谱描述子和冲突折扣；第四，基础模型、扩散模型和状态空间模型被引入以提升边界与泛化。主要局限包括：未配准RGB-T SOD专用基准仍少于检测和分割基准；不确定性建模在部分工作中是启发式门控而非严格概率校准；部分方法在检测或分割任务上验证，直接迁移到SOD的证据不足；输入摘要中缺少统一评测协议、跨论文统计比较和失败案例分析；部分论文仅提供摘要级信息，未提供可复现实验细节。因此，当前证据支持“显式对齐加可靠性引导融合”是有前景的方向，但尚不足以断言某一具体方法在未配准UAV RGB-T SOD上具有普遍优势。

依据：[Alignment-Free RGB-T Salient Object Detection: A Large-Scale Dataset and Progressive Correlation Network](/conference/aaai-2025/aaai-2025-32838-alignment-free-rgb-t-salient-object-detection-a-large-scale-dataset-and-progressive-correlation-network)；[Graph-based Semantic Calibration Network for Unaligned UAV RGBT Image Semantic Segmentation and A Large-scale Benchmark](/20250921-20260920/2604.26893v2)；[Bridging Severe Cross-Modal Misalignment: End-to-End Visible-Infrared Object Detection via Explicit Feature-Domain Affine Registration](/20250921-20260920/2608.10680v1)；[Breaking Alignment Barriers: TPS-Driven Semantic Correlation Learning for Alignment-Free RGB-T Salient Object Detection](/20250921-20260920/2512.21856v1)；[LER-YOLO: Reliability-Aware Expert Routing for Misaligned RGB-Infrared UAV Detection](/20250921-20260920/2605.20667v1)；[RA-SOD: Reliability-Aware RGB-T Salient Object Detection under Modality Degradation](/20250921-20260920/2609.12622v1)；[Uncertainty-Aware Multimodal Anti-UAV Detection via Evidential Fusion and Conflict-Discounted Belief Aggregation](/20250921-20260920/2608.29235v1)；[Bridging Multimodal Fusion and Expert Routing via Spectral Reliability Descriptors for Robust Object Detection](/20250921-20260920/2606.01173v2)；[GAAT: Geometry-Aware Alignment Transformer for Multimodal UAV Perception](/20250921-20260920/2608.27971v2)；[HyPSAM: Hybrid Prompt-driven Segment Anything Model for RGB-Thermal Salient Object Detection](/20250921-20260920/2509.18738v1)；[SAMSOD: Rethinking SAM Optimization for RGB-T Salient Object Detection](/20250921-20260920/2510.03689v1)

## 建议阅读顺序

以下为建议学习顺序，不是公布时间排序。

1. [Alignment-Free RGB-T Salient Object Detection: A Large-Scale Dataset and Progressive Correlation Network](/conference/aaai-2025/aaai-2025-32838-alignment-free-rgb-t-salient-object-detection-a-large-scale-dataset-and-progressive-correlation-network) · 入门
   - 阅读理由：提供大规模未配准RGB-T SOD数据集UVT20K和渐进相关网络，是理解该任务定义、数据挑战和基础方法的入口。
   - 公布时间：2025（年精度）
   - AAAI-2025-Accepted · 2025（年精度）：[原文](https://ojs.aaai.org/index.php/AAAI/article/view/32838) / [PDF](https://ojs.aaai.org/index.php/AAAI/article/download/32838/34993)

2. [Breaking Alignment Barriers: TPS-Driven Semantic Correlation Learning for Alignment-Free RGB-T Salient Object Detection](/20250921-20260920/2512.21856v1) · 入门
   - 阅读理由：面向真实未配准图像对提出薄板样条驱动语义相关学习，直接对应主题中的未配准对齐问题。
   - 公布时间：2025-12-26（日精度）
   - AAAI-2026-Accepted · 2026（年精度）：[原文](https://ojs.aaai.org/index.php/AAAI/article/view/42492) / [PDF](https://ojs.aaai.org/index.php/AAAI/article/download/42492/46453)
   - arxiv · 2025-12-26（日精度）：[原文](https://arxiv.org/pdf/2512.21856v1) / [PDF](https://arxiv.org/pdf/2512.21856v1)

3. [RA-SOD: Reliability-Aware RGB-T Salient Object Detection under Modality Degradation](/20250921-20260920/2609.12622v1) · 入门
   - 阅读理由：系统讨论模态退化下的可靠性建模与不确定性引导融合，是理解可靠性感知SOD的核心工作。
   - 公布时间：2026-09-11（日精度）
   - arxiv · 2026-09-11（日精度）：[原文](https://arxiv.org/pdf/2609.12622v1)
   - ECCV-2026-Accepted-Program · 2026（年精度）：[原文](https://eccv.ecva.net/virtual/2026/poster/3933) / [PDF](https://media.eventhosts.cc/Conferences/ECCV2026/pdfs/3743.pdf)

4. [LER-YOLO: Reliability-Aware Expert Routing for Misaligned RGB-Infrared UAV Detection](/20250921-20260920/2605.20667v1) · 入门
   - 阅读理由：提出不确定性感知目标对齐与可靠性引导稀疏专家路由，直接连接未配准与不确定性融合两个主题。
   - 公布时间：2026-05-20（日精度）
   - arxiv · 2026-05-20（日精度）：[原文](https://arxiv.org/pdf/2605.20667v1) / [PDF](https://arxiv.org/pdf/2605.20667v1)

5. [Graph-based Semantic Calibration Network for Unaligned UAV RGBT Image Semantic Segmentation and A Large-scale Benchmark](/20250921-20260920/2604.26893v2) · 进阶
   - 阅读理由：面向未配准UAV RGBT语义分割，提供特征解耦对齐与图语义校准思路，并构建URTF基准。
   - 公布时间：2026-04-29（日精度）
   - arxiv · 2026-04-29（日精度）：[原文](https://arxiv.org/pdf/2604.26893v2) / [PDF](https://arxiv.org/pdf/2604.26893v2)

6. [GAAT: Geometry-Aware Alignment Transformer for Multimodal UAV Perception](/20250921-20260920/2608.27971v2) · 进阶
   - 阅读理由：从几何感知预训练角度处理局部对应可靠性，适合深入理解对齐优先的跨模态交互。
   - 公布时间：2026-08-28（日精度）
   - arxiv · 2026-08-28（日精度）：[原文](https://arxiv.org/pdf/2608.27971v1)
   - arxiv · 2026-08-28（日精度）：[原文](https://arxiv.org/pdf/2608.27971v2) / [PDF](https://arxiv.org/pdf/2608.27971v2)

7. [Progressive Pixel-Neighborhood Deformable Cross-Attention for Multispectral Object Detection](/20250921-20260920/2606.24092v1) · 进阶
   - 阅读理由：提出渐进像素邻域可变形交叉注意力，适合理解局部可变形对齐与效率权衡。
   - 公布时间：2026-06-23（日精度）
   - arxiv · 2026-06-23（日精度）：[原文](https://arxiv.org/pdf/2606.24092v1) / [PDF](https://arxiv.org/pdf/2606.24092v1)

8. [EGM-Det: Entropy-Guided Multimodal Adaptive Fusion for UAV RGB-IR Object Detection](/20250921-20260920/2608.11685v1) · 进阶
   - 阅读理由：以熵引导多模态自适应融合，展示空间变化可靠性在检测融合中的实现方式。
   - 公布时间：2026-08-12（日精度）
   - arxiv · 2026-08-12（日精度）：[原文](https://arxiv.org/pdf/2608.11685v1)

9. [Bridging Multimodal Fusion and Expert Routing via Spectral Reliability Descriptors for Robust Object Detection](/20250921-20260920/2606.01173v2) · 进阶
   - 阅读理由：提出频谱可靠性描述子并驱动融合与专家路由，适合理解可靠性信号的后融合复用。
   - 公布时间：2026-05-31（日精度）
   - arxiv · 2026-05-31（日精度）：[原文](https://arxiv.org/pdf/2606.01173v2) / [PDF](https://arxiv.org/pdf/2606.01173v2)

10. [Uncertainty-Aware Multimodal Anti-UAV Detection via Evidential Fusion and Conflict-Discounted Belief Aggregation](/20250921-20260920/2608.29235v1) · 进阶
   - 阅读理由：将证据深度学习与折扣信念融合用于RGB-T感知，适合理解冲突建模与不确定性校准。
   - 公布时间：2026-08-29（日精度）
   - arxiv · 2026-08-29（日精度）：[原文](https://arxiv.org/pdf/2608.29235v1)

11. [CRFT: Consistent-Recurrent Feature Flow Transformer for Cross-Modal Image Registration](/20250921-20260920/2604.05689v1) · 专题
   - 阅读理由：从跨模态图像配准角度提供特征流学习与迭代细化框架，可作为对齐模块的专题参考。
   - 公布时间：2026-04-07（日精度）
   - arxiv · 2026-04-07（日精度）：[原文](https://arxiv.org/pdf/2604.05689v1) / [PDF](https://arxiv.org/pdf/2604.05689v1)

12. [Bridging Severe Cross-Modal Misalignment: End-to-End Visible-Infrared Object Detection via Explicit Feature-Domain Affine Registration](/20250921-20260920/2608.10680v1) · 专题
   - 阅读理由：针对严重跨模态错位提出显式特征域仿射配准与对齐质量一致性门控，适合专题研究严重未配准场景。
   - 公布时间：2026-08-11（日精度）
   - arxiv · 2026-08-11（日精度）：[原文](https://arxiv.org/pdf/2608.10680v1)

13. [HyPSAM: Hybrid Prompt-driven Segment Anything Model for RGB-Thermal Salient Object Detection](/20250921-20260920/2509.18738v1) · 专题
   - 阅读理由：展示如何用混合提示驱动SAM进行RGB-T SOD，适合专题研究基础模型适配与提示工程。
   - 公布时间：2025-09-23（日精度）
   - arxiv · 2025-09-23（日精度）：[原文](https://arxiv.org/pdf/2509.18738v1) / [PDF](https://arxiv.org/pdf/2509.18738v1)

14. [SAMSOD: Rethinking SAM Optimization for RGB-T Salient Object Detection](/20250921-20260920/2510.03689v1) · 专题
   - 阅读理由：讨论SAM微调中的模态收敛不平衡与梯度冲突，适合专题研究基础模型优化稳定性。
   - 公布时间：2025-10-04（日精度）
   - arxiv · 2025-10-04（日精度）：[原文](https://arxiv.org/pdf/2510.03689v1) / [PDF](https://arxiv.org/pdf/2510.03689v1)

15. [DiMSOD: A Diffusion-Based Framework for Multi-Modal Salient Object Detection](/conference/aaai-2025/aaai-2025-33096-dimsod-a-diffusion-based-framework-for-multi-modal-salient-object-detection) · 专题
   - 阅读理由：将多模态SOD统一为扩散条件掩码生成任务，适合专题研究扩散模型在SOD中的集成。
   - 公布时间：2025（年精度）
   - AAAI-2025-Accepted · 2025（年精度）：[原文](https://ojs.aaai.org/index.php/AAAI/article/view/33096) / [PDF](https://ojs.aaai.org/index.php/AAAI/article/download/33096/35251)

16. [DGSSM: Diffusion guided state-space models for multimodal salient object detection](/20250921-20260920/2604.17585v1) · 专题
   - 阅读理由：结合扩散结构先验与状态空间模型进行多模态SOD，适合专题研究去噪与状态空间融合。
   - 公布时间：2026-04-19（日精度）
   - arxiv · 2026-04-19（日精度）：[原文](https://arxiv.org/pdf/2604.17585v1) / [PDF](https://arxiv.org/pdf/2604.17585v1)

17. [S&#36;^3&#36;AM: A Single-Stream SAM with Reliability-Calibrated Frequency Adapter for Multi-modal Salient Object Detection](/20250921-20260920/2608.17475v1) · 专题
   - 阅读理由：提出单流SAM与可靠性校准频率适配器，适合专题研究参数高效适配与频域可靠性控制。
   - 公布时间：2026-08-18（日精度）
   - arxiv · 2026-08-18（日精度）：[原文](https://arxiv.org/pdf/2608.17475v1)

18. [RSONet: Region-guided Selective Optimization Network for RGB-T Salient Object Detection](/20250921-20260920/2603.12685v1) · 专题
   - 阅读理由：针对RGB与热红外显著区域不一致提出区域引导选择性优化，适合专题研究模态不一致融合。
   - 公布时间：2026-03-13（日精度）
   - arxiv · 2026-03-13（日精度）：[原文](https://arxiv.org/pdf/2603.12685v1) / [PDF](https://arxiv.org/pdf/2603.12685v1)

19. [MSTF-Net: A UAV-Oriented Multi-Spectral Video Segmentation Method via Modality-Robust, Scale-Adaptive, and Consistent Fusion](/20250921-20260920/2607.15628v1) · 专题
   - 阅读理由：面向UAV多光谱视频分割处理模态融合困境与时序变化，适合专题研究视频与时序一致性。
   - 公布时间：2026-07-17（日精度）
   - arxiv · 2026-07-17（日精度）：[原文](https://arxiv.org/pdf/2607.15628v1) / [PDF](https://arxiv.org/pdf/2607.15628v1)

20. [SMR-Net: Semantic-Guided Mutually Reinforcing Network for Cross-Modal Image Fusion and Salient Object Detection](/conference/aaai-2025/aaai-2025-32933-smr-net-semantic-guided-mutually-reinforcing-network-for-cross-modal-image-fusion-and-salient-object-detection) · 专题
   - 阅读理由：以语义引导实现图像融合与SOD相互增强，适合专题研究多任务协同与轻量化设计。
   - 公布时间：2025（年精度）
   - AAAI-2025-Accepted · 2025（年精度）：[原文](https://ojs.aaai.org/index.php/AAAI/article/view/32933) / [PDF](https://ojs.aaai.org/index.php/AAAI/article/download/32933/35088)

任务：研究方向大礼包

固定窗口：arXiv &#91;2025-09-21, 2026-09-21&#41;；会议 &#91;2024-09-21, 2026-09-21&#41;（UTC，结束日不含）

本次候选评审上限 300，最终名单上限 100；本轮内容预算 10。

覆盖限制：仅检索配置范围内已有库存与预算内候选；向量/会议Top-k召回并非全库遍历，不保证找全相关论文。未核实录用、日期边界和缺失库存不能当作已覆盖。

缺失库存：eccv 2025、emnlp 2026、ijcai 2026、neurips 2026。

研究需求：面向UAV未配准RGB-T显著目标检测的不确定性感知跨模态对齐方法

# uav-rgbt-sod

以下为本次固定最终名单，按相关性评分降序；不代表全部相关论文。

1. [Breaking Alignment Barriers: TPS-Driven Semantic Correlation Learning for Alignment-Free RGB-T Salient Object Detection](https://arxiv.org/abs/2512.21856v1) · 分数 9
2. [Alignment-Free RGB-T Salient Object Detection: A Large-Scale Dataset and Progressive Correlation Network](https://ojs.aaai.org/index.php/AAAI/article/view/32838) · 分数 9
3. [LER-YOLO: Reliability-Aware Expert Routing for Misaligned RGB-Infrared UAV Detection](https://arxiv.org/abs/2605.20667v1) · 分数 9
4. [RA-SOD: Reliability-Aware RGB-T Salient Object Detection under Modality Degradation](https://arxiv.org/abs/2609.12622v1) · 分数 7
5. [Graph-based Semantic Calibration Network for Unaligned UAV RGBT Image Semantic Segmentation and A Large-scale Benchmark](https://arxiv.org/abs/2604.26893v2) · 分数 7
6. [RSONet: Region-guided Selective Optimization Network for RGB-T Salient Object Detection](https://arxiv.org/abs/2603.12685v1) · 分数 7
7. [GAAT: Geometry-Aware Alignment Transformer for Multimodal UAV Perception](https://arxiv.org/abs/2608.27971v2) · 分数 7
8. [SAMSOD: Rethinking SAM Optimization for RGB-T Salient Object Detection](https://arxiv.org/abs/2510.03689v1) · 分数 6
9. [HyPSAM: Hybrid Prompt-driven Segment Anything Model for RGB-Thermal Salient Object Detection](https://arxiv.org/abs/2509.18738v1) · 分数 6
10. [DiMSOD: A Diffusion-Based Framework for Multi-Modal Salient Object Detection](https://ojs.aaai.org/index.php/AAAI/article/view/33096) · 分数 6
11. [Bridging Severe Cross-Modal Misalignment: End-to-End Visible-Infrared Object Detection via Explicit Feature-Domain Affine Registration](https://arxiv.org/abs/2608.10680v1) · 分数 6
12. [Uncertainty-Aware Multimodal Anti-UAV Detection via Evidential Fusion and Conflict-Discounted Belief Aggregation](https://arxiv.org/abs/2608.29235v1) · 分数 6
13. [EGM-Det: Entropy-Guided Multimodal Adaptive Fusion for UAV RGB-IR Object Detection](https://arxiv.org/abs/2608.11685v1) · 分数 6
14. [MSTF-Net: A UAV-Oriented Multi-Spectral Video Segmentation Method via Modality-Robust, Scale-Adaptive, and Consistent Fusion](https://arxiv.org/abs/2607.15628v1) · 分数 6
15. [Progressive Pixel-Neighborhood Deformable Cross-Attention for Multispectral Object Detection](https://arxiv.org/abs/2606.24092v1) · 分数 6
16. [SMR-Net: Semantic-Guided Mutually Reinforcing Network for Cross-Modal Image Fusion and Salient Object Detection](https://ojs.aaai.org/index.php/AAAI/article/view/32933) · 分数 6
17. [DGSSM: Diffusion guided state-space models for multimodal salient object detection](https://arxiv.org/abs/2604.17585v1) · 分数 6
18. [Small Target Detection Based on Mask-Enhanced Attention Fusion of Visible and Infrared Remote Sensing Images](https://arxiv.org/abs/2603.06925v1) · 分数 6
19. [Bridging Multimodal Fusion and Expert Routing via Spectral Reliability Descriptors for Robust Object Detection](https://arxiv.org/abs/2606.01173v2) · 分数 6
20. [S&#36;^3&#36;AM: A Single-Stream SAM with Reliability-Calibrated Frequency Adapter for Multi-modal Salient Object Detection](https://arxiv.org/abs/2608.17475v1) · 分数 6
21. [Frequency-Guided Fusion For RGB-Thermal Semantic Segmentation](https://arxiv.org/abs/2605.26273v1) · 分数 6
22. [FreDFT: Frequency Domain Fusion Transformer for Visible-Infrared Object Detection](https://arxiv.org/abs/2511.10046v2) · 分数 6
23. [CRFT: Consistent-Recurrent Feature Flow Transformer for Cross-Modal Image Registration](https://arxiv.org/abs/2604.05689v1) · 分数 6

[按公布时间查看](#/starter-pack/20260921-e959361397be/dates)

阅读内容：已完成 2，待补充 21。

部分阅读内容生成失败；固定名单及导出保留，可继续生成缺失内容。
