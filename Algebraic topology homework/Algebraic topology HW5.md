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

