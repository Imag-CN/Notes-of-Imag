___

> [!problem] [HAR] II.1.18
> Adjoint Property of $f^{-1}$. Let $f: X \rightarrow Y$ be a continuous map of topological spaces. Show that for any sheaf $\mathscr{F}$ on $X$ there is a natural map $f^{-1} f_{*} \mathscr{F} \rightarrow \mathscr{F}$, and for any sheaf $\mathscr{G}$ on $Y$ there is a natural map $\mathscr{G} \rightarrow f_{*} f^{-1} \mathscr{G}$. Use these maps to show that there is a natural bijection of sets, for any sheaves $\mathscr{F}$ on $X$ and $\mathscr{G}$ on $Y$,
> $$ \operatorname{Hom}_{X}(f^{-1} \mathscr{G}, \mathscr{F}) = \operatorname{Hom}_{Y}(\mathscr{G}, f_{*} \mathscr{F}). $$
> Hence we say that $f^{-1}$ is a left adjoint of $f_{*}$, and that $f_{*}$ is a right adjoint of $f^{-1}$.

**Proof:**
Let
$$
(f^{-1}f_*\mathscr{F})(U) = \varinjlim_{V \supseteq f(U)} \mathscr{F}(f^{-1}(V)),
$$

and
$$
(f_*f^{-1}\mathscr{G})(V) = \varinjlim_{U \supseteq f^{-1}(V)} \mathscr{G}(U).
$$

Define a map $h_1 : f^{-1}f_*\mathscr{F} \to \mathscr{F}$ by $h_{1U}(\overline{\sigma}_{f^{-1}(V)}) = \rho_U^{f^{-1}(V)}(\sigma_{f^{-1}(V)})$. Since $V \supseteq f(f^{-1}(V))$, define $h_2 : \mathscr{G} \to f_*f^{-1}\mathscr{G}$ by $h_{2V}(\sigma_V) = \overline{\sigma}_V$. 

Any $h : f^{-1}\mathscr{G} \to \mathscr{F}$ induces $f_*h : f_*f^{-1}\mathscr{G} \to f_*\mathscr{F}$; pre-composing with $h_2$ gives $\Phi(h) = f_*h \circ h_2 : \mathscr{G} \to f_*\mathscr{F}$. Any $k : \mathscr{G} \to f_*\mathscr{F}$ induces $f^{-1}k : f^{-1}\mathscr{G} \to f^{-1}f_*\mathscr{F}$; composing with $h_1$ gives $\Psi(k) = h_1 \circ f^{-1}k : f^{-1}\mathscr{G} \to \mathscr{F}$.

Verify $\Psi(\Phi(h))=h$: $(h_1 \circ f^{-1}(f_*h) \circ f^{-1}(h_2))_U(\overline{\sigma}_W) = \rho_U^{f^{-1}(W)}(h_W(\sigma_W)) = h_U(\overline{\sigma}_W)$.

Verify $\Phi(\Psi(k))=k$: $(f_*(h_1 \circ f^{-1}k) \circ h_2)_V(\sigma_V) = k_V(\sigma_V)$.

Thus $\Phi,\Psi$ are bijections, so $\operatorname{Hom}_X(f^{-1}\mathscr{G},\mathscr{F}) = \operatorname{Hom}_Y(\mathscr{G},f_*\mathscr{F})$.
___

> [!problem] [HAR] II.2.16
> Let $X$ be a scheme, let $f \in \Gamma(X, \mathcal{O}_X)$, and define $X_f$ to be the subset of points $x \in X$ such that the stalk $f_x$ of $f$ at $x$ is not contained in the maximal ideal $\mathfrak{m}_x$ of the local ring $\mathcal{O}_x$.
>
> (a) If $U = \text{Spec } B$ is an open affine subscheme of $X$, and if $\bar{f} \in B = \Gamma(U, \mathcal{O}_X|_U)$ is the restriction of $f$, show that $U \cap X_f = D(\bar{f})$. Conclude that $X_f$ is an open subset of $X$.
>
> (b) Assume that $X$ is quasi-compact. Let $A = \Gamma(X, \mathcal{O}_X)$, and let $a \in A$ be an element whose restriction to $X_f$ is $0$. Show that for some $n > 0$, $f^n a = 0$.
>
> (c) Now assume that $X$ has a finite cover by open affines $U_i$ such that each intersection $U_i \cap U_j$ is quasi-compact. (This hypothesis is satisfied, for example, if $\text{sp}(X)$ is noetherian.) Let $b \in \Gamma(X_f, \mathcal{O}_{X_f})$. Show that for some $n > 0$, $f^n b$ is the restriction of an element of $A$.
>
> (d) With the hypothesis of (c), conclude that $\Gamma(X_f, \mathcal{O}_{X_f}) \cong A_f$.

**Proof:**
Define $X_f = \{x \in X \mid f_x \notin \mathfrak{m}_x \subseteq \mathcal{O}_x\}$.

**(a)** $x \in U \cap X_f$ iff $x \in U$ and $f_x \notin \mathfrak{m}_x$. Since $U$ is affine, take $x$ as a prime $\mathfrak{p} \in \text{Spec } B$ with maximal ideal $\mathfrak{m} = \mathfrak{p}B_\mathfrak{p}$. $\bar{f} \in \mathfrak{m}$ iff $\bar{f} \in \mathfrak{p}$, so $U \cap X_f = D(\bar{f})$. Since a subset of a topological space is open iff it is open in every element of an open cover, $X_f$ is open in $X$.

**(b)** Assume $X$ quasi-compact. Let $U_i = \text{Spec } A_i$ be a finite affine cover. Restriction of $a$ to $U_i \cap X_f = \text{Spec } (A_i)_f$ is zero, so $f^{n_i}a = 0$ in $A_i$ for some $n_i$. Choose $n > n_i$ for all $i$. Then $f^n a = 0$ on each $\text{Spec } A_i$. Since $X = \bigcup \text{Spec } A_i$ and $\mathcal{O}_X$ is a sheaf, $f^n a = 0$.

**(c)** Let $U_i = \text{Spec } A_i$. $b|_{U_i \cap U_f} = \frac{b_i}{f^{n_i}}$ for each $i$. By finiteness choose common $n$ with $b_i \in A_i$ s.t. $f^n b|_{U_i \cap X_f} = b_i$. On $U_{ij} := U_i \cap U_j$ (quasi-compact), $b_i - b_j$ restricts to zero on $U_{ij} \cap X_f$, so by (b) $\exists m_{ij}$ s.t. $f^{m_{ij}}(b_i - b_j) = 0$. Choose common $m$. Then $f^m b_i$ agree on intersections and lift to global $c \in \Gamma(X, \mathcal{O}_X)$. $c - f^{n+m}b$ restricts to zero on $X_f$, so $c = f^{n+m}b$ on $X_f$. Hence $f^{n+m}b$ is restriction of $c$.

**(d)** Morphism $A_f \to \Gamma(X_f, \mathcal{O}_{X_f})$. If $\frac{a}{f^n}$ in kernel then $a|_{X_f} = 0$, by (b) $f^m a = 0$ so $\frac{a}{f^n} = 0$ (injective). For any $b \in \Gamma(X_f, \mathcal{O}_{X_f})$, by (c) $\exists m, c \in A$ s.t. $f^m b = c|_{X_f}$, so $\frac{c}{f^m} \mapsto b$ (surjective). Thus $\Gamma(X_f, \mathcal{O}_{X_f}) \cong A_f$.
___

> [!problem] [HAR] II.2.17
> A Criterion for Affineness.
>
> (a) Let $f: X \to Y$ be a morphism of schemes, and suppose that $Y$ can be covered by open subsets $U_i$, such that for each $i$, the induced map $f^{-1}(U_i) \to U_i$ is an isomorphism. Then $f$ is an isomorphism.
>
> (b) A scheme $X$ is affine if and only if there is a finite set of elements $f_1, \dots, f_r \in A = \Gamma(X, \mathcal{O}_X)$, such that the open subsets $X_{f_i}$ are affine, and $f_1, \dots, f_r$ generate the unit ideal in $A$. 

**Proof:**
**(a)** Let $U_i$ cover $Y$ with $f^{-1}(U_i) \cong U_i$. $f$ is a homeomorphism since $V = \bigcup (V \cap f^{-1}(U_i))$ is open for any $V \subset X$. Stalks $f_p: \mathcal{O}_{Y,f(p)} \to \mathcal{O}_{X,p}$ are isomorphisms via $f^{-1}(U_i) \cong U_i$. Gluing gives an isomorphism of sheaves, so $f$ is an isomorphism.

**(b)** If $X$ affine take $f_1=1$. Conversely, let $f_1,\dots,f_r \in A=\Gamma(X,\mathcal{O}_X)$ generate $1$ with $X_{f_i}$ affine. Consider $f: X \to \text{Spec } A$. $D(f_i) = \text{Spec } A_{f_i}$ cover $\text{Spec } A$; pre-images are $X_{f_i} \cong \text{Spec } A_{f_i}$ (by 2.16d). Restrict to $\varphi_i: \text{Spec } A_i \to \text{Spec } A_{f_i}$ (isomorphism by Ex. 2.4).

Injectivity of $\varphi_i$: $\frac{a}{f_i^n} \in A_{f_i}$ maps to $0$ on $X_{f_i} \implies \frac{a}{f_i^n}=0$ on intersections $\implies f_j^{n_j}a=0$ in $A_j$. Common $m$ gives $f_i^m a=0$, so $\frac{a}{f_i^n}=0$.

Surjectivity of $\varphi_i$: For $a \in A_i$, on $X_{f_i f_j}$ write $a|_{X_{f_i f_j}} = \frac{b_j}{f_j^{n_i}}$. Finitely many intersections $\implies$ common $n$. On triple intersections $f_k^m(b_j-b_k)=0$. Common $m$ gives $f_i^m b_j$ agreeing on intersections, lifting to global $d$. Restriction of $d$ to $X_{f_i}$ is $f_i^{n+m}a$, so $\frac{d}{f_i^{n+m}} \mapsto a$. By (a), $f$ is an isomorphism, so $X$ is affine.
___

> [!problem] [GOR] 3.6
>Let $p$ be a prime number, and let $X$ be a scheme of characteristic $p$ (Exercise 3.5). Show that there exists a unique morphism $\text{Frob}_X = (f, f^\sharp): X \to X$ of schemes such that $f = \text{id}_X$ and that for every open subset $U \subseteq X$, $f^\sharp_U$ is given by the ring homomorphism $\Gamma(U, \mathcal{O}_X) \to \Gamma(U, \mathcal{O}_X), a \mapsto a^p$.
>
> Give an example of a scheme $X$, such that the morphism $\text{Frob}_X$ induces an isomorphism on the global sections $\Gamma(X, \mathcal{O}_X)$ without being an isomorphism itself.
>
> The morphism $\text{Frob}_X$ is called the *absolute Frobenius morphism* of $X$.

**Proof:**
Define $\text{Frob}_X = (\text{id}_X, f^\sharp)$ where for each open $U \subseteq X$,
$$
f^\sharp_U: \Gamma(U, \mathcal{O}_X) \to \Gamma(U, \mathcal{O}_X), \quad a \mapsto a^p.
$$

In characteristic $p$, $(a+b)^p = a^p + b^p$ and $(ab)^p = a^p b^p$, so $f^\sharp_U$ is a ring homomorphism. It commutes with restrictions because restriction maps are ring homs and $(a|_V)^p = (a^p)|_V$. Hence $f^\sharp$ is a sheaf morphism, and $(\text{id}_X, f^\sharp)$ is a scheme morphism. Uniqueness follows because $f = \text{id}_X$ is fixed and $f^\sharp$ is forced by $a \mapsto a^p$ on every affine open.

**Example:**
Let $X = \mathbb{P}^1_k$ where $k = \overline{\mathbb{F}}_p$.

- $\Gamma(X, \mathcal{O}_X) = k$, and $a \mapsto a^p$ is an automorphism of $k$ since $k$ is perfect.
- On the affine open $U = \text{Spec } k[x]$, $\text{Frob}_X$ induces $k[x] \to k[x]$, $x \mapsto x^p$. This map is not surjective (its image is $k[x^p]$), so it is not an isomorphism of rings. Hence $\text{Frob}_X$ is not an isomorphism of schemes.