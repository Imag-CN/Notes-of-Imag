___

> [!problem]
> Consider sets and functions on $\mathbb{R}$.
> (1) Explain that a family of disjoint (non-empty) open intervals is a countable set.
> (2) Explain that the set of discontinuity points of a monotonic function is countable.

**Proof:** 
**(1)** Let $\{I_\alpha\}_{\alpha \in \Lambda}$ be a family of disjoint, non-empty open intervals in $\mathbb{R}$. Since $\mathbb{Q}$ is dense in $\mathbb{R}$, for each $\alpha$, the intersection $I_\alpha \cap \mathbb{Q}$ is non-empty. Choose a rational number $r_\alpha \in I_\alpha \cap \mathbb{Q}$. Because the intervals are disjoint, the assignment $\alpha \mapsto r_\alpha$ defines an injective map from the index set $\Lambda$ into the countable set $\mathbb{Q}$. Hence, the family $\{I_\alpha\}_{\alpha \in \Lambda}$ is at most countable.

**(2)** Let $f:\mathbb{R} \to \mathbb{R}$ be monotone increasing (the decreasing case is analogous). For any $x \in \mathbb{R}$, the left-hand limit $f(x^-)$ and the right-hand limit $f(x^+)$ exist, and $f(x^-) \le f(x^+)$. The function $f$ is discontinuous at $x$ iff $f(x^-) < f(x^+)$. For each such discontinuity point $x$, associate the non-empty open interval $J_x := \big( f(x^-),\, f(x^+) \big)$.

If $x_1 < x_2$ are two distinct discontinuity points, monotonicity implies $f(x_1^+) \le f(x_2^-)$. Therefore, $J_{x_1}$ and $J_{x_2}$ are disjoint intervals. Consequently, $\{J_x \mid x \text{ is a discontinuity point of } f\}$ is a family of pairwise disjoint, non-empty open intervals. By part **(1)**, this family is at most countable. Hence, the set of discontinuity points of $f$ itself is at most countable.
___

> [!problem]
> Let $f(x), f_1(x), f_2(x), \ldots$ be real-valued functions on $\mathbb{R}$. Denote by $D$ the set of all points $x$ such that $\lim_{n \to \infty} f_n(x) \neq f(x)$. Prove that
> $$
> D = \bigcup_{k=1}^{\infty} \bigcap_{N=1}^{\infty} \bigcup_{n=N}^{\infty} \left\{ x \in \mathbb{R} : |f_n(x) - f(x)| \geq \frac{1}{k} \right\}.
> $$

**Proof:**
Denote $E_{n,k} = \{x : |f_n(x)-f(x)| \geq 1/k\}$.

**($\subseteq$)** Let $x_0 \in D$, so $\lim_{n}f_n(x_0) \neq f(x_0)$.
Then $\exists \varepsilon>0$ such that $\forall N,\ \exists n\geq N$ with $|f_n(x_0)-f(x_0)| \geq \varepsilon$.
Take $k$ with $1/k \leq \varepsilon$.
Then $\forall N,\ \exists n\geq N$ with $|f_n(x_0)-f(x_0)| \geq 1/k$,
i.e. $x_0 \in \bigcap_N \bigcup_{n\geq N} E_{n,k} \subseteq$ RHS.

**($\supseteq$)** Let $x_0$ be in RHS.
Then $\exists k$ such that $x_0 \in \bigcap_N \bigcup_{n\geq N} E_{n,k}$.
Thus for infinitely many $n$, $|f_n(x_0)-f(x_0)| \geq 1/k > 0$, so $f_n(x_0) \not\to f(x_0)$, i.e. $x_0 \in D$.

Hence $D$ equals the given union.
___

> [!problem] [SHE] 1A.1
> Suppose $f:[a,b] \to \mathbb{R}$ is a bounded function, and there exists a partition $P$ of $[a,b]$ such that the lower sum equals the upper sum, i.e.,
> $$ L(f,P,[a,b]) = U(f,P,[a,b]). $$
> Prove that $f$ must be constant on $[a,b]$.

**Proof:**
Let $P = \{x_0 = a < x_1 < \dots < x_n = b\}$ be the given partition. For each subinterval $I_i = [x_{i-1},x_i]$, define
$m_i = \inf_{x \in I_i} f(x)$ and $M_i = \sup_{x \in I_i} f(x)$. The lower and upper sums are
$$
L(f,P) = \sum_{i=1}^n m_i (x_i - x_{i-1}), \quad
U(f,P) = \sum_{i=1}^n M_i (x_i - x_{i-1}).
$$
Since $L(f,P) = U(f,P)$, we have
$$
0 = U(f,P) - L(f,P) = \sum_{i=1}^n (M_i - m_i)(x_i - x_{i-1}).
$$
Each term is $\ge 0$ and $(x_i - x_{i-1}) > 0$. Hence $M_i = m_i$ for every $i$, i.e. $\sup_{I_i} f = \inf_{I_i} f$.

Therefore, on each $I_i$, $f$ is constant; say $f(x) = c_i$ for all $x \in I_i$.

Now take a common point $x_i$ of two consecutive intervals $I_i$ and $I_{i+1}$. On $I_i$, $f(x_i) = c_i$; on $I_{i+1}$, $f(x_i) = c_{i+1}$. Hence $c_i = c_{i+1}$. By induction, all $c_i$ are equal. Thus $f$ is constant on $[a,b]$.
___

> [!problem] [SHE] 1B.2
> Let $f:[a,b] \to \mathbb{R}$ be a bounded function. Show that $f$ is Riemann integrable on $[a,b]$ if and only if
> $$
> L(-f, [a,b]) = -L(f, [a,b]),
> $$
> where $L(f,[a,b])$ denotes the lower integral of $f$ on $[a,b]$.

**Proof:**
For any subinterval $I$, $\inf_I (-f) = -\sup_I f$. Thus for any partition $P$,
$$ L(-f, P) = \sum_i \bigl( \inf_{I_i} (-f) \bigr) \Delta x_i = \sum_i \bigl( -\sup_{I_i} f \bigr) \Delta x_i = -U(f, P). $$
Taking supremum over all partitions $P$,
$$
L(-f) = \sup_P L(-f, P) = \sup_P \bigl[ -U(f, P) \bigr] = -\inf_P U(f, P) = -U(f).
$$
Therefore, $f$ is Riemann integrable (i.e., $L(f)=U(f)$) if and only if $L(-f)=-L(f)$.
___

