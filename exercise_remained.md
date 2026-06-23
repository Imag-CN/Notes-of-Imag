Exercise 5.11
Let $f: A \to B$ be a flat homomorphism of rings. Then $f$ has the going-down property. 

*Solution:*
A ring homomorphism $f: A \to B$ possesses the going-down property if, whenever $\mathfrak{p} \subseteq \mathfrak{p}'$ are primes of $A$ and $\mathfrak{q}'$ is a prime of $B$ lying over $\mathfrak{p}'$, there exists a prime $\mathfrak{q}$ of $B$ lying over $\mathfrak{p}$ and contained in $\mathfrak{q}'$. Exercise 10 says that  the property holds precisely when the induced map $\operatorname{Spec}(B_{\mathfrak{q}}) \to \operatorname{Spec}(A_{\mathfrak{p}})$ is surjective for every prime ideal $\mathfrak{q}$ of $B$ whose contraction to $A$ is $\mathfrak{p} = \mathfrak{q} \cap A$. The result of Chapter 3, Exercise 18 asserts that flatness of the homomorphism $f$ guarantees exactly this surjectivity on the localized spectra. It follows directly that $f$ has the going-down property.

---
Exercise 5.12
Let $G$ be a finite group of automorphisms of a ring $A$, and let $A^G$ denote the subring of $G$-invariants, that is of all $x \in A$ such that $\sigma(x) = x$ for all $\sigma \in G$. Prove that $A$ is integral over $A^G$. If $x \in A$, observe that $x$ is a root of the polynomial $\prod_{\sigma \in G} (t - \sigma(x))$.

Let $S$ be a multiplicatively closed subset of $A$ such that $\sigma(S) \subseteq S$ for all $\sigma \in G$, and let $S^G = S \cap A^G$. Show that the action of $G$ on $A$ extends to an action on $S^{-1}A$, and that $(S^G)^{-1}A^G \cong (S^{-1}A)^G$.

*Solution:*
Let $x$ be an arbitrary element of the ring $A$. The polynomial whose roots are the images of $x$ under the automorphisms comprising the finite group $G$ takes the form $\prod_{\sigma \in G} (t - \sigma(x))$. This polynomial is monic of degree equal to the order of $G$, and its coefficients are the elementary symmetric polynomials evaluated at the conjugates $\sigma(x)$. Every automorphism $\tau$ belonging to $G$ simply permutes the set of these conjugates, leaving the symmetric functions unchanged; the coefficients therefore all belong to the invariant subring $A^G$. The polynomial vanishes upon substitution of $t = x$, so $x$ is a root of a monic polynomial over $A^G$ and is consequently integral over $A^G$. Since the choice of $x$ was arbitrary, the ring $A$ is integral over its subring of $G$-invariants.

For the second assertion, let $S$ be a multiplicatively closed subset of $A$ stable under the automorphisms of $G$, and let $S^G$ denote its intersection with the invariant subring. Each automorphism $\sigma$ of $A$ extends to an automorphism of the localization $S^{-1}A$ via the assignment $\sigma(a/s) = \sigma(a)/\sigma(s)$. This assignment respects the equivalence relation defining the localization: whenever two fractions agree in $S^{-1}A$, some element of $S$ annihilates their difference, and applying $\sigma$ yields an element of $S$ annihilating the difference of the images (by the stability assumption on $S$). The resulting maps assemble into a group action of $G$ on $S^{-1}A$ extending the given action on $A$.

The subring of elements of $S^{-1}A$ fixed by every automorphism in $G$ is canonically isomorphic to the localization of $A^G$ at $S^G$. The natural ring homomorphism from $A^G$ to the invariant subring of $S^{-1}A$ carries $S^G$ to units, inducing a homomorphism $(S^G)^{-1}A^G \to (S^{-1}A)^G$. This homomorphism is injective, as any element of $A^G$ that becomes zero after localization at $S^G$ was already zero. To show surjectivity, consider an arbitrary $G$-invariant element $x$ of $S^{-1}A$ and write it in the form $x = a/s$ with $a \in A$ and $s \in S$. Invariance means that $\sigma(a)/\sigma(s) = a/s$ holds in the localization for every $\sigma \in G$. Construct the product $s' = \prod_{\sigma \in G} \sigma(s)$; the factors are permuted by any automorphism, so $s'$ is fixed by $G$ and therefore lies in $S^G$. Set $a' = a \prod_{\sigma \neq \mathrm{id}} \sigma(s) \in A$. Hence we have $x = a'/s'$ in $S^{-1}A$. The same invariance relation, together with the fact that automorphisms merely permute the factors appearing in the auxiliary product, implies that every automorphism fixes the element $a'$. Hence $a' \in A^G$, and $x$ arises as the image of the fraction $a'/s'$ under the natural map from the localized invariants. 

___
Exercise 5.13
In the situation of Exercise 12, let $\mathfrak{p}$ be a prime ideal of $A^G$, and let $P$ be the set of prime ideals of $A$ whose contraction is $\mathfrak{p}$. Show that $G$ acts transitively on $P$. In particular, $P$ is finite.

*Solution:*
In the situation of the preceding exercise the ring $A$ is integral over the invariant subring $A^G$. Let $\mathfrak{p}$ be a prime ideal of $A^G$ and let $P$ denote the set of all prime ideals of $A$ that contract to $\mathfrak{p}$. The group $G$ acts on the set of all prime ideals of $A$ by transport of structure, and this action preserves contractions to $A^G$; consequently $G$ permutes the elements of the fiber $P$. To show transitivity, fix two primes $\mathfrak{q}_1, \mathfrak{q}_2 \in P$ and an arbitrary element $x \in \mathfrak{q}_1$. The product $\prod_{\sigma \in G} \sigma(x)$ lies in $\mathfrak{q}_1$ because $\mathfrak{q}_1$ is a prime ideal and one of the factors already belongs to $\mathfrak{q}_1$. At the same time the product is fixed by every automorphism in $G$ and therefore belongs to $A^G$, hence it lies in the intersection $\mathfrak{q}_1 \cap A^G = \mathfrak{p}$. Since $\mathfrak{p} \subseteq \mathfrak{q}_2$ it follows that the product also belongs to the prime ideal $\mathfrak{q}_2$. Because $\mathfrak{q}_2$ is prime, at least one factor $\sigma(x)$ must lie in $\mathfrak{q}_2$, which means that $x$ lies in $\sigma^{-1}(\mathfrak{q}_2)$. As $x$ was arbitrary, $\mathfrak{q}_1$ is contained in the union $\bigcup_{\sigma \in G} \sigma^{-1}(\mathfrak{q}_2)$. Equivalently, $\mathfrak{q}_1$ is contained in the finite union $\bigcup_{\tau \in G} \tau(\mathfrak{q}_2)$ of prime ideals. By the prime avoidance lemma the ideal $\mathfrak{q}_1$ is contained in one of the primes $\tau(\mathfrak{q}_2)$. Both $\mathfrak{q}_1$ and $\tau(\mathfrak{q}_2)$ lie over the same prime $\mathfrak{p}$ of $A^G$. Corollary 5.9 then forces $\mathfrak{q}_1 = \tau(\mathfrak{q}_2)$. Hence some element of $G$ carries $\mathfrak{q}_2$ to $\mathfrak{q}_1$, proving that the action is transitive. Since the acting group is finite, every orbit is finite; transitivity therefore implies that the entire fiber $P$ is finite.

___

Exercise 5.8
(i) Let $A$ be a subring of an integral domain $B$, and let $C$ be the integral closure of $A$ in $B$. Let $f, g$ be monic polynomials in $B[x]$ such that $fg \in C[x]$. Then $f, g \in C[x]$.

*Solution*: Because $B$ is an integral domain we may form its field of fractions and embed the latter in a splitting field for the monic polynomials $f$ and $g$ inside some algebraically closed extension. In this splitting field we may therefore write $f = \prod_{i=1}^m (x - \xi_i)$ and $g = \prod_{j=1}^n (x - \eta_j)$. The hypothesis that the product $fg$ lies in $C[x]$ implies that every root $\xi_i$ of $f$ satisfies a monic equation over $C$ and is consequently integral over $C$. The coefficients of $f$, being (up to sign) the elementary symmetric polynomials in the $\xi_i$, are therefore themselves integral over $C$ and must belong to the integral closure $C$. Hence $f$ itself lies in $C[x]$. The identical reasoning applied to the roots $\eta_j$ of $g$ shows that the coefficients of $g$ likewise lie in $C$, so $g \in C[x]$.

(ii) Prove the same result without assuming that $B$ (or $A$) is an integral domain.

*Solution*: It suffices to show that $B$ can be embedded in a ring where $fg$ splits, and then all the same applies. To argue this clearly, we pr ove the following lemma:

*Lemma.* Given ring $A$ and monic $f \in A[x]$, there exists some ring $B$ with $A \subset B$ such that $f$ splits in $B[x]$. 
*Proof.* Argue by induction, suppose that this lemma stands for any $g$ with degree smaller than $k$ and suppose $\mathrm{deg}f = k > 1$. Let $B = A[x]/(f)$. Note that $A$ is included in $B$ and $\bar{x}$ , the image of $x \in A[x]$, is non-zero in $B$. Hence consider the function $f'$ that is formally the same as $f$ in $B[t]$, i.e. say $f = \sum a_{n}x^n \in A[x]$, let $f' =\sum a_{n}t^n \in B[t]$. Then $f'(\bar{x}) = \bar{f} = 0$ and $f'$ factors as $g(t)(t-\bar{x})$ with $\mathrm{deg}g = k-1$. By inductive assumption, $g$ splits in the polynomial ring of some $C$ with $B \subset C$, which is the desired ring. 

---

Exercise 5.9
Let $A$ be a subring of a ring $B$ and let $C$ be the integral closure of $A$ in $B$. Prove that $C[x]$ is the integral closure of $A[x]$ in $B[x]$.

*Solution*: 
Let $f$ be an arbitrary element of $B[x]$ that is integral over $A[x]$. Then there exist a positive integer $n$ and polynomials $g_1,\dots,g_n\in A[x]$ such that
$$
f^n + g_1 f^{n-1} + \cdots + g_n = 0.
$$
Choose an integer $r$ strictly larger than $n$, strictly larger than the degree of each $g_i$, and also strictly larger than the degree of $f$ whenever $f$ is nonzero. Define the auxiliary element $f_1 := f - x^r \in B[x]$. Substituting the relation $f = f_1 + x^r$ into the integral equation and expanding each power by the binomial theorem produces, after collecting terms, the new monic equation
$$
f_1^n + h_1 f_1^{n-1} + \cdots + h_n = 0
$$
in which every coefficient $h_i$ now lies in $A[x]$. In particular the constant term $h_n$ (with respect to powers of $f_1$) belongs to $A[x]$. Rearrangement of this equation yields the factorization
$$
(-f_1) \cdot P = h_n \in A[x] \subset C[x],
$$
where $P$ denotes the polynomial $f_1^{n-1} + h_1 f_1^{n-2} + \cdots + h_{n-1} \in B[x]$. By the choice of the integer $r$ the translated polynomial $-f_1$ is monic in $B[x]$. Exercise 8(i) therefore applies directly to the pair of monic polynomials $(-f_1,P)$ whose product lies in $C[x]$, and we conclude that both factors belong to $C[x]$. In particular $f_1 \in C[x]$. Adding the monomial $x^r \in A[x] \subset C[x]$ then shows that the original polynomial $f = f_1 + x^r$ lies in $C[x]$. Since $f$ was arbitrary, every element of $B[x]$ that is integral over $A[x]$ already lies in $C[x]$, as claimed.

---
