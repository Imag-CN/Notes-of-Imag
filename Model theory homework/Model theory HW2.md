___

> [!problem] [MAR] 2.5.1
> We say that an ordered group $(G,+,<)$ is *Archimedean* if for all $x,y\in G$ with $x,y>0$ there is an integer $m$ such that $|x|<m|y|$. Show that there are non-Archimedean fields elementarily equivalent to the field of real numbers.

**Proof:**
Expand the language of ordered fields by adding a new constant symbol $c$. Consider the theory
$$
T=\operatorname{Th}(\mathbb{R})\cup\{c>n:n\in\mathbb{N}\}.
$$

Every finite subset of $T$ is satisfiable in $\mathbb{R}$: indeed, only finitely many conditions $c>n$ occur, so we may interpret $c$ as a sufficiently large real number.

By the Compactness Theorem, $T$ has a model $(K,c)$. Since $K\models\operatorname{Th}(\mathbb{R})$, we have $K\equiv\mathbb{R}$.

On the other hand, $c>n$ for every $n\in\mathbb{N}$. Taking $x=c$ and $y=1$, we have
$$
|x|=c>m=m|y|
$$
for every positive integer $m$. Thus $K$ is non-Archimedean.

>[!remark] Remark
> If we take the elementary diagram of $\mathbb{R}$, we can actually make $K$ an extension of $\mathbb{R}$.

___

> [!problem] [MAR] 2.5.2
> Suppose that $T$ has arbitrarily large finite models. Show that $T$ has an infinite model.

**Proof:**
For each $n\geq 1$, let $\varphi_n$ be the sentence asserting that there are at least $n$ distinct elements:
$$
\varphi_n:=\exists x_1\cdots\exists x_n\bigwedge_{i\neq j}x_i\neq x_j.
$$
Consider
$$
T'=T\cup\{\varphi_n:n\geq 1\}.
$$

Every finite subset of $T'$ contains only finitely many $\varphi_n$, say up to $\varphi_N$. Since $T$ has arbitrarily large finite models, it has a model of size at least $N$, which satisfies this finite subset.

Thus every finite subset of $T'$ is satisfiable. By the Compactness Theorem, $T'$ has a model $\mathcal{M}$. Since $\mathcal{M}\models\varphi_n$ for every $n$, $\mathcal{M}$ is infinite. Since $\mathcal{M}\models T$, it is an infinite model of $T$.
___

> [!problem] [MAR] 2.5.5
> Let $\mathcal{L}=\{E\}$ where $E$ is a binary relation symbol. Let $T$ be the $\mathcal{L}$-theory of an equivalence relation with infinitely many infinite classes.
>
> a) Write axioms for $T$.
>
> b) How many models of $T$ are there of cardinality $\aleph_0$? $\aleph_1$? $\aleph_2$? $\aleph_{\omega_1}$?
>
> c) Is $T$ complete?

**Proof:**
**(a)** Take the usual axioms for an equivalence relation, together with the following schemes.

For each $n\geq1$, every equivalence class has at least $n$ elements:
$$
\forall x\,\exists y_1,\ldots,y_n\left(\bigwedge_i E(x,y_i)\land\bigwedge_{i\neq j}y_i\neq y_j\right).
$$

For each $n\geq1$, there are at least $n$ distinct equivalence classes:
$$
\exists x_1,\ldots,x_n\bigwedge_{i\neq j}\neg E(x_i,x_j).
$$

Thus every class is infinite and there are infinitely many classes.

**(b)** A model is determined up to isomorphism by the number of equivalence classes of each infinite cardinality.

For cardinality $\aleph_0$, every class is countable and there are countably many classes, so there is exactly $1$ model up to isomorphism.

For cardinality $\aleph_1$, classes have size $\aleph_0$ or $\aleph_1$, and their multiplicities are among the finite cardinals, $\aleph_0$, and $\aleph_1$. Hence there are exactly $\aleph_0$ isomorphism types.

The same argument for $\aleph_2$, with possible class sizes $\aleph_0,\aleph_1,\aleph_2$, again gives exactly $\aleph_0$ isomorphism types.

For cardinality $\aleph_{\omega_1}$, there are $\aleph_1$ possible infinite class sizes, so there are at most
$$
(\aleph_1)^{\aleph_1}=2^{\aleph_1}
$$
isomorphism types. Conversely, for each $S\subseteq\omega_1$, take countably many countable classes, one class of size $\aleph_{\omega_1}$, and one class of size $\aleph_{\alpha+1}$ for each $\alpha\in S$. These models are pairwise nonisomorphic, giving $2^{\aleph_1}$ types.

Therefore the answers are
$$
1,\qquad\aleph_0,\qquad\aleph_0,\qquad2^{\aleph_1}.
$$

**(c)** Yes. By (b), $T$ is $\aleph_{0}$-categorical, $T$ and has no finite models.
___

> [!problem] [MAR] 2.5.6
> (Skolem's Paradox) Let ZFC be the Zermelo–Fraenkel axioms for set theory with the Axiom of Choice. Show that there is a countable model $\mathcal{M}$ of ZFC. How do you explain the fact that $\mathcal{M}\models$ "there is an uncountable set"?

**Proof:**
Assume ZFC is consistent, so it has a model $\mathcal{N}$. Since the language of set theory is countable, the Downward Löwenheim–Skolem Theorem gives a countable elementary substructure
$$
\mathcal{M}\preccurlyeq\mathcal{N}.
$$
Hence $\mathcal{M}\models\mathrm{ZFC}$.

There is no contradiction with
$$
\mathcal{M}\models\text{"there is an uncountable set."}
$$
Indeed, suppose
$$
\mathcal{M}\models\text{"$X$ is uncountable."}
$$
The set of elements that $\mathcal{M}$ regards as belonging to $X$ is
$$
X^{\mathcal{M}}=\{x\in M:\mathcal{M}\models x\in X\}.
$$
Since $X^{\mathcal{M}}\subseteq M$ and $M$ is countable externally, $X^{\mathcal{M}}$ is countable externally. However, $\mathcal{M}$ contains no bijection that it recognizes as a bijection between $\mathbb{N}^{\mathcal{M}}$ and $X$. Thus $X$ is uncountable inside $\mathcal{M}$ but countable externally.
___

> [!problem] [MAR] 2.5.9
> Suppose that $\mathcal{M}_0\subset\mathcal{M}_1\subset\mathcal{M}_2$, $\mathcal{M}_0\preceq\mathcal{M}_2$, and $\mathcal{M}_1\preceq\mathcal{M}_2$. Show that $\mathcal{M}_0\preceq\mathcal{M}_1$.

**Proof:**
Let $\phi(\overline{x})$ be any formula and $\overline{a}\in M_0$. Since $\mathcal{M}_0\preceq\mathcal{M}_2$,
$$
\mathcal{M}_0\models\phi(\overline{a})
\iff
\mathcal{M}_2\models\phi(\overline{a}).
$$
Since $\mathcal{M}_1\preceq\mathcal{M}_2$ and $\overline{a}\in M_0\subseteq M_1$,
$$
\mathcal{M}_1\models\phi(\overline{a})
\iff
\mathcal{M}_2\models\phi(\overline{a}).
$$
Therefore
$$
\mathcal{M}_0\models\phi(\overline{a})
\iff
\mathcal{M}_1\models\phi(\overline{a}),
$$
so $\mathcal{M}_0\preceq\mathcal{M}_1$.
___

