___

>[!problem] [HAT] 2.1.24
>Show that each $n$-simplex in the barycentric subdivision of $\Delta^n$ is defined by $n$ inequalities
>$$
>t_{i_0}\leq t_{i_1}\leq\cdots\leq t_{i_n}
>$$
>in its barycentric coordinates, where $(i_0,\dots,i_n)$ is a permutation of $(0,\dots,n)$.

**Proof:**
Let $\Delta^n=[v_0,\dots,v_n]$ with barycentric coordinates $(t_0,\dots,t_n)$ where $t_i\ge0$ and $\sum_i t_i=1$. For $n=0$, the statement is trivial. Assume the statement holds for dimension $n-1$.

Let $b=(\frac1{n+1},\dots,\frac1{n+1})$ be the barycenter. Each $n$-simplex in the subdivision is of the form $[b,w_0,\dots,w_{n-1}]$, where $[w_0,\dots,w_{n-1}]$ is an $(n-1)$-simplex in the barycentric subdivision of a face $\sigma=[v_0,\dots,\hat v_i,\dots,v_n]$. In $\sigma$, $t_i=0$.

By induction, $[w_0,\dots,w_{n-1}]$ is described by a permutation $(j_1,\dots,j_n)$ of $\{0,\dots,n\}\setminus\{i\}$ satisfying $t_{j_1}\le\dots\le t_{j_n}$, with $t_{j_1}=0$. For any $p=\lambda b+(1-\lambda)q$ ($0\le\lambda\le1$, $q\in[w_0,\dots,w_{n-1}]$), we have $t_k=\frac{\lambda}{n+1}+(1-\lambda)s_k$ where $(s_0,\dots,s_n)$ are the barycentric coordinates of $q$ with $s_i=0$. Then $t_k-t_i=(1-\lambda)s_k\ge0$, so $t_k\ge t_i$ for all $k\neq i$, with equality iff $s_k=0$. In particular, $t_{j_1}=t_i$. Thus we obtain a permutation $(i_0,\dots,i_n)$ of $\{0,\dots,n\}$ (by setting $i_0=i$ and suitably ordering the rest) such that $t_{i_0}\le t_{i_1}\le\dots\le t_{i_n}$.

Conversely, given such a permutation, let $i=i_0$; then $t_{i_0}=0$ corresponds to the face omitting $v_{i_0}$, and the remaining permutation describes an $(n-1)$-simplex in the subdivision of that face, which together with $b$ yields the desired $n$-simplex. This completes the induction.
___

>[!problem] [HAT] 2.1.25
>Find an explicit, noninductive formula for the barycentric subdivision operator $S:C_n(X)\to C_n(X)$.

**Proof:**
The barycentric subdivision operator $S_n:C_n(X)\to C_n(X)$ is defined on a singular $n$-simplex $\sigma$ by
$$
S_n(\sigma)=\sum_{\pi\in \mathfrak{S}_{n+1}}\operatorname{sgn}(\pi)\,\sigma_{b_\pi},
$$
where $\sigma_{b_\pi}:\Delta^n\to X$ is the affine map sending the vertices of $\Delta^n$ in order to the vertices of the simplex $b_\pi$ in $\Delta^n$ and then composed with $\sigma$. (The sign accounts for orientation consistency.)
___

>[!problem] [HAT] 2.1.28
>Let $X$ be the cone on the $1$-skeleton of $\Delta^3$, the union of all line segments joining points in the six edges of $\Delta^3$ to the barycenter of $\Delta^3$. Compute the local homology groups $H_n(X, X - \{x\})$ for all $x \in X$. Define $\partial X$ to be the subspace of points $x$ such that $H_n(X, X - \{x\}) = 0$ for all $n$, and compute the local homology groups $H_n(\partial X, \partial X - \{x\})$. Use these calculations to determine which subsets $A \subset X$ have the property that $f(A) \subset A$ for all homeomorphisms $f: X \to X$.

**Proof:**
Let $B_r(x)$ be the $r$-neighborhood of $x$ in $X$. For small $r$, $H_*(X,X-x)\cong H_*(B_r(x),L_r(x))$, where $L_r(x)=\partial B_r(x)$ is the "link" of $x$ in $X$. The reduced homology of the quotient $B_r(x)/L_r(x)$ gives the local homology.

- $x$ in interior of a 2‑face: $B_r(x)/L_r(x)\simeq S^2\Rightarrow H_2\cong\mathbb Z$, others 0.
- $x$ on an edge $[V_iV_j]$ of $\Delta^3$: $B_r(x)$ is a half‑disk, $L_r(x)$ a half‑circle $\Rightarrow H_n\cong0$.
- $x$ on an edge $[OV_i]$ ($O$ is the barycenter): $B_r(x)$ is three half‑disks glued along diameters $\Rightarrow B_r/L_r\simeq S^2\vee S^2\Rightarrow H_2\cong\mathbb Z^2$, others 0.
- $x$ is a vertex $V_i$: $B_r/L_r$ contractible $\Rightarrow H_n\cong0$.
- $x=O$: $B_r\simeq X$, $L_r=Y$ (1‑skeleton of $\Delta^3$). From the exact sequence of $(X,Y)$ and contractibility of $X$, $H_2\cong H_1(Y)\cong\mathbb Z^3$, others 0.

Hence $\partial$ is the 1‑skeleton of $\Delta^3$.

For $x\in Y$, the same neighborhood analysis gives:
- $x$ a vertex $V_i$: $H_1\cong\mathbb Z^2$, others 0.
- $x$ in interior of an edge $[V_iV_j]$: $H_1\cong\mathbb Z$, others 0.

A homeomorphism preserves local homology, hence preserves the following orbit decomposition:
(1) $\{O\}$ (unique point with $H_2\cong\mathbb Z^3$)
(2) Four vertices $V_i$ ($H_n\cong0$ but different local homology on $Y$ from edge points)
(3) Interiors of edges $[OV_i]$ ($H_2\cong\mathbb Z^2$)
(4) Interiors of edges $[V_iV_j]$ ($H_n\cong0$ but belong to $\partial X$)
(5) Interiors of $2$‑faces ($H_2\cong\mathbb Z$)

Therefore $A\subset X$ satisfies $f(A)\subset A$ for all homeomorphisms $f$ iff $A$ is a union of these orbits.
___

>[!problem] [HAT] 2.1.29
>Show that $S^{1}\times S^{1}$ and $S^{1}\vee S^{1}\vee S^{2}$ have isomorphic homology groups in all dimensions, but their universal covering spaces do not.

**Proof:**
Both spaces have homology groups: 
- $H_0\cong\mathbb Z$,
- $H_1\cong\mathbb Z^2$,
- $H_2\cong\mathbb Z$,
- $H_n=0$ for $n\ge3$.

The universal cover of $S^1\times S^1$ is $\mathbb R^2$, whose $H_{2}$ is trivial. But the universal cover of $S^1\vee S^1\vee S^2$ is the wedge product of an $S^{2}$ and some other space, and the $H_{2}$ of $S^{2}$ is non-trivial, so the $H_{2}$ of the universal cover of $S^1\vee S^1\vee S^2$ is non-trivial.