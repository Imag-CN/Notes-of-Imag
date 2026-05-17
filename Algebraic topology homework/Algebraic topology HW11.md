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


