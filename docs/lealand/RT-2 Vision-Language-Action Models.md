# RT-2: Vision-Language-Action Models

represent robot actions as another language, which can be cast into text tokens and trained together with Internet-scale vision-language datasets.

疑惑：training the model from scratch, co-fine-tuning概念含义

> 开源桌面任务检测程序（真实+模拟）：https://github.com/google-research/language-table
> 

主要特点：

This includes significantly improved generalization to novel objects, the ability to interpret commands not present in the robot training data (such as placing an object onto a particular number or icon), and the ability to perform rudimentary reasoning in response to user commands (such as picking up the smallest or largest object, or the one closest to another object). We further show that incorporating chain of thought reasoning allows RT-2 to perform multi-stage semantic reasoning.