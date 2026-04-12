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

**Construction of $E$**
Let $\{I_n\}$ enumerate all open intervals with rational endpoints. In each $I_n$, construct disjoint "fat" Cantor sets $A_n, B_n \subset I_n$ with $m(A_n)=m(B_n)=\frac{1}{3}m(I_n)$. Set  

$$
E = \bigcup_n A_n, \quad F = \bigcup_n B_n.
$$

**Properties:**
- $E$ and $F$ are disjoint Borel sets.
- For any open interval $J$, choose $I_n \subset J$. Then $E\cap J \supset A_n$ and $F\cap J \supset B_n$, so $m(E\cap J)>0$ and $m(F\cap J)>0$. Since $F \subset E^c$, $m(E^c\cap J)>0$.
- Hence $E$ and $E^c$ are dense and have positive measure in every open interval.

**The function**

Take $f = \chi_E$, Borel measurable. Suppose $\exists B$ with $m(\mathbb{R}\setminus B)=0$ and $f|_B$ continuous. Since $E$ and $E^c$ are dense and intersect every interval positively, $B\cap E$ and $B\cap E^c$ are both dense in $B$. Then $f|_B$ takes both $0$ and $1$ densely near any point of $B$, so it cannot be continuous anywhere — contradiction.

Thus $f$ is the desired function.
___


