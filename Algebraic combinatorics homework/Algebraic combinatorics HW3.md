___

> [!problem] 9.1
> Let $\lambda$ be a partition and $\lambda'$ its conjugate. Prove that
> $$
> s_\lambda(\mathbf{x})=\det(M)
> $$
> where $M$ is a $\lambda_1\times\lambda_1$ matrix and $M_{i,j}=e_{\lambda'_j-j+i}(\mathbf{x})$.

**Proof:**
Let $l=\lambda_1$, and set
$$
u_i=(1-i,1),\qquad v_i=(\lambda'_i-i+1,\infty)
$$
for $1\le i\le l$. Consider northeast lattice paths from the $u_i$'s to the $v_j$'s.

Use the $e$-labeling of the east steps: if the east steps of a path, from left to right, occur at heights
$$
a_1<a_2<\cdots<a_r,
$$
give the path weight $x_{a_1}\cdots x_{a_r}$. Thus the weight-generating function of paths having $r$ east steps is $e_r(\mathbf{x})$.

A path from $u_i$ to $v_j$ has exactly
$$
(\lambda'_j-j+1)-(1-i)=\lambda'_j-j+i
$$
east steps. Hence its weight-generating function is
$$
e_{\lambda'_j-j+i}(\mathbf{x}).
$$
Therefore, by the LGV lemma,
$$
\det\left(e_{\lambda'_j-j+i}(\mathbf{x})\right)_{1\le i,j\le l}
$$
is the weight-generating function of the nonintersecting path families connecting $u_i$ to $v_i$.

It remains to identify these families with semistandard Young tableaux of shape $\lambda$. Given a nonintersecting family $(P_1,\ldots,P_l)$, record the labels of the east steps of $P_j$ in the $j$-th column of $\lambda$, from top to bottom. Since the $e$-labels along each path are strictly increasing, the entries in each column are strictly increasing. Since the paths are nonintersecting, the entries in each row are weakly increasing. Thus we obtain a semistandard Young tableau of shape $\lambda$.

Conversely, from a semistandard Young tableau of shape $\lambda$, the entries in its $j$-th column uniquely determine the east steps of $P_j$. Column-strictness gives a valid path, and row weak increase implies that the resulting paths are nonintersecting. Hence this is a weight-preserving bijection.

Therefore the generating function of the nonintersecting families is
$$
\sum_{T\in\operatorname{SSYT}(\lambda)}\mathbf{x}^T=s_\lambda(\mathbf{x}).
$$
Consequently,
$$
s_\lambda(\mathbf{x})
=
\det\left(e_{\lambda'_j-j+i}(\mathbf{x})\right)_{1\le i,j\le\lambda_1}
=
\det(M).
$$
>[!remark] Remark
>Applying $\omega$ to the identity gives $\omega(s_{\lambda})=s_{\lambda'}$.

___

> [!problem] 9.2
> Prove in two ways that
> $$
> s_{(k,1^{n-k})}(\mathbf{x})=\sum_{i=0}^{n-k}(-1)^i h_{k+i}(\mathbf{x})e_{n-k-i}(\mathbf{x});
> $$
> - using a sign reversing involution
> - by expanding the Jacobi-Trudi determinant along the first column.

**Proof:**
Put $r=n-k$.

**First proof:**
A monomial in $h_{k+i}e_{r-i}$ can be represented by a pair
$$
(a_1\le\cdots\le a_{k+i};\,b_1<\cdots<b_{r-i}),
$$
with weight $x_{a_1}\cdots x_{a_{k+i}}x_{b_1}\cdots x_{b_{r-i}}$ and sign $(-1)^i$.

We define a sign-reversing involution as follows. Compare $a_1$ with the entries $b_j$. If $a_1<b_1$ (or if there is no $b_1$), move $a_1$ from the weakly increasing sequence to the strictly increasing sequence. Otherwise, let $b_j$ be the largest $b_j\le a_1$ and move $b_j$ from the strictly increasing sequence to the weakly increasing sequence.

The move changes $i$ by $1$, preserves the weight, and reversing the same move recovers the original pair. Hence all terms cancel except when $i=0$ and
$$
a_1\le\cdots\le a_k,\qquad
a_1<b_1<\cdots<b_r.
$$
These are precisely the semistandard tableaux of hook shape $(k,1^r)$, with the $a_j$ in the first row and the $b_j$ below $a_1$ in the first column. Therefore
$$
\sum_{i=0}^r(-1)^ih_{k+i}e_{r-i}=s_{(k,1^r)}.
$$
**Second proof:**
Use the Jacobi-Trudi determinant
$$
s_\lambda=\det\left(h_{\lambda_j-j+i}\right).
$$
For $\lambda=(k,1^r)$, its first column is
$$
(h_k,h_{k+1},\ldots,h_{k+r})^T.
$$
Expanding along this column, the cofactor corresponding to $h_{k+i}$ has sign $(-1)^i$, and its minor is the Jacobi-Trudi determinant for $(1^{r-i})$, hence equals $e_{r-i}$. Therefore
$$
s_{(k,1^r)}
=\sum_{i=0}^r(-1)^ih_{k+i}e_{r-i}.
$$
Since $r=n-k$, this is
$$
s_{(k,1^{n-k})}
=\sum_{i=0}^{n-k}(-1)^ih_{k+i}e_{n-k-i}.
$$
___

