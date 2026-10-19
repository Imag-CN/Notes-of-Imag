___
# 1. Valuations and Valuation Rings

> [!problem] Definition 1.1  
> Let $K$ be a field and $\Gamma$ a totally ordered abelian group, written additively. A **valuation** is a map  
> $$  
> v^\times\to\Gamma  
> $$  
> such that  
> $$  
> v(xy)=v(x)+v(y),\qquad v(x+y)\ge\min{v(x),v(y)},  
> $$  
> whenever $x+y\neq0$. We extend it by setting $v(0)=+\infty$.
> 
> The **value group** of $K$ is  
> $$  
> \Gamma_K=v(K^\times).  
> $$  
> Unless otherwise stated, we take $\Gamma=\Gamma_K$, so that $v$ is surjective.
> 
> The associated **valuation ring** is  
> $$  
> \mathcal O_v={x\in K(x)\ge0},  
> $$  
> with maximal ideal  
> $$  
> \mathfrak m_v={x\in K(x)>0}.  
> $$  
> The **residue field** is  
> $$  
> k_v=\mathcal O_v/\mathfrak m_v.  
> $$

We can also start from the valuation ring itself.

> [!problem] Definition 1.2  
> A subring $\mathcal O\subseteq K$ is a **valuation ring** of $K$ if for every $x\in K^\times$, either $x\in\mathcal O$ or $x^{-1}\in\mathcal O$.
> 
> A domain is called a valuation ring if it is a valuation ring in its field of fractions.

Given a valuation ring $\mathcal O\subseteq K$, its value group can be recovered as  
$$  
\Gamma=K^\times/\mathcal O^\times,  
$$  
with the order induced by divisibility. The quotient map  
$$  
v^\times\to K^\times/\mathcal O^\times  
$$  
is the corresponding valuation.

Thus the two definitions of a valuation ring are equivalent.
___

# 2. Groups that can Occur as Value Groups

> [!problem] Proposition 2.1  
> Every totally ordered abelian group occurs as the value group of some valued field.

**Proof:**  
Let $k$ be a field and consider the Hahn series field  
$$  
K=k((t^\Gamma)).  
$$  
Its elements are formal sums  
$$  
f=\sum_{\gamma\in\Gamma}a_\gamma t^\gamma  
$$  
with well-ordered support. Define  
$$  
v(f)=\min\operatorname{supp}(f).  
$$  
Since $v(t^\gamma)=\gamma$, we have  
$$  
v(K^\times)=\Gamma.  
$$

Thus there is no restriction on a value group beyond being a totally ordered abelian group.
___

# 3. Archimedean Value Groups and Absolute Values

> [!problem] Definition 3.1  
> An ordered abelian group $\Gamma$ is **Archimedean** if for every $\gamma,\delta>0$, there exists $n\ge1$ such that  
> $$  
> n\gamma>\delta.  
> $$
> 
> Equivalently, $\Gamma$ has no nonzero infinitesimal relative to another positive element.

The fundamental result is Hölder's theorem.

> [!problem] Theorem 3.2 (Hölder's Theorem)  
> An ordered abelian group $\Gamma$ is Archimedean iff it admits an order-preserving group embedding  
> $$  
> \phi:\Gamma\hookrightarrow(\mathbb R,+).  
> $$

**Proof:**  
Choose $u>0$ and regard it as a unit. For $x\in\Gamma$ and $n\ge1$, the Archimedean property gives a unique $m_n\in\mathbb Z$ such that  
$$  
m_nu\le nx<(m_n+1)u.  
$$  
Then $m_n/n$ converges to a real number $\phi(x)$. One verifies that  
$$  
\phi(x+y)=\phi(x)+\phi(y)  
$$  
and that $\phi$ is order-preserving and injective.

The converse follows immediately since every ordered subgroup of $\mathbb R$ is Archimedean.

> [!problem] Corollary 3.3  
> A valuation can be represented by a real-valued non-Archimedean absolute value iff its value group is Archimedean.

**Proof:**  
Suppose $v^\times\to\Gamma$ and $\Gamma$ is Archimedean. By Hölder's theorem, choose an order embedding $\iota:\Gamma\hookrightarrow\mathbb R$. Then  
$$  
|x|=\exp(-\iota(v(x)))  
$$  
defines a non-Archimedean absolute value.

Conversely, given a real-valued non-Archimedean absolute value, define  
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
for every $n\ge1$. Hence a valuation with value group $\mathbb Z^2_{\mathrm{lex}}$ cannot be represented by an ordinary real-valued absolute value.

___

# 4. The Valuation Topology and Completeness

Even when $\Gamma$ is not Archimedean, a valuation still defines a natural topology on $K$.

> [!problem] Definition 4.1  
> For $\gamma\in\Gamma$, define  
> $$  
> B_\gamma(0)={x\in K(x)>\gamma}.  
> $$  
> These sets form a neighborhood basis of $0$. By translation,  
> $$  
> B_\gamma(a)={x\in K(x-a)>\gamma}  
> $$  
> forms a neighborhood basis of $a$.
> 
> This topology is called the **valuation topology**.

Thus $x_i\to x$ means  
$$  
v(x_i-x)\to+\infty,  
$$  
i.e. for every $\gamma\in\Gamma$, eventually $v(x_i-x)>\gamma$.

This should not be confused with the order topology on $\Gamma$. The value group serves as a scale measuring how close two elements of $K$ are.

> [!problem] Definition 4.2  
> A sequence $(x_n)$ is **Cauchy** if for every $\gamma\in\Gamma$, there exists $N$ such that  
> $$  
> m,n\ge N\implies v(x_m-x_n)>\gamma.  
> $$

For general value groups, sequences need not detect the whole topology, so completeness is more properly formulated using Cauchy nets or Cauchy filters.

In the Archimedean case, after representing the valuation by $|\cdot|=e^{-v}$, the valuation topology is induced by the ultrametric  
$$  
d(x,y)=|x-y|.  
$$

Thus the absolute-value language contains no additional information for a fixed Archimedean valuation; it packages the valuation topology in the usual metric language.
___

# 5. Rank and Convex Subgroups

> [!problem] Definition 5.1  
> A subgroup $\Delta\subseteq\Gamma$ is **convex** if  
> $$  
> 0\le\gamma\le\delta,\quad \delta\in\Delta  
> \quad\Longrightarrow\quad  
> \gamma\in\Delta.  
> $$

The convex subgroups of an ordered abelian group are totally ordered by inclusion.

> [!problem] Definition 5.2  
> The **rank** of an ordered abelian group $\Gamma$ is the order type of the chain of its proper convex subgroups.
> 
> In the finite-rank case, if  
> $$  
> 0=\Gamma_0\subsetneq\Gamma_1\subsetneq\cdots\subsetneq\Gamma_r=\Gamma  
> $$  
> is the full chain of convex subgroups, then $\Gamma$ has rank $r$.

For example,  
$$  
0\subsetneq{0}\times\mathbb Z\subsetneq\mathbb Z^2_{\mathrm{lex}},  
$$  
so $\mathbb Z^2_{\mathrm{lex}}$ has rank $2$.

> [!problem] Proposition 5.3  
> An ordered abelian group $\Gamma$ has rank $1$ iff it is Archimedean.

**Proof:**  
If $\Gamma$ is not Archimedean, choose $\gamma,\delta>0$ such that $n\gamma<\delta$ for every $n$. Then  
$$  
\Delta={x\in\Gamma:|x|\le n\gamma\text{ for some }n}  
$$  
is a nontrivial proper convex subgroup.

Conversely, if $\Delta\subsetneq\Gamma$ is a nontrivial convex subgroup, choose $0<\gamma\in\Delta$ and $0<\delta\notin\Delta$. Then $n\gamma<\delta$ for every $n$, so $\Gamma$ is not Archimedean.

> [!problem] Remark 5.4  
> If $\Gamma$ has finite rank with convex filtration  
> $$  
> 0=\Gamma_0\subsetneq\Gamma_1\subsetneq\cdots\subsetneq\Gamma_r=\Gamma,  
> $$  
> then every quotient $\Gamma_i/\Gamma_{i-1}$ is Archimedean.
> 
> Thus a higher-rank ordered group can be viewed as being built from several Archimedean scales.

In general, these extensions need not split, so one cannot necessarily write  
$$  
\Gamma\cong A_1\oplus_{\mathrm{lex}}\cdots\oplus_{\mathrm{lex}}A_r.  
$$  
What is canonical is the convex filtration and its Archimedean quotients.
___

# 6. Dedekind Completeness of Ordered Groups

Although every ordered abelian group has a divisible hull, ordinary Dedekind completion does not behave well for higher-rank groups.

> [!problem] Proposition 6.1  
> Every Dedekind complete ordered abelian group is Archimedean.

**Proof:**  
Suppose $0<\epsilon,u$ satisfy $n\epsilon<u$ for every $n\ge1$. Then  
$$  
a=\sup{n\epsilon\ge1}  
$$  
exists. But ${(n+1)\epsilon\ge1}$ has the same supremum, so  
$$  
a+\epsilon=a,  
$$  
contradicting $\epsilon>0$.

Therefore, a higher-rank ordered abelian group cannot be embedded as an ordered subgroup into a Dedekind complete ordered abelian group.

In the Archimedean case, the familiar picture is  
$$  
\mathbb Z\longrightarrow\mathbb Q\longrightarrow\mathbb R,  
$$  
where the first step is the divisible hull and the second is the Dedekind completion.

Thus Dedekind completeness of the value group is generally unrelated to completeness of the valued field.
___
# 7. Completion of Valued Fields

> [!problem] Definition 7.1  
> An extension $(L,v)/(K,v)$ is called **immediate** if it does not change either the value group or the residue field:  
> $$  
> \Gamma_L=\Gamma_K,\qquad k_L=k_K.  
> $$

> [!problem] Proposition 7.2  
> Let $(K,v)$ be a valued field and $\widehat K$ its completion. Then $v$ extends uniquely to $\widehat K$, and $\widehat K/K$ is immediate. In particular,  
> $$  
> \Gamma_{\widehat K}=\Gamma_K,\qquad k_{\widehat K}=k_K.  
> $$

**Proof:**  
Let $x\in\widehat K^\times$ and choose $x_n\in K$ with $x_n\to x$. Eventually,  
$$  
v(x_n-x)>v(x),  
$$  
so $v(x_n)=v(x)$. Hence every value in $\widehat K$ already occurs in $K$.

Similarly, every element of $\mathcal O_{\widehat K}$ can be approximated sufficiently closely by an element of $\mathcal O_K$ with the same residue. Hence $k_{\widehat K}=k_K$.

Thus completion of a valued field has nothing to do with Dedekind completion of its value group: completion does not change the value group at all.
___

# 8. Algebraic Extensions and Algebraic Closure


> [!problem] Proposition 8.1  
> Let $(K,v)$ be a valued field with value group $\Gamma$, and choose an extension of $v$ to an algebraic closure $\overline K$. Then  
> $$  
> \Gamma_{\overline K}=\Gamma_{\mathbb Q}:=\Gamma\otimes_{\mathbb Z}\mathbb Q.  
> $$  
> Consequently, for every algebraic extension $K\subseteq L\subseteq\overline K$,  
> $$  
> \Gamma\subseteq\Gamma_L\subseteq\Gamma_{\mathbb Q}.  
> $$
> 
> If $K$ is henselian, the extension of $v$ to $\overline K$, and hence to every algebraic extension $L/K$, is unique.

**Proof:**  
For $\gamma=v(a)\in\Gamma$ and $n\ge1$, choose $x\in\overline K$ such that $x^n=a$. Then  
$$  
v(x)=\frac{\gamma}{n},  
$$
so $\Gamma_{\mathbb Q}\subseteq\Gamma_{\overline K}$.

Conversely, every $x\in\overline K^\times$ lies in some finite extension $E/K$. Since $\Gamma_E/\Gamma$ is torsion, some $n\ge1$ satisfies $nv(x)\in\Gamma$. Hence $v(x)\in\Gamma_{\mathbb Q}$.

> [!problem] Proposition 8.2  
> With the same notation, the residue field of $\overline K$ is an algebraic closure of $k_K$:  
> $$  
> k_{\overline K}\cong\overline{k_K}.  
> $$

**Proof:**  
The extension $k_{\overline K}/k_K$ is algebraic. Moreover, the residue field of an algebraically closed valued field is algebraically closed. Hence it is an algebraic closure of $k_K$.

Therefore,  
$$
\begin{array}{c|cc}  
&\text{value group}&\text{residue field}\  
K&\Gamma_K&k_K\  
\widehat K&\Gamma_K&k_K\  
\overline K&\Gamma_K\otimes_{\mathbb Z}\mathbb Q&\overline{k_K}.  
\end{array}
$$

---

# 9. Example: $\mathbb Q_p$, $\overline{\mathbb Q}_p$, and $C_p$

> [!problem] Example 9.1  
> For $\mathbb Q_p$,  
> $$  
> \Gamma_{\mathbb Q_p}=\mathbb Z,\qquad  
> k_{\mathbb Q_p}=\mathbb F_p.  
> $$
> 
> Passing to the algebraic closure gives  
> $$  
> \Gamma_{\overline{\mathbb Q}_p}=\mathbb Q,\qquad  
> k_{\overline{\mathbb Q}_p}=\overline{\mathbb F}_p.  
> $$
> 
> Finally,  
> $$  
> C_p=\widehat{\overline{\mathbb Q}_p}.  
> $$  
> Since completion is immediate,  
> $$  
> \Gamma_{C_p}=\mathbb Q,\qquad  
> k_{C_p}=\overline{\mathbb F}_p.  
> $$

Thus  
$$  
(\mathbb Z,\mathbb F_p)  
\xrightarrow{\text{algebraic closure}}  
(\mathbb Q,\overline{\mathbb F}_p)  
\xrightarrow{\text{completion}}  
(\mathbb Q,\overline{\mathbb F}_p).  
$$

In particular, although $C_p$ is complete, its value group is still $\mathbb Q$, not $\mathbb R$. Completeness concerns the topology of the field, not the order completeness of its value group.