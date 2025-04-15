# Related Work

* 一、常见的写作逻辑结构
* 二、写作范式与段落结构建议
* 三、避免简单列举增加讨论深度
* 四、长度受限压缩内容
* 五、方法比较：相同点与不同点


> **相关工作**是论文中至关重要的一部分，主要目的是**展示对研究领域的理解**、**辨析已有方法的利弊**，以及**突出工作的创新性和定位**。


> 梳理已有工作的研究脉络，体现你对领域的把握；显示工作的技术来源与创新点；强化**我们比已有方法更好**的逻辑与论据；避免简单罗列，体现分析与对比的深度。



## 一、常见的写作逻辑结构

> 体现逻辑清晰、脉络连贯


#### 1. 按技术模块组织

> 这是最常见的方式，尤其**适合问题明确、方法结构清晰**的论文。可以按照工作涉及的关键模块或子技术展开。

例如在写一个联邦学习方法：
* 联邦学习基础与经典算法（如FedAvg）
* 个性化联邦学习方法（FedPer、FedBN、Ditto 等）
* 联邦学习中的概念学习（如prompt-based、prototype-based 方法）
* 无标签或测试时自适应的方法（TTA、UDA）

#### 2. 按时间演化组织

> 适用于综述类文章或背景发展显著的方向（如Transformer、Diffusion Model）。

* 初始探索阶段（早期方法及背景）
* 过渡阶段（性能提升的代表工作）
* 当前主流与挑战（现阶段的方法瓶颈）
* 你的方法出现的位置（与这些方法的关联与突破）

#### 3. 按任务类别组织

> 适用于多任务或跨领域融合场景、覆盖面较广的论文。

例如在写一个多模态大模型方法：
* 图像-文本对齐研究
* 文本引导图像生成研究
* 多模态预训练模型
* 多模态下游任务适配

#### 4. 按问题与挑战组织

> 适合**问题导向强**、**方法创新动机清晰**的论文。这种方式会聚焦在已有方法未能解决的问题上，并引出你的研究。

* 数据隐私问题 → 联邦学习方法
* 模型个性化挑战 → 个性化方案
* 多任务之间的干扰 → 协同训练研究


## 二、写作范式与段落结构建议

> 每一个小节或段落，建议遵循**背景—现有方法—不足之处**的逻辑，可以记作：**背景引入** + **代表性工作举例** + **存在的问题/不足**

内容安排建议：
* 覆盖核心代表工作：选出研究方向上的5–10篇顶会/顶刊代表性论文。
* 不要只是罗列：避免**列举+结尾**式写法（即 Paper A 做了X，Paper B 做了Y...）。必须**对比/分析**。
* 适当分类：按不同方法、方向或挑战组织论文，不宜混在一起讨论。
* 照顾读者理解：**适当介绍概念**，例如：“Diffusion Model 是一种通过学习反向扩散过程实现数据生成的方法”。
* 突出你工作的位置：在总结中指出你的方法在已有工作的基础上解决了哪些未解决的问题。


示例：
> 最近几年，个性化联邦学习（Personalized Federated Learning, PFL）逐渐成为研究热点。
> 典型的方法如 FedPer [Smith et al., 2018] 通过拆分共享层与个性化层来增强局部适应性，而 Ditto [Li et al., 2021] 引入了局部正则化目标以缓解全局偏移问题。
> 然而，这些方法往往依赖于较强的个性化监督信号，在低资源或无标签场景下表现有限，难以推广至零样本或测试时自适应设置中。


1. 引入类句式：
* “With the increasing demand for..., many methods have been proposed to...”
* “Recent studies have explored... in various settings, such as...”

2. 代表工作引用类句式：
* “FedAvg [McMahan et al., 2017] is one of the earliest and most widely used algorithms in FL.”
* “To address XXX, XXX et al. proposed YYY, which...”

3. 评价与不足类句式：
* “However, these methods often suffer from...”
* “Nonetheless, such approaches require..., which may limit their applicability to...”
* “Despite these advances, few studies have investigated...”
* “Previous methods mainly focus on..., which improves..., but fails to consider...”
* “Recent approaches such as A and B address X by..., yet they require...”
* “However, these methods overlook...”
* “Nonetheless, their reliance on... limits their scalability in...”

4. 总结并引出你方法类句式：
* “In contrast to the above works, our method tackles the problem from a novel perspective by...”
* “Different from previous efforts that focus on..., our approach explores...”
* “Our approach differs in that it...”
* “We propose a novel perspective by...”


## 三、避免简单列举增加讨论深度

问题：
* 仅是罗列了若干已有方法，没有进行归类分析；
* 没有明确指出这些工作的优缺点；
* 没有体现这些工作与你方法之间的关系与差异；
* 缺乏批判性思维和技术对比，即缺乏“深度”。

方法：
* 缺乏深度	 -> 将罗列变为分析，按类别/问题组织
* 无技术批判	 -> 指出已有方法的不足与局限
* 未突出创新	-> 每段结尾明确强调你的不同点和优点


### 怎么办？——从“列举”走向“分析”

> 把原本**谁做了什么**的描述，改为**谁做了什么、有何贡献、有什么问题、与你的工作什么关系**的深入对比分析。


### 三步走解决方案

#### 第一步：结构上重写为“对比分析”格式

> Paper A uses attention for feature refinement. Paper B uses memory network to store concepts. Paper C applies contrastive learning to tackle non-IID...

> To enhance feature refinement in FL, attention-based strategies have been widely explored.
> For instance, Paper A utilizes self-attention to capture spatial dependencies, leading to better representation learning.
> However, it lacks consideration of semantic-level personalization.
> Paper B takes a step further by introducing a memory network to store user-specific concepts, which improves personalization, but introduces large communication overhead.
> Compared to these methods, our approach dynamically adapts lightweight concept prompts, achieving a better trade-off between performance and communication efficiency.


#### 第二步：每个子方向小节内强调三件事

（1）已有方法解决什么问题；
（2）代表工作做法和缺陷；
（3）我们的不同点和改进。

> Existing works in test-time adaptation focus on enhancing model generalization under domain shift.
> Tent et al. [2020] proposed entropy minimization during testing, which implicitly encourages confident predictions.
> However, such implicit regularization may result in overconfident yet incorrect decisions under severe domain shifts.
> CoTTA [Wang et al., 2022] introduced self-ensembling and augmentation to refine predictions but still relies heavily on the initial model.
> In contrast, our method explicitly leverages pre-learned concept prompts, enabling semantically aware adaptation without accessing source data.


#### 第三步：在段落末突出“我们做了什么”和“与前人工作的关系”

> Unlike previous works that focus solely on visual feature adaptation, we incorporate text-guided concept-level alignment, which enhances generalization under sparse label scenarios.

> To the best of our knowledge, this is the first attempt to combine language-driven prompt learning with test-time adaptation in federated scenarios.


## 四、长度受限压缩内容

#### 1. 主题聚焦：围绕“方法创新点”选取相关工作

你不需要覆盖整个领域，而只需覆盖与你的方法最相关的部分。换句话说：你不写“所有相关工作”，你只写“与我方法紧密相关的代表性研究”。


#### 2. 分类而非堆叠：将大量方法压缩为子类、子方向描述

例如你可以用一句话统摄一类工作，再重点讲你要对比的几个：

> A number of personalized FL methods have been proposed, which can be roughly divided into three categories:
> (1) model partitioning-based [FedPer, pFedMe], (2) regularization-based [Ditto, FedRep], and (3) representation or prompt-based methods [FedPrompt, LoCL].
> Among these, our method focuses on...


#### 3. 代表性引用+批判性表达：不求多，求精与深

你可以选取每个子类中1–2篇代表工作，点到即止，但表达要有“思考”或“批判”。审稿人不在乎你“引用了多少”，更在乎你“是否理解并超越了它”。

> FedRep [Collins et al., 2021] decouples representation and classifier to support personalization.
> However, its static feature encoder struggles under non-IID shifts.
> Our method dynamically adapts concept prompts, enabling better generalization under distributional drift.


#### 4. 将部分综述内容转移到补充材料

如果你真的分析了很多方法，不妨把更详细的版本放入附录，并在主文中写：

> We briefly review the most relevant approaches here; a more comprehensive survey is provided in Appendix A.


#### 5. 术语压缩与并列结构优化写法

**并列结构** + **精准概括** = **最大的信息密度**。

> Previous works in test-time adaptation have explored entropy minimization [TENT], self-ensembling [CoTTA], and data augmentation [SHOT], but most require source data or fail to generalize across domains.

只用一句话提了三类方法、三个代表工作，讲清楚了他们的做法和缺点。



#### 模板示例：紧凑又有深度的相关工作段落

控制在9–10行，引用了6篇代表工作，归类了3类策略，明确点出创新点:
> Personalized Federated Learning (PFL) has attracted increasing attention due to the heterogeneity of client data.
> Early approaches such as FedAvg [McMahan et al., 2017] assume a global model suffices, but perform poorly under distribution shifts.
> To address this, model-splitting strategies (e.g., FedPer [Smith et al., 2018], pFedMe [Dinh et al., 2020]) isolate personalized layers, while regularization-based methods (e.g., Ditto [Li et al., 2021]) introduce client-specific objectives.
> More recent works explore prompt-based personalization [Zhang et al., 2023; Ours], adapting lightweight prompts for client-specific tuning.
> However, existing methods often treat prompts statically and overlook concept-level alignment, which our work addresses via dynamic concept prompting with cross-client generalization.


## 五、方法比较：相同点与不同点

该部分的写作目标总结为：
* ✅ 表达：“我们理解你们的方法，并在其基础上有明确、实质性的突破。”
* ✅ 避免：“我们的方法和他们很像，只是细节有点不同。”（容易被拒）

### 结构化写法框架：相同点 + 不同点 + 优势总结

#### 1. 相同点：站在已有方法肩膀上

说明你工作的合理性和继承性：
> Our method shares with prior works [Method A, Method B] the general idea of using [prompt tuning / concept adaptation / memory modules] for client personalization.

常见表达句式：
* “Inspired by XXX, we also adopt...”
* “Similar to XXX, our model utilizes...”
* “We build upon the idea of..., which has been shown effective in...”

注意：只说“相同点”会显得你没有创新，必须紧接着说出区别。


#### 2. 不同点：明确“我们创新了什么”

强调在结构、机制、任务目标等方面的实质区别：
> However, unlike Method A which uses static prompts shared across tasks, our method dynamically generates concept prompts conditioned on local data, enabling better adaptation to client-specific distributions.

常见对比维度
| 维度       | 示例对比                                       |
|------------|------------------------------------------------|
| 模块设计   | Static vs. Dynamic    Global vs. Local    One-size vs. Personalized |
| 使用方式   | Offline tuning vs. Online adaptation    One-shot vs. Continual |
| 引导目标   | Feature-level vs. Concept-level    Data-driven vs. Knowledge-guided |
| 任务支持   | 仅分类 vs. 多任务<br>只支持单模态 vs. 跨模态     |

常见表达句式：
* “In contrast to..., our approach introduces...”
* “While Method B relies on..., we instead exploit...”
* “Our method differs in that it...”
* “A key distinction is that...”


#### 3. 总结：指出为什么你的方式“更好”或“更广”

别忘了加上一句“总结式比较”，点明你方法的优势或适用性更强：
> This design allows our method to generalize better to heterogeneous clients and unseen tasks, as demonstrated in Section X.

句式模板：
* “This difference leads to improved robustness under...”
* “Consequently, our method performs better when...”
* “As a result, we achieve both higher accuracy and lower communication cost.”


#### 示例片段：高质量的对比写法

示例 1：Prompt-based 方法对比
> Our method is related to FedPrompt [Zhang et al., 2023], which also utilizes prompts for model personalization.
> Similar to FedPrompt, we encode client-specific knowledge into learnable prompts without modifying the backbone model.
> However, FedPrompt learns static prompts that are fixed once trained, whereas our approach introduces dynamic concept prompts that are conditioned on both local data and task semantics.
> This enables more fine-grained personalization and better generalization to new domains.

示例 2：与 Memory-based 方法对比
> While methods such as FedMem [Wang et al., 2022] maintain a memory bank to store client features for adaptation, they suffer from large communication overhead and stale memory.
> In contrast, we distill concept-level knowledge into lightweight prompts, which are updated in real-time and require no explicit memory synchronization.


注意：避免无效的“细节型比较”。




