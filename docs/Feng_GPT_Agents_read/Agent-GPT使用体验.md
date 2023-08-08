# Agent-GPT使用体验

Status: Done
Project: 冯屹芃 (https://www.notion.so/86c24d8e0a714387a116b433f6cc6c2e?pvs=21)

## 网页端AgentGPT使用体验

和Auto-GPT类似，Agent-GPT同样会将大任务划分为几步具体的小任务，并将每一步任务展示给用户

**测试例子：**

要求Agent-GPT写一篇反对日本核废水排海的文章，不多于250词

![屏幕截图 2023-07-15 143418.jpg](Agent-GPT%E4%BD%BF%E7%94%A8%E4%BD%93%E9%AA%8C%2054892f9dc0ff4bf2975c913bdb8a85fc/%25E5%25B1%258F%25E5%25B9%2595%25E6%2588%25AA%25E5%259B%25BE_2023-07-15_143418.jpg)

它自己补充的更具体的任务安排：先调查日本核废水排海政策的详细信息，分析核废水排海后对环境和人类健康的危害，然后组织论据反对日本核废水排海政策，并说明主要从哪几种角度去反对。

Adding Task: Research the details and implications of Japan's nuclear wastewater discharge
policy.
Adding Task: Identify and analyze the potential environmental and health risks associated with the
discharge of nuclear wastewater.
Adding Task: Compile arguments and evidence to oppose Japan's nuclear wastewater discharge
policy, focusing on the potential negative consequences and exploring alternative solutions

不过Agent-GPT完成的文章长度并没有满足设置的字数要求，通常为300-350词，而且可能会出现文章不完整的情况：

[AgentGPT生成文章1.txt](Agent-GPT%E4%BD%BF%E7%94%A8%E4%BD%93%E9%AA%8C%2054892f9dc0ff4bf2975c913bdb8a85fc/AgentGPT%25E7%2594%259F%25E6%2588%2590%25E6%2596%2587%25E7%25AB%25A01.txt)

**优势：**

网页版AgentGPT与Auto-GPT不同之处在于：若用户没有要求Stop Agent（结束服务），则AgentGPT会将这个提示一直迭代下去，生成一篇又一篇文章。随着迭代次数的增加，Agent-GPT反对日本核废水排海政策的角度可能会更广泛且有深入的信息：比如从最开始的环境与人类健康的保护角度，到后面开始考虑从旅游业和海产贸易等经济角度来展开论述，甚至文中详细说明海产的重金属含量。

这种无限迭代生成结果的方法有利于实现更高质量完成用户给出的任务。

[AgentGPT生成文章2.txt](Agent-GPT%E4%BD%BF%E7%94%A8%E4%BD%93%E9%AA%8C%2054892f9dc0ff4bf2975c913bdb8a85fc/AgentGPT%25E7%2594%259F%25E6%2588%2590%25E6%2596%2587%25E7%25AB%25A02.txt)

[AgentGPT生成文章3.txt](Agent-GPT%E4%BD%BF%E7%94%A8%E4%BD%93%E9%AA%8C%2054892f9dc0ff4bf2975c913bdb8a85fc/AgentGPT%25E7%2594%259F%25E6%2588%2590%25E6%2596%2587%25E7%25AB%25A03.txt)

此外，AgentGPT完成任务的效率更高，每一篇文章的生成时长通常只有10s左右。

且网页版Agent GPT使用更加方便，有UI界面，且可调节Temperature值。

**不足：**

AgentGPT似乎不能按照用户的要求去规束其生成文章的长度，甚至会生成不完整的文章；

无限迭代生成结果的方法可能会导致完成任务效率较低。为用户提供太多版本的答案，可能会增加用户筛选时的工作量。（优化方案：规定迭代次数上限？10次？20次？）