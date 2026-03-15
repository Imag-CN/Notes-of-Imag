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
Let $p$ be a point in the common intersection $\bigcap_i X_i$ (exists because all triple intersections are nonempty, e.g., pick $p \in X_1 \cap X_2 \cap X_3$, then $p$ is in every $X_i$).

Since each $X_i$ is convex and contains $p$, $X_i$ is star-shaped with respect to $p$. Therefore, $X = \bigcup_i X_i$ is star-shaped with respect to $p$. Hence $X$ is simply-connected.
___

> [!problem] [HAT] 1.2.4
> Let $X \subset \mathbb{R}^3$ be the union of $n$ lines through the origin. Compute $\pi_1(\mathbb{R}^3 - X)$.

