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
___

>[!problem] [SHE] 6E.18
>Suppose $V$ is a normed vector space and $B$ is a subset of $V$ such that
>$$
>\sup_{f \in B} |\varphi(f)| < \infty
>$$
>for every $\varphi \in V'$. Prove that
>$$
>\sup_{f \in B} \|f\| < \infty.
>$$

**Proof:**
For each $f \in V$, define $\hat{f} \in V''$ (the double dual) by $\hat{f}(\varphi) = \varphi(f)$ for all $\varphi \in V'$.The map $f \mapsto \hat{f}$ is an isometric linear embedding: $\|\hat{f}\|_{V''} = \|f\|_V$.

For every $\varphi \in V'$, the given condition says $\sup_{f \in B} |\hat{f}(\varphi)| = \sup_{f \in B} |\varphi(f)| < \infty$. Regard $\{\hat{f} : f \in B\}$ as a family of bounded linear functionals on the Banach space $V'$. By the Uniform Boundedness Principle applied in $V'$, we have
$$
\sup_{f \in B} \|\hat{f}\|_{V''} < \infty.
$$
Since $\|\hat{f}\|_{V''} = \|f\|_V$ for every $f \in B$, it follows that
$$
\sup_{f \in B} \|f\|_V = \sup_{f \in B} \|\hat{f}\|_{V''} < \infty.
$$
___

>[!problem] [SHE] 6E.19
>Suppose $T: V \to W$ is a linear map from a Banach space $V$ to a Banach space $W$ such that
>$$
>\varphi \circ T \in V' \quad \text{for all } \varphi \in W’.
>$$
>Prove that $T$ is a bounded linear map.

**Proof:**
Assume $T$ is not bounded. Then there exist $f_n \in V$ with $\|f_n\|_V=1$ and $\|Tf_n\|_W \to \infty$.

Let $g_n = f_n / \|Tf_n\|_W$. Then $\|g_n\|_V \to 0$, so $g_n \to 0$ in $V$.

For every $\varphi \in W'$, the functional $\varphi \circ T$ belongs to $V'$ (given). Hence
$$
(\varphi \circ T)(g_n) = \frac{\varphi(Tf_n)}{\|Tf_n\|_W} \xrightarrow{n\to\infty} 0.
$$
Thus, for each $\varphi \in W'$, the set $\{\varphi(Tf_n)\}_{n}$ is bounded; otherwise the quotient above would not tend to $0$.

Now consider the family $\{\psi_n\} \subset W''$ defined by $\psi_n(\varphi) = \varphi(Tf_n)$.  
For every $\varphi \in W'$, $\sup_n |\psi_n(\varphi)| < \infty$. By the Uniform Boundedness Principle, we have $\sup_n \|\psi_n\|_{W''} < \infty$. Since the canonical embedding $W \hookrightarrow W''$ is isometric, $\|\psi_n\|_{W''} = \|Tf_n\|_W$. Hence $\sup_n \|Tf_n\|_W < \infty$, contradicting $\|Tf_n\|_W \to \infty$.

Therefore $T$ must be bounded.
___

>[!problem] [SHE] 6E.10
>Give an example of a Banach space $V$, a normed vector space $W$, a bounded linear map $T$ of $V$ onto $W$, and an open subset $G$ of $V$ such that $T(G)$ is not an open subset of $W$.

**Proof:**
Let $V=\{ (x_{i})_{i\in \mathbb{Z}^{+}} : \text{all but finitely many }x_{i}=0 \}$, $\lVert (x_{i})_{i \in \mathbb{Z}^{+}} \rVert_{V}=\operatorname{sup}_{i\in \mathbb{Z}^{+}}|x_{i}|$ ,$W=l^{\infty}$, then $V$ is natur