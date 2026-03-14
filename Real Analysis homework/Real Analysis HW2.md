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

> [!problem] [SHE] 2A.12
> Suppose $r_1, r_2, \dots$ is a sequence that contains every rational number. Let
> $$F = \mathbb{R} \setminus \bigcup_{k=1}^{\infty} \left( r_k - \frac{1}{2^k},\, r_k + \frac{1}{2^k} \right).$$
> (a) Show that $F$ is a closed subset of $\mathbb{R}$.
> (b) Prove that if $I$ is an interval contained in $F$, then $I$ contains at most one element.
> (c) Prove that $|F| = \infty$.

**Proof:**
**(a)** The set $\bigcup_{k=1}^\infty (r_k - 1/2^k, r_k + 1/2^k)$ is a union of open intervals, hence it is open. Therefore its complement $F$ is closed.

**(b)** Suppose $I$ is an interval containing at least two distinct points $x<y$ in $F$. Then the rationals are dense in $\mathbb{R}$, so there exists a rational $r$ with $x<r<y$. Since $r$ is rational, it appears in the sequence as $r=r_k$ for some $k$. But then $r_k \in (r_k - 1/2^k, r_k + 1/2^k)$, hence $r_k \notin F$, contradicting that the whole open interval $(x,y)$ (and thus $r$) is in $I \subset F$. Therefore $I$ cannot contain two distinct points.

**(c)** We estimate the measure of the complement. Let $U = \bigcup_{k=1}^\infty (r_k - 1/2^k, r_k + 1/2^k)$. Then
$$|U| \le \sum_{k=1}^\infty \ell(r_k - 1/2^k, r_k + 1/2^k) = \sum_{k=1}^\infty \frac{2}{2^k} = 2.$$
Hence $|\mathbb{R} \setminus U| = |F| = \infty$ because $\mathbb{R}$ has infinite measure and removing a set of finite measure leaves the complement with infinite measure.
___

> [!problem] [SHE] 2B.5
> Suppose $\mathcal{S}$ is the smallest $\sigma$-algebra on $\mathbb{R}$ containing $\{(r, r+1) : r \in \mathbb{Q}\}$. Prove that $\mathcal{S}$ is the collection of Borel subsets of $\mathbb{R}$.

**Proof:**
Let $\mathcal{B}$ denote the Borel $\sigma$-algebra on $\mathbb{R}$. Since each interval $(r, r+1)$ (with $r \in \mathbb{Q}$) is open, it belongs to $\mathcal{B}$. Hence $\mathcal{S} \subset \mathcal{B}$.

We show that every open interval $(a,b)$ belongs to $\mathcal{S}$. Let $r_n$ be a rational sequence decreasing to $a$. Then $(a,b) = \bigcup_{n=1}^\infty (r_n, r_n+1) \cap (-\infty, b)$. Since $(-\infty, b) = \bigcup_{m} (q_m, q_m+1)$ for some rational $q_m$ approaching $b$, and $\mathcal{S}$ is closed under countable intersections and unions, $(a,b) \in \mathcal{S}$. Therefore all open intervals are in $\mathcal{S}$, and so $\mathcal{B} \subset \mathcal{S}$.

Thus $\mathcal{S} = \mathcal{B}$.
___

> [!problem] [SHE] 2B.8
> Prove that the collection of Borel subsets of $\mathbb{R}$ is dilation invariant. More precisely, prove that if $B \subset \mathbb{R}$ is a Borel set and $t \in \mathbb{R}$, then $tB$ (which is defined to be $\{tb : b \in B\}$) is a Borel set.

**Proof:**
Let $\mathcal{C}$ be the collection of all subsets $E \subset \mathbb{R}$ such that $tE$ is a Borel set for every $t \in \mathbb{R}$. We show that $\mathcal{C}$ contains all open intervals and is a $\sigma$-algebra, hence contains the Borel $\sigma$-algebra.

If $I = (a,b)$ is an open interval, then $tI$ is an open interval or empty, hence Borel. So all open intervals are in $\mathcal{C}$.

Check $\mathcal{C}$ is a $\sigma$-algebra:
- $\mathbb{R} \in \mathcal{C}$ because $t\mathbb{R} = \mathbb{R}$ (for $t\neq0$) or $\varnothing$ (for $t=0$), both Borel.
- If $E \in \mathcal{C}$, then $tE^c = (tE)^c$ (if $t\neq0$; if $t=0$, it's $\mathbb{R}$ or $\varnothing$), a Borel set, so $E^c \in \mathcal{C}$.
- If $E_n \in \mathcal{C}$ for $n\ge1$, then $t\big(\bigcup_n E_n\big) = \bigcup_n tE_n$, a countable union of Borel sets, hence Borel, so $\bigcup_n E_n \in \mathcal{C}$.

Thus $\mathcal{C}$ is a $\sigma$-algebra containing all open intervals, therefore contains the Borel $\sigma$-algebra. Hence for any Borel set $B$, $B \in \mathcal{C}$, i.e. $tB$ is Borel for all $t$.
___

> [!problem] [SHE] 2B.10
> Show that the set of real numbers that have a decimal expansion with the digit $5$ appearing infinitely often is a Borel set.

**Proof:**
Let $A$ be the set described. For each $n \in \mathbb{N}$, let
$$E_n = \{x \in \mathbb{R} : \text{the $n$th digit in some decimal expansion of $x$ is 5}\}.$$
Each $E_n$ is a countable union of intervals (since fixing a digit gives a countable union of intervals of length $10^{-n}$), hence Borel.

The set of numbers whose decimal expansion contains infinitely many $5$'s is
$$A = \bigcap_{k=1}^\infty \bigcup_{n=k}^\infty E_n.$$
This is a countable intersection of countable unions of Borel sets, hence Borel.
___
