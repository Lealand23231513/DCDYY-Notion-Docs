# GPT-Academic使用体验

Status: Done
Project: 冯屹芃 (https://www.notion.so/86c24d8e0a714387a116b433f6cc6c2e?pvs=21)

[README.md](GPT-Academic%E4%BD%BF%E7%94%A8%E4%BD%93%E9%AA%8C%20bbf038e99cf043e883a74ad67f46a770/README.md)

GitHub链接：

[https://github.com/binary-husky/gpt_academic](https://github.com/binary-husky/gpt_academic)

## 基本介绍

GPT-Academic，即GPT 学术优化是github上基于大语言模型提供学术论文纠错、润色、翻译、局部撰写等功能的开源项目。其现版本能提供的功能已经不止关于学术论文方面，它还有回答一些基础的学术与理论知识问题、编写代码、AI绘画等功能。

## 使用体验

### 1. 介绍傅里叶变换

提出问题，并要求用latex格式回答

![Untitled](GPT-Academic%E4%BD%BF%E7%94%A8%E4%BD%93%E9%AA%8C%20bbf038e99cf043e883a74ad67f46a770/Untitled.png)

它的回答：

![Untitled](GPT-Academic%E4%BD%BF%E7%94%A8%E4%BD%93%E9%AA%8C%20bbf038e99cf043e883a74ad67f46a770/Untitled%201.png)

从结果上看，它简短了介绍傅里叶变换用处，用latex格式写出CFT与DFT公式来介绍傅里叶变换，对快速傅里叶变换FFT也做了很简单的说明，至于公式的推导过程以及FFT算法具体流程都没有解释。

于是我要求它讲解得更详细一些：

![Untitled](GPT-Academic%E4%BD%BF%E7%94%A8%E4%BD%93%E9%AA%8C%20bbf038e99cf043e883a74ad67f46a770/Untitled%202.png)

结果它从傅里叶逆变换来进行正变换公式的推导，和我想象的通过傅里叶级数来讲解方法有出入。

![Untitled](GPT-Academic%E4%BD%BF%E7%94%A8%E4%BD%93%E9%AA%8C%20bbf038e99cf043e883a74ad67f46a770/Untitled%203.png)

（以上为连续傅里叶变换公式的推导，离散傅里叶推导方法和此完全相同

至于快速傅里叶变换，它也做出了更详细的讲解：

![Untitled](GPT-Academic%E4%BD%BF%E7%94%A8%E4%BD%93%E9%AA%8C%20bbf038e99cf043e883a74ad67f46a770/Untitled%204.png)

### 2. 论文翻译与润色

这里使用一篇论文的节选片段交给它来进行翻译：

![Untitled](GPT-Academic%E4%BD%BF%E7%94%A8%E4%BD%93%E9%AA%8C%20bbf038e99cf043e883a74ad67f46a770/Untitled%205.png)

翻译结果如下，个人感觉与ChatGPT的翻译结果相比优势并不明显

![Untitled](GPT-Academic%E4%BD%BF%E7%94%A8%E4%BD%93%E9%AA%8C%20bbf038e99cf043e883a74ad67f46a770/Untitled%206.png)

再要求它将翻译后的片段进行润色，得到润色结果：

![Untitled](GPT-Academic%E4%BD%BF%E7%94%A8%E4%BD%93%E9%AA%8C%20bbf038e99cf043e883a74ad67f46a770/Untitled%207.png)

润色的效果还是很明显的：句子更加通顺、用词更加准确，可读性增强明显。

## 优势

1. 功能多样、插件丰富
2. 有UI，用户交互体验好，指引明确
3. 支持latex格式，可以用公式讲解学术或理论知识