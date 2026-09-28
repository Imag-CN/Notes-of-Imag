___

>[!problem] Problem 1
>Let $\zeta_n$ denote a primitive $n$-th root of unity (so that powers of $\zeta_n$ give all $n$-th roots of unity). Consider $L = \mathbb{Q}(\zeta_n)$ over $K = \mathbb{Q}$. This is a Galois extension and there is an isomorphism (which deserves to be called "canonical"; you may review this from [L], VI.3)
>$$
>i: \operatorname{Gal}(\mathbb{Q}(\zeta_n)/\mathbb{Q}) \xrightarrow{\sim} (\mathbb{Z}/n\mathbb{Z})^\times
>$$
>characterized by the equation that
>$$
>\sigma(\zeta_n) = \zeta_n^{i(\sigma)}, \quad \forall \sigma \in \operatorname{Gal}(\mathbb{Q}(\zeta_n)/\mathbb{Q}).
>$$
>(Note that $\zeta_n^i$ depends only on $i \bmod n$, so this makes sense.)
>
>Now let $p$ be a prime number coprime to $n$. You may accept that $p$ is unramified in $\mathbb{Q}(\zeta_n)/\mathbb{Q}$. (You need not justify this because this becomes simpler to check when we learn discriminants.)
>
>(i) Prove that the Frobenius element $(p, \mathbb{Q}(\zeta_n)/\mathbb{Q})$ maps to $p \in (\mathbb{Z}/n\mathbb{Z})^\times$ under the map $i$. (Feel free to use the fact that the integral closure of $\mathbb{Z}$ in $\mathbb{Q}(\zeta_n)$ is $\mathbb{Z}[\zeta_n]$ without justification, which we verified when $n$ is a prime.)
>
>(ii) Using (i) show that $p$ splits completely in $\mathbb{Q}(\zeta_n)$ if and only if $p \equiv 1 \bmod n$.

**Proof:**
**(i)** Let $\mathfrak{p}$ be a prime of $\mathbb{Q}(\zeta_n)$ above $p$. Since $p$ is unramified, the Frobenius element $\operatorname{Frob}_{\mathfrak p}$ satisfies
$$
\operatorname{Frob}_{\mathfrak p}(x)\equiv x^p\pmod{\mathfrak p}
$$
for every $x\in\mathbb{Z}[\zeta_n]$.

Applying this to $\zeta_n$ gives
$$
\operatorname{Frob}_{\mathfrak p}(\zeta_n)
\equiv \zeta_n^p\pmod{\mathfrak p}.
$$
Both sides are $n$-th roots of unity. Since $p\nmid n$, the polynomial $X^n-1$ has distinct roots modulo $\mathfrak p$, so the congruence implies
$$
\operatorname{Frob}_{\mathfrak p}(\zeta_n)=\zeta_n^p.
$$
By the definition of the canonical isomorphism $i$,
$$
i(\operatorname{Frob}_{\mathfrak p})\equiv p\pmod n.
$$

**(ii)** For an unramified prime, $p$ splits completely in $L/\mathbb{Q}$ if and only if its Frobenius element is the identity. By (i),
$$
\operatorname{Frob}_{\mathfrak p}=\operatorname{id}
\iff
i(\operatorname{Frob}_{\mathfrak p})=1
\iff
p\equiv1\pmod n.
$$
Therefore,
$$
p\text{ splits completely in }\mathbb{Q}(\zeta_n)
\iff
p\equiv1\pmod n.
$$

>[!remark] Remark
>The prime $p$ is inert in $\mathbb{Q}(\zeta_n)$ if and only if the Frobenius element generates the whole Galois group. 
>
>By (i), $$ i(\operatorname{Frob}_{\mathfrak p})\equiv p\pmod n. $$ Hence $$ p\text{ is inert in }\mathbb{Q}(\zeta_n) \iff \langle p\bmod n\rangle=(\mathbb{Z}/n\mathbb{Z})^\times \iff \operatorname{ord}_n(p)=\varphi(n). $$ Thus $p$ is inert if and only if $p$ has multiplicative order $\varphi(n)$ modulo $n$, i.e. $p\bmod n$ is a generator of $(\mathbb{Z}/n\mathbb{Z})^\times$.

___

>[!problem] Problem 2 (Continue from the previous problem.)
>Assume that $n = q$ is a prime such that $q \equiv 1 \bmod 4$. Recall there is a canonical isomorphism
   $$ i: \operatorname{Gal}(\mathbb{Q}(\zeta_q)/\mathbb{Q}) \xrightarrow{\sim} (\mathbb{Z}/q\mathbb{Z})^\times $$
   sending the Frobenius element $(p, \mathbb{Q}(\zeta_q)/\mathbb{Q})$ to $p \in (\mathbb{Z}/q\mathbb{Z})^\times$ for every $p \neq q$. Let's take on faith the fact that $\mathbb{Q}(\sqrt{q}) \subset \mathbb{Q}(\zeta_q)$. (We'll be able to show this later in the course.) Now fix an odd prime $p \neq q$. Use the isomorphism $i$ to do the following.
>
>(i) Verify that $p$ is a square modulo $q$ if and only if $(p, \mathbb{Q}(\zeta_q)/\mathbb{Q})$ fixes the subfield $\mathbb{Q}(\sqrt{q})$ element-wise.
>
>(ii) Check that $(p, \mathbb{Q}(\zeta_q)/\mathbb{Q})$ fixes the subfield $\mathbb{Q}(\sqrt{q})$ element-wise if and only if $p$ splits (completely) in $\mathbb{Q}(\sqrt{q})$.
>
>(iii) Deduce from (i), (ii), and Problem Set 02 #4 that $p$ is a square modulo $q$ if and only if $q$ is a square modulo $p$, namely
>$$
>\left(\frac{p}{q}\right) \left(\frac{q}{p}\right) = 1.
>$$

**Proof:**
**(i)** Under the isomorphism
$$
i:\operatorname{Gal}(\mathbb{Q}(\zeta_q)/\mathbb{Q})\xrightarrow{\sim}(\mathbb{Z}/q\mathbb{Z})^\times,
$$
the subgroup fixing $\mathbb{Q}(\sqrt q)$ corresponds to the subgroup of squares in $(\mathbb{Z}/q\mathbb{Z})^\times$.

Since
$$
[\mathbb{Q}(\zeta_q):\mathbb{Q}]=q-1,
\qquad
[\mathbb{Q}(\sqrt q):\mathbb{Q}]=2,
$$
the subgroup fixing $\mathbb{Q}(\sqrt q)$ has index $2$. Since $q\equiv1\pmod4$, $(\mathbb{Z}/q\mathbb{Z})^\times$ is cyclic of even order $q-1$, and its unique subgroup of index $2$ is the subgroup of squares.

By the previous problem,
$$
i\left(\operatorname{Frob}_p\right)=p\pmod q.
$$
Therefore,
$$
p\text{ is a square modulo }q
\iff
\operatorname{Frob}_p\text{ fixes }\mathbb{Q}(\sqrt q)\text{ element-wise}.
$$

**(ii)** Since $p\neq q$, we have $p\nmid q$, so $p$ is unramified in $\mathbb{Q}(\sqrt q)$.

For a quadratic extension, an unramified prime splits completely if and only if its Frobenius element is the identity. The Frobenius in $\mathbb{Q}(\zeta_q)/\mathbb{Q}$ fixes $\mathbb{Q}(\sqrt q)$ element-wise if and only if its restriction to $\mathbb{Q}(\sqrt q)$ is the identity. Hence
$$
\operatorname{Frob}_p\text{ fixes }\mathbb{Q}(\sqrt q)
\iff
p\text{ splits completely in }\mathbb{Q}(\sqrt q).
$$
**(iii)** By (i) and (ii),
$$
p\text{ is a square modulo }q
\iff
p\text{ splits in }\mathbb{Q}(\sqrt q).
$$

Since $q\equiv1\pmod4$, Problem Set 02 #4 applied with $d=q$ gives, for $p\neq2,q$,
$$
p\text{ splits in }\mathbb{Q}(\sqrt q)
\iff
\left(\frac{q}{p}\right)=1.
$$
Thus
$$
p\text{ is a square modulo }q
\iff
\left(\frac{q}{p}\right)=1
\iff
q\text{ is a square modulo }p.
$$

Equivalently,
$$
\left(\frac{p}{q}\right)\left(\frac{q}{p}\right)=1.
$$

(This proves the quadratic reciprocity law in the case $q\equiv1\pmod4$ without using quadratic reciprocity itself.)

>[!remark] Remark
>Suppose $q\equiv3\pmod4$. Then $\mathbb{Q}(\sqrt{-q})\subset\mathbb{Q}(\zeta_q)$.
>
>As before, the subgroup of $\operatorname{Gal}(\mathbb{Q}(\zeta_q)/\mathbb{Q})$ fixing $\mathbb{Q}(\sqrt{-q})$ corresponds under $i$ to the unique subgroup of index $2$ in $(\mathbb{Z}/q\mathbb{Z})^\times$, namely the subgroup of squares.
>
>Hence, for $p\neq q$,
>$$
>p\text{ is a square modulo }q
>\iff
>\operatorname{Frob}_p\text{ fixes }\mathbb{Q}(\sqrt{-q})
>\iff
>p\text{ splits in }\mathbb{Q}(\sqrt{-q}).
>$$
>
>Applying Problem Set 02 #4 with $d=-q$, we get
>$$
>p\text{ splits in }\mathbb{Q}(\sqrt{-q})
>\iff
>\left(\frac{-q}{p}\right)=1.
>$$
>
>Therefore
>$$
>\left(\frac{p}{q}\right)=1
>\iff
>\left(\frac{-q}{p}\right)=1.
>$$
>Since both Legendre symbols are $\pm1$,
>$$
>\left(\frac{p}{q}\right)\left(\frac{-q}{p}\right)=1
>$$

___
































   * **Bonus:** When $q \equiv 3 \bmod 4$, a similar argument with $\mathbb{Q}(\sqrt{-q})$ in place of $\mathbb{Q}(\sqrt{q})$ shows that
   $$ \left(\frac{p}{q}\right) \left(\frac{-q}{p}\right) = 1 $$
   but you need not include this in your solution. [PROCEED TO PAGE 2.]