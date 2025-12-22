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
