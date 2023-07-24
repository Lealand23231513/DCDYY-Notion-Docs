# agentgpt使用报告

Assignee: Lealand
Status: Done
Due: July 9, 2023
Project: 汪俊辰 
Priority: Medium

## 使用方法

直接在互联网上搜索agentgpt，通过网页端使用。或者在电脑上部署使用。

**注意：**网页端每天只能使用5次。如需要更多的使用次数，最好部署到电脑上使用。

部署方法：[*Setup - Reworkd*](https://docs.reworkd.ai/development/setup)

可以根据特定任务选择已有模板开始。

## 测试1：Create a comprehensive report of the Nike company

网页端：

[agent-gpt-output.png](agentgpt使用报告/agent-gpt-output.png)

本地：

开始运行后AgentGPT便开始从互联网上搜集有关Nike公司的信息。一段时间后，注意到其搜索的内容具有较高相似度，其反复搜索有关Nike公司产品利润、营销策略、市场表现等内容，虽然具体表述不同，但实际内容具有较高相似度。同时注意到若非使用者干涉，AgentGPT似乎不会自行停止。

停止AgentGPT运行后，可以选择让其生成一份总结。结果如下：

[**Nike Company Profile, Products, and Financial Performance**](agentgpt使用报告/Nike.md)

AgentGPT的全部执行过程如下：

[agent-gpt-output (1).png](agentgpt使用报告/agent-gpt-output_(1).png)

## 测试2：写一篇关于中国古代的论文

使用的模型是GPT-3.5turbo

生成结果如下：

[my-document (1).pdf](agentgpt使用报告/my-document_(1).pdf)

AgentGPT支持中文作为输出。

在使用GPT-3的情况下，AgentGPT虽然生成了一系列执行任务的方法，如查找文献、生成大纲等，甚至列举出了可供参考的资料库，但是其并没有阅读并归纳其提及到的文章，而仅仅是罗列了一些不明所以的文段。从这个意义上，AgentGPT并没有真正理解命令的要求，其只是循环往复地使用GPT生成命令-生成总结而已。

## 总结：

1. 生成内容上：AgentGPT主要生成文本内容（包括特定文本如python代码），还未测试其是否能够生成图片。
2. 运行效率上：运行速度很快，但若用户不干涉其容易陷入死循环，即不停地重复生成问题-上网搜索-总结回答的过程，即使其已经收集到足够多的信息。AgentGPT似乎不具备自行判断是否应该停止的能力。
3. 交互界面上：有UI，对用户友好。用户可以直观地了解AgentGPT的执行状态。