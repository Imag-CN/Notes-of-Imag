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
- **Mergeable:** $\{ 1 \}$

**2. Sign-Reversing Involution**

Let $\Pi$ be the set of all set compositions of $[n]$. For $\pi = (B_1,\dots,B_k) \in \Pi$, define $\phi(\pi)$ by scanning from $j=1$ to $k-1$:

- If $B_j$ is **mergeable**, merge $B_j$ and $B_{j+1}$ into one block ($k \to k-1$).
- Else if $B_j$ is **splittable**, split $B_j$ by isolating its minimum element into a new singleton block ($k \to k+1$).
- If neither exists, $\phi(\pi) = \pi$ (fixed point).

This is a sign-reversing involution: non-fixed points are paired with opposite signs $(-1)^k$.

**Fixed point analysis**: No splittable blocks ⇒ all blocks are singletons ($k=n$). No mergeable blocks ⇒ $\min(B_j) > \min(B_{j+1})$ for all $j$. The unique fixed point is $(\{n\},\{n-1\},\dots,\{1\})$ with sign $(-1)^n$.

Hence,
$$\sum_{k=1}^{n} (-1)^k B(n,k) = (-1)^n.$$