
与 ChatGPT 互动几轮后，可以让他把问答过程整理成一篇推文 (或笔记)。使用如下提示词可以让 ChatGPT 自动生成推文的标题和关键词：

&emsp;

--- - --

```md
User： 
 1. 请帮我拟定 10 个备选的推文标题，分成 2-3 中不同的风格；
 2. 在 **Keywords**: 部分补充推文中的关键词。
    标题中已经出现的关键词不必列入；
    关键词主要是推文中提及次数较多的命令、模型名称、计量方法等；
    关键词之间用半角逗号分开。
  
要求：只需输出如下两行即可，正文不必重复输出   
- **Title**: xxx
- **Keywords**: k1, k2, k3, ...
```
