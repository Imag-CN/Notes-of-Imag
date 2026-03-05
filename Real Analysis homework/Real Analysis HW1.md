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

> [!problem] [SHE] 1B.4
> Construct an example of bounded functions $f, g: [0,1] \to \mathbb{R}$ such that
> $$
> L(f, [0,1]) + L(g, [0,1]) < L(f + g, [0,1])
> $$
> and
> $$
> U(f + g, [0,1]) < U(f, [0,1]) + U(g, [0,1]),
> $$
> where $L(f, [0,1])$ and $U(f, [0,1])$ denote the lower and upper Riemann integrals of $f$ on $[0,1]$, respectively.

**Proof:**
Define $f, g: [0,1] \to \mathbb{R}$:
$$
f(x)=\begin{cases}
-1,&x \in \mathbb{Q} \\
1,&x \in \mathbb{R}\setminus \mathbb{Q}
\end{cases}\quad,g(x)=-f(x).
$$
Then $L(f, [0,1]) = L(g, [0,1]) =-1$, $L(f + g, [0,1])=0$, and $U(f, [0,1]) = U(g, [0,1])=1$, $U(f + g, [0,1])=0$. This satisfies the given conditions.
___

> [!problem] [SHE] 6A.6
> (a) Prove that if $V$ is a metric space, $f \in V$, and $r > 0$, then $\overline{B(f, r)} \subset \overline{B}(f, r)$.  
> (b) Give an example of a metric space $V$, $f \in V$, and $r > 0$ such that $\overline{B(f, r)} \neq \overline{B}(f, r)$.

**Proof:**
**(a)** By definition we have $B(f, r) \subset \overline{B}(f, r)$. The closure $\overline{B(f, r)}$ is the smallest closed set containing $B(f,r)$, and $\overline{B}(f, r)$ is a closed set containing $B(f,r)$, thus $\overline{B(f, r)} \subset \overline{B}(f, r)$.
**(b)** Let $V$ be a set containing at least two elements, and equip it with discrete metric (then it has the discrete topology). Let $f \in V$, then $B(f,1)= \{ f \}$, and $\overline{ B }(f,1)=V$. However, ${f}$ itself is a closed set, thus $\overline{ B(f,r) }=\{ f \}$ . Therefore $\overline{B(f, r)} \neq \overline{B}(f, r)$.
___

> [!problem] [SHE] 2A.2
> Suppose $A \subset \mathbb{R}$ and $t \in \mathbb{R}$. Let $tA = \{ta : a \in A\}$. Prove that $|tA| = |t|\,|A|$.  

**Proof:**
**Case 1.** $t=0$.
Then $tA=\{0\}$ or $\varnothing$, so $|tA|=0$.
RHS is $0 \cdot |A|=0$ (by convention $0\cdot\infty=0$). Equality holds.
**Case 2.** $t\neq0$.
- For an interval $I=(a,b)$, $tI$ is $(ta,tb)$ or $(tb,ta)$; $|tI|=|t|(b-a)=|t|\,|I|$.
- For an open set $G=\bigcup_k I_k$ (disjoint intervals), $tG=\bigcup_k tI_k$ disjoint, so
$|tG|=\sum_k |tI_k|=\sum_k |t|\,|I_k|=|t|\,|G|$.
- For any $A\subset\mathbb{R}$, by definition of outer measure,
$$\begin{align}
|tA|&=\inf\{|tG|:A\subset G,\;G\text{ open}\}\\
&=\inf\{|t|\,|G|:A\subset G,\;G\text{ open}\}\\
&=|t|\,\inf\{|G|:A\subset G,\;G\text{ open}\}\\
&=|t|\,|A|.
\end{align} $$
Thus $|tA|=|t|\,|A|$ for all $A$ and all $t$.
___

> [!problem] [SHE] 2A.3
> Prove that if $A, B \subset \mathbb{R}$ and $|A| < \infty$, then $|B \setminus A| \geq |B| - |A|$.

**Proof:**
Since $B = (B \setminus A) \cup (B \cap A)$ and the two sets are disjoint, we have
$$ |B| \leq |B \setminus A| + |B \cap A| $$
by the countable subadditivity of outer measure.

Because $B \cap A \subset A$, monotonicity gives $|B \cap A| \leq |A|$. Hence
$$ |B| \leq |B \setminus A| + |A|. $$
Now subtract $|A|$ (which is finite, so subtraction is safe) to obtain
$$
|B| - |A| \leq |B \setminus A|.
$$