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

