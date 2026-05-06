___

>[!problem] [SHE] 4B.7
>Give an example of a Borel subset of $\mathbb{R}$ whose density at $0$ is not defined.

**Proof:**
Let $E=\bigcup_{k=1}^{\infty}(2^{-2k+1},2^{-2k+2})$, then $\dfrac{\lvert E \cap (-2^{-k},2^{-k})\rvert}{\lvert (-2^{-k},2^{-k}) \rvert}=\begin{cases} \dfrac{1}{3} & \text{, if }k \text{ even,}\\ \dfrac{1}{6}&\text{, if }k\text{ odd.}\end{cases}$. Thus density of $E$ at $0$ is not defined.
___

>[!problem] [SHE] 4B.9
>Prove that if $t\in[0,1]$, then there exists a Borel set $E\subset\mathbb{R}$ such that the density of $E$ at 0 is $t$.

**Proof:**
Let $A_{n}=( (n+1)^{-1}, (n+1)^{-1}+t(n^{-1}-(n+1)^{-1}))$, and let
$$
E=\bigcup_{n\ge1}(A_n\cup(-A_n)).
$$
Then $E$ is Borel and symmetric. For $r\in((n+1)^{-1},n^{-1}]$,
$$
\frac{m(E\cap(-r,r))}{2r}
=\frac{2((n+1)^{-1}t+m(E\cap(r,n^{-1}]))}{2r}
\leq t\cdot \dfrac{(n+1)^{-1}}{r} + \dfrac{n^{-1}-r}{r}.
$$
Since $(n+1)^{-1}/r\to1$ and $(n^{-1}-r ) / r \to 0$ as $r\to0^+$, the density at $0$ is $t$.