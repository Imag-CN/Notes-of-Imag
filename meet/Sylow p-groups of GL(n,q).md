___

> [!problem]
> Let $p$ be a prime, $n,r$ positive integers, and $q = p^r$. Find a Sylow $p$-subgroup of the finite group $G=\operatorname{GL}(n,q)$.

**Proof:**
Compute the order of the group:
$$
|G| = (q^n-1)(q^n-q)\cdots(q^n-q^{n-1})=q^{n(n-1)/2}\cdot(q^{n}-1)(q^{n-1}-1)\cdots(q-1).
$$
The $p$-part of the order is
$$
q^{n(n-1)/2} = p^{r n(n-1)/2},
$$

because $q^{n-i}-1$ is coprime to $p$ for $i \ge 1$.

Let $U$ be the set of upper unitriangular matrices (diagonal entries $1$, strictly upper triangular part arbitrary). $U$ is a subgroup, and $|U| = q^{n(n-1)/2}$. Hence $|U|$ equals the $p$-part of $|G|$, so $U$ is a Sylow $p$-subgroup of $G$.
___

>[!remark]
>To find the number $n_{p}$ of Sylow $p$-groups of $G$, we can compute the normalizer $N_{G}(U)$ of $U$. Then $n_{p}=\lvert G \rvert / \lvert N_{G}(U) \rvert$ due to the counting formular. 

**Claim:** $N_G(U) = B$, where $G = \operatorname{GL}(n,q)$ and $B$ is the Borel subgroup (invertible upper-triangular matrices).

**Proof:**
For $b \in B$, $u \in U$, conjugate $b u b^{-1}$ remains upper triangular with diagonal 1. So $B \subseteq N_G(U)$.

Let $g \in N_G(U)$. For each $1 \le i < n$, take $u_i = I + E_{i,i+1} \in U$. Since $g u_i g^{-1} \in U$, it is strictly upper triangular. The $(j,i)$ entry of $g u_i g^{-1}$ is
$$
(g u_i g^{-1})_{ji} = \sum_{k,l} g_{jk} (u_i)_{kl} (g^{-1})_{li}.
$$
In particular, for $j > i$, requiring it to be $0$ for all such $u_i$ forces $g_{j,i+1}=0$ whenever $j > i+1$. This implies $g$ is upper triangular, i.e. $g \in B$.

Thus $N_G(U) = B$. Then $\lvert B \rvert=(q-1)^{n}\cdot q^{n(n-1)/2}$, and $|G| / |B|$ gives the number of Sylow $p$-groups of $G$.



