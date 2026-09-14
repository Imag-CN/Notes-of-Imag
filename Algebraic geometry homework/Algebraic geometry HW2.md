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

