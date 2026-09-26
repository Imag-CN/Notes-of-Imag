___

>[!problem] 5.1
>A set composition of $[n]$ into $k$ blocks is a collection of $k$ pairwise disjoint subsets of $[n]$ whose union is $[n]$. For $n = 3$ and $k = 2$ the set compositions are $(\{1\},\{2,3\}), (\{2\},\{1,3\}), (\{3\},\{1,2\}), (\{1,2\},\{3\})$, $(\{1,3\},\{2\})$ and $(\{2,3\},\{1\})$.
>
>Given a set composition $(B_1, \dots, B_k)$ we say that $B_j$ is *splittable* if it contains at least two elements and that $B_j$ is *mergeable* if it contains one element and this element is less than the minimal element of $B_{j+1}$.
>- List the mergeable and splittable sets of $(\{2,5\},\{4\},\{1\},\{3,6,7\})$.
>- Let $B(n,k)$ be the number of set of compositions of $[n]$ into $k$ blocks. Define a sign reversing involution on set compositions of $[n]$ that shows that for $n \ge 1$
>$$
>\sum_{k=1}^{n} (-1)^k B(n,k) = (-1)^n .
>$$

**Proof:**
For the set composition $(\{2,5\},\{4\},\{1\},\{3,6,7\})$:
- **Splittable:** $\{2,5\}$, $\{3,6,7\}$
- **Mergeable:** $\{ 2,5 \}$,$\{ 1 \}$


Let $\Pi$ be the set of all set compositions of $[n]$. For $\pi = (B_1,\dots,B_k) \in \Pi$, define $\phi(\pi)$: choose the minimum $j$ such that $B_{j}$ is splittable or mergeable. If $B_j$ is mergeable, merge $B_j$ and $B_{j+1}$ into one block ($k \to k-1$). If $B_j$ is splittable, split $B_j$ by isolating its minimum element into a new singleton block ($k \to k+1$). If such $j$ doesn't exist, $\phi(\pi) = \pi$ (fixed point).

This is a sign-reversing involution: non-fixed points are paired with opposite signs $(-1)^k$.

Fixed points analysis: No splittable blocks $\Rightarrow$ all blocks are singletons ($k=n$). No mergeable blocks $\Rightarrow$ $\min(B_j) > \min(B_{j+1})$ for all $j$. The unique fixed point is $(\{n\},\{n-1\},\dots,\{1\})$ with sign $(-1)^n$.

Hence,
$$
\sum_{k=1}^{n} (-1)^k B(n,k) = (-1)^n.
$$
___

>[!problem] 5.2
>Prove that for any odd integer $n$,
>$$
>\sum_{\substack{A,B \subseteq \{1,2,...,n\} \\ |A|+|B|=n}} (-1)^{|A|} = 0.
>$$

**Proof:**
For any ordered pair $(A,B)$ satisfying $|A|+|B|=n$, define the map:
$$
\phi(A,B) =(A',B')= (A \triangle \{x\}, B \triangle \{x\})
$$
where $x$ is the smallest element which is contained in exactly one of $A$ and $B$.

Flipping $x$ changes $|A|$ by $\pm 1$ and $|B|$ by $\pm 1$. Hence, we have $(-1)^{|A'|} = -(-1)^{|A|}$.
Also, $\phi(\phi(A,B)) = (A,B)$, and $\phi(A,B) \neq (A,B)$ because the membership of $x$ is strictly altered.

Therefore, the total sum is $0$.
___

>[!problem] 6.1
>Give a proof of the Cauchy-Binet Theorem using the LGV lemma.

**Proof:**
Let $A$ be an $m\times n$ matrix and $B$ an $n\times m$ matrix, with $m\le n$. We prove the Cauchy-Binet formula
$$
\det(AB)=\sum_{\substack{S\subseteq [n]\\ |S|=m}}\det(A_{[m],S})\det(B_{S,[m]})
$$
using the LGV lemma.

Construct a directed acyclic graph with vertices arranged in three layers. The first layer consists of vertices $u_1,\dots,u_m$, the middle layer consists of $v_1,\dots,v_n$, and the last layer consists of $w_1,\dots,w_m$. Put an edge $u_i\to v_j$ of weight $a_{ij}$ and an edge $v_j\to w_k$ of weight $b_{jk}$.

A path from $u_i$ to $w_k$ has weight
$$
\sum_{j=1}^n a_{ij}b_{jk}=(AB)_{ik}.
$$
Thus, the matrix of single-path weights from the $u_i$'s to the $w_k$'s is exactly $AB$.

By the LGV lemma, since the only vertex-disjoint path families connect $u_i$ to $w_i$ up to a permutation, we have
$$
\det(AB)=\sum_{\sigma\in S_m}\operatorname{sgn}(\sigma)
\prod_{i=1}^m\left(\sum_{j=1}^n a_{ij}b_{j,\sigma(i)}\right).
$$

Expand the products. Each term corresponds to choosing a middle vertex $v_{j_i}$ for each $i$. If two indices $j_i$ and $j_k$ are equal, the corresponding paths intersect at the same middle vertex, so the LGV involution cancels such intersecting path families.

Hence only families using $m$ distinct middle vertices survive. Let
$$
S=\{j_1,\dots,j_m\}\subseteq[n],\qquad |S|=m.
$$
For a fixed $S$, the LGV lemma applied to the paths from $u_1,\dots,u_m$ to the middle vertices indexed by $S$ gives the contribution
$$
\det(A_{[m],S}),
$$
while the paths from the middle vertices indexed by $S$ to $w_1,\dots,w_m$ give
$$
\det(B_{S,[m]}).
$$

Therefore, summing over all $m$-element subsets $S\subseteq[n]$ gives
$$
\det(AB)
=
\sum_{\substack{S\subseteq[n]\\ |S|=m}}
\det(A_{[m],S})\det(B_{S,[m]}).
$$
___

>[!problem] 6.2
>Let $[n]_q = 1 + q + \ldots + q^{n-1}$ and $[n]_q! = [n]_q[n-1]_q\ldots[1]_q$. Define the $q$-binomial coefficient by
>$$
>\binom{n}{k}_q = \frac{[n]_q!}{[k]_q![n-k]_q!}.
>$$
>
>- Prove that $\binom{n}{k}_q$ is the generating polynomial of $N,E$ paths from $(0,0)$ to $(k,n-k)$ where the weight of the step $(x,y) \to (x+1,y)$ is $q^y$ and the weight of the steps $(x,y) \to (x,y+1)$ is $1$.
>
>- Use the LGV lemma to prove that
>$$
>\binom{n}{k}_q \binom{n+1}{k}_q \binom{n}{k-1}_q = \binom{n+1}{k+1}_q
>$$
>is a polynomial in $q$ with non negative coefficients.

**Proof:**
**1.** Let $P(n,k)$ be the generating polynomial of $N,E$ paths from $(0,0)$ to $(k,n-k)$, where an east step at height $y$ has weight $q^y$ and a north step has weight $1$.

Every such path either ends with an east step or a north step. Thus
$$
P(n,k)=q^{n-k}P(n-1,k-1)+P(n-1,k).
$$
The initial conditions are
$$
P(n,0)=P(n,n)=1.
$$

On the other hand, the $q$-binomial coefficients satisfy the same recurrence
$$
\binom{n}{k}_q
=
q^{n-k}\binom{n-1}{k-1}_q+\binom{n-1}{k}_q,
$$
with
$$
\binom{n}{0}_q=\binom{n}{n}_q=1.
$$
Therefore
$$
P(n,k)=\binom{n}{k}_q.
$$
**2.** The claimed identity is not correct in general. For example, when $n=2$ and $k=1$,
$$
\binom21_q\binom31_q\binom20_q
=
[2]_q[3]_q
\ne
[3]_q
=
\binom32_q.
$$
___


