___

> [!problem] 9.1
> Let $\lambda$ be a partition and $\lambda'$ its conjugate. Prove that
> $$
> s_\lambda(\mathbf{x})=\det(M)
> $$
> where $M$ is a $\lambda_1\times\lambda_1$ matrix and $M_{i,j}=e_{\lambda'_j-j+i}(\mathbf{x})$.

**Proof:**
Apply the Jacobi-Trudi identity to $\lambda'$:
$$
s_{\lambda'}=\det\left(h_{\lambda'_i-i+j}\right)_{1\le i,j\le\lambda_1}.
$$
Let $\omega$ be the standard involution of the ring of symmetric functions, characterized by $\omega(h_r)=e_r$ and $\omega(s_\mu)=s_{\mu'}$. Applying $\omega$ gives
$$
s_\lambda=\det\left(e_{\lambda'_i-i+j}\right)_{1\le i,j\le\lambda_1}.
$$
Taking the transpose of the matrix does not change its determinant, so
$$
s_\lambda=\det\left(e_{\lambda'_j-j+i}\right)_{1\le i,j\le\lambda_1}=\det(M).
$$
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

**First proof:** By the Pieri rule,
$$
h_{k+i}e_{r-i}
=s_{(k+i)}e_{r-i}
=s_{(k+i,1^{r-i})}+s_{(k+i+1,1^{r-i-1})},
$$
where the second term is omitted when $i=r$.

Thus we may regard the signed objects contributing to $(-1)^ih_{k+i}e_{r-i}$ as semistandard tableaux of these two possible hook shapes. Pair a tableau of shape $(k+i+1,1^{r-i-1})$ occurring in the $i$-th term with the identical tableau of shape
$$
(k+(i+1),1^{r-(i+1)})
$$
occurring in the $(i+1)$-st term. This is a weight-preserving, sign-reversing involution.

All such objects cancel. The only unpaired objects are the tableaux of shape $(k,1^r)$ from the $i=0$ term. Hence
$$
\sum_{i=0}^r(-1)^ih_{k+i}e_{r-i}=s_{(k,1^r)}=s_{(k,1^{n-k})}.
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