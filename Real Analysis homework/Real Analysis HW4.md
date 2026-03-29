___

> [!problem] [SHE] 5A.3
> Let $\mathcal{B}$ denote the $\sigma$-algebra of Borel subsets of $\mathbb{R}$. Show that there exists a set $E \subset \mathbb{R} \times \mathbb{R}$ such that $[E]_a \in \mathcal{B}$ and $[E]^a \in \mathcal{B}$ for every $a \in \mathbb{R}$, but $E \notin \mathcal{B} \otimes \mathcal{B}$.

**Proof:**
Let $E$ be the graph of a bijection $\phi: \mathbb{R} \to \mathbb{R}$ that is not Borel measurable (such $\phi$ exists: there are $2^\mathfrak{c}$ bijections but only $\mathfrak{c}$ Borel sets in $\mathbb{R}^2$, so some graph is not in $\mathcal{B} \otimes \mathcal{B}$).

For any $a \in \mathbb{R}$:
- $[E]_a = \{y : (a,y) \in E\} = \{\phi(a)\}$ (singleton, Borel)
- $[E]^a = \{x : (x,a) \in E\} = \{\phi^{-1}(a)\}$ (singleton, Borel)

Thus all sections are Borel, but $E \notin \mathcal{B} \otimes \mathcal{B}$.
___

> [!problem] [SHE] 2D.2
>Prove that there exists a bounded set $A \subset \mathbf{R}$ such that $|F| \leq |A| - 1$ for every closed set $F \subset A$.

**Construction**: Under the Continuum Hypothesis (CH), a Lusin set exists. Let $L \subset [0,1]$ be a Lusin set: $|L| = \mathfrak{c}$, and for every meager set $M \subset \mathbb{R}$, $|L \cap M| \le \aleph_0$. Take $A = L$. Then $A$ is bounded and $|A| = \mathfrak{c}$.

**Existence proof of Lusin set (CH)**:
Let $\{M_\alpha : \alpha < \omega_1\}$ enumerate all meager $F_\sigma$ subsets of $\mathbb{R}$ (under CH, there are exactly $\mathfrak{c} = \aleph_1$ such sets). Construct $L = \{x_\alpha : \alpha < \omega_1\}$ by transfinite recursion:
- At step $\alpha$, the set $\bigcup_{\beta < \alpha} M_\beta$ is meager, so its complement is co-meager, hence uncountable. Pick $x_\alpha \in [0,1] \setminus \bigl(\bigcup_{\beta < \alpha} M_\beta \cup \{x_\beta : \beta < \alpha\}\bigr)$.
Then $L$ is a Lusin set: if $M$ is meager, it is contained in some meager $F_\sigma$ set $M_\alpha$, so $L \cap M \subset \{x_\beta : \beta \le \alpha\}$ is countable.

**Proof for $A$**: Let $F \subset A$ be closed. Since $L$ contains no interval, $F$ has empty interior, so $F$ is nowhere dense, hence meager. By the Lusin property, $|F| = |F \cap L| \le \aleph_0$. Thus $|F| < |A|$, so $|F| \le |A|-1$ holds.
___

> [!problem] [SHE] 2D.6
>Suppose $A \subset \mathbf{R}$ and $|A| < \infty$. Prove that $A$ is Lebesgue measurable if and only if for every $\varepsilon > 0$ there exists a set $G$ that is the union of finitely many disjoint bounded open intervals such that $|A \setminus G| + |G \setminus A| < \varepsilon$.

**Proof:**
($\Rightarrow$) Suppose $A$ is Lebesgue measurable with $|A|<\infty$. For any $\varepsilon>0$, by outer regularity, there exists an open set $U \supset A$ such that $|U \setminus A| < \varepsilon/2$. Write $U = \bigcup_{j=1}^\infty I_j$ as a countable union of disjoint bounded open intervals. Since $|A|<\infty$, we have $|U| < |A| + \varepsilon/2 < \infty$. Choose $N$ large so that $\sum_{j>N} |I_j| < \varepsilon/2$. Let $G = \bigcup_{j=1}^N I_j$, a finite union of disjoint bounded open intervals. Then
$$
|A \setminus G| \le |A \setminus U| = 0, \quad |G \setminus A| \le |U \setminus A| + |U \setminus G| < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon.
$$
Hence $|A \setminus G| + |G \setminus A| < \varepsilon$.

($\Leftarrow$) Suppose for every $\varepsilon>0$ there exists a finite union $G_\varepsilon$ of disjoint bounded open intervals with $|A \setminus G_\varepsilon| + |G_\varepsilon \setminus A| < \varepsilon$. For each $n$, take $G_n$ such that the symmetric difference measure $|A \triangle G_n| < 1/n$. Let $B = \bigcap_{k=1}^\infty \bigcup_{n=k}^\infty G_n$ and $C = \bigcup_{k=1}^\infty \bigcap_{n=k}^\infty G_n$. Then $B$ is a $G_\delta$ set, $C$ is an $F_\sigma$ set, and $C \subset A \subset B$ up to null sets. More precisely, 
$$
|B \setminus A| \le \liminf_{n \to \infty} |G_n \setminus A| = 0, \quad |A \setminus C| \le \liminf_{n \to \infty} |A \setminus G_n| = 0.
$$
Thus $A = C \cup (A \setminus C)$ with $C$ Borel and $|A \setminus C| = 0$, so $A$ is Lebesgue measurable.
___

> [!problem] [SHE] 2C.12
> Suppose $b < c$ and $A \subset (b, c)$. Prove that $A$ is Lebesgue measurable if and only if
> $$|A| + |(b, c) \setminus A| = c - b.$$

**Proof:**
($\Rightarrow$) If $A$ is Lebesgue measurable, then $(b,c)\setminus A$ is also measurable. Since $A$ and $(b,c)\setminus A$ are disjoint and $A \cup ((b,c)\setminus A) = (b,c)$, by additivity of Lebesgue measure,
$$
|A| + |(b,c)\setminus A| = |(b,c)| = c-b.
$$

($\Leftarrow$) Suppose $|A| + |(b,c)\setminus A| = c-b$. Write $B = (b,c)\setminus A$. For any set $E \subset \mathbb{R}$, by subadditivity of outer measure $m^*$,
$$
m^*(E) \le m^*(E \cap A) + m^*(E \setminus A).
$$
It remains to prove the reverse inequality. Take $E = (b,c)$. Then
$$
m^*(E) = c-b = |A| + |B| \le m^*(E \cap A) + m^*(E \cap B) \le m^*(E \cap A) + m^*(E \setminus A).
$$
But $m^*(E) = m^*(E \cap A) + m^*(E \setminus A)$ follows from Carathéodory's criterion. For general $E$, split $E = (E \cap (b,c)) \cup (E \setminus (b,c))$ and use that $A \subset (b,c)$. More formally, for any $T \subset \mathbb{R}$,
$$
m^*(T) = m^*(T \cap (b,c)) + m^*(T \setminus (b,c)).
$$
Since $T \cap (b,c) \subset (b,c)$, the condition for $A$ on $(b,c)$ implies
$$
m^*(T \cap (b,c)) = m^*((T \cap (b,c)) \cap A) + m^*((T \cap (b,c)) \setminus A).
$$
Thus
$$
m^*(T) = m^*(T \cap A) + m^*(T \setminus A).
$$
Hence $A$ satisfies the Carathéodory criterion and is Lebesgue measurable.
___

> [!problem] [SHE] 2C.24(a) 
> For $A \subset \mathbb{R}$, the quantity
> $$\sup\{|F| : F \text{ is a closed bounded subset of } \mathbb{R} \text{ and } F \subset A\}$$
> is called the inner measure of $A$.
> 
>Show that if $A$ is a Lebesgue measurable subset of $\mathbb{R}$, then the inner measure of $A$ equals the outer measure of $A$.

**Proof:**
Let $A$ be Lebesgue measurable. Outer measure $m^*(A) = |A|$ (since $A$ is measurable, outer measure equals measure). We need to show
$$
\sup\{|F| : F \subset A, F \text{ closed bounded}\} = |A|.
$$

**Case 1: $|A| < \infty$.** For any $\varepsilon > 0$, by inner regularity of Lebesgue measure, there exists a closed set $F \subset A$ such that $|A \setminus F| < \varepsilon$. Since $|A| = |F| + |A \setminus F|$, we have $|F| > |A| - \varepsilon$. Thus the inner measure is at least $|A| - \varepsilon$ for every $\varepsilon > 0$, so it is at least $|A|$. But clearly inner measure $\le |A|$, hence equality.

**Case 2: $|A| = \infty$.** Write $A = \bigcup_{k=1}^\infty A_k$ with $A_k = A \cap [-k, k]$, so $|A_k| \le 2k < \infty$. For each $k$, pick closed $F_k \subset A_k$ with $|F_k| > |A_k| - 1$. Then $\sup_k |F_k| = \infty$, so inner measure is $\infty$, equal to outer measure.

Thus for any measurable $A$, inner measure = outer measure.
___

> [!problem] [SHE] 2B.16(b)
> Suppose $\mathcal{S}$ is a $\sigma$-algebra on a set $X$ and $A \subset X$. Let
> $$\mathcal{S}_A = \{E \in \mathcal{S} : A \subset E \text{ or } A \cap E = \varnothing\}.$$
> 
>Suppose $f: X \to \mathbf{R}$ is a function. Prove that $f$ is measurable with respect to $\mathcal{S}_A$ if and only if $f$ is measurable with respect to $\mathcal{S}$ and $f$ is constant on $A$.

**Proof:**
**($\Rightarrow$)**: Suppose $f$ is $\mathcal{S}_A$-measurable.  
- Since $\mathcal{S}_A \subset \mathcal{S}$, for any open $U \subset \mathbb{R}$, $f^{-1}(U) \in \mathcal{S}_A \subset \mathcal{S}$, so $f$ is $\mathcal{S}$-measurable.  
- Assume $f$ is not constant on $A$. Then $\exists x_1, x_2 \in A$ with $f(x_1) \ne f(x_2)$. Choose $r$ between $f(x_1)$ and $f(x_2)$. Let $U = (-\infty, r)$. Then $x_1 \in f^{-1}(U)$ but $x_2 \notin f^{-1}(U)$, so $A \not\subset f^{-1}(U)$ and $A \cap f^{-1}(U) \neq \varnothing$. Hence $f^{-1}(U) \notin \mathcal{S}_A$, contradiction. Thus $f$ is constant on $A$.

**($\Leftarrow$)**: Suppose $f$ is $\mathcal{S}$-measurable and $f|_A \equiv c$ (constant). For any open $U \subset \mathbb{R}$, $f^{-1}(U) \in \mathcal{S}$. Now:
  - If $c \in U$, then $A \subset f^{-1}(U)$.
  - If $c \notin U$, then $A \cap f^{-1}(U) = \varnothing$.
In either case, $f^{-1}(U) \in \mathcal{S}_A$ by definition. Hence $f$ is $\mathcal{S}_A$-measurable.
___

> [!problem] [SHE] 2B.17
> Suppose $X$ is a Borel subset of $\mathbb{R}$ and $f: X \to \mathbb{R}$ is a function such that
> $$\{x \in X : f \text{ is not continuous at } x\}$$
> is a countable set. Prove $f$ is a Borel measurable function.

**Proof:**
Let $D = \{x \in X : f \text{ is discontinuous at } x\}$, which is countable. Write $D = \{d_1, d_2, \dots\}$. Let $C = X \setminus D$, where $f$ is continuous.

For any open $U \subset \mathbb{R}$, we have
$$f^{-1}(U) = (f^{-1}(U) \cap C) \cup (f^{-1}(U) \cap D).$$

- Since $f|_C$ is continuous, $f^{-1}(U) \cap C$ is open in $C$, hence Borel (because $C$ is Borel, and relatively open sets in a Borel set are Borel).
- $f^{-1}(U) \cap D$ is countable (a subset of $D$), hence Borel.

Thus $f^{-1}(U)$ is a union of two Borel sets, so Borel. Therefore $f$ is Borel measurable.
___

> [!problem] [SHE] 2B.19
> Suppose $X$ is a nonempty set and $\mathcal{S}$ is the $\sigma$-algebra on $X$ consisting of all subsets of $X$ that are either countable or have a countable complement in $X$. Give a characterization of the $\mathcal{S}$-measurable real-valued functions on $X$.

**Answer:** A function $f: X \to \mathbb{R}$ is $\mathcal{S}$-measurable if and only if it is constant except possibly on a countable set. In other words, there exists a constant $c \in \mathbb{R}$ such that the set $\{x \in X : f(x) \ne c\}$ is countable.

**Proof:**
 If $f$ is constant $c$ outside a countable set $C$, then for any $a \in \mathbb{R}$, $f^{-1}((a, \infty))$ is either a subset of $C$ (if $c \le a$) or contains the co-countable set $X \setminus C$ (if $c > a$), hence is in $\mathcal{S}$.

Conversely, let $f$ be $\mathcal{S}$-measurable. Partition $\mathbb{R}$ into intervals $I_n=[n, n+1]$. Their preimages are in $\mathcal{S}$ and cover $X$. Since $X$ is uncountable (trivial if $X$ countable), at least one preimage, say $A=f^{-1}(I_m)$, is co-countable. Restrict to $I_m$ and repeatedly bisect. The preimage of at least one half is co-countable each time, yielding a nested sequence of intervals with intersection a point $\{c\}$. Then $f^{-1}(\{c\})$ is a countable intersection of co-countable sets, hence co-countable. Thus $\{x: f(x)\ne c\}$ is countable.
___

> [!problem] [SHE] 2B.20
> Suppose $(X, \mathcal{S})$ is a measurable space and $f, g: X \to \mathbb{R}$ are $\mathcal{S}$-measurable functions. Prove that if $f(x) > 0$ for all $x \in X$, then $f^g$ (which is the function whose value at $x \in X$ equals $f(x)^{g(x)}$) is an $\mathcal{S}$-measurable function.

**Proof:**
Since $f(x) > 0$, we can write
$$
f(x)^{g(x)} = e^{g(x)\ln f(x)}.
$$

Because $f$ and $g$ are $\mathcal{S}$-measurable, $\ln f$ is measurable (composition of the measurable function $f$ with the continuous function $\ln:(0,\infty)\to\mathbb{R}$).  
Hence $g\ln f$ is measurable (product of two measurable functions).  

Finally, $e^{g\ln f}$ is measurable as the composition of the measurable function $g\ln f$ with the continuous exponential function $\exp:\mathbb{R}\to\mathbb{R}$.  

Thus $f^g = e^{g\ln f}$ is $\mathcal{S}$-measurable.
___

