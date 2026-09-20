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

>[!problem] 5.3