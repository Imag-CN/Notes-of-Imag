___

Let $K$ be a non-Archimedean CVF (complete valued field). By $A$ we mean its valuation ring, $\mathfrak{m}$ the unique maximal ideal of $A$, and $k:=A/\mathfrak{m}$ the residue field.

>[!definition] Definition
>We say $K$ is a **perfectoid field** if the following three conditions hold:
>
> (P1) $\operatorname{char}(k)=p>0$ (but $\operatorname{char}(K)$ can be either $0$ or $p$).
>
> (P2) Valuation is *non-discrete*, i.e., the value group $\Gamma:=|K^\times|\subset\mathbb{R}^\times$ is not a discrete subgroup.
>
> (P3) The Frobenius map $\Phi:A/pA\longrightarrow A/pA$ given by $x\mapsto x^p$ is surjective.
>
> (In typical examples, one does not have an isomorphism in (P3).)

___

> [!problem] Problem 1
> (1) Show that the inclusion $\mathcal{O}_{\overline{\mathbb{Q}}_p}\subset\mathcal{O}_C$ induces isomorphisms
> $$
> \mathcal{O}_{\overline{\mathbb{Q}}_p}/p\mathcal{O}_{\overline{\mathbb{Q}}_p}\cong\mathcal{O}_C/p\mathcal{O}_C
> \quad\text{and}\quad
> \mathcal{O}_{\overline{\mathbb{Q}}_p}/\mathfrak{m}_{\overline{\mathbb{Q}}_p}\cong\mathcal{O}_C/\mathfrak{m}_C.
> $$
> (It is not hard to see that the residue field $\mathcal{O}_{\overline{\mathbb{Q}}_p}/\mathfrak{m}_{\overline{\mathbb{Q}}_p}$ is $\overline{\mathbb{F}}_p$ since it is an algebraic extension of $\mathbb{F}_p$ containing an arbitrary finite extension of $\mathbb{F}_p$ in light of Problem Set 06, #3.)
>
> (2) Show that $\Gamma:=|C^{\times}|=p^{\mathbb{Q}}=\{p^a:a\in\mathbb{Q}\}$ in this case, if we normalize the valuation such that $|p|=1/p$.
>
> (3) Check that the Frobenius map $\mathcal{O}_C/p\mathcal{O}_C\longrightarrow\mathcal{O}_C/p\mathcal{O}_C$ is surjective.

**Proof:**
Write $F=\overline{\mathbb{Q}}_p$.

**(1)** In either valuation ring, $p\mathcal{O}=\{x:|x|\le|p|\}$ and $\mathfrak{m}=\{x:|x|<1\}$. Hence
$$
\mathcal{O}_F\cap p\mathcal{O}_C=p\mathcal{O}_F,
\qquad
\mathcal{O}_F\cap\mathfrak{m}_C=\mathfrak{m}_F,
$$
so both induced maps are injective.

For any $x\in\mathcal{O}_C$, density of $F$ in $C$ gives $y\in F$ with $|x-y|<|p|$. The ultrametric inequality gives $|y|\le1$, so $y\in\mathcal{O}_F$. Since $x-y\in p\mathcal{O}_C\subset\mathfrak{m}_C$, both maps are surjective.

**(2)** Every $y\in F^\times$ lies in a finite extension $L/\mathbb{Q}_p$. If its ramification index is $e$, then $|L^\times|=p^{(1/e)\mathbb{Z}}\subset p^{\mathbb{Q}}$. Conversely, $|p^{1/n}|=p^{-1/n}$ for every $n\ge1$, so $|F^\times|=p^{\mathbb{Q}}$.

For $x\in C^\times$, choose $y\in F$ with $|x-y|<|x|$. Then $|y|=|x|$, so completion adds no new values. Thus $\Gamma=p^{\mathbb{Q}}$.

**(3)** Given $x\in\mathcal{O}_C$, choose $y\in\mathcal{O}_F$ with $x-y\in p\mathcal{O}_C$ by (1). Since $F$ is algebraically closed, there exists $z\in F$ with $z^p=y$. Then $|z|^p=|y|\le1$, so $z\in\mathcal{O}_F$, and $z^p\equiv x\pmod{p\mathcal{O}_C}$. Therefore Frobenius is surjective.
___

For problems 2–4, we put ourselves in the following setting. Now we go back to a general perfectoid field $K$ and its valuation ring $A$. Fix a nonzero element
$$
\varpi\in A\quad\text{such that}\quad |p|\le|\varpi|<1.
$$
Such an element is often called a “**pseudo-uniformizer**” as it plays a similar role as a uniformizer for a DVR. If $\operatorname{char}(K)=0$ then one can simply take $\varpi=p$. However if $\operatorname{char}(K)=p$ then one should make a different choice. (E.g., for the completion of $\mathbb{F}_p((t^{1/p^\infty}))$ one can take $\varpi=t$.) In either case, (P3) implies that the $p$-th power map induces a surjection $A/\varpi A\to A/\varpi A$.
___

> [!problem] Problem 2
> Consider the inverse limit along this $p$-th power map (the concrete description given below directly follows the definition of inverse limit):
> $$
> A^\flat:=\varprojlim_p A/\varpi A
> =\{(x_0,x_1,\ldots):x_i\in A/\varpi A,\ x_{i+1}^p=x_i\ \forall i\ge0\}.
> $$
>
> (1) Prove that $A^\flat$ is a perfect ring of characteristic $p$.
>
> (The addition and multiplication are defined by term-by-term operations.)
>
> (2) Show that the canonical map
> $$
> f:\varprojlim_p A=\{(y_0,y_1,\ldots):y_i\in A,\ y_{i+1}^p=y_i\}\longrightarrow A^\flat
> $$
> given by $f:(y_i)\mapsto(y_i\bmod\varpi)$ is a bijection.
>
> (This map is obviously multiplicative with respect to the term-by-term multiplication on both sides. The bijection could be counter-intuitive at first: $A$ is “much bigger” than $A/\varpi A$, but the inverse limits along the respective $p$-th power maps “reduce the gap” between them, and finally they are in a multiplicative bijection after the limits!)

**Proof:**
**(1)** Since $|p|\le|\varpi|$, we have $p\in\varpi A$, so $A/\varpi A$ has characteristic $p$. Its Frobenius is a ring homomorphism, hence the compatibility conditions defining $A^\flat$ are preserved by coordinatewise addition and multiplication. Thus $A^\flat$ is a ring of characteristic $p$.

Its Frobenius map $(x_i)\mapsto(x_i^p)$ has inverse $(x_i)\mapsto(x_{i+1})$, since $x_{i+1}^p=x_i$. Therefore $A^\flat$ is perfect.

**(2)** Put $r=|\varpi|$. For $a,b\in A$, suppose $|a|\leq|b|$, the binomial theorem gives
$$
a^{p}=((a-b)+b)^{p}=(a-b)^{p}+b^{p}+\sum_{i=1}^{p-1}\binom{p}{i} (a-b)^{i}b^{p-i}
$$
since $a,b\in A$, we have $|a-b|,|b|\leq 1$, and since $p\mid \binom{p}{i}$, we get
$$
\left| \binom{p}{i} (a-b)^{i}b^{p-i} \right|\leq  |p| \cdot |a-b|\qquad(i=1,\dots,p-1)
$$
therefore, by the ultrametric inequality,
$$
|a^p-b^p|\le\max\{|p||a-b|,\ |a-b|^p\}.
$$
Consequently, if $|a-b|\le r$, induction and $r=|\varpi|\geq p$ gives
$$
|a^{p^n}-b^{p^n}|\le r^{n+1}\qquad(n\ge0).
$$
We call this estimate *the key lemma.

For surjectivity, take $x=(x_i)\in A^\flat$ and choose lifts $a_i\in A$ of $x_i$. For each $i$, set $b_{i,n}=a_{i+n}^{p^n}$. Since $|a_{i+n+1}^p-a_{i+n}|\le r$, the key lemma gives $|b_{i,n+1}-b_{i,n}|\le r^{n+1}$. By the ultrametric inequality, $(b_{i,n})_n$ is Cauchy. Completeness of $A$ gives
$$
y_i:=\lim_{n\to\infty}a_{i+n}^{p^n}\in A.
$$
We call this equality *the important formula*.

Every $b_{i,n}$ reduces to $x_i$, so $y_i\bmod\varpi=x_i$. Moreover,
$$
y_{i+1}^p=\lim_{n\to\infty}a_{i+n+1}^{p^{n+1}}=y_i.
$$
Thus $(y_i)\in\varprojlim_p A$ and $f((y_i))=x$.

For injectivity, suppose $f((y_i))=f((z_i))$. Then $|y_j-z_j|\le r$ for every $j$. For any $i,n\ge0$, the key lemma give
$$
|y_i-z_i|
=|y_{i+n}^{p^n}-z_{i+n}^{p^n}|
\le r^{n+1}.
$$
Letting $n\to\infty$ yields $y_i=z_i$ for every $i$. Hence $f$ is bijective.
___

For each $x\in A^\flat$, write $f^{-1}(x)=(y_0,y_1,\ldots)$. Define $x^\#\in A$ to be $y_0$, namely the first coordinate in $f^{-1}(x)$. Thus we obtain a map $f^\#:A^\flat\longrightarrow A$ given by $x\mapsto x^\#$.

>[!remark] Remark
>Fix the residue characteristic $p$. The construction $A\mapsto A^\flat$ defines a functor from valuation rings of perfectoid fields, with continuous ring homomorphisms, to perfect rings of characteristic $p$. Using the identification $A^\flat\cong\varprojlim_p A$, a morphism $\phi:A\to B$ induces $\phi^\flat((y_i))=(\phi(y_i))$. This preserves multiplication and, by continuity, addition, since
>$$
>(y+z)_i=\lim_{n\to\infty}(y_{i+n}+z_{i+n})^{p^n}.
>$$
>The construction is canonically independent of the choice of pseudo-uniformizer.
>
>The maps $\#:A^\flat\to A$ satisfy $\phi(x^\#)=(\phi^\flat(x))^\#$, so they form a natural transformation after passing to multiplicative monoids. In mixed characteristic, $\#$ is not a ring homomorphism. In characteristic $p$, it is a ring isomorphism.

___

> [!problem] Problem 3
> (1) Given $x\in K^\times$, show that there exists $y\in K^\times$ such that $|y^p|=|x|$. (This tells us that $\Gamma=|K^\times|$ is not only non-discrete but “$p$-divisible”.)
>
> (2) Prove that there exists an element $\varpi^\flat\in A^\flat$ such that $|(\varpi^\flat)^\#|=|\varpi|$.
>
> (3) Consider the following localization of $A^\flat$ (with respect to the multiplicative set consisting of powers of $\varpi^\flat$)
> $$
> K^\flat:=A^\flat[1/\varpi^\flat].
> $$
> Show that the map $f^\#$ extends to a multiplicative map $K^\flat\to K$, still to be called $f^\#$. Concretely, construct this map by extending the bijection $f^{-1}$ (where $f$ is as in #2.(2)) to a multiplicative bijection $K^\flat\to\varprojlim_p K$ and projecting onto the first component. Deduce that $K^\flat$ is a field of characteristic $p$.
>
> (4) Show that the function
> $$
> |\cdot|:K^\flat\longrightarrow\mathbb{R}_{\ge0},\qquad |y|:=|f^\#(y)|
> $$
> is a valuation on $K^\flat$ and that $A^\flat$ is the valuation ring for $|\cdot|$.

**Proof:**
Put $r=|\varpi|$.

**(1)** If $\operatorname{char}(K)=p$, (P3) says that Frobenius on $A$ is surjective. Applying this to $x$ gives the result.

Suppose $\operatorname{char}(K)=0$. (P2) gives $t\in K$ with $|p|<|t|^p<1$. Choose $m\in\mathbb{Z}$ such that $u=x/t^{mp}$ satisfies $|t|^p<|u|\le1$. By (P3), there is $v\in A$ with $v^p-u\in pA$. Since $|v^p-u|\le|p|<|u|$, we have $|v|^p=|u|$. Thus $y=t^mv$ satisfies $|y|^p=|x|$.

**(2)** By (1), choose $a_1\in A$ with $|a_1|^p=r$. Surjectivity of Frobenius on $A/\varpi A$ allows us to choose $a_{n+1}\in A$ with $a_{n+1}^p\equiv a_n\pmod{\varpi}$.

Inductively, $|a_n|=r^{1/p^n}>r$: indeed, $|a_{n+1}^p-a_n|\le r<|a_n|$ implies $|a_{n+1}|^p=|a_n|$. Hence
$$
\varpi^\flat=(0,\overline{a_1},\overline{a_2},\ldots)\in A^\flat.
$$
By the important formula (see Problem 2.(2)),
$$
(\varpi^\flat)^\#=\lim_{n\to\infty}a_n^{p^n}.
$$
We have $|a_n^{p^n}|=r$, so $|(\varpi^\flat)^\#|=r=|\varpi|$.

**(3)** Write $w=\varpi^\flat$ and $f^{-1}(w)=(w_i)$. Then $|w_i|=r^{1/p^i}$, so every $w_i$ is nonzero.

The multiplicative bijection $f^{-1}:A^\flat\to\varprojlim_p A$ shows that $A^\flat$ is a domain: a nonzero compatible sequence has every coordinate nonzero, and coordinatewise products of nonzero sequences are nonzero.

Define
$$
g:K^\flat\longrightarrow\varprojlim_p K,\qquad
g(a/w^m)=\left(\frac{a_i}{w_i^m}\right)_{i\ge0},
\quad f^{-1}(a)=(a_i).
$$
This is well-defined, multiplicative, and injective, by clearing denominators and using the injectivity of $f^{-1}$.

For surjectivity, take $(z_i)\in\varprojlim_p K$. Choose $m\ge0$ with $|z_0|r^m\le1$. Since
$$
|z_iw_i^m|=(|z_0|r^m)^{1/p^i}\le1,
$$
the sequence $(z_iw_i^m)$ lies in $\varprojlim_p A$. If $f^{-1}(a)=(z_iw_i^m)$, then $g(a/w^m)=(z_i)$.

Composing $g$ with the first projection gives the desired multiplicative map, explicitly
$$
(a/w^m)^\#=\frac{a^\#}{(w^\#)^m}.
$$
Every nonzero sequence in $\varprojlim_p K$ has the coordinatewise inverse $(z_i^{-1})$. By the multiplicative bijection $g$, every nonzero element of $K^\flat$ is invertible. Thus $K^\flat$ is a field, and its characteristic is $p$ because it contains $A^\flat$.

**(4)** Multiplicativity and $|x|=0\iff x=0$ follow from $g$. To prove the ultrametric inequality, first take $a,b\in A^\flat$, with $f^{-1}(a)=(a_i)$ and $f^{-1}(b)=(b_i)$. The lifting formula gives
$$
(a+b)^\#=\lim_{n\to\infty}(a_n+b_n)^{p^n}.
$$
Since $|a_n|^{p^n}=|a^\#|$ and $|b_n|^{p^n}=|b^\#|$, we obtain
$$
|(a_n+b_n)^{p^n}|\le\max\{|a^\#|,|b^\#|\}.
$$
Taking limits yields $|a+b|\le\max\{|a|,|b|\}$. For arbitrary elements of $K^\flat$, multiply both by a common power of $w$ to reduce to this case.

Finally, if $g(x)=(z_i)$, then $|z_i|=|z_0|^{1/p^i}$. Consequently,
$$
|x|\le1
\iff z_i\in A\text{ for every }i
\iff x\in A^\flat.
$$
Thus $A^\flat$ is the valuation ring of $K^\flat$.
___

