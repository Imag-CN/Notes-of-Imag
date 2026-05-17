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