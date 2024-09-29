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

> e.g. 求函数 $f(z) = x+2yi$ 的导数

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

#### 复变函数在一点可导的充要条件

复变函数 $f(z)$ 在复平面上一点 $z_0$ 可导的条件是

$$
\lim_{\Delta{z}\to0}\frac{f(z_0+\Delta{z})-f(z_0)}{\Delta{z}}
$$

存在且在各个方向上相等。

#### 复变函数在区域内解析的充要条件(柯西-黎曼方程)

对于函数 $f(z) = u+vi$ 在 $\mathbb{D}$ 内有定义，那么若 $u, v$ 可微，且满足

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

对于一个解析函数，我们可以得到其导数为

$$
f'(z)=\frac{\partial u}{\partial x}+i\frac{\partial v}{\partial x}
$$

> e.g. 判断函数 $f(z)=z^2$ 是否解析

$z^2 = (x+iy)^2=x^2-y^2+2xyi$，令 $u=x^2-y^2,v=2xy$。

经计算，该函数满足 C-R 方程，因此在定义域内解析。

> e.g. 判断函数 $f(z)=\vert z\vert^2$ 是否解析

$\vert z\vert^2 = x^2+y^2+0i$，令 $u=x^2+y^2,v=0$。

$\displaystyle \frac{\partial u}{\partial x}=2x,\frac{\partial v}{\partial y}=0, \frac{\partial v}{\partial x}=0,\frac{\partial u}{\partial y}2y$。若 C-R 方程成立，需满足 $x=y=0$。因此该函数仅在复平面上一点 $(0,0)$ 可导，在定义域内不解析。

## 初等函数

### 指数函数

- 定义
  
  $$
  \exp(z)=e^x(\cos{y}+i\sin{y}) = e^{x+iy} = e^z
  $$
  
- 导数
  
  $$
  \exp'(z)=\exp(z)
  $$
  
- 性质

  $e^{z_1}e^{z_2}=2^{z_1+z_2}$

  $\exp(z)$ 是周期函数，且周期为 $T=2k\pi i$

### 对数函数

- 定义
  
  $$
  \text{Ln}z = \ln{z}+2k\pi i = (\ln{r}+i\theta)+2k\pi i = (\ln{\vert z\vert}+i\arg{z})+2k\pi i
  $$
  
  其中 $\ln{z}$ 称为对数主值。

- 导数
  
  $$
  (\ln{z})'=\frac{1}{z}
  $$
  
- 性质

  $\text{Ln}{z_1z_2} = \text{Ln}z_1+\text{Ln}z_2$

  $\displaystyle \text{Ln}\frac{z_1}{z_2} = \text{Ln}z_1-\text{Ln}z_2$

  **注意: $\text{Ln}z^2\neq 2\text{Ln}z$**

### 幂函数

- 定义
  
  $$
  z^n = e^{n\text{Ln}z} \\
  z^{\frac{1}{n}} = e^{\frac{1}{n}\text{Ln}z} = e^{\frac{1}{n}(\ln{z}+2k\pi i)} \\
  z^{\frac{m}{n}} = (z^{\frac{1}{n}})^m
  $$

- 导数
  
  $$
  (z^n)' = nz^{n-1} \\
  (z^\alpha)' = (e^{\alpha\text{Ln}z})' = \alpha z^{\alpha-1}(在正实轴上)
  $$

### 三角函数

- 定义
  
  $$
  \cos{z} = \frac{e^{iz}+e^{-iz}}{2} \\
  \sin{z} = \frac{e^{iz}-e^{-iz}}{2i} \\
  $$
  
- 导数
  
  $$
  (\sin{z})' = \cos{z} \\
  (\cos{z})' = -\sin{z} \\
  $$

- 性质

  $\cos{z},\sin{z}$ 均为周期函数，且周期为 $T=2\pi$

  $\sin^2{z+\cos^2{z}=1}$ 

### 反三角函数

- 定义
  
  $$
  \text{Arcsin}z = -i\text{Ln}(iz+\sqrt{1-z^2}) \\
  \text{Arcsin}z = -i\text{Ln}(z+\sqrt{z^2-1}) \\
  $$
  
  **注意：上式中根号有正负两个值。**

## 积分

### 复变函数积分的概念

#### 复变函数的积分与性质

- 积分

  复变函数的积分与实函数类似，仍然是四步：分割、近似替代、求和、取极限。

  关于定义此处不再赘述。

- 性质

  - 线性
    
    $$
    \int_C[f(z)+g(z)]\text{d}z = \int_Cf(z)\text{d}z+\int_{C}g(z)\text{d}z
    $$

  - 可加性
    
    $$
    \int_{C} = \int_{C_1}+\int_{C_2}
    $$

  - 最大值
    
    $$
    \left| \int_Cf(z)\text{d}z \right|\leqslant\int_C\vert f(z)\vert\text{d}S\leqslant M\int_C{1\text{d}S} = M\cdot L
    $$

  - 方向性
    
    $$
    \int_{C^-}f(z)\text{d}z = -\int_C f(z)\text{d}z
    $$
    特别地，对于封闭区域 $C$，在其区域上的积分记作 $\displaystyle \oint_Cf(z)\text{d}z$。

- 与实函数积分的关系

  对于 $f(z)=u+iv,\ z = x+iy$，有 $\displaystyle \text{d}z = \frac{\partial z}{\partial x}\text{d}x+\frac{\partial z}{\partial y}\text{d}y = 1\text{d}x+i\text{d}y$。

  那么就有 $\displaystyle \int_Cf(z)\text{d}z = \int_C(u+iv)(\text{d}x+i\text{d}y) = \int_C{u\text{d}x-v\text{d}y}+i\int_C{v\text{d}x+u\text{d}y}$。

  对于上式中实函数积分的部分，不难看出其形式符合 $\displaystyle \int{P\text{d}x+Q\text{d}y}$，也就是第二类曲面积分。

#### 复变函数积分的计算

若一点 $z$ 在曲线 $C$ 上，且满足曲线 $C$ 的方程，那么可以将曲线 $C$ 用参数方程表示

$$
C:
\begin{cases}
x=x(t) \\
y=y(t) \\
\end{cases} 
\quad
\alpha\leqslant t\leqslant\beta
$$

此时有

$$
z=z(t)=x(t)+iy(t) \\
\text{d}z = (x'(t)+iy'(t))\text{d}t = z'(t)\text{d}t \\
\int_C{f(z)}\text{d}z = \int_{\alpha}^{\beta}{f(z(t))\cdot z'(t)\text{d}t}
$$

> e.g. 计算 $\displaystyle \int_C{z^2\text{d}z}$，其中 $C$ 是从点 $(0,0)$ 到点 $(2,1)$ 的直线段。

不难设出 $x=2t,y=t,t\in[0,1],z=2t+it,\text{d}z = (2+i)\text{d}t$。那么积分变为

$$
\int_C{f(z)\text{d}z} = \int_0^1{(2t+it)^2(2+i)\text{d}t} = \frac{2+11i}{3}
$$

> e.g. 计算从 $A=-i$ 到 $B=i$ 的积分 $\displaystyle \int_C{\vert z\vert\text{d}z}$，其中 $C$ 为
>
> (1) 线段 $AB$
>
> (2) 逆时针方向从 $A$ 到 $B$ 的单位圆周

(1) 对于本问，有 $x=0, y\in[-1,1],z = x+iy=iy,\vert z\vert=\vert y\vert, \text{d}z = i\text{d}y$。那么积分就是 

$$
\int_C{\vert z\vert\text{d}z} = \int_{-1}^{1}\vert y\vert i\text{d}y = i\int_0^1 y\text{d}y = i
$$

(2) 对于本问，有 $\displaystyle C:z = e^{i\theta},\theta\in \left[-\frac{\pi}{2},\frac{\pi}{2}\right],\vert z\vert=1,\text{d}z = (-\sin\theta+i\cos\theta)\text{d}\theta$。那么积分就是

$$
\int_C \vert z\vert\text{d}z = \int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}1\cdot (\sin\theta+i\cos\theta)\text{d}\theta = \int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\sin\theta\text{d}\theta + i\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\cos\theta\text{d}\theta = 2i
$$

> e.g. 证明$\displaystyle \oint_C \frac{1}{(z-z_0)^{n+1}}\text{d}z = \begin{cases}2\pi i \quad n=0\\ 0 \quad n=\pm1, \pm2, \cdots\end{cases}$，其中 $C$ 为 $\vert z-z_0\vert=r$，$r$ 为任意值。

不难看出 $z = z_0+re^{i\theta},\text{d}z = ire^{i\theta}\text{d}\theta$。那么积分就是

$$
\oint_C \frac{1}{(z-z_0)^{n+1}}\text{d}z = \int_0^{2\pi}\frac{ire^{i\theta}\text{d}\theta}{(re^{i\theta})^{n+1}} =\frac{i}{r^n}\int_0^{2\pi}e^{-in\theta}\text{d}\theta
$$

对于 $n=0$ 时，有 $\displaystyle I = \frac{i}{r^0}2\pi = 2\pi i$，

对于 $n=\pm1, \pm2,\cdots$，有 $\displaystyle I = \frac{i}{r^n}\int_0^{2\pi}(\cos{n\theta}-i\sin{n\theta})\text{d}\theta$。

> e.g. 计算 $\displaystyle \oint_{\vert z\vert=2}\frac{\overline{z}}{\vert z\vert}\text{d}z$。

根据上一题的结论，可以做出如下转化

$$
\oint_{\vert z\vert=2}\frac{\overline{z}}{\vert z\vert}\text{d}z = \oint_{\vert z\vert=2}\frac{\frac{\vert z\vert^2}{z}}{\vert z\vert}\text{d}z = \oint_{\vert z\vert=2}\frac{\vert z\vert}{z}\text{d}z = \oint_{\vert z\vert=2}\frac{2}{z}\text{d}z = 2\oint_{\vert z\vert=2}\frac{1}{z}\text{d}z = 2\cdot2\pi i = 4\pi i
$$

### 柯西-古萨定理

若函数 $f(z)$ 在单连通区域 $D$ 内解析，则对于任意 $D$ 内的封闭曲线 $C$，总满足

$$
\oint_Cf(z)\text{d}z = 0
$$

此处仅给出当满足 $f'(z)$ 连续情况下的证明。

$$
\begin{aligned}
\oint_Cf(z)\text{d}z &= \oint_C(u+iv)(\text{d}x+i\text{d}y) \\
&= \oint_C u\text{d}x-v\text{d}y+i\oint_C v\text{d}x+u\text{d}y \\
&= \iint_G\left(-\frac{\partial v}{\partial x}-\frac{\partial u}{\partial y}\right)\text{d}x\text{d}y + i\iint_G\left(\frac{\partial u}{\partial x}-\frac{\partial v}{\partial y}\right)\text{d}x\text{d}y \\
&= 0
\end{aligned}
$$

> e.g. 计算 $\displaystyle \oint_{\vert z\vert=1}\frac{1}{\cos{z}}\text{d}z$

首先判断函数的奇点，也就是满足 $\cos{z}=0$ 的点，显然 $z = k\pi + \frac{\pi}{2}$。对于任意的 $k\in\mathbb{Z}$，都有 $\vert z\vert>1$。也就是说 $\frac{1}{\cos{z}}$ 在 $\vert z\vert<1$ 区域内解析，因此积分为 $0$。

**Morera 定理：若 $f(z)$ 在单连通区域 $D$ 连续，且对于任意简单封闭曲线的积分为 $0$，那么 $f(z)$ 在区域 $D$ 内解析。**

### 复合闭路定理

将柯西-古萨定理推广到多连通区域的情况，我们就得到了复合闭路定理。

假设存在内部有 $n$ 个空洞的多连通区域 $D$，函数 $f(z)$ 在区域 $D$ 内解析，且在各边界连续，那么有

$$
\int_C+\int_{C_1^-}+\int_{C_2^-}+\cdots+\int_{C_n^-}=0 \\
\begin{aligned}
\oint_C &= -\int_{C_1^-}-\int_{C_2^-}-\cdots-\int_{C_n^-} \\
&=\oint_{C_1}+\oint_{C_2}+\cdots+\oint_{C_n}
\end{aligned}
$$

所以复合闭路定理的表达式为

$$
\oint_C f(z)\text{d}z = \sum_{k=1}^{n}\oint_{C_k}f(z)\text{d}z
$$

> e.g. 计算 $\displaystyle \oint_C\frac{\cos{z}}{z}\text{d}z$，其中 $C$ 由 $\vert z\vert=2$ 的逆时针方向和 $\vert z\vert=1$ 的顺时针方向构成

显然函数仅在 $z=0$ 处不解析，在所求区域内解析，因此根据复合闭路定理，有

$$
\oint_C\frac{\cos{z}}{z}\text{d}z=0
$$

> e.g. 计算 $\displaystyle \oint_{\vert z\vert=\frac{1}{2}}\frac{1}{z^2-z}\text{d}z$

显然函数的奇点为 $z=0$ 和 $z=1$。其中 $z=0$ 在所求区域内部，令 $C_1:\vert z\vert=r$ 为环绕 $z=0$ 的一个小空洞，那么根据复合闭路定理，有

$$
\begin{aligned}
\oint_{\vert z\vert=\frac{1}{2}}\frac{1}{z^2-z}\text{d}z &= \oint_{C_1}\frac{1}{z^2-z}\text{d}z \\
&=\oint_{C_1}\frac{1}{z(z-1)}\text{d}z \\
&= \oint_{C_1}\left(\frac{1}{z-1}-\frac{1}{z}\right)\text{d}z \\
&= \oint_{C_1}\frac{1}{z-1}\text{d}z - \oint_{C_1}\frac{1}{z}\text{d}z \\
&= 0-2\pi i \\
&= -2\pi i
\end{aligned}
$$

> e.g. 计算 $\displaystyle \oint_{\vert z\vert=\frac{1}{2}}\frac{1}{z^2-z}\text{d}z$，其中 $C$ 是把 $\vert z\vert=1$ 包围的任意简单闭曲线

在上一题的基础上，额外地令 $C_2:\vert z-1\vert=r$ 为环绕 $z=1$ 的一个小空洞，那么有

$$
\begin{aligned}
\oint_{\vert z\vert=\frac{1}{2}}\frac{1}{z^2-z}\text{d}z &= \oint_{C_1}\frac{1}{z^2-z}\text{d}z + \oint_{C_2}\frac{1}{z^2-z}\text{d}z \\
&= -2\pi i + \oint_{C_2}\left(\frac{1}{z-1}-\frac{1}{z}\right)\text{d}z \\
&= -2\pi i + \oint_{C_2}\frac{1}{z-1}\text{d}z - \oint_{C_2}\frac{1}{z}\text{d}z \\
&= -2\pi i+2\pi i-0 \\
&= 0
\end{aligned}
$$

### 积分计算的总结

对于以下三种情况积分，需要记住。

- $\displaystyle \oint_C{f(z)\text{d}z}=0$，若 $f(z)$ 是在 $C$ 所围成的 $D$ 区域内解析。
- $\displaystyle \oint_C f(z)\text{d}z = \sum_{k=1}^{n}\oint_{C_k}f(z)\text{d}z$，其中 $n$ 是函数 $f(z)$ 的奇点数。
- $\displaystyle \oint_C \frac{1}{(z-z_0)^{n+1}}\text{d}z = \begin{cases}2\pi i \quad n=0\\ 0 \quad n=\pm1, \pm2, \cdots\end{cases}$

