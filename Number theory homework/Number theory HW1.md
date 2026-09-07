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
Let $A$ be a commutative ring, $\mathfrak{p} \subset A$ a prime ideal, and $\mathfrak{a}, \mathfrak{b} \subset A$ two ideals. We verify the two identities.

**1. $(\mathfrak{a} \cdot \mathfrak{b})_{\mathfrak{p}} = \mathfrak{a}_{\mathfrak{p}} \cdot \mathfrak{b}_{\mathfrak{p}}$**

$(\subseteq)$: Take $\dfrac{\sum a_i b_i}{s} \in (\mathfrak{a} \cdot \mathfrak{b})_{\mathfrak{p}}$ with $a_i \in \mathfrak{a}$, $b_i \in \mathfrak{b}$, $s \notin \mathfrak{p}$. Write it as $\sum \dfrac{a_i}{1} \cdot \dfrac{b_i}{s} \in \mathfrak{a}_{\mathfrak{p}} \cdot \mathfrak{b}_{\mathfrak{p}}$.

$(\supseteq)$: Take a generator $\dfrac{a}{s} \cdot \dfrac{b}{t} \in \mathfrak{a}_{\mathfrak{p}} \cdot \mathfrak{b}_{\mathfrak{p}}$. Then $\dfrac{a}{s} \cdot \dfrac{b}{t} = \dfrac{ab}{st}$ with $ab \in \mathfrak{a} \cdot \mathfrak{b}$ and $st \notin \mathfrak{p}$, so it lies in $(\mathfrak{a} \cdot \mathfrak{b})_{\mathfrak{p}}$. Finite sums follow similarly.

Thus equality holds.

**2. $(\mathfrak{a} : \mathfrak{b})_{\mathfrak{p}} = (\mathfrak{a}_{\mathfrak{p}} : \mathfrak{b}_{\mathfrak{p}})$**

$(\subseteq)$: Take $\dfrac{x}{s} \in (\mathfrak{a} : \mathfrak{b})_{\mathfrak{p}}$ with $x \in (\mathfrak{a} : \mathfrak{b})$, $s \notin \mathfrak{p}$. For any $\dfrac{b}{t} \in \mathfrak{b}_{\mathfrak{p}}$, we have $\dfrac{x}{s} \cdot \dfrac{b}{t} = \dfrac{xb}{st}$. Since $xb \in \mathfrak{a}$, this lies in $\mathfrak{a}_{\mathfrak{p}}$, hence $\dfrac{x}{s} \in (\mathfrak{a}_{\mathfrak{p}} : \mathfrak{b}_{\mathfrak{p}})$.

$(\supseteq)$: Take $\dfrac{x}{s} \in (\mathfrak{a}_{\mathfrak{p}} : \mathfrak{b}_{\mathfrak{p}})$. For each $b \in \mathfrak{b}$, consider $\dfrac{x}{s} \cdot \dfrac{b}{1} = \dfrac{xb}{s} \in \mathfrak{a}_{\mathfrak{p}}$, so there exists $u_b \notin \mathfrak{p}$ with $u_b x b \in \mathfrak{a}$. If $\mathfrak{b}$ is finitely generated (as in the proposition's context), take generators $b_1,\dots,b_n$ and let $t = u_{b_1}\cdots u_{b_n} \notin \mathfrak{p}$. Then $t x b_i \in \mathfrak{a}$ for all $i$, so $t x \mathfrak{b} \subseteq \mathfrak{a}$, i.e., $t x \in (\mathfrak{a} : \mathfrak{b})$. Hence $\dfrac{x}{s} = \dfrac{t x}{t s} \in (\mathfrak{a} : \mathfrak{b})_{\mathfrak{p}}$.

Thus equality holds.

**3. Why "The proposition follows from this by localisation"**

Proposition 5 states that certain properties of ideals (e.g., being primary, being a product, etc.) hold if and only if they hold after localising at every maximal (or prime) ideal. The two equalities above show that the operations of sum, product, and quotient commute with localisation. Therefore, checking these operations locally reduces to checking them in the local rings $A_{\mathfrak{p}}$. When $A$ is a DVR, the structure is simple enough to verify directly. By localising at each prime, the general case follows from the DVR case via these commutation relations.