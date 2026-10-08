___

> [!problem] [MAR] 1.4.2
> a) Let $\mathcal{L} = \{\cdot, e\}$ be the language of groups. Show that there is a sentence $\phi$ such that $\mathcal{M} \models \phi$ if and only if $\mathcal{M} \cong \mathbb{Z}/2\mathbb{Z} \times \mathbb{Z}/2\mathbb{Z}$.
>
> b) Let $\mathcal{L}$ be any finite language and let $\mathcal{M}$ be a finite $\mathcal{L}$-structure. Show that there is an $\mathcal{L}$-sentence $\phi$ such that $\mathcal{N} \models \phi$ if and only if $\mathcal{N} \cong \mathcal{M}$.

**Proof:**
**a)** The group $\mathbb{Z}/2\mathbb{Z} \times \mathbb{Z}/2\mathbb{Z}$ is characterized up to isomorphism by being a group of size $4$ where every element has order $2$ except the identity. So define the $\mathcal{L}$-sentence:
$$ \phi := \phi_{\text{grp}} \wedge \phi_{4} \wedge \forall x (x \cdot x = e) $$
where $\phi_{\text{grp}}$ is the conjunction of standard group axioms, and $\phi_{4}$ asserts the universe has exactly $4$ elements ($\exists x_1 \dots x_4 (\bigwedge_{i<j} x_i \neq x_j \wedge \forall y \bigvee_i y = x_i)$). Then $\mathcal{M} \models \phi$ iff $\mathcal{M} \cong \mathbb{Z}/2\mathbb{Z} \times \mathbb{Z}/2\mathbb{Z}$.

**b)** Let $\mathcal{L}$ be a finite language and $\mathcal{M}$ a finite $\mathcal{L}$-structure with domain $\{a_1, \dots, a_n\}$. We construct a sentence $\phi$ capturing $\mathcal{M}$ up to isomorphism:

1. Let $\phi_{\text{size}}$ assert there are exactly $n$ elements.
2. Let $\Delta(x_1, \dots, x_n)$ be the conjunction of all atomic and negated atomic facts (involving relation, function, and constant symbols of $\mathcal{L}$) true in $\mathcal{M}$ on $a_1, \dots, a_n$.

Define $\phi := \phi_{\text{size}} \wedge \exists x_1 \dots \exists x_n \, \Delta(x_1, \dots, x_n)$.
If $\mathcal{N} \models \phi$, $\mathcal{N}$ has exactly $n$ elements and satisfies the same atomic diagram as $\mathcal{M}$; the map sending witnesses in $\mathcal{N}$ to $a_i$ is an isomorphism. Conversely, $\mathcal{N} \cong \mathcal{M}$ implies $\mathcal{N} \models \phi$. Thus $\mathcal{N} \models \phi$ iff $\mathcal{N} \cong \mathcal{M}$.
___

> [!problem] [MAR] 1.4.7
> Let $\phi$ be an $\mathcal{L}$-sentence. The *finite spectrum* of $\phi$ is the set $\{n \in \mathbb{N}^+ : \text{there is } \mathcal{M} \models \phi \text{ with } |M| = n\}$, where $\mathbb{N}^+$ is the set of positive natural numbers.
>
> a) Let $\mathcal{L} = \{E\}$ where $E$ is a binary relation, and let $\phi$ be the sentence that asserts that $E$ is an equivalence relation where every equivalence class has exactly two elements. Show that the finite spectrum of $\phi$ is the set of positive even numbers.
>
> b) For each of the following subsets $X$ of $\mathbb{N}^+$, show that $X$ occurs as the finite spectrum of an $\mathcal{L}$-sentence for some language $\mathcal{L}$:
> i) $\{2^n 3^m : n, m > 0\}$;
> ii) $\{m > 0 : m \text{ is composite}\}$ (i.e. $m = ab$ where $a \neq 1$ and $b \neq 1$);
> iii) $\{p^n : p \text{ is prime and } n > 0\}$;
> iv) $\{p : p \text{ is prime}\}$;
>
> c)† Show that $X \subseteq \mathbb{N}^+$ is a finite spectrum if and only if there is a nondeterministic Turing machine $M$ running in exponential time such that given a string of $n$ 1's as input $M$ halts accepting if and only if $n \in X$. [Remark: An interesting open problem is whether the complement of a finite spectrum is a finite spectrum. This problem shows that it is equivalent to the question of whether the collection of sets recognizable in nondeterministic exponential time is closed under complement.]

**Proof:**
**(a)** If $E$ is an equivalence relation and every equivalence class has exactly two elements, then the domain is partitioned into pairs. Hence $|M|$ is even.

Conversely, if $|M|=2r$, partition $M$ into $r$ pairs and let $E$ be the equivalence relation whose classes are these pairs. Thus the finite spectrum is $\{2r:r>0\}$.

**(b)**
**(i) $\{2^n3^m:n,m>0\}$** Use the language of groups. Let $\phi$ say that $M$ is a group of exponent dividing $6$, together with
$$
\exists x(x\neq e\land x^2=e)
$$
and
$$
\exists y(y\neq e\land y^3=e).
$$

For a finite group satisfying $g^6=e$ for every $g$, Cauchy's theorem implies that only $2$ and $3$ divide $|M|$. The last two conditions ensure that both $2$ and $3$ divide $|M|$. Hence
$$
|M|=2^n3^m,\qquad n,m>0.
$$

Conversely, for every $n,m>0$, the group
$$
(\mathbb Z/2\mathbb Z)^n\times(\mathbb Z/3\mathbb Z)^m
$$
satisfies $\phi$ and has size $2^n3^m$.

**(ii) Composite numbers** Use a language with one binary relation $E$. Let $\phi$ say that $E$ is an equivalence relation, all equivalence classes have the same size, every class has at least two elements, and there are at least two classes.

Then every finite model has
$$
|M|=ab,\qquad a,b>1,
$$
so $|M|$ is composite.

Conversely, if $m=ab$ with $a,b>1$, partition an $m$-element set into $b$ classes of size $a$. This gives a model of $\phi$.

**(iii) $\{p^n:p\text{ prime},\,n>0\}$** Take the language of rings and let $\phi$ be the axioms for a field.

Every finite field has order $p^n$ for some prime $p$ and $n>0$. Conversely, for every prime power $p^n$, there exists a finite field with $p^n$ elements. Therefore the finite spectrum is exactly
$$
\{p^n:p\text{ prime},\,n>0\}.
$$

**(iv) Prime numbers** Use the language of rings, together with a binary relation $<$. Let $\phi$ say that:

1. the structure is a field;
2. $<$ is a linear order with $0$ as its least element;
3. every non-maximal element $x$ has an immediate successor $y$, and
$$
y=x+1.
$$

Starting from $0$, the elements must therefore be
$$
0,1,1+1,\ldots
$$
and every element lies in the additive subgroup generated by $1$. Thus the additive group is cyclic. Since the additive group of a finite field has order $p^n$ and is an elementary abelian $p$-group, it can be cyclic only when $n=1$. Hence
$$
|M|=p
$$
for some prime $p$.

Conversely, $\mathbb F_p$ can be ordered as
$$
0<1<2<\cdots<p-1,
$$
and this order satisfies the required conditions. Hence the finite spectrum is exactly the set of primes.

**(c)** Suppose first that $X$ is the finite spectrum of a sentence $\phi$.

Given $1^n$, a nondeterministic Turing machine guesses the interpretations of all relation and function symbols on an $n$-element domain and then checks whether the resulting structure satisfies $\phi$.

There are only polynomially many pieces of information to guess, and checking a fixed first-order sentence takes polynomial time in the size of the structure. Since the guessed structure has polynomial size in $n$, the whole computation takes at most exponential time in $n$. The machine accepts exactly when there is an $n$-element model of $\phi$, so it accepts exactly when $n\in X$.

Conversely, suppose a nondeterministic Turing machine $M$ accepts $1^n$ in exponential time exactly when $n\in X$. An accepting computation has at most exponentially many steps, so it can be encoded by a finite structure of size polynomial in $2^n$.

Using a standard tableau encoding, a first-order sentence $\phi$ can express that the structure encodes an accepting computation of $M$ on input $1^n$. Thus
$$
n\in X
\iff
\text{there is a finite structure of size }n\text{ satisfying }\phi.
$$

Hence $X$ is a finite spectrum if and only if it is recognizable in nondeterministic exponential time.
___

>[!problem] [MAR] 1.4.8
>Let $\mathcal{L} = \{+, 0\}$. Show that $\mathbb{Z} \oplus \mathbb{Z} \not\cong \mathbb{Z}$.

**Proof:**
The sentence
$$
\exists x \forall y \exists z (y=z+z \vee y=z+z+x)
$$
is true in $\mathbb{Z}$ but not in $\mathbb{Z}\oplus \mathbb{Z}$.
___

>[!problem] [MAR] 1.4.9
>Let  be an -structure. We say that  is definable if the graph of  is a definable set in .
>
>a) Show that if $f: M^n \to M^m$ and $g: M^m \to M^l$ are definable, then so is $g \circ f$.
>
>b) Suppose that $f: M^n \to M$ is definable. Show that the image of $f$ is definable.
>
>c) Suppose that $f: M^n \to M$ is definable and one-to-one. Show that $f^{-1}$ is definable.

**Proof:**
(a) Suppose $f:M^n\to M^m$ and $g:M^m\to M^l$ are definable. Then
$$
\operatorname{Graph}(g\circ f)=\{(x,z):\exists y\,((x,y)\in\operatorname{Graph}(f)\land(y,z)\in\operatorname{Graph}(g))\}.
$$
Since definable sets are closed under conjunction and projection, $\operatorname{Graph}(g\circ f)$ is definable. Hence $g\circ f$ is definable.

(b) Suppose $f:M^n\to M$ is definable. Its image is
$$
f(M^n)=\{y\in M:\exists x\in M^n\,(x,y)\in\operatorname{Graph}(f)\}.
$$
Thus $f(M^n)$ is the projection of a definable set, so it is definable.

(c) Suppose $f:M^n\to M$ is definable and one-to-one. Then $f^{-1}:f(M^n)\to M^n$ is a function, and
$$
\operatorname{Graph}(f^{-1})=\{(y,x):(x,y)\in\operatorname{Graph}(f)\}.
$$
This is definable since $\operatorname{Graph}(f)$ is definable. Hence $f^{-1}$ is definable.
___

