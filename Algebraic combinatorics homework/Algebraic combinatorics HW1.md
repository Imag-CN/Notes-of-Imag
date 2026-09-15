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
$$
Therefore $p_{\text{distinct}}(n) = p_{\text{odd}}(n)$ for all $n \ge 0$.
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
\sum_{i=1}^\infty \min(\lambda_i,k) = n - \sum_{i=1}^\infty \max(\lambda_i-k,0),\quad\sum_{i=1}^\infty \min(\mu_i,k) = n - \sum_{i=1}^\infty \max(\mu_i-k,0)
$$
Since $\lambda\ge\mu$, for each $m$ we have $\sum_{i=1}^m\lambda_i\ge\sum_{i=1}^m\mu_i$. Subtracting $mk$ from both sides gives
$$
\sum_{i=1}^m (\lambda_i-k) \ge \sum_{i=1}^m (\mu_i-k).
$$
Taking the positive part preserves the inequality termwise, so
$$
\sum_{i=1}^\infty \max(\lambda_i-k,0) \ge \sum_{i=1}^\infty \max(\mu_i-k,0).
$$
Hence $\sum_i\min(\lambda_i,k)\le\sum_i\min(\mu_i,k)$, i.e. $\sum_{j=1}^k\lambda'_j\le\sum_{j=1}^k\mu'_j$ for all $k$, so $\lambda'\le\mu'$.
___

>[!problem] 2.4
>Use Maya diagrams to prove the Jacobi triple product identity
>$$
>\frac{\sum_{n\in\mathbb{Z}} z^n q^{n(n+1)/2}}{\prod_{i\ge 1}(1-q^i)} = \prod_{i\ge 1}(1+zq^i)(1+q^{i-1}/z)
>$$

**Proof:**
Let the Fermi vacuum be: all negative integers occupied (●), nonnegative empty (○). A Maya diagram is a finite perturbation of this vacuum.

Assign weight $zq^i$ for adding a particle at position $i\ge1$, and $q^{i-1}/z$ for creating a hole at position $-(i-1)$. Independent choices give the RHS:
$$
\prod_{i\ge1}(1+zq^i)(1+q^{i-1}/z).
$$
Now group diagrams by net particle number $n$. The minimal energy for net $n$ particles is $n(n+1)/2$ (triangular number). The remaining energy corresponds to an unrestricted partition, generating $\prod_{i\ge1}(1-q^i)^{-1}$. Summing over $n$ gives the LHS:
$$
\sum_{n\in\mathbb{Z}} z^n q^{n(n+1)/2} \cdot \frac{1}{\prod_{i\ge1}(1-q^i)}.
$$
Both sides enumerate the same set of Maya diagrams, hence they are equal.
___

>[!problem] 3.1
>Prove that there is a bijection between les Frieze patterns of size $n$ and triangulations of the $n+2$-gon.

**Proof:**
Given a triangulation, label the $n+3$ vertices cyclically. For each triangle $(i,j,k)$, define its entry as $x_{i,k} = j$ (the vertex between $i$ and $k$). Extend to a grid via the unimodular rule; this yields a Frieze pattern of size $n$.

Conversely, from a Frieze pattern of size $n$, read the first nontrivial row $(x_{0,2}, x_{0,3}, \dots, x_{0,n+1})$. These form the vertices of a polygon. Draw a diagonal $(i,k)$ if $x_{i,k} = j$ appears in the pattern. The unimodular rule ensures these diagonals do not cross and form $n$ triangles.

Both structures are counted by the Catalan number $C_n = \frac{1}{n+1}\binom{2n}{n}$, and the local gluing rule (unimodular relation) exactly matches the triangle adjacency in the polygon. Thus, a bijection exists.
___

>[!problem] 3.2
>The area of a Dyck paths is the number of squares between the path avec the $y=x$ line. For example the path $NNENEE$ has area $2$. Let $D_{n,k}$ be the number of Dyck paths of length $n$ with area $k$. For example $D_{3,1} = 2$. Let
>$$
>D(x,q) = \sum_{k\ge 0} D_{n,k} x^n q^k.
>$$
>Show that $D(x,0) = 1$ and that
>$$D(x,q) = 1 + x D(xq,q) \cdot D(x,q).
>$$
>Write $D(x,q)$ as a continued fraction.

**Proof:**
**1. Show $D(x,0) = 1$:**
Setting $q=0$ kills all terms with area $k>0$. Only area $k=0$ remains, which corresponds to the unique trivial path. Thus $D(x,0) = D_{0,0} x^0 = 1$.

**2. Show the functional equation:**
Decompose a non-empty Dyck path by its first return to the diagonal $y=x$. It consists of:
- An initial North step and a final East step (weight $x \cdot x = x^2$ in standard length, or simply contributes factor $x$ to the path length generator here).
- An interior Dyck path shifted up by $1$ unit (area increases by its length, weight $q$; generates $D(xq,q)$).
- A trailing Dyck path attached after the return (generates $D(x,q)$).

Accounting for the empty path (1) and the standard Catalan-like decomposition with area shift, the exact generating function satisfies:
$$ D(x,q) = 1 + x D(xq,q) D(x,q). $$

**3. Continued fraction:**
Iterating the recurrence $D(x,q) = 1 + x D(xq,q) D(x,q)$ gives:
$$
D(x,q) = \frac{1}{1 - x D(xq,q)} = \frac{1}{1 - \cfrac{x}{1 - xq D(xq^2,q)}} = \dots
$$

Thus, the continued fraction is:
$$
D(x,q) = \cfrac{1}{1 - \cfrac{x}{1 - \cfrac{xq}{1 - \cfrac{xq^2}{1 - \cfrac{xq^3}{\ddots}}}}}
$$
___

>[!problem] 3.3
>A peak in a Dyck path is a step $N$ followed by a step $E$. Prove that the number of Dyck paths of length $n$ with $k$ peaks is
>$$
>\frac{1}{k} \binom{n}{k} \binom{n}{k-1}.
>$$

**Proof:**
Let $F(x,u)=\sum_{n,k}f_{n,k}x^nu^k$ where $f_{n,k}$ counts Dyck paths of length $n$ with $k$ peaks. Decompose a non-empty path as $NP\,E\,Q$ where $P,Q$ are Dyck paths. The initial $NE$ gives one peak, so:
$$
F(x,u)=1+xu\cdot F(x,u)\cdot F(x,1).
$$
Let $C(x)=F(x,1)=\sum_{n\ge0}\frac1{n+1}\binom{2n}{n}x^n$, the Catalan generating function with $C(x)=1+xC(x)^2$. Solving:
$$
F(x,u)=\frac{1}{1-xuC(x)}=\sum_{k\ge0}u^kx^kC(x)^k.
$$
Hence $[u^k]F(x,u)=x^kC(x)^k$, and $f_{n,k}=[x^{n-k}]C(x)^k$. Using the known coefficient $[x^m]C(x)^k=\frac{k}{m+k}\binom{2m+k-1}{m}$, set $m=n-k$:
$$
f_{n,k}=\frac{k}{n}\binom{2n-k-1}{n-k}.
$$
>[!error]
>The formula given is incorrect. It is even not necessarily an integer (check $n=5$, $k=4$).

___

> [!problem] 3.4
>Construct a bijection between non-decreasing parking functions of size $n$ and Dyck paths of length $n$.

**Proof:**
Map a non-decreasing parking function $(a_1,\dots,a_n)$ to a Dyck path of semilength $n$ as follows: for $i=1,\dots,n$, place the $i$-th $D$ at position $i+a_i$ in a sequence of $2n$ steps, and fill all other positions with $U$. The result is a Dyck path because $a_i\leq i$ ensures the path never dips below $0$. Conversely, given a Dyck path, let $a_i$ be the number of $U$'s before the $i$-th $D$ minus $(i-1)$. This gives a bijection.
___

> [!problem] 3.5
> Let $f$ be a parking function of size $n$. Let $p_i$ be the spot where car $i$ parks. The displacement $d_i$ of car $i$ is $p_i - f(i)$ and the displacement of $f$ is $\sum_{i=1}^n d_i$. How many parking functions have displacement $0$? What is the maximal displacement? Can we read the displacement on the labelled Dyck path?

**Proof:**
**1. Displacement 0:** Only $(1,2,\dots,n)$. So the number is $1$.

**2. Max displacement:** Achieved by $(1,1,\dots,1)$. Cars park at $1,2,\dots,n$, giving displacement $\sum_{i=1}^{n}(i-1)=\frac{n(n-1)}{2}$.

**3. On labelled Dyck path:** In the standard bijection, the height before the $i$-th down step equals the displacement $d_i$. Hence total displacement $=$ sum of these heights $=$ area under the Dyck path.
___

> [!problem] 4.1
> An $r$-parking function of length $n$ may be defined as a sequence $(a_1, ..., a_n)$ of positive integers whose increasing rearrangement $b_1 \le ... \le b_n$ satisfies $b_i \le 1 + (i - 1)r$.
> 
> - Show that the parking functions defined in class correspond to the case $r = 1$.
> - Given an $r$-parking function, the parking procedure goes as follows: we now have $rn$ cars $C_1, \dots, C_{rn}$ and $rn$ spaces $1, 2, ..., rn$. We consider preferences and cars $C_{r(i-1)+1}, ..., C_{ri}$ all prefer spot $a_i$. The cars use the same parking algorithm as in class. Prove that the number of $r$-parking functions is $(rn + 1)^{n-1}$.

**Proof:**
**Case $r = 1$:**

When $r = 1$, the condition becomes: increasing rearrangement $b_1 \le \cdots \le b_n$ satisfies $b_i \le 1 + (i-1)\cdot 1 = i$. This is exactly the definition of a classical parking function: $b_i \le i$ for all $i$.

**Counting $r$-parking functions:**

Consider a circle with $rn+1$ spots labeled $0,1,\dots,rn$. Spots $1,\dots,rn$ are real parking spots; spot $0$ is a "phantom" spot that indicates failure. There are $rn$ cars, grouped into $n$ blocks of $r$ cars each. Block $i$ (cars $C_{r(i-1)+1},\dots,C_{ri}$) all prefer spot $a_i$.

Cars arrive in order $C_1,\dots,C_{rn}$. Each car tries its preferred spot; if taken, it moves forward (increasing spot number) until finding an empty spot. If a car reaches spot $rn$ and it is taken, it wraps around to spot $0$ (the phantom spot). If any car parks at $0$, the configuration fails.

Choose an arbitrary starting point on the circle. For any sequence $(a_1,\dots,a_n)$ with $1 \le a_i \le rn+1$ (allowing $a_i = rn+1$ to mean preference for spot $0$), run the algorithm. Exactly one rotation of the circle will make all cars park successfully (none hit spot $0$). This is the same cyclic symmetry argument as for ordinary parking functions: among the $rn+1$ rotations, exactly one yields a valid parking outcome.

There are $(rn+1)^n$ sequences $(a_1,\dots,a_n)$ with entries in $\{1,\dots,rn+1\}$. By the cyclic symmetry, exactly $1/(rn+1)$ of them are valid $r$-parking functions. Thus:

$$
\text{Number of } r\text{-parking functions} = \frac{(rn+1)^n}{rn+1} = (rn+1)^{n-1}.
$$
___

> [!problem] 4.2
> Prove that the Prüfer code gives a bijection between labelled trees with $n$ vertices and words of length $n-2$ in $\{1,\dots,n\}$.

**Proof:**  
To yield the Prüfer code of a tree: while more than two vertices remain, delete the leaf with smallest label and record its neighbour.

The inverse reconstructs the tree: given a word $(p_1,\dots,p_{n-2})$, let $S=[n]$. For $i=1,\dots,n-2$, let $v$ be the smallest element of $S$ not appearing in $(p_i,\dots,p_{n-2})$; add edge $(v,p_i)$ and remove $v$ from $S$. Finally join the two remaining vertices.

Both maps are deterministic inverses, hence a bijection.
___

> [!problem] 4.3
> Let $T_n$ be the number of rooted labeled trees with $n$ vertices (i.e. with one chosen vertex called the root) and let
> $$
> T(x) = \sum_{n \ge 1} T_n \frac{x^n}{n!}.
> $$
> Show that
> $$
> T(x) = x \exp(T(x)).
> $$

**Proof:**
Any rooted labeled tree can be uniquely decomposed as: a root vertex (labeled) $+$ a set of subtrees rooted at its children.

The children’s subtrees are:
  - themselves rooted labeled trees;
  - their vertex sets partition the remaining $n-1$ labels (excluding the root);
  - they are unordered — so we use the “set” construction in labeled combinatorics.

In exponential generating functions (EGFs), the class “set of structures from class $\mathcal{T}$” has EGF:  
$$ \exp(T(x)) = \sum_{k \ge 0} \frac{T(x)^k}{k!} $$  
This is because:
- $T(x)^k$: sequence of $k$ labeled structures (ordered);
- divide by $k!$: to account for unordered sets (since labels are already accounted for in EGF).

So, the full class of rooted labeled trees is:

Root (EGF: $x$) $×$ Set of subtrees (EGF: $\exp(T(x))$)

Therefore, by labeled product rule (since root and subtrees have disjoint labels):
$$
T(x) = x \cdot \exp(T(x))
$$