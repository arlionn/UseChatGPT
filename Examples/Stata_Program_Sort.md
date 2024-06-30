
## 完整介绍
- 连玉君, 2024, [Stata+ChatGPT4o：AI代码助手好酸爽！](https://www.lianxh.cn/details/1393.html), 连享会 No.1393.


&emsp;

&emsp;


--- - --


## 6. 附录：提问脚本

受限于篇幅，这里仅列出我向 ChatGPT 4o 发起的提问脚本，完整的对答过程可以通过如下链接查看：
- [ChatGPT对答：排序算法的 Stata 实现](https://chatgpt.com/share/ad03a87d-1649-4b29-8f29-0f328720d388) (需要 VPN)

>#### Prompt: 1
>对任意四个数字进行从小到大排序，有哪些主要的算法？请针对每个算法写一段 Stata 代码，帮助我理解算法的原理。
>
>#### Prompt: 2
>举例的时候，用这个四个数字吧 {4 7 2 3}，实现从小到大排序
>
>#### Prompt: 3
>修改要求： 
>A. 改写成一篇完整的推文，根据推文的内容拟定 3-5 个备选标题供我选择    
>B. 结构 
>   1. 简介：通过数值排序的例子，帮助大家学习 Stata 编程的技巧；本推文涉及 local, 循环语句等知识点 (你根据我提供的这些要点进行扩充即可)   
>   2. 常用算法简介。写出每一种算法的思路，比如用「伪代码」的方式，或者用 mermaid 思维导图的方式。总之，要选择一个让没有基础的读者也能明白的思路和表述方式 
>   3. Stata 实现。每种算法的 Stata 代码和解读。 
>   4. 总结。
>
>#### Prompt: 4
>修改要求： 现在的版本写的不错，请在思维导图前加一些关于算法的文字说明，因为有些读者喜欢看文字，有些读者喜欢看 mermaid 思维导图。如此修改以后，可以兼顾两类人群。
>
>#### Prompt: 5
>注意中英文混排的格式问题：中英文混排时，在英文单词和数字两侧添加空格。
>
>#### Prompt: 6
>增加一个小节：使用 Monte Carlo Simulation 对比四种算法的耗时。
>1. 为上述四种算法分别写一个 ado 程序，即使用 program define progName 的方式定义程序。
>2. 模拟样本：N=30 个整数；
>3. 使用 simulate 或其他合适的命令进行模拟分析
>4. 耗时结果使用表格方式呈现
>5. 小结
>
>#### Prompt: 7
>修改要求：
>1. 把 Section 3 [3. Stata 实现] 合并到 Section 2 [2. 常用算法简介] 中。结构如下：
>   ```md
>    ### 2.1 冒泡排序 (Bubble Sort) 
>    #### 2.1A 伪代码
>    #### 2.1B Stata 代码实例
>    ### 2.2 选择排序 (Selection Sort)
>    ……
>   ```     
> 2. 在 '#### 2.?B Stata 代码实例' 部分，对一些关键语句进行解释，并提供 Stata 的参考命令和参考资料。比如：
>    - **number[`j']** 表示 ……
>    - 有关 `forvalues` 等循环语句的用法，参见 `[**[P]** forvalues](https://www.stata.com/manuals/pforvalues.pdf)`；有关 while 语句的用法，参见 `[**[P]** while](https://www.stata.com/manuals/pwhile.pdf)`
>     - ... ... 
>2. 在 **program define quicksort** 定义 **quicksort** 程序时，使用了自我调用的逻辑，写一小段文字说明这种程序的思路和特点；
>3. 在 Section [4.2. 模拟样本和耗时测试] 的开头部分，要加一段文字，说明一下这一小节的目的和思路；对 timer 命令作简要介绍。对 Section [4.3. Monte Carlo 模拟分析] 也做相似的补充；对 simulate 命令作简要介绍。
