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

> [!problem] [SHE] 5B.1
>(a) Let $\lambda$ denote Lebesgue measure on $[0,1]$. Show that
> $$\int_{[0,1]}\int_{[0,1]}\frac{x^{2}-y^{2}}{(x^{2}+y^{2})^{2}}\,d\lambda(y)\,d\lambda(x)=\frac{\pi}{4}$$
> and
> $$\int_{[0,1]}\int_{[0,1]}\frac{x^{2}-y^{2}}{(x^{2}+y^{2})^{2}}\,d\lambda(x)\,d\lambda(y)=-\frac{\pi}{4}.$$
>
>(b) Explain why (a) violates neither Tonelli’s Theorem nor Fubini’s Theorem.

**Proof:**
**(a)** Note that
$$
\frac{\partial}{\partial y}\frac{y}{x^2+y^2}=\frac{x^2-y^2}{(x^2+y^2)^2}.
$$

Hence for fixed $x>0$,
$$
\int_0^1\frac{x^2-y^2}{(x^2+y^2)^2}\,dy
=\Bigl[\frac{y}{x^2+y^2}\Bigr]_{y=0}^{y=1}
=\frac{1}{1+x^2}.
$$

Then
$$
\int_0^1\Bigl(\int_0^1\frac{x^2-y^2}{(x^2+y^2)^2}\,dy\Bigr)dx
=\int_0^1\frac{1}{1+x^2}\,dx
=\arctan1-\arctan0=\frac{\pi}{4}.
$$

Similarly, for fixed $y>0$,
$$
\int_0^1\frac{x^2-y^2}{(x^2+y^2)^2}\,dx
=-\int_0^1\frac{y^2-x^2}{(y^2+x^2)^2}\,dx
=-\frac{1}{1+y^2}.
$$

Thus
$$
\int_0^1\Bigl(\int_0^1\frac{x^2-y^2}{(x^2+y^2)^2}\,dx\Bigr)dy
=-\int_0^1\frac{1}{1+y^2}\,dy
=-\frac{\pi}{4}.
$$

**(b)** Tonelli’s Theorem requires a non‑negative integrand; here $f(x,y)$ changes sign, so it does not apply.

Fubini’s Theorem requires absolute integrability. In polar coordinates, $|f(x,y)|=|\cos2\theta|/r^2$ near the origin, and
$$
\iint_{[0,1]^2}|f|\,dx\,dy \ge \int_0^{\delta}\frac{dr}{r}\int_0^{\pi/2}|\cos2\theta|\,d\theta = \infty.
$$

Thus $\iint|f|=\infty$, the hypothesis of Fubini’s Theorem is not satisfied, and the two iterated integrals may differ. Hence (a) contradicts neither theorem.
___

> [!problem] [SHE] 5B.2
>(a) Give an example of a doubly indexed collection $\{x_{m,n}:m,n\in\mathbf{Z}^{+}\}$ of real numbers such that
>$$
>\sum_{m=1}^{\infty}\sum_{n=1}^{\infty}x_{m,n}=0\quad\text{and}\quad\sum_{n=1}^{\infty}\sum_{m=1}^{\infty}x_{m,n}=\infty.
>$$
>
>(b) Explain why (a) violates neither Tonelli’s Theorem nor Fubini’s Theorem.

**Proof:**
**(a)** Define
$$
x_{m,n}=
\begin{cases}
m, & n=m,\\
-m, & n=m+1,\\
0, & \text{otherwise}.
\end{cases}
$$
Then for each $m$, $\sum_{n=1}^{\infty}x_{m,n}=0$, so $\sum_{m}\sum_{n}x_{m,n}=0$.

For fixed $n$, $\sum_{m=1}^{\infty}x_{m,1}=1$, so $\sum_{n=1}^{\infty}\sum_{m=1}^{\infty}x_{m,n}=\infty$.

**(b)** Tonelli’s Theorem applies to non‑negative terms.  Here $x_{m,n}$ takes both positive and negative values, so Tonelli does not apply.

Fubini’s Theorem for sums (i.e., interchanging the order of summation) is valid when $\sum_{m,n}|x_{m,n}|<\infty$, and the example above fails to this condition.
___


