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

For $x$ in the kernel, $1\otimes x=0$ implies $1\otimes x=0$ in some $K_{0}\otimes M_{0}$ where $K_{0}$ and $M_{0}$ are some f.g. $A$-module as submodule of $K$ and $M$ with $1\in K_{0}$ and $x \in M_{0}$ (Corollary 2.13).