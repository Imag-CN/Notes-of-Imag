___

> [!problem] [SHE] 2B.24
> Suppose $B \subset \mathbb{R}$ is a Borel set and $f: B \to \mathbb{R}$ is an increasing function.  
> Prove that $f(B)$ is a Borel set.

**Proof:**
Since $f$ is increasing, it is injective. Let $g: f(B) \to B$ be its inverse, which is also increasing. Extend $g$ to a non-decreasing function $G: \mathbb{R} \to \mathbb{R}$ by
$$G(x) = \sup \{ g(y) : y \in f(B), \, y \le x \}$$
with $\sup \varnothing = -\infty$.

$G$ is Borel measurable because any monotone function is Borel measurable. Observe that
$$f(B) = \{ x \in \mathbb{R} : G(x) \in B \} = G^{-1}(B).$$
Since $B$ is Borel and $G$ is Borel measurable, $G^{-1}(B)$ is Borel, hence $f(B)$ is Borel.
___

> [!problem] [SHE] 2B.25
> Let $B \subset \mathbb{R}$ and $f: B \to \mathbb{R}$ be an increasing function.  
> Prove that there exists a sequence of strictly increasing functions $f_k: B \to \mathbb{R}$ such that for every $x \in B$,  
> $$
> f(x) = \lim_{k \to \infty} f_k(x).
> $$

**Proof:**
Define $f_k(x) = f(x) + \frac{x}{k}$ for $x \in B$. Since $f$ is increasing and $x \mapsto \frac{x}{k}$ is strictly increasing, their sum $f_k$ is strictly increasing. For any fixed $x \in B$, $\lim_{k \to \infty} f_k(x) = f(x)$ because $\frac{x}{k} \to 0$. Thus $\{f_k\}$ satisfies the required conditions.
___

> [!problem] [SHE] 2D.20
> Evaluate each of the following:  
> (a) $\Lambda\left(\frac{9}{13}\right)$;  
> (b) $\Lambda(0.93)$.

**Solution:**
**(a)** $\Lambda(9/13) = 4/7$.
**(b)** $\Lambda(0.93) = 7/16$.
___

> [!problem] [SHE] 2D.21
> Find the following sets:  
> (a) $\Lambda^{-1}(\{\frac{1}{3}\})$;  
> (b) $\Lambda^{-1}(\{\frac{5}{16}\})$.

**Solution:**
**(a)** $\frac{1}{3} = 0.\overline{01}_2$ in binary. The unique ternary expansion in $C$ giving this binary is $0.\overline{02}_3 = \frac{1}{4}$. Since $\frac{1}{3}$ is not a dyadic rational, $\Lambda^{-1}(\{1/3\})$ is the singleton $\{\frac{1}{4}\}$.

**(b)** $\frac{5}{16} = 0.0101_2$ (finite binary) = $0.01001111\ldots_2$. The corresponding ternary expansions in $C$ are $0.0202_3 = \frac{20}{81}$ and $0.02000222\ldots_3 = \frac{19}{81}$. Since $\frac{5}{16}$ is dyadic, $\Lambda$ is constant on the interval between these two points. Thus $\Lambda^{-1}(\{5/81\}) = [\frac{20}{27}, \frac{55}{81}]$.
___

> [!problem] [SHE] 2D.23
> Show that there exists a function $f: \mathbb{R} \to \mathbb{R}$ such that the image under $f$ of every nonempty open interval is $\mathbb{R}$.

**Proof:**
Let $\mathcal{I}$ be the collection of all nonempty open intervals in $\mathbb{R}$. Since $|\mathcal{I}| = \mathfrak{c}$ and $|\mathbb{R}| = \mathfrak{c}$, we can well‑order $\mathcal{I} \times \mathbb{R}$ as $\{(I_\alpha, y_\alpha) : \alpha < \mathfrak{c}\}$.

We define $f$ by transfinite recursion. Start with $f$ undefined everywhere. At stage $\alpha < \mathfrak{c}$, choose a point $x_\alpha \in I_\alpha$ that has not been assigned a value yet (possible because $I_\alpha$ is uncountable and fewer than $\mathfrak{c}$ points have been used). Set $f(x_\alpha) = y_\alpha$. After all stages, define $f$ arbitrarily on any remaining points (e.g., $f(x)=0$).

For any nonempty open interval $I$ and any $y \in \mathbb{R}$, there exists $\alpha$ with $I_\alpha = I$ and $y_\alpha = y$. By construction, $x_\alpha \in I$ and $f(x_\alpha) = y$. Hence $f(I) = \mathbb{R}$.
___

> [!problem] [SHE] 2E.4
> Prove or give a counterexample:  
> If $A \subset \mathbb{R}$ and $f_1, f_2, \ldots$ is a sequence of uniformly continuous functions from $A$ to $\mathbb{R}$ that converge uniformly to a function $f: A \to \mathbb{R}$, then $f$ is uniformly continuous on $A$.

**Proof:**
Suppose $f_n: A \to \mathbb{R}$ are uniformly continuous and $f_n \rightrightarrows f$ uniformly on $A$. We show $f$ is uniformly continuous.

Let $\varepsilon > 0$ be given. Choose $N$ such that for all $x \in A$,
$$|f_N(x) - f(x)| < \frac{\varepsilon}{3}.$$
Since $f_N$ is uniformly continuous, there exists $\delta > 0$ such that for all $x, y \in A$ with $|x-y| < \delta$,
$$|f_N(x) - f_N(y)| < \frac{\varepsilon}{3}.$$
Then for any $x, y \in A$ with $|x-y| < \delta$,
$$
\begin{aligned}
|f(x) - f(y)|
&\le |f(x) - f_N(x)| + |f_N(x) - f_N(y)| + |f_N(y) - f(y)| \\
&< \frac{\varepsilon}{3} + \frac{\varepsilon}{3} + \frac{\varepsilon}{3} = \varepsilon.
\end{aligned}
$$
Thus $f$ is uniformly continuous on $A$.
___

> [!problem] [SHE] 2E.5
> Give a counterexample to show that Egorov’s theorem can fail if the hypothesis $\mu(X) < \infty$ is omitted.

**Proof:**
Let $X = \mathbb{R}$ with Lebesgue measure $\mu$. Define
$$f_n(x) = \chi_{[n, n+1]}(x) = 
\begin{cases}
1, & x \in [n, n+1] \\
0, & \text{otherwise}
\end{cases}$$
and $f(x) = 0$.

For each fixed $x$, $f_n(x) = 0$ for all $n > x$, so $f_n \to f$ pointwise everywhere. However, the convergence is not uniform on any set of finite measure complement. Indeed, for any set $E$ with $\mu(E^c) < \infty$, $E^c$ is bounded, so for sufficiently large $n$, $[n, n+1] \subset E$, hence $\sup_{x \in E} |f_n(x) - f(x)| = 1$. Therefore, $f_n$ does not converge uniformly on $E$.

Since $\mu(\mathbb{R}) = \infty$, Egorov’s theorem fails.
___

> [!problem] [SHE] 2E.6
> Suppose $(X, S, \mu)$ is a measure space with $\mu(X) < \infty$. Suppose $f_1, f_2, \ldots$ is a sequence of $S$-measurable functions from $X$ to $\mathbb{R}$ such that  
> $$\lim_{k \to \infty} f_k(x) = \infty \quad \text{for each } x \in X.$$  
> Prove that for every $\varepsilon > 0$, there exists a set $E \in S$ such that $\mu(X \setminus E) < \varepsilon$ and $f_1, f_2, \ldots$ converges uniformly to $\infty$ on $E$  
> (meaning that for every $t > 0$, there exists $n \in \mathbb{Z}^+$ such that $f_k(x) > t$ for all integers $k \geq n$ and all $x \in E$).

**Proof:**
Since $f_k(x) \to \infty$ for each $x$, for any $t > 0$ and any $x$ there exists $N$ such that $f_k(x) > t$ for all $k \ge N$. Equivalently,
$$X = \bigcup_{n=1}^\infty \{x : f_k(x) > t \text{ for all } k \ge n\}.$$
Let
$$A_{n,t} = \bigcap_{k=n}^\infty \{x : f_k(x) > t\} \in S.$$
Then $A_{1,t} \subset A_{2,t} \subset \cdots$ and $\bigcup_{n=1}^\infty A_{n,t} = X$.

Because $\mu(X) < \infty$, we have $\lim_{n\to\infty} \mu(A_{n,t}) = \mu(X)$. Hence, for a given $\varepsilon > 0$, we can choose $n_t$ such that
$$\mu(X \setminus A_{n_t,t}) < \frac{\varepsilon}{2^{\lceil t \rceil}}.$$

Now take a sequence $t_m = m$, $m = 1,2,\dots$. For each $m$, pick $n_m = n_{t_m}$ as above. Define
$$E = \bigcap_{m=1}^\infty A_{n_m, m}.$$
Then
$$\mu(X \setminus E) = \mu\!\left(\bigcup_{m=1}^\infty (X \setminus A_{n_m,m})\right) \le \sum_{m=1}^\infty \mu(X \setminus A_{n_m,m}) < \sum_{m=1}^\infty \frac{\varepsilon}{2^m} = \varepsilon.$$

Finally, we verify uniform convergence to $\infty$ on $E$. Given any $t > 0$, choose an integer $m$ with $m \ge t$. For $x \in E$, we have $x \in A_{n_m, m}$, so $f_k(x) > m \ge t$ for all $k \ge n_m$. Thus, with $n = n_m$, we have $f_k(x) > t$ for all $k \ge n$ and all $x \in E$. This is precisely uniform convergence to $\infty$ on $E$.
___

> [!problem] [SHE] 2E.8
> Suppose $\mu$ is the measure on $(\mathbf{Z}^{+}, 2^{\mathbf{Z}^{+}})$ defined by  
> $$\mu(E) = \sum_{n \in E} \frac{1}{2^n}.$$  
> Prove that for every $\varepsilon > 0$, there exists a set $E \subset \mathbf{Z}^{+}$ with $\mu(\mathbf{Z}^{+} \setminus E) < \varepsilon$ such that $f_1, f_2, \dots$ converges uniformly on $E$ for every sequence of functions $f_1, f_2, \dots$ from $\mathbf{Z}^{+}$ to $\mathbf{R}$ that converges pointwise on $\mathbf{Z}^{+}$.

**Proof:**
Given $\varepsilon > 0$, choose $N \in \mathbb{Z}^+$ such that $\sum_{n=N+1}^\infty \frac{1}{2^n} < \varepsilon$.  
Define $E = \{1,2,\dots,N\}$. Then
$$\mu(\mathbb{Z}^+ \setminus E) = \sum_{n=N+1}^\infty \frac{1}{2^n} < \varepsilon.$$
Now let $f_1,f_2,\dots$ be any sequence of functions from $\mathbb{Z}^+$ to $\mathbb{R}$ that converges pointwise on $\mathbb{Z}^+$. Since $E$ is a finite set, pointwise convergence on $E$ implies uniform convergence on $E$ (a standard result for finite sets). Therefore, $f_n$ converges uniformly on $E$.