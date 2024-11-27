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
\begin{array}{ll}
\displaystyle \arctan\frac{y}{x} & \theta\in\left(-\frac{\pi}{2}, \frac{\pi}{2}\right) \\
\displaystyle \arctan\frac{y}{x} + \pi & \theta\in\left(\frac{\pi}{2}, \pi\right) \\
\displaystyle \arctan\frac{y}{x} - \pi & \theta\in\left(-\pi, -\frac{\pi}{2}\right) 
\end{array}
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

对于复数 $z = x+iy$，如果经过变换 $f$ 后的结果仍是复数，则称 $f$ 是复变函数。

#### 复变函数的极限与连续性

和实函数类似，当且仅当从各个方向趋近一点的值均相同时，复变函数的极限存在。

假设 $f(z) = u(x,y)+iv(x,y)$，则 $\underset{z\to z_0}{\lim}f(z) = \underset{(x,y)\to(x_0,y_0)}{\lim}f(z) = A = u_0+iv_0$ 满足 $\underset{(x,y)\to(x_0,y_0)}{\lim}u(x,y)=u_0,\ \underset{(x,y)\to(x_0,y_0)}{\lim}v(x,y)=v_0$。

对于 $A =f(z_0)$，若存在 $\underset{z\to z_0}{\lim}f(z) = f(z_0)$，则称 $f(z)$ 在 $z_0$ 处连续。

若 $f(z)$ 在区域 $\mathbb{D}$ 内每一点都连续，则称 $f(z)$ 在区域 $\mathbb{D}$ 上连续。

连续函数的四则运算和复合仍是连续函数。

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

$\displaystyle \frac{\partial u}{\partial x}=2x,\frac{\partial v}{\partial y}=0, \frac{\partial v}{\partial x}=0,\frac{\partial u}{\partial y}=2y$。若 C-R 方程成立，需满足 $x=y=0$。因此该函数仅在复平面上一点 $(0,0)$ 可导，在定义域内不解析。

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
\int_C \vert z\vert\text{d}z = \int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}1\cdot (-\sin\theta+i\cos\theta)\text{d}\theta = -\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\sin\theta\text{d}\theta + i\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\cos\theta\text{d}\theta = 2i
$$

> e.g. 证明$\displaystyle \oint_C \frac{1}{(z-z_0)^{n+1}}\text{d}z = \begin{cases}2\pi i \quad n=0\\ 0 \quad n=\pm1, \pm2, \cdots\end{cases}$，其中 $C$ 为 $\vert z-z_0\vert=r$，$r$ 为任意值。

不难看出 $z = z_0+re^{i\theta},\text{d}z = ire^{i\theta}\text{d}\theta$。那么积分就是

$$
\oint_C \frac{1}{(z-z_0)^{n+1}}\text{d}z = \int_0^{2\pi}\frac{ire^{i\theta}\text{d}\theta}{(re^{i\theta})^{n+1}} =\frac{i}{r^n}\int_0^{2\pi}e^{-in\theta}\text{d}\theta
$$

对于 $n=0$ 时，有 $\displaystyle I = \frac{i}{r^0}2\pi = 2\pi i$，

对于 $n=\pm1, \pm2,\cdots$，有 $\displaystyle I = \frac{i}{r^n}\int_0^{2\pi}(\cos{n\theta}-i\sin{n\theta})\text{d}\theta = 0$。

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

首先判断函数的奇点，也就是满足 $\cos{z}=0$ 的点，显然 $z = k\pi + \frac{\pi}{2}$。对于任意的 $k\in\mathbb{Z}$，都有 $\vert z\vert>1$。也就是说 $\frac{1}{\cos{z}}$ 在 $\vert z\vert\leqslant 1$ 区域内解析，因此积分为 $0$。

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

显然函数的奇点为 $z=0$ 和 $z=1$。其中 $z=0$ 在所求区域内部，令 $C_1:\vert z\vert=r$ 为环绕 $z=0$ 的一个小空心圆，那么根据复合闭路定理，有

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

> e.g. 计算 $\displaystyle \oint_{C}\frac{1}{z^2-z}\text{d}z$，其中 $C$ 是把 $\vert z\vert=1$ 包围的任意简单闭曲线

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

### 不定积分与定积分

#### 原函数与不定积分

定义 $F(z) = \displaystyle \int_{z_0}^{z}f(\xi)\text{d}\xi$，则有 $F'(z) = f(z)$。若函数 $f(z)$ 在区域 $D$ 内解析，且有 $\phi'(z)=f(z)$，那么 $\phi(z)$ 为 $f(z)$ 在区域 $D$ 内的原函数，$F(z)$ 为 $f(z)$ 的一个原函数，不定积分为 $\displaystyle\int f(z)\text{d}z = F(z)+C$，$C$ 为任意常数。

#### 牛顿-莱布尼茨公式与定积分

对于复变函数，仍有牛顿-莱布尼茨公式(Newton-Leibniz Formula)，即 $\displaystyle \int_{z_0}^{z_1}f(z)\text{d}z = F(z)\Bigg|_{z_0}^{z_1} = F(z_1)-F(z_0)$。

> e.g. 计算 $\displaystyle \int_{0}^{i}\cos{z}\text{d}z$

不难写出 $\displaystyle \int_{0}^{i}\cos{z}\text{d}z = \sin{z}\Bigg|_0^i = \frac{e-e^{-1}}{2}i$。

### 柯西积分

若 $f(z)$ 在由曲线 $C$ 围成的区域 $D$ 内解析，且 $f(z)$ 在 $C$ 上正向连续，那么有
$$
\oint_C\frac{f(z)}{z-z_0}\text{d}z = 2\pi if(z_0)
$$
此时可以得到 $\displaystyle f(z_0) = \frac{1}{2\pi i}\oint_{\vert z-z_0\vert=r}\frac{f(z)}{z-z_0}\text{d}z$。由于 $z-z_0=r$ 代表距离点 $z_0$ 距离为 $r$ 的圆周，因此我们可以用 $re^{i\theta} \ 0\leqslant\theta\leqslant2\pi$ 替代 $z-z_0$。则有 $\displaystyle f(z_0) = \frac{1}{2\pi i}\int_0^{2\pi}\frac{f(z_0+re^{i\theta})}{re^{i\theta}}ire^{i\theta}\text{d}\theta = \frac{1}{2\pi}\int_0^{2\pi}f(z_0+re^{i\theta})\text{d}\theta$，这也就意味着解析函数在圆心处的取值等于圆周上的平均值。

对于柯西积分，我们使用 $\xi$ 替代 $z$，并对于区域 $D$ 内任意一点 $z$，有 $\displaystyle \forall z\in D, f(z) = \oint_C\frac{f(\xi)}{\xi-z}\text{d}\xi$，这就意味着解析函数 $f(z)$ 在区域 $D$ 内部的点的取值完全由边界上的点确定。

> e.g. 计算 $\displaystyle \oint_{\vert z\vert=2}\frac{\cos{z}}{z}\text{d}z$

该函数的奇点为 $z=0$，那么有 $\displaystyle I = \oint_{C_1}\frac{\cos{z}}{z}\text{d}z = 2\pi i\cdot \cos{z}\Bigg|_{z=0}=2\pi i$。

> e.g. 计算 $\displaystyle \oint_{C}\frac{e^{iz}}{z-\frac{\pi}{2}i}\text{d}z$，其中(1) $C:\vert z\vert=1$，(2) $C:\vert z\vert=2$

该函数的奇点为 $z=\frac{\pi}{2}i$，而 $1<\frac{\pi}{2}<2$。对于(1)，我们发现在区域 $C$ 内没有奇点，因此积分 $I_1=0$。对于(2)，有
$$
I_2 = \displaystyle \oint_{C_1}\frac{e^{iz}}{z-\frac{\pi}{2}i}\text{d}z = 2\pi i\cdot e^{iz}\Bigg|_{z=\frac{\pi}{2}i} = 2i\pi e^{-\frac{\pi}{2}}
$$

> e.g. 计算 $\displaystyle \oint_{\vert z-1-\sqrt{3}i\vert=2}\frac{\ln(1+z)}{z-\sqrt{3}i}\text{d}z$

该函数的奇点为 $z=\sqrt{3}i$，在所求区域内，因此有 
$$
I = \oint_{C_1}\frac{\ln(1+z)}{z-\sqrt{3}i}\text{d}z = 2\pi i\ln(1+z)\Bigg|_{z=\sqrt{3}i} = 2\pi i\ln(1+\sqrt{3}i) = 2i\pi(\ln{2}+i\frac{\pi}{3})
$$

> e.g. 计算 $\displaystyle \oint_{\vert z\vert=2}\frac{1}{z^2-z}\text{d}z$

该函数的奇点为 $z=0,z=1$，因此有
$$
I = \displaystyle \oint_{C_1}\frac{\frac{1}{z-1}}{z-0}\text{d}z + \oint_{C_2}\frac{\frac{1}{z}}{z-1}\text{d}z = 2\pi i\frac{1}{z-1}\Bigg|_{z=0}+2\pi i\frac{1}{z}\Bigg|_{z=1} = 0
$$

> e.g. 计算 $\displaystyle \oint_{\vert z\vert=3}\frac{e^z}{z^2+4}\text{d}z$

该函数的奇点为 $z=2i,z=-2i$，因此有
$$
\displaystyle I = \oint_{C_1}\frac{\frac{e^z}{z+2i}}{z-2i}\text{d}z + \oint_{C_2}\frac{\frac{e^z}{z-2i}}{z-(-2i)}\text{d}z = 2\pi i\frac{e^z}{z+2i}\Bigg|_{z=2i} + 2\pi i\frac{e^z}{z-2i}\Bigg|_{z=-2i} = i\pi\sin2
$$

### 解析函数的高阶导数(柯西积分的推广)

解析函数可求任意阶导数，且导数仍是解析函数。

若函数 $f(z)$ 在 $C_1$ 围成的区域 $D$ 内解析，且在边界 $C$ 连续，则有
$$
f^{(n)}(z_0) = \frac{1}{2\pi i}n!\oint_C\frac{f(z)\text{d}z}{(z-z_0)^{n+1}}
$$
在实际应用中，往往以以下形式给出
$$
\oint_C\frac{f(z)\text{d}z}{(z-z_0)^{n+1}} = \frac{2\pi i}{n!}f^{(n)}(z_0)
$$
解析函数的高阶导数证明如下

根据柯西积分公式，有 $\displaystyle f(z) = \frac{1}{2\pi i}\oint_C\frac{f(\xi)}{\xi-z}\text{d}\xi$。对 $z$ 求导，得
$$
\begin{aligned}
\frac{\text{d}^{(n)}f(z)}{\text{d}z^{(n)}} &= \frac{1}{2\pi i}\oint_C \left[\frac{\text{d}^{(n)}}{\text{d}z^{(n)}}\frac{f(\xi)}{\xi-z}\right]\text{d}\xi \\
&= \frac{1}{2\pi i}n!\oint_C \left[\frac{f(\xi)}{(\xi-z)^{n+1}}\right]\text{d}\xi \\
\end{aligned}
$$

> e.g. 求 $\displaystyle \oint_{\vert z\vert=2}\frac{\cos(5z)}{(z-1)^5}\text{d}z$

该函数显然存在奇点 $z=1$，因此有
$$
\displaystyle I = \oint_{C_1}\frac{\cos(5z)}{(z-1)^5}\text{d}z = 2\pi i\frac{(\cos(5z))^{(4)}}{4!}\Bigg|_{z=1} = \frac{5^4\pi i}{12}\cos(5)
$$

> e.g. 求 $\displaystyle \oint_{\vert z\vert=2}\frac{1}{z^3(z+1)}\text{d}z$

不难发现该函数奇点为 $z=0,z=-1$，因此有
$$
\begin{aligned}
I &= \oint_{\vert z-0\vert=r}\frac{\frac{1}{z+1}}{z^3} + \oint_{\vert z-(-1)\vert=r}\frac{\frac{1}{z^3}}{z-(-1)} \\
&= 2\pi i\frac{\left(\frac{1}{z+1}\right)''}{2!}\Bigg|_{z=0}+2\pi i\frac{1}{z^3}\Bigg|_{z=-1} \\
&= 2\pi i -2\pi i \\
&= 0
\end{aligned}
$$

### 解析函数与调和函数

#### 调和函数

定义：若二元实值函数 $\phi(x,y)$ 的二阶偏导存在且连续，那么若满足 Laplace 方程 $\displaystyle \frac{\partial^2\phi}{\partial x^2} + \frac{\partial^2\phi}{\partial y^2} = 0$，则称 $\phi$ 为调和函数。

> e.g. 证明若 $f(z) = u+iv$ 解析则 $u,v$ 调和

验证 $u$ 是调和的，且解析函数满足 C-R 方程，因此有
$$
\frac{\partial^2u}{\partial x^2} + \frac{\partial^2u}{\partial y^2} =
\frac{\partial^2v}{\partial y\partial x} - \frac{\partial^2v}{\partial x\partial y} = 0 \\
$$
类似地，可以得到 $v$ 也是调和的。

#### 共轭调和函数

定义：若 $u$ 是调和函数，且 $v$ 使得 $u+iv$ 为解析函数，则 $v$ 成为 $u$ 的共轭调和函数。

**求共轭调和函数的三种方法**

已知调和函数 $u$，求共轭调和函数 $v$，其中 $u+iv$ 解析。

- 线积分法

  对于 $v$，我们有 $\text{d}v = \displaystyle \frac{\partial v}{\partial x}\text{d}x+\frac{\partial v}{\partial y}\text{d}y = -\frac{\partial u}{\partial y}\text{d}x+\frac{\partial u}{\partial x}\text{d}y$，

  那么就有
  $$
  v = \int_{(x_0,y_0)}^{(x,y)}\text{d}v+C = \int_{(x_0,y_0)}^{(x,y)}\left(-\frac{\partial u}{\partial y}\text{d}x+\frac{\partial u}{\partial x}\text{d}y\right)+C
  $$
  设 $\displaystyle P(x,y)=-\frac{\partial u}{\partial y},Q(x,y)=\frac{\partial u}{\partial x}$，由于该函数解析，因此积分与路径无关，有
  $$
  v = \int_{(x_0,y_0)}^{(x,y)}P(x,y)\text{d}x+Q(x,y)\text{d}y = \int_{x_0}^{x}P(x,y_0)\text{d}x+\int_{y_0}^{y}Q(x,y)\text{d}y
  $$

  > e.g. 已知 $u = y^3-3x^2y$，证明 $u$ 是调和函数，并求出其共轭调和函数 $v$，其中 $f(z)=u+iv$ 解析

  根据题目可知 $\displaystyle \frac{\partial u}{\partial x} = -6xy,\frac{\partial u}{\partial y} = 3y^2-3x^2,\frac{\partial^2 u}{\partial x^2} = -6y,\frac{\partial^2 u}{\partial y^2} = 6y$，显然满足 $\displaystyle \frac{\partial^2u}{\partial x^2} + \frac{\partial^2u}{\partial y^2} = 0$，因此 $u$ 是调和函数。对于 $v$，取 $(x_0,y_0) = (0,0)$，有
  $$
  \begin{aligned}
  v &= \int_{(x_0,y_0)}^{(x,y)}\left(-\frac{\partial u}{\partial y}\text{d}x+\frac{\partial u}{\partial x}\text{d}y\right)+C \\
  &= \int_{(x_0,y_0)}^{(x,y)}(3x^2-3y^2)\text{d}x+(-6xy)\text{d}y+C \\
  &= \int_{x_0}^{x}(3x^2-3y_0^2)\text{d}x+\int_{y_0}^{y}(-6xy)\text{d}y+C \\
  &= \int_{x_0}^{x}(3x^2)\text{d}x+\int_{y_0}^{y}(-6xy)\text{d}y+C \\
  &= x^3-3xy^2+C
  \end{aligned}
  $$
  将 $x,y$ 分别用 $\displaystyle x = \frac{z+\overline{z}}{2},y = \frac{z-\overline{z}}{2i}$ 替换即可得到含 $z$ 的表达式。

- 不定积分法

  对于 $f(z) = u+iv$，有 $f'(z) = \displaystyle \frac{\partial u}{\partial x}+\frac{\partial v}{\partial x}i = \frac{\partial u}{\partial x}-\frac{\partial u}{\partial y}i$，那么 
  $$
  f(z) = \int f'(z)\text{d}z = \int\left(\frac{\partial u}{\partial x}-i\frac{\partial u}{\partial y}\right)
  $$
  同样对于上面的题目，使用不定积分法来解，就有 
  $$
  \begin{aligned}
  f'(z) &= \frac{\partial u}{\partial x}+i\frac{\partial v}{\partial x} \\
  &= -6xy+i(3x^2-3y^2) \\
  &= 3ix^2-6xy-3iy^2 \\
  &= 3i(x^2+2ixy-3y^2) \\
  &= 3iz^2
  \end{aligned}
  $$
  所以 $\displaystyle f(z) = \int f'(z)\text{d}z = \int 3iz^2\text{d}z = iz^3+C$，将 $z=x+iy$ 代入即可得到 $v$。

  > e.g. 若 $\displaystyle v = \frac{y}{x^2+y^2}$，且满足 $f(2) = 0$ 求 $f=u+iv$ 解析，求 $f$

  先求偏导
  $$
  \begin{cases}
  \displaystyle \frac{\partial u}{\partial x} = \frac{\partial v}{\partial y} = \frac{x^2-y^2}{(x^2+y^2)^2} \\
  \displaystyle \frac{\partial u}{\partial y} = -\frac{\partial v}{\partial x} = \frac{2xy}{(x^2+y^2)^2}
  \end{cases}
  $$
  那么 
  $$
  \begin{aligned}
  f'(z) &= \frac{\partial u}{\partial x}+i\frac{\partial v}{\partial x} \\
  &= \frac{x^2-y^2-2ixy}{(x^2+y^2)^2} \\
  &= \frac{(x-iy)^2}{(x^2+y^2)^2} \\
  &= \frac{\overline{z}^2}{z\cdot\overline{z}^2} \\
  &= \frac{1}{z^2} \\
  \end{aligned}
  $$
  因此 $\displaystyle f(z) = \int f'(z)\text{d}z = \int \frac{1}{z^2}\text{d}z = -\frac{1}{z}+C$，又因为 $f(2) = -\frac{1}{2}+C=0$，所以 $C = \frac{1}{2}$。那么 $\displaystyle f(z) = -\frac{1}{x+iy}+\frac{1}{2}$。

- 偏积分法

  先将 $x$ 视为常数，根据 $\displaystyle v = \int\frac{\partial v}{\partial y}\text{d}y$ 计算出 $C(x)$，再对得到的 $v$ 求关于 $x$ 的偏导，此时与 C-R 方程求得的 $\displaystyle \frac{\partial v}{\partial x}$ 进行比对，得到 $C(x)$ 的完整表达式，此时即可求出 $v$。

  同样对于上面的题目，使用偏积分法求解，就有 $\displaystyle v = \int\frac{\partial v}{\partial y}\text{d}y = \int(-6xy)\text{d}y = -3xy^2+C(x)$，则 $\displaystyle \frac{\partial v}{\partial x} = -3y^2+C'(x)$，又因为 $\displaystyle \frac{\partial v}{\partial x} = -\frac{\partial u}{\partial y} = -3y^2+3x^2$，所以 $C'(x) = 3x^2,C(x) = x^3+C$。因此 $v = -3xy^2+x^3+C,f(z) = u+iv$。

## 级数

### 级数的敛散性

#### 复数列的极限

定义复数列 $\{\alpha_n\}$，其中 $\alpha_n = a_n+ib_n$。若 $\{\alpha_n\}$ 收敛于 $\alpha=a+ib$，则记为 $\displaystyle \lim_{n\to\infty}\alpha_n=\alpha$。

对于 $\displaystyle \lim_{n\to\infty}\alpha_n = \alpha$，$\displaystyle \lim_{n\to\infty}(a_n+ib_n)=a+ib$ 的充要条件为 $\displaystyle \lim_{n\to\infty}a_n = a$ 且 $\displaystyle \lim_{n\to\infty}b_n = b$。

#### 级数收敛的充要条件

定义复变函数的级数
$$
\alpha_q+\alpha_2+\alpha_3+\cdots+\alpha_n = \sum_{n=1}^{\infty}\alpha_n
$$
构造 
$$
\begin{aligned}
S_1 &= \alpha_1 \\
S_2 &= \alpha_1 + \alpha_2 \\
S_3 &= \alpha_1 + \alpha_2 + \alpha_3 \\
&\vdots \\
S_n &= \alpha_1 + \alpha_2 + \alpha_3 + \cdots + \alpha_n = \sum_{k=1}^{n}\alpha_k \\
\end{aligned}
$$
那么若 $\displaystyle \lim_{n\to\infty}S_n = S$，则称级数 $\displaystyle \sum_{n=1}^{\infty}\alpha_n$ 收敛于 $S$。若 $\displaystyle \lim_{n\to\infty}S_n$ 不存在，则称级数 $\displaystyle \sum_{n=1}^{\infty}\alpha_n$ 发散。

级数 $\displaystyle \sum_{n=1}^{\infty}\alpha_n = \sum_{n=1}^{\infty}(a_n+ib_n)$ 收敛的充要条件是级数 $\displaystyle \sum_{n=1}^{\infty}a_n$ 和 $\displaystyle \sum_{n=1}^{\infty}b_n$ 同时收敛。此时有 $\displaystyle S_n = \sum_{k=1}^{n}\alpha_k = \sum_{k=1}^{n}(a_k+ib_k) = \sum_{k=1}^{n}a_k+\sum_{k=1}^{n}b_k$。

**级数不等式**

若有 $\displaystyle \sum_{n=1}^{\infty}a_n$ 收敛 $\displaystyle \Rightarrow \lim_{n\to\infty}a_n = 0$ 和 $\displaystyle \sum_{n=1}^{\infty}b_n$ 收敛 $\displaystyle \Rightarrow \lim_{n\to\infty}b_n = 0$，那么就有 $\displaystyle \sum_{n=1}^{\infty}\alpha_n$ 收敛 $\displaystyle \Rightarrow \lim_{n\to\infty}\alpha_n  = \lim_{n\to\infty}(a_n+ib_n) = 0$ 。

若有 $\displaystyle \sum_{n=1}^{\infty}\vert\alpha_n\vert$ 收敛 $\displaystyle \Rightarrow \sum_{n=1}^{\infty}\alpha_n$  收敛，且 $\displaystyle \Bigg|\sum_{n=1}^{\infty}\alpha_n\Bigg|\leqslant\sum_{n=1}^{\infty}\vert\alpha_n\vert$，那么就有 $\vert\alpha_n\vert=\sqrt{a_n^2+b_n^2}$。

#### 级数敛散性的判断

若 $\displaystyle \sum_{n=1}^{\infty}\vert\alpha_n\vert$ 收敛，则称 $\displaystyle \sum_{n=1}^{\infty}\alpha_n$ 绝对收敛。若 $\displaystyle \sum_{n=1}^{\infty}\alpha_n$ 收敛，但 $\displaystyle \sum_{n=1}^{\infty}\vert\alpha_n\vert$ 发散，则称 $\displaystyle \sum_{n=1}^{\infty}\alpha_n$ 条件收敛。

此处复变函数级数敛散性的判断方法与实变函数级数敛散性的判断方法几乎完全一样，此处仅列举部分。

对于级数 $\displaystyle \sum_{n=1}^{\infty}\alpha_n$，我们可以通过如下步骤判断其敛散性。

- 若 $\alpha_n\to0$，说明级数发散；否则继续判断

- 此时我们对级数分为如下几类分别判断

  - 正项级数($\alpha_n>0$)

    - 比较判别法：

      对于 $p$ 级数，有
      $$
      \sum_{n=1}^{\infty}\frac{1}{n^p} = 
      \begin{cases}
      \text{converges} & p>1 \\
      \text{diverges} & p\leqslant 1
      \end{cases}
      $$
      对于等比级数，还有
      $$
      \sum_{n=1}^{\infty}q^n = 
      \begin{cases}
      \text{converges} & \vert p\vert<1 \\
      \text{diverges} & \vert p\vert\geqslant 1
      \end{cases}
      $$
      也可以使用和其他级数的比值判别。若级数 $\displaystyle \sum_{n=1}^{\infty}\alpha_n, \sum_{n=1}^{\infty}\beta_n$，若满足
      $$
      \lim_{n\to\infty}\frac{\alpha_n}{\beta_n}=l(0<l<+\infty)
      $$
      则说明这两个级数的敛散性相同。

    - 比值判别法
      $$
      \lim_{n\to\infty}\frac{\alpha_{n+1}}{\alpha_n}=l
      \begin{cases}
      \text{converges} & 0\leqslant l<1 \\
      \text{uncertain} & l = 1 \\
      \text{diverges} & l>1
      \end{cases}
      $$

    - 根式判别法
      $$
      \lim_{n\to\infty}\sqrt[n]{\alpha_n} = q 
      \begin{cases}
      \text{converges} &q<1 \\
      \text{uncertain} & q = 1 \\
      \text{diverges} & q>1
      \end{cases}
      $$

  - 交错级数

    根据 Leibniz 法则，若 $\vert(-1)^n\alpha_n\vert\to0$ 且单调递减，则级数收敛。

  - 一般级数

    对于一般级数，我们可以判断其绝对收敛性。

    若级数 $\displaystyle \sum_{n=1}^{\infty}\beta_n$ 收敛，且有
    $$
    \sum_{n=1}^{\infty}\vert\alpha_n\vert \leqslant \sum_{n=1}^{\infty}\beta_n
    $$
    则级数 $\displaystyle \sum_{n=1}^{\infty}\alpha_n$ 绝对收敛。

> e.g. 判断级数 $\displaystyle \sum_{n=1}^{\infty}\left[\ln{(1+\frac{1}{n^2})}+\frac{2^n\cdot n!}{n^n}i\right]$ 是否收敛

对于实部，有 $\displaystyle \sum_{n=1}^{\infty}\ln(1+\frac{1}{n^2})\sim\sum_{n=1}^{\infty}\frac{1}{n^2}$，因此收敛。

对于虚部，有 
$$
\lim_{n\to\infty}\frac{u_{n+1}}{u_n} = \lim_{n\to\infty}\frac{\frac{2^{n+1}\cdot (n+1)!}{(n+1)^{n+1}}}{\frac{2^n\cdot n!}{n^n}} = \lim_{n\to\infty}\frac{2}{\left(1+\frac{1}{n}\right)^n} = \frac{2}{e}<1
$$
因此收敛。

因为该级数的实部和虚部均收敛，因此级数收敛。

> e.g. 判断级数 $\displaystyle \sum_{n=1}^{\infty}\frac{(2+3i)^n}{5^n}$ 是否收敛

对于该级数，我们有 
$$
\sum_{n=1}^{\infty}\Bigg|\frac{(2+3i)^n}{5^n}\Bigg| = \sum_{n=1}^{\infty}\Bigg|\frac{2+3i}{5}\Bigg|^n = \sum_{n=1}^{\infty}\left(\frac{\vert 2+3i\vert}{\vert 5\vert}\right)^n
$$
上式中最右级数是等比级数，有 $\displaystyle q=\frac{\vert 2+3i\vert}{5} = \frac{\sqrt{2^2+3^2}}{5}<1$，因此级数收敛。

### 幂级数

#### 幂级数的概念

对于如下形式的级数
$$
\sum_{n=0}^{\infty}C_n(z-z_0)^2 = C_0+C_1(z-z_0)+C_2(z-z_0)^2+\cdots+C_n(z-z_0)^n+\cdots
$$
称为幂级数。对于幂级数，有以下定义

- 如果存在 $z$ 使得级数收敛，则称 $z$ 为该收敛点
- 所有收敛点的集合称为收敛域
- 若级数的收敛域为 $\vert z\vert<m$，则也可将收敛域称为收敛圆

#### 阿贝尔定理

阿贝尔定理(Abel Theorem)描述如下

对于级数 $\displaystyle \sum_{n=0}^{\infty}C_nz^n$，若在 $z=z_0(z_0\neq0)$ 处收敛，则对于任意 $\vert z\vert<\vert z_0\vert$ 的 $z$，级数都绝对收敛；若在 $z=z_0$ 处发散，则对于任意 $\vert z\vert>\vert z_0\vert$ 的 $z$，级数都发散。

> e.g. 若级数 $\displaystyle \sum_{n=0}^{\infty}C_n z_n$ 在 $1+i$ 处收敛，在 $3$ 处发散，试判断级数在 $i$ 处和 $2+3i$ 处的敛散性

显然 $\vert i\vert<\vert 1+i\vert$，因此级数在 $i$ 处收敛；$\vert 2+3i\vert>\vert3\vert$，因此级数在 $2+3i$ 处发散。

#### 收敛半径

设级数 $\displaystyle \sum_{n=0}^{\infty}C_n z^n$ 的收敛半径为 $R$，则

- 若满足 $\displaystyle \lim_{n\to\infty}\left|\frac{C_{n+1}}{C_n}\right|=\lambda$，则收敛半径为 $\displaystyle R=\frac{1}{\lambda}$
- 若满足 $\displaystyle \lim_{n\to\infty}\sqrt[n]{\vert C_n\vert} = \lambda$，则收敛半径为 $\displaystyle R=\frac{1}{\lambda}$

对于级数，有
$$
\lim_{n\to\infty}\frac{\vert C_{n+1}z^{n+1}\vert}{\vert C_n z_n\vert} = \lim_{n\to\infty}\left|\frac{C_{n+1}}{C_n}\right|\cdot\vert z\vert = 
\begin{cases}
<1 & \text{Converges} \\
>1 & \text{Diverges}
\end{cases}
$$
而 $\displaystyle \lambda = \lim_{n\to\infty}\left|\frac{C_{n+1}}{C_n}\right|$，所以收敛半径以 $\lambda\cdot\vert z\vert=1$ 为界。

> e.g. 计算 $\displaystyle \sum_{n=0}^{\infty}(\sin{in})z^n$ 的收敛半径

$$
\lambda = \lim_{n\to\infty}\left|\frac{C_{n+1}}{C_n}\right| = \lim_{n\to\infty}\left|\frac{\sin{i(n+1)}}{\sin{in}}\right| = \lim_{n\to\infty}\left|\frac{\frac{e^{-(n+1)}-e^{n+1}}{2i}}{\frac{e^{-n}-e^n}{2i}}\right| = e
$$

因此收敛半径为 $\displaystyle R = \frac{1}{\lambda} = \frac{1}{e}$。

>  e.g. 计算 $\displaystyle \sum_{n=0}^{\infty}(1-i)^nz^n$ 的收敛半径

$$
\lambda = \lim_{n\to\infty}\left|\frac{C_{n+1}}{C_n}\right| = \lim_{n\to\infty}\left|\frac{(1-i)^{n+1}}{(1-i)^n}\right| = \lim_{n\to\infty}\left|1-i\right| = \sqrt{2} \\
or \\
\lambda = \lim_{n\to\infty}\sqrt[n]{\vert C_n\vert} = \lim_{n\to\infty}\sqrt[n]{\vert (1-i)^n\vert} = \lim_{n\to\infty}\vert 1-i\vert = \sqrt{2}
$$

因此收敛半径为 $\displaystyle R = \frac{1}{\lambda} = \frac{1}{\sqrt{2}}$。

#### 幂级数的性质

- 两个幂级数在公共收敛域，能够进行 $+, -, \times$ 的计算

- 若级数 $\displaystyle \sum_{n=0}^{\infty}a_n(z-z_0)^n$ 在 $\mathbb{D}:\vert z-z_0\vert<R$ 收敛，则

  (1) 和函数 $\displaystyle f(z) = \sum_{n=0}^{\infty}a_n(z-z_0)^n$ 在 $\mathbb{D}$ 内解析

  (2) 可在 $\mathbb{D}$ 内逐项求导，即 $\displaystyle f'(z) = \sum_{n=0}^{\infty}(a_n(z-z_0)^n)' = \sum_{n=0}^{\infty}a_n\cdot n(z-z_0)^n$

  (3) 可在 $\mathbb{D}$ 内逐项积分，即 $\displaystyle \int_C f(z)\text{d}z = \sum_{n=0}^{\infty}\int_C a_n(z-z_0)^n\text{d}z$

  特别地，有
  $$
  \int_{z_0}^{z}f(z)\text{d}z = \sum_{n=0}^{\infty}\int_{z_0}^{z}a_n(z-z_0)^n\text{d}(z-z_0) = \sum_{n=0}^{\infty}a_n\frac{(z-z_0)^{n+1}}{n+1}\Bigg|_{z_0}^{z} = \sum_{n=0}^{\infty}\frac{a_n(z-z_0)^{n+1}}{n+1}
  $$

### Taylor 级数

#### 泰勒展开定理

若级数 $\displaystyle f(z) = \sum_{n=0}^{\infty}a_n(z-z_0)^n$ 在 $\mathbb{D}:\vert z-z_0\vert<R$  解析，则
$$
f(z) = \sum_{n=0}^{\infty}C_n(z-z_0)^n \\
\text{where }C_n = \frac{f^{(n)}(z_0)}{n!} = \frac{1}{2\pi i}\oint_{C}\frac{f(z)}{(z-z_0)^{n+1}}\text{d}z \\
C:\vert z-z_0\vert=\rho
$$

#### 泰勒级数的两个结论

- $f(z)$ 在 $z_0$ 处解析等价于 $f(z)$ 在 $z_0$ 附近可以展开成幂级数
- 对于级数 $\displaystyle f(z) = \sum_{n=0}^{\infty}C_n(z-z_0)^n$，其收敛半径为 $R=\vert z_0-a\vert$，其中 $a$ 是与 $z_0$ 中心距离最近的奇点。

> e.g. 若 $\displaystyle \frac{1}{(z-1)(z-2)}$ 在 $z=1+i$ 附近可以展开成幂级数，求级数的收敛半径

显然该式有两个奇点分别为 $z=1, z=2$，那么对于 $z=1+i$，距离其最近的奇点为 $z=1$，且二者距离为 $\vert (1+i)-(1)\vert$，因此该级数的收敛半径就是 $R=1$。

> e.g. 将 $e^{z^2}z$ 在 $z=0$ 处展开为泰勒级数

$$
e^{z^2} = \sum_{n=0}^{\infty}\frac{(z^2)^n}{n!} \\
ze^{z^2} = \sum_{n=0}^{\infty}\frac{z^{2n+1}}{n!}
$$

> e.g. 分别将 $\displaystyle f(z) = \frac{1}{z}$ 和 $\displaystyle g(z) = \frac{1}{z^2}$ 在 $z=1$ 处展开为泰勒级数

$$
f(z) = \frac{1}{1-(-(z-1))} = \sum_{n=0}^{\infty}(-(z-1))^n = \sum_{n=0}^{\infty}(-1)^n(z-1)^n \\
g(z) = (-f'(z)) = \left(\sum_{n=0}^{\infty}(-1)^n(z-1)^n\right)' = \sum_{n=1}^{\infty}(-1)^{n+1}n(z-1)^{n-1}
$$

> e.g. 将 $e^z\sin{z}$ 在 $z=0$ 处展开为幂级数

$$
\begin{aligned}
e^z\sin{z} 
&= e^z\frac{e^{iz}-e^{-iz}}{2i} \\
&= \frac{1}{2i}\left(e^{(1+i)z}-e^{(1-i)z}\right) \\
&= \frac{1}{2i}\left(\sum_{n=0}^{\infty}\frac{(1+i)^n z^n}{n!}-\sum_{n=0}^{\infty}\frac{(1-i)^n z^n}{n!}\right) \\
&= \frac{1}{2i}\sum_{n=0}^{\infty}\frac{1}{n!}((1+i)^n-(1-i)^n)z^n \\
&= \sum_{n=0}^{\infty}\frac{1}{n!}\cdot\frac{(1+i)^n-(1-i)^n}{2i}z^n \\
&= \sum_{n=0}^{\infty}\frac{1}{n!}\text{Im}\{(1+i)^n\}z^n \\
&= \sum_{n=0}^{\infty}\frac{1}{n!}\text{Im}\{(\sqrt{2}e^{i\frac{\pi}{4}})^n\}z^n \\
&= \sum_{n=0}^{\infty}\frac{1}{n!}2^{\frac{n}{2}}\sin{\frac{n}{4}\pi}\cdot z^n \\
\end{aligned}
$$

### Laurent 级数

#### Laurent 级数的引入

对于级数
$$
\frac{C_{-n}}{(z-z_0)^n}+\cdots+\frac{C_{-2}}{(z-z_0)^2}+\frac{C_{-1}}{(z-z_0)^1}+C_0+C_1(z-z_0)+\cdots
$$
假设后半部分在 $\vert z-z_0\vert<R_2$ 时收敛，令 $\displaystyle t = \frac{1}{z-z_0}$，则前半部分为 $C_{-n}t^n+\cdots+C_{-2}t^{2}+C_1t^1$，当 $\vert t\vert<\mu$ 时该部分收敛。此时有 $\displaystyle \left|\frac{1}{z-z_0}\right|<\mu\Leftrightarrow\vert z-z_0\vert>\frac{1}{\mu} = R_1$，那么级数的收敛域为 $R_1<\vert z-z_0\vert<R_2$。

因此，若函数 $f(z)$ 在 $R_1<\vert z-z_0\vert<R_2$ 内解析，则其可以表示成如下形式
$$
f(z) = \sum_{n=-\infty}^{+\infty}C_n(z-z_0)^n
$$
其中 $f(z)$ 在 $z_0$ 处展开为 Laurent 级数，且有 $\displaystyle C_n = \frac{1}{2\pi i}\oint_C\frac{f(\xi)}{(\xi-z_0)^{n+1}}\text{d}\xi,\ C:\vert z-z_0\vert=r(R_1<r<R_2)$。

#### Laurent 级数的推论

若 $f(z)$ 在 $R_1<\vert z-z_0\vert<R_2$ 内解析，则对于 $C:\vert z-z_0\vert=r(R_1<r<R_2)$ 有 $C_{-1} = \displaystyle \frac{1}{2\pi i}\oint_C f(z)\text{d}z$，也就是 $\displaystyle \oint_C f(z)\text{d}z = 2\pi i\cdot C_{-1}$，其中 $C_{-1}$ 是 $\displaystyle\frac{1}{z-z_0}$ 的系数。

> e.g. 将函数 $\displaystyle f(z) = \frac{1}{z^2-3z+2}$ 在 $z=0$ 处展开为 Laurent 级数

不难发现函数 $\displaystyle f(z) = \frac{1}{z^2-3z+2} = \frac{1}{(z-1)(z-2)} = \frac{1}{z-2} - \frac{1}{z-1}$ 的奇点为 $z=1,z=2$，因此其在三个区域内完全解析。

- $\vert z-0\vert<1$

  在此区域内，有
  $$
  \begin{aligned}
  f(z) &= \frac{1}{z-2} - \frac{1}{z-1} \\
  &= -\frac{1}{2}\frac{1}{1-\frac{z}{2}} + \frac{1}{1-z} \\
  &= -\frac{1}{2}\sum_{n=0}^{\infty}\left(\frac{z}{2}\right)^n + \sum_{n=0}^{\infty}z^n \\
  &= -\sum_{n=0}^{\infty}\frac{1}{2^{n+1}}z^n + \sum_{n=0}^{\infty}z^n
  \end{aligned}
  $$

- $1<\vert z-0\vert<2$

  在此区域内，有
  $$
  \begin{aligned}
  f(z) &= \frac{1}{z-2} - \frac{1}{z-1} \\
  &= -\frac{1}{2}\frac{1}{1-\frac{z}{2}} - \frac{1}{z}\frac{1}{1-\frac{1}{z}} \\
  &= -\frac{1}{2}\sum_{n=0}^{\infty}\left(\frac{z}{2}\right)^n - \frac{1}{z}\sum_{n=0}^{\infty}\left(\frac{1}{z}\right)^n \\
  &= -\sum_{n=0}^{\infty}\frac{1}{2^{n+1}}z^n - \sum_{n=0}^{\infty}\frac{1}{z^{n+1}}
  \end{aligned}
  $$

- $\vert z-0\vert>2$

  在此区域内，有
  $$
  \begin{aligned}
  f(z) &= \frac{1}{z-2} - \frac{1}{z-1} \\
  &= -\frac{1}{z}\frac{1}{1-\frac{2}{z}} - \frac{1}{z}\frac{1}{1-\frac{1}{z}} \\
  &= -\frac{1}{z}\sum_{n=0}^{\infty}\left(\frac{2}{z}\right)^n - \frac{1}{z}\sum_{n=0}^{\infty}\left(\frac{1}{z}\right)^n \\
  &= -\sum_{n=0}^{\infty}\frac{1}{z^{n+1}}2^n - \sum_{n=0}^{\infty}\frac{1}{z^{n+1}}
  \end{aligned}
  $$

> e.g. 计算 $\displaystyle \oint_{\vert z\vert=3}\frac{1}{z(z+1)^2}\text{d}z$

不难发现此函数的奇点为 $z=0, z=-1$，我们可以将其展开为 Laurent 级数。
$$
\begin{aligned}
\frac{1}{z(z+1)^2} &= \frac{1}{(z+1)^2}\frac{1}{(z+1)-1} \\
&= \frac{1}{(z+1)^2}\frac{1}{z+1}\frac{1}{1-\frac{1}{z+1}} \\
&= \frac{1}{(z+1)^3}\sum_{n=0}^{\infty}\left(\frac{1}{z+1}\right)^n \\
&= \sum_{n=0}^{\infty}\left(\frac{1}{z+1}\right)^{n+3} \\
\end{aligned}
$$
显然 $C_{-1}=0$，因此 $\displaystyle \oint_{\vert z\vert=3}\frac{1}{z(z+1)^2}\text{d}z = 2\pi i\cdot C_{-1} = 0$。

> e.g. 计算 $\displaystyle \oint_{\vert z\vert=2}\frac{ze^{\frac{1}{z}}}{1-z}\text{d}z$

不难发现此函数的奇点为 $z=1$，且 $\vert z\vert=2$ 在以 $z=0$ 为圆心 $1$ 为半径的圆外。

对于 $e^{\frac{1}{z}}$，其在 $z=0$ 附近可展开为 
$$
e^\frac{1}{z} = 1+\frac{1}{z}+\frac{1}{2!}\frac{1}{z^2}+\cdots
$$
在 $\vert z\vert>1$ 区域内，$\displaystyle \frac{z}{1-z}$ 可展开为
$$
\frac{z}{1-z} = \frac{1}{\frac{1}{z}-1} = -\frac{1}{1-\frac{1}{z}} = -\sum_{n=0}^{\infty}\left(\frac{1}{z}\right)^n
$$
因此，$\displaystyle \frac{ze^{\frac{1}{}}}{1-z} = -1-\frac{2}{z}-\frac{5}{2}\frac{1}{z^2}+\cdots$，也就意味着 $C_{-1} = -2$。

所以 $\displaystyle \oint_{\vert z\vert=2}\frac{ze^{\frac{1}{z}}}{1-z}\text{d}z = 2\pi i\cdot C_{-1} = -4\pi i$。

## 留数

### 孤立奇点

若 $f(z)$ 有奇点 $z_0$ ，$\exist \delta>0$，使得 $0<\vert z-z_0\vert<\delta$，则称 $z_0$ 为 $f(z)$ 的孤立奇点。

> e.g. 判断 $\displaystyle \frac{1}{z(z-1)}$ 的奇点是否均为孤立奇点

显然 $f(z)$ 具有奇点 $0,1$，均为孤立奇点

> e.g. 判断 $\displaystyle \frac{1}{\sin{\frac{1}{z}}}$ 的奇点是否均为孤立奇点

$f(z)$ 的奇点有 $0,\displaystyle \frac{1}{k\pi}, k\in{Z}$。当 $k\to\infty$ 时，有 $\displaystyle \frac{1}{k\pi}\to 0$，因此 $f(z)$ 的奇点不都是孤立奇点。

若 $f(z)$ 在 $0<\vert z-z_0\vert<\delta$ 处展开 Laurent 级数，则有
$$
f(z) = \cdots+\frac{C_{-n}}{(z-z_0)^n}+\cdots+\frac{C_{-1}}{z-z_0}+C_0+C_1(z-z_0)+\cdots
$$
那么若奇点为

- 可去奇点

  则有
  $$
  f(z) = C_0+C_1(z-z_0)+C_2(z-z_0)^2+\cdots
  $$
  对于奇点而言，其等价的极限表达式为 $\displaystyle \lim_{z\to z_0}f(z)=C_0$。

- 极点

  则有
  $$
  f(z) = \cdots+\frac{C_{-m}}{(z-z_0)^m}+\cdots+\frac{C_{-1}}{z-z_0}+C_0+C_1(z-z_0)+\cdots
  $$
  且 $C_{-m}\neq0$，则称 $z_0$ 为 $f(z)$ 的 $m$ 阶极点。

  $f(z)$ 还可改写为如下形式
  $$
  f(z) = \frac{1}{(z-z_0)^m}[C_{-m}+C_{-(n-1)}(z-z_0)+\cdots+C_0(z-z_0)^m+\cdots]
  $$
  若令 $\phi(z) = C_{-m}+C_{-(n-1)}(z-z_0)+\cdots+C_0(z-z_0)^m+\cdots$，且 $C_{-m} \neq 0$，那么则有如下定义

  对于函数 $\displaystyle f(z) = \frac{1}{(z-z_0)^m}\phi(z)$，若 $\phi(z)$ 解析，且 $\phi(z_0)\neq0$，则称 $z=z_0$ 为$f(z)$ 的 $m$ 阶极点。

  > e.g. 求 $\displaystyle f(z) = \frac{2z}{(z^2+1)(z-i)^3}$ 的极点

  整理得 $\displaystyle f(z) = \frac{2z}{(z^2+1)(z-i)^3} = \frac{2z}{(z+i)(z-i)^4}$，不难发现奇点为 $z=\pm i$，因此

  当 $z=i$ 时，$\displaystyle f(z) = \frac{1}{(z-i)^4}\cdot\frac{2z}{z+i}$，且 $\displaystyle \frac{2z}{z+i}\Bigg|_{z=i}\neq0$，因此 $i$ 是 $f(z)$ 的 4 阶极点。

  当 $z=-i$ 时，$\displaystyle f(z) = \frac{1}{z+i}\cdot\frac{2z}{(z-i)^4}$，且 $\displaystyle \frac{2z}{(z-i)^4}\Bigg|_{z=-i}\neq0$，因此 $-i$ 是 $f(z)$ 的 1 阶极点。

  对于极点而言，其等价的极限表达式为 $\displaystyle \lim_{z\to z_0}f(z)=\infty$。

  > e.g. 求 $\displaystyle f(z) = \frac{\sin{z}}{z^3}$ 的极点

  对 $\sin{z}$ 进行泰勒展开，得 $\displaystyle \frac{\sin{z}}{z^3} = \frac{z-\frac{z^3}{3!}+\cdots}{z^3} = \frac{1}{z^2}-\frac{1}{3!}+\cdots$，显然有 $f(z)$ 的 2 阶极点为 $z=0$。

- 本性奇点

  若 $f(z)$ 在 $z=z_0$ 处满足
  $$
  f(z) = \phi(z)+C_0+\cdots
  $$
  其中 $\phi(z) = \cdots+\displaystyle \frac{C_{-m}}{(z-z_0)^m}+\cdots+\frac{C_{-1}}{z-z_0}$，且拥有无穷多项，则称 $z_0$ 为 $f(z)$ 的本性奇点。

  常见的拥有本性奇点的表达式有

  - $\displaystyle e^{\frac{1}{z}} = \sum_{n=0}^{\infty}\frac{1}{n!}z^{-n}(0<\vert z\vert<\infty)$，有 $z=0$ 为本性奇点

  - $\displaystyle \sin{\frac{1}{z}} = \frac{1}{z}-\frac{1}{3!}z^{-3}+\cdots$，有 $z=0$ 为本性奇点

  - $\displaystyle \cos\frac{1}{z} = 1-\frac{1}{2!}z^{-2}+\cdots$，有 $z=0$ 为本性奇点

  对于本性奇点而言，其等价的极限表达式为 $\displaystyle \lim_{z\to z_0}f(z)$ 不存在。

- 零点

  若 $f(z)$ 在 $z=0$ 处满足
  $$
  f(z) = \displaystyle (z-z_0)^m\phi(z)
  $$
  且 $\phi(z)$ 解析，$\phi(z_0)\neq 0$，则称 $z_0$ 为 $f(z)$ 的 $m$ 阶零点。

  若有 $f(z_0) = f'(z_0) = f''(z_0) = \cdots = f^{(m-1)}(z_0) = 0$，且 $f^{(m)}(z_0)\neq 0$，则也认为 $z_0$ 为 $f(z)$ 的 $m$ 阶零点。

  若 $z=z_0$ 为 $f(z)$ 的 $m$ 级零点，$g(z)$ 的 $n$ 级零点。则 

  - $z=z_0$ 为 $f(z)\cdot g(z)$ 的 $(m+n)$ 级零点
  - $z=z_0$ 为 $\displaystyle \frac{f(z)}{g(z)}$ 的 $\begin{cases}\text{可去奇点} & m\geqslant n \\ (n-m)\text{阶极点} & m<n\end{cases}$ 
  
  > e.g. 求 $f(z) = z^2(e^z-1)$ 的零点
  
  对 $f(z)$ 进行展开，可得 $\displaystyle f(z) = z^2(1+z+\frac{z^2}{2!}+\cdots - 1) = z^3(1+\frac{z}{2!}+\cdots)$。令 $\displaystyle \phi(z) = 1+\frac{z}{2!}+\cdots$，则有 $\phi(0)=1$，因此 $z=0$ 是 $f(z)$ 的三阶极点。

**零点与极点的关系**

若 $z=z_0$ 为 $f(z)$ 的 $m$ 阶零点，则 $z=z_0$ 为 $\displaystyle \frac{1}{f(z)}$ 的 $m$ 阶极点，反之也成立。

> e.g. 求 $f(z) = \displaystyle \frac{1}{z^3(e^z-1)}$ 的极点

题目等价于求 $g(z) = z^3(e^z-1)$ 的零点。$z=0$ 显然为 $3+1=4$ 阶零点。对于 $e^z-1=0$，有 $z = \text{Ln}{1} = \ln{1}+2k\pi i = 2k\pi i$，所以 $z=2k\pi i(k\neq 0)$ 均为 $1$ 阶零点。因此 $f(z)$ 的 $1$ 阶极点是 $z=2k\pi i(k\neq 0)$，$4$ 阶极点是 $z=0$。

### 函数在无穷远点的性态

若 $f(z)$ 在 $z=\infty$ 附近一邻域 $R<\vert z\vert<\infty$ 内解析，咋称 $z=\infty$ 是 $f(z)$ 的孤立奇点。

若有 
$$
f(z) = \sum_{n=-\infty}^{+\infty}C_nz^n
$$
那么对于 $\displaystyle z = \frac{1}{t}$，就有 $\displaystyle \phi(t) = f(\frac{1}{t}) = \sum_{n=-\infty}^{+\infty}C_n\frac{1}{t^n}$。

我们规定，若 $z=\infty$ 为

- 可去奇点，那么其等价于 $\phi(t)$ 在 $t=0$ 处拥有可去奇点
- $m$ 阶极点，那么其等价于 $\phi(t)$ 在 $t=0$ 处拥有 $m$ 阶极点
- 本性奇点，那么其等价于 $\phi(t)$ 在 $t=0$ 处拥有本性奇点

