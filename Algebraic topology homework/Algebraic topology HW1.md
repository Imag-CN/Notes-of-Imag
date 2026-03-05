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
**(a) $\Rightarrow$ (b):** Let $f: S^1 \to X$. Given (a), $f \simeq c$ (constant map). Let $H: S^1 \times I \to X$ be the homotopy with $H_0=f, H_1=c$. Define $\tilde{f}: D^2 \to X$ as $\tilde{f}(r\theta) = H(\theta, 1-r)$ for $r \in [0,1], \theta \in S^1$. This extends $f$ because when $r=1$, $\tilde{f}(\theta)=H(\theta, 0)=f(\theta)$.

**(b) $\Rightarrow$ (c):** Let $[f] \in \pi_1(X, x_0)$, represented by a loop $f: S^1 \to X$ with $f(1)=x_0$. By (b), $f$ extends to $F: D^2 \to X$. Define $H: S^1 \times I \to X$ by $H(\theta, t) = F((1-t)\theta + t\cdot 0)$ (radial contraction in $D^2$ to the center $F(0)$). Then $H$ is a path homotopy from $f$ to the constant loop at $F(0)$. Since $f$ is a loop at $x_0$, $H(1, t)=x_0$ for all $t$, forcing $F(0)=x_0$. Thus $[f]=0$.

**(c) $\Rightarrow$ (a):** Let $f: S^1 \to X$. Pick a basepoint $x_0 = f(1)$. Then $f$ represents an element of $\pi_1(X, x_0)=0$, so $f$ is path-homotopic to the constant loop at $x_0$. A path-homotopy is in particular a homotopy (ignoring basepoints), so (a) holds.
___

> [!problem] [HAT] 1.1.10
> From the isomorphism $\pi_1(X \times Y, (x_0, y_0)) \approx \pi_1(X, x_0) \times \pi_1(Y, y_0)$ it follows that loops in $X \times \{y_0\}$ and $\{x_0\} \times Y$ represent commuting elements of $\pi_1(X \times Y, (x_0, y_0))$. Construct an explicit homotopy demonstrating this.

