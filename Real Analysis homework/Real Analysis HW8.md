___

> [!problem] [SHE] 3B.10
>(a) Suppose $(X,\mathcal{S},\mu)$ is a measure space such that $\mu(X)<\infty$. Suppose $p,r$ are positive numbers with $p<r$. Prove that if $f:X\to[0,\infty)$ is an $\mathcal{S}$-measurable function such that $\int f^{r}\,d\mu<\infty$, then $\int f^{p}\,d\mu<\infty$.
>
>(b) Give an example to show that the result in part (a) can be false without the hypothesis that $\mu(X)<\infty$.

**Proof:**
**(a)** Since $\mu(X)<\infty$, we can write $X=A\cup B$ where $A=\{x\in X:f(x)\leq1\}$ and $B=\{x\in X:f(x)>1\}$.

On $A$, we have $f^p\leq1$, so $\int_A f^p\,d\mu\leq\mu(A)\leq\mu(X)<\infty$.

On $B$, we have $f^p\leq f^r$ because $f>1$ and $p<r$. Thus $\int_B f^p\,d\mu\leq\int_B f^r\,d\mu\leq\int_X f^r\,d\mu<\infty$.

Combining both parts, $\int_X f^p\,d\mu=\int_A f^p\,d\mu+\int_B f^p\,d\mu<\infty$.

**(b)** Take $X=[1,+\infty)$, $p=1$, $r=2$, and define
$$
f(x)=\frac{1}{x}.
$$
Then
$$
\int_1^\infty f^2(x)\,dx=\int_1^\infty\frac{1}{x^2}\,dx=1<\infty,
$$
but
$$\int_1^\infty f(x)\,dx=\int_1^\infty\frac{1}{x}\,dx=\infty.$$
___

