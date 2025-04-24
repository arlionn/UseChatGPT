
> **作者：** 连玉君 (中山大学)    
> **邮箱：** <arlionn@163.com> 

&emsp;

- **Title**: 如何借助 AI 工具来伴读一篇理论类的论文？
- **Keywords**: 理论模型, AI 工具, ChatGPT, 寇宗来, 调整成本函数

&emsp; 

今天，我们来分享一下，我是如何借助 AI 工具来伴读一篇理论类的论文的。今天读的论文不算太难：

> 寇宗来、毕睿罡、查存. (2020). 融资约束对企业广告和研发策略的影响：理论与经验证据. 《世界经济》, 43 (4), 28–51. [Link-PDF](https://manu30.magtech.com.cn/sjjj/CN/Y2020/V43/I4/28)  
- 内容提要：广告有助于扩大产品的市场份额，研发则可以提高产品的利润加成，故两项活动都是企业提升绩效的主要途径。尽管既有文献分别考察了融资约束对企业广告和研发活动的抑制作用，但一个不足之处是忽视了广告和研发之间的互补性及其影响。本文通过一个简单的理论模型表明，给定企业可以同时选择广告和研发，且两者具有功能互补性，则融资约束的小幅变化可能会导致企业在广告和研发策略组合上的＂跳跃性＂变化，故单独考虑广告或研发将有可能低估融资约束的负面影响。基于中国工业企业数据库（2005－2007 年）数据和多项式选择模型的经验检验支持理论分析的主要结论。
- 关键词：融资约束 广告和研发 互补性 多项式选择模型

我开启了两组 ChatGPT 的对话，分别是：
- [ChatGPT提示词 1：伴读一篇理论类的论文](https://chatgpt.com/c/67f8b6cc-9da4-8005-b78d-4c3c03693de0)
- [ChatGPT提示词 2：RD调整成本函数](https://chatgpt.com/share/680a3b68-c180-8005-a2f6-00172b13126f)
  
有兴趣的读者也可以尝试把本文的提示词丢给 [DeepSeek](https://www.deepseek.com/) 或 [豆包](https://www.doubao.com/)，体验不同 AI 工具的表现。

<br>

---

<br>

多数人都不太愿意读理论模型类的论文，尤其是数学模型的设定和推导。然而，理论模型类的文章往往更有深度，也更容易帮助我们抓住某一类问题的本质。

一个好的理论模型往往是作者经过长时间的观察和思考后，去粗取精，提炼出最核心的问题，并从一些基本假设条件出发，利用几个主要的方程 (如预期收益函数、调整成本函数、效用函数)，来描述一个复杂的经济现象。

AI 工具在理解理论模型时有以下几方面的优势：

- **模型梳理能力**：能快速梳理出模型的核心假设和主要方程，帮助我们把握整体框架。
- **通俗解释复杂设定**：能用通俗易懂的语言解释复杂的数学设定，让经济学直觉变得更易理解，尤其对数学基础薄弱的同学非常友好。
- **函数可视化与直观展示**：能生成函数的可视化图形，直观展示不同参数对模型性质的影响。例如：[ChatGPT-RD调整成本函数](https://chatgpt.com/share/680a3b68-c180-8005-a2f6-00172b13126f)。
- **模型扩展与创新辅助**：能辅助我们扩展模型。当我们希望在已有理论框架基础上做出创新，但受限于数学推导能力时，AI 可以帮助完善推导过程，或协助描述更复杂的效用函数、成本函数及其互补或交互效应。此外，AI 还能结合文献检索能力，帮助论证新设定的合理性，减少被审稿人质疑的风险。

下面，我结合我与 ChatGPT 的对话，分别解释上述四个要点。需要说明的是，由于与 ChatGPT 对话过程中我会根据它的反馈多次修改我的提示词，因此，下文中展示的提示词只是我对话过程中一部分内容。




&emsp;

## 1. 模型梳理能力

>❓ **Prompt 1**: 帮我写出这篇论文的理论模型 

  Note: 把论文的 PDF 文件上传到 ChatGPT 中

ChatGPT 会自动识别 PDF 中的文本内容，并提取出论文的理论模型，写成了一份 2000 字左右的简化版的理论模型。他的总结能力很强，把模型研究假设，主要方程的设定思路，模型的经济学直觉都提炼出来了。

完整回复参见：[ChatGPT-Prompt1-Answer](https://github.com/arlionn/UseChatGPT/blob/main/Examples/read_Paper_theory_outline.md)

&emsp;

## 2. 通俗解释复杂设定

>❓ **Prompt 2**: 补充一些「大白话」版本的解释，让学生能够理解复杂设定背后的经济学直觉。

✅ **ChatGPT 答复 (截取部分内容)**：

  ![20250424202114](https://fig-lianxh.oss-cn-shenzhen.aliyuncs.com/20250424202114.png)

   ![20250424202504](https://fig-lianxh.oss-cn-shenzhen.aliyuncs.com/20250424202504.png)

&emsp;

## 3. 参数含义和函数可视化

>❓ **Prompt 3**：解释  "且 γ>1  表示研发投入难度高于广告投入" 的含义，以及该表述的依据和合理性。还有没有其它更合理的设定方式？

✅ **ChatGPT 答复 (有删减)：**

>在模型中提到的“且 $\gamma > 1$ 表示研发投入难度高于广告投入”的含义和依据，主要是从**边际成本**的角度来解释研发投入的难度与广告投入的差异。下面我会逐步解释这个表述的含义，以及该表述的合理性和可能的改进方式。
>
>……
>
>虽然在这个模型中，$\gamma>1$ 用来表示研发的边际成本随着投入增加而上升，并且研发难度高于广告，这个设定合理且常见，但也可以考虑以下几种可能的改进方式：
>
>- **更细致的研发成本函数**：  
>  目前的研发成本函数是一个简单的凸函数，假设研发的成本随投入不断上升。实际上，研发的成本曲线可以根据不同领域有所不同。如果考虑到不同类型的研发活动（如基础研发、应用研发等），可能需要更加复杂的成本结构。例如，某些研发领域可能在初期投入时边际成本较低，但随着技术的突破和进展，成本呈现加速上升的趋势。可以考虑使用分段函数或者带有更多非线性项的函数来描述研发成本。
>
>  例如：
>
>  $$
>  I(r) = \frac{\gamma r}{1 - r} + \beta r^2
>  $$
>
>  其中， $\beta$ 可以进一步调整研发投入的加速效应。
>
>- **引入广告的非线性成本函数**：  
>  如果想进一步调整广告成本的设定，可以考虑广告的成本随市场接近饱和而加速增长。比如，广告投入的边际成本并不总是平缓增加，可以设置一个逐渐增大的函数，使广告的投资成本也能体现出“递减的边际效益”。例如，广告成本可以设为：
>
>  $$
>  A(a) = \frac{(m_0 + a)^2}{1 - (m_0 + a)} - \frac{m_0^2}{1 - m_0}
>  $$
>
>  这样可以让广告成本在高市场占有率下的边际增长加速，从而与研发成本更好地对比。

函数可视化部分参见本文：**5. 附录：ChatGPT 生成的代码和图形**。

&emsp;

## 4. 模型扩展与创新辅助

>❓ **Prompt 4.A**：
> 新问题：
>我想修改寇宗来老师这篇论文中研发调整成本函数的设定。基本想法是：$I(r)$ 不但收到 $r$ 的影响，也会受到企业市场规模的影响，市场规模越大，$I(r)$ 应该越高。按此思路，有哪些可能的 $I(r)$ 方程的设定方法，各自的优缺点是什么？

✅ **ChatGPT 答复 (有删减)：** 

- **模型 A：加性规模项** 
 
  $$I(r,m_0)=\frac{\gamma r}{1-r}+\lambda m_0$$  

  - **性质**  
    - 对 $r$ 保持原模型的凸性；对 $m_0$ 线性递增。  
    - $r$ 与 $m_0$ 没有交互；规模大仅平移成本曲线。  
    - 估计简单，适合快速检验规模效应是否显著。  
  - **局限**：无法体现"企业越大，提高 $r$ 越困难"的放大效应。

- **模型 B：乘性缩放项**  
  
  $$I(r,m_0)=(1+\theta m_0)\frac{\gamma r}{1-r}$$ 
  
  - **性质**  
    - $m_0$ 与 $r$ 交互；规模越大，调整 $r$ 的边际成本越陡。  
    - 保持 $r$ 的凸性，只要 $1+\theta m_0>0$。  
    - 直观描述"大企业协调复杂度"随 $r$ 增长被放大。  
  - **局限**：若样本中 $m_0$ 变动幅度大，易造成估计不稳定；需对 $\theta$ 做合理范围约束。

- **模型 C：幂函数交互项**  
  
  $$I(r,m_0)=\kappa r^{\alpha} m_0^{\beta},\qquad \alpha>1$$ 
  
  - **性质**  
    - $r$ 的凸性由 $\alpha$ 控制；$\beta$ 捕捉规模敏感度。  
    - 同时刻画 $r$、$m_0$ 的非线性影响，弹性可解释性强。  
    - 适合连续型 $m_0$，对极端值相对平滑。  
  - **局限**：当 $r\to1$ 时增长不如原式陡峭；需确保 $\alpha,\beta$ 具备清晰经济含义。

- **模型 D：分段规模溢价**  
  
  $$I(r,m_0)=\frac{\gamma r}{1-r}+\mu\max\{0,m_0-m_0^*\}$$  
  
  - **性质**  
    - 当 $m_0\le m_0^*$ 与原式一致；超过阈值后成本按 $\mu$ 线性上升。  
    - 描述"达到一定规模后，研发协调成本激增"的门槛效应。  
    - 便于做政策/情景分析（如规模上限管制）。  
  - **局限**：函数在 $m_0=m_0^{*}$ 处不可导；阈值 $m_0^{*}$ 需外部确定或额外估计。

- **模型 E：对数规模附加项**  
  
  $$I(r,m_0)=\frac{\gamma r}{1-r}+\eta\ln(1+m_0)$$ 
  
  - **性质**  
    - $\ln(1+m_0)$ 增速递减，缓和大规模企业的极端影响。  
    - 估计便利，可与对数线性回归兼容。  
    - 与 $r$ 的凸性相互独立，便于分离两种效应。  
  - **局限**：仍缺交互放大效应；若需体现"规模×研发"协同成本，需再引入乘性项。

--- - --

>❓ **Prompt 4B**：帮我按优先级排个序吧


**1. 模型B：乘性缩放项**  
`函数形式`：$I(r,m_0)=(1+\theta m_0)\frac{\gamma r}{1-r}$  
- **优势**：直接体现“规模 × 研发”的交互作用，**放大融资约束下的大企业调研难度**；  
- **简洁性**：仅新增 1 个参数，保留原函数凸性，易于估计与解释。  

**2. 模型C：幂函数交互项**  
`函数形式`：$I(r,m_0)=\kappa\, r^{\alpha}\, m_0^{\beta},\;\alpha>1$  
- **灵活性**：同时刻画 $r$ 和 $m_0$ 的非线性弹性，可检验规模弹性异质性；  
- **局限性**：复杂度略高于模型B，且 $r\to1$ 时陡峭度不足。  

**3. 模型A：加性规模项**  
`函数形式`：$I(r,m_0)=\frac{\gamma r}{1-r}+\lambda m_0$  
- **适用场景**：作为**基准稳健性检验**，快速验证“规模是否重要”；  
- **缺陷**：无交互项，解释力较弱。  

(…… 略 ……)

**最终结论：**  
- **B** 在捕捉"规模放大研发难度"方面最直接且参数少，优先。  
- **C** 灵活度高，可深入检验弹性，但复杂度略高，列第二。  
- **A** 作为最简单的规模敏感度检验，放第三。  


---

>❓ **Prompt 4.C**：我选择「模型 B：乘性缩放项」。请以此为基础，帮我重新表述寇宗来文中的模型，并进行后续推导。 

ChatGPT 会把模型的设定、推导过程、经济学直觉等都重新梳理一遍。参见：

[ChatGPT 更新后的模型设定和解读](https://github.com/arlionn/UseChatGPT/blob/main/Examples/read_Paper_theory_new_model.md)

&emsp;

&emsp;

## 5. 附录：ChatGPT 生成的代码和图形

> [ChatGPT提示词：研发调整成本函数的性质](https://chatgpt.com/share/680a3b68-c180-8005-a2f6-00172b13126f)

### A.1 Stata 代码

```stata
clear
set obs 100

* 生成 r 值，避免 r=1 导致除以零
gen r = _n/101

* 计算三组 γ 参数对应的研发成本 I(r)
gen I1 = (1 * r) / (1 - r)
gen I2 = (2 * r) / (1 - r)
gen I5 = (5 * r) / (1 - r)

* 绘制图形
twoway ///
  (line I1 r, lcolor(blue)  lpattern(solid) lwidth(medium)) ///
  (line I2 r, lcolor(red)   lpattern(dash)  lwidth(medium)) ///
  (line I5 r, lcolor(green) lpattern(dot)   lwidth(medium)), ///
  legend(order(1 "γ=1" 2 "γ=2" 3 "γ=5") ///
         ring(0) pos(11)) ///
  xtitle("研发成功概率 r") ///
  ytitle("研发成本 I(r)") ///
  title("不同 γ 下的研发成本函数") ///
  aspect(0.8)  ///
  scheme(cleanplots)

graph export "RD_adjust_costs_01.png", replace width(600)
```

![20250424210004](https://fig-lianxh.oss-cn-shenzhen.aliyuncs.com/20250424210004.png)


--- - --

### A.2 Python 代码

> [read_Paper_theory_python_codes.ipynb](https://github.com/arlionn/UseChatGPT/blob/main/Examples/read_Paper_theory_python_codes.ipynb)

```python
import numpy as np
import matplotlib.pyplot as plt

# 设置中文支持
plt.rcParams['font.family'] = 'SimHei'  # 设置中文字体为黑体
plt.rcParams['axes.unicode_minus'] = False  # 正确显示负号

# 定义 r 值
r = np.linspace(0.001, 0.99, 500)

# γ 参数
gamma_values = [1, 2, 5]
linestyles = ['solid', 'dashed', 'dotted']
colors = ['blue', 'red', 'green']
labels = [r"$\gamma = 1$", r"$\gamma = 2$", r"$\gamma = 5$"]

# 创建图形
plt.figure(figsize=(8, 6))

# 绘图
for gamma, ls, color, label in zip(gamma_values, linestyles, colors, labels):
    I_r = gamma * r / (1 - r)
    plt.plot(r, I_r, label=label, linestyle=ls, color=color, linewidth=2)

# 添加中文标签
plt.title(r"研发成本函数 $I(r) = \frac{\gamma r}{1 - r}$", fontsize=15)
plt.xlabel(r"成功概率 $r$", fontsize=12)
plt.ylabel(r"成本 $I(r)$", fontsize=12)
plt.legend(loc="upper left", frameon=False)
plt.grid(True, linestyle='--', alpha=0.6)

plt.tight_layout()
plt.show()
```

![20250424213227](https://fig-lianxh.oss-cn-shenzhen.aliyuncs.com/20250424213227.png)


&emsp;

## 6. 相关推文

> Note：产生如下推文列表的 Stata 命令为：   
> &emsp; `lianxh ChatGPT deepseek AI, ex(avai AIC sai AIT Plain eba xtnum) md0 nocat`  
> 安装最新版 `lianxh` 命令：    
> &emsp; `ssc install lianxh, replace` 

- [ChatGPT](https://www.lianxh.cn/search.html?s=ChatGPT), 2024, [知乎热议：导师都是段子手](https://www.lianxh.cn/details/1433.html), 连享会 No.1433.
- [于凡](https://www.lianxh.cn/search.html?s=于凡), 2024, [AI可以编写Stata代码吗？](https://www.lianxh.cn/details/1348.html), 连享会 No.1348.
- [余坚](https://www.lianxh.cn/search.html?s=余坚), 2023, [Stata：ChatGPT你能帮我干点啥？](https://www.lianxh.cn/details/1164.html), 连享会 No.1164.
- [吴小齐](https://www.lianxh.cn/search.html?s=吴小齐), 2024, [强大的Kimi：中国版ChatGPT平替](https://www.lianxh.cn/details/1423.html), 连享会 No.1423.
- [罗兰若](https://www.lianxh.cn/search.html?s=罗兰若), 2022, [Stata论文复现：高维线性回归的变量筛选-baing-ocmt](https://www.lianxh.cn/details/866.html), 连享会 No.866.
- [罗银燕](https://www.lianxh.cn/search.html?s=罗银燕), 2023, [如何在 R 中安装并使用 chatgpt 包？](https://www.lianxh.cn/details/1171.html), 连享会 No.1171.
- [连享会](https://www.lianxh.cn/search.html?s=连享会), 2024, [AI编程助手大盘点：不止ChatGPT和Copilot](https://www.lianxh.cn/details/1394.html), 连享会 No.1394.
- [连小白](https://www.lianxh.cn/search.html?s=连小白), 2025, [AI助手系列：napkin.ai-文字转换为图片和表格](https://www.lianxh.cn/details/1540.html), 连享会 No.1540.
- [连小白](https://www.lianxh.cn/search.html?s=连小白), 2025, [AI工具系列：英文学术论文语法检测与纠正](https://www.lianxh.cn/details/1562.html), 连享会 No.1562.
- [连小白](https://www.lianxh.cn/search.html?s=连小白), 2025, [DeepSeek对话可以分享了！](https://www.lianxh.cn/details/1566.html), 连享会 No.1566.
- [连小白](https://www.lianxh.cn/search.html?s=连小白), 2025, [No Chinglish：学术写作中的中式英语陷阱](https://www.lianxh.cn/details/1563.html), 连享会 No.1563.
- [连玉君](https://www.lianxh.cn/search.html?s=连玉君), 2024, [VScode：实用 Markdown 插件推荐](https://www.lianxh.cn/details/1390.html), 连享会 No.1390.
- [连玉君](https://www.lianxh.cn/search.html?s=连玉君), 2024, [从基础到 AI 助手：Python 用户最爱的 VScode 插件清单](https://www.lianxh.cn/details/1489.html), 连享会 No.1489.
- [连玉君](https://www.lianxh.cn/search.html?s=连玉君), 2024, [借助ChatGPT4o学习排序算法：AI代码助手好酸爽！](https://www.lianxh.cn/details/1393.html), 连享会 No.1393.
- [连玉君](https://www.lianxh.cn/search.html?s=连玉君), 2025, [老连买电脑：ChatGPT，DeepSeek，豆包来帮忙](https://www.lianxh.cn/details/1561.html), 连享会 No.1561.
- [连玉君](https://www.lianxh.cn/search.html?s=连玉君), 2023, [连玉君：我与ChatGPT聊了一个月](https://www.lianxh.cn/details/899.html), 连享会 No.899.
- [颜国强](https://www.lianxh.cn/search.html?s=颜国强), 2024, [ChatGPT争议：学术研究的加速器or信任危机的催化剂？](https://www.lianxh.cn/details/1421.html), 连享会 No.1421.
