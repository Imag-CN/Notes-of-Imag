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
No. Consider the subring $A=k[x^2 - 1]$ of $B=k[x]$, where $k$ is a field, and let $\mathfrak{n} = (x - 1)$, then $\mathfrak{m}=\mathfrak{n}\cap A=(x^{2}-1)$. Pick $y=1 /(x+1) \in B_{\mathfrak{n}}$, suppose $f(y)=0$ for some monic $f(t)\in A_{\mathfrak{m}}[t]$. Suppose $\operatorname{deg}f=n$, then $f(y)=f(1 /(x+1))$ has a pole $x=-1$ of order $n$, thus nonzero, contradiction. Therefore, $B_{\mathfrak{n}}$ is not integral over $A_{\mathfrak{m}}$.
___

> [!problem] [ATI] 5.5
> Let $A \subseteq B$ be rings, $B$ integral over $A$.
>
> i) If $x \in A$ is a unit in $B$, then it is a unit in $A$.
>
> ii) The Jacobson radical of $A$ is the contraction of the Jacobson radical of $B$.

**Proof:**
**i)** Since $B$ integral over $A$, there exists some monic $f(t)\in A[t]$ such that $f(x^{-1})=0$. Suppose $\operatorname{deg}f=n$, then $x^{-1}=x^{n-1}(x^{-n}-f(x^{-1}))\in B$ (since $x^{n-1}(x^{-n}-f(x^{-1}))$ is a polynomial of $x$ with coefficients in $A$).

**ii)** Since the contraction of a maximal ideal of $B$ is a maximal ideal of $A$, the Jacobson radical of $A$ is contained in the contraction of the Jacobson radical of $B$ (Corollary 5.8).

Conversely, take any $x$ in contraction of the Jacobson radical of $B$, then $1-bx$ is a unit in $B$ for any $b\in B$. Thus by **i)**, $1-ax$ is a unit in $A$ for any $a\in A$, so $x$ is in the Jacobson radical of $A$.
___

>[!problem] [ATI] 5.6
>Let $B_1, \dots, B_n$ be integral $A$-algebras. Show that $\prod_{i=1}^{n} B_i$ is an integral $A$-algebra.

**Proof:**
Denote $B=\prod_{i=1}^{n} B_i$.

We clarify the definition:
$$
B_{i} \text{ is an integral } A\text{-algebra} \iff \exists f_{i}:A\to B_{i} \text{ s.t. }B_{i} \text{ is integral over }f_{i}(A)
$$
So it suffices to find a $f:A\to B$ such that $B$ is integral over $f(A)$.

We define $f:A\to B$ as $a\mapsto(f_{1}(a),\dots,f_{n}(a))$. Take any $b=(b_{1},\dots,b_{n})\in B$. Since $B_{i}$ is integral $A$-algebra, there exist monic $p_{i}\in f_{i}(A)[x]$ such that $p_{i}(b_{i})=0$ ($i=1,\dots,n$). Since $f_{i}:A\to f_{i}(A)$ is surjective, we can find monic $q_{i}\in A[x]$ such that $p_{i}=f_{i}(q_{i})$. Let $q=q_{1}\cdot\dots \cdot q_{n}$ and $p=f(q)$, then $p \in f(A)[x]$ is monic. And $p(b)=(f_{1}(q)(b_{1}),\dots ,f_{n}(q)(b_{n}))=(0,\dots,0)$. Therefore, $B$ is integral over $f(A)$.
___

> [!problem] [ATI] 5.7
> Let $A$ be a subring of a ring $B$, such that the set $B - A$ is closed under multiplication. Show that $A$ is integrally closed in $B$.

**Proof:**
Suppose $b \in B$ is integral over $A$, so there exist $f(x)=x^{n}+a_{n-1}x^{n-1}+\dots+a_{0}\in A[x]$ of minimal degree such that
$$
f(b)=b^n + a_{n-1}b^{n-1} + \cdots + a_0 = 0.
$$
Assume for contradiction that $b \notin A$, i.e., $b \in B - A$. 

Rewrite the equation as
$$
b(b^{n-1} + a_{n-1}b^{n-2} + \cdots + a_1) = -a_0 \in A.
$$
By the minimality of degree of $f(x)$, $b^{n-1} + a_{n-1}b^{n-2} + \cdots + a_1\not\in A$. And since $B-A$ is closed under multiplication, $b(b^{n-1} + a_{n-1}b^{n-2} + \cdots + a_1)\in B-A$, contradition.

Therefore, $A$ is integrally closed in $B$.
___

> [!problem] [ATI] 5.10
> Let $f: A \to B$ be a homomorphism of rings. We say that $f$ has the going-up property (resp. the going-down property) if the conclusion of the going-up theorem (5.11) (resp. the going-down theorem (5.16)) holds for $B$ and its subring $f(A)$. Let $f^*: \operatorname{Spec}(B) \to \operatorname{Spec}(A)$ be the mapping associated with $f$.
>
> i) Consider the following three statements:
>
> (a) $f^*$ is a closed mapping.
> (b) $f$ has the going-up property.
> (c) For any prime ideal $\mathfrak{q}$ of $B$, let $\mathfrak{p} = \mathfrak{q}^c$; then the mapping $f^*: \operatorname{Spec}(B/\mathfrak{q}) \to \operatorname{Spec}(A/\mathfrak{p})$ is surjective.
>
> Prove that (a) $\Rightarrow$ (b) $\Leftrightarrow$ (c). (See also Chapter 6, Exercise 11.)
>
> ii) Consider the following three statements:
>
> (a') $f^*$ is an open mapping.
> (b') $f$ has the going-down property.
> (c') For any prime ideal $\mathfrak{q}$ of $B$, let $\mathfrak{p} = \mathfrak{q}^c$; then the mapping $f^*: \operatorname{Spec}(B_{\mathfrak{q}}) \to \operatorname{Spec}(A_{\mathfrak{p}})$ is surjective.
>
> Prove that (a') $\Rightarrow$ (b') $\Leftrightarrow$ (c').

**Proof:**
**i) (b) $\Leftrightarrow$ (c)**
Let $\mathfrak{q} \subseteq B$ be prime, $\mathfrak{p} = \mathfrak{q}^c$. Going-up for $f$ means: for any $\mathfrak{p}' \supseteq \mathfrak{p}$ in $A$, there exists $\mathfrak{q}' \supseteq \mathfrak{q}$ in $B$ with $(\mathfrak{q}')^c = \mathfrak{p}'$. This is exactly the surjectivity of $f^*: \operatorname{Spec}(B/\mathfrak{q}) \to \operatorname{Spec}(A/\mathfrak{p})$. Hence (b) $\Leftrightarrow$ (c).

**(a) $\Rightarrow$ (b)**
Assume $f^*$ is closed. Let $\mathfrak{p} \subseteq \mathfrak{p}'$ in $A$ and $\mathfrak{q}$ prime in $B$ with $\mathfrak{q}^c = \mathfrak{p}$. The set $V(\mathfrak{q}) \subseteq \operatorname{Spec}(B)$ is closed, so $f^*(V(\mathfrak{q}))$ is closed in $\operatorname{Spec}(A)$. Since $\mathfrak{p} \in f^*(V(\mathfrak{q}))$, we have $V(\mathfrak{p}) \subseteq f^*(V(\mathfrak{q}))$. Hence $\mathfrak{p}' \in V(\mathfrak{p}) \subseteq f^*(V(\mathfrak{q}))$, so there exists $\mathfrak{q}' \in V(\mathfrak{q})$ with $(\mathfrak{q}')^c = \mathfrak{p}'$. Then $\mathfrak{q}' \supseteq \mathfrak{q}$ and $(\mathfrak{q}')^c = \mathfrak{p}'$, proving going-up.

**ii) (b') $\Leftrightarrow$ (c')**  
Let $\mathfrak{q} \subseteq B$ be prime, $\mathfrak{p} = \mathfrak{q}^c$. Going-down for $f$ means: for any $\mathfrak{p}_0 \subseteq \mathfrak{p}$ in $A$, there exists $\mathfrak{q}_0 \subseteq \mathfrak{q}$ in $B$ with $\mathfrak{q}_0^c = \mathfrak{p}_0$. This is exactly the surjectivity of $f^*: \operatorname{Spec}(B_{\mathfrak{q}}) \to \operatorname{Spec}(A_{\mathfrak{p}})$. Hence (b') $\Leftrightarrow$ (c').

**(a') $\Rightarrow$ (b')**  
Assume $f^*$ is open. Let $\mathfrak{p} \subseteq \mathfrak{p}'$ in $A$ and $\mathfrak{q}'$ prime in $B$ with $(\mathfrak{q}')^c = \mathfrak{p}'$. Write $B_{\mathfrak{q}'} = \varinjlim_{t \in B \setminus \mathfrak{q}'} B_t$. Then
$$ f^*(\operatorname{Spec}(B_{\mathfrak{q}'})) = \bigcap_{t \in B \setminus \mathfrak{q}'} f^*(\operatorname{Spec}(B_t)). $$
Each $Y_t = \operatorname{Spec}(B_t)$ is open in $\operatorname{Spec}(B)$, so $f^*(Y_t)$ is open in $\operatorname{Spec}(A)$ (since $f^*$ is open). Moreover, $\mathfrak{q}' \in Y_t$ for all $t$, so $f^*(Y_t)$ is an open neighbourhood of $\mathfrak{p}'$. Hence $\operatorname{Spec}(A_{\mathfrak{p}'}) \subseteq \bigcap_t f^*(Y_t) = f^*(\operatorname{Spec}(B_{\mathfrak{q}'}))$. In particular, for $\mathfrak{p} \subseteq \mathfrak{p}'$, there exists $\mathfrak{q} \in \operatorname{Spec}(B_{\mathfrak{q}'})$ with $\mathfrak{q}^c = \mathfrak{p}$. Since $\operatorname{Spec}(B_{\mathfrak{q}'})$ corresponds to primes of $B$ contained in $\mathfrak{q}'$, we have $\mathfrak{q} \subseteq \mathfrak{q}'$ and $\mathfrak{q}^c = \mathfrak{p}$, proving going-down.
___

> [!problem] [ATI] 5.14
> Let $A$ be an integrally closed domain, $K$ its field of fractions and $L$ a finite normal separable extension of $K$. Let $G$ be the Galois group of $L$ over $K$ and let $B$ be the integral closure of $A$ in $L$. Show that $\sigma(B) = B$ for all $\sigma \in G$, and that $A = B^G$.

**Proof**
For any $\sigma \in G$ and $b \in B$, $b$ is integral over $A$, so $\sigma(b)$ is also integral over $A$ (apply $\sigma$ to the monic polynomial satisfied by $b$). Hence $\sigma(b) \in B$, so $\sigma(B) \subseteq B$. Applying $\sigma^{-1}$ gives $B \subseteq \sigma(B)$, so $\sigma(B) = B$.

Clearly $A \subseteq B^G$. Conversely, let $x \in B^G$. Then $x \in L$ and $\sigma(x) = x$ for all $\sigma \in G$, so $x \in K$ by Galois theory. Since $x \in B$ and $A$ is integrally closed in $K$, we have $x \in A$. Thus $B^G \subseteq A$, so $A = B^G$.
___

> [!problem] [ATI] 5.15
> Let $A$, $K$ be as in Exercise 14, let $L$ be any finite extension field of $K$, and let $B$ be the integral closure of $A$ in $L$. Show that, for any prime ideal $\mathfrak{p}$ of $A$, the set of prime ideals $\mathfrak{q}$ of $B$ such that $\mathfrak{q} \cap A = \mathfrak{p}$ is finite (i.e., that the morphism $\operatorname{Spec}(B) \to \operatorname{Spec}(A)$ has finite fibres).

**Proof:**
Factor $L/L_{\text{sep}}/K$ with $L_{\text{sep}}$ the separable closure of $K$ in $L$. Let $B_{\text{sep}}$ be the integral closure of $A$ in $L_{\text{sep}}$. The fiber over $\mathfrak{p}$ factors through $\operatorname{Spec}(B) \to \operatorname{Spec}(B_{\text{sep}})$ and $\operatorname{Spec}(B_{\text{sep}}) \to \operatorname{Spec}(A)$. Finiteness of the first follows from case (b), the second from case (a). So treat each case.

**Case (a): $L/K$ separable.** Embed $L$ into a finite normal separable extension $N/K$. Let $C$ be the integral closure of $A$ in $N$. By Exercise 14, $C$ is $G = \operatorname{Gal}(N/K)$-stable and $A = C^G$. By Exercise 13, primes of $C$ over $\mathfrak{p}$ are finitely many (bounded by $[N:K]$). Since $B \subseteq C$, each prime $\mathfrak{q}$ of $B$ over $\mathfrak{p}$ lifts to a prime of $C$ over $\mathfrak{p}$, and distinct $\mathfrak{q}$ give distinct contractions to $A$, so the number of such $\mathfrak{q}$ is finite.

**Case (b): $L/K$ purely inseparable.** $\operatorname{char}(K) = p > 0$. For $\mathfrak{q} \subseteq B$ with $\mathfrak{q} \cap A = \mathfrak{p}$, define
$$ \mathfrak{q}' = \{ x \in B \mid x^{p^m} \in \mathfrak{p} \text{ for some } m \ge 0 \}. $$
If $x \in \mathfrak{q}$, then $x^{p^m} \in \mathfrak{q} \cap K = \mathfrak{p}$ for large $m$, so $x \in \mathfrak{q}'$. Conversely, if $x \in \mathfrak{q}'$, then $x^{p^m} \in \mathfrak{p} \subseteq \mathfrak{q}$ and $\mathfrak{q}$ prime gives $x \in \mathfrak{q}$. Hence $\mathfrak{q} = \mathfrak{q}'$ is uniquely determined by $\mathfrak{p}$, so the fiber is a singleton, hence finite.