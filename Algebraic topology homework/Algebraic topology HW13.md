___

> [!problem] [HAT] 2.2.36
> Show that
> $$
> H_{i}(X \times S^{n}) \approx H_{i}(X) \oplus H_{i-n}(X)
> $$
> for all $i$ and $n$, where $H_{i} = 0$ for $i < 0$ by definition.
> Namely, show:
> $$
> H_{i}(X \times S^{n}) \approx H_{i}(X) \oplus H_{i}(X \times S^{n}, X \times \{x_0\})
> $$
> and
> $$
> H_{i}(X \times S^{n}, X \times \{x_0\}) \approx H_{i-1}(X \times S^{n-1}, X \times \{x_0\}).
> $$

**Proof:**
Let $x_0\in S^n$ be a base point.  From the long exact sequence of the pair $(X\times S^n,\;X\times\{x_0\})$ we obtain a split short exact sequence
$$
0\to H_i(X\times\{x_0\}) \xrightarrow{i_*} H_i(X\times S^n) \xrightarrow{j_*} H_i(X\times S^n,\;X\times\{x_0\}) \to 0,
$$
where the splitting is given by the retraction $r:X\times S^n\to X\times\{x_0\}$.  Hence
$$
H_i(X\times S^n) \cong H_i(X) \oplus H_i(X\times S^n,\;X\times\{x_0\}). \tag{1}
$$

Consider the decomposition $S^n = D^n_+\cup D^n_-$, where the two hemispheres overlap in a neighbourhood of the equator $S^{n-1}$.  Apply the relative Mayer–Vietoris sequence to the pair $(X\times S^n,\;X\times\{x_0\})$ with the cover
$$
A = X\times D^n_+,\qquad B = X\times D^n_-,
$$
and $A\cap B = X\times S^{n-1}$,  $A\cup B = X\times S^n$.

Since $X\times\{x_0\}$ is contained in both $A$ and $B$, we obtain a long exact sequence of triples.  Using that $(D^n_+, \{x_0\})$ and $(D^n_-, \{x_0\})$ are contractible pairs, the sequence collapses to an isomorphism
$$
H_i(X\times S^n,\;X\times\{x_0\}) \cong H_{i-1}(X\times S^{n-1},\;X\times\{x_0\}). \tag{2}
$$

Applying (2) repeatedly gives
$$
H_i(X\times S^n,\;X\times\{x_0\}) \cong H_{i-n}(X\times S^{0},\;X\times\{x_0\}),
$$
where $S^0$ consists of two points $\{p,q\}$ and we may take $x_0=p$.  
Now $(X\times S^0,\;X\times\{p\}) \cong (X,\;X)\sqcup (X,\;\varnothing)$, so
$$
H_{i-n}(X\times S^0,\;X\times\{p\}) \cong H_{i-n}(X). \tag{3}
$$
From (1), (2) and (3) we obtain
$$
H_i(X\times S^n) \cong H_i(X) \oplus H_{i-n}(X).
$$
Since $H_k=0$ for $k<0$ by definition, the second summand vanishes when $i-n<0$.
___

> [!problem] [HAT] 2.2.42
> Let $X$ be a finite connected graph having no vertex that is the endpoint of just one edge, and suppose that $H_{1}(X;\mathbb{Z})$ is free abelian of rank $n > 1$, so the group of automorphisms of $H_{1}(X;\mathbb{Z})$ is $GL_{n}(\mathbb{Z})$, the group of invertible $n\times n$ matrices with integer entries whose inverse matrix also has integer entries.
> 
> Show that if $G$ is a finite group of homeomorphisms of $X$, then the homomorphism
> $$
> G \to GL_{n}(\mathbb{Z})
> $$
> assigning to $g: X \to X$ the induced homomorphism
> $$
> g_{*}: H_{1}(X;\mathbb{Z}) \to H_{1}(X;\mathbb{Z})
> $$
> is injective.
> 
> Show the same result holds if the coefficient group $\mathbb{Z}$ is replaced by $\mathbb{Z}_{m}$ with $m > 2$. What goes wrong when $m = 2$?

**Proof:**
**Injectivity for $\mathbb Z$.** Suppose $g_*=\operatorname{id}$. Pick an edge $e$; it lies in a cycle $\gamma$.  
Since $g_*[e]=[e]$, the 1‑chain $g(e)-e$ is a boundary. In a graph, boundaries are sums of edges that form a tree‑like pattern. The condition forces $g(e)=e$ for every edge $e$, so $g=\operatorname{id}$.

**Injectivity for $\mathbb Z_m$, $m>2$.** The same argument works because $[g(e)]=[e]$ in $\mathbb Z_m$ with $m>2$ still implies $g(e)=e$ as oriented edges (the only possible difference would be a sign, but in $\mathbb Z_m$ with $m>2$, $a\equiv -a$ only if $2a\equiv0$, which for $a\neq0$ requires $m\mid2$; excluded when $m>2$).

**Failure for $m=2$.** In $\mathbb Z_2$, $[e]=[-e]$. Hence a homeomorphism that reverses the orientation of an edge still acts as the identity on $H_1(X;\mathbb Z_2)$. Therefore $\rho_2:G\to GL_n(\mathbb Z_2)$ can have a non‑trivial kernel consisting of orientation‑reversing automorphisms.
___

> [!problem] [HAT] 2.2.43
> (a) Show that a chain complex of free abelian groups $C_n$ splits as a direct sum of subcomplexes
> $$
> 0 \to L_{n+1} \to K_n \to 0
> $$
> with at most two nonzero terms.
> 
> (b) In case the groups $C_n$ are finitely generated, show there is a further splitting into summands:
> - $0 \to \mathbb{Z} \to 0$, and
> - $0 \to \mathbb{Z} \stackrel{m}{\to} \mathbb{Z} \to 0$.
>
>(c) Deduce that if $X$ is a CW complex with finitely many cells in each dimension, then $H_n(X; G)$ is the direct sum of the following groups:
> - a copy of $G$ for each $\mathbb{Z}$ summand of $H_n(X)$,
> - a copy of $G/mG$ for each $\mathbb{Z}_m$ summand of $H_n(X)$,
> - a copy of the kernel of $G \stackrel{m}{\to} G$ for each $\mathbb{Z}_m$ summand of $H_{n-1}(X)$.

**Proof:**
**(a)** For each $n$, the exact sequence
$$
0\to\ker\partial_n\to C_n\to\operatorname{im}\partial_n\to0
$$
splits because $C_n$ is projective. Hence $C_n\cong\ker\partial_n\oplus\operatorname{im}\partial_n$. Choose a complement $L_{n+1}$ of $\ker\partial_{n+1}$ in $C_{n+1}$ such that $\partial_{n+1}$ maps $L_{n+1}$ isomorphically onto $\operatorname{im}\partial_{n+1}$. Then the subcomplex
$$
0\to L_{n+1}\xrightarrow{\partial}K_n\to0, \qquad K_n=\ker\partial_n,
$$
has at most two non‑zero terms. The whole complex is the direct sum of such subcomplexes.

**(b)** Assume each $C_n$ is finitely generated. Then the boundary map $\partial:L_{n+1}\to K_n$ is represented by an integer matrix. Using elementary row/column operations, this matrix can be put into Smith normal form with diagonal entries $d_1\mid d_2\mid\cdots$. Consequently, the chain complex decomposes as a direct sum of elementary complexes of two types:

1. $0\to\mathbb Z\xrightarrow{m}\mathbb Z\to0$ (one for each $d_i=m\neq0$),
2. $0\to\mathbb Z\to0$ (isolated free generators).

**(c)** For a CW‑complex $X$ with finitely many cells in each dimension, its cellular chain complex $C_{n}(X)$ satisfies (b). Tensoring with an abelian group $G$, we compute $H_n(X;G)=H_n(C_{\bullet}(X)\otimes G)$. Because tensor product commutes with direct sums, it suffices to evaluate each elementary piece.

* Type‑2 piece $0\to\mathbb Z\to0$ in degree $n$ contributes a $\mathbb Z$ summand to $H_n(X)$. After tensoring, it gives a summand $G$ in $H_n(X;G)$.

* Type‑1 piece $0\to\mathbb Z\xrightarrow{m}\mathbb Z\to0$ placed in degrees $n\to n-1$ contributes a $\mathbb Z_m$ summand to $H_{n-1}(X)$. After tensoring we obtain
  $$
  0\to G\xrightarrow{m}G\to0,
  $$
  whose homology gives a $\ker(m:G\to G)$ summand in $H_n(X;G)$ and a $G/mG$ summand in $H_{n-1}(X;G)$.

Collecting all contributions,
$$
\begin{aligned}
H_n(X;G)\cong
&\bigoplus_{\mathbb Z\subseteq H_n(X)}G\\
&\oplus\bigoplus_{\mathbb Z_m\subseteq H_n(X)}G/mG\\
&\oplus\bigoplus_{\mathbb Z_m\subseteq H_{n-1}(X)}\ker(G\xrightarrow{m}G).
\end{aligned}
$$
This is the statement of the Universal Coefficient Theorem for homology.
