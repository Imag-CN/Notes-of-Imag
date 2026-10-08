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



