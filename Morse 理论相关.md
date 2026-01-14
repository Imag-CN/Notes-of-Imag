___

>[!problem]
>设 $f=f(x_1,x_2):\mathbb{R}^2\to \mathbb{R}$ 是 $C^3$ 函数.
>
>1. 证明: 如果 $f(0,0)=0$, 则存在 $C^2$ 函数 $g_1,g_2$ 满足
>
>$$ f(x_1,x_2)=x_1g_1(x_1,x_2)+x_2g_2(x_1,x_2), $$
>
>且 $g_i(0,0)=\frac{\partial f}{\partial x_i}(0,0),\ i=1,2$.
>
>提示: 考虑 $\int_0^1\frac{\mathrm{d}}{\mathrm{d}t}f(tx_1,tx_2)\mathrm{d}t.$
>
>2. 设 $P(x_1^0,x_2^0)$ 是 $f$ 的驻点, 并且 $f$ 的二阶导数矩阵在点 $P$ 非退化, 证明: 存在 $P$ 一个邻域 $U$ 上的参数变换 $\varphi:U\to V,\ \varphi(P)=(0,0)$, 使得对任意 $(u_1,u_2)\in V$,
>
>$$ f\circ\varphi^{-1}(u_1,u_2)=f(P)+\varepsilon_1 u_1^2+\varepsilon_2 u_2^2, $$
>
>其中 $\varepsilon_1,\varepsilon_2=\pm 1$.

**证明:**
**1.** 定义 $g_1$ 和 $g_2$ 如下
$$
g_1(x_1,x_2) = \int_0^1 \frac{\partial f}{\partial x_1}(t x_1, t x_2) \, dt,
\quad
g_2(x_1,x_2) = \int_0^1 \frac{\partial f}{\partial x_2}(t x_1, t x_2) \, dt.
$$
由于 $f \in C^3$, 其一阶偏导数属于 $C^2$, 因此由积分号下求导可知 $g_1, g_2 \in C^2$.

根据提示:
$$
\begin{aligned}
f(x_1, x_2) &= \int_0^1 \frac{d}{dt} f(t x_1, t x_2) \, dt \\
&= \int_0^1 \left( x_1 \frac{\partial f}{\partial x_1}(t x_1, t x_2) + x_2 \frac{\partial f}{\partial x_2}(t x_1, t x_2) \right) dt \\
&= x_1 g_1(x_1, x_2) + x_2 g_2(x_1, x_2).
\end{aligned}
$$
在原点处取值:
$$
g_i(0,0) = \int_0^1 \frac{\partial f}{\partial x_i}(0,0) \, dt = \frac{\partial f}{\partial x_i}(0,0).
$$
---
**2.** 设 $g(x_{1},x_{2})=f(x_{1},x_{2})-f(P)$, 则 $g$ 是 $C^3$ 函数, $g(P)=0$, 且 $P$ 是 $g$ 的驻点

对 $g$ 使用第一问, 得存在 $C^2$ 函数 $g_1,g_2$ 满足
$$
g(x_1,x_2)=x_1g_1(x_1,x_2)+x_2g_2(x_1,x_2),
$$
且 $g_i(0,0)=\frac{\partial g}{\partial x_i}(0,0),\ i=1,2$.

