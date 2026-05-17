___

> [!problem]
> Prove the claim in Example 157 in the lecture notes.

**Proof**:
Construct a singular 2-chain $c$ as follows. Let $c$ be a singular 2-simplex that fills the annular region between $\sigma^2$ and $\tau$ in $V$.

Since $V$ is contractible and $\sigma^2$, $\tau$ are two paths in $V$ with same endpoints, they are homotopic relative to endpoints. Let $H: \Delta^1 \times I \to V$ be a homotopy with $H(\cdot,0)=\sigma^2$, $H(\cdot,1)=\tau$.

This homotopy gives a $2$-chain $c_1$ with $\partial c_1 = \sigma^2 - \tau$.

For $\sigma$ and $s$, consider a singular 2-simplex $c_2: \Delta^2 \to S^1$ where:
- $c_2$ maps one edge to $\sigma$ (from $e^{i(\alpha_0-\delta)}$ to $e^{i(\alpha_0+\delta)}$)
- $c_2$ maps the opposite edge to $s$ (from $e^{i(\alpha_0+\delta)}$ to $e^{i(\alpha_0-\delta)}$)
- $c_2$ collapses the third edge to a point

Then $\partial c_2 = \sigma - s$.

Take $c = c_1 - c_2$. Then:
$\partial c = \partial c_1 - \partial c_2 = (\sigma^2 - \tau) - (\sigma - s) = \sigma^2 - \sigma + s - \tau$

Thus $\sigma^2 - \sigma + s - \tau$ is a 1-boundary.
___

> [!problem]
> Given a CW complex $X$. Prove that $X^m$ is a closed subset of $X$ for all integers $m$. Prove that for every singular chain $c$ for $X$ there is a positive integer $m$ such that $c$ is a singular chain of $X^m$.


**Proof**:
1. **$X^m$ is closed in $X$ for all $m$**:
Each $m$-skeleton $X^m$ is constructed inductively as a quotient space of $X^{m-1} \sqcup (\bigsqcup D_\alpha^m)$ under characteristic maps $\Phi_\alpha: \partial D_\alpha^m \to X^{m-1}$. By the definition of CW topology, a subset $A \subseteq X$ is closed if and only if $A \cap \overline{e}$ is closed in $\overline{e}$ for each cell $e$. For any cell $e^n$ of dimension $n > m$, we have $\overline{e} \cap X^m = \Phi(\partial D^n)$, which is compact and thus closed in $\overline{e}$. For cells of dimension $\leq m$, $\overline{e} \cap X^m = \overline{e}$, which is closed.

Therefore, $X^m$ is closed in $X$.

2. **Every singular chain $c$ is a chain of some $X^m$**:
 Let $c = \sum_{i=1}^k n_i \sigma_i$ be a singular $p$-chain, where each $\sigma_i: \Delta^p \to X$ is a singular simplex.

Each $\sigma_i(\Delta^p)$ is a compact subset of $X$. By the closure-finite property of CW complexes, a compact set intersects only finitely many cells.

Let $m_i$ be the maximum dimension of cells intersecting $\sigma_i(\Delta^p)$. Set $m = \max\{m_1, \ldots, m_k, p\}$.

Since $X^m$ contains all cells of dimension $\leq m$, and $\sigma_i(\Delta^p)$ is contained in the union of cells it intersects (all of dimension $\leq m_i \leq m$), we have $\sigma_i(\Delta^p) \subseteq X^m$.

Therefore, each $\sigma_i$ is a singular simplex of $X^m$, and $c$ is a singular chain of $X^m$.
___

> [!problem] [HAT] 2.2.2
> Given a map $f: S^{2n} \to S^{2n}$, show that there is some point $x \in S^{2n}$ with either $f(x)=x$ or $f(x)=-x$. Deduce that every map $\mathbb{R}P^{2n} \to \mathbb{R}P^{2n}$ has a fixed point. Construct maps $\mathbb{R}P^{2n-1} \to \mathbb{R}P^{2n-1}$ without fixed points from linear transformations $\mathbb{R}^{2n} \to \mathbb{R}^{2n}$ without eigenvectors.

**Proof:**
For $f: S^{2n} \to S^{2n}$, consider the antipodal map $a(x) = -x$. If $f(x) \neq x$ for all $x$, then $f$ is homotopic to $a$ via $f_t(x) = (1-t)f(x) - tx$. This homotopy is valid since $f(x) \neq -x$ for all $x$.

If $f$ is homotopic to $a$, then $\deg f = \deg a = (-1)^{2n+1} = -1$. But if $f(x) \neq -x$ for all $x$, then $f$ is homotopic to identity via $f_t(x) = (1-t)f(x) + tx$, giving $\deg f = 1$.

Since these degrees differ, at least one of the conditions must fail, so there exists $x$ with $f(x)=x$ or $f(x)=-x$.

For $\mathbb{R}P^{2n} \to \mathbb{R}P^{2n}$, any map $g$ lifts to $f: S^{2n} \to S^{2n}$ with $f(-x) = \pm f(x)$. By above, $\exists x$ with $f(x)=x$ or $f(x)=-x$.

If $f(x)=x$, then $g([x]) = [x]$. If $f(x)=-x$, then $g([x]) = [x]$ too. So $g$ has fixed point.

For $\mathbb{R}P^{2n-1} \to \mathbb{R}P^{2n-1}$, take linear $A: \mathbb{R}^{2n} \to \mathbb{R}^{2n}$ with $A = \text{diag}(R, \dots, R)$ where $R = \begin{pmatrix}0&-1\\1&0\end{pmatrix}$. $A$ has no real eigenvectors (only complex eigenvalues $\pm i$), so the induced map on $\mathbb{R}P^{2n-1}$ has no fixed points.
___

> [!problem] [HAT] 2.2.4
> Construct a surjective map $S^n \to S^n$ of degree zero, for each $n \geq 1$.

**Proof:**
For $n=1$, define $f: S^1 \to S^1$ by $f(e^{2\pi i t}) = e^{4\pi i t}$ for $t \in [0, 1/2]$ and $f(e^{2\pi i t}) = e^{4\pi i (2-2t)}$ for $t \in [1/2, 1]$.

Geometrically: wrap first half-circle once positively, second half-circle once negatively.

$f$ is clearly surjective. $\deg f = 0$ since it is homotopic to a constant map via a straight-line homotopy in $\mathbb{C}$.

For $n \geq 2$, take the $(n-1)$-fold suspension $\Sigma^{n-1} f: S^n \to S^n$. Suspension preserves surjectivity and the degree of mapping.
___

> [!problem] [HAT] 2.2.11
> In an exercise for 1.2 we described a $3$-dimensional CW complex obtained from the cube $I^3$ by identifying opposite faces via a one-quarter twist. Compute the homology groups of this complex.

