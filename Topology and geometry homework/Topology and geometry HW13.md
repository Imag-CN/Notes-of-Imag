___

> [!problem] Problem 1
> Let $F: U \subset \mathbb{R}^{2} \longrightarrow \mathbb{R}^{3}$ be given by
>
> $$
> F(u, v)=(u \sin \alpha \cos v, u \sin \alpha \sin v, u \cos \alpha),
> $$
>
> $$
> (u, v) \in U=\{(u, v) \in \mathbb{R}^{2} ; u>0\}, \quad \alpha=\text{const}.
> $$
>
> a. Prove that $F$ is a local diffeomorphism of $U$ onto a cone $C$ with the vertex at the origin and $2\alpha$ as the angle of the vertex.
>
> b. Is $F$ a local isometry?

**Solution:**
**(a)** Compute the partial derivatives:
$$F_u = (\sin\alpha \cos v, \sin\alpha \sin v, \cos\alpha),$$
$$F_v = (-u\sin\alpha \sin v, u\sin\alpha \cos v, 0).$$
The cross product:
$$
F_u \times F_v=(-u\sin\alpha\cos\alpha\cos v, u\sin\alpha\cos\alpha\sin v, u\sin^2\alpha).
$$
Since $u>0$, this vector is nonzero (provided $\alpha$ is not an integer multiple of $\pi$). Therefore, the Jacobian matrix $DF(u,v)$ has full rank ($\operatorname{rank}=2$), so $F$ is an immersion. It is smooth and, locally, one-to-one. Hence, $F$ is a local diffeomorphism from $U$ onto its image $C$.

Now, the image $C$ satisfies:
$$x^2 + y^2 = (u \sin\alpha)^2, \quad z = u\cos\alpha.$$
Eliminating $u$ gives $x^2 + y^2 = z^2 \tan^2\alpha$. This is the equation of a circular cone with vertex at the origin and axis along the $z$-axis. The angle between the generatrix and the axis is $\alpha$, so the vertex angle is $2\alpha$.

**(b)** Compute the coefficients of the first fundamental form:
$$E = F_u \cdot F_u = \sin^2\alpha + \cos^2\alpha = 1,$$
$$F = F_u \cdot F_v = 0,$$
$$G = F_v \cdot F_v = u^2 \sin^2\alpha.$$
Thus, the induced metric is $I = du^2 + u^2 \sin^2\alpha \, dv^2$.

The Euclidean metric on the domain $U$ is $du^2 + dv^2$. For $I$ to be equal to the Euclidean metric, we require $u^2 \sin^2\alpha = 1$ for all $u>0$, which is impossible unless $\sin^2\alpha=1$ (i.e., $\alpha=\pi/2$). In that special case, the cone degenerates to a plane ($z=0$) and $F$ becomes a local isometry. For a general $\alpha \neq \pi/2$, $F$ is not a local isometry.
___

> [!problem] Problem 2
> Use the stereographic projection
>$$
>\pi^{-1}(u,v) =\begin{cases}
x = \dfrac{4u}{u^2 + v^2 + 4}, \\[6pt]
y = \dfrac{4v}{u^2 + v^2 + 4}, \\[6pt]
z = \dfrac{2(u^2 + v^2)}{u^2 + v^2 + 4}.
\end{cases}
>$$
>to show that the sphere is locally conformal to a plane.

**Proof:**
Let $f(u,v) = (x(u,v), y(u,v), z(u,v)) = \pi^{-1}(u,v)$, and let $\rho = u^2 + v^2 + 4$.

Compute partial derivatives:

$$f_u = \left( \frac{4\rho - 8u^2}{\rho^2}, -\frac{8uv}{\rho^2}, \frac{16u}{\rho^2} \right),$$
$$f_v = \left( -\frac{8uv}{\rho^2}, \frac{4\rho - 8v^2}{\rho^2}, \frac{16v}{\rho^2} \right).$$

Compute the coefficients of the first fundamental form:
$$
E = f_u \cdot f_u = \frac{(4\rho - 8u^2)^2 + (8uv)^2 + (16u)^2}{\rho^4}=\dfrac{16}{\rho^2}.
$$
$$
F = \frac{(4\rho - 8u^2)(-8uv) + (-8uv)(4\rho - 8v^2) + (16u)(16v)}{\rho^4}=0.
$$
By symmetry, $G = 16/\rho^2$.


Therefore, the induced metric is:

$$I = \frac{16}{\rho^2}(du^2 + dv^2).$$

Since $I$ is a scalar multiple $\lambda(u,v) = 16/(u^2+v^2+4)^2$ of the Euclidean metric $du^2 + dv^2$, the map $\pi^{-1}$ is conformal. Hence, the sphere is locally conformal to the plane via stereographic projection.
___

> [!problem] Problem 3
> We say that a differentiable map $\varphi: S_{1} \longrightarrow S_{2}$ preserves angles when for every $p \in S_{1}$ and every pair $v_{1}, v_{2} \in T_{p}(S_{1})$ we have
>
> $$
> \cos(v_{1}, v_{2}) = \cos(d\varphi_{p}(v_{1}), d\varphi_{p}(v_{2})).
> $$
>
> Prove that $\varphi$ is locally conformal if and only if it preserves angles.

**Proof:**
**($\Rightarrow$)** By definition, $\varphi$ is locally conformal if for each $p \in S_1$ there exists a neighborhood $U$ of $p$ and a positive function $\lambda: U \to \mathbb{R}^+$ such that for all tangent vectors $w_1, w_2 \in T_q(S_1)$, $q \in U$,
$$
\langle d\varphi_q(w_1), d\varphi_q(w_2) \rangle_{\varphi(q)} = \lambda(q)^2 \langle w_1, w_2 \rangle_q.
$$
That is, the differential $d\varphi_q$ scales the inner product by the factor $\lambda(q)^2$. Then for any $v_1, v_2 \in T_p(S_1)$,
$$
\cos(d\varphi_p(v_1), d\varphi_p(v_2)) = \frac{\langle d\varphi_p(v_1), d\varphi_p(v_2) \rangle}{\|d\varphi_p(v_1)\| \|d\varphi_p(v_2)\|} = \frac{\lambda^2 \langle v_1, v_2 \rangle}{\lambda \|v_1\| \cdot \lambda \|v_2\|} = \frac{\langle v_1, v_2 \rangle}{\|v_1\| \|v_2\|} = \cos(v_1, v_2).
$$
Hence, angle-preservation holds.

**($\Leftarrow$)** Assume $\varphi$ preserves angles. Fix $p \in S_1$. Let $\{e_1, e_2\}$ be an orthonormal basis of $T_p(S_1)$. Since $\varphi$ preserves angles, the images $w_i = d\varphi_p(e_i)$ satisfy
$$
\cos(e_1, e_2) = 0 = \frac{\langle w_1, w_2 \rangle}{\|w_1\| \|w_2\|} \quad \Rightarrow \quad \langle w_1, w_2 \rangle = 0.
$$
So $w_1, w_2$ are orthogonal. Moreover, for any unit vector $v = \cos\theta \, e_1 + \sin\theta \, e_2$,
$$
\cos(v, e_1) = \cos\theta = \cos(d\varphi_p(v), w_1) = \frac{\langle d\varphi_p(v), w_1 \rangle}{\|d\varphi_p(v)\| \|w_1\|}.
$$
But $d\varphi_p(v) = \cos\theta \, w_1 + \sin\theta \, w_2$, so
$$
\langle d\varphi_p(v), w_1 \rangle = \cos\theta \|w_1\|^2, \quad \|d\varphi_p(v)\|^2 = \cos^2\theta \|w_1\|^2 + \sin^2\theta \|w_2\|^2.
$$
Thus,
$$
\cos\theta = \frac{\cos\theta \|w_1\|^2}{\sqrt{\cos^2\theta \|w_1\|^2 + \sin^2\theta \|w_2\|^2} \cdot \|w_1\|}.
$$
If $\cos\theta \neq 0$, cancel $\cos\theta$ and cross-multiply:
$$
\sqrt{\cos^2\theta \|w_1\|^2 + \sin^2\theta \|w_2\|^2} = \|w_1\|^2.
$$
Square both sides: $\cos^2\theta \|w_1\|^2 + \sin^2\theta \|w_2\|^2 = \|w_1\|^4$. Since this holds for all $\theta$, compare coefficients of $\cos^2\theta$ and $\sin^2\theta$:
$$
\|w_1\|^2 = \|w_1\|^4, \quad \|w_2\|^2 = 0 \quad \text{or} \quad \|w_1\|^2 = \|w_2\|^2.
$$
But $\|w_1\|>0$ (since $\varphi$ is an immersion, otherwise angle-preservation fails), so $\|w_1\|^2 = 1$ and $\|w_2\|^2 = \|w_1\|^2 = 1$. Therefore $\|w_1\| = \|w_2\| =: \lambda(p)$.

Thus for the orthonormal basis $\{e_1, e_2\}$, we have
$$
\langle d\varphi_p(e_i), d\varphi_p(e_j) \rangle = \lambda(p)^2 \delta_{ij}.
$$
For any $v_1, v_2 \in T_p(S_1)$, write $v_k = a_k e_1 + b_k e_2$, $k=1,2$. Then
$$
\langle d\varphi_p(v_1), d\varphi_p(v_2) \rangle = \lambda(p)^2 (a_1 a_2 + b_1 b_2) = \lambda(p)^2 \langle v_1, v_2 \rangle.
$$
Since $p$ was arbitrary, $\varphi$ is locally conformal.
___

> [!problem] Problem 4
> Let $\varphi: R^{2} \longrightarrow R^{2}$ be given by $\varphi(x,y) =(u(x,y),v(x,y))$, where $u$ and $v$ are differentiable functions that satisfy the Cauchy-Riemann equations
>
> $$
> u_{x}=v_{y},\quad u_{y}=-v_{x}.
> $$
>
> Show that $\varphi$ is a local conformal map from $R^{2}-Q$ into $R^{2}$, where $Q=\left\{(x,y)\in R^{2}:u_{x}^{2}+u_{y}^{2}=0\right\}.$

**Proof:**
Compute:
$$
E = u_x^2 + v_x^2,
$$
$$
F = u_x u_y + v_x v_y,
$$
$$
G = u_y^2 + v_y^2.
$$
Using the Cauchy–Riemann equations, we obtain:
$$
E = u_x^2 + v_x^2,
$$
$$
G = u_y^2 + v_y^2 = v_x^2 + u_x^2 = E,
$$
$$
F = u_x u_y + v_x v_y = u_x(-v_x) + v_x u_x = 0.
$$
Therefore, on the set $\mathbb{R}^2 \setminus Q$ where $u_x^2 + u_y^2 \neq 0$, we have $E = G > 0$ and $F = 0$. Hence the first fundamental form is
$$
I = E(du^2 + dv^2),
$$
which is a positive scalar multiple $\lambda^2 = E$ of the Euclidean metric $du^2 + dv^2$. Therefore $\varphi$ is a local conformal map on $\mathbb{R}^2 \setminus Q$.
___

>[!problem] Problem 5
>A diffeomorphism $\varphi:S\longrightarrow\bar{S}$ is said to be area-preserving if the area of any region $R\subset S$ is equal to the area of $\varphi(R)$. Prove that if $\varphi$ is area-preserving and conformal, then $\varphi$ is an isometry.

**Proof:**
Let $g$ and $\bar{g}$ denote the Riemannian metrics on $S$ and $\bar{S}$, respectively. In local coordinates $(u,v)$, the area element on $S$ is $dA = \sqrt{\det g} \, du \wedge dv$, and the pullback of the area element on $\bar{S}$ is
$$
\varphi^* d\bar{A} = \sqrt{\det (\varphi^* \bar{g})} \, du \wedge dv = \sqrt{\lambda^4 \det g} \, du \wedge dv = \lambda^2 dA.
$$
Since $\varphi$ is area-preserving, for any region $R$ we have
$$ \int_R dA = \int_{\varphi(R)} d\bar{A} = \int_R \varphi^* d\bar{A} = \int_R \lambda^2 dA. $$
This implies $\lambda^2 = 1$ almost everywhere, and by continuity, $\lambda \equiv 1$ on $S$. Therefore,
$$ \varphi^* \bar{g} = g, $$
which means $\varphi$ is an isometry.
___

> [!problem] Problem 6
>Let $x: U \subset \mathbb{R}^{2} \longrightarrow S$ be the parametrization of a surface of revolution $S$:
>
> $$
> \begin{align*} x(u,v) &=(f(v)\cos u, f(v)\sin u, g(v)), \qquad f(v)>0, \\
> U &=\{(u,v)\in \mathbb{R}^{2};\,0<u<2\pi,\ a<v<b\}.
> \end{align*}
> $$
>
> a. Show that the map $\varphi: U \longrightarrow \mathbb{R}^{2}$ given by
>
> $$\varphi(u,v)=\left(u, \int \frac{\sqrt{(f^{\prime}(v))^{2}+(g^{\prime}(v))^{2}}}{f(v)}\, dv\right)$$
>
> is a local diffeomorphism.
>
> b. Use part a to prove that a surface of revolution $S$ is locally conformal to a plane in such a way that each local conformal map $\theta: V\subset S\rightarrow \mathbb{R}^{2}$ takes the parallels and the meridians of the neighborhood $V$ into an orthogonal system of straight lines in $\theta(V)\subset \mathbb{R}^{2}$.
>
> c. Show that the map $\psi: U \longrightarrow \mathbb{R}^{2}$ given by
>
> $$
> \psi(u,v)=\left(u, \int f(v)\sqrt{(f^{\prime}(v))^{2}+(g^{\prime}(v))^{2}}\, dv\right)
> $$
>
> is a local diffeomorphism.
>
> d. Use part c to prove that for each point $p$ of a surface of revolution $S$ there exists a neighborhood $V\subset S$ and a map $\bar{\theta}: V\longrightarrow \mathbb{R}^{2}$ of $V$ into a plane that is area-preserving.

**Proof:**
**(a)** Let $\varphi(u,v) = (u, h(v))$, where $h(v) = \int \frac{\sqrt{(f'(v))^2 + (g'(v))^2}}{f(v)} \, dv$. The Jacobian matrix of $\varphi$ is
$$
D\varphi = \begin{pmatrix} 1 & 0 \\ 0 & h'(v) \end{pmatrix}.
$$
Since $f(v) > 0$ and $f'(v), g'(v)$ are smooth, the integrand is smooth and $h'(v) = \frac{\sqrt{(f'(v))^2 + (g'(v))^2}}{f(v)} > 0$. Hence $\det(D\varphi) = h'(v) > 0$, so $\varphi$ is a local diffeomorphism.

**(b)** Compute the first fundamental form of $S$:
$$x_u = (-f(v)\sin u, f(v)\cos u, 0), \quad x_v = (f'(v)\cos u, f'(v)\sin u, g'(v)).$$
Then
$$E = \langle x_u, x_u \rangle = f(v)^2, \quad F = \langle x_u, x_v \rangle = 0, \quad G = \langle x_v, x_v \rangle = (f'(v))^2 + (g'(v))^2.$$
Thus $I = f(v)^2 du^2 + \big((f'(v))^2 + (g'(v))^2\big) dv^2$.

Now consider the coordinate change $(u,v) \mapsto (u, w)$ with $w = h(v)$ as in part (a). Then $dw = h'(v) dv = \frac{\sqrt{(f'(v))^2 + (g'(v))^2}}{f(v)} dv$, so $dv = \frac{f(v)}{\sqrt{(f'(v))^2 + (g'(v))^2}} dw$. Substitute into $I$:
$$
I = f(v)^2 du^2 + \big((f'(v))^2 + (g'(v))^2\big) dv^2 = f(v)^2 (du^2 + dw^2).
$$
Thus in coordinates $(u,w)$, the first fundamental form is a scalar multiple $f(v)^2$ of the Euclidean metric $du^2 + dw^2$. Hence the map $\theta = \varphi \circ x^{-1}: V \subset S \to \mathbb{R}^2$ (where $V = x(U)$) is conformal. Moreover, $u$-curves (parallels) map to lines $w = \text{const}$, and $v$-curves (meridians) map to lines $u = \text{const}$, which are orthogonal.

**(c)** Let $\psi(u,v) = (u, k(v))$, where $k(v) = \int f(v)\sqrt{(f'(v))^2 + (g'(v))^2} \, dv$. Its Jacobian is
$$
D\psi = \begin{pmatrix} 1 & 0 \\ 0 & k'(v) \end{pmatrix},
\quad k'(v) = f(v)\sqrt{(f'(v))^2 + (g'(v))^2} > 0.
$$
Thus $\det(D\psi) = k'(v) > 0$, so $\psi$ is a local diffeomorphism.

**(d)** Consider the coordinate change $(u,v) \mapsto (u, z)$ with $z = k(v)$. Then $dz = k'(v) dv = f(v)\sqrt{(f'(v))^2 + (g'(v))^2} \, dv$, so $dv = \frac{dz}{f(v)\sqrt{(f'(v))^2 + (g'(v))^2}}$. Substitute into the area element of $S$:
$$dA = \sqrt{EG - F^2} \, du \wedge dv = f(v)\sqrt{(f'(v))^2 + (g'(v))^2} \, du \wedge dv = du \wedge dz.$$
Hence the map $\bar{\theta} = \psi \circ x^{-1}: V \to \mathbb{R}^2$ pulls back the Euclidean area element $du \wedge dz$ to $dA$, i.e., it is area-preserving.
___

> [!problem] Problem 7
>Show that if $\mathbf{x}$ is an isothermal parametrization, that is, $E=G=\lambda(u,v)$ and $F=0$, then
>
>$$
>K=-\frac{1}{2\lambda}\Delta(\log\lambda),
>$$
>
> where $\Delta\varphi$ denotes the Laplacian $(\partial^{2}\varphi/\partial u^{2})+(\partial^{2}\varphi/\partial v^{2})$ of the function $\varphi$. Conclude that when $E=G=(u^{2}+v^{2}+c)^{-2}$ and $F=0$, then $K=\text{const.}=4c$.

**Solution.**
For an isothermal parametrization, the first fundamental form is $I = \lambda(u,v)(du^2 + dv^2)$. The Gaussian curvature $K$ can be computed from the formula
$$K = -\frac{1}{2\lambda} \Delta \log \lambda,$$
where $\Delta = \frac{\partial^2}{\partial u^2} + \frac{\partial^2}{\partial v^2}$ is the Laplacian. Derivation: In isothermal coordinates, the Christoffel symbols simplify, and the Gaussian curvature reduces to this expression (e.g., via Brioschi's formula with $E=G=\lambda$, $F=0$).

Now let $\lambda(u,v) = (u^2 + v^2 + c)^{-2}$. Compute $\log \lambda$:
$$\log \lambda = -2 \log(u^2 + v^2 + c).$$
Let $r^2 = u^2 + v^2$ and $\rho = u^2 + v^2 + c$. Then $\log \lambda = -2 \log \rho$.

Compute the Laplacian:
$$\frac{\partial}{\partial u} \log \rho = \frac{2u}{\rho}, \quad \frac{\partial^2}{\partial u^2} \log \rho = \frac{2}{\rho} - \frac{4u^2}{\rho^2}.$$
Similarly,
$$\frac{\partial^2}{\partial v^2} \log \rho = \frac{2}{\rho} - \frac{4v^2}{\rho^2}.$$
Thus
$$
\Delta \log \rho = \left( \frac{2}{\rho} - \frac{4u^2}{\rho^2} \right) + \left( \frac{2}{\rho} - \frac{4v^2}{\rho^2} \right) = \frac{4(\rho - r^2)}{\rho^2}.
$$
But $\rho = r^2 + c$, so $\rho - r^2 = c$. Hence
$$
\Delta \log \rho = \frac{4c}{\rho^2}.
$$
Now $\Delta \log \lambda = -2 \Delta \log \rho = -\frac{8c}{\rho^2}$. Therefore,
$$
K = -\frac{1}{2\lambda} \Delta \log \lambda = -\frac{1}{2\rho^{-2}} \left( -\frac{8c}{\rho^2} \right) = -\frac{\rho^2}{2} \left( -\frac{8c}{\rho^2} \right) = 4c.
$$
Thus $K$ is constant, equal to $4c$.
___

> [!problem] Problem 8
> Verify that the surfaces
>
> $$\mathbf{x}(u, v)=(u\cos v,u\sin v,\log u)$$
>
> $$\bar{\mathbf{x}}(u, v)=(u\cos v,u\sin v,v)$$
>
> have equal Gaussian curvature at the points $\mathbf{x}(u, v)$ and $\bar{\mathbf{x}}(u, v)$ but that the mapping $\bar{x}\circ \mathbf{x}^{-1}$ is not an isometry. This shows that the "converse" of the Gauss theorems is not true.

**Proof:**
Compute for the for surface:
$$
\mathbf{x}_u = (\cos v, \sin v, \tfrac{1}{u}), \quad \mathbf{x}_v = (-u\sin v, u\cos v, 0).
$$
$$
\mathbf{x}_{uu} = (0, 0, -\tfrac{1}{u^2}), \quad \mathbf{x}_{uv} = (-\sin v, \cos v, 0), \quad \mathbf{x}_{vv} = (-u\cos v, -u\sin v, 0).
$$
$$
E = \mathbf{x}_u \cdot \mathbf{x}_u = \cos^2 v + \sin^2 v + \frac{1}{u^2} = 1 + \frac{1}{u^2},
$$
$$F = \mathbf{x}_u \cdot \mathbf{x}_v = -u\cos v \sin v + u\sin v \cos v + 0 = 0,$$
$$G = \mathbf{x}_v \cdot \mathbf{x}_v = u^2 \sin^2 v + u^2 \cos^2 v = u^2.$$
$$
\mathbf{x}_u \times \mathbf{x}_v = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ \cos v & \sin v & 1/u \\ -u\sin v & u\cos v & 0 \end{vmatrix} = (-\cos v, -\sin v, u).
$$
$$
|\mathbf{x}_u \times \mathbf{x}_v| = \sqrt{u^2+1}.
$$
$$
\mathbf{N} = \frac{1}{\sqrt{u^2+1}}(-\cos v, -\sin v, u).
$$
$$
e = \mathbf{x}_{uu} \cdot \mathbf{N} = -\frac{1}{u\sqrt{u^2+1}},
$$
$$
f = \mathbf{x}_{uv} \cdot \mathbf{N}  = 0,
$$
$$
g = \mathbf{x}_{vv} \cdot \mathbf{N}  = \frac{u}{\sqrt{u^2+1}}.
$$
$$K_1 = \frac{eg - f^2}{EG - F^2} = \frac{-\dfrac{1}{ u^2+1} }{u^2+1} = -\frac{1}{(u^2+1)^2}.$$

Compute Gaussian curvature for the second surface:
$$\bar{\mathbf{x}}_u = (\cos v, \sin v, 0), \quad \bar{\mathbf{x}}_v = (-u\sin v, u\cos v, 1).$$
$$
\bar{\mathbf{x}}_{uu} = (0,0,0), \quad \bar{\mathbf{x}}_{uv} = (-\sin v, \cos v, 0), \quad \bar{\mathbf{x}}_{vv} = (-u\cos v, -u\sin v, 0).
$$
$$\bar{E} = 1, \quad \bar{F} = 0, \quad \bar{G} = u^2+1.$$
$$\bar{\mathbf{x}}_u \times \bar{\mathbf{x}}_v = (\sin v, -\cos v, u), \quad |\bar{\mathbf{x}}_u \times \bar{\mathbf{x}}_v| = \sqrt{\sin^2 v + \cos^2 v + u^2} = \sqrt{1+u^2}.$$
$$\bar{\mathbf{N}} = \frac{1}{\sqrt{1+u^2}}(\sin v, -\cos v, u).$$
$$\bar{e} = 0,$$
$$\bar{f} = \bar{\mathbf{x}}_{uv} \cdot \bar{\mathbf{N}} = \frac{1}{\sqrt{1+u^2}}(-\sin^2 v - \cos^2 v + 0) = -\frac{1}{\sqrt{1+u^2}},$$
$$\bar{g} = 0.
$$
$$K_2 = \frac{\bar{e}\bar{g} - \bar{f}^2}{\bar{E}\bar{G} - \bar{F}^2} = \frac{0 - \left(-\frac{1}{\sqrt{1+u^2}}\right)^2}{u^2+1} = -\frac{1}{(1+u^2)^2}.$$


Thus at corresponding points on the two surfaces, the Gaussian curvatures are equal.

However, the first fundamental forms are:
$$
\mathbf{x}:I_1 = (1+1/u^2) du^2 + u^2 dv^2.
$$
$$
\bar{\mathbf{x}}:I_2 = du^2 + (1+u^2) dv^2.
$$
The mapping $\bar{\mathbf{x}} \circ \mathbf{x}^{-1}$ sends the point with coordinates $(u,v)$ on the first surface to the point with the same coordinates on the second surface. Under this correspondence, the pulled‑back metric is $I_2$, which is different from $I_1$ for general $u$ (e.g., compare the coefficients of $du^2$ and $dv^2$). Hence the mapping is not an isometry.
___

> [!problem] Problem 9
> Does there exist a surface $x = x(u,v)$ with $E = 1$, $F = 0$, $G = \cos^2 u$ and $e = \cos^2 u$, $f = 0$, $g = 1$?

**Solution:**
For a given set of coefficients $\{E,F,G,e,f,g\}$ to be the first and second fundamental forms of a surface, they must satisfy the Gauss equation and the two Codazzi–Mainardi equations.

The second Codazzi equation is:
$$f_v - g_u = e\,\Gamma_{22}^1 + f(\Gamma_{22}^2 - \Gamma_{12}^1) - g\,\Gamma_{12}^2.$$
Substitute $f=0$, $g=1$, $e=\cos^2 u$:
LHS: $f_v - g_u = 0 - 0 = 0.$
RHS: $\cos^2 u (\cos u \sin u) + 0 - 1\cdot (-\tan u) = \cos^3 u \sin u + \tan u.$

Thus the equation requires
$$0 = \cos^3 u \sin u + \tan u = \sin u\left(\cos^3 u + \frac{1}{\cos u}\right).$$
This equality holds only when $\sin u = 0$ (i.e., $u = n\pi$). Thus there doesn't exist such a surface.
___

> [!problem] Problem 10
> Compute the Christoffel symbols for an open set of the plane
>
> a. In cartesian coordinates.
>
> b. In polar coordinates.
>
> Use the Gauss formula to compute $K$ in both cases.

**Proof:**
**(a)** The metric is
$$ds^2 = dx^2 + dy^2,$$
so
$$E = 1, \quad F = 0, \quad G = 1.$$

All first partial derivatives $E_x, E_y, F_x, F_y, G_x, G_y$ are zero. The Christoffel symbols are given by
$$\Gamma_{ij}^k = \frac12 g^{kl} \bigl( \partial_i g_{jl} + \partial_j g_{il} - \partial_l g_{ij} \bigr),$$
where $(g_{ij}) = \begin{pmatrix}1&0\\0&1\end{pmatrix}$ and $(g^{ij})$ is its inverse. Since all $\partial_i g_{jk}=0$, we obtain
$$\Gamma_{ij}^k = 0 \quad \text{for all } i,j,k.$$
Now apply the Gauss formula for the curvature in terms of the Christoffel symbols. For a metric with $F=0$, one expression is
$$K = -\frac{1}{2\sqrt{EG}} \Bigl[ \partial_x\!\Bigl(\frac{G_x}{\sqrt{EG}}\Bigr) + \partial_y\!\Bigl(\frac{E_y}{\sqrt{EG}}\Bigr) \Bigr].$$
With $E=G=1$ and $\sqrt{EG}=1$, we have $G_x=0$, $E_y=0$, hence
$$
K = 0.
$$
**(b)** The metric becomes
$$ds^2 = dr^2 + r^2 d\theta^2,$$
so
$$
E = 1, \quad F = 0, \quad G = r^2.
$$
Compute the non‑zero first derivatives:
$$
G_r = 2r, \qquad \text{all other } E_r, E_\theta, F_r, F_\theta, G_\theta = 0.
$$
The Christoffel symbols (only non‑zero ones):
$$\Gamma_{12}^2 = \Gamma_{21}^2 = \frac{G_r}{2G} = \frac{2r}{2r^2} = \frac{1}{r},$$
$$\Gamma_{22}^1 = -\frac{G_r}{2E} = -\frac{2r}{2} = -r.$$
All other $\Gamma_{ij}^k = 0$.

Now compute $K$ via the Gauss formula. Again with $F=0$,
$$K = -\frac{1}{2\sqrt{EG}} \Bigl[ \partial_r\!\Bigl(\frac{G_r}{\sqrt{EG}}\Bigr) + \partial_\theta\!\Bigl(\frac{E_\theta}{\sqrt{EG}}\Bigr) \Bigr].$$
Here $\sqrt{EG} = r$, $G_r = 2r$, so
$$\frac{G_r}{\sqrt{EG}} = \frac{2r}{r} = 2, \qquad \partial_r\!\Bigl(\frac{G_r}{\sqrt{EG}}\Bigr) = \partial_r(2) = 0.$$
Also $E_\theta=0$, hence
$$
K = -\frac{1}{2r}\,(0+0) = 0.
$$