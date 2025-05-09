<div align=center>
  <h1>从0手动复现DeepSeek v3模型</h1>
</div>

&emsp;&emsp;最近，国产开源大模型 **DeepSeek v3** 火遍全球，仅以 **557万美元** 的超低成本训练出媲美 OpenAI、Google 和 Meta 等巨头数十亿美元投入的模型，还在性能上超越了 Claude 3.5 Sonnet 和 GPT-4o等顶尖闭源模型，被誉为“东方魔法”！

## 为什么 DeepSeek v3 这么强？

<details>
  <summary>低成本高效率</summary>

&emsp;&emsp;DeepSeek v3 仅用 **2048 张 H800 GPU** 训练两个月，成本仅为 LLaMA 3 的 **1/8**，API服务价格更是低至**每百万 tokens 1 元人民币**，是 GPT-4 Turbo 的 **1/70**，可以说是达到了极致的性价比！

</details>

<details>
  <summary>技术创新</summary>

  - MLA（多层注意力架构）：通过合并计算层，减少内存占用和计算量。
  - FP8 混合精度训练：在保证关键计算精度的同时，大幅降低整体计算量。
  - DualPipe跨节点通信：解决大规模分布式训练中的通信瓶颈问题，降低了通信成本。
  - 动态负载均衡：优化专家模型（MoE）的任务分配，确保每个“专家”高效工作。
  - MTP（多 token 预测）：同时预测多个 token，提升生成效率和准确性。
</details>

<details>
  <summary>数据与模型优势</summary>

&emsp;&emsp;DeepSeek v3 拥有 **671B** 参数，训练数据量高达 **14.8T token**，且经过精细清洗和处理。此外，它还从自研的推理模型 **DeepSeek R1** 中提取解题策略，进一步提升了数学和编程能力。
</details>

## DeepSeek-V3开源对国内开发者的重大意义：

- 价格地震：DeepSeek v3 的低成本将倒逼 AI 行业降价，推动高性能 AI 走向平民化
- 思维革命：其工程化创新将引发全球对效率与成本平衡的重新思考
- 开源生态：作为开源模型，DeepSeek v3 为开发者提供了强大工具，加速 AI 民主化进程

&emsp;&emsp;听起来好像有点空？换句话说，它完完全全降低了开发复杂AI系统的门槛和价格，尤其是对于资源有限的中小企业和个人开发者意义非凡，别管现在硅谷巨头们对于AGI的探索到底到了哪一步，可以肯定的是，未来各行各业AI化是必然的趋势，除了大厂，更多的中小型企业对于大模型的需求也会迅速增多！

&emsp;&emsp;正是基于**让开发者们能够快速拥抱大模型蓝海市场**的愿景，[@九天Hector](https://space.bilibili.com/385842994) 老师团队，在DeepSeek v3开源的第一时间，就开始了紧锣密鼓的研发工作，历时两周，深扒文献、攻克技术难点、痛击底层原理——

&emsp;&emsp;终于！！从原理框架到训练微调一站式速通，**完整复现了DeepSeek v3训练全过程**，并已经训练出来了一个mini版本的DeepSeek v3模型，你可以点击👇放链接查看完整训练过程记录！（温馨提示：课件+老师讲解视频，配合食用效果更佳！！）

#### 【从零手动复现DeepSeek v3】
☑️ [DeepSeek v3分词器训练](https://github.com/fufankeji/LLMs-Technology-Community-Beyondata/blob/main/Open-source-model/DeepSeek-V3/6.MiniDeepSeek分词器训练流程.md)：详细介绍了分词器的训练流程，从数据准备、分词器初始化、训练、保存到评估，完整展示了如何为一个大模型训练一个高效的分词器。分词器的训练是大模型训练的基础步骤，合理的分词策略能够显著提升模型的性能。

☑️ [DeepSeek v3预训练](https://github.com/fufankeji/LLMs-Technology-Community-Beyondata/blob/main/Open-source-model/DeepSeek-V3/7.MiniDeepSeek预训练.md)：详细介绍了从数据准备、模型架构设计、训练脚本编写到模型训练与评估的完整流程。通过合理的参数调整、分布式训练支持、学习率调度和模型保存机制，能够高效地进行大规模语言模型的预训练。同时，通过WandB等工具进行训练监控和日志记录，确保训练过程的透明性和可追溯性。

☑️ [DeepSeek v3后训练](https://github.com/fufankeji/LLMs-Technology-Community-Beyondata/blob/main/Open-source-model/DeepSeek-V3/8.MiniDeepSeek后训练.md)：详细介绍了全量指令微调和DPO强化学习微调全过程，这是大模型后训练中的关键技术，能够显著提升模型在特定任务上的表现，到这里我们的小型DeepSeek v3大模型训练就基本完成了，老师还进行了前端部署教程，用户可以直接与模型进行交互，验证其在实际应用中的效果！

🔥 [【全网独家】手动复现Mini DeepSeek v3！模型预训练+全量指令微调+DPO强化学习微调全流程实战（合集）](https://www.bilibili.com/video/BV1KtwueYE54)

>欢迎加入「赋范大模型技术社区」，扫描文章底部二维码入群，即可获取完整代码、数据以及模型权重等完整公开课资料～

</div>

&emsp;&emsp;当然不仅于此，相较于大模型训练原理开发，我们还结合当下最新的框架和最前沿的技术，做出了**一系列的Agent智能体开发项目**，同时已经制作成完整的教程文件，为你接轨大模型领域，提供最坚实的技术支持！赶紧点击下方👇链接查看吧

#### 【DeepSeek v3基础入门】

☑️ [DeepSeek v3的API 调用全流程](https://github.com/fufankeji/LLMs-Technology-Community-Beyondata/blob/main/Open-source-model/DeepSeek-V3/1.DeepSeek%20v3%20API接入指南.md)

☑️ [DeepSeek v3 Function calling实现方法](https://github.com/fufankeji/LLMs-Technology-Community-Beyondata/blob/main/Open-source-model/DeepSeek-V3/2.DeepSeek%20v3%20Function%20calling实现方法.md)

💎 [DeepSeek-v3调用指南与Function calling技术实战（视频）](https://www.bilibili.com/video/BV1JuwVewELc)

......

#### 【DeepSeek v3本地部署】

☑️ [DeepSeek v3本地部署流程](https://github.com/fufankeji/LLMs-Technology-Community-Beyondata/blob/main/Open-source-model/DeepSeek-V3/9.DeepSeek%20v3%E6%9C%AC%E5%9C%B0%E9%83%A8%E7%BD%B2%E6%B5%81%E7%A8%8B.md)

💎 [DeepSeek v3本地部署与调用实战｜vLLM、SGLang、LMDeploy（视频）](https://www.bilibili.com/video/BV1jjwVe4EKn)

......

#### 【DeepSeek v3智能体开发】

☑️ [DeepSeek v3基于Open-WebUI打造专属聊天机器人](https://github.com/fufankeji/LLMs-Technology-Community-Beyondata/blob/main/Open-source-model/DeepSeek-V3/3.打造专属聊天机器人：Open-WebUI接入DeepSeek%20v3流程详解.md)

💎 [DeepSeek v3+Open WebUI搭建专属聊天机器人（视频）](https://www.bilibili.com/video/BV1JuwVewELc)

☑️ [DeepSeek v3借助Swarm搭建多代理智能体](https://github.com/fufankeji/LLMs-Technology-Community-Beyondata/blob/main/Open-source-model/DeepSeek-V3/4.DeepSeek智能体开发实战.md)

💎 [DeepSeek v3+OpenAI Swarm的Multi-Agent技术入门实战（视频）](https://www.bilibili.com/video/BV1T8czeSEf1)

☑️ [DeepSeek v3借助GraphRAG搭建知识库问答机器人](https://github.com/fufankeji/LLMs-Technology-Community-Beyondata/blob/main/Open-source-model/DeepSeek-V3/5.DeepSeek知识库问答实战.md)

💎 [DeepSeek v3+GraphRAG知识图谱检索增强技术实战（视频）](https://www.bilibili.com/video/BV1Xwc6eoEW5)

......

**当然，此项目在持续维护更新中～！！**

## 写在后面：

&emsp;&emsp;站在25年的开端回望，不管是OpenAI o3的诞生，还是DeepSeek v3的发布，大模型技术正在以惊人的速度重塑世界，正在以前所未有的方式改变着人类文明的进程！每一天，我们都在见证技术奇迹的发生，都在参与这场改变人类命运的技术革命。

&emsp;&emsp;这也许是“最好的时代”，但也是“最坏的时代”，技术的快速迭代意味着我们从业者面临着巨大的压力，新技术层出不穷，知识的半衰期正在急剧缩短，持续学习不再是一种选择，或许更是一种生存必需！

&emsp;&emsp; 我们正是切身感受到了这种压力，才深知：只有不断的更新知识体系，才能为学员提供最有价值的技术赋能。每一次课程的更新，每一个项目的设计，都是我们对技术前沿的追赶，对每一位技术人负责的教育初心坚守！

&emsp;&emsp;[@九天Hector](https://space.bilibili.com/385842994)老师常说，在大模型技术浪潮中，我们不仅要传授知识，更要培养学员们的创新思维和适应能力，要教会大家如何在技术的浪潮中保持清醒，如何在变革的时代中找到方向。这是我们的使命，是我们的荣耀，也是赋范空间创办的初心！

&emsp;&emsp;如今，九天老师团队正式成立了【**赋范大模型技术社区**】，目的就是**提供国内最前沿的优质大模型学习内容**，成为大模型与学习者们的交流阶梯，**实现个人学业/职业/兴趣的梦想**，拥抱更恢弘而辽阔的大模型世界。

>我们提供各类大模型的包括环境设置、本地部署、高效微调等技能在内的**全流程指导**，简化大模型的使用和应用流程，让更多的普通学生、研究者更好地使用大模型，帮助前沿、有效的大模型更快融入到普通学习者的生活中。

<div align=center>

海量硬核独家技术干货内容+无门槛技术交流

<div align=center>
  <img src="./images/QRcode.png" >
</div>

上图扫码👆即刻入群！

📍 社群技术交流氛围浓厚，不定期开设硬核干货&前沿技术公开课噢~



