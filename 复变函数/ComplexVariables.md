# 复变函数

## 复数

### 复数及其代数运算

#### 定义

$z = x + iy,\ i = \sqrt{-1}$

实部: $\text{Re}z$，虚部: $\text{Im}z$

$z_1 = z_2$ 满足 $x_1 = x_2,\ y_1 = y_2$

#### 四则运算

$z_1 \pm z_2 = (x_1\pm x_2)+i(y_1\pm y_2)$

$z_1\cdot z_2 = (x_1+iy_1)\cdot(x_2+iy_2) = (x_1x_2-y_1y_2)+i(x_1y_2+y_1x_2)$

$\displaystyle \frac{z_1}{z_2} = \frac{x_1+iy_1}{x_2+iy_2} = \frac{(x_1+iy_1)(x_2-iy_2)}{(x_2+iy_2)(x_2-iy_2)} = \frac{(x_1x_2+y_1y_2)+i(x_2y_1-x_1y_2)}{x_2^2+y_2^2}$

#### 共轭复数

$z = x+iy,\ \overline{z} = x-iy$

$\overline{z_1\pm z_2} = \overline{z_1} \pm \overline{z_2},\ \overline{z_1\cdot z_2} = \overline{z_1}\cdot\overline{z_2},\ \displaystyle \overline{\left(\frac{z_1}{z_2}\right)} = \frac{\overline{z_1}}{\overline{z_2}}$

$z\cdot\overline{z} = x^2+y^2,\ \displaystyle x = \frac{z+\overline{z}}{2},\ y = \frac{z-\overline{z}}{2i}$

### 复数的表示

#### 复平面

对于复数 $z = x+iy$，其表示复平面上一点 $P(x,y)$

对于从原点出发的向量 $\vec{OP}$，有长度 $r = \sqrt{x^2+y^2} = \vert z\vert$，方向 $\theta = \text{Arg}z$

选定 $-\pi<\theta_0\leqslant\pi$，有 $\theta_0 = \arg{z}$，称为辐角主角，且满足 $\text{Arg}z = \arg{z}+2k\pi$

对于 $\displaystyle \tan\theta = \frac{y}{x}$，应该有 $\displaystyle \theta = \arctan{\frac{y}{x}}$

但是 $\arctan{x}$ 具有范围 $\displaystyle \left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$，因此 $\arg{z}$ 满足

$$
\arg{z} = 
\begin{cases}
\displaystyle \arctan\frac{y}{x}, \theta\in\left(-\frac{\pi}{2}, \frac{\pi}{2}\right) \\\\
\displaystyle \arctan\frac{y}{x} + \pi, \theta\in\left(\frac{\pi}{2}, \pi\right) \\\\
\displaystyle \arctan\frac{y}{x} - \pi, \theta\in\left(-\pi, -\frac{\pi}{2}\right) 
\end{cases}
$$

#### 复数的三角表示及指数表示

三角表示: $z = x+iy = r\cos\theta+ir\sin\theta = r(\cos\theta+i\sin\theta)$

指数形式: $z = re^{i\theta}$

其中 $r = \vert z\vert,\ \theta = \arg{z}$

#### 复数的乘幂和方根

假设存在 $z_1 = r_1(\cos\theta_1+i\sin\theta_1) = r_1e^{i\theta_1},\ z_2 = r_2(\cos\theta_2+i\sin\theta_2) = r_2e^{i\theta_2}$

- 乘积

  $z_1\cdot z_2 = r_1\cdot r_2[\cos(\theta_1+\theta_2)+i\sin(\theta_1+\theta_2)] = r_1\cdot r_2 e^{i(\theta_1+\theta_2)}$

  $\vert z_1\cdot z_2\vert = r_1\cdot r_2 = \vert z_1\vert\cdot\vert z_2\vert,\ \text{Arg}(z_1\cdot z_2) = \text{Arg}z_1+\text{Arg}z_2$

- 商

  $\displaystyle \frac{z_1}{z_2} = \frac{r_1}{r_2}[\cos(\theta_1-\theta_2)+i\sin(\theta_1-\theta_2)] = \frac{r_1}{r_2}e^{i(\theta_1-\theta_2)}$

  $\displaystyle \left| \frac{z_1}{z_2} \right| = \frac{\vert z_1\vert}{\vert z_2\vert},\ \text{Arg}\left(\frac{z_1}{z_2}\right) = \text{Arg}z_1-\text{Arg}z_2$

- 乘幂

  假设 $z = r(\cos\theta+i\sin\theta)$，那么

  $z^n = r^n(\cos\theta+i\sin\theta)^n = r^n(\cos{n\theta}+i\sin{n\theta})$

  $\displaystyle z^{-n} = \frac{1}{z^n}$

  其中 $(\cos\theta+i\sin\theta)^n = (\cos{n\theta}+i\sin{n\theta})$ 可以用指数形式证明: 

  $(\cos\theta+i\sin\theta)^n = (e^{i\theta})^n = e^{i(n\theta)} = (\cos{n\theta}+i\sin{n\theta})$

- 方根

  假设 $w = \rho(\cos\phi+i\sin\phi) = \sqrt[n]{z},\ z = r(\cos\theta+i\sin\theta) = r[\cos(\theta+2k\pi)+i\sin(\theta+2k\pi)]$

  那么 $w^n = \rho^n(\cos{n\phi + i\sin{n\phi}}) = z$

  所以 $\rho^n = r,\ n\phi = \theta+2k\pi$，即

  $\displaystyle w = \sqrt[n]{r}\left[\cos\frac{\theta+2k\pi}{n}+i\sin\frac{\theta+2k\pi}{n}\right],\ k=0,1,2\cdots,n-1$

  所以根式 $\sqrt[n]{z}$ 具有 $n$ 个值，并且 $w$ 的 $n$ 个值均匀分布在圆周上

### 复平面中的区域

- 邻域

  $z_0$ 及其附近一点，即 $\vert z-z_0\vert<\delta$

- 去心邻域

  $z_0$ 附近一点，即 $0 < \vert z-z_0\vert<\delta$

- 内点

  集合内部的点

- 外点

  集合外部的点

- 边界点

  集合边界上的点

- 开集

  所有点均为内点的集合

- 区域

  连通的开集

- 闭区域

  区域与边界的并集

- 有界区域

  距离远点最远处为定值的区域

- 无界区域

  延伸至无穷远处的区域

- 简单曲线

  连续且不自相交的曲线

- 单连通区域

   由单条简单闭曲线围成的区域，对于区域内任意一条简单闭曲线，其总能收缩成区域内一点

- 多连通区域

  不是由单条简单闭曲线围成的区域，区域内总存在一条简单闭曲线，使得其收缩后的点不在区域内

### 复变函数

#### 定义

对于复数 $z = x+iy$，如果经过变换 $f$ 后的结果仍是复数，则称 $f$ 是复变函数

#### 复变函数的极限与连续性

和实函数类似，当且仅当从各个方向趋近一点的值均相同时，复变函数的极限存在

假设 $f(z) = u(x,y)+iv(x,y)$，则 $\underset{z\to z_0}{\lim}f(z) = \underset{(x,y)\to(x_0,y_0)}{\lim}f(z) = A = u_0+iv_0$ 满足oner

$\underset{(x,y)\to(x_0,y_0)}{\lim}u(x,y)=u_0,\ \underset{(x,y)\to(x_0,y_0)}{\lim}v(x,y)=v_0$

对于 $A =f(z_0)$，若存在 $\underset{z\to z_0}{\lim}f(z) = f(z_0)$，则称 $f(z)$ 在 $z_0$ 处连续

若 $f(z)$ 在区域 $\mathbb{D}$ 内每一点都连续，则称 $f(z)$ 在区域 $\mathbb{D}$ 上连续

连续函数的四则运算和复合仍是连续函数

#### 复变函数的导数与微分

- 导数

  若 $w = f(z)$ 在 $\mathbb{D}$ 内有定义，$z\in \mathbb{D},\ z+\Delta{z}\in \mathbb{D},\ \Delta{w} = f(z+\Delta{z})-f(z)$，且 $\displaystyle \lim_{\Delta{z}\to0}\frac{\Delta{w}}{\Delta{z}} = \lim_{\Delta{z}\to0}\frac{f(z+\Delta{z})-f(z)}{\Delta{z}}$ 存在，则 $\displaystyle f'(z)=\frac{\text{d}w}{\text{d}z}$。其中 $\Delta{z}\to0$ 等价于 $\Delta{x}+i\Delta{y}\to0(\Delta{x}\to0,\ \Delta{y}\to0)$。

- 微分

  $\Delta{w} = f(z+\Delta{z})-f(z) = A\Delta{z}+o(\vert \Delta{z}\vert)$

和实函数类似，复变函数的可导与可微实际上是一样的，也就是 $\text{d}w = A\Delta{z} = f'(z)\text{d}z$。

> e.g. 求函数 $f(z) = z^2$ 的导数

$\displaystyle f'(z) = \lim_{\Delta{z}\to0}\frac{f(z+\Delta{z})-f(z)}{\Delta{z}} =  \lim_{\Delta{z}\to0}\frac{(z+\Delta{z})^2-z^2}{\Delta{z}} = 2z$。

类似地，有 $(z^n)' = nz^{n-1}(n\in \mathbb{Z})$。

> e.g. 求函数 $f(z) = x+2yi$ 的导数。

$$
\begin{aligned}
f'(z) &= \lim_{\Delta{z}\to0}\frac{f(z+\Delta{z})-f(z)}{\Delta{z}} \\
&= \lim_{\Delta{z}\to0}\frac{(x+\Delta{z})+2(y+\Delta{y})i-(x+2yi)}{\Delta{x}+i\Delta{y}} \\
&= \lim_{(\Delta{x},\Delta{y})\to(0,0)}\frac{\Delta{z}+2\Delta{y}i}{\Delta{x}+i\Delta{y}} \\
&\xlongequal{\Delta{y}=k\Delta{x}}\frac{\Delta{x}+2k\Delta{x}i}{\Delta{x}+k\Delta{x}i} \\
&= \frac{1+2ki}{1+ki}
\end{aligned}
$$

所以 $f'(z)$ 不存在。

## 解析函数

### 解析函数的概念

若 $w = f(z)$ 在 $\mathbb{D}$ 内有定义，则 $f(z)$ 在 $z_0$ 解析等价于 $f(z)$ 在 $z_0$ 附近可导。

定义：若 $f(z)$ 在 $\mathbb{D}$ 可导，则其在 $\mathbb{D}$ 内的每一点都可导；若 $f(z)$ 在 $\mathbb{D}$ 解析，则其在 $\mathbb{D}$ 内处处解析。

### 复变函数的求导

#### 奇点

$f(z)$ 不解析的点叫做奇点。

> e.g. 求函数 $\displaystyle f(z) = \frac{1}{z^3+27}$ 的奇点

$f(z) = 0$ 时不解析，所以使得 $z^3+27=0$ 的点是奇点，$z = -3,\ z = \sqrt[3]{-27}$。

#### 复变函数的求导公式与法则

- $(C)' = 0$
- $(z^n)' = nz^{n-1}(n\in\mathbb{N})$
- $(f\pm g)' = f'\pm g'$
- $(f\cdot g)' = f'\cdot g+f\cdot g'$
- $\displaystyle \left(\frac{f}{g}\right)' = \frac{f'\cdot g-f\cdot g'}{g^2}$
- $[f(g(z))]' = f'(g(z))g'(z)$
- $\displaystyle \frac{\text{d}w}{\text{d}z} = \frac{1}{\frac{\text{d}z}{\text{d}w}}$

#### 解析函数的充要条件(C-R方程)

对于函数 $f(z) = u+vi$，若 $f(z)$ 在 $\mathbb{D}$ 内有定义，$u, v$ 可微，且满足
$$
\begin{cases}
\displaystyle \frac{\partial u}{\partial x} = \frac{\partial v}{\partial y} \\
\displaystyle \frac{\partial u}{\partial y} = -\frac{\partial v}{\partial x}
\end{cases}
$$
则该函数在 $\mathbb{D}$ 上是解析的。

上述方程组叫做柯西-黎曼方程(Cauchy-Riemann Equations, C-R Equations)。

证明如下

若 $\displaystyle f'(z)=\lim_{\Delta{z}\to0}\frac{f(z+\Delta{z})-f(z)}{\Delta{z}}$ 存在，则有
$$
f(z+\Delta{z})-f(z) = f'(z_0)\Delta{z}+o(\vert\Delta{z}\vert) \\
\Delta{u}+i\Delta{v} = (a+ib)(\Delta{x}+i\Delta{y})+o(\vert\Delta{z}\vert) \\
\Delta{u}+i\Delta{v} = (a\Delta{x}-b\Delta{y})+i(b\Delta{x}+a\Delta{y})+o(\vert\Delta{z}\vert) \\
$$
通过 $u, v$ 可微，我们可以得到
$$
\Delta{u} = a\Delta{x}-b\Delta{y}+o(\vert\Delta{z}\vert) \\
\Delta{v} = b\Delta{x}+a\Delta{y}+o(\vert\Delta{z}\vert) \\
$$
所以得到
$$
a = \frac{\partial u}{\partial x}\quad -b = \frac{\partial u}{\partial y} \\
b = \frac{\partial v}{\partial x}\quad a = \frac{\partial v}{\partial y} \\
$$
整理之后可得 C-R 方程。
