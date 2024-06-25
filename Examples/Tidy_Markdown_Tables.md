---
Title: Tidy Markdown Tables
Author: Yujun Lian, ChatGPT 4o
Date: 2024/6/24 23:12
---

<br>

> 原始对话记录：[click](https://chatgpt.com/share/0c64bafa-5ab1-454d-b5fc-3143884d972a)，`2024/6/24 22:38`


--- - --


>### 提示词 1：

```Markdown 
帮我把这个表格做成宽表，共四列：
| Abbreviation | Command     |
| ------------ | ----------- |
| `br`         | `browse`    |
| `tw`         | `twoway`    |
| `dis`        | `display`   |
| `des`        | `describe`  |
| `gen`        | `generate`  |
| `gr`         | `graph`     |
| `mat`        | `matrix`    |
| `reg`        | `regress`   |
| `lab`        | `label`     |
| `sum`        | `summarize` |
| `tab`        | `tabulate`  |
| `bys`        | `bysort`    |
| `qui`        | `quietly`   |
| `noi`        | `noisily`   |
| `cap`        | `capture`   |
| `forv`       | `forvalues` |
| `prog`       | `program`   |
| `hist`       | `histogram` |
```

--- - --

#### ChatGPT 回答 1：

```Markdown 
可以将这个表格转换成宽表格式，共四列：

| Abbreviation | Command     | Abbreviation | Command     |
| ------------ | ----------- | ------------ | ----------- |
| `br`         | `browse`    | `reg`        | `regress`   |
| `tw`         | `twoway`    | `lab`        | `label`     |
| `dis`        | `display`   | `sum`        | `summarize` |
| `des`        | `describe`  | `tab`        | `tabulate`  |
| `gen`        | `generate`  | `bys`        | `bysort`    |
| `gr`         | `graph`     | `qui`        | `quietly`   |
| `mat`        | `matrix`    | `noi`        | `noisily`   |
| `cap`        | `capture`   | `forv`       | `forvalues` |
| `prog`       | `program`   | `hist`       | `histogram` |

这样表格就被整理成了四列宽表。
```

&emsp;

>### 提示词 2：

`请按 a-z 顺序呈现；第二列右侧插入一个空列`

--- - --

#### ChatGPT 回答2：

```Markdown 
按 a-z 顺序呈现，并在第二列右侧插入一个空列：

| Abbreviation | Command     |       | Abbreviation | Command     |
| ------------ | ----------- | ----- | ------------ | ----------- |
| `br`         | `browse`    |       | `lab`        | `label`     |
| `bys`        | `bysort`    |       | `mat`        | `matrix`    |
| `cap`        | `capture`   |       | `noi`        | `noisily`   |
| `des`        | `describe`  |       | `prog`       | `program`   |
| `dis`        | `display`   |       | `qui`        | `quietly`   |
| `forv`       | `forvalues` |       | `reg`        | `regress`   |
| `gen`        | `generate`  |       | `sum`        | `summarize` |
| `gr`         | `graph`     |       | `tab`        | `tabulate`  |
| `hist`       | `histogram` |       | `tw`         | `twoway`    |

这样表格按照字母顺序排列，并在第二列右侧插入了一个空列。
```
输出效果：
| Abbreviation | Command     |       | Abbreviation | Command     |
| ------------ | ----------- | ----- | ------------ | ----------- |
| `br`         | `browse`    |       | `lab`        | `label`     |
| `bys`        | `bysort`    |       | `mat`        | `matrix`    |
| `cap`        | `capture`   |       | `noi`        | `noisily`   |
| `des`        | `describe`  |       | `prog`       | `program`   |
| `dis`        | `display`   |       | `qui`        | `quietly`   |
| `forv`       | `forvalues` |       | `reg`        | `regress`   |
| `gen`        | `generate`  |       | `sum`        | `summarize` |
| `gr`         | `graph`     |       | `tab`        | `tabulate`  |
| `hist`       | `histogram` |       | `tw`         | `twoway`    |
