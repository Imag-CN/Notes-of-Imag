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
