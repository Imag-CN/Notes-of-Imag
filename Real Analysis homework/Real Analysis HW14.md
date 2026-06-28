___

>[!problem] [SHE] 7A.13
>Show that $\bigcup_{p>1} \mathcal{L}^p([0, 1]) \neq \mathcal{L}^1([0, 1])$.

**Proof:**
We have $f(x)=1 /x \in \mathcal{L}^p([0, 1])$ for any $p>1$, but $f(x)\neq 1 /x \in \mathcal{L}^1([0, 1])$.
___

>[!problem] [SHE] 7A.18
>Suppose $0 < p < \infty$ and $f \in \mathcal{L}^p(\mathbf{R})$. Prove that for every $\varepsilon > 0$, there exists a step function $g \in \mathcal{L}^p(\mathbf{R})$ such that $\|f - g\|_p < \varepsilon$.

**Proof:**
First, assume $f \geq 0$. There exists a sequence of nonnegative simple functions $\varphi_n \uparrow f$ pointwise. By monotone convergence, $\|\varphi_n - f\|_p \to 0$, so pick a simple function $\varphi = \sum_{i=1}^k a_i \chi_{E_i}$ with $\|f-\varphi\|_p < \varepsilon/2$.

For each measurable set $E_i$, by regularity of Lebesgue measure, there exists a finite union of intervals $F_i$ such that $m(E_i \triangle F_i) < (\varepsilon/(2k^{1/p} |a_i|))^p$ (if $a_i = 0$, ignore). Define the step function $g = \sum_{i=1}^k a_i \chi_{F_i}$. Then
$$
\|\varphi - g\|_p^p = \sum_{i=1}^k |a_i|^p m(E_i \triangle F_i) < \sum_{i=1}^k |a_i|^p \cdot \frac{\varepsilon^p}{2^p k |a_i|^p} = \frac{\varepsilon^p}{2^p},
$$
so $\|\varphi - g\|_p < \varepsilon/2$. Hence $\|f - g\|_p \leq \|f-\varphi\|_p + \|\varphi - g\|_p < \varepsilon$.

For general $f \in \mathcal{L}^p(\mathbb{R})$, write $f = f^+ - f^-$, approximate each part separately by step functions $g_1, g_2$, and take $g = g_1 - g_2$.
___

>[!problem] [SHE] 7B.4
>Suppose $(X, \mathcal{S}, \mu)$ is a $\sigma$-finite measure space and $1 \leq p \leq \infty$. Prove that if $f: X \to \mathbf{F}$ is an $\mathcal{S}$-measurable function such that $fh \in \mathcal{L}^1(\mu)$ for every $h \in \mathcal{L}^{p'}(\mu)$, then $f \in \mathcal{L}^p(\mu)$.

**Proof:**
**Case $1 < p < \infty$:**  
By $\sigma$-finiteness, take $f_n = f \cdot \chi_{\{|f| \leq n\} \cap E_n}$ where $E_n \uparrow X$ with $\mu(E_n) < \infty$. Then $f_n \in \mathcal{L}^p$ and for any $h \in \mathcal{L}^{p'}$, $\int f_n h \to \int f h$ by dominated convergence. Each $f_n$ induces a bounded functional on $L^{p'}$ with norm $\|f_n\|_p$. By the uniform boundedness principle, $\sup_n \|f_n\|_p < \infty$, so $\|f\|_p = \lim_n \|f_n\|_p < \infty$.

**Case $p = 1$:**  
Take $h = \operatorname{sgn}(f) \in L^\infty$. Then $\int |f| = \int f h < \infty$, so $f \in \mathcal{L}^1$.

**Case $p = \infty$:**  
Define $\Lambda(h) = \int f h$ for $h \in \mathcal{L}^1$. If $h_n \to h$ in $L^1$ and $\Lambda(h_n) \to c$, then a subsequence $h_{n_k} \to h$ a.e., so $f h_{n_k} \to f h$ a.e. and Fatou gives $fh \in \mathcal{L}^1$. Dominated convergence yields $\int f h_{n_k} \to \int f h$, so $c = \int f h$. Thus $\Lambda$ has closed graph, hence is bounded, so $\|\Lambda\| = \|f\|_\infty < \infty$.
___

>[!problem] [SHE] 7B.5
> (a) Prove that if $\mu$ is a measure, $1 < p < \infty$, and $f, g \in L^p(\mu)$ are such that
> $$ \|f\|_p = \|g\|_p = \left\| \frac{f+g}{2} \right\|_p, $$
> then $f = g$.
>
> (b) Give an example to show that the result in part (a) can fail if $p = 1$.
>
> (c) Give an example to show that the result in part (a) can fail if $p = \infty$.

**Proof:**
**(a)** Let $1 < p < \infty$. By strict convexity of $t \mapsto t^p$ for $t \geq 0$ when $p > 1$, we have for any $a, b \geq 0$,
$$
\left(\frac{a+b}{2}\right)^p \leq \frac{a^p + b^p}{2},
$$
with equality iff $a = b$. Apply this pointwise to $|f|, |g|$:
$$
\left|\frac{f+g}{2}\right|^p \leq \left(\frac{|f|+|g|}{2}\right)^p \leq \frac{|f|^p + |g|^p}{2}.
$$
Integrating gives
$$
\left\| \frac{f+g}{2} \right\|_p^p \leq \frac{\|f\|_p^p + \|g\|_p^p}{2}.
$$
Given $\|f\|_p = \|g\|_p = \|(f+g)/2\|_p$, we have equality throughout. Hence equality holds in both inequalities a.e.:

- Equality in the second inequality (Minkowski-type) forces $|f| = |g|$ a.e.
- Equality in the first inequality (triangle inequality for absolute value) forces $f$ and $g$ to have the same sign a.e., i.e., $f/g \geq 0$ a.e. (with the convention $0/0 = 1$).

Thus $f = g$ a.e.

**(b)** Take $f = \chi_{[0,1]}$, $g = \chi_{[1,2]}$ on $\mathbb{R}$ with Lebesgue measure. Then $\|f\|_1 = \|g\|_1 = 1$, and $(f+g)/2 = \frac12(\chi_{[0,1]} + \chi_{[1,2]})$ has $L^1$ norm $1$, but $f \neq g$.

**(c)** Take $f = \chi_{[0,1]}$, $g = \chi_{[0,2]}$ on $\mathbb{R}$ with Lebesgue measure. Then $\|f\|_\infty = 1$, $\|g\|_\infty = 1$, and $(f+g)/2 = \chi_{[0,1]} +1 /2 \cdot\chi_{[0,2]})$ has $\sup$ norm $1$, but $f \neq g$.
___

>[!problem] [SHE] 7B.13
>Suppose $(X, \mathcal{S}, \mu)$ is a measure space, $1 \leq p \leq \infty$, $f \in \mathcal{L}^p(\mu)$, and $f_1, f_2, \dots$ is a sequence in $\mathcal{L}^p(\mu)$ such that
>$$
>\lim_{k \to \infty} \|f_k - f\|_p = 0.
>$$
>Show that if $g: X \to \mathbf{F}$ is a function such that
>$$
>\lim_{k \to \infty} f_k(x) = g(x)
>$$
>for almost every $x \in X$, then
>$$
>f(x) = g(x)
>$$
>for almost every $x \in X$.

**Proof:**
Since $\|f_k - f\|_p \to 0$, there exists a subsequence $\{f_{k_j}\}$ such that $f_{k_j}(x) \to f(x)$ for almost every $x \in X$. By hypothesis, $f_k(x) \to g(x)$ for almost every $x \in X$, so the subsequence also satisfies $f_{k_j}(x) \to g(x)$ a.e. By uniqueness of limits, $f(x) = g(x)$ for almost every $x \in X$.
___

>[!problem] [SHE] 7B.15
>Let
>$$
>c_{0} = \left\{ (a_1, a_2, \dots) \in \ell^{\infty} : \lim_{k \to \infty} a_k = 0 \right\}.
>$$
>Give $c_0$ the norm that it inherits as a subspace of $\ell^{\infty}$.
>
>(a) Prove that $c_0$ is a Banach space.
>
>(b) Prove that the dual space of $c_0$ can be identified with $\ell^{1}$.

**Proof:**
**(a)** $c_0$ is a closed subspace of $\ell^\infty$: if $a^{(n)} \to a$ in $\ell^\infty$ and each $a^{(n)} \in c_0$, then $a \in c_0$. Indeed, given $\varepsilon > 0$, pick $N$ such that $\|a^{(N)} - a\|_\infty < \varepsilon/2$, and $K$ such that $|a_k^{(N)}| < \varepsilon/2$ for all $k \geq K$. Then for $k \geq K$, $|a_k| \leq |a_k - a_k^{(N)}| + |a_k^{(N)}| < \varepsilon$, so $\lim_{k\to\infty} a_k = 0$. Hence $c_0$ is closed in the Banach space $\ell^\infty$, therefore complete.

**(b)** Identify $\ell^1$ with the dual of $c_0$ via the pairing $\langle a, b \rangle = \sum_{k=1}^\infty a_k b_k$ for $a \in c_0$, $b \in \ell^1$. This map $b \mapsto \varphi_b$ is an isometric embedding of $\ell^1$ into $(c_0)^*$ because $|\langle a, b \rangle| \leq \|a\|_\infty \|b\|_1$ and taking $a = (\operatorname{sgn}(b_1), \dots, \operatorname{sgn}(b_N), 0, 0, \dots)$ shows $\|\varphi_b\| = \|b\|_1$. Conversely, any $\varphi \in (c_0)^*$ defines $b_k = \varphi(e_k)$ where $e_k$ is the $k$-th standard basis vector. For any $a \in c_0$, $a = \sum_{k=1}^\infty a_k e_k$ in norm, so $\varphi(a) = \sum a_k b_k$. To see $b \in \ell^1$, consider $a^{(N)} = (\operatorname{sgn}(b_1), \dots, \operatorname{sgn}(b_N), 0, 0, \dots) \in c_0$ with $\|a^{(N)}\|_\infty = 1$. Then $\sum_{k=1}^N |b_k| = \varphi(a^{(N)}) \leq \|\varphi\|$, so $\|b\|_1 \leq \|\varphi\| < \infty$. Hence $b \in \ell^1$ and the identification is isometric.
___

>[!problem] [SHE] 8A.11
>Suppose $f$ and $g$ are elements of an inner product space. Prove that $\|f\| = \|g\|$ if and only if $\|sf + tg\| = \|tf + sg\|$ for all $s, t \in \mathbb{R}$.

**Proof:**
($\Rightarrow$) Assume $\|f\| = \|g\|$. Compute
$$
\begin{aligned}
\|sf + tg\|^2 &= \langle sf + tg, sf + tg \rangle \\
&= s^2\|f\|^2 + t^2\|g\|^2 + 2st \langle f, g \rangle, \\
\|tf + sg\|^2 &= t^2\|f\|^2 + s^2\|g\|^2 + 2st \langle f, g \rangle.
\end{aligned}
$$
Since $\|f\| = \|g\|$, the first two terms are equal: $s^2\|f\|^2 + t^2\|g\|^2 = t^2\|f\|^2 + s^2\|g\|^2$. Hence $\|sf + tg\|^2 = \|tf + sg\|^2$, and taking square roots gives $\|sf + tg\| = \|tf + sg\|$.

($\Leftarrow$) Taking $s=0$ and $t=1$ yields the result.
___

>[!problem] [SHE] 8A.17
>Let $\lambda$ denote Lebesgue measure on $[1, \infty)$.
>
>(a) Prove that if $f: [1, \infty) \to [0, \infty)$ is Borel measurable, then
>$$
>\left(\int_{1}^{\infty} f(x) \, d\lambda(x)\right)^2 \leq \int_{1}^{\infty} x^2 (f(x))^2 \, d\lambda(x).
>$$
>
>(b) Describe the set of Borel measurable functions $f: [1, \infty) \to [0, \infty)$ such that the inequality in part (a) is an equality.

**Proof:**
Write
$$
\int_1^\infty f(x) \, dx = \int_1^\infty \frac{1}{x} \cdot x f(x) \, dx.
$$
Apply the Cauchy-Schwarz inequality:
$$
\left( \int_1^\infty \frac{1}{x} \cdot x f(x) \, dx \right)^2 \leq \left( \int_1^\infty \frac{1}{x^2} \, dx \right) \left( \int_1^\infty x^2 (f(x))^2 \, dx \right).
$$
Since $\int_1^\infty 1/x^2 \, dx = 1$, we obtain
$$
\left( \int_1^\infty f(x) \, dx \right)^2 \leq \int_1^\infty x^2 (f(x))^2 \, dx.
$$

**(b)** Equality in Cauchy-Schwarz holds iff the two functions are linearly dependent, i.e., there exists a constant $c \in \mathbb{R}$ such that
$$
\frac{1}{x} = c \cdot x f(x) \quad \text{a.e.}
$$
Equivalently, $f(x) = c/x^2$ for almost every $x \in [1, \infty)$. Since $f \geq 0$, we require $c \geq 0$. Thus the set of functions attaining equality is
$$
\{ f : [1, \infty) \to [0, \infty) \mid f(x) = \frac{c}{x^2} \text{ a.e. for some } c \geq 0 \}.
$$
___

>[!problem] [SHE] 8B.3
>Suppose $V_1, V_2, \dots$ are Hilbert spaces. Let
>$$
>V = \left\{ (f_1, f_2, \dots) \in V_1 \times V_2 \times \cdots : \sum_{k=1}^{\infty} \|f_k\|^2 < \infty \right\}.
>$$
>Show that the equation
>$$
>\left\langle (f_1, f_2, \dots), (g_1, g_2, \dots) \right\rangle = \sum_{k=1}^{\infty} \left\langle f_k, g_k \right\rangle
>$$
>defines an inner product on $V$ that makes $V$ a Hilbert space.

**Proof:**
For $f = (f_1, f_2, \dots)$, $g = (g_1, g_2, \dots)$, $h = (h_1, h_2, \dots) \in V$ and $a, b \in \mathbb{C}$:

1. **Linearity:** $\langle af + bg, h \rangle = \sum_k \langle a f_k + b g_k, h_k \rangle = a \sum_k \langle f_k, h_k \rangle + b \sum_k \langle g_k, h_k \rangle = a \langle f, h \rangle + b \langle g, h \rangle$.
2. **Conjugate symmetry:** $\langle g, f \rangle = \sum_k \langle g_k, f_k \rangle = \sum_k \overline{\langle f_k, g_k \rangle} = \overline{\langle f, g \rangle}$.
3. **Positive definiteness:** $\langle f, f \rangle = \sum_k \|f_k\|^2 \geq 0$, and equals $0$ iff $\|f_k\| = 0$ for all $k$, i.e., $f = 0$.

Thus $\langle \cdot, \cdot \rangle$ is an inner product. The induced norm is $\|f\| = \sqrt{\sum_k \|f_k\|^2}$.

**Completeness:** Let $\{f^{(n)}\}_{n=1}^\infty$ be a Cauchy sequence in $V$, where $f^{(n)} = (f_1^{(n)}, f_2^{(n)}, \dots)$. For each fixed $k$, the sequence $\{f_k^{(n)}\}_{n=1}^\infty$ is Cauchy in $V_k$ because $\|f_k^{(n)} - f_k^{(m)}\| \leq \|f^{(n)} - f^{(m)}\|$. Since $V_k$ is complete, there exists $f_k \in V_k$ such that $f_k^{(n)} \to f_k$ in $V_k$.

Now we show $f = (f_1, f_2, \dots) \in V$ and $f^{(n)} \to f$ in $V$. Given $\varepsilon > 0$, pick $N$ such that for all $n, m \geq N$, $\|f^{(n)} - f^{(m)}\|^2 = \sum_{k=1}^\infty \|f_k^{(n)} - f_k^{(m)}\|^2 < \varepsilon^2$. For any finite $K$,
$$
\sum_{k=1}^K \|f_k^{(n)} - f_k^{(m)}\|^2 < \varepsilon^2.
$$
Fix $n \geq N$ and let $m \to \infty$. By continuity of the norm, $\sum_{k=1}^K \|f_k^{(n)} - f_k\|^2 \leq \varepsilon^2$. Taking $K \to \infty$ gives $\sum_{k=1}^\infty \|f_k^{(n)} - f_k\|^2 \leq \varepsilon^2$, so $f^{(n)} - f \in V$ and $\|f^{(n)} - f\| \leq \varepsilon$. Hence $f = f^{(n)} - (f^{(n)} - f) \in V$, and $f^{(n)} \to f$ in $V$.
___

>[!problem] [SHE] 8B.11
>Suppose $V$ is a Hilbert space. A *closed half-space* of $V$ is a set of the form
>$$
>\{g \in V : \operatorname{Re}\langle g, h \rangle \geq c\}
>$$
>for some $h \in V$ and some $c \in \mathbb{R}$.
>
>Prove that every closed convex subset of $V$ is the intersection of all the closed half-spaces that contain it.

**Proof:**
Let $C \subseteq V$ be a closed convex set. Define
$$
D = \bigcap \{ H : H \text{ is a closed half-space containing } C \}.
$$
Clearly $C \subseteq D$. We prove $D \subseteq C$.

Suppose $x \notin C$. Since $C$ is closed and convex, by the Hilbert space projection theorem, there exists a unique $y \in C$ such that $\|x - y\| = \operatorname{dist}(x, C) > 0$. Set $h = x - y \neq 0$ and $c = \langle y, h \rangle$. Then for any $z \in C$, by convexity and the minimizing property of $y$, we have $\langle z - y, h \rangle \leq 0$, i.e.,
$$
\langle z, h \rangle \leq \langle y, h \rangle = c.
$$
Thus every $z \in C$ satisfies $\langle z, h \rangle \leq c$, so the half-space $H = \{ v \in V : \langle v, h \rangle \leq c \}$ contains $C$. But $x$ satisfies
$$
\langle x, h \rangle = \langle y + h, h \rangle = \langle y, h \rangle + \|h\|^2 = c + \|h\|^2 > c,
$$
so $x \notin H$. Hence $x \notin D$, proving $D \subseteq C$.
___

>[!problem] [SHE] 8B.18
>Suppose $U$ and $W$ are subspaces of a Hilbert space $V$. Prove that $\overline{U} = \overline{W}$ if and only if $U^\perp = W^\perp$.

**Proof:**
Let $U, W$ be subspaces of a Hilbert space $V$.

$(\Rightarrow)$ Assume $\overline{U} = \overline{W}$. Since $U^\perp = (\overline{U})^\perp$ and $W^\perp = (\overline{W})^\perp$, we have $U^\perp = (\overline{U})^\perp = (\overline{W})^\perp = W^\perp$.

$(\Leftarrow)$ Assume $U^\perp = W^\perp$. Taking orthogonal complements, we obtain $(U^\perp)^\perp = (W^\perp)^\perp$. For any subspace $S$ of a Hilbert space, $(S^\perp)^\perp = \overline{S}$. Hence $\overline{U} = (U^\perp)^\perp = (W^\perp)^\perp = \overline{W}$.