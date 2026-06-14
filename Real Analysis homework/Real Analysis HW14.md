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

