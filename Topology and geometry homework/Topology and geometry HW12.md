___

>[!problem] Problem 1
>*(Theorem of Beltrami-Enneper)* Prove that the absolute value of the torsion $\tau$ at a point of an asymptotic curve, whose curvature is nowhere zero, is given by
>
>$$
>|\tau|=\sqrt{-K},
>$$
>
>where $K$ is the Gaussian curvature of the surface at the given point.

**Proof:**
Let $\gamma$ be an asymptotic curve on the surface with arc length parameter $s$, curvature $\kappa(s) \ne 0$, and torsion $\tau(s)$. Let $\{\mathbf{T}, \mathbf{N}, \mathbf{B}\}$ be its Frenet frame, and $\mathbf{n}$ the unit surface normal.

First we have $\mathbf{n} \cdot \mathbf{T}=0$ since $\mathbf{T}\in T_{p}S$. Differentiating gives $\mathbf{n}'\cdot \mathbf{T} + \mathbf{n} \cdot \mathbf{T}' = 0$. Since $\mathbf{n}'\cdot \mathbf{T}=0$ (asymptotic condition) and $\mathbf{T}'=\kappa \mathbf{N}$, we have $\kappa (\mathbf{n}\cdot \mathbf{N})=0$. Since $\kappa \ne 0$, we have $\mathbf{n} \cdot \mathbf{N}=0$. Hence $\mathbf{n}$ is orthogonal to both $\mathbf{T}$ and $\mathbf{N}$, so $\mathbf{n} \parallel \mathbf{B}$. Thus $\mathbf{n} = \pm \mathbf{B}$.

Differentiate $\mathbf{n} = \pm \mathbf{B}$ and use $\mathbf{B}' = \tau \mathbf{N}$, we get $\mathbf{n}' = \pm \tau \mathbf{N}$.

Also, $\mathbf{n}' = -\mathrm{d}N_{p}(\mathbf{T})$. In the orthonormal tangent basis $\{\mathbf{T}, \mathbf{N}\}$, write $-\mathrm{d}N_{p}(\mathbf{T}) = a\mathbf{T} + b\mathbf{N}$. Since $\gamma$ is asymptotic, $a = -\mathrm{d}N_{p}(\mathbf{T})\cdot \mathbf{T} = II(\mathbf{T},\mathbf{T})=0$, so $-\mathrm{d}N_{p}(\mathbf{T}) = b\mathbf{N}$.

The Gaussian curvature is $K = \det (\mathrm{d}N_{p}(\mathbf{T})) = a d - b^2 = -b^2$. Thus $b^2 = -K$.

Since $-\mathrm{d}N_{p}(\mathbf{T}) = b\mathbf{N}=\mathbf{n}' = \pm \tau \mathbf{N}$ and $b^2 = -K$, we have $|\tau|=\sqrt{-K}$.
___

>[!problem] Problem 2
>If the surface $S_{1}$ intersects the surface $S_{2}$ along the regular curve $C$, then the curvature $k$ of $C$ at $p \in C$ is given by
>
>$$
>k^{2}\sin^{2}\theta=\lambda_{1}^{2}+\lambda_{2}^{2}-2\lambda_{1}\lambda_{2}\cos\theta,
>$$
>
>where $\lambda_{1}$ and $\lambda_{2}$ are the normal curvatures at $p$, along the tangent line to $C$, of $S_{1}$ and $S_{2}$, respectively, and $\theta$ is the angle made up by the normal vectors of $S_{1}$ and $S_{2}$ at $p$.

**Proof:** 
Let $\mathbf{n}_1, \mathbf{n}_2$ be unit normals to $S_1, S_2$ at $p$, $\mathbf{T}$ the unit tangent to $C$, and $\mathbf{k}_g=\mathbf{T}'=k\mathbf{N}$ the curvature vector of $C$. Then $\lambda_1=\mathbf{k}_g\cdot\mathbf{n}_1$, $\lambda_2=\mathbf{k}_g\cdot\mathbf{n}_2$. Let $\cos\theta=\mathbf{n}_1\cdot\mathbf{n}_2$.

Since $C$ lies on both surfaces, $\mathbf{T}$ is orthogonal to both $\mathbf{n}_{1}$ and $\mathbf{n}_{2}$. Therefore, $\mathbf{k}_g$ (as it is orthogonal to $\mathbf{T}$,) lies in the span of $\mathbf{n}_1$ and $\mathbf{n}_2$:
$$ \mathbf{k}_g=\alpha\mathbf{n}_1+\beta\mathbf{n}_2. $$
Dotting with $\mathbf{n}_1$ and $\mathbf{n}_2$ gives
$$ \lambda_1=\alpha+\beta\cos\theta,\quad \lambda_2=\alpha\cos\theta+\beta. $$
Solving,
$$ \alpha=\frac{\lambda_1-\lambda_2\cos\theta}{\sin^2\theta},\quad \beta=\frac{\lambda_2-\lambda_1\cos\theta}{\sin^2\theta}. $$

Now compute $k^2=\|\mathbf{k}_g\|^2=\alpha^2+\beta^2+2\alpha\beta\cos\theta$:
$$
k^2=\frac{(\lambda_1-\lambda_2\cos\theta)^2+(\lambda_2-\lambda_1\cos\theta)^2+2(\lambda_1-\lambda_2\cos\theta)(\lambda_2-\lambda_1\cos\theta)\cos\theta}{\sin^4\theta}.
$$
Rearranging yields the conclusion:
$$
k^{2}\sin^{2}\theta=\lambda_{1}^{2}+\lambda_{2}^{2}-2\lambda_{1}\lambda_{2}\cos\theta.
$$
___

>[!problem] Problem 3
>*(Theorem of Joachimsthal)* Suppose that $S_{1}$ and $S_{2}$ intersect along a regular curve $C$ and make an angle $\theta(p)$, $p \in C$.
>
>Assume that $C$ is a line of curvature of $S_{1}$. Prove that $\theta(p)$ is constant if and only if $C$ is a line of curvature of $S_{2}$.

**Proof:**
($\Leftarrow$)Assume $C$ is a line of curvature of $S_2$. Let $\mathbf{n}_1, \mathbf{n}_2$ be the unit normals of $S_1, S_2$, and $\mathbf{T}$ the unit tangent of $C$. Since $C$ is a line of curvature on $S_1$, we have $\frac{d}{ds}\mathbf{n}_1 = -\lambda_1 \mathbf{T}$ for some $\lambda_1$ (the principal curvature). Similarly, since $C$ is a line of curvature on $S_2$, $\frac{d}{ds}\mathbf{n}_2 = -\lambda_2 \mathbf{T}$. Then
$$
\frac{d}{ds}\cos\theta = \frac{d}{ds}(\mathbf{n}_1 \cdot \mathbf{n}_2) = (-\lambda_1 \mathbf{T})\cdot\mathbf{n}_2 + \mathbf{n}_1\cdot(-\lambda_2 \mathbf{T}) = -\lambda_1(\mathbf{T}\cdot\mathbf{n}_2) - \lambda_2(\mathbf{T}\cdot\mathbf{n}_1).
$$
Since $\mathbf{T}$ is tangent to both surfaces, $\mathbf{T}\cdot\mathbf{n}_1 = \mathbf{T}\cdot\mathbf{n}_2 = 0$. Hence $\frac{d}{ds}\cos\theta = 0$, so $\cos\theta$ and thus $\theta$ is constant.

($\Rightarrow$) Now assume $\theta$ is constant. We know $\frac{d}{ds}\mathbf{n}_1 = -\lambda_1 \mathbf{T}$. Let $\frac{d}{ds}\mathbf{n}_2 = \alpha \mathbf{T} + \beta \mathbf{N}$, where $\mathbf{N}$ is a unit vector perpendicular to $\mathbf{T}$ in the tangent plane to $S_2$ (e.g., the direction of the principal curvature). Since $\mathbf{n}_2\cdot \mathbf{T}=0$, differentiating gives $\frac{d}{ds}\mathbf{n}_2 \cdot \mathbf{T} + \mathbf{n}_2 \cdot \mathbf{T}' = 0$. As $\mathbf{T}' = k \mathbf{N}_c$ (the curvature vector of $C$) and $\mathbf{n}_2$ is normal to $S_2$, $\mathbf{n}_2 \cdot \mathbf{T}'$ is the normal curvature $\lambda_2$ of $S_2$ in direction $\mathbf{T}$. Thus $\alpha = -\lambda_2$.
Now differentiate $\cos\theta = \mathbf{n}_1\cdot\mathbf{n}_2$:
$$
0 = \frac{d}{ds}\cos\theta = (-\lambda_1 \mathbf{T})\cdot\mathbf{n}_2 + \mathbf{n}_1\cdot(\alpha \mathbf{T} + \beta \mathbf{N}) = -\lambda_1(\mathbf{T}\cdot\mathbf{n}_2) + \alpha(\mathbf{n}_1\cdot\mathbf{T}) + \beta(\mathbf{n}_1\cdot\mathbf{N}).
$$
Since $\mathbf{T}\cdot\mathbf{n}_2 = 0$ and $\mathbf{n}_1\cdot\mathbf{T}=0$, we get $0 = \beta(\mathbf{n}_1\cdot\mathbf{N})$. Since $\mathbf{n}_1$ and $\mathbf{n}_2$ are at constant angle $\theta$, and $\mathbf{N}$ is in the tangent plane of $S_2$, $\mathbf{n}_1$ generally has a component along $\mathbf{N}$ (unless $\theta=0$ or $\pi$, trivial cases). Thus $\beta = 0$. Therefore $\frac{d}{ds}\mathbf{n}_2 = -\lambda_2 \mathbf{T}$, meaning $C$ is a line of curvature of $S_2$.
___

>[!problem] Problem 4
>Let $\lambda_{1}, \ldots, \lambda_{m}$ be the normal curvatures at $p \in S$ along directions making angles $0$, $2\pi / m$, $\ldots$, $(m-1)2\pi / m$ with a principal direction. Prove that
>
>$$ \lambda_{1} + \cdots + \lambda_{m} = m H, $$
>
>where $H$ is the mean curvature at $p$.

**Proof:**
Let $k_1$ and $k_2$ be the principal curvatures at $p$, and let $\varphi$ be the angle a given direction makes with the first principal direction. By Euler's formula, the normal curvature in the direction $\varphi$ is:
$$
\lambda(\varphi) = k_1 \cos^2\varphi + k_2 \sin^2\varphi.
$$
The given directions correspond to $\varphi_j = (j-1)\frac{2\pi}{m}$ for $j=1,\dots,m$. Therefore,
$$
\lambda_j = \lambda(\varphi_j) = k_1 \cos^2\varphi_j + k_2 \sin^2\varphi_j.
$$
Summing over $j$:
$$
\sum_{j=1}^m \lambda_j = k_1 \sum_{j=1}^m \cos^2\varphi_j + k_2 \sum_{j=1}^m \sin^2\varphi_j.
$$
Since $\varphi_j$ are equally spaced angles on the circle, we known for $m \ge 1$:
$$
\sum_{j=1}^m \cos^2\varphi_j = \sum_{j=1}^m \frac{1+\cos(2\varphi_j)}{2} = \frac{m}{2} + \frac12 \sum_{j=1}^m \cos(2\varphi_j)= \dfrac{m}{2}
$$
$$
\sum_{j=1}^m \sin^2\varphi_j = \sum_{j=1}^m \frac{1-\cos(2\varphi_j)}{2} = \frac{m}{2} - \frac12 \sum_{j=1}^m \cos(2\varphi_j) = \frac{m}{2}.
$$

Therefore,
$$
\sum_{j=1}^m \lambda_j = k_1 \cdot \frac{m}{2} + k_2 \cdot \frac{m}{2}  = m H.
$$
___

>[!problem] Problem 5
>Let $C \subset S$ be a regular curve in $S$. Let $p \in C$ and $\alpha(s)$ be a parametrization of $C$ in $p$ by arc length so that $\alpha(0) = p$. Choose in $T_{p}(S)$ an orthonormal positive basis $\{t, h\}$, where $t = \alpha'(0)$. The geodesic torsion $\tau_{g}$ of $C \subset S$ at $p$ is defined by
>
>$$ \tau_{g} = \left\langle \frac{dN}{ds}(0), h \right\rangle. $$
>
>Prove that
>
>**a.** $\tau_{g} = (k_{1} - k_{2}) \cos \varphi \sin \varphi$, where $\varphi$ is the angle from $e_{1}$ to $t$.
>
>**b.** If $\tau$ is the torsion of $C$, $n$ is the (principal) normal vector of $C$ and $\cos \theta = \langle N, n \rangle$, then
>
>$$
>\frac{d\theta}{ds} = \tau - \tau_{g}.
>$$
>
>**c.** The lines of curvature of $S$ are characterized by having geodesic torsion identically zero.

**Proof:**
**a.** Let $\{e_1, e_2\}$ be the principal directions at $p$ with corresponding principal curvatures $k_1, k_2$, and let $N$ be the unit normal. Then $dN_p(e_1) = -k_1 e_1$, $dN_p(e_2) = -k_2 e_2$.
The tangent vector $t$ can be written as $t = \cos\varphi \, e_1 + \sin\varphi \, e_2$. The vector $h$ is chosen such that $\{t, h\}$ is a positive orthonormal basis of $T_p(S)$. Thus $h = -\sin\varphi \, e_1 + \cos\varphi \, e_2$.
Now compute $\tau_g = \langle \frac{dN}{ds}(0), h \rangle$. Since $\frac{dN}{ds} = dN_p(t)$, we have
$$
\frac{dN}{ds} = dN_p(\cos\varphi \, e_1 + \sin\varphi \, e_2) = -k_1\cos\varphi \, e_1 - k_2\sin\varphi \, e_2.
$$
Then
$$
\tau_g = \langle -k_1\cos\varphi \, e_1 - k_2\sin\varphi \, e_2, \, -\sin\varphi \, e_1 + \cos\varphi \, e_2 \rangle = (k_1 - k_2)\cos\varphi\sin\varphi.
$$

**b.** Let $B=t\times n$, then by Frenet frame, $\dfrac{d}{ds} n=-kt-\tau B$, where $k$ is the curvature of $C$. Since $N,h,n,B$ are all orthogonal to $t$, they all lie in $\mathrm{span}\{ N,h \}$. Since $n \bot B,h\bot N,\cos\theta=\left< N,n \right>$ and $n\times B=h\times N=t$ (which indicates the orientation), we can observe the graph to yield 
$$
n=\cos \theta \cdot N+\sin\theta \cdot h,B=\sin\theta \cdot N-\cos\theta \cdot h.\tag{\dagger}
$$
![[Pasted image 20251223231756.png]]
Differentiating $\cos \theta = \langle N, n \rangle$ by $s$ yields:
$$
-\sin\theta \cdot\dfrac{d}{ds}\theta=\left< \dfrac{dN}{ds} ,n \right> +\left< N, -kt-\tau B\right> = \left< \dfrac{dN}{ds} ,n \right>-\tau \left< N,B \right> 
$$
Substituting by $(\dagger)$ gives
$$
-\sin\theta \cdot\dfrac{d}{ds}\theta=\left< \dfrac{dN}{ds} , \cos \theta \cdot N+\sin\theta \cdot h\right>-\tau \left< N,\sin\theta \cdot N-\cos\theta \cdot h \right>
=\sin\theta\left\langle \frac{dN}{ds}, h \right\rangle-\sin\theta \cdot\tau
$$
By definition we know $\left\langle \frac{dN}{ds}(0), h \right\rangle=\tau_{g}$, therefore,
$$
-\sin\theta \cdot\dfrac{d}{ds}\theta=\sin\theta \cdot(\tau_{g}-\tau)
$$
This proves the conclusion.

**c.**
A curve is a line of curvature if and only if its tangent direction is everywhere a principal direction. From **a.** we know $\tau_g = (k_1 - k_2) \cos\varphi \sin\varphi$. For a line of curvature, the tangent direction is always along a principal direction, so $\varphi = 0$ or $\pi/2$ modulo $\pi$. Then $\cos\varphi \sin\varphi = 0$, so $\tau_g = 0$ identically. Conversely, if $\tau_g = 0$ identically, then $(k_1 - k_2) \cos\varphi \sin\varphi = 0$. At non-umbilic points ($k_1 \neq k_2$), this implies $\cos\varphi \sin\varphi = 0$, so $\varphi = 0$ or $\pi/2$ modulo $\pi$, meaning the tangent is always along a principal direction, hence a line of curvature. At umbilic points, all directions are principal, so the curve is trivially a line of curvature. Thus, lines of curvature are exactly curves with $\tau_g \equiv 0$. 
___

>[!problem] Problem 6
>Show that at the origin $(0,0,0)$ of the hyperboloid $z=axy$ we have $K=-a^2$ and $H=0$.

**Proof:**
Let the surface be given by $\mathbf{r}(x,y) = (x, y, a x y)$.

Compute the first fundamental form coefficients:
$$
\mathbf{r}_x = (1, 0, a y),\quad \mathbf{r}_y = (0, 1, a x),
$$
$$
E = \mathbf{r}_x \cdot \mathbf{r}_x = 1 + a^2 y^2,\quad F = \mathbf{r}_x \cdot \mathbf{r}_y = a^2 x y,\quad G = \mathbf{r}_y \cdot \mathbf{r}_y = 1 + a^2 x^2.
$$

At the origin $(0,0,0)$: $E = 1,F = 0,G = 1$.

Compute the unit normal vector $\mathbf{N}$:
$$
\mathbf{r}_x \times \mathbf{r}_y = (-a y, -a x, 1),\quad \|\mathbf{r}_x \times \mathbf{r}_y\| = \sqrt{a^2 y^2 + a^2 x^2 + 1}
$$
At $(0,0,0)$: $\mathbf{N} = (0, 0, 1)$.

Compute the second fundamental form coefficients:
$$
\mathbf{r}_{xx} = (0, 0, 0),\quad \mathbf{r}_{xy} = (0, 0, a),\quad \mathbf{r}_{yy} = (0, 0, 0),
$$
$$
L = \mathbf{N} \cdot \mathbf{r}_{xx} = 0,\quad M = \mathbf{N} \cdot \mathbf{r}_{xy} = a\quad N = \mathbf{N} \cdot \mathbf{r}_{yy} = 0
$$

At $(0,0,0)$: $L = 0, M = a, N = 0$.

Compute $K$ and $H$ at the origin:
$$
K = \frac{LN - M^2}{EG - F^2} = \frac{0 \cdot 0 - a^2}{1 \cdot 1 - 0} = -a^2,
$$
$$
H = \frac{1}{2} \frac{EN - 2FM + GL}{EG - F^2} = \frac{1}{2} \frac{1 \cdot 0 - 2 \cdot 0 \cdot a + 1 \cdot 0}{1} = 0.
$$
Therefore, at the origin $(0,0,0)$ of the hyperboloid $z=axy$ we have $K=-a^2$ and $H=0$.
___

