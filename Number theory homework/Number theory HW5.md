___

> [!problem] Problem 1 ([SER] II.2.1)
> (Krasner's lemma) Let $E/K$ be a finite Galois extension of a non-Archimedean complete field $K$. Prolong the valuation of $K$ to $E$. Let $x \in E$ and let $\{x_1, \dots, x_n\}$ be the set of conjugates of $x$ over $K$, with $x = x_1$. Let $y \in E$ be such that $\|y - x\| < \|y - x_i\|$ for $i \ge 2$. Show that $x$ belongs to the field $K(y)$.

**Proof:**
Since $E/K$ is Galois, we have $E/K(y)$ is Galois. Suppose that $x\notin K(y)$, then there is a $K(y)$-automorphism $\sigma$ of $E$ such that $\sigma(x)\ne x$ (since $\operatorname{Gal}(E/K(y))$ acts transitively on the roots of the minimal polynomial of $x$ with respect to $E/K(y)$). In particular, $\sigma$ is also a $K$-automorphism of $E$, so $\sigma(x)=x_i$ for some $i\ge2$.

By the uniqueness of extension of valuations, we have$\|y-x\|=\|\sigma(y-x)\|$. Because $\sigma$ fixes $y$, we have $\|\sigma(y-x)\|=\|y-\sigma(x)\|=\|y-x_i\|$, contradicting the assumption $\|y-x\|<\|y-x_i\| \quad (i\ge2)$.

Therefore $x$ has no conjugate over $K(y)$ other than itself, so $x\in K(y)$.
___

> [!problem] Problem 2
> (i) ([SER II.2.1]) Let $K$ be a non-Archimedean complete field, and let $f(\mathrm{X}) \in \mathrm{K}[\mathrm{X}]$ be a separable irreducible polynomial of degree $n$. Let $\mathrm{L}/\mathrm{K}$ be the extension of degree $n$ defined by $f$. Show that for every polynomial $h(\mathrm{X})$ of degree $n$ that is close enough to $f$, $h(\mathrm{X})$ is irreducible and the extension $\mathrm{L}_h/\mathrm{K}$ defined by $h$ is isomorphic to $\mathrm{L}$.
>
> (ii) Note that the $p$-adic valuation on $\mathbb{Q}_p$ extends uniquely to a valuation on $\overline{\mathbb{Q}}_p$; the latter is still called the $p$-adic valuation. Complete $\overline{\mathbb{Q}}_p$ with respect to the $p$-adic valuation and call it $C$. Use (i) to prove that $C$ is algebraically closed. (People often write $\mathbb{C}_p$ for this $C$.)

**Proof:**
**(i)** Let $x_1,\dots,x_n$ be the roots of $f$. Since $f$ is separable, $\|x_i-x_j\|>0$ for $i\ne j$. Choose $\varepsilon>0$ such that
$$
\varepsilon<\min_{i\ne j}\|x_i-x_j\|.
$$
If $h$ is sufficiently close to $f$, its roots $y_1,\dots,y_n$ can be rearranged so that $\|y_i-x_i\|<\varepsilon$ for every $i$ (by the continuity of simple roots of $f$ with respect to the coefficients, if the coefficients are close enough, then so are the roots). In particular,
$$
\|y_1-x_1\|<\|y_1-x_i\| \qquad (i\ge2).
$$
By Krasner's lemma, $x_1\in K(y_1)$. Hence $K(x_1)\subseteq K(y_1)$. $K(x_{1})$ has extension degree $n$ and $K(y_{1})$ has extension degree at most $n$, so $K(x_1)=K(y_1)$.

Therefore,  since $K[X]/(f(X))\cong L\cong K(x_{1}) = K(y_{1})\cong L_{h}\cong  K[X]/(h(X))$, we have $h$ is irreducible and $L_h\cong L$.

>[!remark] Remark
>Similarly we have $K(x_i)=K(y_i)\quad(i\geq2)$, so $K(y_{1},\dots, y_{n}) = K(x_{1},\dots ,x_{n})$. Therefore we have $h$ is separable and has the same splitting field as $f$'s.
>
>It is worth noting that $L_h$ and $L$ are not necessarily the same subfield of a fixed algebraic closure $\overline K$ of $K$ since $L$ or $L_{n}$ can be realized by add any roots of $f$ and $h$, not necessarily the corresponding ones. While their splitting fields are the same subfield of $\overline K$ because they contain all roots of $f$ or $h$.

**(ii)** Let $f$ be a non-constant irreducible polynomial in $C[X]$. By the density of $\overline{ \mathbb{Q}_{p} }$ in $C$, we may choose a polynomial $h\in\overline{\mathbb{Q}}_p[X]$ of the same degree whose coefficients are sufficiently close to those of $f$. By (i), since $f$ is separable ($\operatorname{char}C=0$, thus $C$ is perfect) and irreducible in $C$, then $h$ is irreducible in $C$. In particular, $h$ is irreducible in $\overline{ \mathbb{Q}_{p} }$, thus $\operatorname{deg}f=\operatorname{deg}h=1$ for $\overline{ \mathbb{Q}_{p} }$ is algebraically closed.

Therefore, every non-constant irreducible polynomial in $C[X]$ is of degree $1$, i.e. $C$ is algebraically closed.
___

> [!problem] Problem 3
> Fix an integer $n \ge 2$ and an algebraic closure $\overline{\mathbb{Q}}_p$ of the field $\mathbb{Q}_p$ of $p$-adic numbers. Let $L_n$ be a degree $n$ extension of $\mathbb{Q}_p$ in $\overline{\mathbb{Q}}_p$ such that $(p) \subset \mathbb{Z}_p$ is unramified in $L_n$. Write $\mu(L_n)$ for the (multiplicative) torsion subgroup of $L_n^\times$, namely the group of all roots of unity in $L_n$, and $\mu_N$ for the subgroup of $N$-th roots of unity in $\overline{\mathbb{Q}}_p^\times$.
>
> (1) Show that $\mu(L_n) = \mu_{p^n-1}$ if $p$ is odd, and $\mu(L_n) = \mu_{2(p^n-1)}$ if $p$ is even (namely if $p=2$).
> **Hint:** Hensel's lemma can help to show $\supset$.
>
> (2) Prove that $L_n = \mathbb{Q}_p(\mu_{p^n-1})$.
> (Note: This implies that there exists a unique degree $n$ unramified extension of $\mathbb{Q}_p$ in $\overline{\mathbb{Q}}_p$. It also follows that such an extension is Galois over $\mathbb{Q}_p$.)

**Proof:**
**(1)** Let $\mathcal{O}_{L_n}$ be the ring of integers of $L_n$ and let $\mathfrak{m}_{L_n}$ be its maximal ideal. Since $L_n/\mathbb{Q}_p$ is unramified of degree $n$, its residue field is
$$
\mathcal{O}_{L_n}/\mathfrak{m}_{L_n}\cong\mathbb{F}_{p^n}.
$$
Hence
$$
\left(\mathcal{O}_{L_n}/\mathfrak{m}_{L_n}\right)^\times
$$
has order $p^n-1$.

First suppose that $\zeta\in\mu(L_n)$ has order prime to $p$. Its reduction $\overline{\zeta}$ is nonzero, and reduction is injective on roots of unity of order prime to $p$. Thus
$$
\operatorname{ord}(\zeta)\mid p^n-1.
$$
Moreover, every element of $\mathbb{F}_{p^n}^\times$ has a unique lift to a root of unity of order prime to $p$ by Hensel's lemma. Therefore
$$
\mu_{p^n-1}\subseteq\mu(L_n).
$$

If $p$ is odd, $p^n-1$ is even. There are no nontrivial $p$-power roots of unity in an unramified extension of $\mathbb{Q}_p$: a $p$-power root of unity would reduce to $1$, while the group $1+\mathfrak{m}_{L_n}$ is torsion-free for $p$ odd. Hence every root of unity in $L_n$ has order dividing $p^n-1$, and
$$
\mu(L_n)=\mu_{p^n-1}.
$$

If $p=2$, the same argument shows that every root of unity of odd order belongs to $\mu_{2^n-1}$. The only $2$-power roots of unity in an unramified extension are $\pm1$. Hence
$$
\mu(L_n)=\mu_{2(2^n-1)}.
$$

**(2)** Put $m=p^n-1$. By (1), $\mu_m\subset L_n$, so
$$
\mathbb{Q}_p(\mu_m)\subseteq L_n.
$$

Let $\zeta_m$ be a primitive $m$-th root of unity. Its reduction has order $m$ in $\mathbb{F}_{p^n}^\times$. The order of $p$ modulo $m$ is exactly $n$: indeed,
$$
p^n\equiv1\pmod m,
$$
while for $1\le d<n$,
$$
0<p^d-1<p^n-1=m,
$$
so $p^d\not\equiv1\pmod m$. Therefore the minimal polynomial of $\overline{\zeta}_m$ over $\mathbb{F}_p$ has degree $n$.

By Hensel's lemma, $\zeta_m$ has the same degree over $\mathbb{Q}_p$, so
$$
[\mathbb{Q}_p(\mu_m):\mathbb{Q}_p]=n.
$$
Since $[L_n:\mathbb{Q}_p]=n$ and
$$
\mathbb{Q}_p(\mu_m)\subseteq L_n,
$$
we obtain
$$
L_n=\mathbb{Q}_p(\mu_{p^n-1}).
$$

For $p=2$, this is unchanged by the extra factor $2$, since $-1\in\mathbb{Q}_2$ and hence
$$
\mathbb{Q}_2(\mu_{2(2^n-1)})
=\mathbb{Q}_2(\mu_{2^n-1}).
$$