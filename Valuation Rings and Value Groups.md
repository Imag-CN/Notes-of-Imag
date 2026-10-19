___

>[!problem] Definitions
>
>Let $K$ be a field and $\Gamma$ a totally ordered abelian group, written additively. A **valuation** is a map
>$$
>v:K^\times\to\Gamma
>$$
>such that
>$$
>v(xy)=v(x)+v(y),\qquad
>v(x+y)\ge\min\{v(x),v(y)\},
>$$
>whenever $x+y\neq0$. We usually extend it by setting $v(0)=+\infty$.
>
>The **value group** is
>$$
>\Gamma_K=v(K^\times).
>$$
>
>In this note, we always assume that $v$ is surjective onto its value group unless explicitly stated otherwise.
>
>The associated **valuation ring** is
>$$
>\mathcal O_v=\{x\in K:v(x)\ge0\},
>$$
>with maximal ideal
>$$
>\mathfrak m_v=\{x\in K:v(x)>0\}.
>$$
>Its residue field is
>$$
>k_v=\mathcal O_v/\mathfrak m_v.
>$$

We can also start from defining a valuation ring:

>[!problem] Definition 2
>A subring $\mathcal O\subseteq K$ is a **valuation ring** of $K$ if for every $x\in K^\times$, either $x\in\mathcal O$ or $x^{-1}\in\mathcal O$.
>
>We also call a domain a valuation ring if it is **a valuation ring** in its field of fraction.

Given a valuation ring $\mathcal O\subseteq K$, its value group can be recovered as
$$
\Gamma=K^\times/\mathcal O^\times,
$$
with the order induced by divisibility. The valuation map is defined as the quotient map of the identity above. It's easy to verify that the two definitions are identical.
___

>[!problem] Proposition 3
>Every totally ordered abelian group can occur as the value group of some valued field.

**Proof:**
A construction is
$$
K=k((t^\Gamma)).
$$
Its elements are formal sums
$$
f=\sum_{\gamma\in\Gamma}a_\gamma t^\gamma
$$
whose support is well-ordered. Define
$$
v(f)=\min\operatorname{supp}(f).
$$
Then
$$
v(t^\gamma)=\gamma,
$$
so
$$
v(K^\times)=\Gamma.
$$

Thus there is essentially no restriction beyond being a totally ordered abelian group.
___

>[!problem] Definition 4
>An ordered abelian group $\Gamma$ is **Archimedean** if for every $\gamma,\delta>0$, there exists $n\ge1$ such that
>$$
>n\gamma>\delta.
>$$
>
>Equivalently, $\Gamma$ has no nonzero infinitesimal relative to another positive element.

The fundamental result is **Hölder's theorem**:

>[!problem] Theorem 5 (Hölder's theorem)
> An ordered abelian group $\Gamma$ is Archimedean iff it admits an order-preserving group embedding
> $$
>\phi: \Gamma\hookrightarrow(\mathbb R,+).
> $$

**Proof:**
The idea is to choose $u>0$ as a unit, i.e. let $\phi(u)=1$. For $x\in\Gamma$ and $n\in \mathbb{N}$, the Archimedean condition guarantees that there exists a unique $m_{n}\in \mathbb{Z}$ such that
$$
m_{n}u\leq nx <(m_{n}+1)u.
$$
It's easy to verify that $\{ m_{n} / n \}$ is a Cauchy sequence, we define $\phi(x)$ to be its limit.

It remains to verify that $\phi$ is an order-preserving injective group homeomorphism, but those are all standard from construction.
___

>[!problem] Corollary 6
>There is a natrual bijection:
>
>$$
>\text{real-valued non-Archimedean absolute values}\longleftrightarrow\text{Archimedean-valued valuations}.
>$$
>
>This explains exactly when an additive valuation can be represented by a real-valued non-Archimedean absolute value.

**Proof:**
Suppose $v:K^\times\to\Gamma$ and $\Gamma$ is Archimedean. Choose an order embedding $\iota:\Gamma\hookrightarrow\mathbb R$. Then
$$
|x|=\exp(-\iota(v(x)))
$$
defines a non-Archimedean absolute value satisfying
$$
|x+y|\le\max\{|x|,|y|\}.
$$

Conversely, given a real-valued non-Archimedean absolute value, one may set
$$
v(x)=-\log|x|.
$$
Its value group is an ordered subgroup of $\mathbb R$, hence Archimedean.
___

For example, $\mathbb Z$, $\mathbb Q$, $\mathbb Z[\sqrt2]$, and $\mathbb R$ are Archimedean ordered groups.

On the other hand, $\mathbb Z^2$ with lexicographic order is not Archimedean, since
$$
n(0,1)<(1,0)
$$
for every $n\ge1$. Hence a valuation with value group $\mathbb Z^2_{\mathrm{lex}}$ cannot be encoded by an ordinary real-valued absolute value.
___

## 4. The valuation topology

For a general value group $\Gamma$, there may be no real-valued absolute value. Nevertheless, every valuation defines a natural topology on $K$.

For $\gamma\in\Gamma$, set
$$
B_\gamma(0)=\{x\in K:v(x)>\gamma\}.
$$
These form a neighborhood basis of $0$. By translation,
$$
B_\gamma(a)=\{x\in K:v(x-a)>\gamma\}
$$
forms a neighborhood basis of $a$.

Thus
$$
x_i\to x
$$
means
$$
v(x_i-x)\to+\infty,
$$
where this notation means that for every $\gamma\in\Gamma$, eventually
$$
v(x_i-x)>\gamma.
$$

This is **not** the order topology on $\Gamma$. For example, for the $p$-adic valuation,
$$
v_p(p^n)=n\to+\infty,
$$
although $1,2,3,\ldots$ does not converge in the order topology on $\mathbb Z$.

The value group should therefore be thought of as a generalized ruler: its order tells us when one difference is smaller than another. We care about moving arbitrarily far toward $+\infty$, not about convergence inside $\Gamma$ itself.

A sequence $(x_n)$ is Cauchy if for every $\gamma\in\Gamma$, there exists $N$ such that
$$
m,n\ge N\implies v(x_m-x_n)>\gamma.
$$

For sufficiently general value groups, sequences need not detect the whole topology, so completeness is more properly formulated using Cauchy nets or Cauchy filters.

In the Archimedean case, after replacing $v$ by $|\cdot|=e^{-v}$, this becomes the usual ultrametric language:
$$
d(x,y)=|x-y|.
$$

Thus the absolute-value language does not contain more information for a fixed rank-one valuation. Its advantage is that it places valued fields directly in the language of metric spaces, Banach spaces, and non-Archimedean analysis.

---

## 5. Rank and convex subgroups

A subgroup $\Delta\subseteq\Gamma$ is **convex** if
$$
0\le\gamma\le\delta,\quad \delta\in\Delta
\quad\Longrightarrow\quad
\gamma\in\Delta.
$$

The convex subgroups of an ordered abelian group are totally ordered by inclusion.

For example,
$$
0\subsetneq\{0\}\times\mathbb Z\subsetneq\mathbb Z^2_{\mathrm{lex}}
$$
is the chain of convex subgroups of $\mathbb Z^2_{\mathrm{lex}}$.

The **rank** of $\Gamma$ measures the length of this chain. In particular,
$$
\operatorname{rank}(\Gamma)=1
$$
iff $\Gamma$ has no nontrivial proper convex subgroup, which is equivalent to $\Gamma$ being Archimedean.

For a finite-rank group, a maximal convex filtration
$$
0=\Gamma_0\subsetneq\Gamma_1\subsetneq\cdots\subsetneq\Gamma_r=\Gamma
$$
has the property that every quotient
$$
\Gamma_i/\Gamma_{i-1}
$$
is Archimedean, hence embeds into $\mathbb R$.

Thus a higher-rank ordered group can be viewed as being built from several Archimedean scales.

However, one should not conclude that
$$
\Gamma\cong A_1\oplus_{\mathrm{lex}}\cdots\oplus_{\mathrm{lex}}A_r.
$$
The successive extensions need not split. What is canonical is the convex filtration and its Archimedean quotients, not a direct-sum decomposition.

The Hahn embedding theorem makes this picture precise: general ordered abelian groups can be embedded into suitable lexicographically ordered Hahn products of Archimedean groups.

---

## 6. Dedekind completeness of the value group

It is important not to confuse completeness of the valued field with order completeness of its value group.

A Dedekind complete ordered abelian group must be Archimedean. Indeed, if $0<\epsilon$ were infinitesimal relative to $u>0$, so that
$$
n\epsilon<u
$$
for all $n$, then
$$
a=\sup\{n\epsilon:n\ge1\}
$$
would satisfy
$$
a+\epsilon=a,
$$
contradicting cancellation.

Thus a genuinely higher-rank ordered group cannot be embedded into a Dedekind complete ordered abelian group while preserving its ordered-group structure.

In the Archimedean case, the familiar picture is
$$
\mathbb Z\longrightarrow\mathbb Q\longrightarrow\mathbb R,
$$
where the first step is divisible closure and the second is Dedekind completion.

For general higher-rank groups, ordinary Dedekind completion is therefore not the appropriate notion of completion in valuation theory.

---

## 7. Completion of a valued field

Let $\widehat K$ be the completion of a valued field $K$. The valuation extends uniquely to $\widehat K$, and
$$
\Gamma_{\widehat K}=\Gamma_K.
$$

Indeed, if $x\in\widehat K^\times$ and $x_n\in K$ converges to $x$, then eventually
$$
v(x_n-x)>v(x),
$$
and the ultrametric inequality implies
$$
v(x_n)=v(x).
$$
Thus every value occurring in $\widehat K$ already occurs in $K$.

The residue field is unchanged as well:
$$
k_{\widehat K}\cong k_K.
$$

Hence completion is an **immediate extension**:
$$
\boxed{
\Gamma_{\widehat K}=\Gamma_K,\qquad
k_{\widehat K}=k_K.
}
$$

This shows again why completing the valued field has essentially nothing to do with taking an order-theoretic completion of its value group.

---

## 8. Algebraic closure and the divisible hull

Algebraic closure behaves very differently.

Let $\overline K$ be an algebraic closure and extend $v$ to $\overline K$. Then
$$
\boxed{
\Gamma_{\overline K}
=
\Gamma_K\otimes_{\mathbb Z}\mathbb Q.
}
$$

Indeed, if $a\in K^\times$ and $x^n=a$, then
$$
nv(x)=v(a),
$$
so
$$
v(x)=\frac{v(a)}n.
$$
Thus algebraic closure produces all rational divisions of values.

Conversely, every $x\in\overline K$ lies in some finite extension $L/K$, and $\Gamma_L/\Gamma_K$ is torsion. Hence some positive multiple of $v(x)$ lies in $\Gamma_K$. Therefore no values outside the divisible hull can appear.

Similarly, the residue field becomes algebraically closed:
$$
k_{\overline K}\cong\overline{k_K}.
$$

Thus the two fundamental operations behave schematically as
$$
\begin{array}{c|cc}
&\text{value group}&\text{residue field}\\
\hline
K&\Gamma_K&k_K\\
\widehat K&\Gamma_K&k_K\\
\overline K&\Gamma_K\otimes\mathbb Q&\overline{k_K}.
\end{array}
$$

---

## 9. Example: $\mathbb Q_p$, $\overline{\mathbb Q}_p$, and $C_p$

For $\mathbb Q_p$,
$$
\Gamma_{\mathbb Q_p}=\mathbb Z,\qquad
k_{\mathbb Q_p}=\mathbb F_p.
$$

Passing to the algebraic closure gives
$$
\Gamma_{\overline{\mathbb Q}_p}=\mathbb Q,\qquad
k_{\overline{\mathbb Q}_p}=\overline{\mathbb F}_p.
$$

Finally,
$$
C_p=\widehat{\overline{\mathbb Q}_p}.
$$
Since completion is immediate,
$$
\Gamma_{C_p}=\mathbb Q,\qquad
k_{C_p}=\overline{\mathbb F}_p.
$$

Thus
$$
(\mathbb Z,\mathbb F_p)
\xrightarrow{\text{algebraic closure}}
(\mathbb Q,\overline{\mathbb F}_p)
\xrightarrow{\text{completion}}
(\mathbb Q,\overline{\mathbb F}_p).
$$

In particular, the completeness of $C_p$ does **not** make its value group $\mathbb R$. Completeness concerns the uniform structure on the field, not order completeness of the value group.

---

## 10. Summary

The basic hierarchy is
$$
\boxed{
\begin{array}{c}
\text{totally ordered abelian groups}\\
\updownarrow\\
\text{possible value groups of general valuations}
\end{array}}
$$

while
$$
\boxed{
\begin{array}{c}
\text{Archimedean ordered abelian groups}\\
\updownarrow\\
\text{ordered subgroups of }\mathbb R\\
\updownarrow\\
\text{real-valued non-Archimedean absolute values}.
\end{array}}
$$

Rank measures the number of different Archimedean scales present in a value group. Rank one is precisely the Archimedean case; higher rank records genuinely infinitesimal levels that cannot be represented by a single real-valued absolute value.

Finally, the value group should be viewed as a **scale of measurement**, not as the space being completed:
$$
\boxed{
\text{completion of }K\text{ leaves }\Gamma\text{ unchanged},
\qquad
\text{algebraic closure replaces }\Gamma\text{ by }\Gamma\otimes\mathbb Q.
}
$$
___
Notice that every ordered abelian group is torsion-free. Hence it has a divisible hull
$$
\Gamma_{\mathbb Q}:=\Gamma\otimes_{\mathbb Z}\mathbb Q,
$$
and the order on $\Gamma$ extends uniquely to $\Gamma_{\mathbb Q}$.

>[!problem] Proposition 4
>The valuation $v$ on $K$ extend uniquely to its algebraic closure $\bar{K}$, with the valuation group $\Gamma$ extended to $\Gamma_{\mathbb{Q}}$.
>
>Therefore, if $L/K$ is an algebraic extension, then $v$ extend uniquely to $L$, with the valuation group $\Gamma$ extended to some subgroup of $\Gamma_{\mathbb{Q}}$.
