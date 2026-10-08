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
>Let  $\mathcal{M}$ be an -structure. We say that  is definable if the graph of  is a definable set in $M^{n+m}$.
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

>[!problem] [MAR] 1.4.10
>Let $\mathcal{M}$ be an $\mathcal{L}$-structure and $A \subseteq M$. We say that $b \in M$ is definable over $A$ if there is a formula $\phi(v, \overline{w})$ and $\overline{a} \in A$ such that
>$$
>\mathcal{M} \models \phi(b, \overline{a}) \land \forall y \ (\phi(y, \overline{a}) \to y = b).
>$$
>In other words, $\{b\}$ is $A$-definable.
>
>a) Show that $x$ is definable over $A$ if and only if for some $n$ there is an $A$-definable function $f : M^n \to M$ and $\overline{a} \in M$ such that $f(\overline{a}) = x$.
>
>b) Suppose that $x$ is definable from $A$ and $\sigma$ is an automorphism of $\mathcal{M}$ such that $\sigma(a) = a$ for all $a \in A$. Show that $\sigma(x) = x$.
>
>Let $\operatorname{dcl}(A) = \{x \in M : x \text{ is definable from } A\}$.
>
>c) Show that $\operatorname{dcl}(\operatorname{dcl}(A)) = A$.

**Proof:**
**(a)** Suppose first that $x$ is definable over $A$. Then $\{x\}$ is $A$-definable. Define the constant function $f:M\to M$ by $f(y)=x$. Its graph is
$$
\operatorname{Graph}(f)=M\times\{x\},
$$
which is $A$-definable. Thus $f$ is $A$-definable, and $f(a)=x$ for any $a\in M$.

Conversely, suppose $f:M^n\to M$ is $A$-definable, $\overline{a}\in A^n$, and $f(\overline{a})=x$. If $\psi(\overline{v},w)$ defines the graph of $f$ over $A$, then
$$
\psi(\overline{a},w)
$$
uniquely defines $x$ over $A$. Hence $x\in\operatorname{dcl}(A)$.

**(b)** Let $\phi(v,\overline{a})$ uniquely define $x$, where $\overline{a}\in A$. Since $\sigma$ fixes $A$ pointwise,
$$
\mathcal M\models\phi(x,\overline{a})
\quad\Longrightarrow\quad
\mathcal M\models\phi(\sigma(x),\overline{a}).
$$
But $\phi(v,\overline{a})$ has a unique solution, so $\sigma(x)=x$.

**(c)** We prove
$$
\operatorname{dcl}(\operatorname{dcl}(A))=\operatorname{dcl}(A).
$$
The inclusion $\operatorname{dcl}(A)\subseteq\operatorname{dcl}(\operatorname{dcl}(A))$ is immediate.

Conversely, let $x\in\operatorname{dcl}(\operatorname{dcl}(A))$. Then $x$ is uniquely defined by some formula
$$
\phi(v,b_1,\ldots,b_n),
$$
where each $b_i\in\operatorname{dcl}(A)$. For each $i$, choose a formula $\psi_i(w,\overline{a}_i)$ over $A$ uniquely defining $b_i$. Then $x$ is uniquely defined over $A$ by
$$
\exists w_1\cdots\exists w_n\left(
\bigwedge_{i=1}^n\psi_i(w_i,\overline{a}_i)
\land
\phi(v,w_1,\ldots,w_n)
\right).
$$
Thus $x\in\operatorname{dcl}(A)$, proving
$$
\operatorname{dcl}(\operatorname{dcl}(A))=\operatorname{dcl}(A).
$$
___

> [!problem] [MAR] 1.4.11
> Let $\mathcal{M}$ be an $\mathcal{L}$-structure and $A\subseteq M$. We say that $b\in M$ is *algebraic over $A$* if there is an $\mathcal{L}$-formula $\phi(v,\overline{w})$ and $\overline{a}\in A$ such that
> $$
> \mathcal{M}\models\phi(b,\overline{a})
> $$
> and $\{y\in M:\mathcal{M}\models\phi(y,\overline{a})\}$ is finite. We let $\operatorname{acl}(A)=\{x:x\text{ is algebraic over }A\}$.
>
> a) Suppose that $x\in\operatorname{acl}(A)$. Show that there are $x_1,\ldots,x_m$ such that if $\sigma$ is an automorphism of $\mathcal{M}$ with $\sigma(a)=a$ for all $a\in A$, then $\sigma(x)=x_i$ for some $i$. In other words, there are only finitely many conjugates of $x$ under automorphisms of $\mathcal{M}$ fixing $a$.
>
> b) Show that $\operatorname{acl}(\operatorname{acl}(A))=\operatorname{acl}(A)$.
>
> c) Show that if $x\in\operatorname{acl}(A)$, then $x\in\operatorname{acl}(A_0)$ for some finite $A_0\subseteq A$.
>
> d) Show that if $A\subseteq B$, then $\operatorname{acl}(A)\subseteq\operatorname{acl}(B)$.

**Proof:**
**(a)** Since $x\in\operatorname{acl}(A)$, there is a formula $\phi(v,\overline{a})$ with $\overline{a}\in A$ such that
$$
X=\{y\in M:\mathcal{M}\models\phi(y,\overline{a})\}
$$
is finite and contains $x$. Write $X=\{x_1,\ldots,x_m\}$.

If $\sigma\in\operatorname{Aut}(\mathcal{M})$ fixes $A$ pointwise, then it fixes $\overline{a}$. Since $\mathcal{M}\models\phi(x,\overline{a})$, we have
$$
\mathcal{M}\models\phi(\sigma(x),\overline{a}).
$$
Thus $\sigma(x)\in X$, so $\sigma(x)=x_i$ for some $i$.

**(b)** Clearly $\operatorname{acl}(A)\subseteq\operatorname{acl}(\operatorname{acl}(A))$. For the reverse inclusion, let $x\in\operatorname{acl}(\operatorname{acl}(A))$. Then there are $b_1,\ldots,b_n\in\operatorname{acl}(A)$ and a formula $\phi(v,\overline{b})$ such that
$$
X=\{x'\in M:\mathcal{M}\models\phi(x',\overline{b})\}
$$
is finite and contains $x$.

For each $i$, choose a formula $\psi_i(w,\overline{a}_i)$ over $A$ whose solution set $B_i$ is finite and contains $b_i$. Consider
$$
\theta(v):=\exists w_1\cdots\exists w_n\left(\phi(v,w_1,\ldots,w_n)\land\bigwedge_{i=1}^n\psi_i(w_i,\overline{a}_i)\right).
$$
This is a formula over $A$ satisfied by $x$. Its solution set is contained in
$$
\bigcup_{(c_1,\ldots,c_n)\in B_1\times\cdots\times B_n}
\{y:\mathcal{M}\models\phi(y,c_1,\ldots,c_n)\}.
$$
However, these sets need not all be finite, so we refine $\phi$ to assert that it has exactly $|X|$ solutions. Let $m=|X|$ and let $\chi_m(\overline{w})$ express that $\phi(v,\overline{w})$ has exactly $m$ solutions. Replacing $\phi$ by $\phi(v,\overline{w})\land\chi_m(\overline{w})$, every set in the above union is finite of size $m$. Hence $\theta(M)$ is finite.

Therefore $x\in\operatorname{acl}(A)$, and
$$
\operatorname{acl}(\operatorname{acl}(A))=\operatorname{acl}(A).
$$

**(c)** If $x\in\operatorname{acl}(A)$, then $x$ satisfies some formula $\phi(v,\overline{a})$ with parameters $\overline{a}\in A$, having only finitely many solutions. Since a formula contains only finitely many parameters, let $A_0\subseteq A$ be the finite set of entries of $\overline{a}$. Then $x\in\operatorname{acl}(A_0)$.

**(d)** Suppose $A\subseteq B$ and $x\in\operatorname{acl}(A)$. Then some formula $\phi(v,\overline{a})$ with $\overline{a}\in A$ defines a finite set containing $x$. Since $A\subseteq B$, the same formula is also a formula with parameters from $B$. Hence $x\in\operatorname{acl}(B)$.

Therefore
$$
\operatorname{acl}(A)\subseteq\operatorname{acl}(B).
$$