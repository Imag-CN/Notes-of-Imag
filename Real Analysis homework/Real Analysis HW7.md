___

> [!problem] [SHE] 3A.15
> Suppose $\lambda$ is Lebesgue measure on $\mathbf{R}$ and $f:\mathbf{R}\to[-\infty,\infty]$ is a Borel measurable function such that $\int f d\lambda$ is defined.
> (a) For $t\in\mathbf{R}$, define $f_t:\mathbf{R}\to[-\infty,\infty]$ by $f_t(x)=f(x-t)$. Prove that $\int f_t d\lambda=\int f d\lambda$ for all $t\in\mathbf{R}$
> (b) For $t\in\mathbf{R}\setminus\{0\}$, define $f_t:\mathbf{R}\to[-\infty,\infty]$ by $f_t(x)=f(tx)$. Prove that $\int f_t d\lambda=\frac{1}{|t|}\int f d\lambda$ for all $t>0$.

**Proof:**
**(a)** For any measurable set $A$, $x \in A$ if and only if $x - t \in A - t$, hence $\lambda(A) = \lambda(A - t)$.
By the translation invariance of Lebesgue measure, we have
$$
\int_{\mathbb{R}} f_t(x) \, d\lambda(x) = \int_{\mathbb{R}} f(x - t) \, d\lambda(x) = \int_{\mathbb{R}} f(y) \, d\lambda(y + t) = \int_{\mathbb{R}} f(y) \, d\lambda(y).
$$
Therefore $\int f_t \, d\lambda = \int f \, d\lambda$ for all $t \in \mathbf{R}$.

**(b)** For any measurable set $A$, $x \in t^{-1}A$ if and only if $tx \in A$, and
$$
\lambda(t^{-1}A) = \int_{\mathbb{R}} 1_{t^{-1}A}(x) \, d\lambda(x) = \int_{\mathbb{R}} 1_{A}(tx) \, d\lambda(x).
$$
Since $\lambda(t^{-1}A) = t^{-1} \lambda(A)$, by linearity for simple functions and a monotone convergence argument,
$$
\int_{\mathbb{R}} f(tx) \, d\lambda(x) = t^{-1} \int_{\mathbb{R}} f(y) \, d\lambda(y) = \frac{1}{t} \int f \, d\lambda.
$$
For $t < 0$, let $t' = -t$. Then
$$
f_t(x) = f(tx) = f(-t'x) = (f \circ (-1)) (t'x).
$$
Since $\int f \circ (-1) \, d\lambda = \int f \, d\lambda$ (by translation symmetry) and $|t| = t'$, applying the result for $t'>0$ gives
$$
\int f_t \, d\lambda = \frac{1}{t'} \int f \, d\lambda = \frac{1}{|t|} \int f \, d\lambda.
$$
Hence $\int f_t \, d\lambda = \frac{1}{|t|} \int f \, d\lambda$ for all $t \neq 0$.
___

> [!problem] [SHE] 3A.20
> Suppose $(X,\mathcal{S},\mu)$ is a measure space and $f_1,f_2,\dots$ is a monotone (meaning either increasing or decreasing) sequence of $\mathcal{S}$-measurable functions. Define $f:X\to[-\infty,\infty]$ by
> $$
> f(x)=\lim_{k\to\infty}f_k(x).
>$$
> Prove that if $\int|f_1|d\mu<\infty$, then
> $$
> \lim_{k\to\infty}\int f_kd\mu=\int fd\mu.
>$$

**Proof:**
**Case 1: $f_k\nearrow f$.**  
Define $g_k = f_k - f_1 \ge 0$. Then $g_k\nearrow f - f_1$. By MCT,
$$
\int g_k \to \int(f - f_1) \implies \int f_k \to \int f.
$$

**Case 2: $f_k\searrow f$.**  
Define $g_k = f_1 - f_k \ge 0$. Then $g_k\nearrow f_1 - f$. By MCT,
$$
\int g_k \to \int(f_1 - f) \implies \int f_k \to \int f.
$$

In both cases, $\lim \int f_k = \int f$.
___

> [!problem] [SHE] 3B.3
> Suppose $\lambda$ is Lebesgue measure on $\mathbb{R}$ and $f:\mathbb{R}\to\mathbb{R}$ is a Borel measurable function such that $\int|f|d\lambda<\infty$. Define $g:\mathbb{R}\to\mathbb{R}$ by
> $$
> g(x)=\int_{(-\infty,x)}fd\lambda.
>$$
> Prove that $g$ is uniformly continuous on $\mathbb{R}$.

**Proof:**
Let $x,y\in\mathbb{R}$ with $x<y$, then
$$
|g(y)-g(x)| = \left| \int_{(-\infty,y)} f\,d\lambda - \int_{(-\infty,x)} f\,d\lambda \right|
= \left| \int_{[x,y)} f\,d\lambda \right|
\le \int_{[x,y)} |f|\,d\lambda.
$$

Since $\int_{\mathbb{R}} |f|\,d\lambda<\infty$, for any $\epsilon>0$ there exists $\delta>0$ such that for any measurable set $E$ with $\lambda(E)<\delta$, we have $\int_E |f|\,d\lambda<\epsilon$.

Now take $|y-x|<\delta$. Then $\lambda([x,y)) = y-x < \delta$, so
$$
|g(y)-g(x)| \le \int_{[x,y)} |f|\,d\lambda < \epsilon.
$$

The same estimate holds for $x>y$ by symmetry. Therefore $g$ is uniformly continuous on $\mathbb{R}$. 
___

> [!problem] [SHE] 3B.4
>(a) Suppose $(X,\mathcal{S},\mu)$ is a measure space with $\mu(X) < \infty$. Suppose that $f: X \to [0,\infty)$ is a bounded $\mathcal{S}$-measurable function. Prove that  
>$$
>\int f d\mu = \inf\left\{ \sum_{j=1}^{m} \mu(A_j) \sup_{A_j} f : A_1,\ldots,A_m \text{ is an } \mathcal{S}\text{-partition of } X \right\}.
>$$
>
>(b) Show that the conclusion of part (a) can fail if the hypothesis that $f$ is bounded is replaced by the hypothesis that $\int f d\mu < \infty$.
>
>(c) Show that the conclusion of part (a) can fail if the condition that $\mu(X) < \infty$ is deleted.

**Proof:**
**(a)** For any $\mathcal{S}$-partition $\mathcal{P}=\{A_1,\dots,A_m\}$ of $X$, define
$$
U(f,\mathcal{P})=\sum_{j=1}^m\mu(A_j)\sup_{A_j}f.
$$
If $s\le f$ is a simple function adapted to $\mathcal{P}$, then $\int s\,d\mu\le U(f,\mathcal{P})$. Taking supremum over all such $s$ gives
$$
\int f\,d\mu\le U(f,\mathcal{P})\quad\Rightarrow\quad\int f\,d\mu\le\inf_{\mathcal{P}}U(f,\mathcal{P}).\tag{1}
$$

For the reverse inequality, fix $\epsilon>0$. Choose $n$ so large that $M/n<\epsilon/\mu(X)$, where $M=\sup_X f$. Partition the range $[0,M]$ into $n$ subintervals of length $M/n$, and let $E_k$ be the preimage of the $k$-th subinterval. Then $\{E_k\}$ is an $\mathcal{S}$-partition of $X$, and
$$
\sup_{E_k}f\le\inf_{E_k}f+\frac{M}{n}\le f(x)+\frac{M}{n}\quad\text{for }x\in E_k.
$$
Hence
$$
U(f,\{E_k\})\le\int f\,d\mu+\frac{M}{n}\mu(X)<\int f\,d\mu+\epsilon.
$$
Thus $\inf_{\mathcal{P}}U(f,\mathcal{P})\le\int f\,d\mu$, which with (1) proves the equality.

**(b)** Take $X=[1,\infty)$ with Lebesgue measure, $f(x)=1/x^2$. Then $\int f\,d\lambda=1<\infty$. For any finite partition $\{A_1,\dots,A_m\}$ of $X$, some $A_j$ contains an infinite interval, so $\mu(A_j)=\infty$ and $\sup_{A_j}f>0$. Hence $U(f,\mathcal{P})=\infty$ for every $\mathcal{P}$, so $\inf_{\mathcal{P}}U(f,\mathcal{P})=\infty\neq1=\int f\,d\mu$.

**(c)** Take $X=\mathbb{R}$ with Lebesgue measure, $f(x)=e^{-x^2}$. Then $\int f\,d\lambda=\sqrt{\pi}<\infty$. For any finite partition $\{A_1,\dots,A_m\}$ of $\mathbb{R}$, some $A_j$ has infinite measure and $\sup_{A_j}f>0$, so $U(f,\mathcal{P})=\infty$ for every $\mathcal{P}$. Hence $\inf_{\mathcal{P}}U(f,\mathcal{P})=\infty\neq\sqrt{\pi}=\int f\,d\mu$.
___

> [!problem] [SHE] 3B.6
> Let $\lambda$ denote Lebesgue measure on $\mathbb{R}$. Give an example of a continuous function $f: [0,\infty)\to\mathbb{R}$ such that
> $$
> \lim_{t\to\infty}\int_{[0,t]}f\,d\lambda
>$$
> exists (in $\mathbb{R}$) but
> $$
>\int_{[0,\infty)}f\,d\lambda
>$$
> is not defined.

**Proof:**
Take $f(x)=\dfrac{\sin x}{x}$ for $x>0$ and $f(0)=1$.  Then see the argument in [SHE] 3B.14(c) (which is right behind).
___

> [!problem] [SHE] 3B.10
> (a) Suppose $(X,\mathcal{S},\mu)$ is a measure space such that $\mu(X)<\infty$. Suppose $p,r$ are positive numbers with $p<r$. Prove that if $f:X\to[0,\infty)$ is an $\mathcal{S}$-measurable function such that $\int f^r\,d\mu<\infty$, then $\int f^p\,d\mu<\infty$.
> 
> (b) Give an example to show that the result in part (a) can be false without the hypothesis that $\mu(X)<\infty$.

**Proof:**
**(a)** Let $A=\{x\in X: f(x)\le 1\}$ and $B=\{x\in X: f(x)>1\}$.  
On $A$ we have $f^p\le 1$, so
$$
\int_A f^p\,d\mu\le\int_A 1\,d\mu=\mu(A)\le\mu(X)<\infty.
$$
On $B$ we have $f>1$, and since $p<r$, we have $f^p<f^r$ on $B$. Therefore
$$
\int_B f^p\,d\mu\le\int_B f^r\,d\mu\le\int_X f^r\,d\mu<\infty.
$$
Hence
$$
\int_X f^p\,d\mu=\int_A f^p\,d\mu+\int_B f^p\,d\mu<\infty.
$$

**(b)** Take $X=(1,\infty)$ with Lebesgue measure $\lambda$, and define $f(x)=\frac{1}{x}$. Let $p=1$, $r=2$.

Then $\mu(X)=\infty$ (violating the hypothesis). Compute
$$
\int_X f^2\,d\lambda=\int_1^\infty\frac{1}{x^2}\,dx=1<\infty,
$$
but
$$
\int_X f\,d\lambda=\int_1^\infty\frac{1}{x}\,dx=\infty.
$$
Thus $\int f^r<\infty$ but $\int f^p=\infty$, so the conclusion of (a) fails when $\mu(X)=\infty$.
___

> [!problem] [SHE] 3B.11
> Suppose $(X,\mathcal{S},\mu)$ is a measure space and $f\in\mathcal{L}^{1}(\mu)$. Prove that
> $$
> \{x \in X : f(x) \neq 0\}
>$$
> is the countable union of sets with finite $\mu$-measure.

**Proof:**
Let $E = \{x \in X : f(x) \neq 0\}$.  
For each $n \in \mathbb{N}$, define  
$$
E_n = \left\{x \in X : |f(x)| \ge \frac{1}{n}\right\}.
$$
Clearly $E_n \subset E_{n+1}$ and $E = \bigcup_{n=1}^\infty E_n$.

Since $f \in \mathcal{L}^1(\mu)$, we have $\int_X |f|\,d\mu < \infty$.  
For each fixed $n$,
$$
\frac{1}{n} \mu(E_n) = \int_{E_n} \frac{1}{n}\,d\mu \le \int_{E_n} |f|\,d\mu \le \int_X |f|\,d\mu < \infty.
$$
Hence $\mu(E_n) \le n \int_X |f|\,d\mu < \infty$ for every $n$.

Therefore $E = \bigcup_{n=1}^\infty E_n$ is a countable union of sets $E_n$ with finite $\mu$-measure.
___

> [!problem] [SHE] 3B.14(c)
> Let $\lambda$ denote Lebesgue measure on $\mathbb{R}$. Let $f(x)=\dfrac{\sin x}{x}$. Show that the integral
> $$
> \int_{(0,\infty)}f\,d\lambda
>$$
> is not defined (i.e., $f\notin L^1((0,\infty))$), but
> $$
> \lim_{t\to\infty}\int_{(0,t)}f\,d\lambda
>$$
>exists in $\mathbb{R}$ (i.e., the improper Riemann integral or Dirichlet integral converges).

**Proof:**
**1.** $\int_{(0,\infty)} |f|\,d\lambda = \infty$.

Consider the integral of $|\sin x/x|$ over intervals $[k\pi, (k+1)\pi]$, $k\ge 1$.  
For $x\in[k\pi,(k+1)\pi]$, we have
$$
\frac{|\sin x|}{x} \ge \frac{|\sin x|}{(k+1)\pi}.
$$
Hence
$$
\int_{k\pi}^{(k+1)\pi} \frac{|\sin x|}{x}\,dx
\ge \frac{1}{(k+1)\pi} \int_{k\pi}^{(k+1)\pi} |\sin x|\,dx
= \frac{2}{(k+1)\pi},
$$
because $\int_{0}^{\pi} |\sin x|\,dx = 2$.  

Summing over $k=1$ to $N$ gives
$$
\int_{\pi}^{(N+1)\pi} \frac{|\sin x|}{x}\,dx
\ge \frac{2}{\pi} \sum_{k=1}^{N} \frac{1}{k+1} \to \infty \quad\text{as }N\to\infty.
$$
Therefore $\int_{(0,\infty)} |f|\,d\lambda = \infty$, so $f\notin L^1((0,\infty))$ and the Lebesgue integral $\int_{(0,\infty)} f\,d\lambda$ is not defined.

**2.** $\displaystyle\lim_{t\to\infty} \int_{(0,t)} f\,d\lambda$ exists in $\mathbb{R}$.

The function $f(x)=\frac{\sin x}{x}$ is continuous on $(0,\infty)$ and its improper Riemann integral
$$
\lim_{t\to\infty} \int_0^t \frac{\sin x}{x}\,dx
$$
converges to $\frac{\pi}{2}$ (Dirichlet integral).

Since $f$ is bounded on $[0,1]$ and the improper integral converges, the limit of the Lebesgue integrals over $(0,t)$ coincides with the improper Riemann limit:
$$
\lim_{t\to\infty} \int_{(0,t)} f\,d\lambda = \frac{\pi}{2} \in \mathbb{R}.
$$

Thus the required conclusion holds: the Lebesgue integral over $(0,\infty)$ is undefined, but the limit of integrals over finite intervals exists.
___

> [!problem] [SHE] 3B.15
> Prove or give a counterexample: If $G$ is an open subset of $(0,1)$, then $\chi_G$ is Riemann integrable on $[0,1]$.

**Counterexample:**  
Let $C$ be a fat Cantor set contained in $[0,1]$ with positive measure, say $m(C)=\frac{1}{2}>0$.  
Define $G = [0,1]\setminus C$. Then $G$ is open in $(0,1)$ (since $C$ is closed and contains endpoints).  

The characteristic function $\chi_G$ is discontinuous exactly on the boundary $\partial G$.  
For this construction, $\partial G = C$ (because $C$ is nowhere dense and closed, and $G$ is its complement in $(0,1)$).  
Since $m(\partial G)=m(C)=\frac12>0$, the set of discontinuities of $\chi_G$ has positive Lebesgue measure.  

A bounded function on $[0,1]$ is Riemann integrable iff its set of discontinuities has measure zero. Hence $\chi_G$ is not Riemann integrable on $[0,1]$.
___

> [!problem] [SHE] 3B.16
> Suppose $f\in\mathcal{L}^{1}(\mathbf{R})$.
> (a) For $t\in\mathbf{R}$, define $f_t:\mathbf{R}\to\mathbf{R}$ by $f_t(x)=f(x-t)$. Prove that
> $$
> \lim_{t\to0}\|f-f_t\|_1=0.
>$$
> (b) For $t>0$, define $f_t:\mathbf{R}\to\mathbf{R}$ by $f_t(x)=f(tx)$. Prove that
> $$
> \lim_{t\to1}\|f-f_t\|_1=0.
> $$

**Proof:
**(a)** Let $C_c(\mathbb{R})$ denote the space of continuous functions with compact support.  
Since $C_c(\mathbb{R})$ is dense in $L^1(\mathbb{R})$, for any $\epsilon>0$ we can choose $g\in C_c(\mathbb{R})$ such that $\|f-g\|_1<\epsilon/3$.

Define $g_t(x)=g(x-t)$. Then
$$
\|f-f_t\|_1\le\|f-g\|_1+\|g-g_t\|_1+\|g_t-f_t\|_1.
$$
Because translation preserves the $L^1$-norm, $\|g_t-f_t\|_1=\|g-f\|_1<\epsilon/3$ and $\|f-g\|_1<\epsilon/3$. Hence
$$
\|f-f_t\|_1< \frac{2\epsilon}{3}+\|g-g_t\|_1.
$$

Since $g$ is uniformly continuous (continuous with compact support), there exists $\delta>0$ such that $|t|<\delta$ implies $|g(x)-g(x-t)|<\frac{\epsilon}{3m(\operatorname{supp}(g))}$ for all $x$. Then
$$
\|g-g_t\|_1=\int_{\mathbb{R}}|g(x)-g(x-t)|dx
\le m(\operatorname{supp}(g))\cdot\frac{\epsilon}{3m(\operatorname{supp}(g))}=\frac{\epsilon}{3}.
$$
Therefore $\|f-f_t\|_1<\epsilon$ for $|t|<\delta$, which proves $\lim_{t\to0}\|f-f_t\|_1=0$.

**(b)** Again choose $g\in C_c(\mathbb{R})$ with $\|f-g\|_1<\epsilon/3$. Define $g_t(x)=g(tx)$. Then
$$
\|f-f_t\|_1\le\|f-g\|_1+\|g-g_t\|_1+\|g_t-f_t\|_1.
$$
Since $\|g_t-f_t\|_1=\frac{1}{t}\|g-f\|_1$, for $t$ near 1 we have $\|g_t-f_t\|_1\le 2\|f-g\|_1<2\epsilon/3$. Thus
$$
\|f-f_t\|_1< \epsilon + \|g-g_t\|_1.
$$

Now
$$
\|g-g_t\|_1 = \int_{\mathbb{R}}|g(x)-g(tx)|dx.
$$
Because $g$ is uniformly continuous and has compact support, for $t$ sufficiently close to 1 we have $|g(x)-g(tx)|<\frac{\epsilon}{m(\operatorname{supp}(g))+1}$ for all $x$. Hence $\|g-g_t\|_1<\epsilon$ for $t$ near 1.

Combining the estimates gives $\|f-f_t\|_1<2\epsilon$ for $t$ sufficiently close to 1, which proves $\lim_{t\to1}\|f-f_t\|_1=0$.
