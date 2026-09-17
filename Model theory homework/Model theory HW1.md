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
**a)** $\phi$ asserts $E$ is an equivalence relation with each class of size exactly $2$. If $|M| = n$ and $\mathcal{M} \models \phi$, then $n$ must be even. Conversely, for any even $n = 2k$, partition $\{1,\dots,n\}$ into $k$ pairs; the resulting structure models $\phi$. Hence the spectrum is $\{2,4,6,\dots\}$.

**b)**
i) $X = \{2^n 3^m : n,m > 0\}$.  
$\mathcal{L} = \{E,F\}$, two equivalence relations. $\phi$: $E$ has classes of size $2$, $F$ has classes of size $3$, and each $E$-class intersects each $F$-class exactly once. Then $|M| = 2^a \cdot 3^b$ for some $a,b > 0$.

ii) $X = \{m > 0 : m \text{ is composite}\}$.  
$\mathcal{L} = \{E,F\}$, two equivalence relations. $\phi$: $E$ has at least one class of size $>1$, $F$ has at least one class of size $>1$, and every $E$-class and $F$-class intersect in exactly one element. Then $|M| = a \cdot b$ with $a,b > 1$, i.e., composite.

iii) $X = \{p^n : p \text{ prime}, n > 0\}$.  
$\mathcal{L} = \{E,U\}$, $U$ a unary predicate, $E$ an equivalence relation. $\phi$: $U$ is nonempty, $E$ restricted to $U$ has classes of equal size $p$, and $E$ restricted to the complement of $U$ has classes of size 1. Then $|M| = p \cdot k$; iterate to get $p^n$.

iv) $X = \{p : p \text{ is prime}\}$.  
$\mathcal{L} = \{E\}$. $\phi$: $E$ is an equivalence relation with all classes of the same size $k \ge 2$, and there is exactly one class (so $|M| = k$), together with a sentence forcing $k$ to be prime (e.g., $k$ cannot be factored into smaller uniform class sizes).

**c)†**  
($\Rightarrow$) If $X$ is a finite spectrum, there is a sentence $\phi$ with models of size $n$ iff $n \in X$. A nondeterministic Turing machine on input $1^n$ guesses an $\mathcal{L}$-structure of size $n$ and verifies $\phi$ in exponential time.  
($\Leftarrow$) If a NTM $M$ accepts $1^n$ in exponential time iff $n \in X$, encode its computation as a first-order structure of size exponential in $n$. Using equivalence relations to compress the encoding to size $n$, we obtain a sentence whose finite spectrum is $X$.