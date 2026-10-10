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

> [!problem] [MAR] 2.5.13
> Let $\mathcal{L}=\{s\}$, where $s$ is a unary function symbol. Let $T$ be the $\mathcal{L}$-theory that asserts that $s$ is a bijection with no cycles (i.e., $s^{(n)}(x)\neq x$ for $n=1,2,\ldots$). For what cardinals $\kappa$ is $T$ $\kappa$-categorical?

**Proof:**
Since $s$ is a bijection with no cycles, for every $a$ the orbit
$$
\{s^{(n)}(a):n\in\mathbb{Z}\}
$$
is isomorphic to $(\mathbb{Z},n\mapsto n+1)$. Thus every model of $T$ is a disjoint union of copies of $\mathbb{Z}$.

Hence a model is determined up to isomorphism by the number of its orbits.

If $\kappa>\aleph_0$, then the model must have $\kappa$ copies of orbits, thus is unique up to isomorphism.

If $\kappa=\aleph_0$, a model may have $1,2,\ldots$, or $\aleph_0$ many orbits, giving nonisomorphic countable models. Thus $T$ is not $\aleph_0$-categorical.

Therefore $T$ is $\kappa$-categorical for only cardinal $\kappa>\aleph_{0}$.
___

> [!problem] [MAR] 2.5.15
> We say that $T$ has a $\forall\exists$-axiomatization if it can be axiomatized by sentences of the form $\forall v_1\cdots\forall v_n\exists w_1\cdots\exists w_m\,\phi(\overline{v},\overline{w})$ where $\phi$ is a quantifier-free formula.
>
> a) Suppose that $T$ has a $\forall\exists$-axiomatization, $(I,<)$ is a linear order, and $(\mathcal{M}_i:i\in I)$ is a chain of models of $T$. Show that $\bigcup\mathcal{M}_i$ is a model of $T$.
>
> We will show that the converse also holds. Suppose that whenever $(\mathcal{M}_i:i\in I)$ is a chain of models of $T$, then $\bigcup\mathcal{M}_i\models T$. Let $\Gamma=\{\phi:\phi\text{ is a }\forall\exists\text{-sentence and }T\models\phi\}$. Let $\mathcal{M}\models\Gamma$. We will show that $\mathcal{M}\models T$.
>
> b) Show that there is $\mathcal{N}\models T$ such that if $\psi$ is an $\exists\forall$-sentence and $\mathcal{M}\models\psi$, then $\mathcal{N}\models\psi$.
>
> c) Show that there is $\mathcal{N}'\supseteq\mathcal{M}$ with $\mathcal{N}'\equiv\mathcal{N}$.
>
> d) Show that there is $\mathcal{M}'\supseteq\mathcal{N}'$ such that $\mathcal{M}\preceq\mathcal{M}'$.
>
> e) Iterate the constructions from c) and d) to build a chain of structures
> $$
> \mathcal{M}=\mathcal{M}_0\subseteq\mathcal{N}_1\subseteq\mathcal{M}_1\subseteq\mathcal{N}_2\cdots
> $$
> such that $\mathcal{M}_i\preceq\mathcal{M}_{i+1}$ for $i=0,1,\ldots$ and each $\mathcal{N}_i\preceq\mathcal{N}_{i+1}$. Let $\mathcal{M}^*=\bigcup\mathcal{M}_i=\bigcup\mathcal{N}_i$. Show that $\mathcal{M}^*\models T$ and $\mathcal{M}\preceq\mathcal{M}^*$.
>
> f) Conclude that $T$ is $\forall\exists$-axiomatizable.

**Proof:**
**(a)** Let $\mathcal{M}=\bigcup_{i\in I}\mathcal{M}_i$. Suppose
$$
\forall\overline{v}\exists\overline{w}\,\phi(\overline{v},\overline{w})
$$
is an axiom of $T$, where $\phi$ is quantifier-free. Given $\overline{a}\in M$, choose $i$ such that $\overline{a}\in M_i$. Since $\mathcal{M}_i\models T$, there is $\overline{b}\in M_i$ such that
$$
\mathcal{M}_i\models\phi(\overline{a},\overline{b}).
$$
Quantifier-free formulas are preserved under substructures, so
$$
\mathcal{M}\models\phi(\overline{a},\overline{b}).
$$
Thus $\mathcal{M}\models T$.

**(b)** Let $\Sigma$ be the set of all $\exists\forall$-sentences true in $\mathcal{M}$. We claim that $T\cup\Sigma$ is consistent. Otherwise, by compactness there are $\psi_1,\ldots,\psi_n\in\Sigma$ such that
$$
T\models\neg(\psi_1\land\cdots\land\psi_n).
$$
The conjunction $\psi_1\land\cdots\land\psi_n$ is equivalent to an $\exists\forall$-sentence, so its negation is equivalent to a $\forall\exists$-sentence. Hence
$$
\neg(\psi_1\land\cdots\land\psi_n)\in\Gamma.
$$
But $\mathcal{M}\models\Gamma$ and $\mathcal{M}\models\psi_1\land\cdots\land\psi_n$, a contradiction.

Therefore $T\cup\Sigma$ has a model $\mathcal{N}$. Then $\mathcal{N}\models T$, and every $\exists\forall$-sentence true in $\mathcal{M}$ is true in $\mathcal{N}$.

**(c)** Expand the language by constants $c_a$ for $a\in M$. Let $\operatorname{Diag}(\mathcal{M})$ be the quantifier-free diagram of $\mathcal{M}$. We claim that
$$
\operatorname{Th}(\mathcal{N})\cup\operatorname{Diag}(\mathcal{M})
$$
is consistent.

Otherwise, some quantifier-free formula $\theta(\overline{c})$ from the diagram would give
$$
\operatorname{Th}(\mathcal{N})\models\neg\exists\overline{x}\,\theta(\overline{x}).
$$
Thus $\mathcal{N}\models\forall\overline{x}\neg\theta(\overline{x})$. But its negation $\exists\overline{x}\theta(\overline{x})$ is an $\exists\forall$-sentence true in $\mathcal{M}$, hence true in $\mathcal{N}$ by (b), a contradiction.

Therefore there is $\mathcal{N}'\equiv\mathcal{N}$ containing an isomorphic copy of $\mathcal{M}$. Identifying this copy with $\mathcal{M}$, we have $\mathcal{N}'\supseteq\mathcal{M}$.

**(d)** Since $\mathcal{M}\subseteq\mathcal{N}'$, apply the standard elementary-extension lemma: there is an elementary extension $\mathcal{M}'\succeq\mathcal{M}$ containing $\mathcal{N}'$. Thus
$$
\mathcal{M}\preceq\mathcal{M}'\quad\text{and}\quad\mathcal{N}'\subseteq\mathcal{M}'.
$$

**(e)** Repeating (c) and (d), we obtain
$$
\mathcal{M}=\mathcal{M}_0\subseteq\mathcal{N}_1\subseteq\mathcal{M}_1\subseteq\mathcal{N}_2\subseteq\cdots
$$
with $\mathcal{M}_i\preceq\mathcal{M}_{i+1}$ and $\mathcal{N}_i\preceq\mathcal{N}_{i+1}$.

Let
$$
\mathcal{M}^*=\bigcup_i\mathcal{M}_i=\bigcup_i\mathcal{N}_i.
$$
By the elementary chain theorem,
$$
\mathcal{M}=\mathcal{M}_0\preceq\mathcal{M}^*.
$$
Also each $\mathcal{N}_i\models T$. By the hypothesis that unions of chains of models of $T$ are models of $T$,
$$
\mathcal{M}^*=\bigcup_i\mathcal{N}_i\models T.
$$

**(f)** Since $\mathcal{M}\preceq\mathcal{M}^*$ and $\mathcal{M}^*\models T$, we have $\mathcal{M}\models T$. Thus every model of $\Gamma$ is a model of $T$, so
$$
\Gamma\models T.
$$
By compactness, every sentence of $T$ follows from finitely many sentences of $\Gamma$. Hence $T$ is axiomatized by the $\forall\exists$-sentences in $\Gamma$, and therefore $T$ is $\forall\exists$-axiomatizable.
___

> [!problem] [MAR] 2.5.17
> We say that $\mathcal{M}\models T$ is *existentially closed* if whenever $\mathcal{N}\models T$, $\mathcal{N}\supseteq\mathcal{M}$, and $\mathcal{N}\models\exists\overline{v}\,\phi(\overline{v},\overline{a})$, where $\overline{a}\in M$ and $\phi$ is quantifier-free, then $\mathcal{M}\models\exists\overline{v}\,\phi(\overline{v},\overline{a})$.
>
> a) Show that if $T$ is $\forall\exists$-axiomatizable, then $T$ has an existentially closed model. Indeed, if $\mathcal{M}\models T$, there is $\mathcal{N}\supseteq\mathcal{M}$ existentially closed with $|N|=|M|+|\mathcal{L}|+\aleph_0$.
>
> b) Suppose that $T$ has an infinite nonexistentially closed model. Prove that $T$ has a nonexistentially closed model of cardinal $\kappa$ for any infinite cardinal $\kappa\geq|\mathcal{L}|$.
>
> c) Suppose that $T$ is $\kappa$-categorical for some infinite $\kappa\geq|\mathcal{L}|$ and axiomatized by $\forall\exists$-sentences. Prove that all models of $T$ are existentially closed. Conclude that every algebraically closed field is existentially closed.

**Proof:**
**(a)** Let $\lambda=|M|+|\mathcal{L}|+\aleph_0$. Starting with $\mathcal{M}_0=\mathcal{M}$, construct a chain
$$
\mathcal{M}_0\subseteq\mathcal{M}_1\subseteq\cdots
$$
as follows.

For every existential formula $\exists\overline{v}\,\phi(\overline{v},\overline{a})$ with $\overline{a}\in M_i$ that is realized in some extension $\mathcal{N}\supseteq\mathcal{M}_i$, $\mathcal{N}\models T$, add a witness to $\mathcal{M}_{i+1}$. Since there are at most $\lambda$ such formulas, we may arrange $|M_{i+1}|\leq\lambda$.

Because $T$ is $\forall\exists$-axiomatizable, unions of chains of models of $T$ are again models of $T$. Repeating this construction $\omega$ times and taking
$$
\mathcal{N}=\bigcup_{i<\omega}\mathcal{M}_i,
$$
we obtain $\mathcal{N}\models T$, $|N|=\lambda$, and every existential formula over $N$ that can be realized in an extension is already realized in $N$. Thus $\mathcal{N}$ is existentially closed.

**(b)** Let $\mathcal{M}\subseteq\mathcal{N}$ be models of $T$ witnessing that $\mathcal{M}$ is not existentially closed. Thus for some quantifier-free $\phi$ and $\overline{a}\in M$,
$$
\mathcal{N}\models\exists\overline{v}\,\phi(\overline{v},\overline{a}),
\qquad
\mathcal{M}\not\models\exists\overline{v}\,\phi(\overline{v},\overline{a}).
$$

Expand the language by a unary predicate $P$ interpreted as $M$ in $\mathcal{N}$. By the Upward Löwenheim-Skolem Theorem, for any infinite $\kappa\geq|\mathcal{L}|$, there is
$$
(\mathcal{N}',P')\equiv(\mathcal{N},M)
$$
of cardinality $\kappa$, with $|P'|=\kappa$.

Let $\mathcal{M}'$ be the substructure with universe $P'$. By elementarity, $\mathcal{M}'\models T$, $\mathcal{N}'\models T$, and the same existential formula is realized in $\mathcal{N}'$ but not in $\mathcal{M}'$. Hence $\mathcal{M}'$ is not existentially closed and $|M'|=\kappa$.

**(c)** Suppose some $\mathcal{M}\models T$ is not existentially closed. By (b), $T$ has a nonexistentially closed model $\mathcal{M}_0$ of cardinality $\kappa$.

By (a), $\mathcal{M}_0$ has an existentially closed extension $\mathcal{N}$. By choosing the construction in (a) with cardinality $\kappa$, we may take $|N|=\kappa$.

Thus $T$ has two models of cardinality $\kappa$, one existentially closed and one not. They cannot be isomorphic, contradicting $\kappa$-categoricity. Therefore every model of $T$ is existentially closed.

Finally, the theory $\mathrm{ACF}_p$ of algebraically closed fields of fixed characteristic $p$ is $\kappa$-categorical for every uncountable $\kappa$ and is axiomatized by $\forall\exists$-sentences. Hence every algebraically closed field is existentially closed among fields of the same characteristic.
___

> [!problem] [MAR] 2.8.25
> Let $\mathcal{L}_3=\{<,c_0,c_1,\ldots\}$, where $c_0,c_1,\ldots$ are constant symbols. Let $T_3$ be the theory of dense linear orders with sentences added asserting $c_0<c_1<\cdots$.
>
> a) Show that $T_3$ has exactly three countable models up to isomorphism.
>
> b) Prove the following two general results and use them to prove that $T_3$ is complete.
>
> i) For any language $\mathcal{L}$, two $\mathcal{L}$-structures $\mathcal{M}$ and $\mathcal{N}$ are elementarily equivalent if and only if they are elementarily equivalent for every finite sublanguage.
>
> ii) If $\mathcal{L}$ is countable, $T$ is an $\mathcal{L}$-theory with no finite models, and any two countable models of $T$ are elementarily equivalent, then $T$ is complete.
>
> c) Let $\mathcal{L}_4=\mathcal{L}_3\cup\{P\}$, where $P$ is a unary predicate. Let $T_4$ be $T_3$ with the added sentences
> $$
> \forall x\forall y(x<y\to\exists z\exists w(x<z<y\land x<w<y\land P(z)\land\neg P(w))).
> $$
> In other words, $P$ is a dense-codense subset. Show that $T_4$ is a complete theory with exactly four countable models.
>
> d) Generalize c) to give examples of complete theories with exactly $n$ countable models for $n=5,6,\ldots$.

**Proof:**
**(a)** Let $\mathcal{M}\models T_3$. Since $M$ is a countable dense linear order without endpoints, the isomorphism type is determined by the position of the increasing sequence
$$
c_0<c_1<c_2<\cdots.
$$
There are exactly three possibilities:

1. $\{c_n:n\in\mathbb{N}\}$ has no upper bound.
2. It has upper bounds but no least upper bound.
3. It has a least upper bound.

In each case, any two countable models are isomorphic by the usual back-and-forth argument for dense linear orders, sending each $c_n$ to the corresponding $c_n$.

The three cases are pairwise nonisomorphic, so $T_3$ has exactly three countable models up to isomorphism.

**(b)**
(i) The forward direction is immediate.

Conversely, suppose $\mathcal{M}$ and $\mathcal{N}$ are elementarily equivalent in every finite sublanguage. Any $\mathcal{L}$-sentence $\phi$ uses only finitely many symbols, so it belongs to some finite sublanguage $\mathcal{L}_0\subseteq\mathcal{L}$. Hence
$$
\mathcal{M}\models\phi\iff\mathcal{N}\models\phi.
$$
Thus $\mathcal{M}\equiv\mathcal{N}$.

(ii) Suppose $T$ is not complete. Then there is a sentence $\phi$ and models
$$
\mathcal{M},\mathcal{N}\models T
$$
such that
$$
\mathcal{M}\models\phi,\qquad\mathcal{N}\models\neg\phi.
$$
By the Downward Löwenheim-Skolem Theorem, each has a countable elementary submodel. Since $T$ has no finite models, these submodels are countably infinite. Thus there are countable models $\mathcal{M}_0,\mathcal{N}_0\models T$ with
$$
\mathcal{M}_0\models\phi,\qquad\mathcal{N}_0\models\neg\phi,
$$
contradicting the assumption that any two countable models of $T$ are elementarily equivalent. Hence $T$ is complete.

Now let $\mathcal{M},\mathcal{N}\models T_3$ be countable. For any finite sublanguage, only finitely many constants $c_n$ occur. The corresponding finite ordered configurations are the same in both structures, so by back-and-forth the reducts are isomorphic. Hence, by (i),
$$
\mathcal{M}\equiv\mathcal{N}.
$$
Therefore, by (ii), $T_3$ is complete.

**(c)** In a countable model of $T_4$, the first two cases from (a) remain unchanged. In the third case, let $a$ be the least upper bound of $\{c_n:n\in\mathbb{N}\}$. There are now two possibilities:
$$
P(a)
\qquad\text{or}\qquad
\neg P(a).
$$
Thus there are exactly four possible countable isomorphism types.

Each type is unique up to isomorphism by a back-and-forth argument preserving $<$, the constants $c_n$, and $P$. The density and codensity of $P$ guarantee that whenever a new point is chosen, a matching point of the same $P$-status can be found in the corresponding interval.

To prove completeness, let $\mathcal{M},\mathcal{N}\models T_4$ be countable. In any finite sublanguage, only finitely many constants occur. By back-and-forth, the corresponding reducts are isomorphic, since $P$ and its complement are both dense. Hence they are elementarily equivalent in every finite sublanguage. By (b)(i),
$$
\mathcal{M}\equiv\mathcal{N},
$$
and by (b)(ii), $T_4$ is complete.

Therefore $T_4$ is complete and has exactly four countable models.

**(d)** Let $n\geq5$ and set $m=n-2$. Expand $\mathcal{L}_3$ by unary predicates
$$
P_1,\ldots,P_m,
$$
and require that they partition the universe and that each $P_i$ is dense:
$$
\forall x\,\bigvee_{i=1}^m P_i(x),
$$
$$
\forall x\,\bigwedge_{i\neq j}\neg(P_i(x)\land P_j(x)),
$$
and, for each $i$,
$$
\forall x\forall y\,(x<y\to\exists z\,(x<z<y\land P_i(z))).
$$

There are again two cases in which $\{c_n:n\in\mathbb{N}\}$ has no least upper bound, and if it has a least upper bound $a$, then $a$ belongs to exactly one of the $m$ predicates.

Hence the number of countable models is
$$
2+m=2+(n-2)=n.
$$
The same finite-sublanguage back-and-forth argument as in (c) shows that the theory is complete.

Thus for every $n\geq5$ there is a complete theory with exactly $n$ countable models.