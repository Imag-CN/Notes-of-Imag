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

Since $\gamma$ is asymptotic, $\mathbf{n} \cdot \mathbf{T}=0$. Differentiating gives $\mathbf{n}'\cdot \mathbf{T} + \mathbf{n} \cdot \mathbf{T}' = 0$. Since $\mathbf{n}'\cdot \mathbf{T}=0$ (asymptotic condition) and $\mathbf{T}'=\kappa \mathbf{N}$, we have $\kappa (\mathbf{n}\cdot \mathbf{N})=0$. Since $\kappa \ne 0$, we have $\mathbf{n} \cdot \mathbf{N}=0$. Hence $\mathbf{n}$ is orthogonal to both $\mathbf{T}$ and $\mathbf{N}$, so $\mathbf{n} \parallel \mathbf{B}$. Thus $\mathbf{n} = \pm \mathbf{B}$.

Differentiate $\mathbf{n} = \pm \mathbf{B}$ and use $\mathbf{B}' = \tau \mathbf{N}$, we get $\mathbf{n}' = \pm \tau \mathbf{N}$.

3. Also, $\mathbf{n}' = -S(\mathbf{T})$, where $S$ is the shape operator. In the orthonormal tangent basis $\{\mathbf{T}, \mathbf{N}\}$, write $S(\mathbf{T}) = a\mathbf{T} + b\mathbf{N}$.  
   Since $\gamma$ is asymptotic, $a = S(\mathbf{T})\cdot \mathbf{T} = II(\mathbf{T},\mathbf{T})=0$, so $S(\mathbf{T}) = b\mathbf{N}$.  
   The Gaussian curvature is $K = \det S = a d - b^2 = -b^2$ (using symmetry $b = S(\mathbf{T})\cdot \mathbf{N} = S(\mathbf{N})\cdot \mathbf{T}$). Thus $b^2 = -K$.

4. Hence $\mathbf{n}' = -b \mathbf{N}$. Comparing with step 2 gives $-b\mathbf{N} = \mp \tau \mathbf{N}$, i.e., $b = \pm \tau$.  
   Therefore $\tau^2 = b^2 = -K$, and taking square roots yields $|\tau| = \sqrt{-K}$.