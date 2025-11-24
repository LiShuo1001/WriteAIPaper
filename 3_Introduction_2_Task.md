# 三、任务创新式

> 这种风格的论文往往不只是提出一个新方法，而是对问题本身做了重新定义、扩展或泛化，从而赋予研究更高的原创性与学术影响力。

> 核心理念：现有任务定义（或评估设定）不符合真实需求/存在重大缺陷 → 本文提出一种更合理/更具挑战性的新定义 → 为此构建新方法并进行实验验证。

> 与**方法为主**的研究不同，这种引言强调你看到了别人没看到的**任务本身的问题**，是一种从根源出发推动**研究范式演进**的写法。

> 旧任务不足 → 新任务设定 → 新挑战与思路 → 方法 → 贡献

> 旧任务不合理 → 我重新定义 → 带来新挑战 → 我设计方法解决 → 实验验证新定义+新解法的优势。


### 典型适用场景

| 适用场景                 | 示例说明                                                                         |
|--------------------------|----------------------------------------------------------------------------------|
| 提出新任务设置            | 如：Few-Shot Class-Incremental Learning (FSCIL)、Open-World Semantic Segmentation |
| 修正已有任务设定不合理之处 | 如：传统分类只关注 accuracy，不考虑 calibration；图像标注忽略标签冗余                 |
| 引入更贴近现实的数据设定   | 如：Realistic Long-Tail Recognition、Multi-Label under Incomplete Annotation      |
| 跨学科任务迁移            | 如：AI for Science / Social Good，结合真实应用构造任务                              |

### 第一段：引入背景与现有任务设定

> 目的：描述当前的主流任务是什么，它为什么重要，以及它是怎么定义的。

### 第二段：指出现有定义的局限，引出新任务

> 目的：批判现有任务设定不符合现实需求，引出你的“新定义”。

### 第三段：阐明新任务面临的新挑战与建模动机

> 目的：说明新任务带来了哪些新挑战，提出新的建模需求，作为你方法设计的出发点。

### 第四段：方法简述

> 目的：给出你设计的解决方案方法框架。

### 第五段：贡献总结

> 目的：总结贡献。


### 案例分析

论文：《[Open-Vocabulary Object Detection Using Captions](https://openaccess.thecvf.com/content/CVPR2021/papers/Zareian_Open-Vocabulary_Object_Detection_Using_Captions_CVPR_2021_paper.pdf)》

| 段落     | 内容 |
|----------|------|
| 第一段   | **背景与任务**：传统目标检测模型如 Faster R-CNN 虽然精度高，但需要大量人工标注的 bounding box，限制了其在大规模类目下的扩展能力。 |
| 第二段   | **现有任务设定的局限**：现有的 zero-shot 和 weakly supervised 检测方法要么依赖封闭词表、要么精度低，且通常假设测试类别在训练时已知，缺乏泛化能力。 |
| 第三段   | **任务创新与动机**：我们提出了“开放词汇目标检测”任务（OVD），在训练时仅对部分 base classes 提供 bounding box，利用大量 image-caption 对来学习语义空间，实现对未见类的泛化。 |
| 第四段   | **方法简介**：设计了 OVR-CNN 框架，先用 captions 预训练视觉-语言语义空间，再将其迁移到 Faster R-CNN，实现开放词汇检测能力。 |
| 第五段   | **贡献总结**：提出 OVD 新任务设定；构建 image-caption + box 混合监督训练框架；显著优于现有 zero-shot / weakly supervised 方法（27.5% mAP vs 10%）；首次实现大词汇扩展目标检测的实用性能。 |


这篇论文不是仅仅提出一种新方法，而是提出了一个新的问题定义（open-vocabulary object detection），并且清晰界定了与 zero-shot 和 weakly supervised detection 的不同；
引入了新的数据设定组合（caption + base class boxes），并提供了解决方案；
在实验中明确验证了该新任务下的性能表现与泛化能力。

