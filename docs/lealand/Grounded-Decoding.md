# Grounded Decoding

[Grounded Decoding (grounded-decoding.github.io)](https://grounded-decoding.github.io/)

GM (grounded model) : 一个基于应用场景环境信息的模型。

LLM+GM：LLM和GM结合，综合二者的评分得到下一个token。

affordance functions: 对环境信息的评估函数。其中一种类型的affordance function可以保证模型只会选择安全的环境信息。

![Untitled](Grounded%20Decoding%20ded6ae4222cc4a028ddfd3be38a258b8/Untitled.png)

### 阅读论文 《**Grounded Decoding: Guiding Text Generation with Grounded Models for Robot Control》**

将LLM应用于具体环境的问题：

1. LLM本身不和环境交互。
2. 与非语言对象交互的问题。
3. 不能辨别安全的或可行的对象。

执行口头命令

环境信息+LLM语言生成：在实际场景应用中，生成token的概率可以被拆解为基于环境的token概率和基于语言模型的token概率。

提供环境信息的模型叫做Grounding Model，将环境信息和嵌入语言生成的过程叫做Ground Decode（GD）。

pre-trained multi-task language-conditioned CLIPort (short and long)

**实验1：桌面操作系统**

![Untitled](Grounded%20Decoding%20ded6ae4222cc4a028ddfd3be38a258b8/Untitled%201.png)

**实验2：二维迷宫**

和HRL做对比

**实验3：厨房机器人**

*思考：可否给机器人添加记忆功能，让机器人能够记住物品放在什么地方，这样就不用反复搜索房间信息了。*

实验结果

![Untitled](Grounded%20Decoding%20ded6ae4222cc4a028ddfd3be38a258b8/Untitled%202.png)

在任务模棱两可的情况下成功率不佳，“计划”的成功率比“执行”的成功率高，在任务信息准确的情况下GD和SayCan成功率相同（可能是因为Saycan已经知道了所有目标的信息）。

![Untitled](Grounded%20Decoding%20ded6ae4222cc4a028ddfd3be38a258b8/Untitled%203.png)

GD更有效率（但SayCan成功率更高，而且仅就成功率而言，仅仅50%-60%的成功率是完全不足以投入应用的）

**作用机理**

GD缩小了语言空间中的搜索范围。

**缺陷**

首先，虽然grounding funcitons是通用的，但如何保证其质量和可用性是一个问腿，尤其是相较于LLM。

其次，通常需要提示词工程来引导LLM进入理想的action space。

最后，与能够同时进行grounding和语言推理的一个模型相比，LLM+Grounding Model的模式可能仍然具有局限性。

**未来方向**

GD很灵活，可以集成许多其他的grounding functions(ways)。

发展grounding的基础模型将显著提高GD性能。

最后，尽管GD的基于概率过滤的方法非常通用，但在每次token解码后将grounding information融合到语言模型中可能会受到限制，如何在decoding期间优雅地集成这种grounding information是作者团队未来的研究方向