___

> [!problem] [SHE] 2A.8
> Prove that if $A \subset \mathbb{R}$ and $t > 0$, then
> $$|A| = |A \cap (-t,t)| + |A \cap (\mathbb{R} \setminus (-t,t))|.$$

**Proof:**
Let $I = (-t,t)$. For any $A \subset \mathbb{R}$, we have
$$A = (A \cap I) \cup (A \cap I^c),$$
and the two sets on the right are disjoint.

By monotonicity and subadditivity of outer measure,
$$|A| \le |A \cap I| + |A \cap I^c|.$$

For the reverse inequality: for any $\varepsilon > 0$, choose a covering of $A$ by intervals $\{J_k\}$ such that
$$\sum_k l(J_k) \le |A| + \varepsilon.$$

Write $J_k = J_k \cap I$ and $J_k' = J_k \cap I^c$. Then $A \cap I \subset \bigcup_k (J_k \cap I)$ and $A \cap I^c \subset \bigcup_k (J_k \cap I^c)$. Hence
$$|A \cap I| + |A \cap I^c| \le \sum_k l(J_k \cap I) + \sum_k l(J_k \cap I^c) = \sum_k l(J_k) \le |A| + \varepsilon.$$
 Letting $\varepsilon \to 0$ gives $|A \cap I| + |A \cap I^c| \le |A|$.

Therefore
$$|A| = |A \cap (-t,t)| + |A \cap (\mathbb{R} \setminus (-t,t))|.$$
___

> [!problem] [SHE] 2A.9
> Prove that $|A| = \lim_{t \to \infty} |A \cap (-t,t)|$ for all $A \subset \mathbb{R}$.

**Proof:**
Denote $A_t = A \cap (-t, t)$. Clearly $A_t \subset A_{t'}$ for $t < t'$, and $\bigcup_{t>0} A_t = A$.

Let $m_t = |A_t|$. Since $A_t$ increases with $t$, $m_t$ is non-decreasing and bounded above by $|A|$, so $\lim_{t \to \infty} m_t \le |A|$.

To show equality: fix $\varepsilon > 0$. By definition of outer measure, there exists a covering of $A$ by intervals $\{I_k\}$ such that
$$
\sum_k l(I_k) \le |A| + \varepsilon.
$$
Since $\bigcup_{t} A_t = A$, the sets $A_t$ eventually cover any compact subset of $A$. In particular, for large $t$, the covering intervals $\{I_k\}$ can be chosen so that their union covers $A_t$ up to a small error. More directly: for each $k$, choose $t_k$ such that $I_k \subset (-t_k, t_k)$. Let $T = \max_k t_k$. Then $A_T$ covers the part of $A$ inside $\bigcup_k I_k$, so
$$
|A_T| \le \sum_k l(I_k) \le |A| + \varepsilon.
$$
Hence $|A_T| \le |A| + \varepsilon$. Since $m_t$ is non-decreasing and $\varepsilon$ is arbitrary,
$$
\lim_{t \to \infty} m_t \le |A|.
$$
Together with $m_t \le |A|$ for all $t$, we get
$$
\lim_{t \to \infty} |A \cap (-t, t)| = |A|.
$$
___

> [!problem] [SHE] 2A.11
> Prove that if $I_1, I_2, \dots$ is a disjoint sequence of open intervals, then
> $$\left| \bigcup_{k=1}^{\infty} I_k \right| = \sum_{k=1}^{\infty} \ell(I_k).$$

**Proof:**
Let $E=\bigcup_{k=1}^{\infty} I_k$. Since the intervals are disjoint, we have $\sum_{k=1}^n \ell(I_k) = \left|\bigcup_{k=1}^n I_k \right|$ for all $n$. By monotonicity and countable subadditivity of outer measure,
$$
\sum_{k=1}^n \ell(I_k) = \left|\bigcup_{k=1}^n I_k\right| \le |E| \le \sum_{k=1}^\infty \ell(I_k).
$$
Letting $n \to \infty$ gives
$$
\sum_{k=1}^\infty \ell(I_k) \le |E| \le \sum_{k=1}^\infty \ell(I_k),
$$
hence equality holds.
___

> [!problem]
> Suppose $r_1, r_2, \dots$ is a sequence that contains every rational number. Let
> $$F = \mathbb{R} \setminus \bigcup_{k=1}^{\infty} \left( r_k - \frac{1}{2^k},\, r_k + \frac{1}{2^k} \right).$$
> (a) Show that $F$ is a closed subset of $\mathbb{R}$.
> (b) Prove that if $I$ is an interval contained in $F$, then $I$ contains at most one element.
> (c) Prove that $|F| = \infty$.