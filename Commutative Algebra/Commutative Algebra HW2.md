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
___

>[!problem] [ATI] 3.9
>Let $S_0$ be the set of all non-zero-divisors in a ring $A$. Prove that $S_0$ is a saturated multiplicatively closed subset of $A$. Hence the set $D$ of zero-divisors in $A$ is a union of prime ideals. Show that every minimal prime ideal of $A$ is contained in $D$.The ring $S_0^{-1}A$ is called the total ring of fractions of $A$. Prove that:
>
>(i) $S_0$ is the largest multiplicatively closed subset of $A$ for which the homomorphism $A \to S_0^{-1}A$ is injective.
>
>(ii) Every element in $S_0^{-1}A$ is either a zero-divisor or a unit.
>
>(iii) Every non-unit in $S_0^{-1}A$ is a zero-divisor.

**Proof:**
**Multiplicatively closedness:** Obviously $1\in S_{0}$. And if $s_{1},s_{2} \in S_{0}$ but $s_{1}s_{2}\not\in S_{0}$, then $s_{1}s_{2}u=0$ for some $u\in A \neq 0$. Since $s_{2}\in S_{0}$, $s_{2}u\neq 0$, then it becomes a zero divisor of $s_{1}$, contradition.

