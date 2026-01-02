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

