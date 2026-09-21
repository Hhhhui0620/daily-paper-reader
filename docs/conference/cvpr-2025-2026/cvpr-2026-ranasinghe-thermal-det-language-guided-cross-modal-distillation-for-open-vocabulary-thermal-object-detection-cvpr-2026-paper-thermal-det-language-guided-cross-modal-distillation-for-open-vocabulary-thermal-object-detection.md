---
title: "Thermal-Det: Language-Guided Cross-Modal Distillation for Open-Vocabulary Thermal Object Detection"
title_zh: Thermal-Det：面向开放词汇热红外目标检测的语言引导跨模态蒸馏
authors: "Ranasinghe, Yasiru, Schenck, Elim, Yellin, Florence, Hu, Shuowen, Funk, Christopher, Patel, Vishal M."
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Ranasinghe_Thermal-Det_Language-Guided_Cross-Modal_Distillation_for_Open-Vocabulary_Thermal_Object_Detection_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 5.0
evidence: 跨模态蒸馏将可见光语义迁移到热红外图像
tldr: 现有开放词汇检测器主要面向可见光图像，难以泛化到纹理弱、发射率变化大的热红外图像。本文提出Thermal-Det，首个由大语言模型监督的热红外开放词汇检测器，通过构建百万级热域合成数据并联合优化检测、描述与跨模态蒸馏目标。实验表明其显著提升了热红外开放词汇检测性能。该工作为可见光与热红外跨模态特征迁移提供了有效范式。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-ranasinghe-thermal-det-language-guided-cross-modal-distillation-for-open-vocabulary-thermal-object-detection-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 2571, \"height\": 794}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-ranasinghe-thermal-det-language-guided-cross-modal-distillation-for-open-vocabulary-thermal-object-detection-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 2, \"index\": 2, \"width\": 2140, \"height\": 915}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-ranasinghe-thermal-det-language-guided-cross-modal-distillation-for-open-vocabulary-thermal-object-detection-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 7, \"index\": 3, \"width\": 3600, \"height\": 3600}]"
motivation: 开放词汇检测器多面向可见光，难以泛化到纹理弱、发射率变化大的热红外图像。
method: 提出大语言模型监督的热红外检测器，构建热域合成数据并联合优化检测、描述与跨模态蒸馏。
result: 实验表明方法显著提升了热红外开放词汇检测性能。
conclusion: 为可见光与热红外跨模态特征迁移提供了有效范式。
---

## Abstract
Existing open-vocabulary detectors focus on RGB images and fail to generalize to thermal imagery, where low texture and emissivity variations challenge RGB-based semantics. We present Thermal-Det, the first large language model (LLM) supervised open-vocabulary detector tailored for thermal images. To enable large-scale training, we construct a synthetic dataset by converting GroundingCap-1M into the thermal domain and filtering captions to remove RGB-specific terms, yielding over one million thermally aligned samples with bounding boxes, grounding texts, and detailed captions. Thermal-Det jointly optimizes detection, captioning, and cross-modal distillation objectives. A frozen RGB teacher provides geometric and semantic pseudo-supervision for paired but unlabeled RGB-thermal data, transferring open-vocabulary knowledge without manual annotation. The model further employs a Thermal-Text Alignment Head for text calibration and a Modality-Fused Cross-Attention module for dual-modality reasoning. Unlike prior domain-adaptation methods, the detector is fully fine-tuned to internalize thermal contrast patterns while preserving language alignment. Experiments on public benchmarks show consistent 2-4% AP gains over existing open-vocabulary detectors, establishing a strong foundation for scalable, language-driven thermal perception.

---

## 论文详细总结（自动生成）

# Thermal-Det 论文中文总结

## 1. 核心问题与整体含义
- **研究动机**：热红外成像在自动驾驶、监控、搜救等安全关键场景中很重要，但热红外目标检测长期受限于标注数据稀缺、类别少、基准小，现有模型多只能识别行人、车辆等少数闭集类别。
- **核心问题**：开放词汇目标检测在 RGB 图像上已较成熟，但直接迁移到热红外图像时，因低纹理、低对比度、发射率变化和模态差异，性能显著下降；现有热域适配方法多依赖参数高效微调或适配器，仍依赖有限热标注，难以泛化到未见类别。
- **整体含义**：论文提出 **Thermal-Det**，声称是首个由大语言模型监督、面向热红外的开放词汇检测器，目标是在**不使用热红外人工标注**的情况下，实现零样本热红外开放词汇检测，并为可见光到热红外的跨模态知识迁移提供范式。

## 2. 方法论
- **核心思想**：联合利用三类信号：① 大规模合成热红外数据提供检测与语言监督；② RGB 教师到热红外学生的跨模态蒸馏提供几何与语义伪监督；③ 热文本对齐与 LLM 适配增强热域语言 grounding。
- **合成热红外数据集构建**：
  - 以 GroundingCap-1M 为基础，将 RGB 图像经 F-ViTA 转换为合成热红外图像，保留原始边界框和 grounding 文本。
  - 对原 captions 进行轻量文本过滤，移除颜色、光照等 RGB 特有描述词，得到超过 100 万热对齐样本，继承约 13k 类别。
- **基础检测框架**：
  - 采用开放词汇检测公式，冻结 CLIP 文本编码器，使用 transformer 解码器预测框与文本相似度。
  - 检测损失为分类/对齐损失加框回归损失：`Ldet = Lcls + Lbox`。
- **LLM 监督与热适配**：
  - 将检测器特征投影到 LLM token 空间，在 LLM 的 FFN 中插入 LoRA 式残差 MLP 作为 **Thermal Adapters**，学习热域语义。
  - 提出 **Modality-Fused Cross-Attention, MFCA**，让文本查询同时关注热红外特征和 RGB 教师特征，通过门控 α、β 融合；推理时无 RGB 输入，β=0，退化为热红外单模态注意力。
- **描述生成损失**：
  - 场景级 caption 损失 `Lcap-scene` 促进全局热场景理解。
  - 物体级 caption 损失 `Lcap-object` 促进局部区域与语言短语对齐。
  - 总 caption 损失：`Lcap = Lcap-scene + Lcap-object`。
- **跨模态蒸馏**：
  - 使用空间对齐的配对 RGB–热红外数据，冻结 RGB 教师生成伪标签，热红外学生模仿教师。
  - 三类蒸馏损失：
    - `LKD-box`：基于 GIoU 的空间框蒸馏。
    - `LKD-sem`：基于余弦 InfoNCE 的语义特征蒸馏。
    - `LKD-conf`：基于 KL 散度的类别概率/置信度蒸馏。
  - 总蒸馏损失：`LKD = LKD-box + LKD-sem
