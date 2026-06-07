___

>[!problem] [ATI] 3.3
>Let $A$ be a ring, let $S$ and $T$ be two multiplicatively closed subsets of $A$, and let $U$ be the image of $T$ in $S^{-1}A$. Show that the rings $(ST)^{-1}A$ and $U^{-1}(S^{-1}A)$ are isomorphic.

**Proof:**
Defien $\phi: (ST)^{-1}A\to U^{-1}(S^{-1}A)$ as $a /(st) \mapsto (a/s) / (t/1)$. Check:

**Well-definedness:** Let $a/ (st)=a' / (s't')$, then $u(as't'-a'st)=0$ for some $u\in ST$, thus $(u / (ss'))\cdot((at') /s -(a't) /s')=0$. While $u / ss'$ is in $U$, we have $(a /s) /(t /1)=(a' /s') /(t' /1)$.

**Homomorphism:** It is obvious that $\phi(1)=1$ and $\phi$ preserves multiplication. We check for addition:
$$
\phi(a /(st)+a' /(s't'))=\phi((as't'+a'st) /(sts't'))=((as't'+a'st) /(ss') ) /(tt'/1),
$$
$$
\phi(a/(st))+\phi(a' /(s't'))= (a/s) / (t/1)+(a'/s') / (t'/1')=((as't'+a'st) /(ss') ) /(tt'/1),
$$
so $\phi(a /(st)+a' /(s't'))=\phi(a /(st))+\phi(a' /(s't'))$.

**Injectivity:** Let $a / (st) \in \operatorname{ker}\phi$, then $u(a/s)=0$ for some $u \in ST$, and thus $vua=0$ for some $v\in S$. Since $vu$ is in $ST$, we have $a / (st)=0$.

**Surjectivity:** Take any element $(a / s) / (t / s')\in U^{-1}(S^{-1}A)$, it is equal to $(s'a /s) / (t/1)$, thus in the image of $\phi$.
___

>[!problem] [ATI] 3.4
>Let $f: A \to B$ be a homomorphism of rings and let $S$ be a multiplicatively closed subset of $A$. Let $T = f(S)$. Show that $S^{-1}B$ and $T^{-1}B$ are isomorphic as $S^{-1}A$-modules.

**Proof:**
Define $\phi: S^{-1}B\to T^{-1}B$ as $b / s\mapsto b / f(s)$. Check:

**Well-definedness:** Let $b /s=b' /s'$, then $u(bs'-b's)=0$ for some $u\in S$. Apply $f$, we get $f(u)(bf(s')-b' f(s) )=0$, thus $b /f(s)=b' /f(s')$.

**$S^{-1}A$-linearity:** Take $b/s,b' /s'\in S^{-1}B$ and $a /t, a' /t' \in S^{-1}A$, then
$$
\phi((a/t) \cdot (b /s)+(a'/t') \cdot (b' /s'))=\phi((f(a)b) /(st)+(f(a')b') / (s't'))=f(a)b /f(st)+f(a')b' / f(s't'),
$$
$$
\phi((a/t) \cdot (b /s))+\phi((a'/t') \cdot (b' /s'))=f(a)b /f(st)+f(a')b' / f(s't'),
$$
so $\phi$ is $S^{-1}A$-linear.

**Injectivity:** Take $b /s \in \operatorname{ker}\phi$, then $b / f(s)=0$, so $ub=0$ for some $u\in S$, thus $b /s=0$.

**Surjectivity:** Obvious.
___

>[!problem] [ATI] 3.5
>Let $A$ be a ring. Suppose that, for each prime ideal $\mathfrak{p}$, the local ring $A_{\mathfrak{p}}$ has no nilpotent element $\neq 0$. Show that $A$ has no nilpotent element $\neq 0$. If each $A_{\mathfrak{p}}$ is an integral domain, is $A$ necessarily an integral domain?

**Proof:**
Suppose $a\in A$ is a non-zero nilpotent element. Let $\mathfrak{m}$ be a maximal ideal that contains $\operatorname{Ann}a$. Since $\operatorname{Ann}a\subset \mathfrak{m}$, we know $a / 1\in A_{\mathfrak{m}}$ is not zero. But $a /1$ is nilpotent because $a$ is nilpotent, thus contradiction.

Consider $A=\mathbb{F}_{2}\times \mathbb{F}_{2}$, then it has only two prime ideals, $\{ 0 \}\times \mathbb{F}_{2}$ and $\mathbb{F}_{2}\times\{0  \}$. Thus $A_{\mathfrak{p}} \cong \mathbb{F}_{2}$, which is an integral domain. But $A$ is not integral domain because $(0,1)\cdot(1,0)=(0,0)$.

>[!remark]
> The statement can be strengthen by substituting prime ideal into maximal ideal.

___

>[!problem] [ATI] 3.9
>Let $S_0$ be the set of all non-zero-divisors in a ring $A$. Prove that $S_0$ is a saturated multiplicatively closed subset of $A$. Hence the set $D$ of zero-divisors in $A$ is a union of prime ideals. Show that every minimal prime ideal of $A$ is contained in $D$.The ring $S_0^{-1}A$ is called the total ring of fractions of $A$. Prove that:
>
>(i) $S_0$ is the largest multiplicatively closed subset of $A$ for which the homomorphism $A \to S_0^{-1}A$ is injective.
>
>(ii) Every element in $S_0^{-1}A$ is either a zero-divisor or a unit.
>
>(iii) Every ring in which every non-unit is a zero-divisor is equal to its total ring of fractions (i.e., $A \to S_{0}^{-1}A$ is bijective).

**Proof:**
**Multiplicatively closedness:** Obviously $1\in S_{0}$. And if $s_{1},s_{2} \in S_{0}$ but $s_{1}s_{2}\not\in S_{0}$, then $s_{1}s_{2}u=0$ for some $u\in A \neq 0$. Since $s_{2}\in S_{0}$, $s_{2}u\neq 0$, then it becomes a zero divisor of $s_{1}$, contradition.

**Every minimal prime ideal is in $D$:** Let $\mathfrak{p}$ be a minimal prime ideal of $A$, $S_{0}$ be $A\setminus \mathfrak{p}$. Let $\Sigma$ be the collection of multiplicatively close subset $S$ of $A$ such that $S\supset S_{0}$ and $0 \not\in S$. Clearly $\Sigma$ suffices the conditions of Zorn's lemma, so there is a maximal element $S_{1}$. By exercise 6 we know $A\setminus S_{1}$ is a minimal prime ideal, so $S_{1}=S_{0}$. Therefore $\mathfrak{p}\subset A\setminus S_{0}=D$.


**(i)** Take $S$ a multiplicatively closed subset of $A$ which contains a zero divisor $s$, say $st=0$ for $t\in A\neq {0}$. Then $t$ is in the kernel of $A\to S_{0}^{-1}A$, which makes the homomorphism not injective.

**(ii)** Suppose $a /s \in S_{0}^{-1}A$ is a not a unit and $a\neq 0$, then $a\not\in S_{0}$ (otherwise $s /a$ is an inverse of $a /s$). Then $a$ is a zero-divisor, say $ta=0$ for some $t\in A$ . Then $a /s \cdot t /1 =0$, thus $a /s$ is a zero divisor.

**(iii)** First check injectivity: take  $a\in \operatorname{ker} (A\to S_{0}^{-1}A)$, then $as=0$ for some $s \in S_{0}$. Since $s$ is not a zero divisor, $a$ must be $0$.

Then check surjectivity: take $a / s \in S_{0}^{-1}A$, then $s$ is a unit since it is not a zero divisor. Then $a /s=as^{-1} /1$ is in the image.
___

>[!problem] [ATI] 3.10
>Let $A$ be a ring.
>
>(i) If $A$ is absolutely flat and $S$ is any multiplicatively closed subset of $A$, then $S^{-1}A$ is absolutely flat.
>
>(ii) $A$ is absolutely flat $\Leftrightarrow$ $A_{\mathfrak{m}}$ is a field for each maximal ideal $\mathfrak{m}$.

**Proof:**
**(i)** For any $S^{-1}A$-module $M$, we have $M$ is naturally an $A$-module. Since $A$ is absolutely flat, $M$ is flat as an $A$-module. The functor $S^{-1}$ is exact, so $S^{-1}M$ is flat as an $S^{-1}A$-module. And $S^{-1}M$ is isomorphic to $M$ as $S^{-1}A$-module, so $M$ is flat, thus $S^{-1}A$ is absolutely flat.

**(ii)** $\Rightarrow$: By (i), $A_{\mathfrak{m}}$ is absolutely flat. Let $x \in A_{\mathfrak{m}}$, $x \neq 0$. Since $A_{\mathfrak{m}}$ is absolutely flat, consider the ideal generated by $x$ and use Chapter 2 exercise 27, there exists $y_{1},y_{2} \in A_{\mathfrak{m}}$ with $x = (xy_{1})(xy_{2})$, i.e., $x(1 - xy) = 0$ where $y=y_{1}y_{2}$. Suppose $x$ is not a unit, then $x$ is in the Jacobson radical because $A_{\mathfrak{m}}$ is local. Then $1-xy$ is invertible, which implies that $x=0$, contradiction.

$\Leftarrow$: It suffices to show absolute flatness is a local property. Let $N,P,M$ be three $A$-module and $f$ be an injection from $N$ to $P$. Denote the localization of $N,P,M$ at $\mathfrak{m}$ as $N',P',M'$. Then $N',P',M'$ naturally $A_{\mathfrak{m}}$-modules, and $f':N'\to P'$ is injection. Since $A_{\mathfrak{m}}$ is absolutely flat, $f'\otimes \operatorname{id}:N'\otimes_{A_{\mathfrak{m}}}M'\to P'\otimes_{A_{\mathfrak{m}}}M'$ is injection. Since flatness is a local property, $f\otimes \operatorname{id}$ is injection. Therefore, $A$ is absolutely flat.
___

>[!problem] [ATI] 3.12
>Let $A$ be an integral domain and $M$ an $A$-module. An element $x \in M$ is a torsion element of $M$ if $\mathrm{Ann}(x) \neq 0$, that is if $ax = 0$ for some $a \neq 0$. Prove that the torsion elements of $M$ form a submodule of $M$. This submodule is called the torsion submodule and is denoted by $T(M)$. If $T(M) = 0$ the module $M$ is said to be torsion-free. Prove
>
>(i) If $M$ is any $A$-module, then $M/T(M)$ is torsion-free.
>
>(ii) If $f: M \to N$ is a module homomorphism, then $f(T(M)) \subseteq T(N)$.
>
>(iii) If $0 \to M' \to M \to M''$ is an exact sequence, then the sequence $0 \to T(M') \to T(M) \to T(M'')$ is exact.
>
>(iv) $T(M)$ is the kernel of the mapping $x \mapsto 1 \otimes x$ of $M$ into $K \otimes_A M$, where $K$ is the field of fractions of $A$.

**Proof:**
**Torsion elements form a submodule:** For $a,a'\in A$ and $m,m'\in T(M)$, it suffices to show $am+a'm'\in T(M)$. Suppose $bm=b'm'=0$ for non-zero $b,b'\in A$. Then $bb'$ is non-zero (because $A$ is an integral domain) and $bb'(am+a'm')=0$. Therefore, $T(M)$ is a submodule of $M$.

**(i)** Suppose $\overline{ m }\in M / T(M)$ is a torsion element, then $a \overline{ m }=\overline{ 0 }$ for some $a\in A\neq 0$, and $am \in T(M)$. Suppose $bam=0$ for $b\in A \neq 0$, then $m$ is a torsion element since $ab \neq 0$. Therefore, $\overline{ m }=0$, and $M / T(M)$ is torsion-free.

**(ii)** Suppose $m \in T(M)$, say $am=0$ for some $a\in A \neq 0$. Then $f(am)=af(m)=0$. Thus $f(m)\in T(N)$, and $f(T(M))\subseteq T(N)$.

**(iii)** Denote $f:M'\to M$ and $g:M\to M''$, and $T(f)$, $T(g)$ be the corresponding maps between torsion submodule. Because $T(M)$ and $T(M')$ are submodule of $M$ and $M'$, it is obvious that $T(f)$ is injection and $\operatorname{im} T(f)\subset \operatorname{ker}T(g)$ suffices to show $\operatorname{ker}T(g)=\operatorname{im}T(f)$. Take $m\in \operatorname{ker}T(g)$, then $m\in \operatorname{ker}g=\operatorname{im}f$, thus $m=f(m')$ for some $m'\in M'$. Suppose $am=0$ for $a\in A \neq 0$, then $f(am')=am=0$. Since $f$ is injection, $am'=0$, and $m'\in T(M')$. Therefore, $m\in \operatorname{im}T(f)$, so $\operatorname{im}T(f)=\operatorname{ker}T(g)$.

**(iv)** For $m \in T(m)$, say $am=0$ for $a\in A \neq 0$, $1\otimes m=(1 /a)\otimes(am)=0$, thus $m$ is in that kernel.

Take $x$ in the kernel. Let $S=A \setminus\{ 0 \}$, then $K=S^{-1}A$, so $K\otimes_{A}M$ is isomorphic to $S^{-1}M$. Then $x /1=0$, so $ax=0$ for some $a\in S$. Therefore, $x$ is in $T(M)$.
___

>[!problem] [ATI] 3.13
>Let $S$ be a multiplicatively closed subset of an integral domain $A$. In the notation of Exercise 12, show that
>
>$$T(S^{-1}M) = S^{-1}(TM).$$
>
>Deduce that the following are equivalent:
>
>(i) $M$ is torsion-free.
>
>(ii) $M_{\mathfrak{p}}$ is torsion-free for all prime ideals $\mathfrak{p}$.
>
>(iii) $M_{\mathfrak{m}}$ is torsion-free for all maximal ideals $\mathfrak{m}$.

**Proof:**
Assume $0 \not\in S$, then $S^{-1}A \neq 0, S^{-1} M\neq 0$.
**"$\subset$":** Take $m /s \in T(S^{-1}M)$, say $am / ts =0$ where $a / t\in S^{-1}A \neq 0$. Then $uam=0$ for some $u\in S\neq 0$, so $m\in T(M)$. Therefore, $m / s \in S^{-1}(TM)$.
**"$\supset$":** Take $m / s \in S^{-1}(TM)$, say $am=0$ where $a\in A \neq 0$. Then $a/ 1 \cdot m /s =0$, thus $m / s \in T(S^{-1} M)$.

The equivalence of **(i)(ii)(iii)** follows from that vanishing is a local property.
___

>[!problem] [ATI] 5.7
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

> [!problem] [ATI] 3.14
> Let $M$ be an $A$-module and $\mathfrak{a}$ an ideal of $A$. Suppose that $M_{\mathfrak{m}} = 0$ for all maximal ideals $\mathfrak{m} \supseteq \mathfrak{a}$. Prove that $M = \mathfrak{a}M$.

**Proof:**
Consider the module $N=M / \mathfrak{a}M$ as a $A /\mathfrak{a}A$-module. Every maximal ideal of $A /\mathfrak{a}A$ corresponds to a maximal ideal of $A$ containing $\mathfrak{a}$. Thus $N_{\mathfrak{m}}=0$ for any maximal ideals in $A/\mathfrak{a}A$. Since vanishing is a local property, $N=0$, thus $M= \mathfrak{a} M$.
___

> [!problem] [ATI] 3.20
> Let $f: A \to B$ be a ring homomorphism, $f^*: \operatorname{Spec}(B) \to \operatorname{Spec}(A)$ the associated mapping. Show that
> i) Every prime ideal of $A$ is a contracted ideal $\Leftrightarrow f^*$ is surjective.
> ii) Every prime ideal of $B$ is an extended ideal $\Rightarrow f^*$ is injective.
> Is the converse of ii) true?

**Proof:**
**(i)** **"$\Rightarrow$":** Take any $\mathfrak{p}\in \operatorname{Spec}(A)$, let $\mathfrak{p}=\mathfrak{q}^{c}$, then $f^{*}(\mathfrak{q})=\mathfrak{p}$, thus $f^{*}$ is surjective.
**"$\Leftarrow$":** Take any $\mathfrak{p}\in \operatorname{Spec}(A)$, let $\mathfrak{p}=f^{*}(\mathfrak{q})$, then $\mathfrak{p}=\mathfrak{q}^{c}$.
**(ii)** Suppose $f^{*}(\mathfrak{q}_1) = f^{*}(\mathfrak{q}_2)$. Write $\mathfrak{q}_1 = \mathfrak{p}_1^{\;e}$ and $\mathfrak{q}_2 = \mathfrak{p}_2^{\;e}$ for some prime ideals $\mathfrak{p}_1, \mathfrak{p}_2$ of $A$. Then
$$
f^{*}(\mathfrak{q}_1) = \mathfrak{p}_1, \qquad f^{*}(\mathfrak{q}_2) = \mathfrak{p}_2,
$$
so $\mathfrak{p}_1 = \mathfrak{p}_2$. Hence $\mathfrak{q}_1 = \mathfrak{p}_1^{\;e} = \mathfrak{p}_2^{\;e} = \mathfrak{q}_2$. Therefore $f^{*}$ is injective.

**Converse of (ii) is false:** Let $A=\mathbb{C}[t^{2},t^{3}]$, $B=\mathbb{C}[t]$, $f$ be the inclusion map. Take any $(t-a)\in \operatorname{Spec}B$, then $f^{*}((t-a))=(t^{2}-a^{2},t^{3}-a^{3})$, thus $f^{*}$ is injective. But $(t)^{ce}=(t^{2},t^{3})^{e}=(t^{2})\neq (t)$, thus $(t)$ is not an extended ideal.
___

> [!problem] [ATI] 4.1
>If an ideal $\mathfrak{a}$ has a primary decomposition, then $\operatorname{Spec}(A/\mathfrak{a})$ has only finitely many irreducible components.

**Proof:**
Let $\mathfrak{a} = \bigcap_{i=1}^n \mathfrak{q}_i$ be a minimal primary decomposition, $\mathfrak{p}_i = r(\mathfrak{q}_i)$. Then
$$
V(\mathfrak{a}) = \bigcup_{i=1}^n V(\mathfrak{q}_i) = \bigcup_{i=1}^n V(\mathfrak{p}_i).
$$
Each $V(\mathfrak{p}_i) \cong \operatorname{Spec}(A/\mathfrak{p}_i)$ is irreducible because $A/\mathfrak{p}_i$ is a domain.

Hence the $V(\mathfrak{p}_i)$ are the finitely many irreducible components of $\operatorname{Spec}(A/\mathfrak{a})$.'
___

> [!problem] [ATI] 4.7
>Let $A$ be a ring and let $A[x]$ denote the ring of polynomials in one indeterminate over $A$. For each ideal $\mathfrak{a}$ of $A$, let $\mathfrak{a}[x]$ denote the set of all polynomials in $A[x]$ with coefficients in $\mathfrak{a}$.
>
>i) $\mathfrak{a}[x]$ is the extension of $\mathfrak{a}$ to $A[x]$.
>
>ii) If $\mathfrak{p}$ is a prime ideal in $A$, then $\mathfrak{p}[x]$ is a prime ideal in $A[x]$.
>
>iii) If $\mathfrak{q}$ is a $\mathfrak{p}$-primary ideal in $A$, then $\mathfrak{q}[x]$ is a $\mathfrak{p}[x]$-primary ideal in $A[x]$.
>
>iv) If $\mathfrak{a} = \bigcap_{i=1}^n \mathfrak{q}_i$ is a minimal primary decomposition in $A$, then $\mathfrak{a}[x] = \bigcap_{i=1}^n \mathfrak{q}_i[x]$ is a minimal primary decomposition in $A[x]$.
>
>v) If $\mathfrak{p}$ is a minimal prime ideal of $\mathfrak{a}$, then $\mathfrak{p}[x]$ is a minimal prime ideal of $\mathfrak{a}[x]$.

**Proof:**
i) $\mathfrak{a}[x]$ consists of polynomials with all coefficients in $\mathfrak{a}$. This is precisely the ideal $\mathfrak{a}^e = \mathfrak{a}A[x]$ generated by $\mathfrak{a}$ in $A[x]$.

ii) Let $f,g \in A[x]$, $fg \in \mathfrak{p}[x]$. Reduce coefficients mod $\mathfrak{p}$; then $\bar f \bar g = 0$ in $(A/\mathfrak{p})[x]$, an integral domain. Hence $\bar f = 0$ or $\bar g = 0$, i.e., $f \in \mathfrak{p}[x]$ or $g \in \mathfrak{p}[x]$. So $\mathfrak{p}[x]$ is prime.

iii) Let $fg \in \mathfrak{q}[x]$ with $f \notin \mathfrak{p}[x]$. Reducing mod $\mathfrak{p}$ gives $\bar f \bar g = 0$ in $(A/\mathfrak{p})[x]$. Since $\bar f \neq 0$ and $A/\mathfrak{p}$ is a domain, $\bar g = 0$, so all coefficients of $g$ are in $\mathfrak{p}$. Thus $g^m \in \mathfrak{q}[x]$ for some $m$ (because $\mathfrak{q}$ is $\mathfrak{p}$-primary and coefficients of $g$ lie in $\mathfrak{p}$). Hence $\mathfrak{q}[x]$ is primary; its radical is $\mathfrak{p}[x]$.

iv) Extension preserves intersections: $\mathfrak{a}[x] = \bigcap \mathfrak{q}_i[x]$. Each $\mathfrak{q}_i[x]$ is $\mathfrak{p}_i[x]$-primary by (iii), and the primes $\mathfrak{p}_i[x]$ are distinct (since $\mathfrak{p}_i$ are distinct). Minimality follows because no $\mathfrak{q}_i[x]$ can be omitted (otherwise contracting to $A$ would contradict minimality of the decomposition in $A$).

v) If $\mathfrak{p}$ is minimal over $\mathfrak{a}$, then $\mathfrak{p}[x]$ contains $\mathfrak{a}[x]$. If $\mathfrak{q}$ is prime in $A[x]$ with $\mathfrak{a}[x] \subseteq \mathfrak{q} \subseteq \mathfrak{p}[x]$, then contracting to $A$ gives $\mathfrak{a} \subseteq \mathfrak{q}^c \subseteq \mathfrak{p}$. By minimality of $\mathfrak{p}$, $\mathfrak{q}^c = \mathfrak{p}$. Hence $\mathfrak{q} = \mathfrak{p}[x]$ (since $\mathfrak{p} \subseteq \mathfrak{q}^c$ implies $\mathfrak{p}[x] \subseteq \mathfrak{q}$ and $\mathfrak{q} \subseteq \mathfrak{p}[x]$). Thus $\mathfrak{p}[x]$ is minimal over $\mathfrak{a}[x]$.
___

>[!problem] [ATI] 4.8
>Let $k$ be a field. Show that in the polynomial ring $k[x_1, \ldots, x_n]$ the ideals
>$\mathfrak{p}_i = (x_1, \ldots, x_i) \quad (1 \leqslant i \leqslant n)$ are prime and all their powers are primary.

**Proof:**
**Prime:** $k[x_1,\dots,x_n]/\mathfrak{p}_i \cong k[x_{i+1},\dots,x_n]$ is an integral domain, so $\mathfrak{p}_i$ is prime.

**All powers are primary:** We induct on $n$. For $n=1$, $\mathfrak{p}_1=(x_1)$ is prime, and in a PID, powers of a prime ideal are primary (even prime).  

Assume the statement holds for $n-1$ variables. Set $A=k[x_1,\dots,x_{n-1}]$, $y=x_n$. Then $k[x_1,\dots,x_n]=A[y]$, and $\mathfrak{p}_i$ in $A[y]$ is $\mathfrak{p}_{i}'[y]$ where $\mathfrak{p}_i'=(x_1,\dots,x_i)\subset A$ (if $i<n$), or $\mathfrak{p}_n=(x_1,\dots,x_{n-1},y)$.

If $i<n$, by the induction hypothesis, $(\mathfrak{p}_i')^m$ is primary in $A$. By Exercise 7(iii), $(\mathfrak{p}_i')^m A[y] = (\mathfrak{p}_i)^m$ is primary in $A[y]$.

If $i=n$, $\mathfrak{p}_n = (x_1,\dots,x_{n-1},y)$. Then $\mathfrak{p}_n^m$ is generated by monomials of total degree $m$ in $x_1,\dots,x_{n-1},y$. Let $fg \in \mathfrak{p}_n^m$ with $f\notin \mathfrak{p}_n$. Then $f$ has a term not in $(x_1,\dots,x_{n-1},y)$; hence $f$ has a nonzero constant term in the variable $y$ after setting $x_1=\dots=x_{n-1}=0$. Modulo $(x_1,\dots,x_{n-1})$, we are in $k[y]$, where $(y)^m$ is primary. Hence $g^m \in \mathfrak{p}_n^m$.  

Thus all powers of $\mathfrak{p}_i$ are primary.
___

>[!problem] [ATI] 4.9
>In a ring $A$, let $D(A)$ denote the set of prime ideals $\mathfrak{p}$ which satisfy the following condition: there exists $a \in A$ such that $\mathfrak{p}$ is minimal in the set of prime ideals containing $(0:a)$. Show that $x \in A$ is a zero divisor $\Leftrightarrow x \in \mathfrak{p}$ for some $\mathfrak{p} \in D(A)$.
>
>Let $S$ be a multiplicatively closed subset of $A$, and identify $\operatorname{Spec}(S^{-1}A)$ with its image in $\operatorname{Spec}(A)$ (Chapter 3, Exercise 21). Show that
>$$D(S^{-1}A) = D(A) \cap \operatorname{Spec}(S^{-1}A).$$
>
>If the zero ideal has a primary decomposition, show that $D(A)$ is the set of associated prime ideals of $0$.

**Proof:**
**1.** $x$ is a zero divisor  $\iff$ $\exists a \neq 0$ with $xa = 0$  $\iff$ $\exists a \neq 0$ with $(0:a) \supseteq (x)$.  
Let $\mathfrak{p}$ be minimal among primes containing $(0:a)$. Then $\mathfrak{p} \in D(A)$ and $x \in \mathfrak{p}$.  

Conversely, if $x \in \mathfrak{p} \in D(A)$, then $\mathfrak{p}$ is minimal over $(0:a)$ for some $a \neq 0$. Since $x \in \mathfrak{p}$ and $\mathfrak{p}$ is minimal over $(0:a)$, $x$ is in every prime containing $(0:a)$, hence $x$ is in the intersection of all primes containing $(0:a)$, which is $\sqrt{(0:a)}$. Thus $x^n a = 0$ for some $n$, so $x$ is a zero divisor.

**2.** Let $\mathfrak{p} \in D(S^{-1}A)$. Then $\mathfrak{p} = S^{-1}\mathfrak{q}$ for some $\mathfrak{q} \in \operatorname{Spec}(A)$ disjoint from $S$, and $\mathfrak{p}$ is minimal over $(0:a/s)$ in $S^{-1}A$ for some $a/s \in S^{-1}A$. This is equivalent to $\mathfrak{q}$ being minimal over $(0:a)$ in $A$ and $\mathfrak{q} \cap S = \varnothing$. Hence $\mathfrak{p} \in D(A) \cap \operatorname{Spec}(S^{-1}A)$. The reverse inclusion is similar.

**3.**  If $0 = \bigcap_{i=1}^n \mathfrak{q}_i$ is a minimal primary decomposition with $\mathfrak{p}_i = \sqrt{\mathfrak{q}_i}$, then the associated primes of $0$ are $\{\mathfrak{p}_1,\dots,\mathfrak{p}_n\}$. For each $i$, pick $a \in \bigcap_{j \neq i} \mathfrak{q}_j \setminus \mathfrak{q}_i$. Then $(0:a)$ is $\mathfrak{p}_i$-primary, so $\mathfrak{p}_i$ is the unique minimal prime containing $(0:a)$. Thus $\mathfrak{p}_i \in D(A)$. Conversely, if $\mathfrak{p} \in D(A)$, then $\mathfrak{p}$ is minimal over $(0:a)$ for some $a$. Since $(0:a)$ is an ideal whose radical contains $\mathfrak{p}$, and $0$ has primary decomposition, $\mathfrak{p}$ must be one of the $\mathfrak{p}_i$ (by uniqueness theorems for associated primes). Hence $D(A) = \{\mathfrak{p}_1,\dots,\mathfrak{p}_n\}$.
___

>[!problem] [ATI] 4.10
>For any prime ideal $\mathfrak{p}$ in a ring $A$, let $S_{\mathfrak{p}}(0)$ denote the kernel of the homomorphism $A \to A_{\mathfrak{p}}$. Prove that
>**i)** $S_{\mathfrak{p}}(0) \subseteq \mathfrak{p}$.
>**ii)** $r(S_{\mathfrak{p}}(0)) = \mathfrak{p} \iff \mathfrak{p}$ is a minimal prime ideal of $A$.
>**iii)** If $\mathfrak{p} \supseteq \mathfrak{p}'$, then $S_{\mathfrak{p}}(0) \subseteq S_{\mathfrak{p}'}(0)$.
>**iv)** $\bigcap_{\mathfrak{p} \in D(A)} S_{\mathfrak{p}}(0) = 0$, where $D(A)$ is defined in Exercise 9.

**Proof:**
**i)** Let $a \in S_{\mathfrak{p}}(0)$. Then $\frac{a}{1}=0$ in $A_{\mathfrak{p}}$, so there exists $s \notin \mathfrak{p}$ with $sa=0$. Since $0 \in \mathfrak{p}$ and $\mathfrak{p}$ is prime, $s \notin \mathfrak{p}$ and $sa \in \mathfrak{p}$ imply $a \in \mathfrak{p}$. Hence $S_{\mathfrak{p}}(0) \subseteq \mathfrak{p}$.

**ii)** $\Rightarrow$: Suppose $r(S_{\mathfrak{p}}(0)) = \mathfrak{p}$. If $\mathfrak{q} \subsetneq \mathfrak{p}$ is a prime ideal, pick $x \in \mathfrak{p} \setminus \mathfrak{q}$. Since $x \in r(S_{\mathfrak{p}}(0))$, $x^n \in S_{\mathfrak{p}}(0)$ for some $n$. Then $s x^n = 0$ for some $s \notin \mathfrak{p}$, hence $s \in \mathfrak{q}$ (because $\mathfrak{q}$ is prime and $x \notin \mathfrak{q}$), contradicting $s \notin \mathfrak{p} \supset \mathfrak{q}$. Thus $\mathfrak{p}$ is minimal.

$\Leftarrow$: Let $\mathfrak{p}$ be minimal. By (i), $S_{\mathfrak{p}}(0) \subseteq \mathfrak{p}$, so $r(S_{\mathfrak{p}}(0)) \subseteq \mathfrak{p}$. For the reverse, take $x \in \mathfrak{p}$. Consider the multiplicatively closed set $S = \{ x^n \mid n \ge 0 \}$. In $A_x = S^{-1}A$, $\mathfrak{p}_x$ is a prime. Since $\mathfrak{p}$ is minimal, $\mathfrak{p}_x$ is minimal in $A_x$, and by (i) applied to $A_x$, $S_{\mathfrak{p}_x}(0) \subseteq \mathfrak{p}_x$. But $x/1$ is in the kernel of $A_x \to (A_x)_{\mathfrak{p}_x}$ (because localizing at $\mathfrak{p}_x$ inverts elements outside $\mathfrak{p}$, and $x \in \mathfrak{p}$), so $x/1 \in S_{\mathfrak{p}_x}(0)$. Hence $(x/1)^m = 0$ in $A_x$ for some $m$, i.e., $x^m \in S_{\mathfrak{p}}(0)$. Thus $x \in r(S_{\mathfrak{p}}(0))$.

**iii)** If $\mathfrak{p} \supseteq \mathfrak{p}'$, then $A_{\mathfrak{p}'}$ is a localization of $A_{\mathfrak{p}}$. The map $A \to A_{\mathfrak{p}}$ factors as $A \to A_{\mathfrak{p}'} \to A_{\mathfrak{p}}$, so $\ker(A \to A_{\mathfrak{p}}) \subseteq \ker(A \to A_{\mathfrak{p}'})$, i.e., $S_{\mathfrak{p}}(0) \subseteq S_{\mathfrak{p}'}(0)$.

**iv)** By Exercise 9, $D(A)$ is the set of associated primes of $(0)$ if $(0)$ has a primary decomposition; otherwise $D(A)$ is the set of primes minimal over $(0:a)$ for some $a \neq 0$. In either case, $D(A)$ contains all minimal primes of $A$.  

Let $a \in \bigcap_{\mathfrak{p} \in D(A)} S_{\mathfrak{p}}(0)$. For each $\mathfrak{p} \in D(A)$, $\frac{a}{1}=0$ in $A_{\mathfrak{p}}$, so there exists $s_{\mathfrak{p}} \notin \mathfrak{p}$ with $s_{\mathfrak{p}} a = 0$. The ideal generated by all such $s_{\mathfrak{p}}$ is not contained in any $\mathfrak{p} \in D(A)$, hence is the whole ring $A$. Thus $1 = \sum r_i s_{\mathfrak{p}_i}$ for finitely many $\mathfrak{p}_i \in D(A)$, and multiplying by $a$ gives $a=0$. Therefore $\bigcap_{\mathfrak{p} \in D(A)} S_{\mathfrak{p}}(0) = 0$.
___

>[!problem] [ATI] 4.20
>Let $M$ be a fixed $A$-module, $N$ a submodule of $M$. The *radical* of $N$ in $M$ is defined to be
>$$
>r_M(N) = \{x \in A : x^q M \subseteq N \text{ for some } q > 0\}.
>$$
>Show that $r_M(N) = r(N : M) = r(\text{Ann}(M/N))$. In particular, $r_M(N)$ is an ideal.
>
>State and prove the formulas for $r_M$ analogous to (1.13).

**Proof:**
Let $x \in r_M(N)$. Then $\exists q>0$ such that $x^q M \subseteq N$, so $x^q \in (N : M)$, hence $x \in r(N : M)$.

Conversely, let $x \in r(N : M)$. Then $\exists q>0$ such that $x^q \in (N : M)$, i.e. $x^q M \subseteq N$, hence $x \in r_M(N)$.

Therefore,   $$r_M(N) = r(N : M) = r(\operatorname{Ann}(M/N))$$
Since $(N : M)$ is an ideal, $r(N : M)$ is an ideal. Hence $r_M(N)$ is an ideal.

Let $N_1, N_2$ be submodules of $M$. Then:
1. $r_M(N_1 \cap N_2) = r_M(N_1) \cap r_M(N_2)$
2. $r_M(N_1 + N_2) = r(r_M(N_1) + r_M(N_2))$
3. $r_M(r_M(N_1)) = r_M(N_1)$
4. $N_1 \subseteq N_2 \Rightarrow r_M(N_1) \subseteq r_M(N_2)$
5. $r_M(M) = A$, $r_M(0) = r(\operatorname{Ann}(M))$
6. $r_M(N) = A \iff M = N$

**Proofs of the formulas:**

**(1)** $x \in r_M(N_1 \cap N_2)$  
$\iff \exists q>0$ with $x^q M \subseteq N_1 \cap N_2$  
$\iff \exists q>0$ with $x^q M \subseteq N_1$ and $x^q M \subseteq N_2$  
$\iff x \in r_M(N_1) \cap r_M(N_2)$.

**(2)** First note $r_M(N_1) \subseteq r_M(N_1+N_2)$ and $r_M(N_2) \subseteq r_M(N_1+N_2)$, so $r_M(N_1)+r_M(N_2) \subseteq r_M(N_1+N_2)$, hence $r(r_M(N_1)+r_M(N_2)) \subseteq r(r_M(N_1+N_2)) = r_M(N_1+N_2)$.  
Conversely, let $x \in r_M(N_1+N_2)$. Then $\exists q>0$ with $x^q M \subseteq N_1+N_2$. For each $m \in M$, write $x^q m = n_1 + n_2$ with $n_i \in N_i$. This implies $x^q \in (N_1:N_2) \cap (N_2:N_1)$? Actually, a cleaner proof uses (1.13)(v):  
Since $r_M(N_1+N_2) = r((N_1+N_2):M) = r((N_1:M)+(N_2:M))$ and $(N_i:M) = (N_i:M)$, we have by (1.13)(v) that $r((N_1:M)+(N_2:M)) = r(r(N_1:M)+r(N_2:M)) = r(r_M(N_1)+r_M(N_2))$.

**(3)** Follows from (1.13)(ii) because $r_M(r_M(N_1)) = r(r_M(N_1):M) = r(r((N_1:M)):M) = r((N_1:M)) = r_M(N_1)$.

**(4)** If $N_1 \subseteq N_2$, then $(N_1:M) \subseteq (N_2:M)$, so $r(N_1:M) \subseteq r(N_2:M)$, i.e. $r_M(N_1) \subseteq r_M(N_2)$.

**(5)** $(M:M) = A$, so $r_M(M) = r(A) = A$. $(0:M) = \operatorname{Ann}(M)$, so $r_M(0) = r(\operatorname{Ann}(M))$.

**(6)** $r_M(N) = A \iff r((N:M)) = A \iff (N:M) = A$ 
$\iff 1 \in (N:M) \iff 1\cdot M \subseteq N \iff M = N$.