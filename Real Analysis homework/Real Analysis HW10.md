___

>[!problem] [SHE] 6D.2
>Suppose $\varphi$ is a linear functional on a vector space $V$. Prove that if $U$ is a subspace of $V$ such that $\text{null } \varphi \subset U$, then $U = \text{null } \varphi$ or $U = V$.

**Proof:**
Suppose $\varphi$ is non-zero (otherwise $\operatorname{null}\varphi=U=V$). Since $\varphi \ne 0$, we can pick $v_0 \in V$ with $\varphi(v_0) \ne 0$. Any $v \in V$ can be written as
$$
v = \big(v - \frac{\varphi(v)}{\varphi(v_0)}v_0\big) + \frac{\varphi(v)}{\varphi(v_0)}v_0,
$$
where the first term is in $\text{null }\varphi$, thus $V = \text{null }\varphi \oplus F v_0$ (direct sum).

Now take $u \in U \setminus \text{null }\varphi$ (if such $u$ exists). Then $\varphi(u) \ne 0$, and the same decomposition shows $v_0 \in U$ (since $v_0$ is a scalar multiple of $u$ plus an element of $\text{null }\varphi \subset U$). But then $F v_0 \subset U$, and since $\text{null }\varphi \subset U$, we get $V = \text{null }\varphi \oplus F v_0 \subset U$, hence $U = V$.

Therefore either $U$ contains no vector outside $\text{null }\varphi$, so $U = \text{null }\varphi$; or it does contain such a vector, and then $U = V$.
___

>[!problem] [SHE] 6D.11
>Show that the collection $\mathcal{A} = \{k\mathbf{Z} : k = 2, 3, 4, \ldots\}$ of subsets of $\mathbf{Z}$ satisfies the hypothesis of Zorn’s Lemma.

**Proof:**
We need to show that the collection $\mathcal{A} = \{k\mathbb{Z} : k = 2,3,4,\dots\}$ with the order $k\mathbb{Z} \preceq m\mathbb{Z} \iff m\mathbb{Z} \subseteq k\mathbb{Z}$ satisfies the hypothesis of Zorn’s Lemma: every chain in $\mathcal{A}$ has an upper bound in $\mathcal{A}$.

Let $\mathcal{C}$ be a chain in $\mathcal{A}$. Define
$$
S = \{k \ge 2 : k\mathbb{Z} \in \mathcal{C}\}.
$$
Since $\mathcal{C}$ is a chain, for any $k,m \in S$, either $k \mid m$ or $m \mid k$. Thus $S$ is totally ordered by divisibility. Let
$$
d = \gcd(S)
$$
(the smallest element in $S$ under divisibility, which exists because $S$ is totally ordered by $\mid$). Then $d\mathbb{Z} \in \mathcal{C}$.

For any $k\mathbb{Z} \in \mathcal{C}$, we have $k \in S$ and $d \mid k$, hence $k\mathbb{Z} \subseteq d\mathbb{Z}$, i.e. $k\mathbb{Z} \preceq d\mathbb{Z}$. So $d\mathbb{Z}$ is an upper bound of $\mathcal{C}$ and $d\mathbb{Z} \in \mathcal{A}$.

Thus every chain in $\mathcal{A}$ has an upper bound in $\mathcal{A}$, so the hypothesis of Zorn’s Lemma holds.
___

>[!problem] [SHE] 6D.12
>Prove that every linearly independent family in a vector space can be extended to a basis of the vector space.

**Proof:**
Let $V$ be a vector space, $S_0 \subset V$ linearly independent. Define
$$
\mathcal{F} = \{ S \subset V \mid S_0 \subset S,\; S \text{ linearly independent} \}
$$
ordered by inclusion.

$\mathcal{F} \ne \varnothing$ since $S_0 \in \mathcal{F}$.

Let $\mathcal{C}$ be a chain in $\mathcal{F}$. Put $S_* = \bigcup_{S \in \mathcal{C}} S$.
- $S_0 \subset S_*$.
- $S_*$ is linearly independent: any finite subset of $S_*$ lies in some $S \in \mathcal{C}$ (because $\mathcal{C}$ is a chain), hence independent.

Thus $S_* \in \mathcal{F}$ and is an upper bound of $\mathcal{C}$.

By Zorn’s lemma, $\mathcal{F}$ has a maximal element $B$. We show $B$ is a basis:

$B$ is independent by definition. If $v \in V \setminus \operatorname{span}(B)$, then $B \cup \{v\}$ is independent and contains $S_0$, so $B \cup \{v\} \in \mathcal{F}$, contradicting maximality. Hence $V = \operatorname{span}(B)$.

Therefore $B$ is a basis extending $S_0$.
___

