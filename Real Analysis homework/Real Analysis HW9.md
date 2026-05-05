___

>[!problem] [SHE] 4B.7
>Give an example of a Borel subset of $\mathbb{R}$ whose density at $0$ is not defined.

**Proof:**
Let $E=\bigcup_{k=1}^{\infty}(2^{-2k+1},2^{-2k+2})$, then $\dfrac{\lvert E \cap (-2^{-k},2^{-k})\rvert}{\lvert (-2^{-k},2^{-k}) \rvert}=\begin{cases} \dfrac{1}{3} & \text{, if }k \text{ even,}\\ \dfrac{1}{6}&\text{, if }k\text{ odd.}\end{cases}$. Thus density of $E$ at $0$ is not defined.
___

>[!problem] [SHE] 4B.9
>Prove that if $t\in[0,1]$, then there exists a Borel set $E\subset\mathbb{R}$ such that the density of $E$ at 0 is $t$.

**Proof:**
Pick $r_n=1/2^n$, $I_n=(r_{n+1},r_n]$. Choose $A_n\subset I_n$ with $m(A_n)=t\cdot m(I_n)$. Define
$$
E=\bigcup_{n\ge1}(A_n\cup(-A_n)).
$$
Then $E$ is Borel and symmetric. For $r\in(r_{n+1},r_n]$,
$$
\frac{m(E\cap(-r,r))}{2r}
=\frac{2\sum_{k\ge n}t\cdot m(I_k)}{2r}
=t\cdot\frac{r_n}{r}.
$$
Since $r_n/r\to1$ as $r\to0^+$, the density at $0$ is $t$.