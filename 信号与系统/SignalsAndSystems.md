# 信号与系统

## 绪论

### 信号

信号是表达、传递信息的符号。

根据香农的定义，信息量的值为 $-\log[p(x)]$，信息熵的定义为 $-\sum{p(x)\log[p(x)]} = E[-\log{p(x)}]$。

本课程研究成本低、简洁、传输速度快、传输可靠的信号。

### 系统

系统是接受输入信号，并把输入信号转换为输出信号的实体。

多个基本系统级联起来能构成复杂系统。

## 典型的信号

### 信号的描述与分类

- 基于信号维度的分类

  - 一维信号
  - 二维信号
  - 三维信号
  - 四维信号

  在本课程中，我们仅仅讨论一维信号。

### 连续信号与离散信号

一维信号按自变量的取值是否连续可分为连续时间信号和离散时间信号。

- 连续信号

  连续时间信号：在任何时刻除了若干个不连续点外都有定义的信号。

  连续信号表示方法： $x(t)$。

- 离散信号

  离散时间信号：仅在一系列特定的、离散的时间点上有定义的信号。

  离散信号表示方法： $x[n]$。

### 周期信号与非周期信号

- 周期信号

  周期信号：信号随时间变量 $t$ 或 $n$ 变化，具有重复性。

  连续周期信号满足 $x(t) = x(t+mT)\ (m\in \mathbb{Z})$，其中 $T$ 称为连续信号的最小正周期。

  离散周期信号满足 $x[n] = x[n+mN],\ (m\in\mathbb{Z})$，其中 $N$ 是自然数，$N$ 称为离散信号的最小正周期。

- 非周期信号

  不满足上述周期信号性质的信号是非周期信号。

### 奇信号与偶信号

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

### 功率信号与能量信号

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

### 奇异信号

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
  
- 

### 其他连续时间信号

- 抽样函数

  抽样函数记作 $Sa(t)$，定义为
  $$
  Sa(t) = \frac{\sin(t)}{t} \quad or \quad \sin{c(t)} = \frac{\sin(\pi t)}{\pi t}
  $$
  特别地，在 $t=0$ 时抽样函数满足
  $$
  Sa(t) = 1
  $$
  抽样函数具有以下性质
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

### 单位冲激序列与单位阶跃序列

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
  

