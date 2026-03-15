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
1\to 2\mathbb{Z} \hookrightarrow \mathbb{Z} \overset{ \mathrm{mod}2 }{ \to } \mathbb{Z}/2\mathbb{Z}\to_{1}
$$
$\bar{1}$ is of order $2$ but there is no element of order $2$ in $\mathbb{Z}$, thus right splitting does not exist. 

**(ii)** 

**(iii)** Suppose $b\in B$ is an element of order $n$, then $r(b)\in A$ is of order $n$ since $r \circ u= \mathrm{Id}_{A}$.
Consider the exact sequence:
Consider the sequence:
$$
1 \to C_{2} \xrightarrow{u} A \rtimes_\varphi C \xrightarrow{v} C \to 1
$$
where $A$ is non-abelian, $C$ acts on $A$ via $\varphi: C \to \operatorname{Aut}(A)$, and $A \rtimes_\varphi C$ is the semidirect product. The maps are $u(a)=(a,1_C)$ and $v(a,c)=c$. A right splitting $s: C \to A \rtimes C$ is given by $s(c)=(1_A, c)$, which is a homomorphism because $s(c_1 c_2) = (1, c_1 c_2) = (1, c_1)(1, c_2) = s(c_1) s(c_2)$ (since the action on the identity is trivial). But a left splitting $r: A \rtimes C \to A$ with $r \circ u = \operatorname{Id}_A$ would require $r(a,1)=a$ for all $a \in A$. For $r$ to be a homomorphism, we need $r((a_1, c_1)(a_2, c_2)) = r(a_1, c_1) r(a_2, c_2)$. The product in the semidirect product is $(a_1, c_1)(a_2, c_2) = (a_1 \varphi(c_1)(a_2), c_1 c_2)$. Applying $r$, we get $r(a_1 \varphi(c_1)(a_2), c_1 c_2) = a_1 a_2$. This forces $\varphi(c_1)(a_2) = a_2$ for all $c_1, a_2$, i.e., the action is trivial. So if we choose a nontrivial action, no such $r$ exists. Concrete example: take $A=S_3$, $C=\mathbb{Z}/2\mathbb{Z}$ with the nontrivial action (conjugation by a transposition). Then the right splitting exists as above, but there is no left splitting because the action is nontrivial.



___

