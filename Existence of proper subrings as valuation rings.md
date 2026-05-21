___

>[!question] 
>Given $K$ a field, when does there exists a proper subring $B \subsetneq K$ that is a valuation of $K$ (i.e. $B$ is a valuation ring and its fractional field is $K$) ? 

To approach this problem, we can start with some basic observations:

1. **The prime field cases**​ We first consider these cases because every field contains a prime subfield isomorphic to either $\mathbb{Q}$ or $\mathbb{F}_{}p$​ (depends on its character).

2. **The rational function field case**​ If $K$ contains an element $\alpha$ transcendental over its subfield $F$, then $K$ contains a subfield $F(\alpha)$ isomorphic to the rational function field $F(t)$.

3. **Valuation extension theorems**​ A central tool is Chevalley’s extension theorem. This will help in passing from known cases to more general fields.

Using these steps, we can systematically determine necessary and sufficient conditions on $K$ for the existence of such a proper valuation ring $B$.
___

>[!problem] Valuation rings of $\mathbb{F}_{p}$
>The only valuation ring of $\mathbb{F}_{p}$ is itself.

**Proof:**
The only subring of $\mathbb{F}_{p}$ is itself because $1$ generates the whole $\mathbb{F}_{p}$ by addition.

>[!remark] Finite fields
>For a finite field $K$, the only valuation ring with fraction field $K$ is $K$ itself. This is because $K^\times$ is a cyclic group, and if $x$ is a generator of $K^{\times}$, then $x^{-1}$ is also a generator. Either $x$ or $x^{-1}$ is in $B$, thus $B = K$.  
>
>In fact, this is a special case of the following result.

>[!problem] Valuation rings of algebraic extension of $\mathbb{F}_{p}$
>Let $K$ be an algebraic extension of $\mathbb{F}_{p}$. The only valuation ring of $K$ is itself.

**Proof:** 
Let $B$ be a valuation ring of $K$. Since $1$ generates the whole $\mathbb{F}_{p}$ through addition, $\mathbb{F}_{p}\subset B$. For any $x \in B$, let $p(t)=t^{n}+a_{n-1}t^{n-1}+\dots+a_{0}\in \mathbb{F}_{p}[t]$ be the minimal polynomial of $x$ (by minimality $a_{0}\neq0$). Then $p(x)=0$ implies $x^{-n}+a_{0}^{-1}a_{1}x^{1-n}+\dots+a_{0}^{-1}=0$, where the coefficients are all in $\mathbb{F}_{p}$, thus in $B$. Since $B$ is integrally closed in $K$, we have $x^{-1}\in B$. Therefore, $B$ has to be the whole field $K$.

>[!problem] Valuation rings of $\mathbb{Q}$
>The only valuation ring of $\mathbb{Q}$ are $\mathbb{Q}$ and $\mathbb{Z}_{p}$, where $\mathbb{Z}_{p}$ is the localization of $\mathbb{Z}$ at $(p)$ ($p$ is a prime number).

**Proof:**
Let $B\subsetneq Q$ is a valuation ring of $\mathbb{Q}$. Then there exists a prime number $p$ such that $\dfrac{1}{p} \not\in B$ (if not, then $\dfrac{1}{m} \in B$ for any $m\in \mathbb{Z}$, and $B$ becomes $\mathbb{Q}$). For any prime number $p'\neq p$, by Bezout's theorem there exist $k,k'\in \mathbb{Z}$ such that $kp+k'p'=1$. Then $k+k'\dfrac{p'}{p}=\dfrac{1}{p}$, so $\dfrac{p'}{p}$ is not in $B$. Since $B$ is a valuation ring, $\dfrac{p}{p'}$ is in $B$. And since $k \dfrac{p}{p'}+k'=\dfrac{1}{p'}$, we have $\dfrac{1}{p'}$ is in $B$. Therefore, for any $m\in \mathbb{Z}$ with $p \not\mid m$, we have $\dfrac{1}{m}\in B$. This is to say $B=\mathbb{Z}_{p}$.

>[!remark] Local rings in $\mathbb{Q}$
>In fact, every local ring in $\mathbb{Q}$ has the form $\mathbb{Z}_{s}:=(\mathbb{Z}\setminus s\mathbb{Z})^{-1}\mathbb{Z}$ for some $s\in \mathbb{Z}$.

___

>[!problem] Valuation rings of $F(t)$
>Let $F$ be a field, $F(t)$ be the field of rational functions on $F$ (also can be seen as the fractional field of the polynomial ring $F[t]$ on $F$). Then $F(t)$ has a valuation ring $B\subsetneq F(t)$.

**Proof:**
Every element $\alpha$ in $F(t)$ has the form $t^{k}\dfrac{p(t)}{q(t)}$ with $p(t),q(t)\in F[t]$ and $t \not\mid p(t),q(t)$. Since $F[t]$ is a UFD, $k$, the power of $t$, is uniquely determined by $\alpha$. We define $v(\alpha)=k$. Then it is easy to check $B:=\{ \alpha \in F(t) : v(\alpha)\geq 0\}$ is a valuation ring of $F(t)$ and $B\neq F(t)$.

>[!remark]
>We can see $v$ is actually a valuation of $F(t)$.

___

>[!problem] Chevalley's Extension Theorem
>Let $R$ be a local subring with maximal ideal $\mathfrak{m}$ contained in a field $K$. Then there exists a valuation ring $V$ of $K$ with maximal ideal $\mathfrak{m}_V$ satisfying:
>
>1. $R \subseteq V$;
>2. $\mathfrak{m}_V \cap R = \mathfrak{m}$.



