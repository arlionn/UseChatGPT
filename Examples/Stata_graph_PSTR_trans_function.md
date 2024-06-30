


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
