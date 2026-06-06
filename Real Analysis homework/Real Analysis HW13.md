___

>[!problem] [SHE] 6E.1
>Suppose $U$ is a subset of a metric space $V$. Show that $U$ is dense in $V$ if and only if every nonempty open subset of $V$ contains at least one element of $U$.

**Proof:**
$(\Rightarrow)$ Assume $\overline{U}=V$. Let $O$ be any nonempty open subset of $V$. If $O \cap U = \varnothing$, then $O \subset V \setminus U \subset V \setminus \overline{U}$. But $V \setminus \overline{U} = \varnothing$ since $\overline{U}=V$, contradicting that $O$ is nonempty. Therefore, $O \cap U \neq \varnothing$.

$(\Leftarrow)$ Assume every nonempty open subset of $V$ contains at least one point of $U$. For any $x \in V$ and any $\varepsilon > 0$, the open ball $B(x, \varepsilon)$ is a nonempty open subset. By assumption, $B(x, \varepsilon) \cap U \neq \varnothing$. Hence, $x$ is a limit point of $U$ (or $x \in U$ itself), so $x \in \overline{U}$. Since $x$ was arbitrary, $V \subset \overline{U}$, implying $\overline{U}=V$. Thus, $U$ is dense in $V$.
___

>[!problem] [SHE] 6E.8
>Suppose $(X,d)$ is a complete metric space and $G_1, G_2, \ldots$ is a sequence of dense open subsets of $X$. Prove that $\bigcap_{k=1}^{\infty} G_k$ is a dense subset of $X$.

**Proof:**
Take any nonempty open subset $U\subset X$, then $X\cap G_{k},k\in \mathbb{Z}^{+}$ is an open set and dense in $X$. By Baire's theorem, $X\cap\bigcap_{k=1}^{\infty} G_k=\bigcap_{k=1}^{\infty} (G_k\cap X)$ is nonempty, i.e. $\bigcap_{k=1}^{\infty} G_k$ contains at least one element of $U$. By exercise 6E.1, $\bigcap_{k=1}^{\infty} G_k$ is dense in $X$.
___

>[!problem] [SHE] 6E.17
>Suppose $V$ is a Banach space, $W$ is a normed vector space, and $T_1, T_2, \ldots$ is a sequence of bounded linear maps from $V$ to $W$ such that
>$$
>\lim_{k \to \infty} T_k f \text{ exists for each } f \in V.
>$$
>Define $T: V \to W$ by
>$$
>Tf = \lim_{k \to \infty} T_k f
>$$
>for $f \in V$. Prove that $T$ is a bounded linear map from $V$ to $W$.

**Proof:**
**Linearity:** For any $f, g \in V$ and $\alpha, \beta \in \mathbb{C}$ (or $\mathbb{R}$), we have
$$
 T(\alpha f + \beta g) = \lim_{k \to \infty} T_k(\alpha f + \beta g) = \lim_{k \to \infty} \big( \alpha T_k f + \beta T_k g \big) = \alpha \lim_{k \to \infty} T_k f + \beta \lim_{k \to \infty} T_k g = \alpha T f + \beta T g,
$$
where the second equality uses the linearity of each $T_k$, and the third uses the linearity of the limit in the normed space $W$. Hence $T$ is linear.

**Boundedness:** For each $f \in V$, the sequence $\{T_k f\}$ converges in $W$, hence it is bounded: $\sup_k \|T_k f\|_W < \infty$. Since $V$ is a Banach space, the Uniform Boundedness Principle implies that
$$
\sup_{k} \|T_k\|_{\mathcal{L}(V,W)} < \infty.
$$
Let $C := \sup_k \|T_k\|$. Then for every $f \in V$ and every $k$,
$$
\|T_k f\|_W \le C \|f\|_V.
$$
Taking the limit as $k \to \infty$ preserves the inequality, so
$$
\|T f\|_W = \big\|\lim_{k\to\infty} T_k f\big\|_W = \lim_{k\to\infty} \|T_k f\|_W \le C \|f\|_V.
$$
Hence $T$ is bounded with $\|T\| \le C$.

Therefore, $T$ is a bounded linear map from $V$ to $W$.