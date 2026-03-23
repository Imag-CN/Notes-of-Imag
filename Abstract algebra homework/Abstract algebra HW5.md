___

>[!problem] Problem 1
>Count the number of conjugacy classes of $n \times n$ matrices whose eigenvalues are all zero.

**Answer:** $p(n)$, the partition number.
___

>[!problem] Problem 2
>Draw Young diagrams of total size $6$. For each Young diagram of total size $6$, find the number of elements in the conjugacy class of $S_6$ corresponding to it.

**Answer:**
The conjugacy classes of $S_6$ correspond to the partitions of 6, each giving a Young diagram. The number of elements in the conjugacy class for a partition $\lambda$ is:

$$
|C_\lambda| = \frac{6!}{\prod_k (k^{c_k} c_k!)}
$$

where $c_k$ is the number of cycles of length $k$ in the cycle type associated with $\lambda$.

List of partitions, corresponding Young diagrams, and conjugacy class sizes:

| Partition $\lambda$ | Young diagram shape        | Cycle type                        | Size                                   |
| ------------------- | -------------------------- | --------------------------------- | -------------------------------------- |
| (6)                 | ▢▢▢▢▢▢                     | 1×6-cycle                         | $720 / 6 = 120$                        |
| (5,1)               | ▢▢▢▢▢<br>▢                 | 1×5-cycle + 1×1-cycle             | $720/(5\cdot1) = 144$                  |
| (4,2)               | ▢▢▢▢<br>▢▢                 | 1×4-cycle + 1×2-cycle             | $720/(4\cdot2) = 90$                   |
| (4,1,1)             | ▢▢▢▢<br>▢<br>▢             | 1×4-cycle + 2×1-cycles            | $720/(4\cdot2!) = 90$                  |
| (3,3)               | ▢▢▢<br>▢▢▢                 | 2×3-cycles                        | $720/(3^2\cdot2!) = 40$                |
| (3,2,1)             | ▢▢▢<br>▢▢<br>▢             | 1×3-cycle + 1×2-cycle + 1×1-cycle | $720/(3\cdot2\cdot1) = 120$            |
| (3,1,1,1)           | ▢▢▢<br>▢<br>▢<br>▢         | 1×3-cycle + 3×1-cycles            | $720/(3\cdot3!) = 40$                  |
| (2,2,2)             | ▢▢<br>▢▢<br>▢▢             | 3×2-cycles                        | $720/(2^3\cdot3!) = 15$                |
| (2,2,1,1)           | ▢▢<br>▢▢<br>▢<br>▢         | 2×2-cycles + 2×1-cycles           | $720/(2^2\cdot2!\cdot1^2\cdot2!) = 45$ |
| (2,1,1,1,1)         | ▢▢<br>▢<br>▢<br>▢<br>▢     | 1×2-cycle + 4×1-cycles            | $720/(2\cdot4!) = 15$                  |
| (1,1,1,1,1,1)       | ▢<br>▢<br>▢<br>▢<br>▢<br>▢ | 6×1-cycles                        | $720/(1^6\cdot6!) = 1$                 |

Sum: $120+144+90+90+40+120+40+15+45+15+1 = 720 = 6!$, as expected.

___

>[!problem] Problem 3
>Compute the dimension of the symplectic groups as manifolds

**Answer**:
Define $F: \mathrm{GL}(2n, \mathbb{R}) \to \mathfrak{so}(2n, \mathbb{R})$ by $F(A)=A^\top J A$, where $J = \begin{pmatrix}0 & I_n \\ -I_n & 0\end{pmatrix}$. Then $\mathrm{Sp}(2n,\mathbb{R}) = F^{-1}(J)$.

Compute derivative: for $H \in T_A\mathrm{GL}(2n,\mathbb{R})$,  
$$
DF_A(H) = H^\top J A + A^\top J H.
$$

Let $K = A^{-1}H$. Using $A^\top J A = J$, we get $DF_A(H) = K^\top J + J K$.

This defines a linear map $\phi: M_{2n}(\mathbb{R}) \to \mathfrak{so}(2n,\mathbb{R})$ by $\phi(K)=K^\top J + J K$.

- Domain dimension: $\dim M_{2n}(\mathbb{R}) = 4n^2$
- Target dimension: $\dim \mathfrak{so}(2n,\mathbb{R}) = 2n^2 - n$
- Kernel: $\ker\phi = \{K \mid K^\top J + J K = 0\}$, which is $\mathfrak{sp}(2n,\mathbb{R})$ of dimension $2n^2+n$

Since $\dim \ker\phi + \dim \mathrm{im}\,\phi = \dim M_{2n}(\mathbb{R})$,  
$\dim \mathrm{im}\,\phi = 4n^2 - (2n^2+n) = 2n^2 - n = \dim \mathfrak{so}(2n,\mathbb{R})$, so $\phi$ is surjective.

Thus $DF_A$ is surjective, so by the constant rank theorem, $\mathrm{Sp}(2n,\mathbb{R})$ is a smooth manifold of dimension:

$$
\dim \mathrm{Sp}(2n,\mathbb{R}) = 4n^2 - (2n^2 - n) = 2n^2 + n.
$$
___

>[!problem] Problem 4
>Try to find asymptotic behavior of the number of conjugacy classes of $S_n$ when $n$ tends to infinity.

**Answer:** It's known that:
$$
p(n)\sim \dfrac{1}{4n\sqrt{ 3 }}\exp{ \left( \pi \sqrt{ \dfrac{2n}{3} } \right)  },n\to \infty
$$
___

>[!problem] Problem 5
>Prove that conjugacy is an equivalence relation between elements of a group.

**Proof:**
Let $G$ be a group. For $x, y \in G$, we say $x \sim y$ if there exsists $g \in G$ such that $gxg^{-1} = y$.

1. **Reflexivity**: $x \sim x$ because $e x e^{-1} = x$ (with $g = e$, the identity).
2. **Symmetry**: If $x \sim y$, then $\exists\, g$ with $g x g^{-1} = y$. Then $g^{-1} y (g^{-1})^{-1} = g^{-1} y g = x$, so $y \sim x$.
3. **Transitivity**: If $x \sim y$ and $y \sim z$, then $\exists\, g, h$ with $g x g^{-1} = y$ and $h y h^{-1} = z$. Then $(hg) x (hg)^{-1} = h (g x g^{-1}) h^{-1} = h y h^{-1} = z$, so $x \sim z$.

Therefore, conjugacy is an equivalence relation on $G$.
___

>[!problem] Problem 6
>Find two elements $A, B \in SL_2(\mathbb{R})$ which are conjugate in $SL_2(\mathbb{C})$ but are not conjugate in $SL_2(\mathbb{R})$.

**Proof:** Let $A=\begin{pmatrix}0 &-1 \\ 1 &0\end{pmatrix}, B=\begin{pmatrix}0 &1 \\ -1 &0\end{pmatrix}$, then
$$
B=\begin{pmatrix}i &0 \\ 0 &-i\end{pmatrix}A\begin{pmatrix}-i &0 \\ 0 &i\end{pmatrix},
$$
thus $A,B$ are conjugate in $SL_2(\mathbb{C})$.

Suppose
$$
B=\begin{pmatrix}a &b \\ c &d\end{pmatrix}^{-1}A\begin{pmatrix}a &b \\ c &d\end{pmatrix},\text{ i.e.} \begin{pmatrix}a &b \\ c &d\end{pmatrix}B=A\begin{pmatrix}a &b \\ c &d\end{pmatrix},
$$
where $a,b,c,d\in \mathbb{R}$ and $ad-bc=1$, then
$$
\begin{pmatrix}-b &a \\ -d &c\end{pmatrix}=\begin{pmatrix}-c &-d \\ a &b\end{pmatrix}.
$$
Thus $-a^{2}-b^{2}=1$, contradiction.

