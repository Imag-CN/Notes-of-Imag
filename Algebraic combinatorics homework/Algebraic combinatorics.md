___

>[!problem] 1.1
> Let $L_n$ be the number of tilings of $n$ boxes arranged in a circle with dominoes and monominoes. For example $L_4 = 7$.
>
>(a) Prove that $L_n = F_{n-1} + F_{n+1}$ for $n \ge 1$.
>
>(b) Prove that $L_{m+n} = F_{m-1} L_n + F_m L_{n+1}$ for $m, n \ge 1$.
>
>(c) Prove that $F_{2n} = F_n L_n$.

**Proof:**
**(a)** Let $F_n$ be the standard Fibonacci numbers with $F_1 = F_2 = 1$ and $F_n = F_{n-1} + F_{n-2}$. Then $F_{n+1}$ counts the number of tilings of a line of $n$ boxes with dominoes and monominoes. Define $F_{0}=0$ to maintain the recursive relation.

For a circle of $n$ boxes, consider whether boxes $n$ and $1$ are covered by a single domino:
 - If they are, remove this domino; the remaining $n-2$ boxes form a line, giving $F_{n-1}$ tilings.
 - If they are not, cut the circle between $n$ and $1$ to obtain a line of $n$ boxes, giving $F_{n+1}$ tilings.
 
Therefore, $L_n = F_{n-1} + F_{n+1}$ for $n \ge 1$.

**(b)** For a line of $m+n$ boxes, consider whether boxes $m$ and $m+1$ are covered by a single domino:
- If they are, remove this domino; the remaining $m-1$ and $n-1$ boxes form two lines, giving $F_{m}F_{n}$ tilings.
 - If they are not, cut the line between $m$ and $m+1$ to obtain a line of $m$ boxes and a line of $n$ boxes, giving $F_{m+1}F_{n+1}$ tilings.

Therefore, $F_{m+n+1} = F_{m}F_{n} + F_{m+1}F_{n+1}$ for $n \ge 1$. Substituting $n$ with $n-2$ gives $F_{m+n-1} = F_{m}F_{n-2} + F_{m+1}F_{n-1}$ (define $F_{-1}=1$ to maintain the recursive relation). Adding these two formulas gives
$$
F_{m+n+1}+F_{m+n-1} = F_{m}(F_{n-2}+F_{n}) + F_{m+1}(F_{n+1}+F_{n-1})
$$

Applying **(a)** yields the formula required.

**(c)** We do induction on $n$:
- If $n=1$, then $F_{2n}=F_{n}L_{n}=1$;
- Suppose $F_{2n} = F_n L_n$, then set $m=n+1$ in **(b)** gives $L_{2n+1}=F_{n}L_{n}+F_{n+1}L_{n+1}$. Substitute $L_{2n+1}=F_{2n}+F_{2n+2}$ by **(a)** and $F_{n}L_{n}=F_{2n}$ by induction hyphothesis gives $F_{2n}+F_{2n+2}=F_{2n}+F_{n+1}L_{n+1}$, thus $F_{2n+2}=F_{n+1}L_{n+1}$.

Therefore, $L_n = F_{n-1} + F_{n+1}$.
___

>[!problem] 1.2
>Let $\pi$ be a permutation in $\Sigma_n$. The inverse of $\pi$ is the permutation $\sigma$ such that $\sigma \cdot \pi = 12 \dots n$. Prove that each permutation has a unique inverse.

**Proof:**
Since $\pi$ is a bijection, it has a unique inverse map $\sigma$ satisfying $\sigma\pi = \pi\sigma = \text{id}$ (the left inverse must be the right inverse, thus the left inverse is unique itself).

In group terms, $\Sigma_n$ is a group, so every element has a unique inverse.
___

>[!problem] 1.3
>A permutation $\pi$ is an involution is $\pi^2 = 12 \dots n$. Prove that for $n > 1$ the number of involutions is even.

**Proof:**
An involution consists only of $1$-cycles and $2$-cycles. Denote $I_{n}$ as the number of involutions for $n$. Then $I_{1}=1$, $I_{2}=2$. For $n>2$, the number of involutions where $1$ is in $1$-cycle is $I_{n-2}$, and the number of involutions where $1$ is in $2$-cycle is $(n-1)I_{n-2}$, thus $I_{n}=I_{n-1}+(n-1)I_{n-2}$. By induction on $n$, $I_{n}$ is even for $n>1$.
___

>[!problem] 1.4
> We say that a permutation $\pi \in \Sigma_n$ has a square root if there exists $\sigma \in \Sigma_n$ such that $\sigma^2 = \pi$. Find a sufficient and necessary conditions for $\pi$ to have a square root, in terms of its cycle lengths.

**Proof:**
Let $\pi$ have $c_k$ cycles of length $k$. Then $\pi$ has a square root iff for every even $k$, $c_k$ is even. 

We have $(12\dots m)^{2}=(13\dots m 24\dots m-1)$ for an odd $m$ and $(12\dots2k)^{2}=(13\dots2k-1)(24\dots 2k)$.

By relabeling the elements (in group terms, doing conjugation) we can make any cycles into the situations above. Therefore, squaring a cycle of odd length $m$ gives another $m$-cycle; squaring a cycle of even length $2k$ splits into two $k$-cycles. And conversely, a cycle of odd length $m$ can be written as a square of another $m$-cycle; two $k$-cycles can be written as a square of a $2k$-cycle.
___

> [!problem] 2.1
> A partition $\lambda = (\lambda_1, \dots, \lambda_k)$ is into odd parts if $\lambda_i$ is odd for all $i$. A partition $\lambda = (\lambda_1, \dots, \lambda_k)$ is into distinct parts if $\lambda_i > \lambda_{i+1}$ for all $i$. Show that for all $n$ the number of partitions of $n$ into odd parts is equal to the number of partitions of $n$ into distinct parts. For example if $n = 6$ the sets are respectively $\{(5,1), (3,3), (3,1,1,1), (1,1,1,1,1,1)\}$ and $\{(6), (5,1), (4,2), (3,2,1)\}$.

**Proof:**
Let $p_{\text{odd}}(n)$ be the number of partitions of $n$ into odd parts, and $p_{\text{distinct}}(n)$ be the number of partitions of $n$ into distinct parts.

The generating function for partitions into odd parts is:
$$
\sum_{n=0}^{\infty} p_{\text{odd}}(n) x^n =(1+x+x^{2}+\dots)(1+x^{3}+x^{6}+\dots)\dots= \prod_{k \ge 1} \frac{1}{1 - x^{2k-1}}
$$
The generating function for partitions into distinct parts is:
$$
\sum_{n=0}^{\infty} p_{\text{distinct}}(n) x^n  = (1+x)(1+x^2)(1+x^3)\cdots= \prod_{m \ge 1} (1 + x^m)
$$
We show these two generating functions are equal:
$$
\prod_{m \ge 1} (1 + x^m) = \prod_{m \ge 1} \frac{1 - x^{2m}}{1 - x^m}= \dfrac{\prod_{m \ge 1}(1-x^{2m})}{\prod_{k \ge 1} (1 - x^{2k})\prod_{k \ge 1} (1 - x^{2k})}=\prod_{k \ge 1} \frac{1}{1 - x^{2k-1}}
$$Therefore $p_{\text{distinct}}(n) = p_{\text{odd}}(n)$ for all $n \ge 0$.
___

> [!problem] 2.2
> A partition $\lambda$ is self conjugate if $\lambda' = \lambda$. Let $sc(n)$ be the number of self conjugate partitions of $n$. Show that
> $$
> \sum_{n \ge 0} sc(n) q^n = \prod_{i \ge 1} (1 + q^{2i-1}).
> $$

**Proof:**
We prove that the number of self-conjugate partitions of $n$ equals the number of partitions of $n$ into distinct odd parts.

For a self-conjugate partition, consider its Ferrers diagram. The diagram is symmetric about the main diagonal. Remove the first row and first column. What remains is again a self-conjugate partition. The removed cells form a hook of size $2\lambda_1 - 1$, which is odd. By repeating this process, we decompose any self-conjugate partition uniquely into a set of distinct odd numbers (the hook lengths).

Conversely, given a set of distinct odd numbers $d_1 > d_2 > \cdots > d_k$, we can reconstruct a self-conjugate partition by stacking hooks of these sizes along the diagonal. This gives a bijection.

Therefore, the generating function is:
$$ \sum_{n \ge 0} sc(n) q^n = \prod_{i \ge 1} (1 + q^{2i-1}) $$
since each odd number $2i-1$ can either appear or not in the decomposition.
___

>[!problem] 2.3
>Let $\lambda$ and $\mu$ be partitions of $n$. In the dominance order we say that $\lambda \ge \mu$ if for all $i$ $\lambda_1 + ... + \lambda_i \ge \mu_1 + ... + \mu_i$. Prove that $\lambda \ge \mu$ iff $\lambda' \le \mu'$.

**Proof:**
Since conjugation is symmetric, we only have to prove "$\Rightarrow$".

For any $k\ge1$,  
$$
\sum_{j=1}^k\lambda'_j = \sum_{i=1}^\infty\min(\lambda_i,k),\qquad
\sum_{j=1}^k\mu'_j = \sum_{i=1}^\infty\min(\mu_i,k).
$$
and
$$
\sum_{i=1}^\infty \min(\lambda_i,k) = n - \sum_{i=1}^\infty \max(\lambda_i-k,0)
$$
and similarly for $\mu$. Since $\lambda\ge\mu$, for each $m$ we have $\sum_{i=1}^m\lambda_i\ge\sum_{i=1}^m\mu_i$. Subtracting $mk$ from both sides gives
$$
\sum_{i=1}^m (\lambda_i-k) \ge \sum_{i=1}^m (\mu_i-k).
$$
Taking the positive part preserves the inequality termwise, so
$$
\sum_{i=1}^\infty \max(\lambda_i-k,0) \ge \sum_{i=1}^\infty \max(\mu_i-k,0).
$$
Hence $\sum_i\min(\lambda_i,k)\le\sum_i\min(\mu_i,k)$, i.e. $\sum_{j=1}^k\lambda'_j\le\sum_{j=1}^k\mu'_j$ for all $k$, so $\lambda'\le\mu'$.
Since $\lambda\ge\mu$, for each $i$, the partial sums of $\lambda$ dominate those of $\mu$. A standard fact: this implies $\sum_i\min(\lambda_i,k)\le\sum_i\min(\mu_i,k)$ for every $k$. Hence $\sum_{j=1}^k\lambda'_j\le\sum_{j=1}^k\mu'_j$ for all $k$, i.e., $\lambda'\le\mu'$.
