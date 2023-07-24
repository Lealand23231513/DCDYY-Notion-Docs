# 阅读：ChatGPT原理

Assignee: Lealand
Status: Done
Due: July 9, 2023
Project: 汪俊辰 
Priority: Medium

## 原理

概率匹配：选择下一个出现概率最高的词。

问题：每次都选择出现概率最高的词，则文章缺乏创造力。

温度：以一定的频率选择概率排名较低的词。

n-grams：根据词频和n个前序单词生成下一个单词。

估计序列出现的概率。

神经网络、机器学习、梯度下降

嵌入（embadding）：在meaning space中，词义相近的词会处于相邻的位置，而词义差距较大的词会处于较远的位置。