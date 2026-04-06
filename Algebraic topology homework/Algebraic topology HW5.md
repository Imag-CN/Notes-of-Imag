___

> [!problem] [HAT] 1.3.1
> Let $p: \widetilde{X} \to X$ be a covering space, and let $A \subset X$ be a subspace. Let $\widetilde{A} = p^{-1}(A)$. Show that the restriction $p: \widetilde{A} \to A$ is also a covering space.

**Proof:**
Take $a \in A$. Since $p$ is a covering, there exists an open $U \subset X$ containing $a$ such that
$$p^{-1}(U) = \bigsqcup_i \widetilde{U}_i$$
with each $p|_{\widetilde{U}_i} : \widetilde{U}_i \to U$ a homeomorphism. Let $V = U \cap A$. Then
$$p|_{\widetilde{A}}^{-1}(V) = p^{-1}(V) = \bigsqcup_i (\widetilde{U}_i \cap \widetilde{A}).$$
Each $\widetilde{V}_i = \widetilde{U}_i \cap \widetilde{A}$ is open in $\widetilde{A}$, and $p|_{\widetilde{V}_i} : \widetilde{V}_i \to V$ is the restriction of a homeomorphism to $V$, hence a homeomorphism. Thus $p: \widetilde{A} \to A$ is a covering.
___

> [!problem] [HAT] 1.3.4
> Construct a simply-connected covering space of the space $X \subset \mathbb{R}^3$ that is the union of a sphere and a diameter. Do the same when $X$ is the union of a sphere and a circle intersecting it in two points.

**Proof:**
**Case 1:**  
The universal cover $\widetilde{X}$ is an infinite chain: take copies $S_n^2$ of the sphere indexed by $\mathbb{Z}$, connect the north pole of $S_n^2$ to the south pole of $S_{n+1}^2$ by a line segment (the lift of the diameter). The covering map collapses each sphere to the original sphere and each segment to the diameter. $\widetilde{X}$ is contractible, hence simply‑connected.
**Case 2:**  
$\widetilde{X}$ is an infinite tree of spheres. Start with one sphere, at the two intersection points attach edges (lifts of the circle), at the other ends of those edges attach new spheres, and continue. The covering map sends each sphere to the original sphere and each edge to the circle. The resulting space is simply‑connected (a tree of spheres).
___

> [!problem] [HAT] 1.3.5
> Let $X$ be the subspace of $\mathbb{R}^2$ consisting of the four sides of the square $[0,1] \times [0,1]$ together with the segments of the vertical lines $x = \frac{1}{2}, \frac{1}{3}, \frac{1}{4}, \cdots$ inside the square.  
> Show that for every covering space $\widetilde{X} \to X$, there is some neighborhood of the left edge of $X$ that lifts homeomorphically to $\widetilde{X}$.  
> Deduce that $X$ has no simply-connected covering space.

**Proof:**
Let $L$ be the left edge. Choose $\varepsilon$ so that $U = ([0,\varepsilon)\times[0,1])\cap X$ contains only finitely many vertical segments. Then $\pi_1(U)$ is a free group of finite rank. Because the vertical segments give infinitely many independent loops in $X$, the inclusion $U\hookrightarrow X$ induces an injection $\pi_1(U)\hookrightarrow\pi_1(X)$. For any covering $p:\widetilde{X}\to X$, the subgroup $p_*(\pi_1(\widetilde{X}))\le\pi_1(X)$ must contain the image of $\pi_1(U)$, so the covering is trivial over $U$; hence a neighbourhood of $L$ lifts homeomorphically.

If $X$ had a simply‑connected covering, then $p_*(\pi_1(\widetilde{X}))$ would be trivial, contradicting the injection $\pi_1(U)\hookrightarrow\pi_1(X)$. Thus $X$ has no simply‑connected covering.
___

> [!problem] [HAT] 1.3.6
> Let $X$ be the shrinking wedge of circles in Example 1.25, and let $\widetilde{X}$ be its covering space shown in the figure below.  
> Construct a two-sheeted covering space $Y \to \widetilde{X}$ such that the composition $Y \to \widetilde{X} \to X$ of the two covering spaces is not a covering space.
> 
> Note that a composition of two covering spaces *does* have the unique path lifting property, however.

**Proof:**
Let $X$ be the shrinking wedge of circles. Its covering space $\widetilde{X}$ consists of the real line $\mathbb{R}$ with a copy of $X$ attached at each integer point $n \in \mathbb{Z}$. Let $p: \widetilde{X} \to X$ be the covering map that collapses each copy of $X$ to the basepoint of $X$.

Take two disjoint copies $\widetilde{X}_0$, $\widetilde{X}_1$ of $\widetilde{X}$. Define an equivalence relation on $\widetilde{X}_0 \sqcup \widetilde{X}_1$ as follows: for $x$ in the real line of $\widetilde{X}$,
- if $x \ge 0$, the two copies of the point $x$ are not identified;
- if $x < 0$, identify the copy of $x$ in $\widetilde{X}_0$ with the copy of $x$ in $\widetilde{X}_1$ *after applying the involution that swaps the two copies*.

Equivalently, $Y$ is the two‑sheeted cover of $\widetilde{X}$ that is trivial over the half‑line $[0,\infty)$ and non‑trivial over $(-\infty,0]$. The projection $q: Y \to \widetilde{X}$ is a two‑sheeted covering map.

Consider the basepoint $x_0 \in X$. In $\widetilde{X}$, the preimage $p^{-1}(x_0)$ consists of the basepoints of all attached copies of $X$. In $Y$, the preimage of $x_0$ under the composition $p \circ q$ consists of two points for each integer $n \ge 0$, but for $n < 0$ the identification above makes the two points coincide in the limit as $n \to -\infty$. Consequently, any neighbourhood of $x_0$ in $X$ has a preimage in $Y$ that cannot be written as a disjoint union of sheets each homeomorphic to that neighbourhood. Hence the composition fails to be a local homeomorphism in the sense of covering spaces.

Both $q: Y \to \widetilde{X}$ and $p: \widetilde{X} \to X$ are covering maps, therefore they have the unique path‑lifting property. The composition of two maps with the unique path‑lifting property also has that property, as noted in the problem.

Thus $Y \to \widetilde{X}$ is a two‑sheeted covering space, but $Y \to X$ is not a covering space.
___

