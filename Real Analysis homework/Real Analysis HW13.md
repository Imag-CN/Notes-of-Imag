___

>[!problem] [SHE] 6E.1
>Suppose $U$ is a subset of a metric space $V$. Show that $U$ is dense in $V$ if and only if every nonempty open subset of $V$ contains at least one element of $U$.

**Proof:**
$(\Rightarrow)$ Assume $\overline{U}=V$. Let $O$ be any nonempty open subset of $V$. If $O \cap U = \varnothing$, then $O \subset V \setminus U \subset V \setminus \overline{U}$. But $V \setminus \overline{U} = \varnothing$ since $\overline{U}=V$, contradicting that $O$ is nonempty. Therefore, $O \cap U \neq \varnothing$.

$(\Leftarrow)$ Assume every nonempty open subset of $V$ contains at least one point of $U$. For any $x \in V$ and any $\varepsilon > 0$, the open ball $B(x, \varepsilon)$ is a nonempty open subset. By assumption, $B(x, \varepsilon) \cap U \neq \varnothing$. Hence, $x$ is a limit point of $U$ (or $x \in U$ itself), so $x \in \overline{U}$. Since $x$ was arbitrary, $V \subset \overline{U}$, implying $\overline{U}=V$. Thus, $U$ is dense in $V$.
___

>[!problem] [SHE] 6E.8
>Suppose $(X,d)$ is a complete metric space and $G_1, G_2, \ldots$ is a sequence of dense open subsets of $X$. Prove that $\bigcap_{k=1}^{\infty} G_k$ is a dense subset of $X$.

**Proof:**
Take any nonempty open subset $U\subset X$, then $X\cap G_{k},k\in \mathbb{Z}^{+}$ is an open set and dense in $X$. By Baire's theorem, $X\cap\bigcap_{k=1}^{\infty} G_k=\bigcap_{k=1}^{\infty} (G_k\cap X)$ is nonempty, i.e. $\bigcap_{k=1}^{\infty} G_k$ contains at least one element of $U$. By exercise 6E.1, $\bigcap_{k=1}^{\infty} G_k$ is dense in $X$.
___

>[!problem] [SHE] 6E.17
>Suppose $V$ is a Banach space, $W$ is a normed vector space, and $T_1, T_2, \ldots$ is a sequence of bounded linear maps from $V$ to $W$ such that
>$$
>\lim_{k \to \infty} T_k f \text{ exists for each } f \in V.
>$$
>Define $T: V \to W$ by
>$$
>Tf = \lim_{k \to \infty} T_k f
>$$
>for $f \in V$. Prove that $T$ is a bounded linear map from $V$ to $W$.

**Proof:**
**Linearity:** For any $f, g \in V$ and $\alpha, \beta \in \mathbb{C}$ (or $\mathbb{R}$), we have
$$
 T(\alpha f + \beta g) = \lim_{k \to \infty} T_k(\alpha f + \beta g) = \lim_{k \to \infty} \big( \alpha T_k f + \beta T_k g \big) = \alpha \lim_{k \to \infty} T_k f + \beta \lim_{k \to \infty} T_k g = \alpha T f + \beta T g,
$$
where the second equality uses the linearity of each $T_k$, and the third uses the linearity of the limit in the normed space $W$. Hence $T$ is linear.

**Boundedness:** For each $f \in V$, the sequence $\{T_k f\}$ converges in $W$, hence it is bounded: $\sup_k \|T_k f\|_W < \infty$. Since $V$ is a Banach space, the Uniform Boundedness Principle implies that
$$
\sup_{k} \|T_k\|_{\mathcal{L}(V,W)} < \infty.
$$
Let $C := \sup_k \|T_k\|$. Then for every $f \in V$ and every $k$,
$$
\|T_k f\|_W \le C \|f\|_V.
$$
Taking the limit as $k \to \infty$ preserves the inequality, so
$$
\|T f\|_W = \big\|\lim_{k\to\infty} T_k f\big\|_W = \lim_{k\to\infty} \|T_k f\|_W \le C \|f\|_V.
$$
Hence $T$ is bounded with $\|T\| \le C$.

Therefore, $T$ is a bounded linear map from $V$ to $W$.
___

>[!problem] [SHE] 6E.18
>Suppose $V$ is a normed vector space and $B$ is a subset of $V$ such that
>$$
>\sup_{f \in B} |\varphi(f)| < \infty
>$$
>for every $\varphi \in V'$. Prove that
>$$
>\sup_{f \in B} \|f\| < \infty.
>$$

**Proof:**
For each $f \in V$, define $\hat{f} \in V''$ (the double dual) by $\hat{f}(\varphi) = \varphi(f)$ for all $\varphi \in V'$.The map $f \mapsto \hat{f}$ is an isometric linear embedding: $\|\hat{f}\|_{V''} = \|f\|_V$.

For every $\varphi \in V'$, the given condition says $\sup_{f \in B} |\hat{f}(\varphi)| = \sup_{f \in B} |\varphi(f)| < \infty$. Regard $\{\hat{f} : f \in B\}$ as a family of bounded linear functionals on the Banach space $V'$. By the Uniform Boundedness Principle applied in $V'$, we have
$$
\sup_{f \in B} \|\hat{f}\|_{V''} < \infty.
$$
Since $\|\hat{f}\|_{V''} = \|f\|_V$ for every $f \in B$, it follows that
$$
\sup_{f \in B} \|f\|_V = \sup_{f \in B} \|\hat{f}\|_{V''} < \infty.
$$
___

>[!problem] [SHE] 6E.19
>Suppose $T: V \to W$ is a linear map from a Banach space $V$ to a Banach space $W$ such that
>$$
>\varphi \circ T \in V' \quad \text{for all } \varphi \in W’.
>$$
>Prove that $T$ is a bounded linear map.

**Proof:**
Assume $T$ is not bounded. Then there exist $f_n \in V$ with $\|f_n\|_V=1$ and $\|Tf_n\|_W \to \infty$.

Let $g_n = f_n / \|Tf_n\|_W$. Then $\|g_n\|_V \to 0$, so $g_n \to 0$ in $V$.

For every $\varphi \in W'$, the functional $\varphi \circ T$ belongs to $V'$ (given). Hence
$$
(\varphi \circ T)(g_n) = \frac{\varphi(Tf_n)}{\|Tf_n\|_W} \xrightarrow{n\to\infty} 0.
$$
Thus, for each $\varphi \in W'$, the set $\{\varphi(Tf_n)\}_{n}$ is bounded; otherwise the quotient above would not tend to $0$.

Now consider the family $\{\psi_n\} \subset W''$ defined by $\psi_n(\varphi) = \varphi(Tf_n)$.  
For every $\varphi \in W'$, $\sup_n |\psi_n(\varphi)| < \infty$. By the Uniform Boundedness Principle, we have $\sup_n \|\psi_n\|_{W''} < \infty$. Since the canonical embedding $W \hookrightarrow W''$ is isometric, $\|\psi_n\|_{W''} = \|Tf_n\|_W$. Hence $\sup_n \|Tf_n\|_W < \infty$, contradicting $\|Tf_n\|_W \to \infty$.

Therefore $T$ must be bounded.
___

>[!problem] [SHE] 6E.10
>Give an example of a Banach space $V$, a normed vector space $W$, a bounded linear map $T$ of $V$ onto $W$, and an open subset $G$ of $V$ such that $T(G)$ is not an open subset of $W$.

**Proof:**
Let $V=\ell^{1}$ equipped with standard $\ell^{1}$ norm, $W=\ell^{1}$ but equipped with $\ell^{\infty}$ norm, $T$ be the identity map, $G=B(0,0.5)$. $T$ is bounded because $\lVert f \rVert_{V}\geq \lVert f \rVert_{W}$ for any $f\in \ell^{1}$. For any $\epsilon>0$, define $x=(\epsilon(1-\epsilon)^{i-1})_{i\in \mathbb{Z}^{+}}$, then $\lVert x \rVert_{V}=1$, but $\lVert x \rVert_{W}=\epsilon$, thus $x\not\in T(G)$ but $x$ can be in any open neighborhood of $0\in W$ since we can take $\epsilon$ arbitrarily small. Thus $T(G)$ is not an open subset.
___

>[!problem] [SHE] 6E.12
>Suppose $T: V \to W$ is a bounded linear map from a Banach space $V$ to a Banach space $W$. Prove that $T$ is bounded below if and only if $T$ is injective and the range of $T$ is a closed subspace of $W$.

**Proof:**
($\Rightarrow$) Suppose $T$ is bounded below, i.e., $\exists\,c>0$ such that $\|Tv\|_W \ge c\|v\|_V$ for all $v\in V$.

**$T$ is injective:** If $Tv=0$, then $0=\|Tv\|_W \ge c\|v\|_V$, so $\|v\|_V=0$, hence $v=0$.

**$\mathcal{R}(T)$ is closed:** Let $(w_n)$ be a sequence in $\mathcal{R}(T)$ with $w_n\to w$ in $W$. Write $w_n=Tv_n$. Since $(w_n)$ is Cauchy, the inequality $\|T(v_n-v_m)\|_W \ge c\|v_n-v_m\|_V$ implies $(v_n)$ is Cauchy in $V$. $V$ is complete, so $v_n\to v$ for some $v\in V$. By continuity of $T$, $w_n=Tv_n\to Tv$, hence $w=Tv\in\mathcal{R}(T)$.

($\Leftarrow$) Suppose $T$ is injective and $\mathcal{R}(T)$ is closed in $W$. Then $\mathcal{R}(T)$ is a Banach space.  
Consider $T:V\to\mathcal{R}(T)$. It is a bijective bounded linear map between Banach spaces. By the Bounded Inverse Theorem, $T^{-1}:\mathcal{R}(T)\to V$ is bounded.

Thus there exists $C>0$ such that $\|T^{-1}w\|_V \le C\|w\|_W$ for all $w\in\mathcal{R}(T)$.  
For any $v\in V$, take $w=Tv$. Then $\|v\|_V=\|T^{-1}(Tv)\|_V \le C\|Tv\|_W$, i.e., $\|Tv\|_W \ge (1/C)\|v\|_V$. Hence $T$ is bounded below.
___

>[!problem] [SHE] 6E.14
>Show that there exists a normed space $V$, a Banach space $W$, and a one-to-one bounded linear map $T$ of $V$ onto $W$ such that $T^{-1}$ is not a bounded linear map of $W$ onto $V$.

**Proof:**
Let $V = C[0,1]$ equipped with the supremum norm $\|\cdot\|_\infty$ (which makes it a Banach space) and $W = C[0,1]$ equipped with the $L^1$-norm $\|f\|_1 = \int_0^1 |f(t)|dt$. Then $W$ is not complete. Define $T$ to be the identity map. Then $T$ is linear and one-to-one, and $T$ is bounded because $\lVert f \rVert_{V}\geq \lVert f \rVert_{W}$ for all $f\in C[0,1]$.

Take $f_n(t) = t^n$. Then $\|f_n\|_1 = \int_0^1 t^n dt = \frac{1}{n+1} \to 0$, but $\|f_n\|_\infty = 1$ for all $n$.  
Thus $\frac{\|T^{-1}f_n\|_\infty}{\|f_n\|_1} = \frac{1}{1/(n+1)} = n+1 \to \infty$, so $T^{-1}$ is unbounded.
___

>[!problem] [SHE] 6E.16
>Suppose $V$ is a Banach space with norm $\|\cdot\|$ and that $\varphi: V \to \mathbb{F}$ is a linear functional. Define another norm $\|\cdot\|_\varphi$ on $V$ by
>$$
>\|f\|_\varphi = \|f\| + |\varphi(f)|.
>$$
>Prove that if $V$ is a Banach space with the norm $\|\cdot\|_\varphi$, then $\varphi$ is a continuous linear functional on $V$ (with the original norm).

**Proof:**
Define $I: (V,\|\cdot\|_\varphi) \to (V,\|\cdot\|)$ by $I(f)=f$, the identity map. Since $\|f\| \le \|f\|_\varphi$ for all $f$, $I$ is a bounded linear operator.

Because $(V,\|\cdot\|_\varphi)$ and $(V,\|\cdot\|)$ are both Banach spaces, $I$ is a bijective bounded linear map between Banach spaces. By the Bounded Inverse Theorem, $I^{-1}: (V,\|\cdot\|) \to (V,\|\cdot\|_\varphi)$ is also bounded, i.e., there exists $C>0$ such that
$$
\|f\|_\varphi \le C \|f\| \quad \text{for all } f \in V.
$$

Now $\|f\|_\varphi = \|f\| + |\varphi(f)| \le C \|f\|$ implies
$$
|\varphi(f)| \le (C-1) \|f\| \quad (\text{for all } f \in V).
$$
Thus $\varphi$ is bounded (continuous) on $(V,\|\cdot\|)$.
___

>[!problem] [SHE] 7A.7
>Suppose $(X,\mathcal{S},\mu)$ is a measure space and $f,h:X\to\mathcal{F}$ are $\mathcal{S}$-measurable.
>Prove that
>$$
>\left\|fh\right\|_{r}\leq\left\|f\right\|_{p}\left\|h\right\|_{q}
>$$
>for all positive numbers $p,q,r$ such that $\frac{1}{p}+\frac{1}{q}=\frac{1}{r}$.

**Proof:**
Write $\frac{1}{p/r}+\frac{1}{q/r}=1$. Let $F=|f|^r$, $H=|h|^r$. Then $F\in L^{p/r}$, $H\in L^{q/r}$ because
$$
\|F\|_{p/r}^{p/r}=\int |f|^p=\|f\|_p^p,\qquad \|H\|_{q/r}^{q/r}=\int |h|^q=\|h\|_q^q.
$$
 Apply the Hölder inequality with exponents $\frac{p}{r}$ and $\frac{q}{r}$ to $F$ and $H$:
$$
\int |fh|^r = \int FH \le \|F\|_{p/r}\,\|H\|_{q/r}.
$$
Taking the $1/r$ power on both sides gives
$$
\|fh\|_r = \Big(\int |fh|^r\Big)^{1/r}
\le \big(\|F\|_{p/r}\,\|H\|_{q/r}\big)^{1/r}
= \|F\|_{p/r}^{1/r}\,\|H\|_{q/r}^{1/r}
= \|f\|_p\,\|h\|_q.
$$
This completes the proof.
___

>[!problem] [SHE] 7A.9
>Show that the formula in 7.12 holds for $p = \infty$ if $\mu$ is a $\sigma$-finite measure.

**Proof:**
Let $M = \|f\|_\infty$. We aim to prove
$$
M = \sup\left\{ \left|\int_X f h \, d\mu\right| : h \in L^1(\mu), \|h\|_1 \le 1 \right\}.
$$
**($\le$)** For any $h \in L^1(\mu)$ with $\|h\|_1 \le 1$,
$$
\left|\int f h \, d\mu\right| \le \int |f||h| \, d\mu \le M \|h\|_1 \le M.
$$
Thus RHS $\le M$.

**($\ge$)** Fix $\varepsilon > 0$. Since $\mu$ is $\sigma$-finite, there exists a set $A$ with $0 < \mu(A) < \infty$ such that $|f| \ge M - \varepsilon$ on $A$.  
Define $h = \frac{1}{\mu(A)} \mathbf{1}_A \operatorname{sgn}(f)$. Then $\|h\|_1 = 1$ and
$$
\left|\int f h \, d\mu\right| = \frac{1}{\mu(A)} \int_A |f| \, d\mu \ge M - \varepsilon.
$$
Hence RHS $\ge M - \varepsilon$ for all $\varepsilon > 0$, so RHS $\ge M$.
___

>[!problem] [SHE] 7A.10
>Suppose $0 < p < q \leq \infty$.
>
>(a) Prove that $\ell^{p} \subset \ell^{q}$.
>
>(b) Prove that
>$$
>\left\|\left(a_{1},a_{2},\ldots\right)\right\|_{p} \geq \left\|\left(a_{1},a_{2},\ldots\right)\right\|_{q}
>$$
>for every sequence $a_{1},a_{2},\ldots$ of elements of $\mathbb{F}$.

**Proof:**
**(a)** Let $a=(a_n)\in\ell^p$, $a\neq0$.

If $q=\infty$, then $|a_n|\le\|a\|_p$ for all $n$, so $\|a\|_\infty\le\|a\|_p<\infty$, hence $a\in\ell^\infty$.

If $q<\infty$, since $|a_n|^p\to0$, there exists $N$ such that $|a_n|\le1$ for all $n\ge N$. Then $|a_n|^q\le|a_n|^p$ for $n\ge N$, and
$$
\sum_{n\ge N}|a_n|^q\le\sum_{n\ge N}|a_n|^p<\infty.
$$
The finitely many terms for $n<N$ are finite, so $\sum|a_n|^q<\infty$, i.e., $a\in\ell^q$.

**(b)** Assume $a\neq0$. Let $b_n=|a_n|/\|a\|_p$, then $\sum b_n^p=1$, hence $0\le b_n\le1$ for all $n$. Since $q>p$, we have $b_n^q\le b_n^p$. Summing gives
$$
\sum b_n^q\le\sum b_n^p=1.
$$
Taking the $1/q$ power yields $\|b\|_q\le1$, i.e., $\|a\|_q\le\|a\|_p$.