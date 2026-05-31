___

> [!problem] Problem 1
> A complex number is called an algebraic number if it is a root of a nonzero
> polynomial over $\mathbb{Q}$. Prove that all algebraic numbers form a subfield of $\mathbb{C}$.

**Proof:**
Can use resultant. Or use the fact that $x$ is algebraic iff $\mathbb{Q}[x]$ is a finitely generated $\mathbb{Q}$-module.
___

> [!problem] Problem 2
> Let $a_1,\ldots,a_n \in \mathbb{C}$. We denote
> $$
> \mathbb{Q}(a_1,\ldots,a_n)
> $$
> to be the smallest subfield of $\mathbb{C}$ containing all $a_1,\ldots,a_n$.
> (i) Prove that every element of $\mathbb{Q}(a_1,\ldots,a_n)$ can be expressed as
> $$\frac{P(a_1,\ldots,a_n)}{Q(a_1,\ldots,a_n)}$$
> where $P,Q \in \mathbb{Q}[x_1,\ldots,x_n]$.
> (ii) Suppose the numbers $a_1,\ldots,a_n$ are all algebraic numbers. Prove that every element of $\mathbb{Q}(a_1,\ldots,a_n)$ can be expressed as $P(a_1,\ldots,a_n)$ where $P \in \mathbb{Q}[x_1,\ldots,x_n]$.

**Proof:**
**(i)** $\mathbb{Q}(a_1,\ldots,a_n)$ is the field of fractions of the ring $\mathbb{Q}[a_1,\ldots,a_n]$. Every element in this ring is $P(a_1,\ldots,a_n)$ for some $P \in \mathbb{Q}[x_1,\ldots,x_n]$. Therefore, any element of the field is a quotient of two such evaluations: $P(a_1,\ldots,a_n)/Q(a_1,\ldots,a_n)$, with $Q(a_1,\ldots,a_n) \neq 0$.

**(ii)** Since $a_1,\ldots,a_n$ are algebraic, $\mathbb{Q}(a_1,\ldots,a_n)$ is a finite algebraic extension of $\mathbb{Q}$. For any $x \in \mathbb{Q}(a_1,\ldots,a_n)$, the powers $1, x, x^2, \ldots$ are linearly dependent over $\mathbb{Q}$, so $x$ satisfies a nonzero polynomial $f(t) \in \mathbb{Q}[t]$: $f(x)=0$. This implies $x^{-1}$ (if $x \neq 0$) is a polynomial in $x$ with rational coefficients. Consequently, the ring $\mathbb{Q}[a_1,\ldots,a_n]$ is already a field. Thus, every element of $\mathbb{Q}(a_1,\ldots,a_n)$ is itself of the form $P(a_1,\ldots,a_n)$ for some $P \in \mathbb{Q}[x_1,\ldots,x_n]$.
___

> [!problem] Problem 3
> Let $\omega = e^{\frac{2\pi i}{3}} \in \mathbb{C}$. Let $a$ be the unique real number such that $a^3 = 2$.
> (i) Prove that the six numbers
> $$
> 1, a, a^2, \omega, \omega a, \omega a^2
> $$
> are linearly independent over $\mathbb{Q}$.
> (ii) Prove that
> $$
> \operatorname{Aut}\left( \mathbb{Q}(a, \omega a, \omega^2 a) / \mathbb{Q} \right) \cong S_3.
> $$

**Proof:**
**(i)** The polynomial $x^3-2$ is irreducible over $\mathbb{Q}$ (Eisenstein), so $[\mathbb{Q}(a):\mathbb{Q}]=3$ with basis $\{1, a, a^2\}$. Over $\mathbb{Q}(a)$, the polynomial $x^2+x+1$ (minimal polynomial of $\omega$) remains irreducible because $\mathbb{Q}(a)\subset\mathbb{R}$ and $\omega\notin\mathbb{R}$. Hence $[\mathbb{Q}(a,\omega):\mathbb{Q}(a)]=2$, and $[\mathbb{Q}(a,\omega):\mathbb{Q}]=6$.

The set $\{1, a, a^2, \omega, \omega a, \omega a^2\}$ spans $\mathbb{Q}(a,\omega)$: any element is $f(a)+\omega g(a)$ with $\deg f,g \leq 2$. Since the dimension is 6, this spanning set of size 6 is a basis, hence linearly independent over $\mathbb{Q}$.

**(ii)** The field $L=\mathbb{Q}(a,\omega a,\omega^2 a)$ is the splitting field of $x^3-2$ over $\mathbb{Q}$, so $L=\mathbb{Q}(a,\omega)$. Since $x^3-2$ is separable, $|\operatorname{Aut}(L/\mathbb{Q})| = [L:\mathbb{Q}] = 6$.

Any automorphism $\sigma \in \operatorname{Aut}(L/\mathbb{Q})$ permutes the three roots $\{a,\omega a,\omega^2 a\}$ and sends $\omega$ to $\omega$ or $\omega^2$. The map $\sigma \mapsto$ (its permutation of the roots) gives an injective homomorphism $\operatorname{Aut}(L/\mathbb{Q}) \hookrightarrow S_3$. By counting orders, it is an isomorphism: $\operatorname{Aut}(L/\mathbb{Q}) \cong S_3$.
___

