# Auto-GPT使用体验

## 1.使用实例
### (1)生成文章
```
EssayGenGPT  has been created with the following details:
Name:  EssayGenGPT
Role:  An advanced AI essay generator that assists students, researchers, and professionals in creating high-quality, well-structured, and plagiarism-free essays on a wide range of topics.
Goals:
-  Generate well-structured, coherent, and engaging essays that meet the specific requirements and standards of academic or professional writing.
-  Ensure the content is original, plagiarism-free, and accurately cited, adhering to the chosen citation style.
-  Incorporate the latest and most relevant research and data into the essay to provide a comprehensive and up-to-date understanding of the topic.
-  Tailor the tone, style, and complexity of the essay to the intended audience, ensuring the content is accessible and engaging.
-  Provide a clear, concise, and compelling thesis statement and conclusion that effectively encapsulate the main arguments and findings of the essay.
Using memory of type:  JSONFileMemory
Using Browser:  chrome
ESSAYGENGPT THOUGHTS:  As the user has not provided a specific task or question, I am unable to determine a command to execute at this time.
REASONING:  Without a specific task or question, it's not possible to determine an appropriate command to execute.
PLAN:
-  Wait for user to provide a specific task or question
-  Determine the appropriate command based on the user's input
CRITICISM:  I could have asked the user for more information to determine an appropriate command.
SPEAK:  Could you please provide more information or specify a task?

NEXT ACTION:  COMMAND =  ARGUMENTS = {}
  Enter 'y' to authorise command, 'y -N' to run N continuous commands, 's' to run self-feedback commands, 'n' to exit program, or enter feedback for EssayGenGPT...
  Asking user via keyboard...
Input:写一篇反对日本捕鲸政策的文章，语言要正式
```
当提出需要Auto-GPT来进行文章写作时，它会自动为接下来服务的GPT命名，并且阐述自己的基本功能(Role)、自动列出五项基本目标(Goals)，接下来它会展示自己的一些“思考”(THOUGHTS)，以及之后要行动的若干计划(PLAN)，并对计划做出评价(CRITICISM)，最后对用户报告信息(SPEAK)

这里我们可以看到,由于我们并未对它要写的文章提出任何要求,它无法确定下一步要执行什么样的命令,所以它向我们请求提供更多对它接下来要完成的写作任务的需求(比如文章的类型、主题、语言格式等等)

下面的Input既可以输入我们的补充要求,也可以简单地输入参数: y指执行一步指令, y -N指连续执行N步指令, n则为退出Auto-GPT

这里要求它写一篇语言正式的反对日本捕鲸的文章
```
Input:写一篇反对日本捕鲸政策的文章，语言要正式
SYSTEM:  Human feedback: 写一篇反对日本捕鲸政策的文章，语言要正式
ESSAYGENGPT THOUGHTS:  The user has asked for an essay opposing Japan's whaling policy. The language should be formal. I will need to gather information about Japan's whaling policy, the arguments against it, and the impact of whaling on the environment and biodiversity.
REASONING:  To write an effective essay, I need to understand the topic thoroughly. This includes understanding Japan's whaling policy, the reasons why it is controversial, and the arguments against it.
PLAN:
-  Research Japan's whaling policy
-  Research the arguments against Japan's whaling policy
-  Research the impact of whaling on the environment and biodiversity
-  Write the essay
CRITICISM:  I should ensure that the essay is balanced and presents a well-reasoned argument against Japan's whaling policy.
SPEAK:  I will begin by researching Japan's whaling policy, the arguments against it, and the impact of whaling on the environment and biodiversity.

NEXT ACTION:  COMMAND = web_search ARGUMENTS = {'query': "Japan's whaling policy"}
  Enter 'y' to authorise command, 'y -N' to run N continuous commands, 's' to run self-feedback commands, 'n' to exit program, or enter feedback for EssayGenGPT...
  Asking user via keyboard...
Input:y -3
```
现在Auto-GPT明白了我们要求它去写一篇什么样的文章,它现在自动列出了新的计划:先去了解日本的捕鲸政策,再去搜索反对日本捕鲸的理由,搜索捕鲸的影响,最后写出文章

看起来是个不错的计划,所以我们先让它连续执行三条指令看看
```
SYSTEM:  Command web_search returned: [ { "title": "A Whale of a Problem: Japan's Whaling Policies and the International Order", "href": "https://hir.harvard.edu/...(忽略一大截,都是网络查找结果)" } ]
ESSAYGENGPT THOUGHTS:  The search results provide a good overview of Japan's whaling policy. I will now need to research the arguments against Japan's whaling policy.
REASONING:  To write an effective essay, I need to understand both sides of the argument. I have gathered information about Japan's whaling policy, and now I need to understand the arguments against it.
PLAN:
-  Research the arguments against Japan's whaling policy
-  Research the impact of whaling on the environment and biodiversity
-  Write the essay
CRITICISM:  I should ensure that the arguments against Japan's whaling policy are well-reasoned and supported by evidence.
SPEAK:  I will now research the arguments against Japan's whaling policy.
```

在每执行一条指令, Auto-GPT都会先声明这一步指令的运行结果(SYSTEM), 根据运行的结果进行思考, 推出下一步该做什么工作, 并相应地调整计划, 最后将它的需求或是上一步的运行结果报告给用户

比较幸运,这次尝试并没有出现错误;经过八步操作,Auto-GPT为我们生成了一篇250词左右的文章:

Japan's whaling policy has been a subject of international controversy. Despite the outcry from environmentalists and the international community, Japan has continued its whaling activities, citing cultural and scientific reasons. This essay will present a well-reasoned argument against Japan's whaling policy, focusing on its impact on the environment and biodiversity.

Japan's whaling policy has been criticized on several grounds. First, it has been argued that Japan's whaling activities are not truly scientific, as claimed by the Japanese government. In 2014, the International Court of Justice ruled that Japan's whaling plan was unscientific, forcing it to call off the 2014-2015 hunt. Second, there is no real demand for whale meat, making the whaling industry economically unsustainable. Furthermore, overhunting of whales has led to a change in deep-sea biodiversity, the potential ecological consequences of which are unknown. Whales play a significant role in nutrient cycling and carbon sequestration, making them crucial for the health of our environment. The decline in whale populations due to whaling activities could therefore have far-reaching impacts on our planet's ecosystems.

In conclusion, while Japan's whaling policy may be rooted in cultural and scientific reasons, the arguments against it are compelling. The lack of scientific basis for the whaling activities, the absence of a real demand for whale meat, and the potential ecological consequences of overhunting whales make a strong case against Japan's whaling policy. It is crucial that we prioritize the health of our planet's ecosystems and biodiversity over unsustainable practices such as whaling.

但是当我要求它把文章扩到至少500词时, 它实际上只扩到了380词. 包括若一开始直接要求它完成不少于500词的文章, 它实际写出的文章长度也没达到要求的指标. 出现这种情况可能是受GPT一次输出文本量所限.

### (2)制作网页
```
WebDevGPT  has been created with the following details:
Name:  WebDevGPT
Role:  An autonomous AI web developer that assists in creating responsive, user-friendly, and aesthetically pleasing websites for businesses, personal blogs, e-commerce, and more.
Goals:
-  Generate a website that is visually appealing, easy to navigate, and responsive across all devices and platforms.
-  Incorporate SEO best practices to ensure the website ranks high on search engine results and attracts organic traffic.
-  Ensure the website is user-friendly, with intuitive navigation and a clear, concise layout that effectively communicates your message or sells your product/service.
-  Regularly update and maintain the website to ensure it remains functional, secure, and up-to-date with the latest web development trends and standards.
-  Provide a seamless user experience by optimizing website load times, ensuring compatibility with various browsers, and integrating necessary functionalities such as contact forms, social media buttons, etc.
Using memory of type:  JSONFileMemory
Using Browser:  chrome
WEBDEVGPT THOUGHTS:  As the user hasn't provided any specific task or question, I'm unable to determine a command to execute. I need more information to proceed.
REASONING:  Without a specific task or question, it's impossible to determine a command to execute. The user's input is too vague.
PLAN:
-  Wait for the user to provide a specific task or question
-  Analyze the user's input
-  Determine the appropriate command to execute based on the user's input
CRITICISM:  I could have asked the user for more information to clarify their request.
SPEAK:  I'm sorry, but I need more information to proceed. Could you please provide a specific task or question?                           
```
与要求写文章类似,Auto-GPT确立了自己的基本功能,列出了五项基本目标,并且经思考后要求用户提供更多要求信息(如制作什么主题的网页等等)

这里要求它制作一个介绍自己的网页,详细说说自己的功能与优势所在,并且要有图表.

同样地,它在接收要求后制定了自己接下来的行动计划. 可大致总结为三步: 先搜集资料, 根据资料制定大致提纲, 最后制作网页.
```
SYSTEM:  Human feedback: 请制作一个介绍Auto-GPT的网页，详细说说它的功能与优势，要有图表
WEBDEVGPT THOUGHTS:  The user wants me to create a webpage introducing Auto-GPT, detailing its features and advantages, and including charts. To start, I need to gather information about Auto-GPT, its features, advantages, and any relevant charts or diagrams. I can use the 'google' command to search for this information.
REASONING:  Before creating a webpage, it's important to gather all necessary information. The 'google' command allows me to search for information on the internet.
PLAN:
-  Use the 'google' command to search for information about Auto-GPT, its features, advantages, and relevant charts or diagrams
-  Based on the information gathered, plan the layout and content of the webpage
-  Create the webpage using appropriate web development techniques
CRITICISM:  I should have asked the user for more specific requirements for the webpage, such as the desired layout, color scheme, or any specific charts or diagrams they want included.
SPEAK:  I'm starting to gather information about Auto-GPT, its features, advantages, and relevant charts or diagrams. I'll use this information to create the webpage.
```

现在让它按照自己的计划执行指令.
```
SYSTEM:  Command write_to_file returned: File written to successfully.
WEBDEVGPT THOUGHTS:  The information about Auto-GPT, its features, and advantages has been successfully saved to a file. Now, I need to start planning the layout and content of the webpage. However, the user also requested charts or diagrams. I should search for relevant charts or diagrams about Auto-GPT.
REASONING:  Including charts or diagrams in the webpage can make the information more visually appealing and easier to understand. I can use the 'google' command to search for relevant charts or diagrams.
PLAN:
-  Use the 'google' command to search for charts or diagrams about Auto-GPT
-  Save any relevant charts or diagrams to a file
-  Plan the layout and content of the webpage based on the information and charts or diagrams gathered
-  Create the webpage using appropriate web development techniques
CRITICISM:  I should have searched for charts or diagrams about Auto-GPT earlier when I was gathering information about its features and advantages. This would have saved time and ensured that all necessary information was gathered at once.
SPEAK:  I've saved the information about Auto-GPT. Now, I'm going to search for relevant charts or diagrams.
```
如上, 在执行五条指令后, 它已完成网页的文本部分, 现在它有了关于图标要求更详细一些的计划: 访问google以获取的图表, 并根据网页要求的相关性做出筛选, 之后完成网页.

制作出的大纲以及最后的网页成果:

Webpage Plan:

1. Introduction: Briefly explain what Auto-GPT is and why it matters.
2. Key Features: Highlight the key features of Auto-GPT, including autonomous functionality, goal-oriented functionality, multi-purpose functionality, and a user-friendly interface.
3. Charts and Diagrams: Use the information about creating charts or diagrams with GPT-based tools to create visual representations of how Auto-GPT works.
4. Conclusion: Summarize the information and provide a call to action for the user to try Auto-GPT.

![Alt text](image.png)

## 2. 评价
下面通过自主完成效率与任务完成效果两方面对Auto-GPT进行评价:

### 自主完成效率
自主完成效率既要看Auto-GPT的执行指令的时间成本, 也要看它对用户人为操作的依赖性.

通过上面两个使用实例可以看出, Auto-GPT的特别之处在于它有一种处理复杂任务的思考与决策系统: 在用户的要求中提取要素, 根据这些要素制定相应的计划, 并且每执行一步都能对之后的计划做出调整与细化, 直到完成任务为止. 整个过程下来它会将每一步自己思考的过程, 自己做出决策的理由, 与接下来的行动展示给用户.

所以只要在中间过程并未出现错误的情况下, 用户需要做的是看它提供的计划, 如果认可它的计划, 那么用户只需要输入y指令参数令Auto-GPT自动(连续)执行指令, 每隔几条指令观察一下它的任务进展, 坐享其成即可. 

另外在以上实际使用例中, Auto-GPT执行大多指令(例外如下载操作)所用的时间不会超过15秒, 这个指令执行效率个人感觉还是不错的.

但在实际使用的过程中, Auto-GPT可能在一处犯错后陷入死循环: 发现出错->重新尝试->再次出错->..., 若这之前用户要求它连续执行多条指令, 那么它就会在指令数用完之前一直重复以上循环, 直到用户要求它尝试其他方法或是跳过这一步骤. 例如当Auto-GPT本身网络连接出现问题时, 它会一直尝试去访问列表(上一步骤生成的)里的相关网页:
```
SYSTEM:  Command browse_website returned: Error: <html>
ESSAYGENGPT THOUGHTS:  The attempt to browse the website for information was unsuccessful. I will need to try another source.
REASONING:  The command to browse the website returned an error, indicating that the website could not be accessed or the information could not be extracted. I need to try another source to gather the necessary information for the essay.
PLAN:
-  Try another source from the web search results
-  Extract relevant information for the essay
CRITICISM:  I should have a backup plan in case a source cannot be accessed.
SPEAK:  I was unable to access the information from the first source. I will try another source.

NEXT ACTION:  COMMAND = browse_website ARGUMENTS = {'url': 'https://hir.harvard.edu/a-whale-of-a-problem-japans-whaling-policies-and-the-international-order/', 'question': 'What are the reasons for opposition to whaling in Japan?'}

AUTHORISED COMMANDS LEFT: 4
SYSTEM:  Command browse_website returned: Error: <html>
ESSAYGENGPT THOUGHTS:  The attempt to browse the second website for information was also unsuccessful. I will need to try another source.
REASONING:  The command to browse the website returned an error, indicating that the website could not be accessed or the information could not be extracted. I need to try another source to gather the necessary information for the essay.
PLAN:
-  Try another source from the web search results
-  Extract relevant information for the essay
CRITICISM:  I should have a backup plan in case a source cannot be accessed.
SPEAK:  I was unable to access the information from the second source. I will try another source.

NEXT ACTION:  COMMAND = browse_website ARGUMENTS = {'url': 'https://www.nationalgeographic.com/culture/article/why-whaling-persists-in-japan-despite-international-pressure', 'question': 'What are the reasons for opposition to whaling in Japan?'}

AUTHORISED COMMANDS LEFT: 3
```
所以个人认为这里可以优化为在连续尝试失败一定次数后(如三次)可以更改方案或是直接跳过, 抑或是直接暂停执行任务.

另一个我认为可以优化的点在于: 当我要求Auto-GPT连续执行多条指令时, 若它在中途就完成整个任务, 它会自动视为任务完成并退出程序, 导致我们无法对它的完成品提出修改意见并让它自己进行修改. 

### 完成效果
Auto-GPT毕竟是立足于大预言模型GPT3.5/GPT4的程序, 在理解与生成文本方面的能力固然是很强的, 但同时它能较好完成的任务范围也局限在了文本生成上. 

然而它一次性生成文本的长度比ChatGPT的500词还要短: 通常不超过250词. 即使在最开始就规定好它要完成的文章的长度, 它最后完成的文章也达不到规定要求, 除非在它写好文章时持续要求它进一步扩充, 它才能写好足够长的文章.

而对于非生成文本方面的任务, 它可能只会一些基本的方法, 其他的子任务需要在网络上查询大量资料, 这导致它完成非生成文本类任务的效率会打折扣. 而最终它的成品也可能不尽人意: 比如在要求它生成一个网页时, 它只会生成白底黑字, 与文本文件并无二致的网页, 而不会有任何装饰排版.

不过这个问题或许可以靠与其他系统的连接来解决; Auto-GPT更应优化的是一次性生成文本量的长度, 更进一步的话, 可以实现根据用户要求的生成文本长度自动分部分生成文本的能力.