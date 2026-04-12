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
Let $\{J_m\}$ enumerate all subintervals of $\mathbb{R}$ with rational endpoints. In each $J_m$, construct a fat Cantor set $C_m$ with
$$
m(C_m) = \frac12 m(J_m).
$$
Define
$$
E = \bigcup_{m=1}^\infty C_m.
$$
- $E$ is Borel.
- $E$ is dense (since each $J_m$ contains $C_m$).
- $E^c$ is also dense: for any interval $I$, $I\setminus C_m$ is nonempty open in $I$, and we can arrange that it avoids other $C_{m'}$ in a dense way.
- For any open interval $I$, choose $J_m \subset I$. Then
  $$
  m(E \cap I) \ge m(C_m) = \frac12 m(J_m) > 0,
  $$
  and
  $$
  m(E^c \cap I) = m(I) - m(E \cap I) \ge m(I) - \frac12 m(J_m) > 0
  $$
  (since $m(E \cap I) < m(I)$ by construction in subintervals).

Take $f = \chi_E$, a Borel function. Suppose $\exists B$ with $m(\mathbb{R}\setminus B)=0$ and $f|_B$ continuous. Then $B$ is dense, and because $E$ and $E^c$ are dense and of positive measure in every interval, $B\cap E$ and $B\cap E^c$ are dense in $B$. Hence $f|_B$ takes both 0 and 1 densely near any point, so it cannot be continuous anywhere – contradiction.

Thus $f$ is the required function.
___


