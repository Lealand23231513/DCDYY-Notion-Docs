# GPT_prompt吴恩达课程

Assignee: Lealand
Status: Done
Due: July 9, 2023
Project: 汪俊辰
Priority: High

# 一种和LLM沟通的方式

1. 善用分隔符，如特定的标点符号等。
2. 要求模型以特定格式文本作为输出，如JSON等。
3. 要求模型检查
4. 给模型提供成功的样例

小心：幻觉(Hallucination)——模型试图编造一些看似正确的话语回答问题。 解决方案：要求模型先搜索信息，再回答问题。同时需要要求模型输出其引用的信息。

# 迭代开发

根据要求不断调整prompt

# 功能

摘要、总结

## 推理

推断给定的文本具有的特性，如：情感倾向（积极、消极），主题。 给出文本就可以直接进行推断，不需要经过机器学习训练。

## 转换

文本转换格式，可用于翻译、HTML转Markdown等。

## temperature

temperature 越高，就越可能生成出现概率低的词语。 temperature 低：模型可靠、可预测，同时创造力较差。温度为0时，每次提问都期望得到相同回答。 temperature 高：模型更不可预测、创造力更强。在更高的温度下，AI 助理更容易分心，但也许更加具有创造力。

## system messages

role system:作为系统消息，提供内部提示 role assistant:ChatGPT 模型 role user:用户