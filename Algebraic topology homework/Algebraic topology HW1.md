___

> [!problem] [HAT] 1.1.1
> Show that composition of paths satisfies the following cancellation property: If $f_0 \cdot g_0 \simeq f_1 \cdot g_1$ and $g_0 \simeq g_1$ then $f_0 \simeq f_1$.

**Proof:**
Let $H$ be a homotopy between $f_0 \cdot g_0$ and $f_1 \cdot g_1$, and $G$ be a homotopy between $g_0$ and $g_1$.

Define a homotopy $F: I \times I \to X$ from $f_0$ to $f_1$ by:
$$
F(s, t) =
\begin{cases}
H(2s, t), & 0 \le s \le \frac{1}{2} \\
G(2-2s, t), & \frac{1}{2} \le s \le 1
\end{cases}
$$

Check: $F(s, 0) = f_0(s)$ and $F(s, 1) = f_1(s)$. Continuity follows from the gluing lemma and conditions at $s=1/2$: $H(1, t) = g_0(t) = G(0, t)$.

Thus, $f_0 \simeq f_1$.
___

> [!problem] [HAT] 1.1.5
> Show that for a space $X$, the following three conditions are equivalent:
> 
> (a) Every map $S^1 \to X$ is homotopic to a constant map, with image a point.
> (b) Every map $S^1 \to X$ extends to a map $D^2 \to X$.
> (c) $\pi_1(X, x_0) = 0$ for all $x_0 \in X$.
> 
> Deduce that a space $X$ is simply-connected iff all maps $S^1 \to X$ are homotopic.

**Proof:**
We show that (a) $\implies$ (b) $\implies$ (c) $\implies$ (a).

**(a) $\implies$ (b):** Given $f: S^1 \to X$, let $H: S^1 \times I \to X$ be a homotopy with $H_0 = f$, $H_1 = \text{const}_{x_0}$. Define $F: D^2 \to X$ by $F(re^{2\pi i t}) = H(e^{2\pi i t}, 1-r)$. This extends $f$.

**(b) $\implies$ (c):** Given $f_{1},f_{2}: S^1 \to X$ with base point $x_{0}$ and with extension
