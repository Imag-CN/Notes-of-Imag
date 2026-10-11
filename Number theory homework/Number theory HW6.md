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
Such an element is often called a “**pseudo-uniformizer**” as it plays a similar role as a uniformizer for a DVR. If $\operatorname{char}(K)=0$ then one can simply take $\varpi=p$. However if $\operatorname{char}(K)=p$ then one should make a different choice. (E.g., for the completion of $\mathbb{F}_p((t^{1/p^\infty}))$ one can take $\varpi=t$.) In either case, (P3) implies that the $p$-th power map induces a surjection $A/\varpi A\to A/\varpi A$ (exercise).


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

Its Frobenius $F((x_i))=(x_i^p)$ has inverse $S((x_i))=(x_{i+1})$, since $x_{i+1}^p=x_i$. Therefore $A^\flat$ is perfect.

**(2)** Put $r=|\varpi|\in(0,1)$. For $a,b\in A$, the binomial theorem gives
$$
|a^p-b^p|\le\max\{|p||a-b|,\ |a-b|^p\}.
$$
Consequently, if $|a-b|\le r$, induction gives
$$
|a^{p^n}-b^{p^n}|\le r^{n+1}\qquad(n\ge0).
$$

For surjectivity, take $x=(x_i)\in A^\flat$ and choose lifts $a_i\in A$ of $x_i$. For each $i$, set $b_{i,n}=a_{i+n}^{p^n}$. Since $|a_{i+n+1}^p-a_{i+n}|\le r$, the estimate gives $|b_{i,n+1}-b_{i,n}|\le r^{n+1}$. By the ultrametric inequality, $(b_{i,n})_n$ is Cauchy. Completeness and closedness of $A$ give
$$
y_i:=\lim_{n\to\infty}a_{i+n}^{p^n}\in A.
$$
Every $b_{i,n}$ reduces to $x_i$, so $y_i\bmod\varpi=x_i$. Moreover,
$$
y_{i+1}^p=\lim_{n\to\infty}a_{i+n+1}^{p^{n+1}}=y_i.
$$
Thus $(y_i)\in\varprojlim_p A$ and $f((y_i))=x$.

For injectivity, suppose $f((y_i))=f((z_i))$. Then $|y_j-z_j|\le r$ for every $j$. For any $i,n\ge0$, compatibility and the estimate give
$$
|y_i-z_i|
=|y_{i+n}^{p^n}-z_{i+n}^{p^n}|
\le r^{n+1}.
$$
Letting $n\to\infty$ yields $y_i=z_i$ for every $i$. Hence $f$ is bijective.
___