___

> [!problem] [ATI] 5.1
> Let $f: A \to B$ be an integral homomorphism of rings. Show that $f^*: \operatorname{Spec}(B) \to \operatorname{Spec}(A)$ is a closed mapping, i.e., that it maps closed sets to closed sets.

**Proof:**
Let $V(J) \subseteq \operatorname{Spec}(B)$ be a closed set for some ideal $J \subseteq B$. We aim to show that $f^*(V(J)) = V(f^{-1}(J))$ is closed in $\operatorname{Spec}(A)$.

First, clearly $f^*(V(J)) \subseteq V(f^{-1}(J))$ since if $J \subseteq \mathfrak{q}$, then $f^{-1}(J) \subseteq f^{-1}(\mathfrak{q})$.

Conversely, let $\mathfrak{p} \in V(f^{-1}(J))$, so $f^{-1}(J) \subseteq \mathfrak{p}$. Consider the induced map $f_{\mathfrak{p}}: A_{\mathfrak{p}} \to B_{\mathfrak{p}}$. Here, $B_{\mathfrak{p}}$ is integral over $A_{\mathfrak{p}}$, and $\mathfrak{p}A_{\mathfrak{p}}$ is a prime ideal of $A_{\mathfrak{p}}$. By Theorem 5.10, there exists a prime ideal $\mathfrak{q}' \subseteq B_{\mathfrak{p}}$ such that $\mathfrak{q}' \cap A_{\mathfrak{p}} = \mathfrak{p}A_{\mathfrak{p}}$. Let $\mathfrak{q} = \mathfrak{q}' \cap B$. Then $\mathfrak{q}$ is a prime ideal of $B$, $J \subseteq \mathfrak{q}$ (since elements of $S = A \setminus \mathfrak{p}$ are units in $B_{\mathfrak{p}}$ and not in any prime ideal containing $J$), and $f^{-1}(\mathfrak{q}) = \mathfrak{p}$. Hence, $\mathfrak{p} \in f^*(V(J))$.

Therefore, $f^*(V(J)) = V(f^{-1}(J))$ is closed.
___

> [!problem] [ATI] 5.2
> Let $A$ be a subring of a ring $B$ such that $B$ is integral over $A$, and let $f: A \to \Omega$ be a homomorphism of $A$ into an algebraically closed field $\Omega$. Show that $f$ can be extended to a homomorphism of $B$ into $\Omega$.

**Proof:**
Let $\mathfrak{p} = \ker(f)$, and consider the induced injective homomorphism $f': A/\mathfrak{p} \hookrightarrow \Omega$.
Since $B$ is integral over $A$, the ring $B/\mathfrak{p}B$ is integral over $A/\mathfrak{p}$.

By Theorem 5.10, there exists a prime ideal $\mathfrak{q} \subset B/\mathfrak{p}B$ such that $\mathfrak{q} \cap (A/\mathfrak{p}) = 0$. Let $k = (B/\mathfrak{p}B)/\mathfrak{q}$. Then $k$ is a field, and the composite map $A/\mathfrak{p} \hookrightarrow B/\mathfrak{p}B \twoheadrightarrow k$ is injective.
Thus, $A/\mathfrak{p}$ is isomorphic to a subfield of $k$. Furthermore, $k$ is algebraic over $A/\mathfrak{p}$ because it is integral over $A/\mathfrak{p}$.

Since $\Omega$ is an algebraically closed field containing the image of $f'$, there exists an embedding $\phi: k \hookrightarrow \Omega$ extending $f'$.

Let $\pi: B/\mathfrak{p}B \twoheadrightarrow k$ be the canonical projection. The composition $\phi \circ \pi: B/\mathfrak{p}B \to \Omega$ is a homomorphism such that its restriction to $A/\mathfrak{p}$ is $f'$. This map descends to a well-defined homomorphism $\tilde{f}: B \to \Omega$ given by $\tilde{f}(b) = \phi(\pi(b + \mathfrak{p}B))$.

By construction, $\tilde{f}$ extends $f$ to $B$.
___

> [!problem] [ATI] 5.3
> Let $f: B \to B'$ be a homomorphism of $A$-algebras, and let $C$ be an $A$-algebra. If $f$ is integral, prove that $f \otimes 1: B \otimes_A C \to B' \otimes_A C$ is integral. 

**Proof:**
Let $x = b \otimes c \in B \otimes_A C$. We show $y := (f \otimes 1)(x) = f(b) \otimes c$ is integral over $A$.

Since $f$ is integral, $f(b) \in B'$ is integral over $A$, so $A[f(b)]$ is a finitely generated $A$-module.

Then the $A$-module $A[f(b)] \otimes_A C \subseteq B' \otimes_A C$ is finitely generated over $A$ (since tensoring preserves finite generation).

Now, $y = f(b) \otimes c \in A[f(b)] \otimes_A C$, so the subring $A[y] \subseteq A[f(b)] \otimes_A C$ is contained in a finitely generated $A$-module, thus $A[y]$ is a finitely generated $A$-module.

Therefore, $y$ is integral over $A$. 

Hence, $f \otimes 1$ maps pure tensors to integral elements, and since integrality is checked on generators, $f \otimes 1$ is an integral homomorphism.
___

> [!problem] [ATI] 5.4
> Let $A$ be a subring of a ring $B$ such that $B$ is integral over $A$. Let $\mathfrak{n}$ be a maximal ideal of $B$ and let $\mathfrak{m} = \mathfrak{n} \cap A$ be the corresponding maximal ideal of $A$. Is $B_{\mathfrak{n}}$ necessarily integral over $A_{\mathfrak{m}}$?

**Proof:**
No. Consider the subring $k[x^2 - 1]$ of $k[x]$, where $k$ is a field, and let $\mathfrak{n} = (x - 1)$.