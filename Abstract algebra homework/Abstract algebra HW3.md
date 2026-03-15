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
> (i) Show that right splitting does not necessarily exists.
> (ii) Show that existence of left splitting implies existence of right splitting.
> (iii) Show that existence of right splitting does not imply existence of left splitting.

**Proof:**
**(i)**

(ii) Suppose there is a left splitting $r: B \to A$ with $r \circ u = \operatorname{Id}_A$. Since the sequence is exact, $u$ is injective, $v$ is surjective, and $\operatorname{Im} u = \ker v$. For each $c \in C$, pick $b_c \in B$ with $v(b_c)=c$ (by surjectivity). Define $s: C \to B$ by $s(c) = b_c \cdot u(r(b_c))^{-1}$. First check that $v(s(c)) = v(b_c) \cdot v(u(r(b_c)))^{-1} = c \cdot 1^{-1} = c$, because $v \circ u = 1$ (since $\operatorname{Im} u = \ker v$). Now we need to show $s$ is a homomorphism. For $c_1, c_2 \in C$,
$$s(c_1 c_2) = b_{c_1 c_2} u(r(b_{c_1 c_2}))^{-1}.$$
On the other hand, $s(c_1)s(c_2) = b_{c_1} u(r(b_{c_1}))^{-1} b_{c_2} u(r(b_{c_2}))^{-1}$. Because $b_{c_1} b_{c_2}$ and $b_{c_1 c_2}$ both map to $c_1 c_2$ under $v$, we have $b_{c_1} b_{c_2} = b_{c_1 c_2} \cdot u(a)$ for some $a \in A$. Applying $r$ to both sides gives $r(b_{c_1}) r(b_{c_2}) = r(b_{c_1 c_2}) a$ (since $r \circ u = \operatorname{Id}_A$). Then $a = r(b_{c_1}) r(b_{c_2}) r(b_{c_1 c_2})^{-1}$. Substituting back,
$$b_{c_1} b_{c_2} = b_{c_1 c_2} u\bigl(r(b_{c_1}) r(b_{c_2}) r(b_{c_1 c_2})^{-1}\bigr).$$
Rearranging,
$$b_{c_1 c_2} = b_{c_1} b_{c_2} u\bigl(r(b_{c_1 c_2}) r(b_{c_2})^{-1} r(b_{c_1})^{-1}\bigr).$$
Now compute
$$\begin{aligned}
s(c_1)s(c_2) &= b_{c_1} u(r(b_{c_1}))^{-1} b_{c_2} u(r(b_{c_2}))^{-1} \\
&= b_{c_1} b_{c_2} \bigl(b_{c_2}^{-1} u(r(b_{c_1}))^{-1} b_{c_2}\bigr) u(r(b_{c_2}))^{-1}.
\end{aligned}$$
Since $u(r(b_{c_1})) \in u(A) = \ker v$, it is central? Not necessarily. We need a different approach: define $s(c)$ as the unique element in $B$ such that $v(s(c)) = c$ and $r(s(c)) = 1_A$. Given $c$, pick any $\tilde b$ with $v(\tilde b) = c$, and set $s(c) = \tilde b \cdot u(r(\tilde b))^{-1}$. Then $v(s(c)) = c$ and $r(s(c)) = r(\tilde b) r(u(r(\tilde b)))^{-1} = r(\tilde b) r(\tilde b)^{-1} = 1$. This $s(c)$ is unique with these properties because if $b$ and $b'$ both satisfy $v(b)=v(b')=c$ and $r(b)=r(b')=1$, then $b^{-1}b' \in \ker v = \operatorname{Im} u$, so $b^{-1}b' = u(a)$ for some $a$, and $1 = r(b') = r(b u(a)) = r(b) r(u(a)) = 1 \cdot a$, so $a=1$, hence $b=b'$. Now check homomorphism: $s(c_1 c_2)$ and $s(c_1)s(c_2)$ both map to $c_1 c_2$ under $v$ and to $1$ under $r$, so by uniqueness they are equal. Thus $s$ is a homomorphism splitting on the right.

(iii) Consider the sequence
$$
1 \to A \xrightarrow{u} A \rtimes_\varphi C \xrightarrow{v} C \to 1
$$
where $A$ is non-abelian, $C$ acts on $A$ via $\varphi: C \to \operatorname{Aut}(A)$, and $A \rtimes_\varphi C$ is the semidirect product. The maps are $u(a)=(a,1_C)$ and $v(a,c)=c$. A right splitting $s: C \to A \rtimes C$ is given by $s(c)=(1_A, c)$, which is a homomorphism because $s(c_1 c_2) = (1, c_1 c_2) = (1, c_1)(1, c_2) = s(c_1) s(c_2)$ (since the action on the identity is trivial). But a left splitting $r: A \rtimes C \to A$ with $r \circ u = \operatorname{Id}_A$ would require $r(a,1)=a$ for all $a \in A$. For $r$ to be a homomorphism, we need $r((a_1, c_1)(a_2, c_2)) = r(a_1, c_1) r(a_2, c_2)$. The product in the semidirect product is $(a_1, c_1)(a_2, c_2) = (a_1 \varphi(c_1)(a_2), c_1 c_2)$. Applying $r$, we get $r(a_1 \varphi(c_1)(a_2), c_1 c_2) = a_1 a_2$. This forces $\varphi(c_1)(a_2) = a_2$ for all $c_1, a_2$, i.e., the action is trivial. So if we choose a nontrivial action, no such $r$ exists. Concrete example: take $A=S_3$, $C=\mathbb{Z}/2\mathbb{Z}$ with the nontrivial action (conjugation by a transposition). Then the right splitting exists as above, but there is no left splitting because the action is nontrivial.



___

