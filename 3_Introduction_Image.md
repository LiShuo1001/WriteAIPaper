
# 引言中的常见图示类型

> 在引言部分，插图的目的是用来快速传达论文动机、问题背景或方法思想。

| 图示类型 | 功能描述 | 常见用途 | 优点 | 潜在问题 |
|----------|-----------|-----------|--------|------------|
| 🧩 **问题示意图** | 图示任务定义、输入输出结构或研究问题设置 | 新任务、新范式 | 一目了然，降低理解门槛 | 若任务不新颖，可能显得“多余” |
| ⚙️ **方法框架图** | 展示模型结构、数据流、模块间关系 | 引出方法结构、模块组成 | 快速概括方法核心 | 若太复杂会“信息过载” |
| 🧠 **动机示例图** | 对比现象、错误预测、失败案例等 | 引发问题意识、制造紧迫感 | 情感带入强、抓人眼球 | 容易被视为“主观动机” |
| 🔀 **对比分析图** | 方法对比、类别演化、方案效果变化等 | 动机段落、历史演化型引言 | 强化方法必要性 | 表达逻辑需简明，避免“堆方法” |
| 📊 **定量结果预览图** | 展示一组结果先剧透方法优越性 | 引发兴趣、先声夺人 | 很有说服力 | 要确保图例结果真实可靠 |
| 🧪 **定性结果预览图** | 展示一组结果先剧透方法优越性 | 引发兴趣、先声夺人 | 很有说服力 | 要确保图例结果真实可靠 |
| 🔬 **现实应用图** | 展示实际场景、设备、交互界面等 | 多模态、具身智能、医学、机器人等 | 增强实际价值感 | 非AI类会议可能要求简化处理 |
| 📈 **趋势曲线图** | 展示研究领域的发展趋势或热点演化 | 趋势主导型引言 | 有时代感 | 数据来源需可靠、标注清晰 |

> 注意：以上图示类型通常是**混合的**，即在一篇论文中经常出现多个类型的图示组合成一个大的图示。


### 1. 问题示意图

> 用图说明要解决的任务是什么，输入和输出是什么，任务本身具有什么挑战性。

> 适用情况：提出新任务、新设定或与主流定义有明显不同；对非本领域评审尤其重要。

示例
* [Few-shot Object Detection via Feature Reweighting](https://openaccess.thecvf.com/content_ICCV_2019/papers/Kang_Few-Shot_Object_Detection_via_Feature_Reweighting_ICCV_2019_paper.pdf)
* [Segment Anything](https://openaccess.thecvf.com/content/ICCV2023/papers/Kirillov_Segment_Anything_ICCV_2023_paper.pdf)


### 2. 方法框架图

> 用模块化方式展示你的整体方法结构，突出各模块的设计目标与数据流向。

> 适用情况：方法较复杂（如多模块、跨模态、交互机制）；评审需快速理解你的“结构感”。

示例
* [End-to-End Object Detection with Transformers](https://arxiv.org/pdf/2005.12872)
* [Learning Transferable Visual Models From Natural Language Supervision](https://proceedings.mlr.press/v139/radford21a/radford21a.pdf)
* [BLIP: Bootstrapping Language-Image Pre-training for Unified Vision-Language Understanding and Generation](https://proceedings.mlr.press/v162/li22n/li22n.pdf)
* [LoRA: Low-Rank Adaptation of Large Language Models](https://arxiv.org/pdf/2106.09685v1/1000)


### 3. 动机示例图

> 展示一个直观例子，引发**现有方法在这儿做得不够**的感觉。

> 适用情况：强调现有方法不足；适用于可解释性、推理、多模态等任务。


### 4. 对比分析图

> 系统对比已有方法在某些维度上的演进路线，引出方法的优势。

> 适用情况：强调演化过程和思路；适用于大多数增量创新方法。

示例：
| 方法 | 是否使用语言 | 是否增量推理 | 依赖类别标签 | 可解释性 |
|------|---------------|----------------|----------------|-----------|
| A    | ✘            | ✘             | ✔              | ✘         |
| Ours | ✔            | ✔             | ✘              | ✔         |


### 5. 定量结果预览图

> 在引言中提前亮出关键实验结果，让评审**眼前一亮**。

> 适用情况：效果非常好，想要提前剧透；提高引言吸引力。

示例
* [Visual Prompt Tuning](https://arxiv.org/pdf/2203.12119)
* [DINO: DETR with Improved DeNoising Anchor Boxes for End-to-End Object Detection](https://arxiv.org/pdf/2203.03605)
* [Searching for MobileNetV3](https://openaccess.thecvf.com/content_ICCV_2019/papers/Howard_Searching_for_MobileNetV3_ICCV_2019_paper.pdf)
* [Analyzing and Improving the Training Dynamics of Diffusion Models](https://openaccess.thecvf.com/content/CVPR2024/papers/Karras_Analyzing_and_Improving_the_Training_Dynamics_of_Diffusion_Models_CVPR_2024_paper.pdf)


### 6. 定性结果预览图

> 在引言中提前亮出关键可视化结果，让评审**眼前一亮**。

> 生成的图片，可视化结果，预测的结果等

> 适用情况：效果非常好，想要提前剧透；提高引言吸引力。

示例
* [Emerging Properties in Self-Supervised Vision Transformers](https://openaccess.thecvf.com/content/ICCV2021/papers/Caron_Emerging_Properties_in_Self-Supervised_Vision_Transformers_ICCV_2021_paper.pdf)
* [Stable Video Diffusion: Scaling Latent Video Diffusion Models to Large Datasets](https://arxiv.org/pdf/2311.15127)

### 7. 现实应用图

> 展示真实设备/环境/系统界面等，强调你的方法不仅限于理论。

> 适用情况：人机交互、具身智能、AI+医学/教育等应用场景；向评审传达**可落地性**。

示例
* [ROBUSTNAV: Towards Benchmarking Robustness in Embodied Navigation](https://openaccess.thecvf.com/content/ICCV2021/papers/Chattopadhyay_RobustNav_Towards_Benchmarking_Robustness_in_Embodied_Navigation_ICCV_2021_paper.pdf)


### 8. 趋势曲线图

> 展示领域热点演变、方法发展趋势，建立论文**必要性**。

> 适用情况：想以“趋势推动”方式引入；强调研究背景和任务演化。


### 图示设计灵感图库

> TODO：添加好的图示案例



# 注意事项

> 引言图不是装饰品，而是**论证工具**。它的使命是以最小的认知负担传达最核心的信息，让审稿人快速理解问题和创新点。


* 内容设计原则：清晰、集中、有逻辑

| 项目         | 要点说明                                                   | 示例 / 建议 |
|--------------|------------------------------------------------------------|-------------|
| 目标清晰     | 图示目的明确，仅展示一个核心问题或思路                     | “问题是什么？”或“方法结构是什么？”不能混在一起 |
| 信息聚焦     | 控制信息量，避免冗余，尽量使用最小图单元传达最大信息       | 如果方法复杂，可只画主要模块，细节留在方法部分 |
| 模块分明     | 不同功能区分清晰，有输入、处理、输出的逻辑流              | 使用颜色/边框/箭头辅助结构理解 |
| 任务感强     | 强调任务背景中的挑战和目标，体现问题的真实复杂性           | 标出“难点1”、“难点2”，或用文字说明挑战来源 |

* 视觉设计规范：整洁、协调、易读

| 项目         | 要点说明                                                   | 示例 / 建议 |
|--------------|------------------------------------------------------------|-------------|
| 配色协调     | 配色风格统一，避免使用太鲜艳的颜色                        | 推荐使用灰蓝、灰绿、灰紫色调；避免红绿组合 |
| 字号适中     | 图中文字不应小于8pt，标题建议10-12pt                     | 使用Times New Roman或常规无衬线字体 |
| 线条清晰     | 模块边框、箭头不宜过细，层次感强                          | 建议线宽 > 1.2pt，箭头方向明确 |
| 图层干净     | 避免图中元素重叠，留足视觉空白                           | 保证模块之间留白合理，不显拥挤 |
| 图例可见     | 若有图例，位置适中不遮挡内容，字号清晰                    | 图例建议放右下角或下方，字体与正文统一 |

* 图文对齐逻辑：图配文，文带图

| 项目             | 要点说明                                                   | 示例 / 建议 |
|------------------|------------------------------------------------------------|-------------|
| 图文同步         | 图应出现在文字提及的位置附近，避免跨页或跨段引用         | “如图1所示”应紧随图出现，评审不翻页就能看到 |
| 图注完整         | 图注描述要完整明确，表达图的结构与功能                   | “Figure 1: Overview of our method, including A, B, and C...” |
| 文字引导阅读     | 正文要明确引导读者关注图中哪部分，增强图文互动           | 如：“图1(b)展示了我们提出的prompt生成机制” |

