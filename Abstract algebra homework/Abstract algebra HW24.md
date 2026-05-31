___

> [!problem] Problem 1
> Let $K$ be a field of characteristic zero. Let $P(x) \in K[x]$ be an irreducible polynomial. Let $L$ be a splitting field of $P(x)$. Let $a_1, \ldots, a_n$ be roots of $P(x)$ in $L$.
> (i) Prove that $\operatorname{Gal}(L/K)$ permutes $a_1, \ldots, a_n$, so that we obtain a group homomorphism $\operatorname{Gal}(L/K) \to S_n$.
> (ii) Prove that the group homomorphism $\operatorname{Gal}(L/K) \to S_n$ is injective.
> (iii) Prove that $\sigma \in S_n$ is in the image of $\operatorname{Gal}(L/K) \to S_n$ if and only if
> $$
> f(a_1, \ldots, a_n) = f(a_{\sigma(1)}, \ldots, a_{\sigma(n)})
> $$
> for all $f \in K[x_1, \ldots, x_n]$ such that $f(a_1, \ldots, a_n) \in K$.

**Proof:**
**(i)** For any $\sigma \in \operatorname{Gal}(L/K)$ and any root $a_i$, we have $P(\sigma(a_i)) = \sigma(P(a_i)) = 0$. Thus $\sigma$ permutes the roots $\{a_1,\dots,a_n\}$, giving a homomorphism $\operatorname{Gal}(L/K) \to S_n$.

**(ii)** If $\sigma$ fixes all roots $a_1,\dots,a_n$, then it fixes every element of $L$ because $L = K(a_1,\dots,a_n)$. Hence $\sigma = \mathrm{id}$, so the homomorphism is injective.

**(iii)** Let $H$ be the image of $\operatorname{Gal}(L/K)$ in $S_n$. For any $\sigma \in H$ and any $f \in K[x_1,\dots,x_n]$ with $f(a_1,\dots,a_n) \in K$,
$$
f(a_{\sigma(1)},\dots,a_{\sigma(n)}) = \sigma(f(a_1,\dots,a_n)) = f(a_1,\dots,a_n),
$$
so $\sigma$ satisfies the condition.

Conversely, suppose $\tau \in S_n$ satisfies $f(a_1,\dots,a_n) = f(a_{\tau(1)},\dots,a_{\tau(n)})$ for all such $f$. Define a map $\tilde{\tau}: L \to L$ by $\tilde{\tau}(a_i) = a_{\tau(i)}$ and extend as a $K$-algebra homomorphism. For any relation $h(a_1,\dots,a_n)=0$ with $h \in K[x_1,\dots,x_n]$, we have $0 \in K$, so by hypothesis $h(a_{\tau(1)},\dots,a_{\tau(n)})=0$. Thus $\tilde{\tau}$ is well defined and is a $K$-automorphism of $L$, i.e., $\tilde{\tau} \in \operatorname{Gal}(L/K)$ and maps to $\tau$. Hence $\tau \in H$.
___

> [!problem] Problem 2
> Use the Galois correspondence to build the bijection between subgroups of
> $D_{4}$ and subfields of $\mathbb{Q}(\sqrt[4]{5}, \sqrt{-1})$.

