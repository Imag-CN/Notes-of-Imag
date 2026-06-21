___

>[!problem] Problem 1
>Let $L/K$ be a field extension of finite degree. For a finite-dimensional $K$-algebra $R$, we say it is *split for $L$* if
>$$
>L \otimes_K R \cong \prod_{i=1}^d L
>$$
>as $L$-algebras for some $d$, where $L \otimes_K R$ is viewed as an $L$-algebra via left multiplication.
>
>Assume both $A$ and $B$ are split for $L$. Prove that $A \otimes_K B$ is also split for $L$.

**Proof:**
$$
L\otimes_K(A\otimes_{K} B)   \cong (L\otimes _{K}A)\otimes_{K} B  \cong\left( \prod_{i=1}^{d_{b}} L \right) \otimes_{K} B \cong  \prod_{i=1}^{d_{b}} \left(L \otimes_{K} B\right) \cong \prod_{i=1}^{d_{a}d_{b}} L.
$$
___

> [!problem] Problem 2
> Let $p$ be a prime number. Prove that there exists a homomorphism $\mathbb{F}_{p^{m}}\to \mathbb{F}_{p^{n}}$ of fields if and only if $m$ divides $n$.

**Proof:**
($\Rightarrow$) Homomorphism of fields $\Rightarrow$ injective $\Rightarrow$ $\mathbb{F}_{p^{m}}$ is a subfield of $\mathbb{F}_{p^{n}}$ $\Rightarrow$ $\mathbb{F}_{p^{n}}$ is a vector space of $\mathbb{F}_{p^{m}}$ $\Rightarrow$ $p^{n}=(p^{m})^{k}$ for some $k$ $\Rightarrow$ $m | n$.

($\Rightarrow$) Consider the splitting field of $f(X)=X^{p^{n}}-X$ over $\mathbb{F}_{p^{m}}$. Since:
- $f(X)$ has no multiple roots;
- The roots of $f(X)$ are closed under addition, multiplication and taking inverse;
- Elements in $\mathbb{F}_{p^{m}}$ all suffices $f(X)$ (because they suffices $X^{p^{m}}-X$, which divides $f(X)$ since $m |n$);
this splitting field is exactly $\mathbb{F}_{p^{n}}$. The natural inclusion map is the required homomorphism.
___

>[!problem] Problem 3
>Prove that there exists an irreducible polynomial in $\mathbb{F}_{q}[x]$ of degree $n$ for each positive integer $n$.

**Proof:**
Consider a generator $a$ of $(\mathbb{F}_{q^{n}})^{\times}$ (which is a cyclic group), it is a primitive element of any extension into $\mathbb{F}_{q^{n}}$. Let $f(x)\in\mathbb{F}_{q}[x]$ be the minimal polynomial of $a$, then $\mathbb{F}_{q^{n}}\cong \mathbb{F}_{q}[x] / (f(x))$. Thus $q^{n}=q^{\operatorname{deg}f}$, $\operatorname{deg}f=n$, so $f(x)$ is the required polynomial.