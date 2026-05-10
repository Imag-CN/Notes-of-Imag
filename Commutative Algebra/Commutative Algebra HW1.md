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

