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
Enumerate all open intervals $(a_n,b_n)$ in $\mathbf{R}$ with rational endpoints. For each $n$, construct in $(a_n,b_n)$ a "fat Cantor set" $C_n$ with $m(C_n) > 0$ and $m((a_n,b_n)\setminus C_n) > 0$.

Let $E = \bigcup_{n=1}^\infty C_n$. Then:
1. $E$ is Borel.
2. For any open interval $I$, choose $(a_n,b_n) \subset I$. Then $E\cap I$ contains $C_n$, so $m(E\cap I) > 0$.
3. $E^c\cap I$ contains $(a_n,b_n)\setminus C_n$, so $m(E^c\cap I) > 0$.
4. Both $E$ and $E^c$ are dense in $\mathbf{R}$.

Thus $f = \chi_E$ works: For any $B$ with $m(\mathbf{R}\setminus B)=0$, both $B\cap E$ and $B\cap E^c$ are dense in $B$, so $f|_B$ is nowhere continuous.
___


