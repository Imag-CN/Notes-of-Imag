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

Define a map $h_1 : f^{-1}f_*\mathscr{F} \to \mathscr{F}$ by $h_{1U}(\overline{\sigma}_{f^{-1}(V)}) = \rho_U^{f^{-1}(V)}(\sigma_{f^{-1}(V)})$. Since $V \supseteq f(f^{-1}(V))$, define $h_2 : \mathscr{G} \to f_*f^{-1}\mathscr{G}$ by $h_{2V}(\sigma_V) = \overline{\sigma}_V$. Any $h : f^{-1}\mathscr{G} \to \mathscr{F}$ induces $f_*h : f_*f^{-1}\mathscr{G} \to f_*\mathscr{F}$. Pre-composing with $h_2$ we get $f_*h \circ h_2 : \mathscr{G} \to f_*\mathscr{F}$. Any $h : \mathscr{G} \to f_*\mathscr{F}$ induces $f^{-1}h : f^{-1}\mathscr{G} \to f^{-1}f_*\mathscr{F}$ and composing with $h_1$, we get $h_1 \circ f^{-1}h : f^{-1}\mathscr{G} \to \mathscr{F}$.

Therefore, the Hom groups are isomorphic.
___

