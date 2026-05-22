___

>[!problem] Topology
>For $1\leq p < q\leq \infty$, it is obvious that $l^{p}$ space is a subspace of $l^{q}$ space. Consider the inclusion map: $f: l^{p}\to l^{q}$. Then
>
>1. $f$ is continous; 
>2. $f(l^{p})$ is not open in $l^{q}$;
>3. $f(l^{p})$ is not closed in $l^{q}$;
>4. There exists some open $U\in$

**Proof:**
**1.** By norm inequality, for any $a\in l^{p}$, we have $\lVert f(a) \rVert_{q}\leq \lVert a \rVert_{p}$, so $f$ is bounded, thus continuous.

**2.** Take $a=(n^{-p^{-1}})$, then $a$ is in $l^{q}$ but not in $l^{p}$. For any neighborhood $U$ of $0\in f(l^{p})\subset l^{q}$, we also have some small $\varepsilon>0$ such that $\varepsilon\cdot a$ is in $U$. But $\varepsilon\cdot a$ is not in $f(l^{p})$, thus $f(l^{p})$ is not open in $l^{q}$.

**3.** Take $a^{(m)}=(n^{-p^{-1}-m^{-1}})\in l^{p}$, $m\in \mathbb{N}^{+}$. Then $f(a^{(m)})\to (n^{-p^{-1}})$ in $l^{q}$ as $m\to \infty$. But $(n^{-p^{-1}})$ is not in $f(l^{p})$, thus $f(l^{p})$ is not closed.

