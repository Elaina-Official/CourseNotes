# 复变函数

## 复数及复变函数的基本定义

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

假设 $f(z) = u(x,y)+iv(x,y)$，则 $\underset{z\to z_0}{\lim}f(z) = \underset{(x,y)\to(x_0,y_0)}{\lim}f(z) = A = u_0+iv_0$ 满足

$\underset{(x,y)\to(x_0,y_0)}{\lim}u(x,y)=u_0,\ \underset{(x,y)\to(x_0,y_0)}{\lim}v(x,y)=v_0$

对于 $A =f(z_0)$，若存在 $\underset{z\to z_0}{\lim}f(z) = f(z_0)$，则称 $f(z)$ 在 $z_0$ 处连续

若 $f(z)$ 在区域 $D$ 内每一点都连续，则称 $f(z)$ 在区域 $D$ 上连续

连续函数的四则运算和复合仍是连续函数
