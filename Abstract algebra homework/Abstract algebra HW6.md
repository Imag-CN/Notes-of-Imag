___

> [!problem] Problem 1
> Let $k$ be a field in which $2 \neq 0$. Let $A$ be a symmetric invertible matrix over $k$. The claim is that there exists a matrix $X$ over $k$ such that $X^T A X = I$.  
> (i) Suppose for each element $x \in k$ there exists $y \in k$ such that $y^2 = x$. Prove that the claim is true.  
> (ii) For $k = \mathbb{Q}$, construct a counterexample to the claim.

**Proof:**
**(i)** Since $\operatorname{char}(k) \neq 2$, any symmetric matrix over $k$ is *congruent* to a diagonal matrix.  
So, there exists an invertible matrix $P$ over $k$ such that
$$P^T A P = D = \operatorname{diag}(d_1, \dots, d_n),$$
with $d_i \in k^\times$ ($A$ is invertible).

Let $S = \operatorname{diag}(1/\sqrt{d_1}, \dots, 1/\sqrt{d_n})$. Then
$$S^T D S = I.$$

Setting $X = P S$, we have
$$X^T A X = S^T (P^T A P) S = S^T D S = I.$$
So the claim holds.

**(ii)** If $X^T A X = I$, then $X$ is invertible. For any vector $v\neq 0$, $v^{T}Av=(v^{T}X^{-T})(X^{-1}v)\geq 0$, thus $A$ is positive definite.
Take
$$A = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$$
which is not positive definite, then it is a counterexample.
___

> [!problem] Problem 2
>Let $A_{1},A_{2} \in M_{n\times n}(\mathbb{C})$ be symmetric invertible matrices. Let
>$$
>G_{1} = \{X \in GL_{n}(\mathbb{C}) \mid X^{T}A_{1}X = A_{1}\}
>$$
>$$
>G_{2} = \{X \in GL_{n}(\mathbb{C}) \mid X^{T}A_{2}X = A_{2}\}
>$$
>Prove that $G_{1}$ and $G_{2}$ are conjugate in $GL_{n}(\mathbb{C})$.

**Proof.**
Since $A_1$ and $A_2$ are complex symmetric invertible matrices, they are both congruent to the identity matrix $I_n$ over $\mathbb{C}$. That is, there exist $P_1, P_2 \in GL_n(\mathbb{C})$ such that
$$
P_1^T A_1 P_1 = I_n, \qquad P_2^T A_2 P_2 = I_n.
$$

Let $X \in G_1$, i.e., $X^T A_1 X = A_1$.  
Then
$$(P_1^{-1} X P_1)^T (P_1^{-1} X P_1) = P_1^T X^T (P_1^{-1})^T P_1^{-1} X P_1 = I_n.$$
This shows $P_1^{-1} X P_1 \in O(n, \mathbb{C})$, hence $G_1 = P_1 \, O(n, \mathbb{C}) \, P_1^{-1}$. Similarly, for $G_2$, we have $G_2 = P_2 \, O(n, \mathbb{C}) \, P_2^{-1}$.

Set $Q = P_1 P_2^{-1} \in GL_n(\mathbb{C})$. Then
$$Q^{-1} G_1 Q = (P_2 P_1^{-1}) (P_1 \, O(n, \mathbb{C}) \, P_1^{-1}) (P_1 P_2^{-1}) = P_2 \, O(n, \mathbb{C}) \, P_2^{-1} = G_2.$$
Therefore $G_1$ and $G_2$ are conjugate in $GL_n(\mathbb{C})$.
___

> [!problem] Problem 3
>Let $V$ be a vector space over a field $k$. Let $B_1, B_2$ be two symplectic forms on the vector space $V$. Prove that there exists $T \in GL_n(k)$ such that
> $$
> B_1(x, y) = B_2(Tx, Ty)
>$$
>holds for all $x, y \in V$.

**Proof:**
Let $\dim_k V = 2n$. Both $(V,B_1)$ and $(V,B_2)$ are symplectic vector spaces.

By the existence of a symplectic basis, choose bases
$$\mathcal{E}_1=\{e_i,f_i\},\quad \mathcal{E}_2=\{e'_i,f'_i\}$$
such that
$$
B_1(e_i,f_j)=\delta_{ij}=-B_1(f_j,e_i),\quad B_2(e'_i,f'_j)=\delta_{ij}=-B_2(f'_j,e'_i),
$$
and all other pairings are $0$.

Define $T\in GL(V)$ by $T(e_i)=e'_i,\;T(f_i)=f'_i$.

Then for any $x=\sum_i(a_i e_i+b_i f_i),\;y=\sum_j(c_j e_j+d_j f_j)$, we have
$$
B_1(x,y)=\sum_i(a_i d_i - b_i c_i),\quad
B_2(Tx,Ty)=\sum_i(a_i d_i - b_i c_i).
$$
Thus $B_1(x,y)=B_2(Tx,Ty)$ for all $x,y\in V$.
___

>[!remark]
> Note that the field $k$ in Question 3 can be arbitrary. It can be $\mathbb{Q}$, which does not have square roots in general. It can even be $\mathbb{F}_{2}$. This shows that symplectic forms are not sensitive to the base field, while quadratic forms are, as shown in Question 1.