___

> [!problem] Problem 1
> Elaborate on the proof of [S], I.3, Proposition 5 on p.11; in particular, check that
> $$
>(\mathfrak{a}\cdot\mathfrak{b})_{\mathfrak{p}}=\mathfrak{a}_{\mathfrak{p}}\cdot\mathfrak{b}_{\mathfrak{p}},\qquad(\mathfrak{a}:\mathfrak{b})_{\mathfrak{p}}=(\mathfrak{a}_{\mathfrak{p}}:\mathfrak{b}_{\mathfrak{p}}),
>$$
> and explain how “The proposition follows from this by localisation.” (We admit that the proof when $A$ is a DVR is understood; no need to provide any details on this case. Also, you need not check that
> $$
>(\mathfrak{a}+\mathfrak{b})_{\mathfrak{p}}=\mathfrak{a}_{\mathfrak{p}}+\mathfrak{b}_{\mathfrak{p}},
>$$
> as this is basically the same deal.) $^1$
> 
> The following two problems are taken from exercises in Chapter 9 of [AM].

**Proof:**
Let $A$ be a DVR, $\mathfrak{p} \subset A$ a prime ideal, and $\mathfrak{a}, \mathfrak{b} \subset A$ two ideals. We verify the two identities. 

**1. $(\mathfrak{a} \cdot \mathfrak{b})_{\mathfrak{p}} = \mathfrak{a}_{\mathfrak{p}} \cdot \mathfrak{b}_{\mathfrak{p}}$**

$(\subseteq)$: Take $\dfrac{\sum a_i b_i}{s} \in (\mathfrak{a} \cdot \mathfrak{b})_{\mathfrak{p}}$ with $a_i \in \mathfrak{a}$, $b_i \in \mathfrak{b}$, $s \notin \mathfrak{p}$. Write it as $\sum \dfrac{a_i}{1} \cdot \dfrac{b_i}{s} \in \mathfrak{a}_{\mathfrak{p}} \cdot \mathfrak{b}_{\mathfrak{p}}$.

$(\supseteq)$: Take a generator $\dfrac{a}{s} \cdot \dfrac{b}{t} \in \mathfrak{a}_{\mathfrak{p}} \cdot \mathfrak{b}_{\mathfrak{p}}$. Then $\dfrac{a}{s} \cdot \dfrac{b}{t} = \dfrac{ab}{st}$ with $ab \in \mathfrak{a} \cdot \mathfrak{b}$ and $st \notin \mathfrak{p}$, so it lies in $(\mathfrak{a} \cdot \mathfrak{b})_{\mathfrak{p}}$. Finite sums follow similarly.

Thus equality holds.

**2. $(\mathfrak{a} : \mathfrak{b})_{\mathfrak{p}} = (\mathfrak{a}_{\mathfrak{p}} : \mathfrak{b}_{\mathfrak{p}})$**

$(\subseteq)$: Take $\dfrac{x}{s} \in (\mathfrak{a} : \mathfrak{b})_{\mathfrak{p}}$ with $x \in (\mathfrak{a} : \mathfrak{b})$, $s \notin \mathfrak{p}$. For any $\dfrac{b}{t} \in \mathfrak{b}_{\mathfrak{p}}$, we have $\dfrac{x}{s} \cdot \dfrac{b}{t} = \dfrac{xb}{st}$. Since $xb \in \mathfrak{a}$, $st\not\in \mathfrak{p}$, we have $\dfrac{xb}{st}$ lies in $\mathfrak{a}_{\mathfrak{p}}$, hence $\dfrac{x}{s} \in (\mathfrak{a}_{\mathfrak{p}} : \mathfrak{b}_{\mathfrak{p}})$.

$(\supseteq)$: Take $\dfrac{x}{s} \in (\mathfrak{a}_{\mathfrak{p}} : \mathfrak{b}_{\mathfrak{p}})$. For each $b \in \mathfrak{b}$, consider $\dfrac{x}{s} \cdot \dfrac{b}{1} = \dfrac{xb}{s} \in \mathfrak{a}_{\mathfrak{p}}$, so there exists $u_b \notin \mathfrak{p}$ with $u_b x b \in \mathfrak{a}$. Since $\mathfrak{b}$ is finitely generated (as $A$ is a DVR, DVRs are Noetherian, and every ideal of a Noetherian ring is finitely generated), take generators $b_1,\dots,b_n$ and let $t = u_{b_1}\cdots u_{b_n} \notin \mathfrak{p}$. Then $t x b_i \in \mathfrak{a}$ for all $i$, so $t x \mathfrak{b} \subseteq \mathfrak{a}$, i.e., $t x \in (\mathfrak{a} : \mathfrak{b})$. Hence $\dfrac{x}{s} = \dfrac{t x}{t s} \in (\mathfrak{a} : \mathfrak{b})_{\mathfrak{p}}$.

Thus equality holds.

**3. Why "The proposition follows from this by localisation"**

In a Dedekind domain, localising at any prime ideal gives a DVR. It is known that every nonzero fractional ideal of a DVR is invertible. The three identities verified above show that the operations of product, sum, and quotient ideal commute with localisation. Consequently, a fractional ideal is invertible globally iff it is invertible at every localisation.

Therefore, for any nonzero fractional ideal of a Dedekind domain, localising at each prime yields an invertible ideal in the corresponding DVR, and by the local-global principle, the original ideal must be invertible.
___

> [!problem] Problem 2
> Let $A$ be a Dedekind domain, $S$ a multiplicatively closed subset such that $S^{-1}A$ is not a field.
> (i) Show that $S^{-1}A$ is a Dedekind domain.
> (ii) Show that the extension of ideals (and similarly for fractional ideals) induces a surjection from the ideal class group of $A$ to that of $S^{-1}A$.

**Proof:**
**(i)** A Dedekind domain is Noetherian, integrally closed, and of Krull dimension $\le 1$. Since $A$ is Noetherian, $S^{-1}A$ is Noetherian. Since $A$ is integrally closed in its fraction field $K$, any element $x\in K$ integral over $S^{-1}A$ is also integral over $A$, hence $x\in A\subset S^{-1}A$; thus $S^{-1}A$ is integrally closed. Prime ideals of $S^{-1}A$ correspond bijectively to primes $\mathfrak{p}\subset A$ with $\mathfrak{p}\cap S=\varnothing$. As $A$ is Dedekind, every nonzero such $\mathfrak{p}$ is maximal, so its image in $S^{-1}A$ is also maximal. Hence $\dim S^{-1}A\le 1$. Since $S^{-1}A$ is not a field, it has a nonzero prime ideal, so $\dim S^{-1}A=1$. Therefore $S^{-1}A$ is a Dedekind domain.

**(ii)** Let $\varphi:I(A)\to I(S^{-1}A)$ be the extension map $\mathfrak{a}\mapsto S^{-1}\mathfrak{a}$. This sends principal ideals to principal ideals, hence induces a homomorphism $\overline{\varphi}:\operatorname{Cl}(A)\to\operatorname{Cl}(S^{-1}A)$. To show surjectivity, take any fractional ideal $\mathfrak{b}\subset S^{-1}A$. Its contraction $\mathfrak{a}=\mathfrak{b}\cap A$ is a fractional ideal of $A$, and by standard localization theory we have $\mathfrak{b}=S^{-1}\mathfrak{a}$. Thus every fractional ideal of $S^{-1}A$ is extended from $A$, so $\varphi$ is surjective on fractional ideals. Consequently $\overline{\varphi}$ is surjective on class groups.