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

**Proof:** We proceed by induction on $n$. The base case $n=1$ is degenerate.

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

