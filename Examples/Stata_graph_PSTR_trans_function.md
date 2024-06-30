---
Title: Stata Graphing using ChatGPT 4o
Author: Yujun Lian, ChatGPT 4o
Date: 2024/6/30 0:57
---

<br>

> 原始提问过程：[Click](https://chatgpt.com/share/f4b14c93-8d78-4061-8d8d-409ef1f4bc68)

&emsp; 

## Prompt 1
```md
话题标题：用Stata绘制PSTR模型中的转换函数

# 背景： 

如下是面板平滑转换模型 (PSTR) 的介绍：

$$
y_{it}=\mu_i+\beta_0'x_{it}+\beta_1'x_{it}\cdot g(q_{it};\gamma,c)+u_{it}  \quad(1)
$$
其中，$i = 1, ... , N$ ，  $ t = 1, ... , T$，其中$N$ 和 $T$分别表示面板的横截面和时间维度。$y_{it}$ 是因变量，$x_{it}$ 是 $k$ 维外生解释变量，$\mu_i$ 表示固定个体效应，$u_{it}$是误差项。

其中，$g(q_{it};\gamma,c)$ 被称为「转换函数」，$q_{it}$ 是转换变量，$\gamma$ 是平滑参数 (反应转换的速度)，$c$ 是位置参数 (即发生转换的阈值)。

转换函数的表达式如下：
$$
g(q_{it};\gamma,c) = \frac{1}{1+\exp\left[-\gamma(q_{it}-c)\right]}
$$

# 问题：
请写一段 Stata 代码，用 twoway function 绘制转换函数 g(q, \gamma, c) 随着参数 \gamma 和参数 c 的变化特征。
1. 图 1：固定 c=0，将 gamma=0, gamma=0.5, gamma=1, gamma==8 对应的四条函数曲线绘制在一幅图中，保存为 PSTR_trans_01_gamma.png
2. 图 2：固定 gamma=1, c=-2, c=0, c=+2，，保存为 PSTR_trans_02_location.png
```

## Prompt 2
```md
补充修改说明：
1. 使用 scheme(cleanplots)，请预先使用 ssc install 下载该模板
2. 图例中的 gamma=0，能否把 gamma 显示为数学符号的形式 γ 
3. y 轴的数字显示为 0, 0.1, 0.2, ..., 1
4. 标题中加上转换函数的函数表达式
```

### Prompt 3
```stata
继续修改：
1. 用这个：title("PSTR: Transformation Function {it:g}(q; γ, c) with Different γ")。除了 g，其它变量和参数 (q, γ,c) 也要用斜体
2. ytitle 也对照第一条要求修改
3. y 轴的数字的最终显示效果：0, 0.1, 0.2, ..., 1。注意：0.1 不能显示为 .1
4. 所有函数线都用 lp(dash)，用颜色加以区分
5. 横轴取值范围 -6, +6
```

### Prompt 4
```md
继续修改：
1. title 与图形的垂直间距改为目前的 1.5 倍
2. 第二幅图：在 q=0 的位置，增加一条垂直辅助线，选项：lp(dot) lw(*1.8) lc(black*0.8)
3. ylabel 增加选项 format(%2.1f)
```


### Prompt 5
```md
下面是我修改后的 图2 代码，帮我整合在一起。另外，作如下修改：
1. 代码格式美化。同一个代码块内的 '=' 对齐
2. 同一个代码块中，右侧的 '///' 对齐
3. 一些共同出现的选项可以预先存在暂元中，以保证代码简洁，也易于后期维护

-- 图2新代码

// 图 2：位置参数
* 固定 gamma=1，将 c=-2, c=0, c=+2 对应的三条函数曲线绘制在一幅图中
cap drop g_c_*
gen g_c_neg2 = 1 / (1 + exp(-1 * (q - (-2))))
gen g_c_0 = 1 / (1 + exp(-1 * (q - 0)))
gen g_c_pos2 = 1 / (1 + exp(-1 * (q - 2)))

twoway (line g_c_neg2 q, lcolor(blue) lpattern(dash) lwidth(medium)) ///
       (line g_c_0 q, lcolor(red) lpattern(dash) lwidth(medium)) ///
       (line g_c_pos2 q, lcolor(green) lpattern(dash) lwidth(medium)) ///
       (function y=-2, lcolor(black*0.8) lpattern(dot) lwidth(*1.8) horizon range(0.4 0.6)) ///
       (function y= 0, lcolor(black*0.8) lpattern(dot) lwidth(*1.8) horizon range(0.4 0.6)) ///
       (function y=+2, lcolor(black*0.8) lpattern(dot) lwidth(*1.8) horizon range(0.4 0.6)) ///
       , ///
       title("PSTR: Transformation Function {it:g}(q; {it:γ}, {it:c}) with Different {it:c}", margin(medsmall)) ///
       legend(order(1 "{it:c} = -2" 2 "{it:c} = 0" 3 "{it:c} = 2") ///
              position(4) ring(0) cols(1)) ///
       xtitle("{it:q}") ytitle("{it:g}(q; {it:γ}, {it:c})") ///
       ylabel(0(0.1)1, format(%2.1f)) xlabel(-6(1)6) ///
       scheme(cleanplots)

graph export "PSTR_trans_02_location.png", as(png) replace
```



<br>
<br>

<font color=green>:dog: 下面是最终文本的效果：</font>

<br>
<br>


--- - --

## 2. PSTR 模型设定及参数含义

基本的 PSTR 模型定义为：

$$
y_{it}=\mu_i+\beta_0'x_{it}+\beta_1'x_{it}\cdot g(q_{it};\gamma,c)+u_{it}  \quad(1)
$$

其中，$i = 1, \cdots, N$, $t = 1, \cdots, T$, $N$ 和 $T$ 分别表示面板的横截面和时间维度。$y_{it}$ 是因变量，$x_{it}$ 是 $k$ 维外生解释变量构成的向量，$\mu_i$ 表示固定个体效应，$u_{it}$是误差项。最核心的是 $g(q_{it};\gamma,c)$，$g(\cdot)$ 被称为「转换函数」，$q_{it}$ 是转换变量，$\gamma$ 是平滑参数（速度参数），$c$ 是位置参数，即发生转换的阈值。

转换函数的表达式如下：

$$
g(q_{it};\gamma,c) = \frac{1}{1+\exp\left[-\gamma(q_{it}-c)\right]}
$$

### 2.1 速度参数 γ 的含义

速度参数 $\gamma$ 决定了转换函数 $g(q_{it};\gamma,c)$ 的变化速度。

- 当 $\gamma = 0$ 时，$g(q_{it};\gamma,c) = 0.5$，模型为线性模型，无状态转换。
- 当 $\gamma \to \infty$ 时，$g(q_{it};\gamma,c)$ 迅速从状态 1 转换到状态 2，类似于跳跃，这与 Hansen (1999) 的面板门槛模型相似。
- 当 $\gamma = 0.3$ 和 $\gamma = 1$ 时，表示状态转换的平滑程度。

下面的图形展示了不同 $\gamma$ 值对转换函数的影响：

```stata
// 安装 cleanplot 模版
ssc install cleanplots, replace

// 设置图形字体为 Microsoft YaHei
graph set window fontface "Microsoft YaHei"

// 第一组图形：c=0；gamma=0, gamma=0.3, gamma=1, gamma=9
local c = 0
local gamma0 = 0
local gamma1 = 0.3
local gamma2 = 1
local gamma3 = 9
local g_opts "range(-6 6) lpattern(dash)"
local hline_opts "lc(black*0.9) lp(dot) lw(*1.8)"

twoway ///
     function ///
     g0 = (1 + exp(-`gamma0' * (x - `c'))) ^ (-1),  ///
              `g_opts' lcolor(blue)                 ///
  || function ///
     g1 = (1 + exp(-`gamma1' * (x - `c'))) ^ (-1),  ///
              `g_opts' lcolor(red)                  ///
  || function ///
     g2 = (1 + exp(-`gamma2' * (x - `c'))) ^ (-1),   ///
              `g_opts' lcolor(green)                 ///
  || function /// 
     g3 = (1 + exp(-`gamma3' * (x - `c'))) ^ (-1),   ///
              `g_opts' lcolor(orange)                ///
  || function y = 0, `hline_opts' range(0 1) horizon ///
     legend(order(1 "c = `c', gamma = `gamma0'"      ///
                  2 "c = `c', gamma = `gamma1'"      ///
                  3 "c = `c', gamma = `gamma2'"      ///
                  4 "c = `c', gamma = `gamma3'")     ///
            pos(5) col(1) ring(0) lstyle(none))      ///
    title("转换函数 g(q; γ, c) 随速度参数 γ 的变化")   ///
    ytitle("g(q; γ, c)")                             ///
    xtitle("q")                                      ///
    ylabel(0(0.1)1, format(%2.1f))                   ///
    xlabel(-6.8 " " -6(2)6 6.8 " ")                  ///
    yline(0, lcolor(gs10) lpattern(dot))             ///
    xline(0, lcolor(gs10) lpattern(dot))             ///
    scheme(cleanplots)

// 导出图形
graph export PSTR_01_gamma.png, replace width(1000)
```

![](https://fig-lianxh.oss-cn-shenzhen.aliyuncs.com/PSTR_01_gamma.png)

### 2.2 位置参数 c 的含义

位置参数 $c$ 决定了转换函数 $g(q_{it};\gamma,c)$ 中发生转换的阈值。随着位置参数的不同，转换点也会有所不同。

下面的图形展示了不同 $c$ 值对转换函数的影响：

```stata
// 设置图形字体为 Microsoft YaHei
graph set window fontface "Microsoft YaHei"

// 第二组图形：c=-2, c=0, c=2；gamma=1
local gamma = 1
local c_neg = -2
local c_0   =  0
local c_pos =  2
local g_opts "range(-8 8) lpattern(dash)"
local hline_opts "lc(black*0.9) lp(dot) lw(*1.8)"

twoway ///
     function ///
     g_neg = (1 + exp(-`gamma' * (x - `c_neg'))) ^ (-1), ///
              `g_opts' lcolor(blue)                      ///
  || function ///
     g_0 = (1 + exp(-`gamma' * (x - `c_0'))) ^ (-1),     ///
              `g_opts' lcolor(red)                       ///
  || function ///
     g_pos = (1 + exp(-`gamma' * (x - `c_pos'))) ^ (-1), ///
              `g_opts' lcolor(green)                     ///
  || function y = `c_neg', `hline_opts' range(0.4 0.6) horizon ///
  || function y = `c_0'  , `hline_opts' range(0.4 0.6) horizon ///
  || function y = `c_pos', `hline_opts' range(0.4 0.6) horizon ///
  || function y = 0.5    , `hline_opts' range(-3 +3)           ///
     legend(order(1 "gamma = `gamma', c = `c_neg'"  ///
                  2 "gamma = `gamma', c = `c_0'"    ///
                  3 "gamma = `gamma', c = `c_pos'") ///
            pos(5) col(1) ring(0) lstyle(none))     ///
    title("转换函数 g(q; γ, c) 随位置参数 c 的变化")  ///
    ytitle("g(q; γ, c)")                            ///
    xtitle("q")                                     ///
    ylabel(0(0.1)1, format(%2.1f))                  ///
    xlabel(-8 " " -7 " " -6(2)6 7 " " 8 " ")        ///
    yline(0, lcolor(gs10) lpattern(dot))            ///
    xline(0, lcolor(gs10) lpattern(dot))            ///
    scheme(cleanplots)

// 导出图形
graph export PSTR_02_c_location.png, replace width(1000)
```


![](https://fig-lianxh.oss-cn-shenzhen.aliyuncs.com/PSTR_02_c_location.png)
