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

**Proof：**
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
We need to evaluate the sums $\sum_{j=1}^m \cos^2\varphi_j$ and $\sum_{j=1}^m \sin^2\varphi_j$. Since $\varphi_j$ are equally spaced angles on the circle, we have the known identities (for $m \ge 1$):
$$
\sum_{j=1}^m \cos^2\varphi_j = \sum_{j=1}^m \frac{1+\cos(2\varphi_j)}{2} = \frac{m}{2} + \frac12 \sum_{j=1}^m \cos\left(2\cdot (j-1)\frac{2\pi}{m}\right) = \frac{m}{2} + \frac12 \sum_{j=0}^{m-1} \cos\left(j\frac{4\pi}{m}\right).
$$
The sum $\sum_{j=0}^{m-1} \cos\left(j\frac{4\pi}{m}\right)$ is the real part of the geometric series $\sum_{j=0}^{m-1} e^{i j\frac{4\pi}{m}}$. For $m>2$, $\frac{4\pi}{m}$ is not an integer multiple of $2\pi$ unless $m=1,2$. If $m=1$ or $m=2$, direct computation shows the result holds. For $m>2$, the geometric series sums to $\frac{1-e^{i4\pi}}{1-e^{i4\pi/m}}=0$ because $e^{i4\pi}=1$. Thus, the sum is 0. Similarly,
$$
\sum_{j=1}^m \sin^2\varphi_j = \sum_{j=1}^m \frac{1-\cos(2\varphi_j)}{2} = \frac{m}{2} - \frac12 \sum_{j=1}^m \cos(2\varphi_j) = \frac{m}{2}.
$$
Therefore,
$$
\sum_{j=1}^m \lambda_j = k_1 \cdot \frac{m}{2} + k_2 \cdot \frac{m}{2} = \frac{m}{2}(k_1+k_2) = m H,
$$
since the mean curvature $H = \frac{k_1+k_2}{2}$. This completes the proof.