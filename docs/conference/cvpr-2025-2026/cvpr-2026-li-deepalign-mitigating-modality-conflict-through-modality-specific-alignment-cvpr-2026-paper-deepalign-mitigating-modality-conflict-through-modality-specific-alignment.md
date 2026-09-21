---
title: "DeepAlign: Mitigating Modality Conflict through Modality-Specific Alignment"
title_zh: DeepAlign：通过模态特定对齐缓解模态冲突
authors: "Li, Shuo, Miao, Bingchen, Bu, Wendong, Li, Juncheng, Zhang, Hanwang, Wu, Fei"
date: 2026
publication_date: 2026
publication_date_precision: year
publication_date_source: conference year only; exact release date unverified
publication_date_kind: unknown
pdf: "https://openaccess.thecvf.com/content/CVPR2026/papers/Li_DeepAlign_Mitigating_Modality_Conflict_through_Modality-Specific_Alignment_CVPR_2026_paper.pdf"
tags: ["query:uav-rgbt-sod"]
score: 4.0
evidence: 缓解多模态大模型中的视觉-文本模态错位
tldr: 该文针对多模态大模型中视觉与文本之间模态错位的问题展开研究，指出其源于模态特定表示错位与模态细节流失。作者提出DeepAlign对齐框架，通过表示干预与结构引导知识蒸馏防止模态特定信息的错位与耗散。实验表明该方法能显著缓解模态冲突并提升多模态理解性能。其对齐思想可迁移，但应用场景为MLLM而非UAV RGB-T检测。
source: CVPR-2026-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-deepalign-mitigating-modality-conflict-through-modality-specific-alignment-cvpr-2026-paper/fig-001.webp\", \"caption\": \"\", \"page\": 1, \"index\": 1, \"width\": 682, \"height\": 682}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-deepalign-mitigating-modality-conflict-through-modality-specific-alignment-cvpr-2026-paper/fig-002.webp\", \"caption\": \"\", \"page\": 2, \"index\": 2, \"width\": 1423, \"height\": 451}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-deepalign-mitigating-modality-conflict-through-modality-specific-alignment-cvpr-2026-paper/fig-003.webp\", \"caption\": \"\", \"page\": 4, \"index\": 3, \"width\": 435, \"height\": 434}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-deepalign-mitigating-modality-conflict-through-modality-specific-alignment-cvpr-2026-paper/fig-004.webp\", \"caption\": \"\", \"page\": 4, \"index\": 4, \"width\": 1441, \"height\": 989}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-deepalign-mitigating-modality-conflict-through-modality-specific-alignment-cvpr-2026-paper/fig-005.webp\", \"caption\": \"\", \"page\": 4, \"index\": 5, \"width\": 1441, \"height\": 988}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-deepalign-mitigating-modality-conflict-through-modality-specific-alignment-cvpr-2026-paper/fig-006.webp\", \"caption\": \"\", \"page\": 7, \"index\": 6, \"width\": 1458, \"height\": 1011}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-deepalign-mitigating-modality-conflict-through-modality-specific-alignment-cvpr-2026-paper/fig-007.webp\", \"caption\": \"\", \"page\": 7, \"index\": 7, \"width\": 1160, \"height\": 1010}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-deepalign-mitigating-modality-conflict-through-modality-specific-alignment-cvpr-2026-paper/fig-008.webp\", \"caption\": \"\", \"page\": 7, \"index\": 8, \"width\": 1441, \"height\": 989}, {\"url\": \"assets/figures/cvpr-2026-accepted/cvpr-2026-li-deepalign-mitigating-modality-conflict-through-modality-specific-alignment-cvpr-2026-paper/fig-009.webp\", \"caption\": \"\", \"page\": 7, \"index\": 9, \"width\": 1441, \"height\": 988}]"
motivation: 多模态大模型中视觉与文本的模态错位与模态细节流失制约了多模态理解能力。
method: 提出DeepAlign框架，采用表示干预与结构引导知识蒸馏防止模态特定信息错位。
result: 实验证明可显著缓解模态冲突并提升多模态任务表现。
conclusion: 模态特定对齐有助于缓解错位，但与UAV RGB-T显著检测任务差异较大。
---

## Abstract
Multimodal Large Language Models (MLLMs) have demonstrated promising advancements in augmenting the capabilities of LLMs to comprehend visual input. However, modality misalignment between vision and text remains a key challenge in MLLM, which can be attributed to two aspects: misalignment of modality-specific representations and depletion of modality-specific details. To address the issue of modality misalignment, we propose DeepAlign, a novel multimodal alignment framework to mitigate modality conflict, which employs representation intervention and structure-induced knowledge distillation to prevent the misalignment and depletion of modality-specific information. Extensive experiments demonstrate that DeepAlign significantly mitigates modality conflicts, leading to substantial performance improvements compared to backbone models across multiple vision-language tasks. It also stimulates some emergent abilities in MLLMs, such as multimodal in-context learning on interleaved text-image sequences.

---

## 论文详细总结（自动生成）

# DeepAlign 论文中文总结

## 1. 核心问题与研究动机

- **研究背景**：多模态大语言模型（MLLMs）通常采用“桥接”范式，即预训练视觉编码器 + 预训练 LLM + 轻量连接模块，将视觉特征对齐到文本模态。然而，这种对齐方式是否足以让原本处理语言任务的 LLM 真正理解视觉信息，仍存疑问。
- **核心问题**：视觉与文本之间存在**模态冲突（modality conflict）**，作者将其归因于两个层面：
  - **模态特定表示的错位（misalignment of modality-specific representations）**：当前视觉-语言预训练主要对齐模态共享语义（如生成简短标题），导致颜色、纹理等模态特定信息未被对齐。例如“灰色泰迪熊、蓝色围巾”中的颜色属性可能错位。
  - **模态特定细节的流失（depletion of modality-specific details）**：自回归训练主要依赖文本侧监督，视觉仅作辅助，导致 MLLM 对视觉的理解停留在模态共享层面，难以捕捉难以用文字描述的视觉细节（如岩石纹理、天空光照）。
- **探索性实验证据**：
  - **语言任务**：LLaVA-v1.5-7B 相比对应 LLM（Vicuna-7B）在 MMLU 上平均下降约 10 分；文本 token 预测困惑度显著升高。
  - **视觉辅助语言任务**：在 MNER、MMT、MRE 三个任务上，加入视觉输入反而比纯文本输入表现更差。
  - **感知型 VQA**：将原图替换为密集描述让纯文本 LLM 作答，性能并未显著下降，说明 MLLM 的视觉理解仍停留在模态共享层面。
- **整体含义**：论文揭示并量化了 MLLM 中的模态冲突现象，提出通过“模态特定对齐”来同时解决表示错位与细节流失两大问题。

## 2. 方法论：DeepAlign 框架

DeepAlign 是一个**多模态后训练框架**，从双层面缓解模态冲突，核心由两部分组成：

### 2.1 表示干预（Representation Intervention）

**核心思想**：识别并隔离视觉与文本表示中的模态特定成分，量化模态偏移方向，并通过可训练模块将视觉表示对齐到 LLM 的文本嵌入空间。

**三个关键阶段**：

1. **模态特定成分的提取与解耦**
   - 从 MLLM 最后一层最后一个 token 的隐藏状态中提取池化后的视觉与文本表示 $(h_t, h_v) \in \mathbb{R}^D$。
   - 训练一个**模态分类器** $f$，判断表示来自视觉还是文本模态，输出预测分数 $y = f(h)$。
   - 借鉴 **Grad-CAM** 思想，用预测分数对输入的梯度 $w_{cls} = \nabla_h y_k$ 作为通道级注意力权重，提取模态判别性（模态特定）特征：
     - $h_{mod} = s \, w_{cls} \odot h$
   - 通过自适应非负参数 $s$ 调制能量，使 $\epsilon(h_{mod}) = \epsilon(h)$，即保持能量不变：
     - $s = \sqrt{\frac{\sum_{d=1}^{D} h_d^2}{\sum_{d=1}^{D} (w_{cls,d} h_d)^2}}$

2. **模态偏移方向的量化**
   - **实例级**偏移方向：$d_{instance} = h_{mod}^t - h_{mod}^v$
   - **全局级**偏移方向：$d_{global} = \text{Mean}(\{d_{instance}^i\}_{i=1}^m)$

3. **通过模态偏移模块对齐**
   - 在若干中间 Transformer 层插入**适配器层**（即模态偏移模块 $\text{SHF}(\cdot)$，约 200M 参数），将视觉表示变换为对齐后的表示 $h'_v = \text{SHF}(h_v)$。
   - **全局级监督**：$L_{global} = \alpha(1 - \cos\text{sim}(h'_v[-1] - h_v[-1], d_{global}))$
   - **实例级监督**：$L_{instance} = \beta(1 - \cos\text{sim}(h'_v[-1] - h_v[-1], d_{instance}))$
   - **互信息正则项**：$L_{MI} = -\gamma(\text{MI}(h'_v, h_t) - \text{MI}(h_v, h_t))$，确保偏移后表示在靠近文本模态的同时保留关键信息。

### 2.2 结构引导蒸馏（Structure-Induced Distillation）

**核心思想**：利用纯视觉自监督模型 DINOv2 的结构知识作为视觉侧监督，弥补 MLLM 视觉语义的不足。

- **动机观察**：线性探测显示，MLLM 内部视觉隐藏状态在 ImageNet 分类上的峰值性能显著低于 DINOv2，说明 MLLM 更偏向模态共享语义，缺乏语义丰富的视觉特定表示。
- **方法**：将 DINOv2 编码器输出 $g = \text{Enc}(I) \in \mathbb{R}^{n \times D}$ 与 MLLM 隐藏状态 $\tilde{h} = \text{MLLM}(I) \in \mathbb{R}^{n \times D'}$ 的**patch 级相似度矩阵**进行对齐，用 MSE 损失约束：
  - $L_{visual} = \mu \cdot \frac{1}{n^2} \sum_{i=1}^{n} \sum_{j=1}^{n} \| \text{Sim}(\tilde{h}_i, \tilde{h}_j) - \text{Sim}(g_i, g_j) \|^2$
- 这使得 MLLM 训练不再局限于文本侧监督，视觉模态也获得自身监督。

### 2.3 最终训练损失

- 结合文本自回归损失与上述各损失：
  - $L = L_{AR} + L_{global} + L_{instance} + L_{MI} + L_{visual}$
- 训练时**仅适配器层（模态偏移模块，约 200M 参数）可训练**，骨干模型冻结，峰值学习率为 $3 \times 10^{-5}$。

## 3. 实验设计

### 3.1 数据集与 Benchmark

- **后训练数据**：来自 CC3M 与 COCO Caption 的高质量子集，且全部来自骨干 MLLM 原始预训练与指令微调数据集。
- **零样本视觉-语言理解**：
  - MLLM Benchmark：MMBench、MMStar、MMMU、HallusionBench、OCRBench、MMVet
  - VQA Benchmark：ScienceQA、TextVQA、RealWorldQA、MTVQA
- **细粒度感知**：BLINK 基准（空间关系、局部细节、视觉对应、相似性、计数、深度共 6 个子任务）
- **视觉辅助语言任务**：MNER、MMT、MRE
- **文本困惑度**：Wikipedia 随机采样 1000 个文本片段
- **涌现能力**：
  - 幻觉缓解：HallusionBench
  - 多模态上下文学习：OKVQA、VQAv2（4-shot / 8-shot / 16-shot）
  - 交错图文序列的演示指令跟随：DEMON 基准（MMD、VST、VRI、MMC、KGQA、TRQA、MMR）
- **模态协同分析**：NoCaps（视觉-语言）与 MMLU（纯 NLP）

### 3.2 对比方法

- 闭源模型：GPT-4.5、Gemini-1.5-Pro、GPT-4o
- 骨干模型：LLaVA-v1.5-7B、Qwen2.5-VL-7B、InternVL3-8B
- 后训练对齐基线：RLHF、HADPO、DataTailor、POVID、SIMA、VISTA

## 4. 资源与算力

- 论文正文与附录摘要中**未明确提及具体的 GPU 型号、数量或训练时长**。
- 仅给出了以下训练相关配置：
  - 可训练参数：适配器层（模态偏移模块）约 **200M 参数**
  - 峰值学习率：$3 \times 10^{-5}$
  - 骨干模型：LLaVA-v1.5-7B、Qwen2.5-VL-7B、InternVL3-8B
- 关于算力资源的细节需参考论文附录 A（提供的文本中未包含该部分内容），**无法从现有材料中确认**。

## 5. 实验数量与充分性

论文实验规模较大，主要分为以下几类：

- **零样本综合评测**：3 个骨干模型 × 10 个基准，对比 6 种后训练基线方法（Table 1）。
- **模态冲突缓解验证**：
  - BLINK 细粒度感知（2 个骨干 × 6 个子任务，Table 2）
  - 视觉辅助语言任务（3 个任务，Fig. 5a）
  - 文本困惑度（Fig. 5b）
- **涌现能力实验**：
  - 幻觉缓解（HallusionBench，2 个骨干）
  - 多模态上下文学习（2 个数据集 × 3 种 shot 设置 × 3 个骨干，Table 3）
  - DEMON 演示指令跟随（7 个子任务 × 3 个骨干，Table 4）
- **深入分析**：
  - 模态表示可视化（UMAP，Fig. 6a）
  - DINOv2 语义差距线性探测（Fig. 6b）
  - **组件消融**：4 种变体（w/o intervention、w/o mutual、w/o global、w/o distillation）× 3 个骨干 × 4 个基准（Table 5）
  - **损失权重消融**：10 种权重组合（Table 6）
  - **模态协同实验**：不同图文数据比例下的 NoCaps 与 MMLU 趋势（Fig. 7）

**充分性评价**：

- **优点**：实验覆盖广，涵盖多个骨干、多类任务、多组消融，且模型无关性得到验证；消融实验系统性地验证了各组件贡献。
- **客观性**：对比方法均为已发表的后训练对齐方法，评测基准为标准学术基准，零样本设定较为公平。
- **潜在不足**：损失权重消融主要在 Qwen2.5-VL-7B 上进行，未在所有骨干上验证；部分对比基线（如 VISTA）可能为同期工作，公平性需结合发布时间判断。

## 6. 主要结论与发现

- **DeepAlign 有效缓解模态冲突**：在多个视觉-语言任务上显著提升性能，且方法模型无关，可适用于 LLaVA-v1.5-7B、Qwen2.5-VL-7B、InternVL3-8B 等不同骨干。
- **零样本性能提升显著**：以 Qwen2.5-VL-7B 为例，MMBench +1.0、MMStar +1.6、ScienceQA +1.5、TextVQA +1.7；在 LLaVA-v1.5-7B 上提升更为明显（如 MMBench 从 62.1 提升至 68.2）。
- **细粒度感知增强**：在 BLINK 六个子任务上全面提升，缩小了与 GPT-4o、Gemini-1.5-Pro 等闭源模型的差距。
- **视觉辅助语言任务逆转**：加入视觉输入后，MNER、MMT、MRE 性能由下降转为提升，说明模型能有效利用视觉信息。
- **文本困惑度降低**：虽仍高于纯 LLM，但 DeepAlign 后显著下降，补偿了视觉模态带来的文本能力损失。
- **涌现能力**：
  - 幻觉缓解（HallusionBench 提升）
  - 多模态上下文学习（随着 shot 数增加性能稳步提升）
  - 交错图文序列的演示指令跟随（DEMON 各任务提升）
- **模态协同**：随着图文对数据增加，DeepAlign 在 NoCaps 与 MMLU 上均持续上升，而标准微调会导致 MMLU 显著下降，说明 DeepAlign 实现了初步的跨模态增强协同。

## 7. 优点

- **问题洞察深刻**：将模态冲突细分为“表示错位”与“细节流失”两个可操作层面，并通过探索性实验量化验证，动机扎实。
- **方法设计精巧**：
  - 表示干预通过模态分类器 + Grad-CAM 提取模态特定成分，思路新颖且可解释。
  - 同时考虑实例级与全局级偏移方向，兼顾个体差异与整体趋势。
  - 引入互信息正则项，在拉近模态距离的同时保留关键信息。
  - 结构引导蒸馏利用 DINOv2 的 patch 级相似度作为视觉监督，绕开了对文本描述的依赖。
- **模型无关性强**：在三种不同架构的 MLLM 上均有效，通用性好。
- **训练高效**：仅训练约 200M 参数的适配器层，骨干冻结，训练成本相对较低。
- **损失权重鲁棒**：损失权重消融显示各权重设为 1.0 即可取得优异性能，无需复杂调参。
- **实验覆盖全面**：涵盖零样本评测、细粒度感知、涌现能力、可视化分析、组件消融、损失权重消融、模态协同趋势等多个维度。

## 8. 不足与局限

- **算力信息缺失**：论文未明确说明 GPU 型号、数量与训练时长，复现成本与资源需求不透明。
- **骨干规模有限**：仅在 7B-8B 量级的模型上验证，未涉及更大规模（如 13B、70B）或更小规模模型，泛化性有待进一步验证。
- **损失权重消融覆盖不足**：仅在 Qwen2.5-VL-7B 上进行，未在 LLaVA-v1.5-7B 与 InternVL3-8B 上重复验证。
- **依赖 DINOv2 先验**：结构引导蒸馏的效果受 DINOv2 表征质量影响，若图像域与 DINOv2 预训练域差异较大（如医学影像、遥感影像），效果可能受限。
- **模态分类器与 Grad-CAM 的假设**：模态特定成分的提取依赖于模态分类器的判别能力，若分类器本身存在偏差，可能影响对齐效果。
- **应用场景差异**：论文聚焦于通用 MLLM 的视觉-文本对齐，与 UAV RGB-T 显著目标检测等特定任务差异较大，其对齐思想虽有迁移潜力，但未在相关场景验证。
- **潜在偏差风险**：后训练数据来自 CC3M 与 COCO Caption 子集，数据分布可能偏向自然图像与英文描述，对多语言、多领域场景的适用性未充分探讨。
- **与闭源模型的差距仍存**：尽管有所缩小，但在部分基准（如 OCRBench、MMMU）上与 GPT-4o、Gemini-1.5-Pro 仍有明显差距。

（完）
