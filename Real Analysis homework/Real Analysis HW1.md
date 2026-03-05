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