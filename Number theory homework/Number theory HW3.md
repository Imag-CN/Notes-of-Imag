___
*Using DeepSeek to help write markdown problem statements, provided ideas for problem 3 and 4, and enhance writing conventions.*
___

>[!problem] Problem 1
>Let $L/\mathbb{Q}$ be a cubic field, namely $[L:\mathbb{Q}] = 3$, in which the prime $(2)$ splits completely.
>
>(i) Show that the ring of integers $\mathcal{O}_L$ (the integral closure of $\mathbb{Z}$ in $L$) is not monogenic, that is, $\mathcal{O}_L = \mathbb{Z}[\beta]$ for no element $\beta \in \mathcal{O}_L$.
>
>(ii) Consider $L = \mathbb{Q}(\alpha)$, where $\alpha$ is a root of $x^3 - x^2 - 2x - 8$. It is known that $\mathcal{O}_L = \mathbb{Z} \oplus \mathbb{Z}\alpha \oplus \mathbb{Z}\frac{\alpha^2+\alpha}{2}$ as a $\mathbb{Z}$-submodule of $L$. (We'll be able to prove this later but you need not check this in this homework.) Verify that the prime $(2)$ splits completely in $L$.

**Proof:**
**(i)** Assume for contradiction that $\mathcal{O}_L = \mathbb{Z}[\beta]$ for some $\beta \in \mathcal{O}_L$. Let $f(x) \in \mathbb{Z}[x]$ be the minimal polynomial of $\beta$, so $\deg f = 3$. Since $(2)$ splits completely in $L$, the reduction $\bar{f}(x) \in \mathbb{F}_2[x]$ factors into three distinct linear factors over $\mathbb{F}_2$. But $\mathbb{F}_2$ has only two distinct linear polynomials, namely $x$ and $x+1$, so it is impossible for $\bar{f}$ to have three distinct linear factors, contradiction. Hence $\mathcal{O}_L$ is not monogenic.

**(ii)** It suffices to prove $\mathcal{O}_L/(2) \cong \mathbb{F}_2^3$.

Let $\beta = \frac{\alpha^2 + \alpha}{2}$, so $\mathcal{O}_L = \{ x + y\alpha + z\beta \mid x,y,z \in \mathbb{Z} \}$.
From $\alpha^3 - \alpha^2 - 2\alpha - 8 = 0$ and $\beta = \frac{\alpha^2 + \alpha}{2}$, we obtain:
$$
\alpha^2 = -\alpha + 2\beta,\quad \alpha\beta = 2\beta + 4,\quad \beta^2 = 2\alpha + 3\beta + 2.
$$
Reducing modulo 2, we have:
$$
\overline{\alpha}^2 = \overline{\alpha},\quad \overline{\alpha}\,\overline{\beta} = \overline{0},\quad \overline{\beta}^2 = \overline{\beta}.
$$
Define a ring homomorphism $\varphi: \mathcal{O}_L/(2) \to \mathbb{F}_2 \oplus \mathbb{F}_2 \oplus \mathbb{F}_2$ by:
$$
\varphi(\overline{1}) = (1,1,1),\quad \varphi(\overline{\alpha}) = (1,0,0),\quad \varphi(\overline{\beta}) = (0,1,0).
$$
It is straightforward to verify that $\varphi$ is an isomorphism. Hence $\mathcal{O}_L/(2) \cong \mathbb{F}_2^3$, proving that $(2)$ splits completely in $L$.
___

> [!problem] Problem 2
> Consider $L = \mathbb{Q}(\sqrt{7}, \sqrt{10})$. Prove that $\mathcal{O}_L$ (notation as above) is not monogenic.

**Proof:**
Assume for contradiction that $\mathcal{O}_L = \mathbb{Z}[\alpha]$ for some $\alpha \in \mathcal{O}_L$. Let $f(x) \in \mathbb{Z}[x]$ be the minimal polynomial of $\alpha$ over $\mathbb{Z}$, so $\deg f = [L:\mathbb{Q}] = 4$. For any $g \in \mathbb{Z}[x]$, let $\overline{g}$ denote its reduction modulo 3 in $\mathbb{Z}_3[x]$.

For $g \in \mathbb{Z}[x]$, $g(\alpha)$ is divisible by $3$ in $\mathbb{Z}[\alpha]$ iff $\overline{g}$ is divisible by $\overline{f}$ in $\mathbb{Z}_3[x]$. This follows because $\mathbb{Z}[\alpha] \cong \mathbb{Z}[x]/(f(x))$, and reducing modulo $3$ gives $\mathbb{F}_3[\alpha] \cong \mathbb{F}_3[x]/(\overline{f}(x))$.

Consider the four algebraic integers:
$$ \alpha_1 = (1+\sqrt{7})(1+\sqrt{10}), \quad \alpha_2 = (1+\sqrt{7})(1-\sqrt{10}) $$
$$ \alpha_3 = (1-\sqrt{7})(1+\sqrt{10}), \quad \alpha_4 = (1-\sqrt{7})(1-\sqrt{10}) $$
It's easy to check that all products $\alpha_i \alpha_j$ ($i \neq j$) are divisible by $3$ in $\mathbb{Z}[\alpha]$.

Note that the trace is $T^K(\alpha_i^n) = \alpha_1^n + \alpha_2^n + \alpha_3^n + \alpha_4^n$, which is congruent modulo $3$ to $(\alpha_1+\alpha_2+\alpha_3+\alpha_4)^n = 4^n \equiv 1^n \equiv 1 \pmod 3$. Hence $\alpha_i^n \notin 3\mathcal{O}_L$.

Write $\alpha_i = f_i(\alpha)$ with $f_i \in \mathbb{Z}[x]$. Since $\alpha_i \alpha_j \in 3\mathbb{Z}[\alpha]$, we have $\overline{f} \mid \overline{f_i}\overline{f_j}$ in $\mathbb{F}_3[x]$. Since $\alpha_i^n \notin 3\mathbb{Z}[\alpha]$, we have $\overline{f} \nmid \overline{f_i}^n$. As $\mathbb{F}_3[x]$ is a UFD, for each $i$ there exists an irreducible factor $p_i$ of $\overline{f}$ such that $p_i \nmid \overline{f_i}$ but $p_i \mid \overline{f_j}$ for all $j \neq i$. Thus the $p_i$ ($i=1,2,3,4$) are four distinct irreducible factors of $\overline{f}$.

However, $\mathbb{F}_3$ has only three distinct linear polynomials, namely $x$, $x+1$ and $x+2$, so it is impossible for $\bar{f}$ to have four distinct linear factors, contradiction. Therefore $\mathcal{O}_L$ is not monogenic.
___

>[!problem] Problem 3
>Let $A$ be a Dedekind domain, $K = \operatorname{Frac}(A)$. Let $L/K$ be a finite separable extension with normal closure $M$ of $L$ so that $M$ is Galois over $K$. Let $\mathfrak{p}$ be a prime ideal of $A$. (You don't need to assume $\mathfrak{p}$ to be unramified.) Fix a prime ideal $\mathfrak{r}$ of $M$ above $\mathfrak{p}$. (By convention, this means $\mathfrak{r}$ is a nonzero prime in the integral closure of $A$ in $M$ such that $\mathfrak{r}$ divides $\mathfrak{p}$.) Denote by $D_{\mathfrak{r}}(M/K)$ the decomposition group of $\mathfrak{r}$ in $M/K$.
>
>(i) Define a map
>$$
>\operatorname{Gal}(M/K) \longrightarrow \{\text{primes of } L \text{ above } \mathfrak{p}\}, \quad \sigma \longmapsto \sigma(\mathfrak{r}) \cap L.
>$$
>
>Show that this map induces a bijection
>$$
>\operatorname{Gal}(M/L) \backslash \operatorname{Gal}(M/K) / D_{\mathfrak{r}}(M/K) \xrightarrow{\sim} \{\text{primes of } L \text{ above } \mathfrak{p}\}.
>$$
>
>**Note**: When $H, K$ are subgroups of $G$, one can think of $H \backslash G / K$ as the set of orbits of $K$ on $H \backslash G$ via right multiplication. To put it another way, an element of $H \backslash G / K$ is an equivalence class of elements of $G$, where $g$ and $g'$ are equivalent if there are $h \in H$ and $k \in K$ such that $g' = hgk$.
>
>In the problem, well-definedness $+$ injectivity amounts to: $\sigma, \sigma' \in \operatorname{Gal}(M/K)$ have the same image if and only if $\sigma' = \alpha \sigma \beta$ for some $\alpha \in \operatorname{Gal}(M/L)$ and $\beta \in D_{\mathfrak{r}}(M/K)$.
>
>(ii) Assume that $\operatorname{Gal}(M/K) \simeq S_3$, the symmetric group in $3$ variables, that $D_{\mathfrak{r}}(M/K)$ and $\operatorname{Gal}(M/L)$ are order $2$ subgroups of $\operatorname{Gal}(M/K)$ which are equal (not just isomorphic).
>
>Use part (i) to verify that $\mathfrak{p}$ does not split completely in $L$.

**Proof:**
**(i)** Denote the map by $\Phi$.

*Surjectivity:* Let $\mathfrak{q}$ be a prime of $L$ above $\mathfrak{p}$. Choose a prime $\mathfrak{R}$ of $M$ above $\mathfrak{q}$; then $\mathfrak{R}$ also lies above $\mathfrak{p}$. Since $G$ acts transitively on the primes of $M$ above $\mathfrak{p}$, there exists $\sigma \in G$ such that $\sigma(\mathfrak{r}) = \mathfrak{R}$. Then $\Phi(\sigma) = \mathfrak{R} \cap L = \mathfrak{q}$.

*Well-definedness $+$ injectivity:* Suppose $\sigma, \sigma' \in G$ satisfy $\Phi(\sigma) = \Phi(\sigma') = \mathfrak{q}$. Then $\sigma(\mathfrak{r})$ and $\sigma'(\mathfrak{r})$ are both primes of $M$ above $\mathfrak{q}$. Since $H = \operatorname{Gal}(M/L)$ acts transitively on the primes of $M$ above $\mathfrak{q}$, there exists $\alpha \in H$ such that $\alpha(\sigma(\mathfrak{r})) = \sigma'(\mathfrak{r})$. Hence $\sigma^{-1}\alpha^{-1}\sigma'(\mathfrak{r}) = \mathfrak{r}$, so $\beta := \sigma^{-1}\alpha^{-1}\sigma' \in D$. Thus $\sigma' = \alpha\sigma\beta$.

Conversely, if $\sigma' = \alpha\sigma\beta$ with $\alpha \in H$ and $\beta \in D$, then
$$
\Phi(\sigma') = \alpha\sigma\beta(\mathfrak{r}) \cap L = \alpha\sigma(\mathfrak{r}) \cap L = \alpha(\sigma(\mathfrak{r}) \cap L) = \sigma(\mathfrak{r}) \cap L = \Phi(\sigma),
$$
since $\alpha$ fixes $L$ pointwise and $\beta(\mathfrak{r}) = \mathfrak{r}$.

Therefore $\Phi(\sigma) = \Phi(\sigma')$ iff $\sigma' \in H\sigma D$. Hence $\Phi$ induces a bijection
$$
H \backslash G / D \xrightarrow{\sim} \{\text{primes of } L \text{ above } \mathfrak{p}\}.
$$

**(ii)** Now suppose $G \cong S_3$, and $H = D$ is an order-$2$ subgroup of $G$ (so $H = D$ is generated by a single transposition). Then $[L:K] = |G|/|H| = 6/2 = 3$.

If $\mathfrak{p}$ split completely in $L$, there would be exactly $3$ primes of $L$ above $\mathfrak{p}$. By part (i), this number equals $|H \backslash G / H|$.

We compute $|H \backslash G / H|$. Let $G=\left< x,y|x^{3}=y^{2}=1 \right>$ and $H$ generated by $y$. Then the equivalent classes are $\{ 1,y \}$ and $\{ x,x^{2},xy,x^{2}y \}$. Therefore $|H \backslash G / H|=2$,there are only $2$ primes of $L$ above $\mathfrak{p}$. Hence $\mathfrak{p}$ does not split completely in $L$.

>[!remark] Remark
>The point of (ii) is that when the decomposition group of $\mathfrak{r}$ is not normal in $\operatorname{Gal}(M/K)$, the prime $\mathfrak{r}$ need not split completely in the decomposition field, which is $L$ here. A concrete example for (ii) can be given when $K = \mathbb{Q}$, $L = \mathbb{Q}(\sqrt[3]{2})$, $M = \mathbb{Q}(\sqrt[3]{2}, \zeta_3)$. By the Chebotarev density theorem, or by explicit computation, you can find $\mathfrak{r}$ such that $(\mathfrak{r}, M/K)$ is the unique nontrivial element of $\operatorname{Gal}(M/L)$. Then all the conditions of (ii) are satisfied.

___

>[!problem] Problem 4 (Neukirch Ch. I.9, Exercise 3)
>Continue the general setup from Problem 3. Assume the following:
>
>(i) $L/K$ is solvable, meaning that $\operatorname{Gal}(M/K)$ is a solvable group. (We are not assuming $M = L$.)
>
>(ii) $p := [L : K]$ is a prime number.
>
>Now let $\mathfrak{p}$ be a prime of $K$ unramified in $L$. If there are two primes $\mathfrak{q}$ and $\mathfrak{q}'$ of $L$ above $\mathfrak{p}$ such that the inertial degrees $f_{\mathfrak{q}}$ and $f_{\mathfrak{q}'}$ are equal to $1$, then show that $\mathfrak{p}$ splits completely in $L/K$.
>
>**Caveat:** The extension degree $p$ has nothing to do with the prime ideal $\mathfrak{p}$ in the problem.
>
>**Hint:** Feel free to use the following group-theoretic facts. Let $p$ be a prime number. Let $S_p$ denote the symmetric group in $p$ letters acting on $\{1, 2, \dots, p\}$. If $G$ is a solvable subgroup of $S_p$ acting transitively on $\{1, 2, \dots, p\}$ then every nontrivial element of $G$ fixes at most one element in $\{1, 2, \dots, p\}$. (A reference for this fact is given in Neukirch.)

**Proof:**
**(i)** Let $G = \operatorname{Gal}(M/K)$, $H = \operatorname{Gal}(M/L)$, and $D = D_{\mathfrak{r}}(M/K)$. Define
$$
\Phi: G \longrightarrow \{\text{primes of } L \text{ above } \mathfrak{p}\}, \quad \Phi(\sigma) = \sigma(\mathfrak{r}) \cap L.
$$

*Well-definedness:* For any $\sigma \in G$, $\sigma(\mathfrak{r})$ is a prime of $M$ lying above $\mathfrak{p}$, so its intersection with $L$ is a prime of $L$ lying above $\mathfrak{p}$.

*Surjectivity:* Let $\mathfrak{q}$ be a prime of $L$ above $\mathfrak{p}$. Choose a prime $\mathfrak{R}$ of $M$ above $\mathfrak{q}$; then $\mathfrak{R}$ also lies above $\mathfrak{p}$. Since $G$ acts transitively on the primes of $M$ above $\mathfrak{p}$, there exists $\sigma \in G$ such that $\sigma(\mathfrak{r}) = \mathfrak{R}$. Then $\Phi(\sigma) = \mathfrak{R} \cap L = \mathfrak{q}$.

*Fibers:* Suppose $\sigma, \sigma' \in G$ satisfy $\Phi(\sigma) = \Phi(\sigma') = \mathfrak{q}$. Then $\sigma(\mathfrak{r})$ and $\sigma'(\mathfrak{r})$ are both primes of $M$ above $\mathfrak{q}$. Since $H = \operatorname{Gal}(M/L)$ acts transitively on the primes of $M$ above $\mathfrak{q}$, there exists $\alpha \in H$ such that $\alpha(\sigma(\mathfrak{r})) = \sigma'(\mathfrak{r})$. Hence $\sigma^{-1}\alpha^{-1}\sigma'(\mathfrak{r}) = \mathfrak{r}$, so $\beta := \sigma^{-1}\alpha^{-1}\sigma' \in D$. Thus $\sigma' = \alpha\sigma\beta$.

Conversely, if $\sigma' = \alpha\sigma\beta$ with $\alpha \in H$ and $\beta \in D$, then
$$
\Phi(\sigma') = \alpha\sigma\beta(\mathfrak{r}) \cap L = \alpha\sigma(\mathfrak{r}) \cap L = \alpha(\sigma(\mathfrak{r}) \cap L) = \sigma(\mathfrak{r}) \cap L = \Phi(\sigma),
$$
since $\alpha$ fixes $L$ pointwise and $\beta(\mathfrak{r}) = \mathfrak{r}$.

Therefore $\Phi(\sigma) = \Phi(\sigma')$ iff $\sigma' \in H\sigma D$. Hence $\Phi$ induces a bijection
$$
H \backslash G / D \xrightarrow{\sim} \{\text{primes of } L \text{ above } \mathfrak{p}\}.
$$

**(ii)** Now suppose $G \cong S_3$, and $H = D$ is an order-2 subgroup of $G$ (so $H = D$ is generated by a single transposition). Then $[L:K] = |G|/|H| = 6/2 = 3$.

If $\mathfrak{p}$ split completely in $L$, there would be exactly $3$ primes of $L$ above $\mathfrak{p}$. By part (i), this number equals $|H \backslash G / H|$.

We compute $|H \backslash G / H|$. The double cosets $HgH$ correspond to $H$-orbits on the left coset space $G/H$ under right multiplication. Since $|G/H| = 3$ and $|H| = 2$, each orbit has size 1 or 2. If $H$ acted trivially, all orbits would have size 1, giving 3 orbits; but this happens iff $H$ is normal in $G$. Since $H$ is an order-2 subgroup of $S_3$, it is not normal. Hence the action is nontrivial: one orbit has size 1 and the other has size 2, giving exactly 2 orbits. Thus $|H \backslash G / H| = 2$.

Therefore there are only 2 primes of $L$ above $\mathfrak{p}$, not 3. Hence $\mathfrak{p}$ does not split completely in $L$.
