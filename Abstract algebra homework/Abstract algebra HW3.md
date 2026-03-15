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
($\Leftarrow$) $B=TU$ with $T$ diagonal, $U$ strictly upper triangular. $T$ normalizes $U$ (conjugation scales off-diagonals), and $U$ is normal in $B$, so $g \in B \implies gUg^{-1} = U$.

($\Rightarrow$) Suppose $gUg^{-1} = U$. For $i < j$, $I + aE_{ij} \in U$ ($a \in \mathbb{C}$), so $g(I+aE_{ij})g^{-1} = I + a gE_{ij}g^{-1} \in U$. Hence $M_{ij}:=gE_{ij}g^{-1}$ is strictly upper triangular for all $i<j$.

Let $g = (g_{pq})$, $g^{-1} = (h_{pq})$. Then $(M_{ij})_{pq} = g_{pi}h_{jq}$. The condition "strictly upper triangular" means $g_{pi}h_{jq} = 0$ for all $p \ge q$.

We prove $g$ is upper triangular. For column 1 ($i=1$), take $j>1$. Then $g_{p1}h_{j1}=0$ for all $p \ge 1$. Since rows of $g^{-1}$ are independent, some $h_{j1} \neq 0$ for $j>1$, so $g_{p1}=0$ for all $p>1$. By induction, assume columns $1,\dots,k-1$ are zero below the diagonal. For column $k$, take $j>k$. Then $g_{pk}h_{jk}=0$ for all $p \ge k$. Because the submatrix of $g^{-1}$ in rows $>k$ and columns $\ge k$ is non‑singular, for each $p>k$ we can choose $j>k$ with $h_{jk} \neq 0$, forcing $g_{pk}=0$. Hence $g$ is upper triangular, i.e., $g \in B$.

**(ii)** Yes for $n=1$ (trivial), but no for $n\geq_{2}$. Because
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
1\to B \hookrightarrow U \overset{f}{\to}T\to 1
$$
where $\hookrightarrow$ is the inclusion map and $f$ is the map which takes the diagonal.
___

> [!problem] Problem 2
> Consider a short exact sequence of groups
> $$
> 1 \longrightarrow A \stackrel{u}{\longrightarrow} B \stackrel{v}{\longrightarrow} C \longrightarrow 1
> $$
> A right splitting is a group homomorphism $s: C \to B$ such that $v \circ s = \mathrm{Id}_C$, and a left splitting is a group homomorphism $r: B \to A$ such that $r \circ u = \mathrm{Id}_A$.
> (i) Show that right splitting does not necessarily exist.
> (ii) Show that existence of left splitting implies existence of right splitting.
> (iii) Show that existence of right splitting does not imply existence of left splitting.

**Proof:**
**(i)** Suppose $c\in C$ is an element of order $n$, then $s(c)\in B$ is of order $n$ since $v \circ s= \mathrm{Id}_{C}$.
Consider the sequence:
$$
1\to 2\mathbb{Z} \hookrightarrow \mathbb{Z} \overset{ \mathrm{mod}2 }{ \to } \mathbb{Z}/2\mathbb{Z}\to{1}
$$
$\bar{1}$ is of order $2$ but there is no element of order $2$ in $\mathbb{Z}$, thus right splitting does not exist. 

**(ii)** Since $v$ is surjective, for any $c\in C$ we can choose $b_{c}\in B$ such that $v(b_{c})=c$.

Let $s(c)=u(r(b_{c}))^{-1} b_{c}$, then $s$ is a group homomorphism and $v \circ s=\mathrm{Id}_{A}$.

**(iii)** Suppose $b\in B$ is an element of order $n$, then $r(b)\in A$ is of order $n$ since $r \circ u= \mathrm{Id}_{A}$.
Consider the sequence:
$$
1 \to C_{3} \to S_{3} \to C_{2} \to 1
$$
Let $x^{3}=y^{2}=1$ and $x^{2}y=yx$, then $C_{3}= <x>,C_{2}= <y>, S_{3}= <x,y>$.
The right splitting exists (consider the inclusion map), but the left splitting doesn't exist since $y\in S_{3}$ is an element of order $2$ while there's no element of order $2$ in $C_{3}$.
___

>[!problem]
>Consider a short exact sequence of groups
>$$
>1 \longrightarrow A \xrightarrow{u} B \xrightarrow{v} C \longrightarrow 1
>$$
>
>(i) Suppose $B$ is finite. Prove that $|B| = |A| \cdot |C|$.
>
>(ii) Suppose both $A$ and $C$ are finite. Prove that $B$ is finite.
>
>(iii) Give an example in which $A$ and $C$ are abelian but $B$ is not.

