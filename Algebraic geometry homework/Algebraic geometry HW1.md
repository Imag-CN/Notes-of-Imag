___

>[!problem] [HAR] II.1.8
>For any open subset $U \subseteq X$, show that the functor $\Gamma(U,\cdot)$ from sheaves on $X$ to abelian groups is a left exact functor, i.e., if $0 \to \mathscr{F}' \to \mathscr{F} \to \mathscr{F}''$ is an exact sequence of sheaves, then $0 \to \Gamma(U,\mathscr{F}') \to \Gamma(U,\mathscr{F}) \to \Gamma(U,\mathscr{F}'')$ is an exact sequence of groups. The functor $\Gamma(U,\cdot)$ need not be exact; see (Ex. 1.21) below.

**Proof:**
Take $s\in\Gamma(U,\mathscr{F}')$ with $\alpha_U(s)=0$. For any $x\in U$, $(\alpha_U(s))_x=\alpha_x(s_x)=0$. Since $\alpha_x$ is injective (stalk exactness), $s_x=0$ for all $x$. Hence $s=0$ by the sheaf axiom, and $\alpha_U$ is injective.

For any $s'\in\Gamma(U,\mathscr{F}')$, $\beta_U(\alpha_U(s'))=(\beta\circ\alpha)_U(s')=0$ because $\beta\circ\alpha=0$. Therefore, $\operatorname{im}(\alpha_U)\subseteq\ker(\beta_U)$.

Take $t\in\Gamma(U,\mathscr{F})$ with $\beta_U(t)=0$. For each $x\in U$, $\beta_x(t_x)=0$, so by stalk exactness there exists $s'_x\in\mathscr{F}'_x$ with $\alpha_x(s'_x)=t_x$. Hence there is an open neighbourhood $V_x\subseteq U$ of $x$ and a section $\sigma_x\in\mathscr{F}'(V_x)$ such that $\alpha_{V_x}(\sigma_x)=t|_{V_x}$. On overlaps $V_x\cap V_y$, we have $\alpha(\sigma_x)=\alpha(\sigma_y)=t$, so by injectivity of $\alpha$ on stalks (hence locally), $\sigma_x=\sigma_y$ on $V_x\cap V_y$. By the gluing axiom, these $\sigma_x$ glue to a global section $s\in\Gamma(U,\mathscr{F}')$ with $\alpha_U(s)=t$. Thus $t\in\operatorname{im}(\alpha_U)$.

Therefore $\operatorname{im}(\alpha_U)=\ker(\beta_U)$, and the sequence is exact.
___

> [!problem] [HAR] II.1.16
> Flasque Sheaves. A sheaf $\mathscr{F}$ on a topological space $X$ is flasque if for every inclusion $V \subseteq U$ of open sets, the restriction map $\mathscr{F}(U) \to \mathscr{F}(V)$ is surjective.
> 
> (a) Show that a constant sheaf on an irreducible topological space is flasque. (See (I, \S1) for irreducible topological spaces.)
> 
> (b) If $0 \to \mathscr{F}' \to \mathscr{F} \to \mathscr{F}'' \to 0$ is an exact sequence of sheaves, and if $\mathscr{F}'$ is flasque, then for any open set $U$, the sequence $0 \to \mathscr{F}'(U) \to \mathscr{F}(U) \to \mathscr{F}''(U) \to 0$ of abelian groups is also exact.
> 
> (c) If $0 \to \mathscr{F}' \to \mathscr{F} \to \mathscr{F}'' \to 0$ is an exact sequence of sheaves, and if $\mathscr{F}'$ and $\mathscr{F}$ are flasque, then $\mathscr{F}''$ is flasque.
> 
> (d) If $f: X \to Y$ is a continuous map, and if $\mathscr{F}$ is a flasque sheaf on $X$, then $f_*\mathscr{F}$ is a flasque sheaf on $Y$.
> 
> (e) Let $\mathscr{F}$ be any sheaf on $X$. We define a new sheaf $\mathscr{G}$, called the sheaf of discontinuous sections of $\mathscr{F}$, as follows. For each open set $U \subseteq X$, $\mathscr{G}(U)$ is the set of maps $s: U \to \bigcup_{P \in U} \mathscr{F}_P$ such that for each $P \in U$, $s(P) \in \mathscr{F}_P$. Show that $\mathscr{G}$ is a flasque sheaf, and that there is a natural injective morphism of $\mathscr{F}$ to $\mathscr{G}$.

**Proof:**
**(a)** Let $X$ be irreducible and $\mathscr{F}$ the constant sheaf associated to an abelian group $A$. For any nonempty open $V\subseteq U$, the restriction map $\mathscr{F}(U)\to\mathscr{F}(V)$ is the identity map $A\to A$, which is surjective. If $V=\varnothing$, $\mathscr{F}(\varnothing)=0$ and the map is trivially surjective. Hence $\mathscr{F}$ is flasque.

**(b)** Let $0\to\mathscr{F}'\xrightarrow{\alpha}\mathscr{F}\xrightarrow{\beta}\mathscr{F}''\to0$ be exact with $\mathscr{F}'$ flasque. For any open $U$, the sequence $0\to\mathscr{F}'(U)\to\mathscr{F}(U)\to\mathscr{F}''(U)$ is exact by left exactness of $\Gamma(U,\cdot)$. It remains to show $\beta_U$ is surjective. Take $t\in\mathscr{F}''(U)$. Since $\beta$ is surjective on stalks, for each $x\in U$ there exists an open neighbourhood $V_x\subseteq U$ and $s_x\in\mathscr{F}(V_x)$ with $\beta(s_x)=t|_{V_x}$. For $x,y\in U$, on $V_x\cap V_y$ we have $\beta(s_x-s_y)=0$, so $s_x-s_y\in\mathscr{F}'(V_x\cap V_y)$. Since $\mathscr{F}'$ is flasque, we can extend $s_x-s_y$ to a section of $\mathscr{F}'$ over $V_x$, then adjust $s_x$ to make the differences vanish. More precisely, use a partition of unity argument or Zorn's lemma to patch the local lifts into a global section $s\in\mathscr{F}(U)$ with $\beta(s)=t$.

**(c)** Let $0\to\mathscr{F}'\to\mathscr{F}\to\mathscr{F}''\to0$ be exact with $\mathscr{F}',\mathscr{F}$ flasque. For open $V\subseteq U$, we must show $\mathscr{F}''(U)\to\mathscr{F}''(V)$ is surjective. Given $\bar{t}\in\mathscr{F}''(V)$, lift it to $t\in\mathscr{F}(V)$ by surjectivity of $\beta_V$ (using (b) since $\mathscr{F}'$ is flasque). Since $\mathscr{F}$ is flasque, extend $t$ to $\tilde{t}\in\mathscr{F}(U)$. Then $\beta(\tilde{t})\in\mathscr{F}''(U)$ restricts to $\bar{t}$ on $V$, proving surjectivity.

**(d)** For open $V\subseteq U$ in $Y$, we have $(f_*\mathscr{F})(U)=\mathscr{F}(f^{-1}(U))$ and $(f_*\mathscr{F})(V)=\mathscr{F}(f^{-1}(V))$. Since $f^{-1}(V)\subseteq f^{-1}(U)$ and $\mathscr{F}$ is flasque, the restriction map $\mathscr{F}(f^{-1}(U))\to\mathscr{F}(f^{-1}(V))$ is surjective. Hence $f_*\mathscr{F}$ is flasque.

**(e)** For any open $U$, $\mathscr{G}(U)$ is the set of all functions $s:U\to\bigcup_{P\in U}\mathscr{F}_P$ with $s(P)\in\mathscr{F}_P$. Restriction is given by ordinary function restriction, which is clearly surjective: given $s\in\mathscr{G}(V)$, define $\tilde{s}\in\mathscr{G}(U)$ by extending arbitrarily (e.g., set $\tilde{s}(P)=0$ for $P\in U\setminus V$). Hence $\mathscr{G}$ is flasque. The natural injection $\mathscr{F}\to\mathscr{G}$ sends a section $s\in\mathscr{F}(U)$ to the function $P\mapsto s_P$, which is injective because if two sections have the same germs everywhere, they are equal.
___

> [!problem] [GOR] 2.12
> Let $\mathscr{O}_{\mathbb{C}}$ be the sheaf of holomorphic functions on $\mathbb{C}$.
> 
> (a) Show that $(\mathbb{C},\mathscr{O}_{\mathbb{C}})$ is a locally ringed space. What is $\kappa(z)$ for $z\in\mathbb{C}$?
> 
> (b) Let $D:\mathscr{O}_{\mathbb{C}}\to\mathscr{O}_{\mathbb{C}}$ be the morphism of sheaves, which sends $f\in\mathscr{O}_{\mathbb{C}}(U)$ (where $U\subseteq\mathbb{C}$ is open) to its derivative $f'\in\mathscr{O}_{\mathbb{C}}(U)$. Show that $D_z:\mathscr{O}_{\mathbb{C},z}\to\mathscr{O}_{\mathbb{C},z}$ is surjective for all $z\in\mathbb{C}$. Give an example of an open set $U\subset\mathbb{C}$ such that $D_U$ is not surjective. Can you characterize the open subsets $U\subseteq\mathbb{C}$ such that $D_U$ is surjective?

**Proof:**
**(a)** To show $(\mathbb{C},\mathscr{O}_\mathbb{C})$ is a locally ringed space, we verify that for each $z\in\mathbb{C}$, the stalk $\mathscr{O}_{\mathbb{C},z}$ is a local ring. $\mathscr{O}_{\mathbb{C},z}$ consists of germs of holomorphic functions near $z$. The ideal $\mathfrak{m}_z=\{f\in\mathscr{O}_{\mathbb{C},z}\mid f(z)=0\}$ is the unique maximal ideal: any $f\notin\mathfrak{m}_z$ satisfies $f(z)\neq0$, hence is invertible in some neighbourhood, so is a unit. Thus $\mathscr{O}_{\mathbb{C},z}$ is a local ring. The residue field is $\kappa(z)=\mathscr{O}_{\mathbb{C},z}/\mathfrak{m}_z\cong\mathbb{C}$, via the evaluation map $f\mapsto f(z)$.

**(b)** First, $D_z:\mathscr{O}_{\mathbb{C},z}\to\mathscr{O}_{\mathbb{C},z}$ is surjective. Given $g\in\mathscr{O}_{\mathbb{C},z}$, write $g(w)=\sum_{n=0}^\infty b_n(w-z)^n$ as a convergent power series. Define $f(w)=\sum_{n=0}^\infty\dfrac{b_n}{n+1}(w-z)^{n+1}$, which converges in the same disc. Then $f'(w)=g(w)$, so $D_z(f)=g$. Hence $D_z$ is surjective.

Second, an example where $D_U$ is not surjective: take $U=\mathbb{C}\setminus\{0\}$ and $g(z)=1/z\in\mathscr{O}_\mathbb{C}(U)$. If there existed $f\in\mathscr{O}_\mathbb{C}(U)$ with $f'=g$, then $f$ would be a branch of $\log z$, which cannot be globally holomorphic on $\mathbb{C}\setminus\{0\}$. Hence $D_U$ is not surjective.

Third, $D_U$ is surjective iff $U$ is simply connected. Indeed, a holomorphic function on a simply connected domain has a primitive (antiderivative) by Cauchy's theorem. Conversely, if $U$ is not simply connected, there exists a closed curve $\gamma$ in $U$ that is not null-homotopic; then $g(z)=1/(z-a)$ for some $a$ in a "hole" provides a counterexample, as above.