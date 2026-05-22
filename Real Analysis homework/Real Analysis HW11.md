___

> [!problem] [SHE] 6C.1
> Show that the map $f \mapsto \|f\|$ from a normed vector space $V$ to $\mathbb{R}$ is continuous (where the norm on $\mathbb{R}$ is the usual absolute value).

**Proof:**
Take a sequence $f_{1},\dots ,f_{n},\dots$ in $V$ which convergence to $f$. Since the topology is induced by the metric induced by the norm, we have $\lVert f_{n}-f \rVert \to{0}$ as $n\to \infty$. By triangular inequality, $\lVert f_{n}-f \rVert\geq \lvert \lVert f_{n} \rVert- \lVert f \rVert\rvert$, so $\lvert \lVert f_{n} \rVert-\lVert f \rVert \rvert\to 0$ as $n\to \infty$, i.e. $\lVert f_{n} \rVert\to \lVert f \rVert$ as $n\to \infty$. Therefore, $f \mapsto \lVert f \rVert$ is continuous.
___

> [!problem]
> Consider the vector space $V=\{(f:\mathbb{N}\to\mathbb{R}):\sum_{m=1}^{\infty}|f(m)|<\infty\}$. Define $\|\cdot\|$ on $V$ by $\|f\|=2|f(1)|+\sum_{m=2}^{\infty}|f(m)|$ for $f\in V$. Prove that $\|\cdot\|$ is a norm on $V$.

**Proof:**
Check the three norm properties:

**Positive definiteness**: $\|f\| \ge 0$ for all $f$, and $\|f\| = 0$ implies $f(1)=0$ and $f(m)=0$ for all $m\ge2$, i.e. $f=0$.

**Absolute homogeneity**: For $\lambda\in\mathbb{R}$,
$$
\|\lambda f\| = 2|\lambda f(1)| + \sum_{m=2}^\infty |\lambda f(m)| = |\lambda|\,\|f\|.
$$
**Triangle inequality**: For $f,g\in V$,
   $$
   \begin{aligned}
   \|f+g\| &= 2|f(1)+g(1)| + \sum_{m=2}^\infty |f(m)+g(m)| \\
   &\le 2\big(|f(1)|+|g(1)|\big) + \sum_{m=2}^\infty \big(|f(m)|+|g(m)|\big) = \|f\| + \|g\|.
   \end{aligned}
   $$

Hence $\|\cdot\|$ is a norm on $V$.
___

> [!problem]
> Let $C_0(\mathbb{N})=\mathbb{R}^{\oplus\mathbb{N}}$ be the set of functions on $\mathbb{N}$ with compact support. Define $\|\cdot\|$ on it by $\|f\|=\sup_n|f(n)|$. Is $(C_0(\mathbb{N}),\|\cdot\|)$ a Banach space? Please prove your conclusion.

**Proof:**
No. For $k\in \mathbb{N}^{+}$, define
$$
f_{k}(n)=
\begin{cases}
1 / k,&n=k, \\
0,&n \neq k.
\end{cases}
$$
Then $f_{k}\in C_{0}(\mathbb{N})$ and $\lVert f_{k+m}-f_{k} \rVert= 1 /k$ for any $m\geq 1$, thus $\{ f_{k} \}$ is a Cauchy sequence.

Assume $f_{k}\to f$ for some $f \in C_{0}(\mathbb{N})$. Since $f$ has compact support, we may assume $f(n)=0$ for $n>M$, where $M$ is a sufficiently large integer. Then $\lVert f_{k}-f \rVert\geq 1/k > 1 /M$ for $k>M$. Thus contradiction.
___

> [!problem]
> Consider the Banach space $(C[0,1],\|\cdot\|)$ with $\|f\|=\sup_{x\in[0,1]}|f(x)|$. Take a subspace
> $U=\{g\in C[0,1]:\int_0^1g(x)\,\mathrm{d}x=0\text{ and }g(1)=0\}$. Let $f(x)=1-x$ and
> $g_n(x)=\frac12-x+\frac{x^n}{2}+\frac{x-1}{n+1}$.
> (1) Show that $g_n\in U$ and $\lim_{n\to\infty}\|f-g_n\|=\frac12$.
> (2) Show that for any $g\in U$, one has $\|f-g\|>\frac12$.

**Proof:**
**(1)** Compute:
$$
\int_{0}^{1}g_{n}(x)\,\mathrm{d}x= \left. \dfrac{x}{2}- \dfrac{x^{2}}{2}+ \dfrac{x^{n+1}}{2n+2}+ \dfrac{(x-1)^{2}}{2n+2} \right| ^{1}_{0}=0,\quad g(1)=0.
$$
Thus $g_{n}\in U$.

Since $g_{n}(x)-f= -\dfrac{1}{2}+ \dfrac{x^{n}}{2}+ \dfrac{x-1}{n+1}$ is increasing in $[0,1]$, we have
$$
\operatorname{sup}_{x\in[0,1]}|f(x)-g_{n}(x)|=\operatorname{max}_{x \in \{ 0,1 \}}|f(x)-g_{n}(x)|= \dfrac{1}{2}- \dfrac{1}{n+1}.
$$
So $\lim_{n\to\infty}\|f-g_n\|=\frac12$.

**(2)** Assume $\lVert f-g \rVert\leq 1/2$ for some $g\in U$, then $\lvert f(x)-g(x) \rvert\leq 1/2$ for $x \in [0,1]$. Thus $g(x)\geq f(x)- 1 /2=1 /2-x$, and $\int_0^1 g(x) \,\mathrm{d}x \geq \int_0^1  1 /2 -x\,\mathrm{d}x=0$. Since $g(x)$ is continuous, the inequality holds if and only if $g(x)= 1 /2 -x$. But $g(1)=0$, contradiction.
___

> [!problem]
> Let $\|\cdot\|_a$ and $\|\cdot\|_b$ be two norms on a vector space $V$. Prove that they are equivalent if and only if the identity maps
> $I:(V,\|\cdot\|_a)\to(V,\|\cdot\|_b)$ and $I:(V,\|\cdot\|_b)\to(V,\|\cdot\|_a)$ are both continuous.

**Proof:**
($\Rightarrow$) If $\|\cdot\|_a$ and $\|\cdot\|_b$ are equivalent, then $\exists c,C>0$ such that $c\|x\|_a\le\|x\|_b\le C\|x\|_a$ for all $x\in V$.

Take $I:(V,\|\cdot\|_a)\to(V,\|\cdot\|_b)$. If $x_n\to x$ in $\|\cdot\|_a$, then $\|x_n-x\|_a\to0$. Using the upper bound,
$$
\|I(x_n)-I(x)\|_b=\|x_n-x\|_b\le C\|x_n-x\|_a\to0,
$$
so $I$ is continuous. The proof for $I:(V,\|\cdot\|_b)\to(V,\|\cdot\|_a)$ is similar, using the lower bound.

($\Leftarrow$) Suppose both $I:(V,\|\cdot\|_a)\to(V,\|\cdot\|_b)$ and $I:(V,\|\cdot\|_b)\to(V,\|\cdot\|_a)$ are continuous.

Assume for contradiction that no $C>0$ satisfies $\|x\|_b\le C\|x\|_a$ for all $x\in V$. Then for each $n\in\mathbb{N}$, pick $x_n\neq0$ with $\|x_n\|_b>n\|x_n\|_a$. Set $y_n=x_n/\|x_n\|_b$. Then $\|y_n\|_b=1$, but $\|y_n\|_a<1/n\to0$, so $y_n\to0$ in $\|\cdot\|_a$. By continuity of $I:(V,\|\cdot\|_a)\to(V,\|\cdot\|_b)$, we must have $\|y_n\|_b\to0$, contradicting $\|y_n\|_b=1$. Hence $\exists C>0$ with $\|x\|_b\le C\|x\|_a$.

A symmetric argument (using continuity of $I:(V,\|\cdot\|_b)\to(V,\|\cdot\|_a)$) gives $\exists c'>0$ with $\|x\|_a\le c'\|x\|_b$. Setting $c=1/c'$ yields $c\|x\|_a\le\|x\|_b$.

Thus the norms are equivalent.

