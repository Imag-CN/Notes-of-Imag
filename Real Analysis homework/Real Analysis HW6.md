___

>[!problem] [SHE] 2E.10
>Suppose $F \subset \mathbf{R}$ is such that every continuous function from $F$ to $\mathbf{R}$ can be extended to a continuous function from $\mathbf{R}$ to $\mathbf{R}$. Prove that $F$ is a closed subset of $\mathbf{R}$.

**Proof:**
Assume $F$ is not closed. Then there exists a limit point $x_0$ of $F$ such that $x_0 \notin F$.

Define $f: F \to \mathbb{R}$ by $f(x) = \frac{1}{x - x_0}$. Since $x_0 \notin F$, $f$ is well-defined and continuous on $F$.

Suppose $f$ has a continuous extension $\tilde{f}: \mathbb{R} \to \mathbb{R}$. Since $x_0$ is a limit point of $F$, we can find a sequence $\{x_n\} \subset F$ such that $x_n \to x_0$. Then
$$
\lim_{n \to \infty} \tilde{f}(x_n) = \lim_{n \to \infty} \frac{1}{x_n - x_0} = \infty.
$$
This contradicts the continuity of $\tilde{f}$ at $\mathbf{R}$. Therefore, $F$ must be closed.
___

>[!problem] [SHE] 2E.11
>Prove or give a counterexample: If $F \subset \mathbf{R}$ is such that every bounded continuous function from $F$ to $\mathbf{R}$ can be extended to a continuous function from $\mathbf{R}$ to $\mathbf{R}$, then $F$ is a closed subset of $\mathbf{R}$.

**Proof:**
Assume $F$ is not closed. Then there exists a limit point $x_0$ of $F$ with $x_0 \notin F$. Since $x_0$ is a limit point of $F$, we can find a strictly increasing or decreasing sequence $\{x_n\} \subset F$ such that $x_n \to x_0$. W.O.L.G. we suppose $\{ x_{n} \}$ is increasing

Define $f: F \to \mathbb{R}$ by
$$
f(x)=\begin{cases}
1,&\text{if }x =x_{n}\text{ with }n\text{ odd or }x<x_{1}, \\
-1,&\text{if } x =x_{n}\text{ with }n\text{ even}, \\
\dfrac{f(x_{n})-f(x_{n+1})}{x_{n}-x_{n+1}}(x-x_{n})+f(x_{n}),&\text{if }x \in(x_{n},x_{n+1}) \\
0,&\text{if }x>x_{0}
\end{cases}
$$
Since $x_0 \notin F$, $f$ is well-defined and continuous on $F$.

Suppose $f$ has a continuous extension $\tilde{f}: \mathbb{R} \to \mathbb{R}$. Then
$$
\lim_{ n \to \infty } \tilde{f}(x_{n})=\lim_{ n \to \infty } f(x_{n}),\text{ which doesn't exist}.
$$
This contradicts the continuity of $\tilde{f}$ at $\mathbf{R}$. Therefore, $F$ must be closed.
___

>[!problem] [SHE] 2E.12
>Give an example of a Borel measurable function $f$ from $\mathbf{R}$ to $\mathbf{R}$ such that there does not exist a set $B \subset \mathbf{R}$ such that $|\mathbf{R} \backslash B|=0$ and $f|_{B}$ is a continuous function on $B$.

**Proof:**
Let $C \subset [0,1]$ be a fat Cantor set with $m(C) > 0$. Define $f = \chi_C$ (the characteristic function of $C$).

Since $C$ is closed, it is Borel; so $f$ is Borel measurable. It is obvious that every point of $C$ is a limit point of $C^c$ (the complement in $[0,1]$).

Suppose there exists $B \subset \mathbb{R}$ with $m(\mathbb{R} \setminus B) = 0$ such that $f|_B$ is continuous. Because $m(C) > 0$, the set $B \cap C$ has positive measure. Let $x_0 \in B \cap C$ be a point of density of $B \cap C$ (which exists by Lebesgue density theorem). Since $x_0$ is a limit point of $C^c$, and $m(\mathbb{R} \setminus B) = 0$, we can find a sequence $\{y_n\} \subset B \cap C^c$ with $y_n \to x_0$. Then $f(y_n) = 0$ for all $n$, but $f(x_0) = 1$. Hence $f|_B$ is not continuous at $x_0$, contradiction.

Therefore, no such $B$ exists, and $f = \chi_C$ is the required function.
___

>[!problem] [SHE] 2E.14
>Suppose $b_{1}, b_{2}, \ldots$ is a sequence of real numbers. Define $f: \mathbf{R} \rightarrow[0, \infty]$ by
>$$
>f(x)= \begin{cases}\displaystyle\sum_{k=1}^{\infty} \frac{1}{4^{k}\left|x-b_{k}\right|} & \text { if } x \notin\left\{b_{1}, b_{2}, \ldots\right\} \\ \infty & \text { if } x \in\left\{b_{1}, b_{2}, \ldots\right\}.\end{cases}
>$$
>Prove that
>$$
>\left|\left\{x \in \mathbf{R}: f(x)<1\right\}\right|=\infty.
>$$

**Proof:**
Define intervals
$$
I_k = \left(b_k - \frac{1}{2^{k-1}}, b_k + \frac{1}{2^{k-1}}\right), \quad k \ge 1.
$$
Their total length is
$$
\sum_{k=1}^\infty |I_k| = \sum_{k=1}^\infty \frac{2}{2^{k-1}} = 4.
$$

Let $E = \bigcup_{k=1}^\infty I_k$. Then $|E| \le 4$, so $\mathbf{R} \setminus E$ has infinite measure.

Take any $x \in \mathbf{R} \setminus E$. Then $|x - b_k| \ge \frac{1}{2^{k-1}}$ for all $k$, and $x \notin \{b_k\}$. Hence
$$
f(x) = \sum_{k=1}^\infty \frac{1}{4^k |x - b_k|}
\le \sum_{k=1}^\infty \frac{1}{4^k \cdot 2^{-k+1}}
= \sum_{k=1}^\infty \frac{1}{2^{k+1}} = \dfrac{1}{2}<1.
$$
Therefore, $\mathbf{R}\setminus E\subset\left\{x \in \mathbf{R}: f(x)<1\right\}$, then $\left|\left\{x \in \mathbf{R}: f(x)<1\right\}\right| \geq \left| \mathbf{R}\setminus E \right|=\infty$.
___

>[!problem] [SHE] 3A.2
>Suppose $X$ is a set, $\mathcal{S}$ is a $\sigma$-algebra on $X$, and $c \in X$.
>Define the Dirac measure $\delta_c$ on $(X,\mathcal{S})$ by
>$$\delta_c(E)=\begin{cases}1 & \text { if } c \in E, \\ 0 & \text { if } c \notin E.\end{cases}$$
>Prove that if $f: X \rightarrow[0, \infty]$ is $\mathcal{S}$-measurable, then $\int f \, d\delta_c=f(c)$.

**Proof:**
Take simple functions $s_n = \sum_i a_i^{(n)} \chi_{A_i^{(n)}}$ with $s_n \uparrow f$.

For a simple $s = \sum_{i=1}^m a_i \chi_{A_i}$ ($a_i \ge 0$, $A_i$ disjoint in $\mathcal{S}$), by definition
$$
\int s \, d\delta_c = \sum_{i=1}^m a_i \, \delta_c(A_i).
$$
Since the $A_i$ are disjoint, $\delta_c(A_i)=1$ for at most one $i$ (the one containing $c$), else $0$. Hence $\int s \, d\delta_c = s(c)$.

Now
$$
\int f \, d\delta_c = \lim_{n\to\infty} \int s_n \, d\delta_c,
$$
and $\int s_n \, d\delta_c = s_n(c) \uparrow f(c)$. Therefore
$$
\int f \, d\delta_c = f(c).
$$
___

>[!problem] [SHE] 3A.7
>Suppose $X$ is a set, $\mathcal{S}$ is the $\sigma$-algebra of all subsets of $X$, and $w: X \rightarrow[0, \infty]$ is a function. Define a measure $\mu$ on $(X, \mathcal{S})$ by
>$$\mu(E)=\sum_{x \in E} w(x)$$
>for $E \subset X$. Prove that if $f: X \rightarrow[0, \infty]$ is a function, then
>$$\int f \, d \mu=\sum_{x \in X} w(x) f(x),$$
>where the infinite sums above are defined as the supremum of all sums over finite subsets of $X$.

**Proof:**
**Case 1:** $f$ simple: $f = \sum_{i=1}^n a_i \chi_{A_i}$, $A_i$ disjoint. Then
$$
\int f \, d\mu = \sum_{i=1}^n a_i \mu(A_i) = \sum_{i=1}^n a_i \sum_{x \in A_i} w(x) = \sum_{x \in X} w(x) f(x).
$$
**Case 2:** General $f \ge 0$: take simple $s_n \uparrow f$. Then
$$
\int f \, d\mu = \lim_{n\to\infty} \int s_n \, d\mu
\quad\text{(MCT)},
$$
and
$$
\int s_n \, d\mu = \sum_{x \in X} w(x) s_n(x) \uparrow \sum_{x \in X} w(x) f(x)
$$
by monotone convergence of sums. Hence
$$
\int f \, d\mu = \sum_{x \in X} w(x) f(x).
$$
___

>[!problem] [SHE] 3A.3
>Suppose $(X, \mathcal{S}, \mu)$ is a measure space and $f: X \rightarrow[0, \infty]$ is an $\mathcal{S}$-measurable function. Prove that
>$$\int f \, d \mu>0 \quad \text { if and only if } \quad \mu(\{x \in X: f(x)>0\})>0.$$

**Proof:**
Let $E = \{x \in X : f(x) > 0\}$.

($\Leftarrow$) Assume $\mu(E) > 0$.

Define $E_n = \{x \in X : f(x) > 1/n\}$ for $n \in \mathbb{N}$. Then $E_n \uparrow E$, so $\mu(E_n) \uparrow \mu(E) > 0$. Thus there exists $N$ such that $\mu(E_N) > 0$.

Since $f \ge \frac{1}{N} \chi_{E_N}$, we have
$$
\int f \, d\mu \ge \int \frac{1}{N} \chi_{E_N} \, d\mu = \frac{1}{N} \mu(E_N) > 0.
$$

($\Rightarrow$) Assume $\mu(E) = 0$, i.e., $f = 0$ $\mu$-almost everywhere. Then for any simple function $0 \le s \le f$, we have $s = 0$ $\mu$-a.e., so $\int s \, d\mu = 0$. By the definition of the integral of a nonnegative measurable function as the supremum of integrals of simple functions below it, we get
$$
\int f \, d\mu = 0.
$$

Hence $\int f \, d\mu = 0$ if $\mu(E)=0$.

Thus $\int f \, d\mu > 0$ iff $\mu(E) > 0$.
___

>[!problem] [SHE] 3A.4
>Give an example of a Borel measurable function $f:[0,1] \rightarrow(0, \infty)$ such that
>$$L(f,[0,1])=0.$$

**Proof:**
Let $\sim$ be the equivalence relation on $[0,1]$ defined by $x \sim y \iff x-y \in \mathbf{Q}$. The equivalence classes are $C_\alpha = r_\alpha + \mathbf{Q} \ (\text{mod } 1)$，each dense in $[0,1]$.

Enumerate countably many distinct equivalence classes as $C_1, C_2, C_3, \dots$, define
$$
C_0 = [0,1] \setminus \bigcup_{n=1}^\infty C_n.
$$
Then $\{C_0, C_1, \dots, \}$ are disjoint, each is dense in $[0,1]$, and each is Borel.

Now define
$$
f(x) = \frac{1}{2^n} \quad \text{if } x \in C_n \ (n \ge 0).
$$
Then $f(x) > 0$ for all $x$. $f$ is Borel measurable because for any $a\in \mathbf{R}$
$$
f^{-1}((a,+\infty))=\bigcup_{n \text{ with } \frac{1}{2^n}>a}C_{n}.
$$
Each $A_n$ is dense, so any interval contains points from infinitely many $A_n$, hence $\inf_I f = 0$. Thus lower Riemann sums vanish, i.e. $L(f,[0,1])=0.$
___



