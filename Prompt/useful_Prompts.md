
## 产生提示词的提示词

```raw
我想把一份英文书稿翻译成中文，想要表达的比较地道，
而且保持原文的格式，比如说元括号用半角模式等等，
你能不能帮我写一个比较好的提示词？
```

## 给答案自动加标签

```raw
-- round 1 --
注意：每次生成答案时，都在首行按如下格式添加 label，以便我追问时定位。
'mylabel-01'
'mylabel-02'

-- round 2 --
按如下要求修改 'mylabel01' 的内容：
1. xxx
2. xxx

-- round 3 -- Note: 我试了几次，都不成功
帮我把 'mylabel-01'，'mylabel-03'，'mylabel-08' 的内容整合在一起，形成一篇完整的文档。

输出为 .md 格式。
```


## 论文推介
- [推介1：Du-2023-EE](https://chatgpt.com/share/680b7bbb-f720-8005-a9a6-bf2793d01f8d)
- [推介2：Seo-2019-xthenreg-SJ](https://chatgpt.com/share/680bb871-42a8-8005-a34c-4de00d342bf7)

```raw
---Round 1---
[以附件形式上传论文]

写一篇论文推介，介绍附件中的论文。先列个提纲给我。

Note: 你可以对 AI 提供的提纲进行修改。

---Round 2---
分批次输出吧
1. 计量模型的证明和详细推导过程可以省略，但要补充简单直白的语言来解释模型和参数的经济含义
2. 把数学符号和公司都采用 Latex 格式来写，以保证输出美观
3. 行内公式采用 $f=x$ 格式，单行公式采用 $$f=x$$ 格式
4. 所有括号都用半角模式，中英文混排注意加空格
5. 不要添加如何表情符号
6. 按 '## 1. xxx'，'### 1.1 xxx'，'#### xxx'(不编号) 的等格式来分 Section, Subsection, Subsubsection
7. 参考文献格式：
   - xxx, xxx, xxx. (**2023**). xxx. *Journal of xxx*, 1(1), 1-10. [Link](https://doi.org/{DOI}), [-PDF-](http://sci-hub.ren/{DOI}), [Google](<https://scholar.google.com/scholar?q={Title of the Paper}>).
8. 注意：每次生成答案时，都在首行按如下格式添加 label，以便我追问时定位：'mylabel-01'，'mylabel-02'，……

-- Round 3---

请帮我把 mylabel-01 至 mylabel-06 的内容整合为一个完整的 .md 文档。不要做任何删减和格式调整。 

```



```raw
写一篇笔记，介绍这篇论文。
1. 简介。文章摘要翻译，主要结论等
2. 研究方法。重点介绍文中使用的 [xxx model] 的设定；关键变量的界定和含义等
3. 实证结果分析 (主要分析 [xxx] 相关的内容即可，其它的内容简要介绍即可)

---
提炼 Section 2 的内容，重点介绍 2.3. Hypotheses
1. 不要添加任何表情符号
2. 中英文混排加空格
3. 语言朴实，逻辑清晰

--- 
完整介绍论文的 [Section #. Methodology]
```

## 参考文献格式

```raw
用法：提供一些文献的基本信息给 AI，然后写如下提示词

-- Format 1 --
按如下格式输出参考文献：
- xxx, xxx, xxx. (**2023**). xxx. *Journal of xxx*, 1(1), 1-10. [Link](https://doi.org/{DOI}), [-PDF-](http://sci-hub.ren/{DOI}), [Google](<https://scholar.google.com/scholar?q={Title of the Paper}>).

-- Format 2 --
按 'MLA' 格式输出参考文献，参考：
- Allcott, Hunt, Matthew Gentzkow, and Lena Song. "Digital addiction." American Economic Review 112.7 (2022): 2424-2463. [Link](https://doi.org/{DOI}), [-PDF-](http://sci-hub.ren/{DOI}), [Google](<https://scholar.google.com/scholar?q={Title of the Paper}>).

-- Format 3 --
按 'APA' 格式输出参考文献，参考：
- Allcott, H., Gentzkow, M., & Song, L. (2022). Digital addiction. American Economic Review, 112(7), 2424-2463. [Link](https://doi.org/{DOI}), [-PDF-](http://sci-hub.ren/{DOI}), [Google](<https://scholar.google.com/scholar?q={Title of the Paper}>).
```

## 格式调整

```raw
更新如下文本：
1. 内容不要改动
2. 把数学符号和公司都采用 Latex 格式来写，以保证输出美观
3. 行内公式采用 $f=x$ 格式，单行公式采用 $$f=x$$ 格式
4. 所有括号都用半角模式，中英文混排注意加空格

---
贴入待处理的文本

```

### 括号和空格

```raw
文中的括号全部使用半角模式，注意中英文混排时加空格。
后文的修改都按此要求。
```

## 翻译

以下是一个**适用于 ChatGPT、DeepSeek、Claude 等 AI 工具**的高质量提示词（prompt），可用于将英文书稿翻译为**格式规范、表达地道、风格统一的中文文本**，特别适合学术、技术类文稿的翻译任务。

```raw
你是一个专业的中英翻译专家，
擅长将英文书稿翻译为「符合中文表达习惯的地道中文」。
你的任务是将我提供的英文原文翻译成中文，要求如下：

1. **忠实原意，语言通顺自然**，避免直译痕迹；
2. **保留原文的格式结构**，包括：
   - 段落结构与编号；
   - 标题格式（如 Heading 层级）；
   - 括号、引号、逗号、句号等使用**半角符号**；
   - 如果原文有 Markdown 或 LaTeX 格式，请保留；
3. **技术术语、专有名词**准确翻译，必要时可加括号注明英文原文；
4. **举例说明、程序代码等保留原样**，必要时可在代码上方用简短中文注释进行解释；
5. 翻译风格参考中文学术教材或技术手册，**简洁明了，符合中文读者习惯**；
6. 如遇难以翻译的句子或不确定的地方，用中括号标注出原文，如：[原文：...]
7. 不要省略或增补原文信息，**除非明确指示**。

=======

**现在请将以下英文段落翻译为符合上述要求的中文：**

(贴入需要翻译的文本)
```


## 让 AI 写讲义

**Tips**
- 先让它列提纲
- 再让它分批次输出各个章节 (否则它给出的内容过于简单)
- 如果要规定字数，一定要说是 `## 个汉字`，最好明确写出字数上下限，不要用 `2000 字左右` 这种模糊说法。
- [ChatGPT-生成正则表达式讲义](https://chatgpt.com/share/680a54a4-1174-8005-bedc-b101549ad45b)

```raw
写一份讲义，介绍 Python 中的正则表达式。
你先列个提纲给我，附上必要的参考资料。

- 读者：Python 初学者
- 语言：中文
- 目标：学完后能进行基本的静态网页爬虫
- 预期字数：6 个 Sections, 每个 Section 2000-2500 汉字
```

## 生成论文或推文标题

```raw
帮我列出15~20个备选的推文题目

用 [xxx] 作为关键词，帮我拟定 10 个推文标题，要能吸引眼球，我要通过公众号发布
```

[Sample-对话的尾部](https://chatgpt.com/share/67f11fc5-b1a0-8005-b559-c479ffbad641)