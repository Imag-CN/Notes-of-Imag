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

**2.** Take $a=(n^{-p^{-1}})$, then $a$ is in $l^{q}$ but not in $l^{p}$. For any $V$ of $0\in f(l^{p})\subset l^{q}$, we also have some small $\delta>0$ such that $\delta\cdot a$ is in $V$. But $\delta\cdot a$ is not in $f(l^{p})$, thus $f(l^{p})$ is not open in $l^{q}$.

Take $U=B(0,\varepsilon)\subset l^{p}$ for some $\varepsilon>0$, then $0\in f(U)$. Take some $B(0,\varepsilon')\subset V$. Let $b= \dfrac{\varepsilon}{N^{1 /p}}(\underbrace{ 1,1,\dots,1 }_{ N \text{ entries} },0,0\dots)\in l^{p}\subset l^{q}$, then $\lVert b \rVert_{p}=\varepsilon,\lVert b \rVert_{q}=\varepsilon\cdot N^{1/q-1 /p},$ we can take $N$ sufficiently large to make $\lVert b \rVert_{q}=\varepsilon\cdot N^{1/q-1 /p}<\varepsilon'$. Hence, $f(b)\in V \cap f(l^{p})$ but $b \not\in U$. Therefore, $f(U)$ cannot be an intersection of $f(l^{p})$ and some open $V$ in $l^{q}$.

This means the topology on $l^{p}$ is strictly thinner than the subspace topology of $f(l^{p})$.

**3.** Take $a^{(m)}=(n^{-p^{-1}-m^{-1}})\in l^{p}$, $m\in \mathbb{N}^{+}$. Then $f(a^{(m)})\to (n^{-p^{-1}})$ in $l^{q}$ as $m\to \infty$. But $(n^{-p^{-1}})$ is not in $f(l^{p})$, thus $f(l^{p})$ is not closed.

Now we compute the closure of $f(l^{p})$:

**Case 1:** If $q\neq \infty$, then for any $(a_i)\in l^{q}$, we take
$$
a^{(m)}_{i}=\begin{cases}
a_{i}&,i\leq m, \\
0&,i>m.
\end{cases}
$$
Then $(a^{(m)}_{i})\in f(l^{p})$ and $(a^{(m)}_{i})\to (a_{i})$ as $m\to \infty$. So the closure of $f(l^{p})$ is the whole $l^{q}$.

**Case 2:** If $q=\infty$, define
$$
S=\{ (a_{i})\in l^{q}:a_{i}\to 0 \text{ as } i\to \infty\}.
$$
Obviously $f(l^{p})\subset S$.

Conversely, take any $(a_{i})\in S$, we take the same sequence $(a_{i}^{(m)})$ as we defined in case1. Then $(a^{(m)}_{i})\in f(l^{p})$ and $(a^{(m)}_{i})\to (a_{i})$ as $m\to \infty$. So the closure of $f(l^{p})$ is $S$.