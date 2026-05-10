___

> [!problem] [ATI] 1.21
> Let $\phi: A \to B$ be a ring homomorphism. Let $X = \operatorname{Spec}(A)$ and $Y = \operatorname{Spec}(B)$. If $q \in Y$, then $\phi^{-1}(q)$ is a prime ideal of $A$, i.e., a point of $X$. Hence $\phi$ induces a mapping $\phi^{*}: Y \to X$. Show that
>
> i) If $f \in A$ then $\phi^{*-1}(X_{f}) = Y_{\phi(f)}$, and hence that $\phi^{*}$ is continuous.
>
> ii) If $\alpha$ is an ideal of $A$, then $\phi^{*-1}(V(\alpha)) = V(\alpha^{e})$.
>
> iii) If $b$ is an ideal of $B$, then $\overline{\phi^{*}(V(b))} = V(b^{c})$.
>
> iv) If $\phi$ is surjective, then $\phi^{*}$ is a homeomorphism of $Y$ onto the closed subset $V(\operatorname{Ker} \phi)$ of $X$. (In particular, $\operatorname{Spec}(A)$ and $\operatorname{Spec}(A/\mathfrak{R})$ (where $\mathfrak{R}$ is the nilradical of $A$) are naturally homeomorphic.)
>
> v) If $\phi$ is injective, then $\phi^{*}(Y)$ is dense in $X$. More precisely, $\phi^{*}(Y)$ is dense in $X \Leftrightarrow \operatorname{Ker}(\phi) \subseteq \mathfrak{R}$.
>
> vi) Let $\psi: B \to C$ be another ring homomorphism. Then $(\psi \circ \phi)^{*} = \phi^{*} \circ \psi^{*}$.
>
> vii) Let $A$ be an integral domain with just one non-zero prime ideal $\mathfrak{p}$, and let $K$ be the field of fractions of $A$. Let $B = (A/\mathfrak{p}) \times K$. Define $\phi: A \to B$ by $\phi(x) = (\bar{x}, x)$, where $\bar{x}$ is the image of $x$ in $A/\mathfrak{p}$. Show that $\phi^{*}$ is bijective but not a homeomorphism.

**Proof:**
**i)** $\mathfrak{q} \in \phi^{*-1}(X_{f}) \iff \phi^{*}(\mathfrak{q}) \in X_{f} \iff f \notin \phi^{-1}(\mathfrak{q}) \iff \phi(f) \notin \mathfrak{q} \iff \mathfrak{q} \in Y_{\phi(f)}$.
Therefore $\phi^{*-1}(X_{f}) = Y_{\phi(f)}$. Since the sets $X_{f}$ form a basis for the Zariski topology on $X$, the preimage of a basic open set is open. Hence $\phi^{*}$ is continuous.

**ii)** $\alpha^{e}$ is the extension ideal $\langle \phi(\alpha) \rangle$ in $B$.
$\mathfrak{q} \in \phi^{*-1}(V(\alpha)) \iff \phi^{*}(\mathfrak{q}) \in V(\alpha) \iff \alpha \subseteq \phi^{-1}(\mathfrak{q}) \iff \phi(\alpha) \subseteq \mathfrak{q} \iff \alpha^{e} \subseteq \mathfrak{q} \iff \mathfrak{q} \in V(\alpha^{e})$.

**iii)** $b^{c} = \phi^{-1}(b)$ is the contraction ideal in $A$.
The closure of $\phi^{*}(V(b))$ is the intersection of all closed sets containing it. The smallest closed set containing a set $S \subseteq \operatorname{Spec}(A)$ is $V(I(S))$, where $I(S) = \bigcap_{\mathfrak{p} \in S} \mathfrak{p}$.
For $S = \phi^{*}(V(b))$, we have
$I(S) = \bigcap_{\mathfrak{q} \in V(b)} \phi^{-1}(\mathfrak{q}) = \phi^{-1}(\bigcap_{\mathfrak{q} \in V(b)} \mathfrak{q}) = \phi^{-1}(\sqrt{b}) = \sqrt{b^{c}}$.
Since $V(\sqrt{b^{c}}) = V(b^{c})$, we get $\overline{\phi^{*}(V(b))} = V(b^{c})$.

**iv)** By the First Isomorphism Theorem, $B \cong A / \operatorname{Ker} \phi$. The prime ideals of $A / \operatorname{Ker} \phi$ correspond bijectively to prime ideals of $A$ containing $\operatorname{Ker} \phi$, i.e., to $V(\operatorname{Ker} \phi) \subseteq X$. Thus $\phi^{*}: Y \to V(\operatorname{Ker} \phi)$ is a bijection.
It is continuous by (i). Its inverse, induced by the isomorphism $A / \operatorname{Ker} \phi \to B$, is also continuous (since the preimage of a basic open set in $Y$ is a basic open set in $V(\operatorname{Ker} \phi)$). Hence $\phi^{*}$ is a homeomorphism.

**v)** $\phi^{*}(Y)$ is dense in $X$ iff $\overline{\phi^{*}(Y)} = X$ iff $V(\operatorname{Ker}(\phi)) = X$ (by (iii) with $b = (0)$).
$V(\operatorname{Ker}(\phi)) = X$ iff every prime ideal of $A$ contains $\operatorname{Ker}(\phi)$, which is equivalent to $\operatorname{Ker}(\phi) \subseteq \mathfrak{R}$, the nilradical of $A$.
If $\phi$ is injective, $\operatorname{Ker}(\phi) = (0) \subseteq \mathfrak{R}$, so density holds.

**vi)** For $\mathfrak{r} \in \operatorname{Spec}(C)$, we have $(\psi \circ \phi)^{*}(\mathfrak{r}) = (\psi \circ \phi)^{-1}(\mathfrak{r}) = \phi^{-1}(\psi^{-1}(\mathfrak{r})) = \phi^{*}(\psi^{*}(\mathfrak{r})) = (\phi^{*} \circ \psi^{*})(\mathfrak{r})$.

**vii)** $B$ has exactly two prime ideals: $\mathfrak{q}_{1} = (A/\mathfrak{p}) \times (0)$ and $\mathfrak{q}_{2} = (0) \times K$.
$$
\phi^{*}(\mathfrak{q}_{1}) = \phi^{-1}((A/\mathfrak{p}) \times (0)) = \mathfrak{p},
\phi^{*}(\mathfrak{q}_{2}) = \phi^{-1}((0) \times K) = (0).
$$
So $\phi^{*}$ maps the two points of $\operatorname{Spec}(B)$ to the two points $\mathfrak{p}$ and $(0)$ of $\operatorname{Spec}(A)$. It is therefore bijective as a set map.

However, in $\operatorname{Spec}(A)$, the point $(0)$ is dense (since it is the generic point of an integral domain), while in $\operatorname{Spec}(B)$, both points are closed (since $B$ is a product of two fields, its spectrum is discrete). Therefore, $\phi^{*}$ sends a closed point $\mathfrak{q}_{2}$ to a non-closed point $(0)$. Since the image of a closed set is not necessarily closed, $\phi^{*}$ is not a homeomorphism.
___

>[!problem] [ATI] 1.22
>Let $A = \prod_{i=1}^{n} A_{i}$ be the direct product of rings $A_{i}$. Show that $\operatorname{Spec}(A)$ is the disjoint union of open (and closed) subspaces $X_{i}$, where $X_{i}$ is canonically homeomorphic with $\operatorname{Spec}(A_{i})$.
>
>Conversely, let $A$ be any ring. Show that the following statements are equivalent:
>i) $X = \operatorname{Spec}(A)$ is disconnected.
>ii) $A \cong A_{1} \times A_{2}$ where neither of the rings $A_{1}, A_{2}$ is the zero ring.
>iii) $A$ contains an idempotent $\neq 0, 1$.
>In particular, the spectrum of a local ring is always connected.

**Proof:**
Consider the projection maps $\pi_i: A \rightarrow A_i$. Then the map $i \mapsto \mathfrak{p} \leftrightarrow \pi_i^{-1}(\mathfrak{p})$ gives a bijection between $\operatorname{Spec}(A_i)$ and the set of prime ideals of $A$ containing $I_i = \operatorname{Ker}(\pi_i)$. The $I_i$ are mutually orthogonal idempotent ideals ($I_i I_j = 0$ for $i \neq j$ and $I_i^2 = I_i$) and $\sum_{i=1}^n I_i = A$. Hence, $\operatorname{Spec}(A)$ is the disjoint union of the closed (and open) sets $V(I_i)^c = D(I_i)$, each homeomorphic to $\operatorname{Spec}(A_i)$ via the map induced by $\pi_i$.
___
**i) $\Rightarrow$ ii):** If $\operatorname{Spec}(A) = U_1 \cup U_2$ is a disconnection, then $U_i = D(e_i)$ for some idempotents $e_1, e_2$ with $e_1 + e_2 = 1$ and $e_1 e_2 = 0$. The map $A \rightarrow A/(e_1) \times A/(e_2)$ is an isomorphism. Since $U_i$ are non-empty, $(e_i) \neq (1)$, so $A/(e_i)$ are non-zero rings.

**ii) $\Rightarrow$ iii):** Let $\psi: A \rightarrow A_1 \times A_2$ be an isomorphism. Let $e = \psi^{-1}(1,0)$. Then $e$ is a non-trivial idempotent ($e^2 = e$, $e \neq 0,1$).

**iii) $\Rightarrow$ i):** If $e \in A$ is an idempotent with $e \neq 0,1$, then $\operatorname{Spec}(A) = D(e) \cup D(1-e)$ is a disconnection, as $D(e) \cap D(1-e) = D(e(1-e)) = D(0) = \varnothing$ and both are non-empty (since $e$ and $1-e$ are not units).
___

> [!problem] [ATI] 1.26
> Let $A$ be a ring. The subspace of $\operatorname{Spec}(A)$ consisting of the maximal ideals of $A$, with the induced topology, is called the maximal spectrum of $A$ and is denoted by $\operatorname{Max}(A)$. For arbitrary commutative rings it does not have the nice functorial properties of $\operatorname{Spec}(A)$ (see Exercise 21), because the inverse image of a maximal ideal under a ring homomorphism need not be maximal.
>
> Let $X$ be a compact Hausdorff space and let $C(X)$ denote the ring of all real-valued continuous functions on $X$ (add and multiply functions by adding and multiplying their values).
>
> For each $x \in X$, let $\mathfrak{m}_{x}$ be the set of all $f \in C(X)$ such that $f(x) = 0$. The ideal $\mathfrak{m}_{x}$ is maximal, because it is the kernel of the (surjective) homomorphism $C(X) \to \mathbb{R}$ which takes $f$ to $f(x)$.
>
> If $\tilde{X}$ denotes $\operatorname{Max}(C(X))$, we have therefore defined a mapping $\mu: X \to \tilde{X}$, namely $x \mapsto \mathfrak{m}_{x}$. We shall show that $\mu$ is a homeomorphism of $X$ onto $\tilde{X}$.
>
> i) Let $\mathfrak{m}$ be any maximal ideal of $C(X)$, and let $V = V(\mathfrak{m})$ be the set of common zeros of the functions in $\mathfrak{m}$: that is, $V = \{x \in X: f(x) = 0$ for all $f \in \mathfrak{m}\}$. Suppose that $V$ is empty. Then for each $x \in X$ there exists $f_{x} \in \mathfrak{m}$ such that $f_{x}(x) \neq 0$. Since $f_{x}$ is continuous, there is an open neighborhood $U_{x}$ of $x$ in $X$ on which $f_{x}$ does not vanish. The family $\left(U_{x}\right)_{x \in X}$ covers $X$ and since $X$ is compact, a finite number of the $U_{x}$, say $U_{x_{1}}, \ldots, U_{x_{n}}$, cover $X$. Let $f = f_{x_{1}}^{2} + \cdots + f_{x_{n}}^{2}$. Then $f \in \mathfrak{m}$ and $f$ does not vanish at any point of $X$, hence is a unit in $C(X)$. This contradicts the assumption that $\mathfrak{m} \neq C(X)$. Hence $V$ is not empty. Let $x$ be a point of $V$. Then $\mathfrak{m} \subseteq \mathfrak{m}_{x}$, hence $\mathfrak{m} = \mathfrak{m}_{x}$ because $\mathfrak{m}$ is maximal. Hence $\mu$ is surjective.
>
> ii) Urysohn’s lemma (for a compact Hausdorff space) asserts that, if $x$, $y$ are distinct points of $X$, there exists $f \in C(X)$ such that $f(x) = 0$, $f(y) = 1$. Hence $\mathfrak{m}_{x} \neq \mathfrak{m}_{y}$, and therefore $\mu$ is injective.
>
> iii) Let $f \in C(X)$; let $U_{f} = \{x \in X: f(x) \neq 0\}$ and let $\tilde{U}_{f} = \{\mathfrak{m} \in \tilde{X}: f \notin \mathfrak{m}\}$. Show that $\mu\left(U_{f}\right) = \tilde{U}_{f}$.
>
> The open sets $U_{f}$ (resp. $\tilde{U}_{f}$) form a basis of the topology of $X$ (resp. $\tilde{X}$) and therefore $\mu$ is a homeomorphism.
>
> Thus $X$ can be reconstructed from the ring of functions $C(X)$.

**Proof:**
**i)** Given a maximal ideal $\mathfrak{m} \subset C(X)$, let $V = \{ x \in X : f(x) = 0 \text{ for all } f \in \mathfrak{m} \}$.

Suppose $V = \varnothing$. Then for each $x \in X$, there exists $f_x \in \mathfrak{m}$ with $f_x(x) \neq 0$. Since $f_x$ is continuous, there exists an open neighborhood $U_x$ of $x$ where $f_x$ does not vanish.
The collection $\{U_x\}_{x \in X}$ is an open cover of $X$. By compactness, a finite subcover $\{U_{x_1}, \dots, U_{x_n}\}$ exists.

Let $f = f_{x_1}^2 + \dots + f_{x_n}^2 \in \mathfrak{m}$. Then $f(x) > 0$ for all $x \in X$, so $f$ is a unit in $C(X)$. This contradicts the fact that $\mathfrak{m}$ is a proper ideal ($\mathfrak{m} \neq C(X)$). Hence $V \neq \varnothing$.

Take $x \in V$. By definition, $f(x) = 0$ for all $f \in \mathfrak{m}$, so $\mathfrak{m} \subseteq \mathfrak{m}_x$. Since both are maximal ideals, $\mathfrak{m} = \mathfrak{m}_x = \mu(x)$.

Therefore, every maximal ideal $\mathfrak{m}$ is of the form $\mathfrak{m}_x$, so $\mu$ is surjective.

**ii)** Let $x, y \in X$, $x \neq y$. By Urysohn’s Lemma (for compact Hausdorff spaces), there exists $f \in C(X)$ such that $f(x) = 0$ and $f(y) = 1$. Then $f \in \mathfrak{m}_x$ but $f \notin \mathfrak{m}_y$, so $\mathfrak{m}_x \neq \mathfrak{m}_y$. Hence $\mu(x) \neq \mu(y)$, so $\mu$ is injective.

**iii)** We have
$$
x \in U_f \iff f(x) \neq 0 \iff f \notin \mathfrak{m}_x \iff \mathfrak{m}_x = \mu(x) \in \tilde{U}_f,
$$
so $\mu(U_f) = \tilde{U}_f$.

The collection $\{U_f\}_{f \in C(X)}$ forms a basis for the topology of $X$ (as a compact Hausdorff space, the co‑zero sets $U_f$ are a basis). Likewise, $\{\tilde{U}_f\}_{f \in C(X)}$ forms a basis for the Zariski topology on $\tilde{X} = \operatorname{Max}(C(X))$. Since $\mu$ is a bijection that maps a basic open set $U_f$ to the basic open set $\tilde{U}_f$, it is a homeomorphism.

Thus $X$ is homeomorphic to its maximal spectrum $\operatorname{Max}(C(X))$, and the space $X$ can be reconstructed from the ring of continuous functions $C(X)$.
___

> [!problem] [ATI] 1.27
> Let $k$ be an algebraically closed field and let
> $$f_{\alpha}(t_{1}, \ldots, t_{n}) = 0$$
> be a set of polynomial equations in $n$ variables with coefficients in $k$. The set $X$
> of all points $x = (x_{1}, \ldots, x_{n}) \in k^{n}$ which satisfy these equations is an *affine
> algebraic variety*.
>
> Consider the set of all polynomials $g \in k[t_{1}, \ldots, t_{n}]$ with the property that
> $g(x) = 0$ for all $x \in X$. This set is an ideal $I(X)$ in the polynomial ring, and is
> called the *ideal of the variety* $X$. The quotient ring
> $$P(X) = k[t_{1}, \ldots, t_{n}] / I(X)$$
> is the ring of polynomial functions on $X$, because two polynomials $g, h$ define the
> same polynomial function on $X$ if and only if $g - h$ vanishes at every point of $X$,
> that is, if and only if $g - h \in I(X)$.
>
> Let $\xi_{i}$ be the image of $t_{i}$ in $P(X)$. The $\xi_{i}$ ($1 \leqslant i \leqslant n$) are the *coordinate
> functions* on $X$: if $x \in X$, then $\xi_{i}(x)$ is the $i$th coordinate of $x$. $P(X)$ is generated
> as a $k$-algebra by the coordinate functions, and is called the *coordinate ring* (or
> affine algebra) of $X$.
>
> As in Exercise 26, for each $x \in X$ let $\mathfrak{m}_{x}$ be the ideal of all $f \in P(X)$ such that
> $f(x) = 0$; it is a maximal ideal of $P(X)$. Hence, if $\bar{X} = \operatorname{Max}(P(X))$, we
> have defined a mapping $\mu: X \rightarrow \bar{X}$, namely $x \mapsto \mathfrak{m}_{x}$.
>
> It is easy to show that $\mu$ is injective: if $x \neq y$, we must have $x_{i} \neq y_{i}$ 
> for some $i$ ($1 \leqslant i \leqslant n$), and hence $\xi_{i} - x_{i}$ is in $\mathfrak{m}_{x}$ but not in $\mathfrak{m}_{y}$, so that
> $\mathfrak{m}_{x} \neq \mathfrak{m}_{y}$. What is less obvious (but still true) is that $\mu$ is *surjective*. This is one form of Hilbert's Nullstellensatz (see Chapter 7).

Nothing to prove.
___

> [!problem] [ATI] 1.28
> Let $f_{1}, \ldots, f_{m}$ be elements of $k[t_{1}, \ldots, t_{n}]$. They determine a polynomial mapping $\phi: k^{n} \to k^{m}$: if $x \in k^{n}$, the coordinates of $\phi(x)$ are $f_{1}(x), \ldots, f_{m}(x)$.
>
> Let $X, Y$ be affine algebraic varieties in $k^{n}, k^{m}$ respectively. A mapping $\phi: X \to Y$ is said to be regular if $\phi$ is the restriction to $X$ of a polynomial mapping from $k^{n}$ to $k^{m}$.
>
> If $\eta$ is a polynomial function on $Y$, then $\eta \circ \phi$ is a polynomial function on $X$. Hence $\phi$ induces a $k$-algebra homomorphism $P(Y) \to P(X)$, namely $\eta \mapsto \eta \circ \phi$.
>
> Show that in this way we obtain a one-to-one correspondence between the regular mappings $X \to Y$ and the $k$-algebra homomorphisms $P(Y) \to P(X)$.

**Proof:**
Let $\phi: X \to Y$ be a regular map. By definition, $\phi$ is the restriction to $X$ of a polynomial map
$$
\tilde{\phi} = (f_1, \dots, f_m): k^n \to k^m,
$$
where $f_j \in k[t_1,\dots,t_n]$.

Given $\eta \in P(Y) = k[u_1,\dots,u_m]/I(Y)$ represented by $g(u_1,\dots,u_m)$,
define
$$
\psi(\eta) = \eta \circ \phi \in P(X).
$$
Concretely, $\psi(\eta)$ is the class of $g(f_1,\dots,f_m)$ in $P(X)=k[t_1,\dots,t_n]/I(X)$.

If $g, h$ represent the same $\eta$, then $g-h \in I(Y)$. Because $\phi(X) \subseteq Y$, we have $(g-h)(f_1,\dots,f_m) \in I(X)$, so $\psi(\eta)$ is well-defined. Clearly $\psi$ is a $k$-algebra homomorphism.


Let $\psi: P(Y) \to P(X)$ be a $k$-algebra homomorphism. Let $\eta_j$ be the $j$‑th coordinate function on $Y$ (image of $u_j$ in $P(Y)$). Choose $f_j \in k[t_1,\dots,t_n]$ whose class modulo $I(X)$ equals $\psi(\eta_j)$.  
Define a polynomial map $\tilde{\phi}= (f_1,\dots,f_m): k^n \to k^m$.

We check $\tilde{\phi}(X) \subseteq Y$:
If $g \in I(Y)$, then $g(\eta_1,\dots,\eta_m)=0$ in $P(Y)$. Applying $\psi$ gives $g(\psi(\eta_1),\dots,\psi(\eta_m))=0$ in $P(X)$, i.e. $g(f_1,\dots,f_m) \in I(X)$. Hence for all $x \in X$, $g(f_1(x),\dots,f_m(x)) = 0$, so $\tilde{\phi}(x) \in Y$.

Thus $\phi = \tilde{\phi}|_X$ is a regular map $X \to Y$.

* Start with $\phi$, get $\psi(\eta)=\eta \circ \phi$, then reconstruct $\phi'$ via $f_j = \psi(\eta_j)$.  
  But $\psi(\eta_j) = \eta_j \circ \phi$ is exactly the $j$‑th component of $\phi$, so $\phi'=\phi$.

* Start with $\psi$, get $\phi$, then reconstruct $\psi'$ by $\psi'(\eta)=\eta \circ \phi$.  
  For $\eta$ represented by $g$, $\eta \circ \phi$ is the class of $g(f_1,\dots,f_m)$.  
  Since $f_j$ lifts $\psi(\eta_j)$, $g(f_1,\dots,f_m)$ lifts $\psi(g(\eta_1,\dots,\eta_m))=\psi(\eta)$.  
  Hence $\psi'(\eta) = \psi(\eta)$.

Therefore we have a one‑to‑one correspondence.