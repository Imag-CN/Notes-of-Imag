___

>[!problem] [SHE] 2E.10
>Suppose $F \subset \mathbf{R}$ is such that every continuous function from $F$ to $\mathbf{R}$ can be extended to a continuous function from $\mathbf{R}$ to $\mathbf{R}$. Prove that $F$ is a closed subset of $\mathbf{R}$.

**Proof:**
Assume $F$ is not closed. Then there exists a limit point $x_0$ of $F$ such that $x_0 \notin F$.

Define $f: F \to \mathbb{R}$ by $f(x) = \frac{1}{x - x_0}$. Since $x_0 \notin F$, $f$ is well-defined and continuous on $F$.

Suppose there exists a continuous extension $\tilde{f}: \mathbb{R} \to \mathbb{R}$. Then $\tilde{f}|_F = f$. Since $x_0$ is a limit point of $F$, we can find sequences $\{x_n^+\} \subset F$ or $\{x_n^-\} \subset F$ such that $x_n^+ \to x_0^+$ and $x_n^- \to x_0^-$. Then
$$
\lim_{n \to \infty} \tilde{f}(x_n^+) = \lim_{n \to \infty} \frac{1}{x_n^+ - x_0} = +\infty,
$$
$$
\lim_{n \to \infty} \tilde{f}(x_n^-) = \lim_{n \to \infty} \frac{1}{x_n^- - x_0} = -\infty.
$$
This contradicts the continuity of $\tilde{f}$ at $\mathbf{R}$. Therefore, $F$ must be closed.
___

>[!problem] [SHE] 2E.11
>Prove or give a counterexample: If $F \subset \mathbf{R}$ is such that every bounded continuous function from $F$ to $\mathbf{R}$ can be extended to a continuous function from $\mathbf{R}$ to $\mathbf{R}$, then $F$ is a closed subset of $\mathbf{R}$.

**Proof:**
Assume $F$ is not closed. Then there exists a limit point $x_0$ of $F$ with $x_0 \notin F$.

Define $f: F \to \mathbb{R}$ by $f(x) = \sin\left(\frac{1}{x - x_0}\right)$.

- $f$ is bounded since $|\sin(\cdot)| \leq 1$.
- $f$ is continuous on $F$ because $x_0 \notin F$, so $x - x_0 \neq 0$ for all $x \in F$.

Suppose $\tilde{f}: \mathbb{R} \to \mathbb{R}$ is a continuous extension of $f$.

Consider a sequence $\{x_n\} \subset F$ with $x_n \to x_0$ (exists because $x_0$ is a limit point of $F$). Then
$$
\tilde{f}(x_n) = f(x_n) = \sin\left(\frac{1}{x_n - x_0}\right).
$$
Since $\frac{1}{x_n - x_0} \to \pm\infty$ (depending on the sign of $x_n - x_0$), $\sin\left(\frac{1}{x_n - x_0}\right)$ oscillates and has no limit. This contradicts the continuity of $\tilde{f}$ at $x_0$, which would require $\lim_{n \to \infty} \tilde{f}(x_n)$ to exist.

Therefore, $f$ cannot be extended continuously to $\mathbb{R}$, contradicting the hypothesis. Hence, $F$ must be closed.