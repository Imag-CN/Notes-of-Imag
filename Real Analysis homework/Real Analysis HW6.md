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

