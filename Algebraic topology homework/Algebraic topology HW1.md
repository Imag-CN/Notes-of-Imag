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

**Proof:**
Define $H: I \times I \to X \times Y$ by
$$
H(t, s) =
\begin{cases}
(\alpha(2t), y_0), & 0 \le t \le s/2 \\
(\alpha(s), \beta(2t - s)), & s/2 \le t \le (1+s)/2 \\
(x_0, \beta(2t - 1)), & (1+s)/2 \le t \le 1
\end{cases}
$$

Check:
- $H(t, 0) = (x_0, \beta(2t))$ for $t \in [0,1/2]$, and $(x_0, \beta(2t-1))$ for $t \in [1/2,1]$, which is exactly $B \cdot A$.
- $H(t, 1) = (\alpha(2t), y_0)$ for $t \in [0,1/2]$, and $(x_0, \beta(2t-1))$ for $t \in [1/2,1]$, which is exactly $A \cdot B$.
- $H(0,s)=(\alpha(0), y_0)=(x_0, y_0)$, $H(1,s)=(x_0, \beta(1))=(x_0, y_0)$ for all $s$.
- The pieces match at the gluing $t=s/2$ and $t=(1+s)/2$.

Thus $H$ is a path-homotopy from $B \cdot A$ to $A \cdot B$, showing they commute in $\pi_1$.
___

> [!problem] [HAT] 1.1.20
> For a homotopy $f_t: X \to X$ of a space $X$ with $f_0 = f_1 = \operatorname{id}_X$, show that for a basepoint $x_0 \in X$, the loop $t \mapsto f_t(x_0)$ represents an element of the center of $\pi_1(X, x_0)$.

**Proof:**
Define the loop $\alpha(t) = f_t(x_0)$ at $x_0$.
We must show $[\alpha]$ is in the center of $\pi_1(X, x_0)$, i.e., $[\alpha] \cdot [\gamma] = [\gamma] \cdot [\alpha]$ for all $[\gamma] \in \pi_1(X, x_0)$.

Consider the homotopy $H: I \times I \to X$ defined by
$$H(s, t) = f_t(\gamma(s)),$$
where $\gamma$ is a loop at $x_0$.
Then $H(0, t) = f_t(x_0) = \alpha(t)$ and $H(1, t) = f_t(x_0) = \alpha(t)$.
Also, $H(s, 0) = \gamma(s)$ and $H(s, 1) = \gamma(s)$.

Define a new homotopy $G: I \times I \to X$ by
$$G(s, t) =
\begin{cases}
\gamma(2s), & 0 \le s \le \frac{1}{2}, \\
H(2s-1, 2t), & \frac{1}{2} \le s \le 1, 0 \le t \le \frac{1}{2}, \\
H(2-2s, 2t-1), & \frac{1}{2} \le s \le 1, \frac{1}{2} \le t \le 1, \\
\gamma(2-2s), & \frac{1}{2} \le s \le 1, t=1.
\end{cases}$$
Carefully checking the boundary shows that $G$ is a homotopy from $\alpha \cdot \gamma$ to $\gamma \cdot \alpha$.
Equivalently, apply the homotopy extension property or Lemma 1.19 from Hatcher, which states that for a homotopy $f_t$,
$$[f_1 \circ \gamma] = [\alpha]^{-1} \cdot [f_0 \circ \gamma] \cdot [\alpha].$$
Since $f_0 = f_1 = \operatorname{id}_X$, we get $[\gamma] = [\alpha]^{-1} \cdot [\gamma] \cdot [\alpha]$, i.e., $[\alpha] \cdot [\gamma] = [\gamma] \cdot [\alpha]$.
Thus $[\alpha]$ is central in $\pi_1(X, x_0)$.