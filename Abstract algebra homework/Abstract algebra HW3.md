___

> [!problem] Problem 1
> Let $G = GL_n(\mathbb{C})$. Let $B$ be the subgroup of $G$ containing upper triangular invertible matrices. Let $U$ be the subgroup of $B$ containing those matrices with diagonal entries equal to $1$. Let $T$ be the subgroup of $B$ containing diagonal matrices.
> 
> (i) Prove that an element $g \in G$ satisfies $gUg^{-1} = U$ if and only if $g \in B$.
> 
> (ii) Decide whether $B$ is a normal subgroup of $G$.
> 
> (iii) Fit $B$, $U$, $T$ into a short exact sequence.

**Proof: (i)**
**($\Rightarrow$)** 

**(ii)** Yes for $n=1$ (trivial) but no for $n\geq_{2}$. Because
$$
\begin{pmatrix}
1&0 \\
-1&1 \\
\end{pmatrix}\cdot
\begin{pmatrix}
1&1 \\
0&1 \\
\end{pmatrix}\cdot
\begin{pmatrix}
1&0 \\
1&1 \\
\end{pmatrix}=
\begin{pmatrix}
2&1 \\
-1&0 \\
\end{pmatrix}\not\in B.
$$
And for a matrix of order $n>2$, consider the block diagonal construction consisting of the $2$-order matrix mentioned above and the $(n-2)$-order identity matrix.

**(iii)**
Consider
$$
1\to B \hookrightarrow U \overset{f}{\to}T
$$
where $\hookrightarrow$ is the inclusion map and $f$ is taking diagonal.