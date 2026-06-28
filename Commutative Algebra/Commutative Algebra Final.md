___

> [!problem] Problem 0
> Describe the maximal ideals of $\mathbb{C}[x_1, \ldots, x_n]$.

**Proof:**
Let $\mathfrak{m}$ be a maximal ideal of $\mathbb{C}[x_{1},\dots ,x_{n}]$, consider the natural quotient map:
$$
\pi:\mathbb{C}[x_{1},\dots,x_{n}]\to L, \text{ where }L\text{ is defined as } \mathbb{C}[x_{1},\dots ,x_{n}] / \mathfrak{m}\text{ (thus $L$ is a field)}.
$$
let $f_{1}=\pi(x_{1}),\dots,f_{n}=\pi(x_{n})$, then since $\pi$ is surjective, we have $L=\mathbb{C}[f_{1},\dots,f_{n}]$. Thus $L$ is a finite $\mathbb{C}$-algebra. By Corollary 5.24 (or Corollary 7.20), $L$ is a finite field extension of $\mathbb{C}$, thus $f_{1},\dots,f_{n}$ is algebraic over $\mathbb{C}$. And since $\mathbb{C}$ is algebraically closed, $f_{1},\dots,f_{n}\in \mathbb{C}$. Therefore, $(x_{1}-f_{1},\dots,x_{n}-f_{n})$ is an ideal of $\mathbb{C}[x_{1},\dots,x_{n}]$, and it is a maximal ideal because $\mathbb{C}[x_{1},\dots,x_{n}] / (x_{1}-f_{1},\dots,x_{n}-f_{n})\cong \mathbb{C}$. Since $\pi(x_{1}-f_{1})=\dots=\pi(x_{n}-f_{n})=0$, we have $\mathfrak{m}=\operatorname{ker}\pi \supseteq (x_{1}-f_{1},\dots,x_{n}-f_{n})$. And since $(x_{1}-f_{1},\dots,x_{n}-f_{n})$ is maximal, $\mathfrak{m}=(x_{1}-f_{1},\dots,x_{n}-f_{n})$.

In conclusion, any maximal ideal of $\mathbb{C}[x_1, \ldots, x_n]$ has the form $(x_{1}-f_{1},\dots,x_{n}-f_{n})$ for some $f_{1},\dots f_{n}\in \mathbb{C}$. (Also, for any $f_{1},\dots f_{n}\in \mathbb{C}$, $(x_{1}-f_{1},\dots,x_{n}-f_{n})$ is a maximal ideal, because the quotient is $\mathbb{C}$).
___

> [!problem] Problem 1
> Using group action on rings, show that $R := \mathbb{C}[x,y,z,w]/(xy - zw)$ is integrally closed. Is this a Noetherian ring? Is the localization of this ring at every prime ideal $R_{\mathfrak{p}}$ a Regular Local Ring? Is $R_{\mathfrak{p}}$ Cohen-Macaulay?

**Proof:**
**Integrally closed:** Let $S=\mathbb C[a,b,c,d]$. Define an action of $\mathbb G_m=\mathbb C^\times$ on $S$ by
$$
t\cdot a=ta,\qquad t\cdot b=tb,\qquad t\cdot c=t^{-1}c,\qquad t\cdot d=t^{-1}d.
$$
Acting $t$ on a monomial $a^i b^j c^k d^\ell$ yields $t^{i+j-k-\ell}a^i b^j c^k d^\ell$. The group action doesn't change degree, hence $a^i b^j c^k d^\ell$ is invariant if and only if $i+j=k+\ell$, and a invariant polynomial must be a linear combination of . Eveinvariant monomialry invariant monomial can be written as a product of $ac, ad, bc,bd$, thus $S^{\mathbb G_m}=\mathbb C[ac,ad,bc,bd]$.

Define $\varphi:\mathbb C[x,y,z,w]\longrightarrow S$ by
$$
x\mapsto ac,\qquad y\mapsto bd,\qquad z\mapsto ad,\qquad w\mapsto bc.
$$
Then $\varphi(xy-zw)=(ac)(bd)-(ad)(bc)=0$, thus $(xy-zw)\subseteq \ker\varphi$, and $\operatorname{Im}\varphi=S^{\mathbb G_m}$.

Moreover, $\varphi (x^{i}y^{j}z^{k}w^{\ell})=a^{i+k}b^{j+\ell}c^{i+\ell}d^{j+k}$, so the degree (on each variant $a,b,c,d$) of $\varphi (x^{i}y^{j}z^{k}w^{\ell})$ and $\varphi (x^{i'}y^{j'}z^{k'}w^{\ell'})$ agree if and only if $i-i'=j-j'=k'-k=\ell'-\ell$, i.e. $xy-zw\mid x^{i}y^{j}z^{k}w^{\ell}-x^{i'}y^{j'}z^{k'}w^{\ell'}$. For any element in $\operatorname{ker}\varphi$, we can also write it as a sum of some sums of a pair of monomial with opposite coefficients and same degree of image, therefore $xy-zw$ divides any element in $\operatorname{ker} \varphi$, i.e. $(xy-zw)\supseteq \operatorname{ker}\varphi$.

Therefore $\mathbb C[x,y,z,w]/(xy-zw)\cong S^{\mathbb G_m}$. Since $S=\mathbb C[a,b,c,d]$ is a domain and $S^{\mathbb G_m}\subseteq S$, the invariant ring $S^{\mathbb G_m}$ is also a domain.

Now use the standard fact:

>[!lemma] Lemma
> If $B$ is an integrally closed domain and a group $G$ acts on $B$ by ring automorphisms, then $B^G$ is integrally closed.

Let $A=B^G$. If $\alpha\in \operatorname{Frac}(A)$ is integral over $A$, then it is integral over $B$. Since $B$ is integrally closed, $\alpha\in B$. Also $\alpha\in \operatorname{Frac}(A)$ is fixed by $G$, so $\alpha\in B^G=A$.

Applying this to $B=S$ and $G=\mathbb G_m$, since $S$ is a polynomial ring and hence integrally closed, we get that $S^{\mathbb G_m}$ is integrally closed.

Therefore, by the isomorphism above, $\mathbb C[x,y,z,w]/(xy-zw)$ is an integrally closed domain.

**Noetherian:** Yes. By Hilbert's basis theorem, $\mathbb C[x,y,z,w]$ is Noetherian. By Proposition 6.6, $\mathbb C[x,y,z,w]/(xy-zw)$ is also Noetherian.

**Regular Local:** No. Let $\mathfrak{m}=(\overline{ x },\overline{ y },\overline{ z },\overline{ w })$, then the residue field $k=R / \mathfrak{m}=\mathbb{C}$. Since $\mathfrak{m} / \mathfrak{m}^{2}\cong \mathbb{C}[x,y,z,w] / (\text{all 2-degree relations})\cong \mathbb{C}^{4}$, we have $\operatorname{dim}_{k}\mathfrak{m} / \mathfrak{m}^{2}=4$.

By Proposition 3.11 (iv), $(\mathbb{C}[x,y,z,w]/(xy - zw))_{\mathfrak{m}}\cong\mathbb{C}[x,y,z,w]_{(x,y,z,w)} / (xy-zw)_{(x,y,z,w)}$. Since $\mathbb{C}[x,y,z,w]$ is an integral domain, $(xy-zw) / 1$ is not a zero divisor in $\mathbb{C}[x,y,z,w]_{(x,y,z,w)}$. By the example after Theorem 11.4, $\operatorname{dim}\mathbb{C}[x,y,z,w]_{(x,y,z,w)}=4$.

Use Corollary 11.18:
>[!corollary] Corollary 11.18
>Let $A$ be a Noetherian local ring, $x_{A}$ an element of $\mathfrak{m}_{A}$ which is not a zero-divisor. Then $\operatorname{dim} A/(x_{A}) = \operatorname{dim} A - 1$.

here we set $A=\mathbb{C}[x,y,z,w]_{(x,y,z,w)}$, $x_{A}=(xy-zw) / 1$, then $\operatorname{dim}\mathbb{C}[x,y,z,w]_{(x,y,z,w)} / (xy-zw)_{(x,y,z,w)}=4-1=3$, i.e. $\operatorname{dim}(\mathbb{C}[x,y,z,w]/(xy - zw))_{\mathfrak{m}}=4$.

Therefore, $R_{\mathfrak{m}}$ is not a regular local ring.

**Cohen-Macaulay:** 

___

>[!problem] Problem 2
>Is the local ring of $\mathbb{C}[x,y]/(x^{2} −y^{3})$ at every prime ideal a Regular Local ring?

**Proof:**
No. Let $\mathfrak{m}=(\overline{ x },\overline{ y })$, then the residue field $k=R / \mathfrak{m}=\mathbb{C}$. Since $\mathfrak{m} / \mathfrak{m}^{2}\cong \mathbb{C}[x,y] / (\text{all 2-degree relations})\cong \mathbb{C}^{2}$, we have $\operatorname{dim}_{k}\mathfrak{m} / \mathfrak{m}^{2}=2$.

By Proposition 3.11 (iv), $(\mathbb{C}[x,y]/(x^{2} - y^{3}))_{\mathfrak{m}}\cong\mathbb{C}[x,y]_{(x,y)} / (x^{2}-y^{3})_{(x,y)}$. Since $\mathbb{C}[x,y]$ is an integral domain, $(x^{2}-y^{3}) / 1$ is not a zero divisor in $\mathbb{C}[x,y]_{(x,y)}$. By the example after Theorem 11.4, $\operatorname{dim}\mathbb{C}[x,y]_{(x,y)}=2$. By Corollary 11.18, $\operatorname{dim}\mathbb{C}[x,y]_{(x,y)} / (x^{2}-y^{3})_{(x,y)}=2-1=1$.

Therefore, $R_{\mathfrak{m}}$ is not a regular local ring.