All "$\subset$" here are actually $\subsetneq$. $\mathfrak{R}$ is used for nilradical instead of Jacobson radical.

**Ex1.21**
- (i). Firstly, 
$$
{\phi^*}^{-1}(X_{f}) = {\phi^*}^{-1}(X-V_{X}(f)) = Y - {\phi^*}^{-1}V_{X}(f)
$$
- Note that: $${\phi^*}: \mathfrak{p} \mapsto \phi^{-1}(\mathfrak{p})$$then by definition $${\phi^*}^{-1}V_{X}(f) = \{ \mathfrak{p} \in \mathrm{Spec}\,B: (f) \subset \phi^{-1}\mathfrak{p} \subset A \} = \{ \mathfrak{p} \in \mathrm{Spec}\,B : \phi(f) \subset \mathfrak{p} \subset B \} = V_{Y}(\phi(f)).$$Hence ${\phi^*}^{-1}(X_{f}) = Y_{\phi(f)}$. Continuity follows directly by definition.
- (ii). The LHS is $\{ \mathfrak{p} \in \mathrm{Spec}\,B: \mathfrak{a} \subset \phi^{-1}\mathfrak{p} \subset A \}$ and the RHS is $\{ \mathfrak{p} \in \mathrm{Spec} \,B: \mathfrak{a}^e \subset \mathfrak{p} \subset B \}.$ LHS implies RHS for the reason that inclusion is preserved by extension; Conversely, contraction also preserves inclusion, plus, note that $\mathfrak{a} \subset \mathfrak{a}^{ec}$, thus we have $\mathfrak{a} \subset \mathfrak{a}^{ec} \subset \mathfrak{p}^c = \phi^{-1}(\mathfrak{p}) \subset A$.
- (iii). The LHS is $\{\mathfrak{p} \in \mathrm{Spec}\,B : \mathfrak{b}^c \subseteq \mathfrak{p}\}$ and the RHS is $\{\mathfrak{p} \in \mathrm{Spec}\,A : \mathfrak{b} \subseteq \phi(\mathfrak{p})\}$.  LHS implies RHS because if $\mathfrak{b}^c \subseteq \mathfrak{p}$ then $\mathfrak{b} = (\mathfrak{b}^c)^e \subseteq \phi(\mathfrak{p})$. Conversely, suppose $\mathfrak{p} \in V(\mathfrak{b}^c)$. Then $\mathfrak{b}^c \subseteq \mathfrak{p}$, so $\mathfrak{b} \subseteq \mathfrak{p}^e$. But $\mathfrak{p}^e = \phi(\mathfrak{p})$, hence $\mathfrak{p} \in \phi^*(V(\mathfrak{b}))$.  
- (iv). Firstly show that $\phi^{-1}$ is surjective: Assume $\phi$ is surjective. First, $\phi^*(Y) \subseteq V(\mathrm{Ker}\,\phi)$ because $\mathrm{Ker}\,\phi = \phi^{-1}((0)) \subseteq \phi^{-1}(\mathfrak{q})$ for all $\mathfrak{q} \in Y$.  Conversely, let $\mathfrak{p} \in V(\mathrm{Ker}\,\phi)$. Since $\phi$ is surjective, $A/\mathrm{Ker}\,\phi \cong B$, there exists $\mathfrak{q} \in \mathrm{Spec}\,B$ such that $\mathfrak{p} = \phi^{-1}(\mathfrak{q})$. Thus $\phi^*(Y) = V(\mathrm{Ker}\,\phi)$, so $\phi^*$ is surjective onto $V(\mathrm{Ker}\,\phi)$.  

	Then argue the injectivity: Suppose $\phi^{-1}(\mathfrak{q}_1) = \phi^{-1}(\mathfrak{q}_2)$. For any $b \in B$, surjectivity gives $b = \phi(a)$ for some $a \in A$. Then $$b \in \mathfrak{q}_1 \iff \phi(a) \in \mathfrak{q}_1 \iff a \in \phi^{-1}(\mathfrak{q}_1) = \phi^{-1}(\mathfrak{q}_2) \iff b \in \mathfrak{q}_2$$Hence $\mathfrak{q}_1 = \mathfrak{q}_2$.  
	
	Continuity of $\phi^*$ follows from (i) and concludes with the isomorphism that it is a homeomorphism. 
	
	To show $V(\mathrm{Ker}\,\phi)$ is closed: let $V(\mathfrak{b})$ be closed in $Y$. Then $\phi^*(V(\mathfrak{b})) = V(\mathfrak{b}^c) \cap V(\mathrm{Ker}\,\phi)$ by (ii) and (iii), which is closed in the subspace $V(\mathrm{Ker}\,\phi)$. 
- (v). By (iii), $\overline{\phi^*(Y)} = \overline{\phi^*(V((0)))} = V((0)^c) = V(\mathrm{Ker}\,\phi)$. Thus $\phi^*(Y)$ is dense in $X$ iff $V(\mathrm{Ker}\,\phi) = X$ iff $\mathrm{Ker}\,\phi \subseteq \bigcap\{\text{all primes of }A\} = \mathfrak{N}$. Note that $\phi$ is injective then $\mathrm{Ker}\,\phi = (0) \subseteq \mathfrak{N}$, as required.
- (vi). Let $\mathfrak{r}$ be a prime ideal of $C$. Then $$(\psi \circ \phi)^*(\mathfrak{r}) = (\psi \circ \phi)^{-1}(\mathfrak{r}) = \phi^{-1}(\psi^{-1}(\mathfrak{r})) = \phi^*(\psi^*(\mathfrak{r})).$$- (vii). By assumption, we have $\mathrm{Spec}\,A = \{(0),\mathfrak{p}\}$. There are exactly two prime ideals of $B = (A/\mathfrak{p}) \times K$: $\mathfrak{q}_1 = (0) \times K$ and $\mathfrak{q}_2 = (A/\mathfrak{p}) \times (0)$. Indeed, these two ideals are maximal and hence prime, and a prime ideal of $B$ has to contain one of the idempotents $(1,0)$ and $(0,1)$, which force it coincide with either $\mathfrak{q}_{1}$ ro $\mathfrak{q}_{2}$. So **$\mathrm{Spec}\,B = \{\mathfrak{q}_1, \mathfrak{q}_2\}$**. Now $\phi(x) = (\overline{x}, x)$. Then
$$\phi^*(\mathfrak{q}_1) = \phi^{-1}(\mathfrak{q}_1) = \{x \in A : \overline{x} = 0\} = \mathfrak{p},$$and$$\phi^*(\mathfrak{q}_2) = \phi^{-1}(\mathfrak{q}_2) = \{x \in A : x = 0 \in K\} = (0).$$Thus $\phi^* : Y \to X$ is bijective. It is continuous by (i). However, $\{\mathfrak{q}_2\}$ is closed in $Y$ for the reason that $V(\mathfrak{q}_2) = \{\mathfrak{q}_2\}$, but its image $\{(0)\}$ is not closed in $X$ because $\overline{\{(0)\}} = V((0)) = X$. Hence $\phi^*$ is not a homeomorphism.

**Ex1.22**
Firstly show that the spectra of product is disjoint union of spectra. Since the product is finite, it suffices to show the case that $\mathrm{Spce}\,A_{1} \times A_{2}$ is homeomorphic to $\mathrm{Spec} \, A_{1} \amalg \mathrm{Spec} \,B$. The prime ideal of $A_{1} \times A_{2}$ must include either idempotent $(1,0)$ or $(0,1)$. Hence the prime ideals can only be in the form of $\mathfrak{p}_{1} \times A_{2}$ or $A_{1} \times \mathfrak{p}_{2}$. This gives a canonical homeomorphism from $\mathrm{Spec}\,A_{1} \times A_{2}$ to $\mathrm{Spec} \, A_{1} \amalg \mathrm{Spec} \,A_{2}$.

Prove the TEAE part by (iii) $\implies$ (ii) $\implies$ (i) $\implies$ (iii). For the first implication, note that an idempotent $e \neq 0,1$ give rise to the decomposition $Ae \times A(1-e)$ as discussed in class. The second implication is the previous argument. Hence it suffices to show that if $\mathrm{Spec}\,A$ is disconnected, $A$ admits an idempotent $e \neq 0,1$. Indeed, this means $\mathrm{Spec}\,A = V(\mathfrak{a}) \cup V(\mathfrak{b})$ for some $\mathfrak{a},\mathfrak{b} \neq 0$ and $V(\mathfrak{a}) \cap V(\mathfrak{b}) = \emptyset$. By exercise 15, which I suppose is done in class, $V(\mathfrak{a}) \cup V(\mathfrak{b}) = V(\mathfrak{a} \cap \mathfrak{b})$ and $V(\mathfrak{a}) \cap V(\mathfrak{b}) = V(\mathfrak{a} \cup \mathfrak{b})$. The second result implies that $\mathfrak{a} \cup \mathfrak{b} = (1)$, hence there is some $a \in \mathfrak{a},b \in \mathfrak{b}$ such that $a+b = 1$. Moreover note that $ab \in \mathfrak{a}\mathfrak{b} \subset \mathfrak{a} \cap \mathfrak{b} \subset \mathfrak{R}$. Hence, $(ab)^n = 0$. These means $a^n$ and $b^n$ are co-prime while multiply to zero. By Chinese remainder theorem, $A \cong A/(a^n) \times A/(b^n)$. The idempotent $(0,1)$ of the cross product pulls back to an idempotent in $A$ as the ring morphism is additive and multiplicative.

**Ex1.26** 


**Ex2.6**
Define $$\phi:A[x] \times M \to M[x] \quad \left( \sum a_{i}x^i,m \right) \mapsto \sum ma_{i}x^i$$The morphism is clearly bilinear, thus it factors through the tensor product by $$\varphi: A[x] \otimes M \to M[x]\quad f \otimes m \mapsto mf.$$It suffices to show the $\varphi$ is isomorphism. Indeed, for each $g \in M[x]$, it can be decomposed into $$\sum m_{i}x^i = \varphi\left( \sum x^i \otimes m_{i} \right)$$This shows that $\varphi$ is surjective. Now suppose $\varphi(x_{1}-x_{2}) = 0$, still decompose $x_{1}$ and $x_{2}$ into summands $$x_{k} = \sum_{j} \left( \sum_{i} a_{ij}x^i\right) \otimes m_{j} = \sum \sum a_{ij} x^i \otimes m_{j} = \sum_{i} \left( \sum_{j} x^i  \otimes a_{ij}m_{j} \right) = \sum_{i} x^{i} \otimes \left( \sum_{j} a_{ij} m_{j} \right).$$Mapping $x_{1}-x_{2}$ through $\varphi$, then each coefficient is $0$. Through the decomposition,  $x_{1}-x_{2}$ can be written in the form of $\sum x^{k} \otimes c_{k}$ where $c_{k}$ is exactly the coefficient of $x^k$ term in $x_{1}-x_{2}$. Hence the morphism is isomorphic.

**Ex 2.7**
Let $\mathfrak{p}$ be a prime ideal of $A$. Consider the short exact sequence of $A$-modules
$$0 \to \mathfrak{p} \to A \to A/\mathfrak{p} \to 0.$$
Since $A[x]$ is a free $A$-module (hence flat), the tensored sequence remains exact:
$$
0 \to \mathfrak{p} \otimes_A A[x] \to A[x] \to (A/\mathfrak{p}) \otimes_A A[x] \to 0.
$$
By Exercise 2.6, we have canonical isomorphisms $\mathfrak{p} \otimes_A A[x] \cong \mathfrak{p}[x]$ and $(A/\mathfrak{p}) \otimes_A A[x] \cong (A/\mathfrak{p})[x]$. Thus
$$A[x]/\mathfrak{p}[x] \cong (A/\mathfrak{p})[x].$$
Since $A/\mathfrak{p}$ is an integral domain, so is $(A/\mathfrak{p})[x]$. Therefore $p[x]$ is a prime ideal of $A[x]$. 

The maximal case does not stand, for the reason that if $\mathbb{F}$ is a field $\mathbb{F}[x]$ need not to be a field. A counter example can be realized when $A = \mathbb{Z}$ and $\mathfrak{m} = (2)$. $x$ is not invertible in $\mathbb{F}_{2}[x]$.

**Ex2.8**
- (i): Since $T \otimes (M \otimes N) = (T \otimes M) \otimes N$, both $(-\otimes M)$ and $(-\otimes N)$ exact implies that $(-\otimes (M \otimes N))$ is exact.
- (ii). Since $T \otimes_{A}(B \otimes_{B} N) = (T \otimes_{A} B) \otimes_{B}N$ and $B \otimes_{B} N \cong N$, both $(-\otimes_{A}B)$ and $(- \otimes_{B}N)$ exact implies $(- \otimes_{A}(B \otimes _{B}N)) = (-\otimes_{A}N)$ is exact.

**Ex 2.9**
See this diagram:
$$\begin{CD}
0 @>>> A^n @>>> A^{n+m} @>>> A^m@>>> 0 \\
 @. @VVV @VVV @VVV \\
0 @>>> M' @>>> M @>>> M'' @>>> 0 \\
@. @VVV @VVV @VVV  \\
 @. 0 @>>> ? @>>>0 @.
\end{CD}$$The second row is promised by assumption. The finitely-generate property gives rise to the second and fourth column, and implies that their cokernel is 0. One may construct $A^n \to A^{n+m} \to A^m$ with the natural embedding to make the first row exact and the diagram commutes. $?$ is the cokernel of the middle column, which is forced to be $0$ since the bottom row is exact as a part of the long exact sequence of snake lemma.

**Ex 2.14** There seems nothing to do.

**Ex 2.15**
I am more familiar with the description:
$$
M \cong \Bigl( \bigsqcup_{i \in I} M_i \Bigr) \Big/ \sim,
$$
where $x_i \in M_i$ is identified with $x_j \in M_j$ (written $x_i \sim x_j$) if and only if there exists $k \ge i,j$ such that $\mu_{ik}(x_i) = \mu_{jk}(x_j)$ in $M_k$. The canonical map $\mu_i$ sends $x_i$ to its equivalence class $[x_i]$.

One defines the isomorphism $\bigsqcup_i M_i / \sim \xrightarrow{\cong} C/D$ sending the class $[x_i]$ to the class of $\iota_i(x_i)$ in $C/D$; the relations enforced by $D$ are exactly those needed to make the two descriptions coincide by the universal property of quotients and the definition of colimits. Under this identification the canonical maps $\mu_i$ agree.

Since the coproduct $\bigsqcup_i M_i$ surjects onto the quotient, every element of $M$ is of the form $\mu_i(x_i)$ for some $i \in I$ and some $x_i \in M_i$. Now suppose $\mu_i(x_i) = 0$ in $M$. Then $[x_i] = [0]$ in the quotient, so $x_i \sim 0$. By definition of the equivalence relation there exists $j \ge i$ such that
$$
\mu_{ij}(x_i) = \mu_{ij}(0) = 0
$$
in $M_j$, as required. 

==In following exercises I will use the disjoint union description, with elements denoted as $[(x,i)]$ meaning the equivalence class represented by $x \in A_{i}$, where the pair here is only an index denoting where $x$ comes from, not a product.==

**Ex 2.16**
Define the map $\alpha: M \to N$ sending $[(x,i)] \mapsto \alpha_{i}(x)$, where the pair $(x,i)$ means $x \in M_{i}$. It is trivial to check that this is a module morphism. Now suppose there exists some $\beta \neq \alpha$ commuting the same diagram. Then $\beta ([x,i]) = \beta \circ \mu_{i}(x) = \alpha_{i}(x) = \alpha([x,i])$. Hence $\alpha = \beta$. 

**Ex 2.17**
We claim that the union $S := \bigcup_{i \in I} M_i \subset M$, equipped with the inclusion maps $\iota_i: M_i \hookrightarrow S$, is canonically isomorphic to $M$. Firstly, the family $(\iota_i)$ is compatible with the transitions: if $i \le j$ then $\iota_j \circ \mu_{ij} = \iota_i$. It suffices to check that it satisfies the universal property. 
Let $N$ be any $A$-module and let $\alpha_i: M_i \to N$ ($i \in I$) be a family of $A$-module homomorphisms satisfying $\alpha_j \circ \mu_{ij} = \alpha_i$ whenever $i \le j$. Define a map $\alpha: S \to N$ as follows: given $x \in S$, choose any $i$ with $x \in M_i$ and set $\alpha(x) := \alpha_i(x)$. This is well-defined: if also $x \in M_j$, then there exists $k \ge i,j$, so $x \in M_k$ and compatibility gives $\alpha_i(x) = \alpha_k(x) = \alpha_j(x)$. Moreover $\alpha$ is $A$-linear. Clearly $\alpha \circ \iota_i = \alpha_i$ for all $i$, and any map satisfying this must coincide with $\alpha$ on $S$.

It remains to show $S = \sum_{i \in I} M_i$. The inclusion $S \subset \sum M_i$ is obvious. Conversely, any element of the sum is a finite sum $x = \sum_{r=1}^t x_r$ with $x_r \in M_{i_r}$. By directedness there exists $k \ge i_1,\dots,i_t$, so $M_{i_r} \subseteq M_k$ for all $r$ and hence $x \in M_k \subseteq S$. Thus $S = \sum M_i$.

In particular, let $M$ be any $A$-module and let $I$ be the set of all finitely generated submodules of $M$, partially ordered by inclusion. For any two finitely generated submodules $M_1,M_2$ their sum $M_1 + M_2$ is again finitely generated, so $I$ satisfies the hypothesis of the exercise. It is then a direct limit.

**Ex 2.18**
Let $M = \mathrm{colim} M_i$, with canonical morphisms denoted as $\mu_i: M_i \to M$) and $N = \mathrm{colim} N_i$ with canonical morphisms denoted as $\nu_i: N_i \to N$. Consider the family of composite morphisms $\gamma_i := \nu_i \circ \phi_i : M_i \to N$ for $i \in I$. This family is compatible with the transition maps of the direct system $(M_i)$: 
$$\gamma_j \circ \mu_{ij} = \nu_j \circ \phi_j \circ \mu_{ij} = \nu_j \circ (\nu_{ij} \circ \phi_i) = (\nu_j \circ \nu_{ij}) \circ \phi_i = \nu_i \circ \phi_i = \gamma_i.$$By the universal property of the $M$, there exists a unique $A$-module homomorphism $\phi: M \to N$ such that$$\phi \circ \mu_i = \gamma_i = \nu_i \circ \phi_i \qquad \text{for all } i \in I.$$as is the desired $\mathrm{colim} \phi$.

**Ex 2.19**
Let $\phi_i : M_i \to N_i$, $\psi_i : N_i \to P_i$ be morphisms of direct systems such that for each $i$ the sequence
$$
M_i \xrightarrow{\phi_i} N_i \xrightarrow{\psi_i} P_i
$$
is exact. Let $M = \mathrm{colim} M_i$, $N = \mathrm{colim} N_i$, $P = \mathrm{colim} P_i$ be the direct limits with the induced maps $\phi : M \to N$ and $\psi : N \to P$. Clearly, $\psi \circ \phi = 0$ since $\psi_i \circ \phi_i = 0$ for every $i$ and the whole commutes.

Now let $y \in \ker \psi$. By Ex 2.15 there exist $j \in I$ and $y_j \in N_j$ such that $y = \nu_j(y_j)$, where $\nu_j : N_j \to N$. Since $\psi(y) = 0$, applying the second part of Ex 2.15 to the element $0 \in P$ yields an index $k \ge j$ such that $\pi_{jk}(\psi_j(y_j)) = 0$ in $P_k$. Equivalently, $\psi_k(\nu_{jk}(y_j)) = 0$ in $P_k$. By exactness of the sequence at level $k$, $\ker \psi_k = \mathrm{im} \phi_k$, so there exists $x_k \in M_k$ such that $\phi_k(x_k) = \nu_{jk}(y_j)$ in $N_k$. Hence,$$y = \nu_j(y_j) = \nu_k(\nu_{jk}(y_j)) = \nu_k(\phi_k(x_k)) = \phi(\mu_k(x_k)),$$Thus $y \in \mathrm{im} \phi$.

**Ex 2.20**
Let $P$ be the colimit of the system $(M_{i} \otimes N)$. Let $g_{i} : M_{i} \times N \to M_{i} \otimes N$ be the canonical morphisms, then the compositions form a group of $g_{i} \circ (\mu_{i} \otimes 1): M_{i} \times N \to P$. It factors through the colimit of the system $M_{i} \times N$ which is canonically identifies as $M \times N$. This gives a morphism $M \times N \to P$, which is bilinear as inherited from the $g_{i} \circ (\mu_{i} \otimes 1)$. It factors through $\phi : M \otimes N \to P$. On the other hand, $M \otimes N$ as the candidate of colimit of $(M_{i} \otimes N)$ factors through $\psi:P \to M \otimes N$. It suffices to show that $\phi \circ \psi = \mathrm{id}, \psi \circ \phi = \mathrm{id}$. Indeed, let $\rho : M \times N \to M \otimes N$, then $$\rho \circ (\mu_{i} \times 1) = (\mu_{i} \otimes 1) \circ g_{i}.$$Hence, $$\psi \circ v_{i} \circ g_{i} = \psi \circ \phi \circ \psi \circ v_{i} \circ g_{i}$$where $v_{i}: M_{i} \otimes N \to P$. Therefore $\psi \circ \phi = \mathrm{id}$. Similarly, $$\phi \circ \rho \circ (\mu_{i} \otimes 1) \circ g_{i} = \phi \circ \psi \circ v_{i} \circ g_{i} = \phi \circ \psi \circ \phi \circ \rho \circ (\mu_{i} \times 1) = \phi \circ \psi \circ \phi \circ (\mu_{i} \otimes 1) \circ g_{i}.$$Therefore, $\phi \circ \psi = \mathrm{id}$.

**Ex 2.21**
$\mathbb{Z}$-mod has promised the abelian group structure. By the disjoint union description, $1$ exists in $A$ as the equivalence class of any $1_{A_{i}}$. Now take any two elements $[(x,i)]$ and $[(y,j)]$ from $A$, there is some $k \geq i,j$ such that $\mu_{ik}(x) = z, \mu_{jk}(y) = w$. Define $[(x,i)][(y,j)]$ as $[(zw,k)]$. It is well-defined as for any $k' \geq i,j$, there exists some $l \geq k,k'$ and $$\mu_{kl} \circ \mu_{ik} = \mu_{il} = \mu_{k'l} \circ \mu_{ik'} ,\quad \mu_{kl} \circ \mu_{jk} = \mu_{jl} = \mu_{k'l} \circ \mu_{jk'}.$$Hence $[(zw,k)] = [(z'w',k')]$. It is clear that this multiplication is commutative. Define the addition in the same way and clearly it associates with multiplication. These operations are compatible with the $\mathbb{Z}$-mod structure for the reason that $a \in \mathbb{Z}$ can be embedded in any $A_{i}$, and thus multiplication by $s$ can be directly pass into the bracket without altering index $i$.

Now suppose $A = 0$, then $0 = 1$ in $A$. As non-trival ring morphisms send $1$ to $1$, the class $[(1,i)]$ can not be identified with any $[(0,j)]$ if none of $A_{i}$ is $0$, a contradiction.

**Ex 2.22**
Set for each $i$ a exact sequence $$0 \to \mathfrak{R}_{i} \to A_{i} \to A_{i} / \mathfrak{R}_{i} \colon = B_{i} \to 0.$$The $(B_{i})$ forms a directed systems with the morphisms inherited from $A_{i} \to A_{j}$. By Ex 2.19, the induced colimit sequence is also exact: $$0 \to \mathrm{colim}\mathfrak{R}_{i} \to \mathrm{colim}A_{i} \to \mathrm{colim} B_{i} \to 0.$$Now it suffices to check that $\mathrm{colim}B_{i}$ has no non-zero nilpotent. Suppose for contradiction that there exists some non-trivial $[(x,i)]^n = 0$ in it, then $[(x^n,i)] = 0$ with non-trivial $x$. This means either $x^n$ is mapped to some $0 \in B_{j}$ or $x^n = 0$ in $B_{i}$. The latter case is impossible as $B_{i}$ do not have non-trivial nilpotent. The former one implies that $\mu_{ij}(y) \in \mathfrak{R}_{j}$ for a representing element $y \in A_{i}$ of $x^n \in B_{i}$ with $y \not\in \mathfrak{R}_{i}$. It forces $\mu_{ij}(y) = 0$ and thus $\mu_{i}(y) = 0$ as $\mu_{j} \circ \mu_{ij} = \mu_{i}$, but this means that $[(x,i)]$ is trivial, a contradiction.

To show filtered colimit preserves integral domain, suppose for contradiction that non-trivial $[(x,i)][(y,j)] = 0$ in colimit, then $\mu_{ik}(x)\mu_{jk}(x) = 0 \in A_{k}$ for some $k$. This forces either $\mu_{ik}(x)$ or $\mu_{jk}(x)$ to be $0$, hence either $[(x,i)]$ or $[(y,j)]$ is identified with 0, a contradiction. 

**Ex 2.23** There seems nothing to do.

**Problem 2(a) - Ex 2.15**
Define the map$$\phi:(M\otimes_A N)\times P\to M\otimes_A(N\otimes_B P),\qquad \phi(m\otimes_A n,p)=m\otimes_A(n\otimes_B p).$$This map is $B$-bilinear: it is clearly $\mathbb{Z}$-bilinear, and$$\phi((m\otimes_A n)\cdot b,p)=m\otimes_A((nb)\otimes_B p)=m\otimes_A(n\otimes_B(bp))=\phi(m\otimes_A n,b\cdot p).$$By the universal property of $\otimes_B$, $\phi$ induces a group homomorphism$$\psi:(M\otimes_A N)\otimes_B P\to M\otimes_A(N\otimes_B P)$$satisfying$$\psi\bigl((m\otimes_A n)\otimes_B p\bigr)=m\otimes_A(n\otimes_B p).$$Conversely, let $Z=N\otimes_B P$ (now an $A$-module). Define the map$$\gamma:M\times Z\to(M\otimes_A N)\otimes_B P,\qquad\gamma(m,n\otimes_B p)=(m\otimes_A n)\otimes_B p.$$This map is $A$-bilinear: it is clearly $\mathbb{Z}$-bilinear, and$$\gamma(am,n\otimes_B p)=((am)\otimes_A n)\otimes_B p=(m\otimes_A(an))\otimes_B p=\gamma(m,a\cdot(n\otimes_B p)).$$By the universal property of $\otimes_A$, $\gamma$ induces a group homomorphism$$\theta:M\otimes_A(N\otimes_B P)\to(M\otimes_A N)\otimes_B P$$satisfying$$\theta\bigl(m\otimes_A(n\otimes_B p)\bigr)=(m\otimes_A n)\otimes_B p.$$On generators we have$$\psi\bigl((m\otimes_A n)\otimes_B p\bigr)=m\otimes_A(n\otimes_B p),\quad\theta\bigl(m\otimes_A(n\otimes_B p)\bigr)=(m\otimes_A n)\otimes_B p.$$Thus $\theta\circ\psi=\mathrm{id}$ and $\psi\circ\theta=\mathrm{id}$, so $\psi$ is the desired isomorphism.


**Problem 2(b)**
Let $M$, $N$, $P$ be $A$-modules. We construct mutually inverse $A$-module homomorphisms$$\Phi:\mathrm{Hom}_A(M\otimes_A N,P)\to\mathrm{Hom}_A\bigl(M,\mathrm{Hom}_A(N,P)\bigr)$$and$$\Psi:\mathrm{Hom}_A\bigl(M,\mathrm{Hom}_A(N,P)\bigr)\to\mathrm{Hom}_A(M\otimes_A N,P).$$Given $f\in\mathrm{Hom}_A(M\otimes_A N,P)$, define $\Phi(f):M\to\mathrm{Hom}_A(N,P)$ by$$\bigl(\Phi(f)(m)\bigr)(n):=f(m\otimes_A n)\qquad\text{for all }m\in M,\,n\in N.$$For fixed $m$, the map $n\mapsto f(m\otimes_A n)$ is $A$-linear because $f$ is $A$-linear and the map $n\mapsto m\otimes_A n$ is $A$-linear. Moreover, $\Phi(f)$ itself is $A$-linear in $m$ because $f$ is linear in the first factor of the tensor product. This shows that the construction is well-defined.

Conversely, given $g\in\mathrm{Hom}_A\bigl(M,\mathrm{Hom}_A(N,P)\bigr)$, consider the map$$M\times N\to P,\qquad(m,n)\mapsto g(m)(n).$$This map is $A$-bilinear: For fixed $m$, the map $n\mapsto g(m)(n)$ is $A$-linear by definition of $g(m)$; For fixed $n$, the map $m\mapsto g(m)(n)$ is $A$-linear because $g$ is $A$-linear and evaluation at $n$ is $A$-linear.
By the universal property of the tensor product, there exists a unique $A$-module homomorphism $\Psi(g):M\otimes_A N\to P$ satisfying$$\Psi(g)(m\otimes_A n)=g(m)(n)$$for all $m\in M$, $n\in N$.

It remains to check that $\Phi$ and $\Psi$ are inverse to each other. On generators we have$$\Psi\bigl(\Phi(f)\bigr)(m\otimes_A n)=\bigl(\Phi(f)(m)\bigr)(n)=f(m\otimes_A n),$$so $\Psi\circ\Phi=\mathrm{id}$ (since both sides agree on generators of $M\otimes_A N$). Similarly,$$\bigl(\Phi\bigl(\Psi(g)\bigr)\bigr)(m)(n)=\Psi(g)(m\otimes_A n)=g(m)(n),$$so $\Phi\circ\Psi=\mathrm{id}$. Hence either morphism is the desired isomorphism of abelian groups.

**Problem 2(c)**
(ii) $\implies$ (iii) is immediate.
(i) $\implies$ (ii): Assume $M$ is flat. Let $N$ be any $A$-module and take a free resolution$$\cdots\to F_2\to F_1\to F_0\to N\to 0$$of $N$. Since $M$ is flat, $(-\otimes_A M)$ is exact, then this sequence is exact:$$\cdots\to M\otimes_A F_2\to M\otimes_A F_1\to M\otimes_A F_0\to M\otimes_A N\to 0$$Therefore its homology groups $\mathrm{Tor}_n^A(M,N)$ vanish for all $n>0$.

(iii) $\implies$ (i): Let$$0\to N'\xrightarrow{i} N\xrightarrow{p} N''\to 0$$be any short exact sequence of $A$-modules. The long exact sequence in Tor gives the exact sequence$$\mathrm{Tor}_1^A(M,N'')\to M\otimes_A N'\to M\otimes_A N\to M\otimes_A N''\to 0.$$By (iii), $\mathrm{Tor}_1^A(M,N'')=0$, so$$0\to M\otimes_A N'\to M\otimes_A N\to M\otimes_A N''\to 0$$is exact. Since this holds for every short exact sequence, $M$ is flat by definition.


**Problem 2(d)**
**Application 1:** Let $R$ be an integral domain that is not a field, with fraction field $F$. Then $F$ is not finitely generated as an $R$-module.  

*Proof.* Assume for contradiction that $F$ is finitely generated as an $R$-module. Since $R$ is not a field, it has at least one nonzero proper ideal. By Zorn’s lemma (as is proved in class) there exists a maximal ideal $\mathfrak{m}$ of $R$. Let $S=R\setminus\mathfrak{m}$ and consider the localization $R_{\mathfrak{m}}=S^{-1}R$. This is a local ring whose only maximal ideal, hence also Jacobson radical, is $\mathfrak{m}R_{\mathfrak{m}}$.

Since $F$ is already the localization of $R$ at the multiplicative set $R\setminus\{0\}$ and $S\subset R\setminus\{0\}$, inverting the elements of $S$ does not enlarge the field. Thus $F\cong F\otimes_R R_{\mathfrak{m}}$ as $R_{\mathfrak{m}}$-modules. Moreover, finite generation is preserved under localization,  $F$ is finitely generated as $R_{\mathfrak{m}}$-module. Note that $\mathfrak{m}R_{\mathfrak{m}}\cdot F=F$. Indeed: $F$ is a field, so every nonzero element of $F$ is invertible in $F$; multiplication by any nonzero element of $\mathfrak{m}R_{\mathfrak{m}}$ followed by multiplication of the appropriate inverse recovers the field. By Nakayama’s lemma we conclude that $F=0$, a contradiction.

**Application 2:** Let $(A,\mathfrak{m})$ be a local ring and let $M$ be a finitely generated $A$-module. Suppose $f_1,\dots,f_n\in M$ are elements whose images in $M/\mathfrak{m}M$ generate $M/\mathfrak{m}M$ as an $A/\mathfrak{m}$-vector space. We claim that $f_1,\dots,f_n$ generate $M$ as an $A$-module. In particular, taking $M=\mathfrak{m}$, any set of elements whose images generate $\mathfrak{m}/\mathfrak{m}^2$ also generates $\mathfrak{m}$.

*Proof.* Let $(A,\mathfrak{m})$ be a local ring. Note that the Jacobson radical of $A$ is $\mathfrak{m}$. Suppose $M$ is a finitely generated $A$-module and $f_1,\dots,f_n\in M$ are elements whose images $\overline{f_1},\dots,\overline{f_n}$ generate $M/\mathfrak{m}M$ as an $A/\mathfrak{m}$-vector space. Let $N=\sum_{i=1}^n A f_i\subseteq M$ be the submodule generated by the $f_i$. By assumption, $M=N+\mathfrak{m}M$. Hence $M/N=\mathfrak{m}(M/N)$. Since $M$ is finitely generated, the quotient $M/N$ is also finitely generated. Apply Nakayama’s lemma)to the finitely generated $A$-module $M/N$ and the ideal $\mathfrak{m}$, which is contained in the Jacobson radical of $A$. We have $\mathfrak{m}(M/N)=M/N$ implies $M/N=0$. Hence $M=N$, i.e., the elements $f_1,\dots,f_n$ generate $M$.

**Counterexamples when the finitely generated assumption is dropped**
Let $A=\mathbb{Z}$, $I=(2)$, and $M=\mathbb{Q}$ (as a $\mathbb{Z}$-module). Then  
$$
IM=2\mathbb{Q}=\mathbb{Q}=M,
$$  
but there is no $r\in\mathbb{Z}$ with $r\equiv 1\pmod{(2)}$ such that $rM=0$ since multiplication by any nonzero integer is injective on $\mathbb{Q}$. Thus the conclusion "$M=0$"fails.

**Problem 2(e)**
Let $\phi: M\to M$ be the $R$-linear endomorphism that is surjective. View $M$ as an $R[X]$-module by letting the indeterminate $X$ act via $\phi$, i.e., $X\cdot m=\phi(m)$ for all $m\in M$. Since $M$ is finitely generated as an $R$-module, it remains finitely generated as an $R[X]$-module. The surjectivity of $\phi$ means that $M=\phi(M)=XM=(X)M$. Let $e_1,\dots,e_r$ be a generating set of $M$ over $R$. Since each $e_i\in XM$, there exist $a_{ij}\in(X)\subset R[X]$ such that $$ e_i=\sum_{j=1}^r a_{ij}e_j\qquad(i=1,\dots,r).$$In matrix form, let $\mathbf{e}$ denotes the column vector with entries $e_i$. Then $(I_r-A)\mathbf{e}=0$. Let $\Delta(X)=\det(I_r-A)\in R[X]$. Then there exists a matrix $B(X)$ with entries in $R[X]$ such that $$ B(X)(I_r-A)=\Delta(X)I_r. $$Applying both sides to $\mathbf{e}$ yields $\Delta(X)\mathbf{e}=0$. Since the $e_i$ generate $M$ as an $R[X]$-module, it follows that $\Delta(X)\cdot M=0$ i.e., $\Delta(\phi)=0$ as an endomorphism of $M$.

Expanding the determinant, the constant term of $\Delta(X)$ is $\det(I_r)=1$, while every other term in the expansion contains at least one factor from the matrix $A$ and is therefore divisible by $X$. Thus $$ \Delta(X)\equiv1\pmod{(X)}, $$ so we may write $$ \Delta(X)=1-Xp(X) $$ for some polynomial $p(X)\in R[X]$. The relation $\Delta(\phi)=0$ now equals $$ \mathrm{id}_M=\phi\circ p(\phi). $$Suppose now $\phi(m)=0$ for some $m\in M$. Then $\phi^k(m)=0$ for all $k\geq1$. Write $p(X)=\sum_{k=0}^d c_kX^k$. Then $$ p(\phi)(m)=c_0m+\sum_{k=1}^d c_k\phi^k(m)=c_0m. $$ Applying $\phi$ to both sides, with $\mathrm{id}_M=\phi\circ p(\phi)$ gives $$ m=\phi\bigl(p(\phi)(m)\bigr)=\phi(c_0m)=c_0\cdot\phi(m)=0. $$ Hence $\ker\phi=0$, so $\phi$ is an isomorphism.
x`
**Counterexample:**
Let $R$ be any nonzero commutative ring. Let $$ M=\prod_{n=1}^\infty R $$be the $R$-module of all sequences $(a_1,a_2,a_3,\dots)$ with $a_n\in R$. Define the $R$-linear endomorphism $$ \phi:M\to M,\quad\phi(a_1,a_2,a_3,\dots)=(a_2,a_3,a_4,\dots) $$It is surjective but not injective.

