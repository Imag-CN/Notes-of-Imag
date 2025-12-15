___

>[!problem] [GAM01] III.1.5
> Show that $\int_{\partial D}x\,dy$ is the area of $D$, while $\int_{\partial D}y\,dx$ is minus the area of $D$.

**Proof:**
Let $D$ be a region in the plane with piecewise smooth boundary $\partial D$.
Using Green's Theorem:
$$
\iint_D \left( \frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} \right) dA = \oint_{\partial D} P\,dx + Q\,dy
$$

1.  For the first integral, set $P = 0$ and $Q = x$. Then:
$$
\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} = 1
$$
$$
\oint_{\partial D} x\,dy = \iint_D 1\,dA = \text{Area}(D)
$$
2.  For the second integral, set $P = -y$ and $Q = 0$. Then:
$$
\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y}  = 1
$$
$$
\oint_{\partial D} (-y)\,dx = \iint_D 1\,dA = \text{Area}(D)
$$
Therefore:
$$
\oint_{\partial D} y\,dx = -\text{Area}(D)
$$

This completes the proof.
___

> [!problem] [GAM01] III.2.3
> Suppose that $P$ and $Q$ are smooth functions on the annulus $\{a < |z| < b\}$ that satisfy $\partial P/\partial y = \partial Q/\partial x$. Show directly using Green's theorem that $\oint_{|z|=r} P\,dx + Q\,dy$ is independent of the radius $r$, for $a < r < b$.

**Proof:**
Let $a < r_1 < r_2 < b$. Consider the closed curve $\Gamma$ which is the boundary of the annular region $D = \{r_1 < |z| < r_2\}$, oriented positively. This boundary consists of two circles:
- The outer circle $C_2: |z| = r_2$, traversed counterclockwise.
- The inner circle $C_1: |z| = r_1$, traversed clockwise.

Thus, $\Gamma = C_2 + (-C_1)$, and we have:
$$
\oint_{\Gamma} P\,dx + Q\,dy = \oint_{C_2} P\,dx + Q\,dy - \oint_{C_1} P\,dx + Q\,dy
$$

Now, apply Green's Theorem to the region $D$ and the vector field $(P, Q)$. Since $P$ and $Q$ are smooth on the annulus (which contains the closure of $D$), and since $\partial P/\partial y = \partial Q/\partial x$ holds on $D$, we get:
$$
\oint_{\Gamma} P\,dx + Q\,dy = \iint_{D} \left( \frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} \right) dA = \iint_{D} 0 \, dA = 0
$$

Therefore,
$$
\oint_{C_2} P\,dx + Q\,dy - \oint_{C_1} P\,dx + Q\,dy = 0
$$
which implies
$$
\oint_{|z|=r_2} P\,dx + Q\,dy = \oint_{|z|=r_1} P\,dx + Q\,dy
$$

Since $r_1$ and $r_2$ were arbitrary radii in $(a, b)$, the value of the integral $\oint_{|z|=r} P\,dx + Q\,dy$ is independent of $r$.
___

> [!problem] [GAM01] III.3.4
> Let $u(z)$ be harmonic on the annulus $\{a<|z|<b\}$. Show that there is a constant $C$ such that $u(z)-C\log|z|$ has a harmonic conjugate on the annulus. Show that $C$ is given by
> $$C=\frac{r}{2\pi}\int_{0}^{2\pi}\frac{\partial u}{\partial r}\left(re^{i\theta}\right)d\theta,$$
> where $r$ is any fixed radius, $a < r < b$.

**Proof:**
A function has a harmonic conjugate on a domain if and only if its integral around any closed curve is zero. By CIT, it's sufficient to check this condition for the circle $|z| = r$.

Let $\gamma_r$ denote the circle $|z| = r$ traversed counterclockwise. For $u(z) - C\log|z|$ to have a harmonic conjugate, the necessary and sufficient condition is:
$$
\oint_{\gamma_r} \frac{\partial}{\partial n}(u - C\log|z|) \, ds = 0
$$
where $\frac{\partial}{\partial n}$ is the outward normal derivative. On the circle $|z|=r$, the outward normal derivative is $\frac{\partial}{\partial r}$, and $ds = r d\theta$. Thus, the condition becomes:
$$
\oint_{\gamma_r} \frac{\partial u}{\partial r} \, ds - C \oint_{\gamma_r} \frac{\partial}{\partial r}(\log r) \, ds = 0
$$
Since $\frac{\partial}{\partial r}(\log r) = \frac{1}{r}$, and $ds = r d\theta$, the second integral is:
$$
C \oint_{\gamma_r} \frac{1}{r} \cdot r d\theta = C \int_0^{2\pi} d\theta = 2\pi C
$$
The first integral is:
$$
\oint_{\gamma_r} \frac{\partial u}{\partial r} \, ds = \int_0^{2\pi} \frac{\partial u}{\partial r}(re^{i\theta}) \, r d\theta
$$
So the condition becomes:
$$
\int_0^{2\pi} \frac{\partial u}{\partial r}(re^{i\theta}) \, r d\theta - 2\pi C = 0
$$
Solving for $C$ gives:
$$
C = \frac{1}{2\pi} \int_0^{2\pi} \frac{\partial u}{\partial r}(re^{i\theta}) \, r d\theta = \frac{r}{2\pi} \int_0^{2\pi} \frac{\partial u}{\partial r}(re^{i\theta}) \, d\theta
$$
This value of $C$ is independent of $r$ because the integral $\oint_{\gamma_r} \frac{\partial u}{\partial n} ds$ is independent of $r$ for a harmonic function $u$ on an annulus (a consequence of Green's theorem). Therefore, with this choice of $C$, the function $u(z) - C\log|z|$ has a harmonic conjugate on the annulus.
___

> [!problem] [GAM01] IV.1.1
> Let $\gamma$ be the boundary of the triangle $\{0 < y < 1 - x, 0 < x < 1\}$, with the usual counterclockwise orientation. Evaluate the following integral:
> $$\int_{\gamma} z \, dz$$

**Solution**:
By CIT, the integral is $0$.
___

> [!problem] [GAM01] IV.1.2
> Let $\gamma$ be the unit circle $\{|z|=1\}$, with the usual counterclockwise orientation. Evaluate the following integrals, for $m = 0, \pm1, \pm2, \ldots$
>
> (a) $\int_{\gamma} z^{m}  dz$
>
> (b) $\int_{\gamma} \bar{z}^{m}  dz$
>
> (c) $\int_{\gamma} z^{m}  |dz|$

**Solution:**
Parameterize $\gamma$ by $z = e^{i\theta}$, $0 \leq \theta \leq 2\pi$. Then $dz = i e^{i\theta} d\theta$ and $|dz| = d\theta$.

**(a)**$$\int_{\gamma} z^{m}  dz = \int_0^{2\pi} (e^{i\theta})^{m} \cdot i e^{i\theta} d\theta = i \int_0^{2\pi} e^{i(m+1)\theta} d\theta$$
- If $m = -1$: $i \int_0^{2\pi} e^{0} d\theta = i \cdot 2\pi = 2\pi i$
- If $m \neq -1$: $i \int_0^{2\pi} e^{i(m+1)\theta} d\theta = i \cdot 0 = 0$

**(b)** On $\gamma$, $\bar{z} = e^{-i\theta}$, so $\bar{z}^{m} = e^{-im\theta}$.
$$\int_{\gamma} \bar{z}^{m}  dz = \int_0^{2\pi} e^{-im\theta} \cdot i e^{i\theta} d\theta = i \int_0^{2\pi} e^{i(1-m)\theta} d\theta$$

- If $m = 1$: $i \int_0^{2\pi} e^{0} d\theta = i \cdot 2\pi = 2\pi i$
- If $m \neq 1$: $i \int_0^{2\pi} e^{i(1-m)\theta} d\theta = i \cdot 0 = 0$

**(c)** $$\int_{\gamma} z^{m}  |dz| = \int_0^{2\pi} (e^{i\theta})^{m} \cdot d\theta = \int_0^{2\pi} e^{im\theta} d\theta$$

- If $m = 0$: $\int_0^{2\pi} e^{0} d\theta = 2\pi$
- If $m \neq 0$: $\int_0^{2\pi} e^{im\theta} d\theta = 0$
___

> [!problem] [GAM01] IV.1.4
> Show that if $D$ is a bounded domain with smooth boundary, then
> $$\int_{\partial D} \bar{z} d z=2 i  \operatorname{Area}(D)$$

**Proof:**

Let $z = x + iy$, so $\bar{z} = x - iy$ and $dz = dx + i dy$. Then:
$$
\bar{z}  dz = (x - iy)(dx + i dy) = x dx + y dy + i(x dy - y dx)
$$
Thus:
$$
\int_{\partial D} \bar{z}  dz = \int_{\partial D} (x dx + y dy) + i \int_{\partial D} (x dy - y dx)
$$

The first integral is zero (it's the integral of an exact differential over a closed path).

Apply Green's Theorem to the second integral:
$$
\int_{\partial D} (x dy - y dx) = \iint_{D} \left( \frac{\partial x}{\partial x} - \frac{\partial (-y)}{\partial y} \right) dA = \iint_{D} (1 + 1) dA = 2 \operatorname{Area}(D)
$$

Therefore:
$$
\int_{\partial D} \bar{z}  dz = 0 + i \cdot 2 \operatorname{Area}(D) = 2i \operatorname{Area}(D)
$$
___

> [!problem] [GAM01] IV.1.6
> Show that
> $$\left|\oint_{|z|=R}\frac{\log z}{z^{2}}dz\right|\leq 2\sqrt{2}\pi\frac{\log R}{R},\quad R>e^{\pi}.$$

**Proof:**

Parameterize $|z|=R$ by $z=Re^{i\theta}$, $-\pi\leq\theta\leq\pi$. Then $dz=iRe^{i\theta}d\theta$ and $|dz|=Rd\theta$.

On the contour, $|\log z|=\sqrt{(\log R)^2+\theta^2}$. By the ML-inequality:
$$\left|\oint\frac{\log z}{z^2}dz\right|\leq \max_{|z|=R}\left|\frac{\log z}{z^2}\right|\cdot(2\pi R)=\frac{\max|\log z|}{R^2}\cdot 2\pi R=\frac{2\pi}{R}\max|\log z|$$

Since $|\log z|=\sqrt{(\log R)^2+\theta^2}\leq\sqrt{(\log R)^2+\pi^2}$, and for $R>e^{\pi}$ we have $\log R>\pi$, so:
$$\sqrt{(\log R)^2+\pi^2}\leq\sqrt{2(\log R)^2}=\sqrt{2}\log R$$

Therefore:
$$\left|\oint\frac{\log z}{z^2}dz\right|\leq\frac{2\pi}{R}\cdot\sqrt{2}\log R=2\sqrt{2}\pi\frac{\log R}{R}$$
___

> [!problem] [GAM01] IV.2.4
> Let $D = \mathbb{C} \setminus (-\infty, 1]$, and consider the branch of $\sqrt{z^{2}-1}$ on $D$ that is positive on the interval $(1, \infty)$.
>
> (a) Show that $z + \sqrt{z^{2}-1}$ omits the negative real axis, that is, the range of the function on $D$ does not include any values in the interval $(-\infty, 0]$ on the real axis.
>
> (b) Show that $\log (z + \sqrt{z^{2}-1})$ is a primitive for $1/\sqrt{z^{2}-1}$ on $D$.
>
> (c) Evaluate
> $$\int_{\gamma} \frac{dz}{\sqrt{z^{2}-1}}$$
> where $\gamma$ is the path from $-2i$ to $+2i$ in $D$ counterclockwise around the circle $|z| = 2$.
>
> (d) Evaluate the integral above in the case $\gamma$ is the entire circle $|z| = 2$, oriented counterclockwise. (Note that the primitive is discontinuous at $z = -2$.)

**Solution:**

**(a)** Let $w = z + \sqrt{z^2-1}$. Suppose $w \leq 0$ is real. Then $\sqrt{z^2-1} = w - z$ is real. Squaring gives $z^2-1 = w^2 - 2wz + z^2$, so $-1 = w^2 - 2wz$, hence $z = \frac{w^2+1}{2w}$. For $w \leq 0$, this $z$ is real and $\leq \frac{1}{2w}(w^2+1) \leq 0$ (since $w<0$ gives negative denominator). But $D$ excludes $(-\infty,1]$, so $z$ would be in $D$ only if $z > 1$. Contradiction. Thus $w$ cannot be negative real.

**(b)** Differentiate:
$$\frac{d}{dz}\log(z+\sqrt{z^2-1}) = \frac{1+\frac{z}{\sqrt{z^2-1}}}{z+\sqrt{z^2-1}} = \frac{\frac{\sqrt{z^2-1}+z}{\sqrt{z^2-1}}}{z+\sqrt{z^2-1}} = \frac{1}{\sqrt{z^2-1}}$$

**(c)** Since $\gamma$ starts at $-2i$ and ends at $+2i$ in $D$, and the primitive is analytic along this path:
$$\int_{\gamma} \frac{dz}{\sqrt{z^2-1}} = \log(z+\sqrt{z^2-1})\Big|_{-2i}^{2i}$$

Compute endpoints:
- At $z=2i$: $z+\sqrt{z^2-1} = 2i+\sqrt{-4-1} = 2i+\sqrt{-5} = 2i \pm i\sqrt{5}$
- At $z=-2i$: $z+\sqrt{z^2-1} = -2i+\sqrt{-4-1} = -2i+\sqrt{-5} = -2i \pm i\sqrt{5}$

Using the branch that is positive on $(1,\infty)$, we get:
$$\int_{\gamma} \frac{dz}{\sqrt{z^2-1}} =  \log(2i + i\sqrt{5}) - \log(-2i + i\sqrt{5}) = 2\log(2+\sqrt{5})$$

**(d)** For the closed circle $|z|=2$, the primitive $\log(z+\sqrt{z^2-1})$ is discontinuous at $z=-2$. The jump discontinuity is $2\pi i$ (due to branch cut crossing). Thus:
$$\oint_{|z|=2} \frac{dz}{\sqrt{z^2-1}} = 2\pi i$$
___

> [!problem] [GAM01] IV.2.5
> Show that an analytic function $f(z)$ has a primitive in $D$ if and only if $\int_{\gamma}f(z)dz=0$ for every closed path $\gamma$ in $D$.

**Proof:**

**($\Rightarrow$) Suppose $f$ has a primitive $F$ in $D$:**  
Since $F$ is analytic in $D$ with $F' = f$, and $D$ is a domain, for any closed path $\gamma$ in $D$:
$$\int_{\gamma} f(z)dz = \int_{\gamma} F'(z)dz = 0$$
by the fundamental theorem of calculus for analytic functions.

**($\Leftarrow$) Suppose $\int_{\gamma}f(z)dz=0$ for every closed path $\gamma$ in $D$:**  
Fix $z_0 \in D$. For any $z \in D$, define:
$$F(z) = \int_{\gamma_z} f(w)dw$$
where $\gamma_z$ is any path in $D$ from $z_0$ to $z$. This is well-defined because if $\gamma_z'$ is another such path, then $\gamma_z - \gamma_z'$ is a closed path, so:
$$\int_{\gamma_z} f(w)dw - \int_{\gamma_z'} f(w)dw = \int_{\gamma_z - \gamma_z'} f(w)dw = 0$$

To show $F'(z) = f(z)$, fix $z \in D$ and take $h$ small enough that the disk $B(z,|h|) \subset D$. Then:
$$F(z+h) - F(z) = \int_{z}^{z+h} f(w)dw$$
where the integral is along the straight line segment. Parameterize $w = z + th$, $0 \leq t \leq 1$:
$$F(z+h) - F(z) = h\int_0^1 f(z+th)dt$$

Since $f$ is continuous:
$$\frac{F(z+h) - F(z)}{h} = \int_0^1 f(z+th)dt \to f(z) \quad \text{as } h \to 0$$
Thus $F'(z) = f(z)$, so $F$ is a primitive of $f$ in $D$.
___

> [!problem] [GAM01] IV.3.1
> By integrating $e^{-z^{2}/2}$ around a rectangle with vertices $\pm R$, $i\pm R$, and sending $R$ to $\infty$, show that
> $$\frac{1}{\sqrt{2\pi}}\int_{-\infty}^{\infty}e^{-x^{2}/2}e^{-itx}dx=e^{-t^{2}/2},\quad -\infty<t<\infty.$$
> Use the known value of the integral for $t=0$.

**Proof:**

Let $\Gamma_R$ be the rectangle with vertices $-R$, $R$, $R+it$, $-R+it$, oriented counterclockwise. The function $f(z) = e^{-z^2/2}$ is entire (analytic everywhere), so by Cauchy's theorem:
$$\oint_{\Gamma_R} e^{-z^2/2}dz = 0$$

Decompose the integral into four segments:
1. **Bottom:** $z = x$, $-R \leq x \leq R$, $dz = dx$
   $$I_1 = \int_{-R}^{R} e^{-x^2/2}dx$$
2. **Right:** $z = R + iy$, $0 \leq y \leq t$, $dz = i dy$
   $$I_2 = \int_0^t e^{-(R+iy)^2/2}i dy = i\int_0^t e^{-(R^2 + 2iRy - y^2)/2}dy = ie^{-R^2/2}\int_0^t e^{y^2/2}e^{-iRy}dy$$
3. **Top:** $z = x + it$, $R \geq x \geq -R$, $dz = dx$
   $$I_3 = \int_{R}^{-R} e^{-(x+it)^2/2}dx = -\int_{-R}^{R} e^{-(x^2 + 2itx - t^2)/2}dx = -e^{t^2/2}\int_{-R}^{R} e^{-x^2/2}e^{-itx}dx$$
4. **Left:** $z = -R + iy$, $t \geq y \geq 0$, $dz = i dy$
   $$I_4 = \int_t^0 e^{-(-R+iy)^2/2}i dy = -i\int_0^t e^{-(R^2 - 2iRy - y^2)/2}dy = -ie^{-R^2/2}\int_0^t e^{y^2/2}e^{iRy}dy$$

As $R \to \infty$, $I_2$ and $I_4$ vanish because:
$$|I_2|, |I_4| \leq e^{-R^2/2}\int_0^t e^{y^2/2}dy \to 0$$

Thus, taking $R \to \infty$:
$$I_1 + I_3 = 0 \Rightarrow \int_{-\infty}^{\infty} e^{-x^2/2}dx - e^{t^2/2}\int_{-\infty}^{\infty} e^{-x^2/2}e^{-itx}dx = 0$$

Using the known value for $t=0$:
$$\int_{-\infty}^{\infty} e^{-x^2/2}dx = \sqrt{2\pi}$$

Therefore:
$$e^{t^2/2}\int_{-\infty}^{\infty} e^{-x^2/2}e^{-itx}dx = \sqrt{2\pi}$$
$$\Rightarrow \frac{1}{\sqrt{2\pi}}\int_{-\infty}^{\infty} e^{-x^2/2}e^{-itx}dx = e^{-t^2/2}$$
>[!tip] Remark
>This shows that $e^{-x^{2}/2}$ is an eigenfunction of the Fourier transform with eigenvalue $1$.

___

> [!problem] [GAM01]IV.3.6
> Suppose $f(z)$ is continuous in the closed disk $\{|z|\leq R\}$ and analytic on the open disk $\{|z|<R\}$. Show that $\oint_{|z|=R}f(z)dz=0$.

**Proof:**

For $0 < r < 1$, define $f_r(z) = f(rz)$. Since $f$ is analytic on $\{|z| < R\}$, the function $f_r(z)$ is analytic on the larger disk $\{|z| < R/r\}$, which contains the closed disk $\{|z| \leq R\}$.

By Cauchy's theorem for analytic functions on simply connected domains:
$$
\oint_{|z|=R} f_r(z)  dz = 0 \quad \text{for all } 0 < r < 1
$$

Now, since $f$ is continuous on the compact set $\{|z| \leq R\}$, it is uniformly continuous there. Therefore, as $r \to 1^-$, we have:
$$
f_r(z) = f(rz) \to f(z) \quad \text{uniformly on } \{|z| = R\}
$$

Since uniform convergence allows us to interchange limit and integration:
$$
\oint_{|z|=R} f(z)  dz = \oint_{|z|=R} \lim_{r \to 1^-} f_r(z)  dz = \lim_{r \to 1^-} \oint_{|z|=R} f_r(z)  dz = \lim_{r \to 1^-} 0 = 0
$$

This completes the proof.
___
> [!problem]
> Let $f(x)=u(x)+iv(x):[a,b]\to\mathbb{C}$ be a continuous complex-valued function. Define
> $$\int_{a}^{b}f(x)dx:=\int_{a}^{b}u(x)dx+i\int_{a}^{b}v(x)dx.
> $$
> Verify that 
> $$
> \int_{a}^{b}\lambda f(x)dx=\lambda\int_{a}^{b}f(x)dx\quad\text{for any}\quad\lambda\in\mathbb{C}.
> $$

**Solution:**
Let $\lambda = \alpha + i\beta$ where $\alpha, \beta \in \mathbb{R}$. Then:
- $\lambda f(x) = (\alpha + i\beta)(u(x) + iv(x)) = (\alpha u(x) - \beta v(x)) + i(\alpha v(x) + \beta u(x))$

By definition:
$$
\int_{a}^{b}\lambda f(x)dx = \int_{a}^{b}[(\alpha u(x) - \beta v(x)) + i(\alpha v(x) + \beta u(x))]dx
$$
$$
= \int_{a}^{b}(\alpha u(x) - \beta v(x))dx + i\int_{a}^{b}(\alpha v(x) + \beta u(x))dx
$$

On the other hand:
$$
\lambda\int_{a}^{b}f(x)dx = (\alpha + i\beta)\left[\int_{a}^{b}u(x)dx + i\int_{a}^{b}v(x)dx\right]
$$
$$
= \alpha\int_{a}^{b}u(x)dx + i\alpha\int_{a}^{b}v(x)dx + i\beta\int_{a}^{b}u(x)dx + i^2\beta\int_{a}^{b}v(x)dx
$$
$$
= \left(\alpha\int_{a}^{b}u(x)dx - \beta\int_{a}^{b}v(x)dx\right) + i\left(\alpha\int_{a}^{b}v(x)dx + \beta\int_{a}^{b}u(x)dx\right)
$$

Since integration is linear for real-valued functions, the two expressions are equal.
___

> [!problem]
> Let $\mathbb{H}:=\{z\in\mathbb{C}\mid\operatorname{Im}(z)>0\}$ be the upper half plane, and let $\mathbb{D}:=\{z\in\mathbb{C}\mid|z|<1\}$ be the unit disk. Show that
> $$f(z)=\frac{z-i}{z+i}$$
> provides a bijective conformal map from $\mathbb{H}$ onto $\mathbb{D}$.

**Proof:**

**(1)** $f(\mathbb{H}) \subset \mathbb{D}$:
For $z \in \mathbb{H}$ (so $\operatorname{Im}(z) > 0$), compute:
$$
|f(z)|^2 = \left|\frac{z-i}{z+i}\right|^2 = \frac{|z-i|^2}{|z+i|^2} = \frac{(x)^2 + (y-1)^2}{(x)^2 + (y+1)^2}
$$
Since $y > 0$, we have $(y-1)^2 < (y+1)^2$, so $|f(z)|^2 < 1$, hence $|f(z)| < 1$.

**(2)** $f$ is bijective:
- **Injective**: Suppose $f(z_1) = f(z_2)$. Then:
  $$
  \frac{z_1-i}{z_1+i} = \frac{z_2-i}{z_2+i} \Rightarrow (z_1-i)(z_2+i) = (z_2-i)(z_1+i)
  $$
  Simplifying gives $2i(z_1 - z_2) = 0$, so $z_1 = z_2$.

- **Surjective**: For any $w \in \mathbb{D}$, solve $f(z) = w$:
  $$
  \frac{z-i}{z+i} = w \Rightarrow z-i = w(z+i) \Rightarrow z(1-w) = i(1+w)
  $$
  $$
  \Rightarrow z = i\frac{1+w}{1-w}
  $$
  Check that $z \in \mathbb{H}$: Let $w = u+iv$, then:
  $$
  \operatorname{Im}(z) = \operatorname{Im}\left(i\frac{1+w}{1-w}\right) = \operatorname{Re}\left(\frac{1+w}{1-w}\right)
  $$
  Since $|w| < 1$, we have $\operatorname{Re}\left(\frac{1+w}{1-w}\right) > 0$.

**(3)** $f$ is conformal:
$f$ is a rational function, hence analytic on $\mathbb{C}\setminus\{-i\}$. Since $-i \notin \mathbb{H}$, $f$ is analytic on $\mathbb{H}$. Also, $f'(z) = \frac{2i}{(z+i)^2} \neq 0$ for all $z \in \mathbb{H}$. Therefore, $f$ is conformal on $\mathbb{H}$.

Thus, $f$ is a bijective conformal map from $\mathbb{H}$ onto $\mathbb{D}$.
___

> [!problem]
> Let $f(z)$ be an analytic function on a star-shaped domain $D$. Suppose that $f'(z)$ is analytic and $f(z)\neq 0$ for all $z\in D$.
>
> (a) Show that there exists an analytic function $g(z)$ on $D$ such that $f(z)=e^{g(z)}$; such a $g(z)$ is called an analytic branch of the logarithm of $f(z)$ on $D$.
>
> (b) Let $n$ be a positive integer. Prove that there exists an analytic function $h(z)$ on $D$ such that $h(z)^{n}=f(z)$.

**Proof:**
**(a)** Since $D$ is star-shaped and $f(z) \neq 0$ on $D$, the function $\frac{f'(z)}{f(z)}$ is analytic on $D$. By the existence of primitives on star-shaped domains, there exists an analytic function $G(z)$ on $D$ such that:
$$G'(z) = \frac{f'(z)}{f(z)}$$

Define $g(z) = G(z) - c$, where $c$ is a constant to be determined. Consider the function:
$$\phi(z) = f(z)e^{-g(z)}$$

Differentiate:
$$\phi'(z) = f'(z)e^{-g(z)} - f(z)e^{-g(z)}g'(z) = e^{-g(z)}[f'(z) - f(z)g'(z)]$$

Since $g'(z) = G'(z) = \frac{f'(z)}{f(z)}$, we have:
$$\phi'(z) = e^{-g(z)}[f'(z) - f(z)\cdot\frac{f'(z)}{f(z)}] = 0$$

Thus $\phi(z)$ is constant on $D$. Let $\phi(z) = k$ for all $z \in D$, so:
$$f(z) = ke^{g(z)}$$

Now choose $c$ such that $k = 1$. Since $f(z_0) \neq 0$ for some $z_0 \in D$, we can take:
$$c = \log f(z_0) - G(z_0)$$
where the logarithm is chosen appropriately. Then:
$$f(z_0) = ke^{G(z_0)-c} = ke^{G(z_0)-[\log f(z_0)-G(z_0)]} = ke^{2G(z_0)-\log f(z_0)} = k\frac{e^{2G(z_0)}}{f(z_0)}$$

This gives $k = 1$, so $f(z) = e^{g(z)}$.

**(b)** By part (a), there exists an analytic function $g(z)$ on $D$ such that $f(z) = e^{g(z)}$. Define:
$$h(z) = e^{g(z)/n}$$

Then $h(z)$ is analytic on $D$ (as composition of analytic functions), and:
$$h(z)^n = [e^{g(z)/n}]^n = e^{g(z)} = f(z)$$

This completes the proof.