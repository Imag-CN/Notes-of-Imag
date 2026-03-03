___
> [!problem] Problem 1
> Let $n$ be a positive integer. Let $k$ be a field.
> 
> Denote $e_{ij}^n$ to be the $n \times n$ matrix which is 1 at entry $(i, j)$ and 0 elsewhere.
> 
> When $i \neq j$, denote $E_{ij}(\lambda) := I_{n \times n} + \lambda \cdot e_{ij}^n$ for $\lambda \in k$.
> 
> Suppose $A$ is an $n \times n$ matrix such that $\det(A) = 1$.
> 
> Prove that $A$ can be expressed as a product of matrices of the form $E_{ij}(\lambda)$ where $i \neq j$ and $\lambda \in k$.

**Proof:** We proceed by induction on $n$. The base case $n=1$ is degenerated.

Assume the statement holds for all $n \times n$ matrices over $k$ with determinant $1$. Let $A=(a_{ij})$ be an $(n+1) \times (n+1)$ matrix with $\det A = 1$.

**Case 1.** Suppose there exists an index $j \neq 1$ such that $a_{j1} \neq 0$. Define
$$
(a'_{ij})=A' = E_{1j}\bigl(a_{j1}^{-1}(a_{11}-1)\bigr)\,A .
$$
Then
$$
a'_{11} = a_{11} + a_{j1}^{-1}(a_{11}-1)\cdot a_{j1} = 1.
$$
Now let
$$
(a''_{ij})=A'' = E_{21}(-a'_{21})\dotsm E_{n+1,1}(-a'_{n+1,1}) \; A' \; E_{12}(-a'_{12})\dotsm E_{1,n+1}(-a'_{1,n+1}),
$$
Then $A''$ has the block form
$$
A'' = \begin{pmatrix}
1 & 0 & \dots & 0 \\
0 & & & \\
\vdots & & B & \\
0 & & &
\end{pmatrix},
$$
where $B$ is an $n \times n$ matrix. Because all elementary matrices $E_{ij}(\lambda)$ have determinant $1$, we have $\det A'' = \det A = 1$, then $\det B = 1$. By the induction hypothesis, $B$ can be written as a product of matrices of the form $E_{ij}(\lambda)$. Therefore $A''$, and hence $A$, is also a product of such matrices.

**Case 2.** Suppose $a_{j1}=0$ for all $j\neq 1$. Since $A$ is invertible, $a_{11}\neq 0$. Consider $B = E_{12}(1)\,A$. Then it goes back to the first case.
___

> [!problem] Problem 2
> Let $A$ be an invertible matrix. Prove that there exists two upper triangular matrices $B_1, B_2$ and a permutation matrix $P$ such that $A = B_1 P B_2$. Prove that $P$ is uniquely determined by $A$.

**Proof:**
**Existence:** We proceed by induction on n. The base case $n=1$ is trivial.

Assume the statement holds for all invertible $(n-1)\times(n-1)$ matrices. Let $A$ be an $n\times n$ invertible matrix. Since $A$ is invertible, it has at least one nonzero entry $a_{i_{0}j_{0}}$ whose left and below entries are all zero (i.e., an entry $a_{ij}$ such that $a_{kj}=0$ for all $k>i$ and $a_{il}=0$ for all $l<j$). 

By left‑multiplying a sequence of upper‑triangular elementary matrices, we can eliminate all entries above $a_{i_0j_0}$; by right‑multiplying a sequence of upper‑triangular elementary matrices, we can eliminate all entries to the right of $a_{i_0j_0}$. Then applying the induction hypothesis to the submatrix obtained by deleting row $i_0$ and column $j_0$ completes the proof.

**Uniqueness:**
Suppose $A = B_1 P B_2 = B_1' P' B_2'$, where $B_1, B_1', B_2, B_2'$ are invertible upper‑triangular matrices and $P, P'$ are permutation matrices.  

Let $e_i$ be the $i$-th standard basis vector. Assume, for sake of contradiction, that $Pe_{i}\neq P'e_{i}$ for some $i\leq n$. Then we'll have $Pe_{i}=e_{j}, P'e_{i}=e_{j'}$ where $j\neq j'$. WOLG we suppose $j>j'$.

$A = B_1 P B_2 = B_1' P' B_2'$ yields $P C_{2}=C_{1}P'$, with $C_{2}=B_2  B_2'^{-1},C_{1}= B_{1}^{-1}B_1'$. Since $B_1, B_1', B_2, B_2'$ are invertible upper‑triangular matrices, $C_{1},C_{2}$ are this type of matrices as well. 

Let $v=C_{1}P'e_{i}=PC_{2}e_{i}=v_{1}e_{1}+\dots+v_ne_{n}.$ On one hand, $v=C_{1}P'e_{i}=C_{1}e_{j'}$, which is the $j'$-th column of $C_{1}$. And since $C_{1}$ is upper‑triangular, $v_k = 0$ for $k > j'$, which in particular means $v_{j}=0$. On the other hand, $C_{2}e_{i}$ is the $i$-th column of $C_{1}$, whose $i$-th coordinate is non-zero (as $C_{2}$ is invertible upper‑triangular). However, left-multiplying by $P$ sends the $i$-th coordinate of $C_{2}e_{i}$ to the $j$-th coordinate, which means $v_{j}\neq 0$, contradictory.

Therefore, $Pe_{i}=P'e_{i}$ for any $i\leq n$, so $P=P'$.