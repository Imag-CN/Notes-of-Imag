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

> [!problem] [SHE] 5B.4
> Suppose $(X,\mathcal{S})$ is a measurable space and $f:X\to\mathbf{R}$ is a function. Let $\operatorname{graph}(f)\subset X\times\mathbf{R}$ denote the graph of $f$:
> $$\operatorname{graph}(f)=\{(x,f(x)):x\in X\}.$$
> Let $\mathcal{B}$ denote the $\sigma$-algebra of Borel subsets of $\mathbf{R}$. Prove that $\operatorname{graph}(f)\in\mathcal{S}\otimes\mathcal{B}$ if and only if $f$ is an $\mathcal{S}$-measurable function.

**Proof:**
$(\Rightarrow)$ Assume $\operatorname{graph}(f)\in\mathcal{S}\otimes\mathcal{B}$. For $a\in\mathbf{R}$, the section
$$
\{x\in X:(x,a)\in\operatorname{graph}(f)\}=\{x:f(x)=a\}
$$
is in $\mathcal{S}$ because sections of product-measurable sets are measurable. Then
$$
\{x:f(x)<a\}=\bigcup_{q<a,q\in\mathbb{Q}}\{x:f(x)=q\}\in\mathcal{S}.
$$
Thus $f$ is $\mathcal{S}$-measurable.

$(\Leftarrow)$ Assume $f$ is $\mathcal{S}$-measurable. Define $F:X\times\mathbf{R}\to\mathbf{R}$ by $F(x,y)=f(x)-y$. Then $F$ is $(\mathcal{S}\otimes\mathcal{B},\mathcal{B})$-measurable, and
$$
\operatorname{graph}(f)=F^{-1}(\{0\})\in\mathcal{S}\otimes\mathcal{B}.
$$
___

> [!problem] [SHE] 5C.6
> Suppose $\lambda$ denotes Lebesgue measure on $(\mathbf{R},\mathcal{L})$, where $\mathcal{L}$ is the $\sigma$-algebra of Lebesgue measurable subsets of $\mathbf{R}$. Show that there exist subsets $E$ and $F$ of $\mathbf{R}^{2}$ such that
> - $F\in\mathcal{L}\otimes\mathcal{L}$ and $(\lambda\times\lambda)(F)=0$;
> - $E\subset F$ but $E\notin\mathcal{L}\otimes\mathcal{L}$.

**Proof:**
Let $V$ be a Vitali set in $\mathbf{R}$, i.e., $V\subset[0,1]$ is not Lebesgue measurable. Define
$$
F=[0,1]\times\{0\}\subset\mathbf{R}^2.
$$
Then $F\in\mathcal{L}\otimes\mathcal{L}$ (since $[0,1]\in\mathcal{L}$ and $\{0\}\in\mathcal{L}$) and
$$
(\lambda\times\lambda)(F)=\lambda([0,1])\cdot\lambda(\{0\})=1\cdot0=0.
$$
Now take
$$
E=V\times\{0\}\subset F.
$$
If $E\in\mathcal{L}\otimes\mathcal{L}$, then its section
$$
E_0=\{x\in\mathbf{R}:(x,0)\in E\}=V
$$
would belong to $\mathcal{L}$ (because sections of a measurable set in the product $\sigma$-algebra are measurable). But $V\notin\mathcal{L}$ by construction. Hence $E\notin\mathcal{L}\otimes\mathcal{L}$.

Thus $E$ and $F$ satisfy the required conditions.
___


