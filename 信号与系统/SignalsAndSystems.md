# 信号与系统

## 前言

感谢浙江大学胡浩基老师的信号与系统课程，使得笔者完成此份笔记。

课程链接：[2022浙江大学信号与系统（含配套课件和代码） - 胡浩基老师](https://www.bilibili.com/video/BV1g94y1Q76G?p=6)

老师主页：[胡浩基的个人主页-浙江大学个人主页 (zju.edu.cn)](https://person.zju.edu.cn/huhaoji)

## 信号与系统

### 绪论

#### 信号

信号是表达、传递信息的符号。

根据香农的定义，信息量的值为 $-\log[p(x)]$，信息熵的定义为 $-\sum{p(x)\log[p(x)]} = E[-\log{p(x)}]$。

本课程研究成本低、简洁、传输速度快、传输可靠的信号。

#### 系统

系统是接受输入信号，并把输入信号转换为输出信号的实体。

多个基本系统级联起来能构成复杂系统。

### 典型的信号

#### 信号的描述与分类

- 基于信号维度的分类

  - 一维信号
  - 二维信号
  - 三维信号
  - 四维信号

  在本课程中，我们仅仅讨论一维信号。

#### 连续信号与离散信号

一维信号按自变量的取值是否连续可分为连续时间信号和离散时间信号。

- 连续信号

  连续时间信号：在任何时刻除了若干个不连续点外都有定义的信号。

  连续信号表示方法： $x(t)$。

- 离散信号

  离散时间信号：仅在一系列特定的、离散的时间点上有定义的信号。

  离散信号表示方法： $x[n]$。

#### 周期信号与非周期信号

- 周期信号

  周期信号：信号随时间变量 $t$ 或 $n$ 变化，具有重复性。

  连续周期信号满足 $x(t) = x(t+mT)\ (m\in \mathbb{Z})$，其中 $T$ 称为连续信号的最小正周期。

  离散周期信号满足 $x[n] = x[n+mN],\ (m\in\mathbb{Z})$，其中 $N$ 是自然数，$N$ 称为离散信号的最小正周期。

- 非周期信号

  不满足上述周期信号性质的信号是非周期信号。

#### 奇信号与偶信号

按信号是关于原点对称或关于坐标纵轴对称，又可分为奇信号与偶信号。

- 奇信号

  满足 $x(t) = -x(-t)$ 或 $x[n] = -x[-n]$ 的信号为奇信号。

- 偶信号

  满足 $x(t) = x(-t)$ 或 $x[n] = x[-n]$ 的信号为偶信号。

**一个信号一定能够拆分成一个奇信号与一个偶信号的和，且拆分方法唯一，如下所示：**
$$
x(t) = \frac{x(t)+x(-t)}{2} + \frac{x(t)-x(-t)}{2}
$$
其中 $\displaystyle x_e(t) = \frac{x(t)+x(-t)}{2}$ 是偶信号，$\displaystyle x_o(t)=\frac{x(t)-x(-t)}{2}$ 是奇信号。

#### 功率信号与能量信号

在 $n_1\leqslant n \leqslant n_2$ 内的离散时间信号的总能量和平均功率是
$$
E = \sum_{n=n_1}^{n=n_2}\vert{x[n]}\vert^2 \\
P = \frac{1}{n_2-n_1+1}\sum_{n=n_1}^{n=n_2}\vert{x[n]}\vert^2 \\
$$
相似地，在 $t_1\leqslant t\leqslant t_2$ 内的连续时间信号的总能量和平均功率是
$$
E = \int_{t_1}^{t_2}\vert{x(t)}\vert^2 \\
P = \frac{1}{t_2-t_1}\int_{t_1}^{t_2}\vert{x(t)}\vert^2\text{d}t \\
$$

- 能量有限信号

  如果信号 $x(t)$ 的能量 $E$ 满足 $0<E<\infty$，而 $P=0$。
  
- 功率有限信号

  如果信号 $x(t)$ 的功率 $P$ 满足 $0<P<\infty$，而 $E=\infty$。

#### 奇异信号

- 单位阶跃信号

  单位阶跃信号记作 $u(t)$，定义为

  $$
  u(t) = 
  \begin{cases}
  0\quad t<0 \\
  1\quad t>0
  \end{cases}
  $$

  在跳变点 $t=0$ 处无定义。

- 冲激信号

  冲激信号记作 $\delta(t)$，定义为
  $$
  \delta(t) = 
  \begin{cases}
  +\infty\quad t = 0 \\
  0\quad otherwise
  \end{cases}
  $$
  且有
  $$
  \int_{-\infty}^{+\infty}\delta(t)\text{d}t = 1
  $$
  以及
  $$
  \delta(t) = \frac{\text{d}u(t)}{\text{d}t}
  $$

#### 其他连续时间信号

- 抽样函数

  抽样函数记作 $Sa(t)$，定义为
  $$
  Sa(t) = \frac{\sin(t)}{t} \quad or \quad \sin{c(t)} = \frac{\sin(\pi t)}{\pi t}
  $$
  特别地，在 $t=0$ 时抽样函数满足
  $$
  Sa(t) = 1
  $$
  抽样函数具有以下性质(<a name="dirichlet integral">狄利克雷积分</a>)
  $$
  \int_0^{\infty}Sa(t)\text{d}t = \int_0^{\infty}\frac{\sin(t)}{t}\text{d}t = \int_0^{\infty}\frac{\sin(\omega t)}{t}\text{d}t = \frac{\pi}{2} \ (\omega>0)\\
  \int_{-\infty}^{\infty}Sa(t)\text{d}t = \int_{-\infty}^{\infty}\frac{\sin(t)}{t}\text{d}t = \int_{-\infty}^{\infty}\frac{\sin(\omega t)}{t}\text{d}t = \pi \ (\omega>0)\\
  $$
   **\*证明 $\displaystyle \int_0^{\infty}\frac{\sin(t)}{t}\text{d}t = \frac{\pi}{2}$**

  设 $\displaystyle I(a) = \int_0^{\infty}\frac{\sin(t)}{t}e^{-at}\text{d}t$，则

  $$
  \begin{aligned}
  \displaystyle \frac{\text{d}I(a)}{\text{d}a} &= \int_0^{\infty}\sin(t)e^{-at}\text{d}t \\
  &= -\frac{1}{2j}\int_0^{\infty}(e^{jt}-e^{-jt})e^{-at}\text{d}t \\
  &= \frac{1}{2j}\int_0^{+\infty}e^{-(a+j)t}-e^{-(a-j)t}\text{d}t \\
  &= \frac{1}{2j}\left(\frac{1}{a+j}-\frac{1}{a-j}\right) \\
  &= -\frac{1}{a^2+1}
  \end{aligned}
  $$

  所以 $I(a) = -\arctan(a)+C$，当 $a=+\infty$ 时，有 $I(a)=-\arctan(+\infty) = 0$，因此 $C = \frac{\pi}{2}$。

  所以 $\displaystyle I(0) = \int_0^{\infty}\frac{\sin(t)}{t}\text{d}t  = -\arctan(0)+\frac{\pi}{2} = \frac{\pi}{2}$。

#### 单位冲激序列与单位阶跃序列

- 单位冲激序列

  单位冲激序列记作 $\delta[n]$，定义为
  $$
  \delta[n] = 
  \begin{cases}
  1\quad n = 0 \\
  0\quad otherwise
  \end{cases}
  $$

- 单位阶跃序列

  单位阶跃序列记作 $u[n]$，定义为
  $$
  \delta[n] = 
  \begin{cases}
  1\quad n \geqslant 0 \\
  0\quad otherwise
  \end{cases}
  $$
  

### 信号的自变量变换

对于任意离散信号 $x[n]$，均满足
$$
x[n] = \sum_{k=-\infty}^{+\infty}x[k]\delta[n-k]
$$

### 典型的系统

#### 线性系统

对于某一系统 $x(t)\xrightarrow{System}y(t)$，若同时满足

- 齐次性

  假设 $\forall x(t)\xrightarrow{System}y(t)$

  有
  $$
  kx(t)\xrightarrow{System}ky(t)\ (\forall k\in\mathbb{R})
  $$

- 叠加性

  假设 $\forall x_1(t)\xrightarrow{System}y_1(t),\ x_2(t)\xrightarrow{System}y_2(t)$

  有
  $$
  x_1(t)+x_2(t)\xrightarrow{System}y_1(t)+y_2(t)
  $$

则称该系统为线性系统，否则为非线性系统。

> e.g. 判断系统 $y(t) = tx(t)$ 是否是线性系统

- 齐次性成立
  $$
  x(t)\to y(t)=tx(t) \\
  f(t) = kx(t)\to tf(t) = tkx(t) = ky(t)
  $$

- 叠加性成立
  $$
  x_1(t)\to y_1(t) = tx_1(t) \\
  x_2(t)\to y_2(t) = tx_2(t) \\
  f(t) = x_1(t)+x_2(t)\to tf(t) = t(x_1(t)+x_2(t)) = y_1(t)+y_2(t)
  $$

所以该系统是线性系统。

微分器 $\displaystyle y(t) = \frac{\text{d}x(t)}{\text{d}t}$ 和积分器 $\displaystyle y(t) = \int_{-\infty}^{t}x(\tau)\text{d}\tau$ 也是线性系统。

> e.g. 判断系统 $y[n] = x[n]-x[n-1]$ 是否是线性系统

- 齐次性成立
  $$
  x[n]\to y[n]=x[n]-x[n-1] \\
  f[n] = kx[n] \to f[n]-f[n-1] = kx[n]-kx[n-1] = ky[n]
  $$

- 叠加性成立
  $$
  x_1[n]\to y_1[n]=x_1[n]-x_1[n-1] \\
  x_2[n]\to y_2[n]=x_2[n]-x_2[n-1] \\
  f[n] = x_1[n]+x_2[n] \to f[n]-f[n-1] = (x_1[n]+x_2[n]) - (x_1[n-1]+x_2[n-1]) = y_1[n]+y_2[n]
  $$

所以该系统是线性系统。同时，该系统又称为离散微分器。

类似地，离散积分器 $\displaystyle y[n] = \sum_{k=-\infty}^{n}x[k]$ 也是线性系统。

#### 时不变系统

若 $\forall x(t)\xrightarrow{System} y(t)$，则 $\forall t_0 \in \mathbb{R}$，满足
$$
x(t-t_0)\xrightarrow{System} y(t-t_0)
$$
则称该系统为时不变系统，否则为时变系统。

> e.g. 判断系统 $y(t)=x(t-1)$ 是否是时不变系统
$$
x(t)\to y(t)=x(t-1) \\
f(t)=x(t-t_0) \to f(t-1) = x(t-t_0-1) = y(t-t_0)
$$
所以该系统是时不变系统。

> e.g. 判断系统 $y(t)=e^{x(t+1)}$ 是否是时不变系统
$$
x(t)\to y(t) = e^{x(t+1)} \\
f(t) = x(t-t_0)\to e^{f(t+1)} = e^{x(t-t_0+1)} = y(t-t_0)
$$
所以该系统是时不变系统。

> e.g. 判断系统 $y(t)=x(2t)$ 是否是时不变系统
$$
x(t)\to y(t) = x(2t) \\
f(t) = x(t-t_0) \to f(2t) = x(2t-t_0) \neq x(2(t-t_0)) = y(t-t_0)
$$
所以该系统是时变系统。

#### 因果系统

如果一个系统在任何时刻的输出只决定于现在和过去的输入，就称该系统为因果系统，否则称为非因果系统。

若一个系统是 **LTI 系统**，则其是因果系统的充要条件为 
$$
h(t) = 0\ when\ t < 0
$$
对于系统 $y(f(t)) = x(g(t))$，若在 $t\in\mathbb{R}$ 上均满足 $f(t)>g(t)$，则该系统是因果系统。

> e.g. 判断系统 $y(t) = x(t)\cos(t+1)$ 是否是因果系统

在此系统中，$\cos(t+1)$ 是常数，仅需考虑 $x(t)$ 部分，又因为 $y(t) = x(t)$ 是因果系统，所以该系统也是因果系统。

> e.g. 判断系统 $y[n] = x[n]x[n-2]$ 是否是因果系统

在此系统中，对于 $x[n-2]$ 部分，有 $n>n-2$ 恒成立，又因为 $y[n] = x[n]$ 是因果系统，所以该系统也是因果系统。

> e.g. 判断系统 $y(t) = x(\sin(t))$ 是否是因果系统

若该系统是因果系统，需满足 $t>\sin(t)$ 恒成立。显然该式仅在 $t > 0$ 下成立，所以该系统是非因果系统。

#### 记忆系统

如果一个系统 $y(t)$ 的值仅仅只依赖于 $x(t)$ 的值，就称该系统为无记忆系统，否则称为记忆系统。

> e.g. 判断系统 $y(t) = x(t)^2+e^{x(t)}$ 是否是记忆系统

该系统每一项的值均只依赖于 $x(t)$，所以是无记忆系统。

> e.g. 判断系统 $y(t) = x(t-1)$ 是否是记忆系统

该系统显然依赖于 $x(t-1)$，所以是记忆系统。

> e.g. 判断系统 $y[n] = x[2n]$ 是否是记忆系统

该系统显然依赖于 $x[2n]$，所以是记忆系统。

**特别地，无记忆系统一定是因果系统。**

#### 可逆系统

若一个系统的输入和输出为一一对应的关系，不存在多个输入对应一个输出，则称该系统为可逆系统，否则称为不可逆系统。

> e.g. 判断系统 $y(t) = x^2(t)$ 是否是可逆系统

$x(t) = \pm\sqrt{y(t)}$，此系统存在 $x(t)$ 对应多个值，所以是不可逆系统。

> e.g. 判断系统 $\displaystyle y[n] = \sum_{k=-\infty}^{n}$ 是否是可逆系统

$x[n] = y[n] - y[n-1]$，此系统的 $x[n]$ 与 $y[n]$ 是一一对应的，所以是可逆系统。

> e.g. 判断积分器 $\displaystyle y(t) = \int_{-\infty}^{t}x(\tau)\text{d}\tau$ 是否是可逆系统

$\displaystyle x(t) = \int_{-\infty}^{t}y(\tau)\text{d}\tau+C$，由于 $C$ 是任意常数，所以此系统是不可逆系统。

#### 稳定系统

若一个系统的输入有界，且输出必有界，则称该系统为稳定系统，否则为非稳定系统。

有界的定义是：若 $\vert x(t)\vert<M$，则有 $\vert y_m(t)\vert<N$。

从冲激响应 $h(t)$ 的角度来看，若一个系统是 **LTI 系统**，则其是稳定系统的充要条件为 
$$
\int_{-\infty}^{+\infty}\vert h(t)\vert\text{d}t < +\infty
$$

> e.g. 判断系统 $y(t) = e^{x(t)}$ 是否是稳定系统

若 $\forall t\in\mathbb{R}$，有 $\vert x(t) \vert<M$，则 $\vert y(t) \vert = \vert e^{x(t)} \vert \leqslant  e^{\vert x(t) \vert} \leqslant e^M$ 有界，所以该系统是稳定系统。

> e.g. 判断系统 $y(t) = x^3(t)-2x^2(t)+x(t)+1$ 是否是稳定系统

若 $\forall t\in\mathbb{R}$，有 $\vert x(t) \vert<M$，则 $\vert y(t) \vert = \vert x^3(t)-2x^2(t)+x(t)+1 \vert \leqslant \vert x^3(t) \vert + 2\vert x^2(t) \vert + \vert x(t) \vert + 1 \leqslant M^3+2M^2+M+1$ 有界，所以该系统是稳定系统。

>  e.g. 判断微分器 $\displaystyle y(t) = \frac{\text{d}x(t)}{\text{d}t}$ 是否是稳定系统

对于 $x(t) = u(t)$，有 $\displaystyle \frac{\text{d}x(t)}{\text{d}t} = \frac{\text{d}u(t)}{\text{d}t} = \delta(t)$，其在 $t=0$ 处的值为 $+\infty$，因此微分器是不稳定系统。

## 线性时不变系统

### 线性时不变系统的定义

如果一个系统既是线性系统又是时不变系统，则称该系统为线性时不变(LTI)系统。

#### 为什么要研究线性时不变系统

- 为什么要研究线性系统

  线性只是对现实问题的近似，线性系统是理想化的系统。在研究现实问题时，其往往很复杂，我们需要取一个便于研究的近似，而线性就是最简单的近似。

- 为什么要研究时不变系统

  时变系统对于不同时刻的输入有着不同的输出，使得我们没有办法对其进行研究，因此我们需要在很短的时间尺度上对其进行研究，这个时候可以将系统看作是时不变系统来研究。

线性时不变系统是非常简单的系统，如果我们知道一个线性时不变系统的一个 $x(t)$ 对应的 $y(t)$，那么我们就知道了所有 $s(t)$ 对应的 $y(t)$。

### 离散线性时不变系统的卷积公式

在离散 LTI 系统中，我们定义 $x[n] = \delta[n]$ 为**单位脉冲序列**，$h[n]$ 为**单位脉冲响应**，即 $\delta[n]$ 经过系统得到的输出。那么**卷积**运算的定义为
$$
y[n] = x[n]\ast h[n]
$$
$h[n]$ 是 LTI 系统的唯一标识，也即系统的特征。

#### 列表法

- 确定 $y[n] = x[n]\ast h[n]$ 的取值范围

  $y[n]$ 最左边(最右边) =  $x[n]$ 最左边(最右边) + $h[n]$ 最左边(最右边)

- 列表计算 $y[n]$

**特别地，列表法的时间复杂度为 $O(N^2)$。**

> e.g. 计算卷积 $y[n] = x[n]\ast h[n]$

| $x$    | -1 | 0 | 1 | 2 |
| ---- | ---- | ---- | ---- | ---- |
| $x[n]$ | 3 | 2 | 1 | -1 |
| $h[n]$ | 1 | 1 | 2 | -1 |

使用列表法计算，首先确定左边界为 $(-1)+(-1) = -2$，右边界 $2+2=4$，然后计算卷积和。

|  $x[n]\backslash h[n]$  | 1 | 1 | 2 | -1 |      | | |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| 3 | 3 | 3 | 6 | -3 |      | | |
| 2 |      | 2 | 2 | 4 | 2 | | |
| 1 |      |      | 1 | 1 | 2 | 1 | |
| -1 |      |      |      | -1 | -1 | -2 | 1 |
| $y[n]$ | 3 | 5 | 9 | 1 | -1 | -3 | 1 |

所以卷积的结果为

| $n$    | -2   | -1   | 0    | 1    | 2    | 3    | 4    |
| ------ | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| $y[n]$ |  3   |  5   |  9   |  1   |  -1  |  -3  |  1   |

> e.g. 已知 $x[n] = \delta[n+1] + 2\delta[n] + \delta[n-1] + \delta[n-2],\ h[n] = \delta[n]-\delta[n-1]-\delta[n-4]+\delta[n-5]$，求 $y[n] = x[n]\ast h[n]$

将 $x[n]$ 与 $h[n]$ 转换为

| $n$    | -1   | 0    | 1    | 2    | 3    | 4    | 5    |
| ------ | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| $x[n]$ | 1    | 2    | 1    | 1    |      |      |      |
| $h[n]$ |      | 1    | -1   | 0    | 0    | -1   | 1    |

此时使用列表法计算，不再赘述，结果如下

| $n$    | -1   | 0    | 1    | 2    | 3    | 4    | 5    | 6    | 7    |
| ------ | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| $y[n]$ | 1    | 1    | -1   | 0    | -2   | -1   | 1    | 0    | 1    |

> e.g. 已知 $x[n] = a^nu[n],\ h[n] = u[n]$，求 $y[n] = x[n]\ast h[n]$

经列表计算后，得到 $\displaystyle y[n] = (1+a+a^2+a^3+\cdots+a^n)u[n] = \frac{(1-a)(1+a+a^2+\cdots+a^n)}{1-a}u[n] = \frac{1-a^{n+1}}{1-a}u[n]$

#### 卷积公式

离散 LTI 系统的卷积公式如下
$$
y[n] = x[n]\ast h[n] = \sum_{k=-\infty}^{+\infty}{x[k]h[n-k]} = \sum_{k=-\infty}^{+\infty}{x[k]h[-(k-n)]}
$$
证明如下
$$
\delta[n]\overset{LTI}h[n] \\
\delta[n-k]\overset{LTI}h[n-k] \\
x[k]\delta[n-k]\overset{LTI}x[k]h[n-k] \\
\sum_{k=-\infty}^{+\infty}x[k]\delta[n-k]\overset{LTI}\sum_{k=-\infty}^{+\infty}x[k]h[n-k]
$$
又因为 $\displaystyle x[n] = \sum_{k=-\infty}^{+\infty}x[k]\delta[n-k]$，所以 $\displaystyle x[n] \overset{LTI}\sum_{k=-\infty}^{+\infty}x[k]h[n-k]$，也就是卷积公式的定义。

### 连续线性时不变系统的卷积公式

在连续 LTI 系统中，我们定义 $x(t)=\delta(t)$ 为**冲激函数**，$h(t)$ 为冲激响应。

连续 LTI 系统的卷积公式如下
$$
y(t) = x(t)\ast h(t) = \int_{-\infty}^{+\infty}x(\tau)h(t-\tau)\text{d}\tau
$$
我们定义在 $t=0$ 到 $t=\Delta$ 上，且高度为 $\displaystyle \frac{1}{\Delta}$ 的方波 $\delta_{\Delta}(t)$，假设其经过某连续 LTI 系统后的输出为 $h_{\Delta}(t)$，那么假设极限存在，就有 $\displaystyle \delta(t) = \lim_{\Delta\to 0}\delta_{\Delta}(t)\overset{LTI}h(t) = \lim_{\Delta\to 0}h_{\Delta}(t)$

接下来证明连续 LTI 系统的卷积公式
$$
\delta_{\Delta}(t)\overset{LTI}h_{\Delta}(t) \\
\delta_{\Delta}(t-k\Delta)\overset{LTI}h_{\Delta}(t-k\Delta) \\
x(k\Delta)\delta_{\Delta}(t-k\Delta)\Delta\overset{LTI}x(k\Delta)h_{\Delta}(t-k\Delta)\Delta \\
x_{\Delta}(t) = \sum_{k=-\infty}^{+\infty}x(k\Delta)\delta_{\Delta}(t-k\Delta)\Delta\overset{LTI}\sum_{k=-\infty}^{+\infty}x(k\Delta)h_{\Delta}(t-k\Delta)\Delta \\
$$
此时有 
$$
\begin{aligned}
x(t) = \lim_{\Delta\to 0}x_{\Delta}(t) = \lim_{\Delta\to 0}\sum_{k=-\infty}^{+\infty}x(k\Delta)\delta_{\Delta}(t-k\Delta)\Delta\xrightarrow{LTI}
& \lim_{\Delta\to 0}\sum_{k=-\infty}^{+\infty}x(k\Delta)h_{\Delta}(t-k\Delta)\Delta \\
=& \lim_{\Delta\to 0}\sum_{k=-\infty}^{+\infty}x(k\Delta)h(t-k\Delta)\Delta \\
=& \int_{-\infty}^{+\infty}x(\tau)h(t-\tau)\text{d}\tau
\end{aligned}
$$

### 冲激函数的性质

- $\displaystyle \int_{-\infty}^{+\infty}\delta(t)\text{d}t = 1$
- $\displaystyle \int_{-\infty}^{+\infty}x(t)\delta(t-t_0)\text{d}t = x(t_0),\ \displaystyle \int_{-\infty}^{+\infty}x(t)\delta(0)\text{d}t = x(0)$
- $x(t)\delta(t) = x(0)\delta(t)$
- $\displaystyle \delta(at) = \frac{1}{\vert a\vert}\delta(t)$
- $\displaystyle \delta(f(t)) = \sum_{\text{for all}\ f(t_0)=0}{\frac{1}{\vert f'(t_0)\vert}}\delta(t-t_0)$

根据上述公式，可以得到
$$
\delta(\cos{t}) =  \sum_{k=-\infty}^{+\infty}\delta(t-k\pi-\frac{\pi}{2}) \\
\delta(\sin{t}) =  \sum_{k=-\infty}^{+\infty}\delta(t-k\pi) \\
$$

> e.g. 求 $\displaystyle \int_{-2\pi}^{2\pi}(1+t)\delta(\cos{t})\text{d}t$

$$
\begin{aligned}
& \int_{-2\pi}^{2\pi}(1+t)\delta(\cos{t})\text{d}t  \\
=& \int_{-2\pi}^{2\pi}(1+t)[\delta(t+\frac{3}{2}\pi)+\delta(t+\frac{1}{2}\pi)+\delta(t-\frac{1}{2}\pi)+\delta(t-\frac{3}{2}\pi)]\text{d}t \\
=& \int_{-2\pi}^{2\pi}(1+t)\delta(t+\frac{3}{2}\pi)\text{d}t + \int_{-2\pi}^{2\pi}(1+t)\delta(t+\frac{1}{2}\pi)\text{d}t + \int_{-2\pi}^{2\pi}(1+t)\delta(t-\frac{1}{2}\pi)\text{d}t + \int_{-2\pi}^{2\pi}(1+t)\delta(t-\frac{3}{2}\pi)\text{d}t \\
=& (1-\frac{3}{2}\pi) + (1-\frac{1}{2}\pi) + (1+\frac{1}{2}\pi) + (1+ \frac{3}{2}\pi) \\
=& 4
\end{aligned}
$$

#### <a name="lemma1">引理1(黎曼-勒贝格引理)</a>

**若 $x(t)$ 不是无限振荡的函数，则**
$$
\lim_{\omega\to +\infty}\int_{-\infty}^{+\infty}x(t)\cos(\omega t)\text{d}t = 0 \\
\lim_{\omega\to +\infty}\int_{-\infty}^{+\infty}x(t)\sin(\omega t)\text{d}t = 0 \\
$$
对于冲激函数，还有定义
$$
\lim_{\omega\to+\infty}\frac{\sin(\omega t)}{\pi t} = \delta(t)
$$
证明如下

由于上式等价于下式，因此只需证明
$$
\int_{-\infty}^{+\infty}\left[\lim_{\omega \to+\infty}\frac{\sin(\omega t)}{\pi t}\right]y(t)\text{d}t = y (0)
$$
对于式子左边，有
$$
\begin{aligned}
左边 &= \lim_{\omega\to +\infty}\int_{-\infty}^{+\infty}\left[\frac{y(t)}{\pi t}\right]\sin(\omega t)\text{d}t \\
&= \lim_{\omega\to +\infty}\int_{-\infty}^{+\infty}\left[\frac{y(t)-y(0)}{\pi t}\right]\sin(\omega t)\text{d}t + y(0)\lim_{\omega\to +\infty}\int_{-\infty}^{+\infty}\frac{\sin(\omega t)}{\pi t}\text{d}t \\
&= 0+y(0)\cdot 1 \\
&= y(0)
\end{aligned}
$$
原式得证。

对于上面的 $\displaystyle \lim_{\omega\to +\infty}\int_{-\infty}^{+\infty}\left[\frac{y(t)-y(0)}{\pi t}\right]\sin(\omega t)\text{d}t$，且因为 $\displaystyle \frac{y(0)-y(0)}{\pi t} = \lim_{t\to 0}\frac{y(t)-y(0)}{\pi t} = \frac{y'(0)}{\pi}$，我们设 
$$
x(t) = \frac{y(t)-y(0)}{\pi t} = 
\begin{cases}
\displaystyle \frac{y'(0)}{\pi}\quad t = 0 \\
\displaystyle \frac{y(t)-y(0)}{\pi t}\quad t\neq0
\end{cases}
$$
所以 $x(t)$ 不是无限振荡的函数，那么根据[引理1](#lemma1)，有
$$
\lim_{\omega\to +\infty}\int_{-\infty}^{+\infty}x(t)\sin(\omega t)\text{d}t = 0 \\
$$

### 连续信号卷积的计算

#### 公式法

> e.g. 对于 $x(t) = e^{-bt}u(t),\ h(t) = e^{-at}u(t)$，求卷积和

$$
\begin{aligned}
x(t)\ast h(t) 
&= \int_{-\infty}^{+\infty}x(\tau)h(t-\tau)\text{d}\tau \\
&= \int_{-\infty}^{+\infty}e^{-b\tau}u(\tau)e^{-a(t-\tau)}u(t-\tau)\text{d}\tau \\
&= \int_0^t e^{-b\tau}e^{-a(t-\tau)}\text{d}\tau \\
&= e^{-at}\int_0^t e^{-(b-a)\tau}\text{d}\tau \\
&= \frac{e^{-at}-e^{-bt}}{b-a}
\end{aligned}
$$

上式是在 $0<\tau<t$ 时取得。因此答案为
$$
x(t)\ast h(t) = 
\begin{cases}
0\quad t<0 \\
\displaystyle \frac{e^{-at}-e^{-bt}}{b-a}\quad t>0 \\
\end{cases}
= \frac{e^{-at}-e^{-bt}}{b-a}u(t)
$$

#### 直观分析

### 卷积的性质

#### <a name="lemma2">引理2</a>

两个 LTI 系统串联或并联仍为 LTI 系统。

#### 交换律

$x(t)\ast h(t) = h(t)\ast s(t)$

证明如下

设 $\tau' = t-\tau$，则
$$
\begin{aligned}
x(t)\ast h(t) 
&= \int_{-\infty}^{+\infty}x(\tau)h(t-\tau)\text{d}\tau \\
&= \int_{+\infty}^{-\infty}x(t-\tau')h(\tau)\text{d}\tau \\
&= \int_{-\infty}^{+\infty}x(t-\tau')h(\tau)\text{d}\tau' \\
&= h(t)\ast x(t)
\end{aligned}
$$

#### 结合律

$[x(t)\ast h_1(t)]\ast h_2(t) = [x(t)\ast h_2(t)]\ast h_1(t)$

证明如下

假设存在[两个 LTI 系统](#lemma2)分别经 $h_1(t),\ h_2(t)$ 符合而成
$$
x(t)\xrightarrow{h_1(t),\ h_2(t)}[x(t)\ast h_1(t)]\ast h_2(t) \\
x(t)\xrightarrow{h_2(t),\ h_1(t)}[x(t)\ast h_2(t)]\ast h_1(t) \\
$$
若要证明两个系统等价，只需证明当 $x(t)=\delta(t)$ 时系统的输出相同。

对于 $\delta(t)$ 分别作为以上两个系统的输入，有
$$
\delta(t)\xrightarrow{h_1(t),\ h_2(t)}[\delta(t)\ast h_1(t)]\ast h_2(t) = h_1(t)\ast h_2(t)\\
\delta(t)\xrightarrow{h_2(t),\ h_1(t)}[\delta(t)\ast h_2(t)]\ast h_1(t) = h_2(t)\ast h_1(t)\\
$$
根据卷积的交换律，可知这两个系统等价，因而结合律得证。

#### 分配律

$x(t)\ast[h_1(t)+h_2(t)] = x(t)\ast h_1(t)+x(t)\ast h_2(t)$

此处不给出证明，因为积分和求和具有分配律。

#### 特殊函数的卷积与性质

- $\displaystyle x(t)\ast u(t) = \int_{-\infty}^{t}x(\tau)\text{d}\tau$

- #### $\displaystyle x[n]\ast u[n] = \sum_{k=-\infty}^{n}x[k]$

- 对于冲击偶函数 $\displaystyle \delta'(t) = \frac{\text{d}\delta(t)}{\text{d}t}$，有 $\displaystyle \int_{-\infty}^{+\infty}\delta'(t)\text{d}t=0$ 和 $\displaystyle \frac{\text{d}x(t)}{\text{d}t} = x(t)\ast \delta'(t)$

- $\displaystyle \frac{\text{d}[x(t)\ast h(t)]}{\text{d}t} = \frac{\text{d}x(t)}{\text{d}t}\ast h(t) = \frac{\text{d}h(t)}{\text{d}t}\ast x(t)$

- $x(t+t_0)\ast h(t-t_0) = x(t)\ast h(t)$

## 连续时间傅里叶变换

### 傅里叶级数

#### 傅里叶级数的定义

若 
$$
f(t)=B_0+\sum_{k=1}^{+\infty}B_k\cos(k\omega_0t)+\sum_{k=1}^{+\infty}C_k\sin(k\omega_0t)\ (T_0=\frac{2\pi}{\omega_0})
$$
则有
$$
\begin{aligned}
B_0 &= \frac{1}{T_0}\int_{0}^{T_0}f(t)\mathrm{d}t \\
B_k &= \frac{2}{T_0}\int_{0}^{T_0}f(t)\cos(k\omega_0{t})\mathrm{d}t \\
C_k &= \frac{2}{T_0}\int_{0}^{T_0}f(t)\sin(k\omega_0{t})\mathrm{d}t \\
\end{aligned}
$$

其中 $\omega_0$ 叫做基波频率，$k\omega_0$ 叫做 $k$ 次谐波频率，$T_0=\frac{2\pi}{\omega_0}$ 叫做基波周期，$B_0$ 叫做直流分量。

#### 傅里叶级数的证明

此处略。

#### 傅里叶级数的复数形式

$$
\begin{aligned}
x(t) &= \sum_{k=-\infty}^{+\infty}a_ke^{jk\omega_0t}\ (\omega_0 = \frac{2\pi}{T_0}) \\
a_k &= \frac{1}{T_0}\int_0^{T_0}x(t)e^{-jk\omega_0t}\text{d}t \\
\end{aligned}
$$

其中

$$
\begin{aligned}
B_0 &= a_0\ (k=0) \\
B_k &= a_{-k}+a_k\ (k\neq 0) \\
C_k &= j(a_k-a_{-k})\ (k\neq 0) \\
\end{aligned}
$$

我们很容易通过下面的步骤证明该表达式与傅里叶级数的原定义等价。

$$
\begin{aligned}
x(t) &= \sum_{k=-\infty}^{+\infty}a_ke^{jk\omega_0t} \\
&= a_0 + \sum_{k=1}^{+\infty}(a_ke^{jk\omega_0t}+a_{-k}e^{-jk\omega_0t}) \\ 
&= a_0 + \sum_{k=1}^{+\infty}((a_k+a_{-k})\cos(\omega_0t)+j(a_k-a_{-k})\sin(\omega_0t)) \\ 
\end{aligned}
$$

#### <a name="lemma3">引理3</a>

若 $x(t)$ 满足狄里赫利条件，则有
$$
\lim_{N\to+\infty}\int_0^{T_0}x(t)\sin(Nt)\text{d}t = 0 \\
\lim_{N\to+\infty}\int_0^{T_0}x(t)\cos(Nt)\text{d}t = 0 \\
$$

#### 傅里叶级数收敛性的证明(狄里赫利条件)

狄里赫利条件

- $x(t)$ 在一个周期内绝对可积，也就是信号的能量有限，即 $\displaystyle \int_0^{+\infty}\vert x(t)\vert \text{d}t<\infty$
- $x(t)$ 在一个周期内极值的数量有限，即信号在一周期内不作无限振荡
- $x(t)$ 在一个周期内连续或存在有限个第一类间断点

若以 $T_0$ 为周期的信号 $x(t)$ 满足狄里赫利条件，则有
$$
x_N(t) =B_0+\sum_{k=1}^{N}B_k\cos(k\omega_0t)+\sum_{k=1}^{N}C_k\sin(k\omega_0t)\ (T_0=\frac{2\pi}{\omega_0}) \\
\begin{aligned}
B_0 &= \frac{1}{T_0}\int_{0}^{T_0}x(t)\mathrm{d}t \\
B_k &= \frac{2}{T_0}\int_{0}^{T_0}x(t)\cos(k\omega_0{t})\mathrm{d}t \\
C_k &= \frac{2}{T_0}\int_{0}^{T_0}x(t)\sin(k\omega_0{t})\mathrm{d}t \\
\end{aligned}
$$
那么则有
$$
\lim_{N\to+\infty}x_N(t)=x(t)
$$
证明如下



### 函数的正交分解

#### 正交函数族

对于函数族 $\{1, \cos(\omega_0t), \sin(\omega_0t),\cos(2\omega_0t),\sin(2\omega_0t),\cdots\}$，任取两个相乘，在一个周期 $T_0 = \frac{2\pi}{\omega_0}$ 上的积分都为 $0$。

也就是说，$\{e^{jk\omega_0t}\}_{k=-\infty\sim+\infty, k\in\mathbb{Z}}$ 是正交基。

对于一族函数 $\{e_i(t)\}_{i=1\sim +\infty}$，若满足任取两个 $e_i(t),e_j(t)$ 相乘的积分为 $0$，即 $\displaystyle \int_a^b e_i(t)e_j(t)\text{d}t=0$，则称该函数族为正交函数族。

#### 施密特正交化

对于一组非正交基 $\{\alpha_k\}_{k=1\sim+\infty}$，可以使用施密特正交化将其变成正交基，新的基底如下
$$
\begin{aligned}
\beta_1 &= \alpha_1 \\
\beta_2 &= \alpha_2-\frac{<\alpha_2,\beta_1>}{<\beta_1,\beta_1>}\beta_1 \\
\beta_3 &= \alpha_3-\frac{<\alpha_3,\beta_1>}{<\beta_1,\beta_1>}\beta_1-\frac{<\alpha_3,\beta_2>}{<\beta_2,\beta_2>}\beta_2 \\
\vdots\\
\beta_k &= \alpha_k-\sum_{m=1}^{k-1}\frac{<\alpha_k,\beta_m>}{<\beta_m,\beta_m>}\beta_m
\end{aligned}
$$
那么 $\{\beta_k\}_{k=1\sim+\infty}$ 就是正交基，这与线性代数中的过程相同，此处推广到复数域。

### 傅里叶变换

#### 傅里叶变换的定义

非周期函数 $x(t)$ 在 $(-\infty,+\infty)$ 上的傅里叶变换为
$$
x(jw) = \int_{-\infty}^{+\infty}x(t)e^{-j\omega t}\text{d}t \\
x(t) = \frac{1}{2\pi}\int_{-\infty}^{+\infty}x(j\omega)e^{j\omega t}\text{d}\omega
$$
这两个变换分别叫做傅里叶变换和傅里叶反变换，$x(j\omega)$ 叫做 $x(t)$ 的傅里叶变换。其中 $x(j\omega t)$ 叫做频域，$x(t)$ 叫做时域，因此有 $x(j\omega)=\mathscr{F}(x(t)),\ x(t) = \mathscr{F}^{-1}(x(j\omega))$，其中 $j$ 在此处无实际意义，$x(j\omega)$ 也可以直接使用 $x(\omega)$ 表示。

下面给出傅里叶变换的证明。

假设已知 $\displaystyle x(j\omega) = \int_{-\infty}^{+\infty}x(u)e^{-j\omega u}\text{d}u$，我们证明 $\displaystyle x(t) = \frac{1}{2\pi}\int_{-\infty}^{+\infty}x(j\omega)e^{j\omega t}\text{d}\omega$。
$$
\begin{aligned}
x(t) &= \frac{1}{2\pi}\int_{-\infty}^{+\infty}x(j\omega)e^{j\omega t}\text{d}\omega \\
&= \frac{1}{2\pi}\int_{-\infty}^{+\infty}\left[\int_{-\infty}^{+\infty}x(u)e^{-j\omega u}\text{d}u\right]e^{j\omega t}\text{d}\omega \\
&= \frac{1}{2\pi}\int_{-\infty}^{+\infty}x(u)\text{d}u\left[\int_{-\infty}^{+\infty}e^{j\omega (t-u)}\text{d}\omega\right] \\ 
&= \frac{1}{2\pi}\int_{-\infty}^{+\infty}x(u)\text{d}u\cdot \frac{1}{j(t-u)}e^{j\omega (t-u)}\Bigg|_{\omega=-\infty}^{+\infty} \\
&= \frac{1}{\pi}\int_{-\infty}^{+\infty}x(u)\text{d}u\left[\lim_{\omega\to+\infty}\frac{\sin(\omega(t-u))}{t-u}\right] \\
&= \frac{1}{\pi}\int_{-\infty}^{+\infty}x(u)\cdot\pi\delta(t-u) \text{d}u \\
&= x(t)
\end{aligned}
$$
上述式子中冲激函数的变换可以查看[引理1](#lemma1)。相应地，我们也可以在已知 $x(t)$ 的前提下证明上述 $x(j\omega)$ 的表达式，此处证明不在给出。

#### 典型信号的傅里叶变换

以下常见信号的傅里叶变换需要牢记，其均可以使用上面的定义证明。

1. $\displaystyle e^{-at}u(t)\xrightarrow{F}\frac{1}{a+j\omega}\ (a>0)$
2. $\displaystyle \delta(t)\xrightarrow{F}1$
3. $\displaystyle 1\xrightarrow{F}2\pi\delta(\omega)$
4. 在区间 $\left[\frac{-\tau}{2},\frac{\tau}{2}\right]$ 上高度为 $E$ 的方波 $\xrightarrow{F}$ $\displaystyle E\tau\text{Sa}(\frac{\tau}{2}\omega) = \frac{2E\sin(\frac{\tau}{2}\omega)}{\omega}$
5. $\displaystyle \frac{\sin(\omega_c t)}{\pi t}\ (\omega_c>0)$ $\xrightarrow{F}$ 在区间 $[-\omega_c,\omega_c]$ 上高度为 $1$ 的方波
6. $\displaystyle \cos(\omega_0t)\xrightarrow{F}\pi[\delta(\omega+\omega_0)+\delta(\omega-\omega_0)]$
7. $\displaystyle \sin(\omega_0t)\xrightarrow{F}\frac{\pi}{j}[\delta(\omega-\omega_0)-\delta(\omega+\omega_0)]$
8. $\displaystyle u(t)\xrightarrow{F}\frac{1}{j\omega}+\pi\delta(\omega)$

接下来我们依次给出证明，此处需要多次使用[狄利克雷积分](#dirichlet integral)。

对于信号 $x(j\omega) = \vert x(j\omega)\vert e^{j\theta(\omega)}$，$\vert x(j\omega)\vert$ 叫做幅度谱(Amplitude)，$e^{j\theta(\omega)}$ 叫做相位谱。

1. $\displaystyle x(t)=e^{-at}u(t)$
$$
  \begin{aligned}
  x(j\omega) &= \int_{-\infty}^{+\infty}\left[e^{-at}u(t)\right]e^{-j\omega t}\text{d}t \\
  &= \int_{0}^{+\infty}e^{-(a+j\omega)t}\text{d}t \\
  &= -\frac{1}{a+j\omega}e^{-(a+j\omega)t}\Bigg|_{t=0}^{+\infty} \\
  &= -\frac{1}{a+j\omega}\left[e^{-(a+j\omega)\cdot(+\infty)}-1\right] \\
  \end{aligned}
$$
  当且仅当 $a>0$ 时，有 $\displaystyle x(j\omega) = \frac{1}{a+j\omega}$。

2. $x(t)=\delta(t)$
$$
  \begin{aligned}
  x(j\omega) &= \int_{-\infty}^{+\infty}\delta(t)e^{-j\omega t}\text{d}t \\
  &= e^{-j\omega t}\Bigg|_{t=0} \\
  &= 1
  \end{aligned}
$$

3. $x(j\omega) = 2\pi\delta(\omega)$
$$
  \begin{aligned}
  x(t) &= \frac{1}{2\pi}\int_{-\infty}^{+\infty}2\pi\delta(\omega)e^{j\omega t}\text{d}\omega \\
  &= \int_{-\infty}^{+\infty}\delta(\omega)e^{j\omega t}\text{d}\omega \\
  &= e^{j\omega t}\Bigg|_{\omega=0} \\
  &= 1
  \end{aligned}
$$
  或者令 $x(t)=1$
$$
  \begin{aligned}
  x(j\omega) &= \int_{-\infty}^{+\infty}e^{-j\omega t}\text{d}t \\
  &= \lim_{N\to+\infty}\int_{-N}^{N}e^{-j\omega t}\text{d}t \\
  &= \lim_{N\to+\infty}-\frac{1}{j\omega}e^{-j\omega t}\Bigg|_{-N}^{N} \\
  &= \lim_{N\to+\infty}\frac{1}{j\omega}2j\sin(\omega N) \\
  &= \lim_{N\to+\infty} \frac{2\sin(\omega N)}{\omega} \\
  &= 2\pi\delta(\omega)
  \end{aligned}
$$

4. $x(t)$ 为在区间 $\left[\frac{-\tau}{2},\frac{\tau}{2}\right]$ 上高度为 $E$ 的方波
$$
\begin{aligned}
  x(j\omega) &= \int_{-\frac{\tau}{2}}^{\frac{\tau}{2}}Ee^{-j\omega t}\text{d}t \\
  &= -\frac{E}{j\omega}e^{-j\omega t}\Bigg|_{t=-\frac{\tau}{2}}^{\frac{\tau}{2}} \\
  &= \frac{E}{j\omega}2j\sin(\omega \frac{\tau}{2}) \\
  &= \frac{2E\sin(\omega \frac{\tau}{2})}{\omega} \\
  &= E\tau\sin(\frac{\tau}{2}\omega)
  \end{aligned}
$$

5. $x(t) = \displaystyle \frac{\sin(\omega_c t)}{\pi t}$
$$
\begin{aligned}
  x(j\omega) &= \int_{-\infty}^{+\infty}\frac{\sin(\omega_c t)}{\pi t}e^{-j\omega t}\text{d}t \\
  &= \int_{-\infty}^{+\infty}\frac{\sin(\omega_c t)}{\pi t}[\cos(\omega t)-j\sin(\omega t)]\text{d}t \\
  &= \int_{-\infty}^{+\infty}\frac{\sin(\omega_c t)}{\pi t}\cos(\omega t)\text{d}t \\
  &= \frac{1}{2}\left[\int_{-\infty}^{+\infty}\frac{\sin((\omega_c+\omega)t)}{\pi t}\text{d}t + \int_{-\infty}^{+\infty}\frac{\sin((\omega_c-\omega)t)}{\pi t}\text{d}t\right] \\
  \end{aligned}
$$

  - 当 $\omega < -\omega_c$ 时，有 $\omega+\omega_c<0,\ \omega_c-\omega>0$ ，因此 $x(j\omega) = \frac{1}{2}(-1+1) = 0$；
  - 当 $-\omega_c<\omega<\omega_c$ 时，有 $\omega_c+\omega>0,\ \omega_c-\omega>0$，因此 $x(j\omega) = \frac{1}{2}(1+1)=1$；
  - 当 $\omega>\omega_c$ 时，有 $\omega_c+\omega>0,\ \omega_c-\omega<0$，因此 $x(j\omega) = \frac{1}{1}(1-1)=0$。

  这正是在区间 $[-\omega_c,\omega_c]$ 上高度为 $1$ 的方波的函数表达式。

6. 

7. 

8. $\displaystyle x(j\omega) = \frac{1}{j\omega}+\pi\delta(\omega)$
   $$
   \begin{aligned}
   x(t) &= \frac{1}{2\pi}\int_{-\infty}^{+\infty}\left[\frac{1}{j\omega}+\pi\delta(\omega)\right]e^{j\omega t}\text{d}\omega \\
   &= \frac{1}{2\pi}\int_{-\infty}^{+\infty}\frac{1}{j\omega}e^{j\omega t}\text{d}\omega  + \frac{1}{2}\int_{-\infty}^{+\infty}\delta(\omega)e^{j\omega t}\text{d}\omega \\
   &= \frac{1}{2\pi}\int_{-\infty}^{+\infty}\frac{1}{j\omega}(\cos(\omega t)+j\sin(\omega t))\text{d}\omega + \frac{1}{2} \\
   &= \frac{1}{2\pi}\int_{-\infty}^{+\infty}\frac{1}{j\omega}\cos(\omega t)\text{d}\omega  + \frac{1}{2\pi}\int_{-\infty}^{+\infty}\frac{\sin(\omega t)}{\omega}\text{d}\omega + \frac{1}{2} \\
   &= \frac{1}{2\pi}\int_{-\infty}^{+\infty}\frac{\sin(\omega t)}{\omega}\text{d}\omega + \frac{1}{2} \\
   \end{aligned}
   $$
   由于 
   $$
   \frac{1}{2\pi}\int_{-\infty}^{+\infty}\frac{\sin(\omega t)}{\omega}\text{d}\omega = 
   \begin{cases}
   \frac{1}{2}\quad t>0 \\
   -\frac{1}{2}\quad t<0
   \end{cases}
   $$
   所以 $x(t) = u(t)$。

   或者令 $x(t) = u(t)$
   $$
   \begin{aligned}
   x(j\omega) &= \int_{-\infty}^{+\infty}u(t)e^{-j\omega t}\text{d}t \\
   &= \int_{0}^{+\infty}e^{-j\omega t}\text{d}t \\
   &= \frac{1}{j\omega}e^{-j\omega t}\Bigg|_{+\infty}^0 \\
   &= \frac{1}{j\omega}\left[1-\lim_{N\to+\infty}e^{-j\omega N}\right] \\
   &= \frac{1}{j\omega} - \lim_{N\to+\infty}\frac{e^{-j\omega N}}{j\omega} \\
   &= \frac{1}{j\omega} - \lim_{N\to+\infty}\frac{\cos(\omega N)-j\sin(\omega N)}{j\omega} \\
   &= \frac{1}{j\omega} - \lim_{N\to+\infty}\frac{\cos(\omega N)}{j\omega} + \lim_{N\to+\infty}\frac{\sin(\omega N)}{\omega} \\
   &= \frac{1}{j\omega} - \lim_{N\to+\infty}\frac{\cos(\omega N)}{j\omega} + \pi\delta(t)
   \end{aligned}
   $$
   接下来证明 $\displaystyle \lim_{N\to+\infty}\frac{\cos(\omega N)}{j\omega}=0$，也就是证明 $\displaystyle \lim_{N\to+\infty}\frac{\cos(\omega N)}{\omega}=0$。根据勒贝格积分定理，只需证对于任意的 $y(\omega)$，有 
   $$
   I = \int_{-\infty}^{+\infty}y(\omega)\left[\lim_{N\to+\infty}\frac{\cos(\omega N)}{j\omega}\right]\text{d}\omega = 0
   $$
   对其进行如下变换
   $$
   \begin{aligned}
   I
   &= \lim_{N\to+\infty}\int_{-\infty}^{+\infty}\frac{y(\omega)}{\omega}\cos(\omega N)\text{d}\omega \\
   &= \lim_{N\to+\infty}\int_{-\infty}^{+\infty}\frac{y(\omega)-y(0)}{\omega}\cos(\omega N)\text{d}\omega +y(0)\lim_{N\to+\infty}\int_{-\infty}^{+\infty}\frac{\cos(\omega N)}{\omega}\text{d}\omega \\
   \end{aligned}
   $$
   设 
   $$
   f(\omega) = 
   \begin{cases}
   y'(0)\quad \omega = 0 \\\\
   \displaystyle \frac{y(\omega)-y(0)}{\omega} \omega\neq0
   \end{cases}
   $$
   由于 $f(\omega)$ 满足狄里赫利条件，所以根据[引理3](#lemma3)，有 $I=0$。 因此有 $\displaystyle x(j\omega) = \frac{1}{j\omega}+\pi\delta(\omega)$。

   



> e.g. 求在区间 $\left[-5,5\right]$ 上高度为 $2$ 的方波的傅里叶变换

根据公式 4，可知 $\frac{\tau}{2}=5,\ E=2$，那么代入结果，有 $\displaystyle x(j\omega) = \frac{2\cdot2\sin(5\omega)}{\omega} = \frac{4\sin(5\omega)}{\omega}$

> e.g. 求 $x(j\omega)=7\text{Sa}(2\omega)$ 的傅里叶反变换

根据公式 4，可知 $E\tau = 7,\ \frac{\tau}{2}=2$，那么就有 $E = \frac{7}{4}$，因此 $x(t)$ 为在区间 $\left[-2,2\right]$ 上高度为 $\frac{7}{4}$ 的方波。



## 离散时间傅里叶变换
