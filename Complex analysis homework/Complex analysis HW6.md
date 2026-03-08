___

> [!problem] [GAM] III.5.5
> Let $f(z)$ be a bounded analytic function on the right half-plane. Suppose that $f(z)$ extends continuously to the imaginary axis and satisfies $|f(iy)|\leq M$ for all points $iy$ on the imaginary axis. Show that $|f(z)|\leq M$ for all $z$ in the right half-plane.

**Proof:**

For $\varepsilon>0$, define $g_\varepsilon(z) = (z+1)^{-\varepsilon}f(z)$ on $\{z: \operatorname{Re}(z) \ge 0\}$.

On the imaginary axis $z=iy$: $|z+1| \ge 1 \Rightarrow |g_\varepsilon(iy)| \le |f(iy)| \le M$.

On the semidisk $\Omega_R = \{z: \operatorname{Re}(z) \ge 0, |z| \le R\}$, for large $R$:
- On $|z|=R$: $|g_\varepsilon(z)| =O( R^{-\varepsilon}|f(z)|) \to 0$ as $R \to \infty$ (since $f$ is bounded)
- By maximum modulus principle: $|g_\varepsilon(z)| \le M$ on $\Omega_R$

Letting $R \to \infty$: $|g_\varepsilon(z)| \le M$ for all $\operatorname{Re}(z) \ge 0$, so $|f(z)| \le M|z+1|^{\varepsilon}$.

Taking $\varepsilon \to 0^+$ gives $|f(z)| \le M$.
___

> [!problem] [GAM] IV.4.1
> (b) $$ \oint_{|z|=1}\frac{z^n}{z-2}dz,\quad n\geq0 $$
> (c) $$ \oint_{|z|=1}\frac{\sin z}{z}dz $$
> (f) $$ \int_{|z-1-i|=5/4}\frac{\log z}{(z-1)^2}dz $$
> (g) $$ \oint_{|z|=1}\frac{dz}{z^2(z^2-4)e^z} $$

**Answer:**
**(b)**
The function $f(z) = z^n$ is analytic on and inside $|z|=1$. The singularity $z=2$ lies outside the path ($|2|>1$). By Cauchy's integral theorem, the integral equals $0$.
**(c)**
The function $f(z) = \sin z$ is entire (analytic everywhere). The singularity $z=0$ lies inside the path. By Cauchy's integral formula:
$$\oint_{|z|=1}\frac{\sin z}{z}dz = 2\pi i f(0) = 2\pi i \cdot \sin 0 = 0.$$
**(f)**
The path is a circle centered at $1+i$ with radius $1.25$. The singularity $z=1$ lies inside the path since $|(1+i)-1| = |i| = 1 < 1.25$. The function $f(z) = \log z$ is analytic on a domain containing the path (taking an appropriate branch). By the generalized Cauchy integral formula:
$$\oint \frac{\log z}{(z-1)^2}dz = 2\pi i \cdot f'(1) = 2\pi i \cdot \left.\frac{1}{z}\right|_{z=1} = 2\pi i.$$

**(g)**
The singularities inside $|z|=1$ are $z=0$ (order 2) and $z=0$ from $e^z$ (analytic). The singularities $z=\pm2$ lie outside ($|\pm2|>1$). Let $f(z) = \frac{1}{(z^2-4)e^z}$, which is analytic inside $|z|=1$. By the generalized Cauchy integral formula:
$$\oint_{|z|=1}\frac{dz}{z^2(z^2-4)e^z} = \frac{2\pi i}{1!} f'(0).$$
Compute $f'(z)$ using quotient rule or product rule: $f(z) = (z^2-4)^{-1}e^{-z}$, so
$$f'(z) = -2z(z^2-4)^{-2}e^{-z} - (z^2-4)^{-1}e^{-z} = -\frac{e^{-z}(2z + z^2 - 4)}{(z^2-4)^2}.$$
Then $f'(0) = -\frac{1\cdot(0 + 0 - 4)}{(-4)^2} = -\frac{-4}{16} = \frac{1}{4}$.
Thus the integral equals $2\pi i \cdot \frac{1}{4} = \frac{\pi i}{2}$.
___

> [!problem] [GAM] IV.4.2
> Show that a harmonic function is $C^{\infty}$, that is, a harmonic function has partial derivatives of all orders.

**Proof:**
Let $u$ be harmonic on a domain $\Omega\subset\mathbb{R}^2$. Locally, on a disk $D\subset\Omega$, $u$ is the real part of an analytic function $f$. Since $f$ is analytic, it is $C^{\infty}$. Therefore, $u=\operatorname{Re}f$ is also $C^{\infty}$.
___

> [!problem] [GAM] IV.5.1
> Show that if $u$ is a harmonic function on $\mathbb{C}$ that is bounded above, then $u$ is constant.

**Proof:**
Since $u$ is harmonic on $\mathbb{C}$, there exists an analytic function $f(z)$ such that $u = \operatorname{Re} f$. Consider $g(z) = e^{f(z)}$. Then $|g(z)| = e^{u(z)}$ is bounded since $u$ is bounded above. By Liouville's theorem, $g(z)$ is constant, so $f(z)$ is constant, hence $u$ is constant.
___

> [!problem] [GAM] IV.5.2
> Show that if $f(z)$ is an entire function, and there is a nonempty disk such that $f(z)$ does not attain any values in the disk, then $f(z)$ is constant.

**Proof:**
Suppose $f(z)$ avoids a disk $D(w_0, r)$. Then $g(z) = \frac{1}{f(z)-w_0}$ is entire and bounded by $1/r$. By Liouville's theorem, $g(z)$ is constant, so $f(z)$ is constant.
___

> [!problem] [GAM] IV.5.3
> A function $f(z)$ on the complex plane is doubly periodic if there are two periods $\omega_0$ and $\omega_1$ of $f(z)$ that do not lie on the same line through the origin (that is, $\omega_0$ and $\omega_1$ are linearly independent over the reals, and $f(z+\omega_0)=f(z+\omega_1)=f(z)$ for all complex numbers $z$). Prove that the only entire functions that are doubly periodic are the constants.

**Proof:**
The periods generate a lattice $\Lambda = \{m\omega_0 + n\omega_1 : m,n\in\mathbb{Z}\}$. The function $f$ is bounded on the fundamental parallelogram $P$, which is compact. By periodicity, $f$ is bounded on $\mathbb{C}$. By Liouville's theorem, $f$ is constant.
___

> [!problem] [GAM] IV.5.4
> Suppose that $f(z)$ is an entire function such that $f(z)/z^n$ is bounded for $|z|\geq R$. Show that $f(z)$ is a polynomial of degree at most $n$. What can be said if $f(z)/z^n$ is bounded on the entire complex plane?

**Proof:**
Let $g(z) = f(z)/z^n$ for $z\neq 0$. The singularity at $0$ is removable, so $g$ is entire. For $|z|\geq R$, $|g(z)|\leq M$. By Liouville, $g$ is constant if bounded on $\mathbb{C}$. Thus $f(z) = cz^n$, a polynomial of degree $\leq n$. If bounded only for $|z|\geq R$, then $g$ is entire but not necessarily constant; however, $f(z)/z^n$ being entire and bounded at infinity implies $f$ is a polynomial of degree $\leq n$ by Cauchy's estimates.
___

> [!problem] [Sl] 3.2.3
> 设 $n$ 为正整数, 试通过计算积分
> $$ \oint_{|z|=1}\left(z+\frac{1}{z}\right)^n\frac{dz}{z} $$
> 证明
> $$ \int_{0}^{2\pi}\cos^{2n}\theta d\theta=2\pi\frac{(2n-1)!!}{(2n)!!}. $$

**证明:**

在单位圆周 $|z|=1$ 上, 令 $z = e^{i\theta}$, 则 $dz = ie^{i\theta}d\theta$, 且
$$z + \frac{1}{z} = e^{i\theta} + e^{-i\theta} = 2\cos\theta.$$

原复积分化为:
$$
\begin{aligned}
\oint_{|z|=1}\left(z+\frac{1}{z}\right)^n\frac{dz}{z} &= \int_0^{2\pi} (2\cos\theta)^n \cdot \frac{ie^{i\theta}d\theta}{e^{i\theta}} \\
&= i \cdot 2^n \int_0^{2\pi} \cos^n\theta  d\theta.
\end{aligned}
$$

另一方面, 被积函数可展开为:
$$
\left(z+\frac{1}{z}\right)^n\frac{1}{z} = \frac{1}{z}\sum_{k=0}^n \binom{n}{k} z^k z^{-(n-k)} = \sum_{k=0}^n \binom{n}{k} z^{2k-n-1}.
$$

在单位圆周上积分时, 仅 $z^{-1}$ 项有贡献, 即要求 $2k-n-1 = -1 \Rightarrow k = n/2$. 由于 $n$ 为正整数, 仅当 $n$ 为偶数时积分才非0. 设 $n=2m$, 则 $k=m$, 因此:
$$
\oint_{|z|=1}\left(z+\frac{1}{z}\right)^{2m}\frac{dz}{z} = 2\pi i \cdot \binom{2m}{m}.
$$

比较两种计算结果:
$$
i \cdot 2^{2m} \int_0^{2\pi} \cos^{2m}\theta  d\theta = 2\pi i \cdot \binom{2m}{m}.
$$

解得:
$$
\int_0^{2\pi} \cos^{2m}\theta  d\theta = 2\pi \cdot \frac{\binom{2m}{m}}{2^{2m}} = 2\pi \cdot \frac{(2m)!}{(m!)^2 2^{2m}}.
$$

利用恒等式 $\frac{(2m)!}{(m!)^2 2^{2m}} = \frac{(2m-1)!!}{(2m)!!}$, 即得所求.
___

> [!problem] [SL] 3.4.5
> 设 $f\in H(B(0,1))\cap C(\overline{B(0,1)})$ 证明:
> (1) $$\frac{2}{\pi}\int_{0}^{2\pi}f(e^{i\theta})\cos^{2}\left(\frac{\theta}{2}\right) d\theta=2f(0)+f^{\prime}(0)$$
> (2) $$\frac{2}{\pi}\int_{0}^{2\pi}f(e^{i\theta})\sin^{2}\left(\frac{\theta}{2}\right) d\theta=2f(0)-f^{\prime}(0)$$
> 提示: 分别计算积分
> $$ \frac{1}{2\pi i}\int_{|\zeta|=1}\left(2+\zeta+\frac{1}{\zeta}\right) f(\zeta)\frac{d\zeta}{\zeta} $$
> 和
> $$ \frac{1}{2\pi i}\int_{|\zeta|=1}\left(2-\zeta-\frac{1}{\zeta}\right) f(\zeta)\frac{d\zeta}{\zeta} $$
> 即可.

**证明:**

(1) 计算提示中的第一个积分. 在 $|\zeta|=1$ 上, $\zeta = e^{i\theta}$, 则:
$$\zeta + \frac{1}{\zeta} = e^{i\theta} + e^{-i\theta} = 2\cos\theta,$$
且由半角公式 $2\cos^2(\theta/2) = 1 + \cos\theta$, 得:
$$2 + \zeta + \frac{1}{\zeta} = 2 + 2\cos\theta = 4\cos^2(\theta/2).$$

由 Cauchy 积分公式:
$$\frac{1}{2\pi i}\int_{|\zeta|=1}\left(2+\zeta+\frac{1}{\zeta}\right)f(\zeta)\frac{d\zeta}{\zeta} = \frac{1}{2\pi}\int_0^{2\pi} 4\cos^2(\theta/2) f(e^{i\theta}) d\theta.$$

另一方面, 展开被积函数:
$$\left(2+\zeta+\frac{1}{\zeta}\right)\frac{f(\zeta)}{\zeta} = \frac{2f(\zeta)}{\zeta} + f(\zeta) + \frac{f(\zeta)}{\zeta^2}.$$

由 Cauchy 积分公式及高阶导数公式:
- $\frac{1}{2\pi i}\int \frac{2f(\zeta)}{\zeta} d\zeta = 2f(0)$
- $\frac{1}{2\pi i}\int f(\zeta) d\zeta = 0$ (被积函数解析)
- $\frac{1}{2\pi i}\int \frac{f(\zeta)}{\zeta^2} d\zeta = f'(0)$

所以积分值为 $2f(0) + f'(0)$. 比较得:
$$\frac{2}{\pi}\int_0^{2\pi} f(e^{i\theta})\cos^2(\theta/2) d\theta = 2f(0) + f'(0).$$

(2) 类似地, 计算第二个积分. 由 $2\sin^2(\theta/2) = 1 - \cos\theta$, 得:
$$2 - \zeta - \frac{1}{\zeta} = 2 - 2\cos\theta = 4\sin^2(\theta/2).$$

展开被积函数:
$$\left(2-\zeta-\frac{1}{\zeta}\right)\frac{f(\zeta)}{\zeta} = \frac{2f(\zeta)}{\zeta} - f(\zeta) - \frac{f(\zeta)}{\zeta^2}.$$

积分值为 $2f(0) - f'(0)$. 比较得第二式.

> [!problem] [SL] 3.4.6
> 利用上题结果证明: 设 $f\in H(B(0,1))\cap C(\overline{B(0,1)})$, 且 $f(0)=1$, $\mathrm{Re}f(z)\geqslant 0$, 那么 $-2\leqslant\mathrm{Re}f^{\prime}(0)\leqslant 2$.

**证明:**

由第5题结果, 两式相加得:
$$\frac{2}{\pi}\int_0^{2\pi} f(e^{i\theta}) d\theta = 4f(0) = 4.$$

两式相减得:
$$\frac{2}{\pi}\int_0^{2\pi} f(e^{i\theta})\cos\theta  d\theta = 2f'(0).$$

取实部, 并注意 $\mathrm{Re}f(e^{i\theta}) \geq 0$:
$$2\mathrm{Re}f'(0) = \frac{2}{\pi}\int_0^{2\pi} \mathrm{Re}f(e^{i\theta})\cos\theta  d\theta.$$

由于 $|\cos\theta| \leq 1$, 且由第一式知 $\frac{2}{\pi}\int_0^{2\pi} \mathrm{Re}f(e^{i\theta}) d\theta = 4$, 故:
$$|2\mathrm{Re}f'(0)| \leq \frac{2}{\pi}\int_0^{2\pi} \mathrm{Re}f(e^{i\theta}) d\theta = 4,$$
即 $|\mathrm{Re}f'(0)| \leq 2$, 得证. 
___

> [!problem]
> (4) Determine the maximum of $|f|$ on $\{z\in\mathbb{C}\mid|z|\leq1\}$ for the following $f$:
> (a) $f=e^{z^{2}}$;
> (b) $f=\frac{z+3}{z-3}$;
> (c) $f=3-|z|^{2}$.
> (In (c), the maximal modulus is taken at $z=0$; does this give a counterexample to the maximum principle?)

**Solution:**

**(a)** The function $f(z)=e^{z^2}$ is analytic on the closed unit disk $|z|\leq 1$. By the Maximum Modulus Principle, the maximum of $|f|$ occurs on the boundary $|z|=1$.

Let $z = e^{i\theta}$ on the boundary. Then:
$$|f(z)| = |e^{e^{2i\theta}}| = e^{\operatorname{Re}(e^{2i\theta})} = e^{\cos 2\theta}.$$

The maximum value is $e^1 = e$, attained when $\cos 2\theta = 1$ ($i.e.z = \pm 1$).

**(b)** The function $f(z)=\frac{z+3}{z-3}$ is analytic on $|z|\leq 1$ since its only singularity is at $z=3$, which lies outside the closed disk. The maximum modulus occurs on $|z|=1$.

On the boundary $|z|=1$, we have:
$$|f(z)| = \frac{|z+3|}{|z-3|}.$$

Using the triangle inequality:
- $|z+3| \leq |z| + 3 = 4$
- $|z-3| \geq |3| - |z| = 2$

Thus, $|f(z)| \leq 4/2 = 2$. Equality occurs when $z$ is a positive real number on the unit circle, i.e., $z=1$, giving $|f(1)| = |4/(-2)| = 2$.

**(c)** The function $f(z)=3-|z|^2$ is not analytic because it is not differentiable. The Maximum Modulus Principle applies only to analytic functions.

Since $|z|^2\geq 0$, the maximum value of $3-|z|^2$ on $|z|\leq 1$ is $3$, attained at $z=0$.
___

> [!problem]
> Prove the following version of minimal modulus principle: If $D\subset\mathbb{C}$ is a domain, and $f:D\to\mathbb{C}$ is analytic and non-constant, and if $f$ has in $a\in D$ a minimal modulus, then $f(a)=0$. Apply this to give another proof of the Fundamental Theorem of Algebra.

**Proof:**
Suppose $f(a) \neq 0$. Then $g(z) = 1/f(z)$ is analytic near $a$. Since $|f(z)|$ has a minimum at $a$, $|g(z)|$ has a maximum at $a$. By the Maximum Modulus Principle, $g$ is constant, so $f$ is constant, contradiction. Thus $f(a) = 0$.

**Application to Fundamental Theorem of Algebra:**
Let $p(z)$ be a nonconstant polynomial. Since $|p(z)| \to \infty$ as $|z| \to \infty$, $|p(z)|$ attains a minimum at some $a \in \mathbb{C}$. By the minimal modulus principle, $p(a) = 0$.
___

> [!problem]
> Let $f$ be a continuous function on a domain $D$. Suppose $f$ is analytic on the subset $D \setminus \mathbb{R}$ of $D$ not lying on the real axis. Show that $f$ is analytic on $D$.

**Proof:**
We need to show that $f$ is analytic at every point $z_0 \in D \cap \mathbb{R}$ by using Morera's Theorem.

Let $\gamma$ be any closed triangle in $D$ containing $z_0$.

If $\gamma$ does not intersect $\mathbb{R}$, then $\oint_\gamma f(z)dz = 0$ since $f$ is analytic on $D \setminus \mathbb{R}$.

If $\gamma$ intersects $\mathbb{R}$, we can approximate $\gamma$ by closed curves $\gamma_n$ in $D \setminus \mathbb{R}$ that converge uniformly to $\gamma$. Since $f$ is continuous on $D$ and analytic on $D \setminus \mathbb{R}$, we have $\oint_{\gamma_n} f(z)dz = 0$ for all $n$. By uniform convergence, $\oint_\gamma f(z)dz = 0$.

By Morera's Theorem, $f$ is analytic at $z_0$. Since $z_0$ was arbitrary, $f$ is analytic on all of $D$. 