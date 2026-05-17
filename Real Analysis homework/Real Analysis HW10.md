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
We need to show that the collection $\mathcal{A} = \{k\mathbb{Z} : k = 2,3,4,\dots\}$ with the order $k\mathbb{Z} \preceq m\mathbb{Z} \iff m\mathbb{Z} \subseteq k\mathbb{Z}\iff k\mid m \,(\text{for positive } k,m)$ satisfies the hypothesis of Zorn’s Lemma: every chain in $\mathcal{A}$ has an upper bound in $\mathcal{A}$.

Let $\mathcal{C}$ be a chain in $\mathcal{A}$. Define
$$
S = \{k \ge 2 : k\mathbb{Z} \in \mathcal{C}\}.
$$
Since $\mathcal{C}$ is a chain, for any $k,m \in S$, either $k \mid m$ or $m \mid k$. Thus $S$ is totally ordered by divisibility. Let
$$
d = \min(S)
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

> [!problem] [SHE] 6A.6 (Already assigned in the first homework)
> (a) Prove that if $V$ is a metric space, $f \in V$, and $r > 0$, then $\overline{B(f, r)} \subset \overline{B}(f, r)$.  
> (b) Give an example of a metric space $V$, $f \in V$, and $r > 0$ such that $\overline{B(f, r)} \neq \overline{B}(f, r)$.

**Proof:**
**(a)** By definition we have $B(f, r) \subset \overline{B}(f, r)$. The closure $\overline{B(f, r)}$ is the smallest closed set containing $B(f,r)$, and $\overline{B}(f, r)$ is a closed set containing $B(f,r)$, thus $\overline{B(f, r)} \subset \overline{B}(f, r)$.
**(b)** Let $V$ be a set containing at least two elements, and equip it with discrete metric (then it has the discrete topology). Let $f \in V$, then $B(f,1)= \{ f \}$, and $\overline{ B }(f,1)=V$. However, ${f}$ itself is a closed set, thus $\overline{ B(f,r) }=\{ f \}$ . Therefore $\overline{B(f, r)} \neq \overline{B}(f, r)$.
___

>[!problem] [SHE] 6A.15(5)
>Verify the following space is a complete metric space:
>
>Define $d$ on $\ell^1 \times \ell^1$ by $d((a_1, a_2, \ldots), (b_1, b_2, \ldots)) = \sum_{k=1}^{\infty} |a_k - b_k|$; here $\ell^1$ is the set of sequences $(a_1, a_2, \ldots)$ of real numbers such that $\sum_{k=1}^{\infty} |a_k| < \infty$.

**Proof:**
This space is obviously a metric space, so we show that it is complete.

Let $(a^{(n)})_{n=1}^{\infty}$ be a Cauchy sequence in $\ell^1$, with $a^{(n)} = (a_1^{(n)}, a_2^{(n)}, \dots)$.
For each fixed $k$, we have
$$
|a_k^{(n)} - a_k^{(m)}| \le d(a^{(n)}, a^{(m)}) \to 0 \quad (n, m \to \infty).
$$
Hence $(a_k^{(n)})_{n=1}^{\infty}$ is a Cauchy sequence in $\mathbb{R}$, so it converges. Define
$$
a_k := \lim_{n \to \infty} a_k^{(n)}, \qquad a := (a_1, a_2, \dots).
$$

**Step 2. $a \in \ell^1$.**  
Since $(a^{(n)})$ is Cauchy, it is bounded: $\sup_n d(a^{(n)}, 0) = M < \infty$. For any $N$,
$$
\sum_{k=1}^{N} |a_k| = \lim_{n \to \infty} \sum_{k=1}^{N} |a_k^{(n)}| \le M.
$$
Letting $N \to \infty$ gives $\sum_{k=1}^{\infty} |a_k| \le M$, so $a \in \ell^1$.

**Step 3. Convergence in $\ell^1$.**  
Fix $\varepsilon > 0$. Choose $N_0$ such that for all $n, m \ge N_0$,
$$
d(a^{(n)}, a^{(m)}) = \sum_{k=1}^{\infty} |a_k^{(n)} - a_k^{(m)}| < \varepsilon.
$$
For any $K$,
$$
\sum_{k=1}^{K} |a_k^{(n)} - a_k| = \lim_{m \to \infty} \sum_{k=1}^{K} |a_k^{(n)} - a_k^{(m)}| \le \varepsilon.
$$
Let $K \to \infty$ to obtain
$$
d(a^{(n)}, a) = \sum_{k=1}^{\infty} |a_k^{(n)} - a_k| \le \varepsilon \quad \text{for all } n \ge N_0.
$$
Hence $a^{(n)} \to a$ in $\ell^1$.

Therefore $(\ell^1, d)$ is complete.