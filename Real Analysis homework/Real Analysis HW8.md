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

> [!problem]
> Let $A$, $B$ be Lebesgue measurable subsets of $\mathbb{R}$. Denote
> $$
> A_x=\{a-x:a\in A\}.
> $$
> Prove that
> $$
> \int_{\mathbb{R}}\lambda(A_x\cap B)\,d\lambda=\lambda(A)\lambda(B).
> $$

**Proof:**
Write the characteristic functions:
$$
\chi_{A_x}(y)=\chi_A(y+x),\qquad \chi_B(y)=\text{characteristic function of }B.
$$
Then
$$
\lambda(A_x\cap B)=\int_{\mathbb{R}}\chi_{A_x}(y)\chi_B(y)\,d\lambda(y)=\int_{\mathbb{R}}\chi_A(y+x)\chi_B(y)\,dy.
$$
Thus
$$
\int_{\mathbb{R}}\lambda(A_x\cap B)\,dx
=\int_{\mathbb{R}}\Bigl[\int_{\mathbb{R}}\chi_A(y+x)\chi_B(y)\,dy\Bigr]dx.
$$
By Tonelli’s theorem, we may interchange the order of integration:
$$
=\int_{\mathbb{R}}\chi_B(y)\Bigl[\int_{\mathbb{R}}\chi_A(y+x)\,dx\Bigr]dy.
$$
The inner integral is independent of $y$: for fixed $y$,
$$
\int_{\mathbb{R}}\chi_A(y+x)\,dx=\int_{\mathbb{R}}\chi_A(z)\,dz=\lambda(A).
$$
Therefore
$$
\int_{\mathbb{R}}\lambda(A_x\cap B)\,dx
=\int_{\mathbb{R}}\chi_B(y)\lambda(A)\,dy
=\lambda(A)\int_{\mathbb{R}}\chi_B(y)\,dy
=\lambda(A)\lambda(B).
$$
___

> [!problem] [SHE] 4A.8
> Find a formula for the Hardy–Littlewood maximal function of the function $h:\mathbb{R}\to[0,\infty)$ defined by
> $$h(x)=
> \begin{cases}
> x, & \text{if }0\leq x\leq1,\\
> 0, & \text{otherwise}.
> \end{cases}$$

**Proof:**
Since $h$ is supported on $[0,1]$ and $h(y)=y$ on $[0,1]$, we compute case by case.

1. $x\le0$: The best average is obtained as $t\to\infty$, giving $h^{*}(x)=\frac14$.

2. $0<x\le\frac12$: The maximum occurs at $t=1-x$, giving $h^{*}(x)=\frac{1}{4(1-x)}$.

3. $\frac12\le x\le1$: The maximum occurs at $t=x$, giving $h^{*}(x)=x$.

4. $x>1$: The maximum occurs at $t=\sqrt{x^2-1}$, giving $h^{*}(x)=\frac{1}{2\bigl(x+\sqrt{x^2-1}\bigr)}$.

Hence
$$
h^{*}(x)=
\begin{cases}
\frac14, & x\le0,\\[4pt]
\frac{1}{4(1-x)}, & 0<x\le\frac12,\\[4pt]
x, & \frac12\le x\le1,\\[4pt]
\displaystyle\frac{1}{2\bigl(x+\sqrt{x^2-1}\bigr)}, & x>1.
\end{cases}
$$
___

> [!problem] [SHE] 4A.10
> Prove or give a counterexample: If $h:\mathbb{R}\to[0,\infty)$ is an increasing function, then $h^*$ (the Hardy–Littlewood maximal function) is an increasing function.

**Proof:**
Let $h:\mathbb{R}\to[0,\infty)$ be increasing. For any $b\in\mathbb{R}$ and $t>0$, define the average
$$
A(b,t)=\frac{1}{2t}\int_{b-t}^{b+t}h(y)\,dy.
$$
Then the Hardy–Littlewood maximal function is
$$
h^*(b)=\sup_{t>0}A(b,t).
$$

Fix $x_1<x_2$. We will show $h^*(x_1)\le h^*(x_2)$.

For any $t>0$, consider the intervals $I_1=[x_1-t,x_1+t]$ and $I_2=[x_2-t,x_2+t]$. Because $h$ is increasing, shifting the interval to the right increases the function values: for any $y\in I_1$, the point $y+(x_2-x_1)\in I_2$ satisfies $h(y)\le h(y+(x_2-x_1))$. By a change of variables or by the monotonicity of integrals over shifted intervals, we get
$$
A(x_1,t)\le A(x_2,t).
$$
Taking supremum over $t>0$ on both sides yields
$$
h^*(x_1)=\sup_{t>0}A(x_1,t)\le\sup_{t>0}A(x_2,t)=h^*(x_2).
$$
Hence $h^*$ is increasing.
___

> [!problem] [SHE] 4A.13
> Show that there exists $h\in\mathcal{L}^{1}(\mathbf{R})$ such that $h^{*}(b)=\infty$ for every $b\in\mathbf{Q}$.

**Proof:**
Enumerate $\mathbb{Q}=\{q_n\}_{n=1}^\infty$. Choose intervals $I_n$ with $q_n\in I_n$ and $|I_n|=2^{-n}$.

Define
$$
h(x)=\sum_{n=1}^{\infty}\frac{n^{-2}}{2^{-n}\log(1+n)}\chi_{I_n}(x).
$$

Then
$$
\|h\|_1=\sum_{n=1}^\infty\frac{n^{-2}}{\log(1+n)}<\infty,
$$
so $h\in L^1(\mathbb{R})$.

For any $q_k\in\mathbb{Q}$ and any $r>0$, there are infinitely many $n$ with $I_n\subset(q_k-r,q_k+r)$. For such $n$,
$$
\frac{1}{2r}\int_{q_k-r}^{q_k+r}h\ge\frac{1}{2r}\int_{I_n}h
=\frac{1}{2r}\cdot\frac{n^{-2}}{\log(1+n)}.
$$
Taking $r\to0^+$ appropriately, the right-hand side can be made arbitrarily large. Hence
$$
h^*(q_k)=\sup_{r>0}\frac{1}{2r}\int_{q_k-r}^{q_k+r}h=\infty
$$
for every $k$.
___
 For $f\in\mathcal{L}^{1}(\mathbb{R})$ and $I$ an interval of $\mathbb{R}$ with $0<|I|<\infty$, let $f_I$ denote the average of $f$ on $I$. In other words, $f_I=\frac{1}{|I|}\int_I f$.
 
> [!problem] [SHE] 4B.1
> Suppose $f\in\mathcal{L}^{1}(\mathbb{R})$. Prove that
> $$
> \lim_{t\downarrow0}\frac{1}{2t}\int_{b-t}^{b+t}\left|f-f_{[b-t,b+t]}\right|=0
> $$
> for almost every $b\in\mathbb{R}$.

**Proof:**
Define $F(x)=\int_0^x f(y)dy$. By the Lebesgue differentiation theorem, for almost every $b$,
$$
\lim_{t\to0}\frac{F(b+t)-F(b-t)}{2t}=f(b).
$$
Hence for a.e. $b$,
$$
\lim_{t\to0}f_{[b-t,b+t]}=\lim_{t\to0}\frac{F(b+t)-F(b-t)}{2t}=f(b).
$$

Now fix such a $b$ and let $\varepsilon>0$. Choose $t_0>0$ such that for all $0<t<t_0$,
$$
|f_{[b-t,b+t]}-f(b)|<\varepsilon.
$$
Then
$$
\begin{align*}
\frac{1}{2t}\int_{b-t}^{b+t}|f-f_{[b-t,b+t]}|dx
&\le\frac{1}{2t}\int_{b-t}^{b+t}|f-f(b)|dx
   +\frac{1}{2t}\int_{b-t}^{b+t}|f(b)-f_{[b-t,b+t]}|dx \\
&<\frac{1}{2t}\int_{b-t}^{b+t}|f-f(b)|dx+\varepsilon.
\end{align*}
$$
By the Lebesgue differentiation theorem again,
$$
\lim_{t\downarrow0}\frac{1}{2t}\int_{b-t}^{b+t}|f-f(b)|dx=0
$$
for a.e. $b$. Therefore
$$
\limsup_{t\downarrow0}\frac{1}{2t}\int_{b-t}^{b+t}|f-f_{[b-t,b+t]}|dx\le\varepsilon
$$
for a.e. $b$. Since $\varepsilon>0$ is arbitrary, the limit equals $0$ for a.e. $b$.
___

> [!problem] [SHE] 4B.3
> Suppose $f:\mathbb{R}\to\mathbb{R}$ is a Lebesgue measurable function such that $f^2\in\mathcal{L}^1(\mathbb{R})$. Prove that
> $$\lim_{t\downarrow0}\frac{1}{2t}\int_{b-t}^{b+t}|f-f(b)|^2=0$$
> for almost every $b\in\mathbb{R}$.

**Proof:**
Let $g=f^2\in L^1(\mathbb{R})$. By Lebesgue differentiation,
$$
\lim_{t\downarrow0}\frac{1}{2t}\int_{b-t}^{b+t}f(x)^2\,dx=f(b)^2
$$
for a.e. $b$. Also, since $f\in L^2_{\text{loc}}$, we have $f\in L^1_{\text{loc}}$, so
$$
\lim_{t\downarrow0}\frac{1}{2t}\int_{b-t}^{b+t}f(x)\,dx=f(b)
$$
for a.e. $b$.

Now expand the square:
$$
\frac{1}{2t}\int_{b-t}^{b+t}|f-f(b)|^2
=\frac{1}{2t}\int_{b-t}^{b+t}f^2
-2f(b)\cdot\frac{1}{2t}\int_{b-t}^{b+t}f
+f(b)^2.
$$
For a.e. $b$, the right‑hand side tends to
$$
f(b)^2-2f(b)f(b)+f(b)^2=0.
$$
Hence the limit holds for almost every $b$.
___

> [!problem] [SHE] 4B.5
> Suppose $f:\mathbf{R}\rightarrow\mathbf{R}$ is a Lebesgue measurable function. Prove that
> $$|f(b)|\le f^{*}(b)$$
> for almost every $b\in\mathbf{R}$.

**Proof:**
Let $f^*$ denote the Hardy–Littlewood maximal function:
$$ f^*(b) = \sup_{t>0} \frac{1}{2t} \int_{b-t}^{b+t} |f(y)| \, dy. $$

By the Lebesgue Differentiation Theorem, for almost every $b \in \mathbb{R}$, the limit of the averages equals the function value:
$$ \lim_{t \to 0^+} \frac{1}{2t} \int_{b-t}^{b+t} |f(y)| \, dy = |f(b)|. $$

Since $f^*(b)$ is the supremum of these averages over all $t > 0$, it must be at least as large as the limit (which exists for a.e. $b$). Therefore:
$$ |f(b)| \le f^*(b) $$
holds for almost every $b \in \mathbb{R}$.