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
$$E_n = \{x \in \mathbb{R} : \text{the $n$-th digit in the decimal expansion of $x$ is 5}\}.$$
Each $E_n$ is a countable union of intervals (since fixing a digit gives a countable union of intervals of length $10^{-n}$), hence Borel.

The set of numbers whose decimal expansion contains infinitely many $5$'s is
$$A = \bigcap_{k=1}^\infty \bigcup_{n=k}^\infty E_n.$$
This is a countable intersection of countable unions of Borel sets, hence Borel.
___

> [!problem] [SHE] 2B.15(a)
> Suppose $X$ is a set and $E_1, E_2, \dots$ is a disjoint sequence of subsets of $X$ such that
> $$\bigcup_{k=1}^{\infty} E_k = X.$$
> Let
> $$\mathcal{S} = \left\{ \bigcup_{k \in K} E_k : K \subset \mathbb{Z}^+ \right\}.$$
> 
> Show that $\mathcal{S}$ is a $\sigma$-algebra on $X$.

**Proof:**
We verify the three conditions for a $\sigma$-algebra:

1. $X \in \mathcal{S}$: Let $K = \mathbb{Z}^+$, then $\bigcup_{k \in \mathbb{Z}^+} E_k = X \in \mathcal{S}$.

2. Closed under complement: Take $A = \bigcup_{k \in K} E_k \in \mathcal{S}$. Since the $E_k$ are disjoint, $X = \bigcup_{k=1}^\infty E_k$, we have
   $$A^c = \bigcup_{k \in \mathbb{Z}^+ \setminus K} E_k.$$
   Since $\mathbb{Z}^+ \setminus K \subset \mathbb{Z}^+$, $A^c \in \mathcal{S}$.

3. Closed under countable unions: Let $A_n = \bigcup_{k \in K_n} E_k \in \mathcal{S}$, $n=1,2,\dots$. Then
   $$\bigcup_{n=1}^\infty A_n = \bigcup_{n=1}^\infty \bigcup_{k \in K_n} E_k = \bigcup_{k \in \bigcup_{n=1}^\infty K_n} E_k.$$
   Since $\bigcup_{n=1}^\infty K_n \subset \mathbb{Z}^+$, this union is in $\mathcal{S}$.

Thus $\mathcal{S}$ is a $\sigma$-algebra on $X$.
___

> [!problem] [SHE] 2B.16(a)
> Suppose $\mathcal{S}$ is a $\sigma$-algebra on a set $X$ and $A \subset X$. Let
> $$\mathcal{S}_A = \{ E \in \mathcal{S} : A \subset E \text{ or } A \cap E = \varnothing \}.$$
> 
>Prove that $\mathcal{S}_A$ is a $\sigma$-algebra on $X$.

**Proof:**
We verify the three conditions for a $\sigma$-algebra:

1. $X \in \mathcal{S}_A$: Since $X \in \mathcal{S}$ and $A \subset X$, we have $X \in \mathcal{S}_A$.

2. Closed under complement: Let $E \in \mathcal{S}_A$. There are two cases:
   - If $A \subset E$, then $A \cap E^c = \varnothing$ (because $A$ is contained in $E$), so $E^c \in \mathcal{S}_A$.
   - If $A \cap E = \varnothing$, then $A \subset E^c$ (since $A$ is disjoint from $E$), so $E^c \in \mathcal{S}_A$.
   In both cases, $E^c \in \mathcal{S}_A$.

3. Closed under countable unions: Let $\{E_n\} \subset \mathcal{S}_A$. Consider $\bigcup_n E_n$. Two cases:
   - If there exists some $n_0$ such that $A \subset E_{n_0}$, then $A \subset \bigcup_n E_n$, so $\bigcup_n E_n \in \mathcal{S}_A$.
   - Otherwise, $A \cap E_n = \varnothing$ for all $n$, so $A \cap (\bigcup_n E_n) = \varnothing$, hence $\bigcup_n E_n \in \mathcal{S}_A$.
   Thus $\bigcup_n E_n \in \mathcal{S}_A$.

Therefore $\mathcal{S}_A$ is a $\sigma$-algebra on $X$.
___

> [!problem] [SHE] 2C.2
> Let $2^{\mathbb{Z}^+}$ denote the $\sigma$-algebra on $\mathbb{Z}^+$ consisting of all subsets of $\mathbb{Z}^+$.
> Suppose $\mu$ is a measure on $(\mathbb{Z}^+, 2^{\mathbb{Z}^+})$. Prove that there is a sequence $w_1, w_2, \dots$ in $[0, \infty]$ such that
> $$
> \mu(E) = \sum_{k \in E} w_k
> $$
> for every set $E \subset \mathbb{Z}^+$.

**Proof:**
Define $w_k = \mu(\{k\})$ for each $k \in \mathbb{Z}^+$. Since $\mu$ is a measure, $w_k \in [0, \infty]$.

For any $E \subset \mathbb{Z}^+$, we can write $E = \bigcup_{k \in E} \{k\}$, a disjoint countable union. By countable additivity of $\mu$,
$$\mu(E) = \mu\left(\bigcup_{k \in E} \{k\}\right) = \sum_{k \in E} \mu(\{k\}) = \sum_{k \in E} w_k.$$

Thus the sequence $(w_k)$ satisfies the required property.
___

>[!definition]
>An outer measure $\mu^*$ on a non-empty set $X$ is a function
>$$
>\mu^* : \mathcal{P}(X) \to [0, \infty]
>$$
>that satisfies  
>(i) $\mu^*(\emptyset) = 0$;  
>(ii) $\mu^*(A) \leq \mu^*(B)$ if $A, B$ are subsets of $X$ with $A \subseteq B$;  
>(iii) $\mu^*\left( \bigcup_{n=1}^{\infty} A_n \right) \leq \bigcup_{n=1}^{\infty} \mu^*(A_n)$ if $A_n$ ($n \in \mathbb{N}$) are subsets of $X$.

> [!problem]
> Let $\mathcal{E}$ be a family of sets of $X$, and $\ell : \mathcal{E} \to [0, \infty]$.
> Suppose that $\emptyset, X \in \mathcal{E}$ and $\ell(\emptyset) = 0$.
> For any $A \subseteq X$, define
> $$\mu^*(A) = \inf\left\{ \sum_{n=1}^{\infty} \ell(I_n) : I_n \in \mathcal{E} \, (n \in \mathbb{N}),\ A \subseteq \bigcup_{n=1}^{\infty} I_n \right\}.$$
> Prove that $\mu^*$ is an outer measure.

**Proof:**
We verify three conditions of an outer measure:

1. $\mu^*(\emptyset) = 0$: Since $\emptyset \in \mathcal{E}$ and $\ell(\emptyset)=0$, the covering $\{I_n\}$ with $I_1 = \emptyset$ and $I_n = \emptyset$ for $n \ge 2$ gives $\sum_{n=1}^\infty \ell(I_n)=0$. Hence $\mu^*(\emptyset)=0$.

2. Monotonicity: If $A \subseteq B \subseteq X$, then every covering of $B$ also covers $A$. Thus the infimum for $A$ is taken over a larger set than that for $B$, so $\mu^*(A) \le \mu^*(B)$.

3. Countable subadditivity: Let $\{A_n\}_{n=1}^\infty$ be subsets of $X$. If $\sum_{n=1}^\infty \mu^*(A_n)=\infty$, the inequality holds trivially. Otherwise, fix $\varepsilon>0$. For each $n$, choose a covering $\{I_{n,k}\}_{k=1}^\infty \subset \mathcal{E}$ of $A_n$ such that
   $$\sum_{k=1}^\infty \ell(I_{n,k}) \le \mu^*(A_n) + \frac{\varepsilon}{2^n}.$$
   Then $\{I_{n,k}\}_{n,k \ge 1}$ is a countable covering of $\bigcup_n A_n$, and
   $$\mu^*\left(\bigcup_{n=1}^\infty A_n\right) \le \sum_{n=1}^\infty\sum_{k=1}^\infty \ell(I_{n,k}) \le \sum_{n=1}^\infty \left(\mu^*(A_n) + \frac{\varepsilon}{2^n}\right) = \sum_{n=1}^\infty \mu^*(A_n) + \varepsilon.$$
   Since $\varepsilon>0$ was arbitrary, $\mu^*\left(\bigcup_n A_n\right) \le \sum_n \mu^*(A_n)$.

Thus $\mu^*$ is an outer measure.