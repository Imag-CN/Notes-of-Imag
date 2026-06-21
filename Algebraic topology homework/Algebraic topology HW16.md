___

> [!problem] [HAT] 3.3.3
> Show that every covering space of an orientable manifold is an orientable manifold.

**Proof:**
Let $p: \tilde{M} \to M$ be a covering map with $M$ orientable. We show $\tilde{M}$ is orientable.

Since $M$ is orientable, there exists an orientation $\mu$ assigning to each $x \in M$ a generator $\mu_x \in H_n(M, M - \{x\})$ satisfying local consistency.

For any $\tilde{y} \in \tilde{M}$, let $x = p(\tilde{y})$. Choose a neighborhood $U$ of $x$ evenly covered by $p$, and let $\tilde{U}$ be the sheet containing $\tilde{y}$ mapping homeomorphically onto $U$. The composition
$$
H_n(\tilde{M}, \tilde{M} - \{\tilde{y}\}) \cong H_n(\tilde{U}, \tilde{U} - \{\tilde{y}\}) \xrightarrow{p_*} H_n(U, U - \{x\}) \cong H_n(M, M - \{x\})
$$
is an isomorphism. Define $\tilde{\mu}_{\tilde{y}}$ to be the preimage of $\mu_x$ under this isomorphism.

Local consistency follows from the local consistency of $\mu$ and the fact that $p$ is a local homeomorphism. Hence $\tilde{M}$ is orientable.
___

>[!problem] [HAT] 3.3.7
>For a map $f: M \to N$ between connected closed orientable $n$-manifolds with fundamental classes $[M]$ and $[N]$, the degree of $f$ is defined to be the integer $d$ such that
>$$
>f_*([M]) = d[N],
>$$
>so the sign of the degree depends on the choice of fundamental classes.
>
>Show that for any connected closed orientable $n$-manifold $M$, there is a degree $1$ map $M \to S^n$.

**Proof:**
Let $M$ be a connected closed orientable $n$-manifold. Choose a closed ball $D \subset M$ (the image of an embedding $D^n \hookrightarrow M$). Define $f: M \to S^n$ by collapsing $M \setminus \operatorname{int}(D)$ to a point and mapping $D/\partial D \cong S^n$ homeomorphically onto $S^n$. More explicitly, let $f$ send $\operatorname{int}(D)$ homeomorphically onto $S^n \setminus \{N\}$ and send $M \setminus \operatorname{int}(D)$ to $N$.

To compute the degree, pick a regular value $y \in S^n \setminus \{N\}$. Then $f^{-1}(y)$ consists of a single point in $\operatorname{int}(D)$, and $f$ is orientation-preserving there, so the local degree is $+1$. Hence $\deg f = 1$.
___

>[!problem] [HAT] 3.3.16
>Show that
>$$
>(\alpha \cap \varphi) \cap \psi = \alpha \cap (\varphi \cup \psi)
>$$
>for all $\alpha \in C_k(X; R)$, $\varphi \in C^\ell(X; R)$, and $\psi \in C^m(X; R)$.
>
>Deduce that cap product makes $H_*(X; R)$ a right $H^*(X; R)$-module.

**Proof:**
Let $\alpha = \sigma$ be a singular $k$-simplex. Then
$$
(\sigma \cap \varphi) \cap \psi = \left( \varphi(\sigma|_{[0,\dots,\ell]}) \cdot \sigma|_{[\ell,\dots,k]} \right) \cap \psi
$$
$$
= \psi\left( \left( \varphi(\sigma|_{[0,\dots,\ell]}) \cdot \sigma|_{[\ell,\dots,k]} \right)|_{[\ell,\dots,\ell+m]} \right) \cdot \sigma|_{[\ell+m,\dots,k]}
$$
$$
= \varphi(\sigma|_{[0,\dots,\ell]}) \cdot \psi(\sigma|_{[\ell,\dots,\ell+m]}) \cdot \sigma|_{[\ell+m,\dots,k]}.
$$
On the other hand,
$$
\sigma \cap (\varphi \cup \psi) = (\varphi \cup \psi)(\sigma|_{[0,\dots,\ell+m]}) \cdot \sigma|_{[\ell+m,\dots,k]}
$$
$$
= \varphi(\sigma|_{[0,\dots,\ell]}) \cdot \psi(\sigma|_{[\ell,\dots,\ell+m]}) \cdot \sigma|_{[\ell+m,\dots,k]}.
$$
Both sides are equal, so $(\alpha \cap \varphi) \cap \psi = \alpha \cap (\varphi \cup \psi)$ holds for all chains $\alpha$.

For $[\alpha] \in H_k(X;R)$ and $[\varphi] \in H^\ell(X;R)$, define $[\alpha] \cdot [\varphi] = [\alpha \cap \varphi]$. The identity gives associativity: $([\alpha] \cdot [\varphi]) \cdot [\psi] = [\alpha] \cdot ([\varphi] \cup [\psi])$, and the unit $1 \in H^0(X;R)$ acts as the identity. Hence $H_*(X;R)$ is a right $H^*(X;R)$-module.
___

>[!problem] [HAT] 3.3.23
>Show that for a locally compact $\Delta$-complex $X$ the simplicial and singular cohomology groups $H_c^i(X; G)$ are isomorphic. This can be done by showing that $\Delta_c^i(X; G)$ is the union of its subgroups $\Delta^i(X, A; G)$ as $A$ ranges over subcomplexes of $X$ that contain all but finitely many simplices, and likewise $C_c^i(X; G)$ is the union of its subgroups $C^i(X, A; G)$ for the same family of subcomplexes $A$.

**Proof:**
Let $\mathcal{A}$ be the collection of subcomplexes $A \subseteq X$ such that $X \setminus A$ contains only finitely many simplices. Since $X$ is locally finite, each compact subset is contained in some $A^c$ with $A \in \mathcal{A}$, so the compact support condition aligns with this filtration.

Define $\Delta_c^i(X;G) = \bigcup_{A \in \mathcal{A}} \Delta^i(X, A; G)$, where $\Delta^i(X, A; G)$ consists of simplicial cochains vanishing on simplices in $A$. Similarly, $C_c^i(X;G) = \bigcup_{A \in \mathcal{A}} C^i(X, A; G)$ for singular cochains.

For each $A \in \mathcal{A}$, the inclusion of $\Delta$-complexes $(X, A) \hookrightarrow (X, A)$ induces a map on relative cohomology. We have the isomorphism
$$
H^i(\Delta(X, A; G)) \cong H^i(C(X, A; G))
$$
for each $A \in \mathcal{A}$, where the left side is simplicial relative cohomology and the right side is singular relative cohomology.

Taking direct limits over $A \in \mathcal{A}$ (directed by inclusion) preserves exactness and isomorphisms. Hence
$$
H_c^i(X;G) \cong \varinjlim_{A \in \mathcal{A}} H^i(\Delta(X, A; G)) \cong \varinjlim_{A \in \mathcal{A}} H^i(C(X, A; G)) \cong H_c^i(X;G)_{\text{singular}}.
$$
Thus the simplicial and singular compactly supported cohomology groups are isomorphic.