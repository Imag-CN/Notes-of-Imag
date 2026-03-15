___

> [!problem] [HAT] 1.2.1
> Show that the free product $G \ast H$ of nontrivial groups $G$ and $H$ has trivial center, and that the only elements of $G \ast H$ of finite order are the conjugates of finite-order elements of $G$ and $H$.

**Proof:**
**1. Trivial center.**
Let $z \in Z(G \ast H)$. Write $z$ as a reduced word.

If $z$ has length $\ge 2$, pick an element from the factor opposite to the last letter of $z$. Multiplying on the right yields a reduced word ending with that element, while multiplying on the left yields a word ending with the original last letter, contradiction.

If $z$ has length $1$, say $z = g \in G \setminus \{1\}$. Take $h \in H \setminus \{1\}$. Then $z h = g h$ and $h z = h g$ are distinct reduced words of length 2, so $z h \ne h z$. Hence $z=1$.

**2. Finite-order elements.**
Let $x \in G \ast H$ have finite order. Among all conjugates of $x$, choose $y = c x c^{-1}$ with minimal reduced length. If $y$ had length $\ge 2$, it would be cyclically reduced (or conjugate to a cyclically reduced word of same length), and all its powers would be reduced words of increasing length, giving infinite order. Hence $y$ must have length 1, i.e., $y \in G$ or $y \in H$. Thus $x$ is conjugate to an element of $G$ or $H$ of the same finite order. The converse is clear.
___

> [!problem] [HAT] 1.2.2
> Let $X \subset \mathbb{R}^m$ be the union of convex open sets $X_1, \cdots, X_n$ such that $X_i \cap X_j \cap X_k \neq \emptyset$ for all $i, j, k$. Show that $X$ is simply-connected.

**Proof:**
Let $X^{(n)} = \bigcup_{i=1}^n X_i$. Proof by induction on $n$.

Base case $n=1$: $X^{(1)} = X_1$ is convex, hence simply-connected.

Assume $X^{(n-1)}$ is simply-connected. Let $X^{(n)} = X^{(n-1)} \cup X_n$.
Choose a point $p \in \bigcap_{i=1}^{n-1} (X_i \cap X_n)$ (nonempty: for any $i,j$, $X_i \cap X_j \cap X_n \neq \varnothing$, and intersections of convex sets that pairwise intersect have a common point).

Let $f$ be a loop in $X^{(n)}$ based at $p$. Subdivide $I$ so each subsegment lies in $X^{(n-1)}$ or $X_n$.

For each subsegment $f|_{[t_{k-1}, t_k]} \subset X_n$, replace it with a path in $X^{(n-1)} \cap X_n$ connecting $f(t_{k-1})$ and $f(t_k)$, homotopic within $X_n$ (possible because $X_n$ is simply-connected and $X^{(n-1)} \cap X_n$ is path-connected, as a union of pairwise intersecting convex sets $X_i \cap X_n$).

This yields a loop $g$ homotopic to $f$ and entirely contained in $X^{(n-1)}$. By induction, $g$ is null-homotopic in $X^{(n-1)}$, hence $f$ is null-homotopic in $X^{(n)}$.

Thus $X^{(n)}$ is simply-connected.
___

> [!problem] [HAT] 1.2.4
> Let $X \subset \mathbb{R}^3$ be the union of $n$ lines through the origin. Compute $\pi_1(\mathbb{R}^3 - X)$.

**Proof:**
Let $X = \bigcup_{i=1}^n L_i$, where each $L_i$ is a line through the origin in $\mathbb{R}^3$.

Consider the radial deformation retraction $r: \mathbb{R}^3 \setminus X \to S^2 \setminus X$ given by $r(x) = x / \|x\|$. 

Each line $L_i$ intersects $S^2$ in a pair of antipodal points. Thus $S^2 \cap X$ consists of $2n$ distinct points. Therefore, $S^2 \setminus X = S^2 \setminus \{2n \text{ points}\}$.

The space $S^2$ minus $2n$ points is homeomorphic to a plane (e.g., via stereographic projection from one of the removed points) with $2n-1$ points removed. The fundamental group of a plane with $k$ points removed is the free group $\mathbb{F}_k$ on $k$ generators. Hence,
$$
\pi_1(S^2 \setminus X) \cong \mathbb{F}_{2n-1}.
$$
Since deformation retraction induces an isomorphism of fundamental groups, we conclude
$$\pi_1(\mathbb{R}^3 \setminus X) \cong \mathbb{F}_{2n-1}.$$
___

