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

