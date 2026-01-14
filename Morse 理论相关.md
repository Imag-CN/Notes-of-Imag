___

>[!problem] 问题
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
**2.** 令 $P=(x_1^0, x_2^0)$. 作平移 $y_1 = x_1 - x_1^0$, $y_2 = x_2 - x_2^0$, 定义
$$
F(y_1, y_2) = f(y_1 + x_1^0, \; y_2 + x_2^0) - f(P).
$$
则 $F(0,0)=0$, $\nabla F(0,0)=0$, 且 $F$ 是 $C^3$ 函数. $F$ 在原点的 Hessian 矩阵 $H_F(0)$ 与 $f$ 在 $P$ 的相同, 非退化.

对 $F$ 用第一问结论: 存在 $C^2$ 函数 $G_1, G_2$ 使得
$$
F(y) = y_1 G_1(y) + y_2 G_2(y), \quad G_i(0,0) = F_{y_i}(0,0) = 0.
$$

用第一问的构造方可得:  存在 $C^1$ 函数 $h_{11},h_{12},h_{21},h_{22}$ 使得

$$
G_1(y) = y_1 h_{11}(y) + y_2 h_{12}(y), \quad
G_2(y) = y_1 h_{21}(y) + y_2 h_{22}(y),
$$
代入 $F$ 得
$$
F(y) = a_{11}(y) y_1^2 + 2a_{12}(y) y_1 y_2 + a_{22}(y) y_2^2,
$$
这里 $a_{11}=h_{11}, \; a_{12}=\frac{h_{12}+h_{21}}{2}, \; a_{22}=h_{22}$ 是对称的 $C^1$ 矩阵函数 $A(y) = (a_{ij}(y))$, 且
$$
a_{ij}(0) = \frac{1}{2} F_{y_i y_j}(0).
$$
故 $A(0)$ 对称非退化.

由惯性定理, 取可逆线性变换 $z = L y$ 使得
$$
L^T A(0) L = D := \begin{bmatrix} \varepsilon_1 & 0 \\ 0 & \varepsilon_2 \end{bmatrix}, \quad \varepsilon_i = \pm 1.
$$
在 $z$ 坐标下,
$$
F(L^{-1} z) = z^T M(z) z, \quad M(z) = L^{-T} A(L^{-1} z) L^{-1},
$$
且 $M(0)=D$, $M(z)$ 对称 $C^1$.

要找局部微分同胚 $z = \Phi(u)$, $\Phi(0)=0$, 使得
$$
\Phi(u)^T M(\Phi(u)) \Phi(u) = u^T D u.
$$
设 $\Phi(u) = (I + N(u)) u$, $N(0)=0$, $N$ 为 $C^1$ 矩阵函数. 代入得矩阵方程
$$
(I+N(u))^T M((I+N(u))u) (I+N(u)) = D.
$$
定义映射
$$
\Psi(N, u) = (I+N)^T M((I+N)u) (I+N) - D.
$$
则 $\Psi(0,0)=0$, 且 $\Psi$ 关于 $N$ 在 $(0,0)$ 的导数为
$$
d_N\Psi(0,0)(H) = H^T D + D H.
$$
因为 $D$ 可逆对称, 该线性映射在对称矩阵空间上是同构. 由隐函数定理, 存在唯一 $C^1$ 函数 $N(u)$ 满足 $N(0)=0$ 且 $\Psi(N(u), u) = 0$.
于是 $\Phi(u) = (I+N(u))u$ 满足 $D\Phi(0)=I$, 是局部 $C^1$ 微分同胚, 且
$$
F(L^{-1} \Phi(u)) = u^T D u = \varepsilon_1 u_1^2 + \varepsilon_2 u_2^2.
$$

定义 $\varphi(x) = \Phi^{-1}(L(x-P))$, 则 $\varphi(P) = 0$, 且
$$
f \circ \varphi^{-1}(u) = f(P) + F(L^{-1} \Phi(u)) = f(P) + \varepsilon_1 u_1^2 + \varepsilon_2 u_2^2.
$$
$\varphi$ 即为所求的 $C^1$ 参数变换.
