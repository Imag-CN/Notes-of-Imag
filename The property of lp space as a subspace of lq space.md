___

>[!problem]
>For $1\leq p < q\leq \infty$, it is obvious that $l^{p}$ space is a subspace of $l^{q}$ space. Consider the inclusion map: $f: l^{p}\to l^{q}$. Then
>
>1. $f$ is continous; 
>2. $f(l^{p})$ is not open in $l^{q}$. What's more, there exists an open $U\in l^{p}$ such that $f(U)$ is not an intersection of $f(l^{p})$ and some open $V$ in $l^{q}$;
>3. $f(l^{p})$ is not closed in $l^{q}$. Furthermore, compute the closure of $f(l^{p})$.

**Proof:**
**1.** By norm inequality, for any $a\in l^{p}$, we have $\lVert f(a) \rVert_{q}\leq \lVert a \rVert_{p}$, so $f$ is bounded, thus continuous.

This means the topology on $l^{p}$ is thinner than the subspace topology of $f(l^{p})$.

**2.** Take $a=(n^{-p^{-1}})$, then $a$ is in $l^{q}$ but not in $l^{p}$. Take $U=B(0,\varepsilon)\subset l^{p}$ for some $\varepsilon>0$, then $0\in f(U)$. For any neighborhood $V$ of $0\in f(l^{p})\subset l^{q}$, we also have some small $\delta>0$ such that $\delta\cdot a$ is in $V$. But $\delta\cdot a$ is not in $f(l^{p})$, thus $f(l^{p})$ is not open in $l^{q}$, and $f(U)$.

**3.** Take $a^{(m)}=(n^{-p^{-1}-m^{-1}})\in l^{p}$, $m\in \mathbb{N}^{+}$. Then $f(a^{(m)})\to (n^{-p^{-1}})$ in $l^{q}$ as $m\to \infty$. But $(n^{-p^{-1}})$ is not in $f(l^{p})$, thus $f(l^{p})$ is not closed.

**4.** Take a 