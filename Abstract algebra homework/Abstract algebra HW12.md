___

> [!problem] Problem 1
> Classify groups of order $8$ up to isomorphism. In particular, you need to show that the dihedral group $D_8$ is different from the quaternion group.


> [!problem] Problem 2
> Show that for all prime numbers $p$, the number of non-isomorphic groups of order $p^{3}$ is the same.

**Proof:**
We directly classify group $G$ of order $p^{3}$ to solve these two problems at the same time.

For $G$ abelian, we easily get three types: $C_{p^{3}},C_{p^{2}}\times C_{p},C_{p}\times C_{p}\times C_{p}$.

For $G$ non-abelian, we get several propositions:
1. $\lvert Z(G) \rvert=p$.
2. For any $g\in G\setminus Z(G)$, $Z(g)$ is a subgroup of order $p^{2}$; Reversely, for subgroup $H<G$ of order $p^{2}$, $H=Z(g)$ for any $g\in H \setminus Z(G)$.
3. Any subgroup $H<G$ of order $p^{2}$ is a normal subgroup.
4. $[G,G]\subset Z(G)$. Furthermore, $(xy)^{k}=x^{k}y^{k}[y,x]^{k(k-1) / 2}$ for any $x,y \in G$ and $k\geq 1$.

Proposition 1,2 is trivial (proof use the fact that groups of order $p^{2}$ is abelian). 

To prove proposition 3, we consider the left multiplication on $G / H$:
$$
G \circlearrowleft G / H: g_{1}(g_{g_{2}}H)=g_{1}g_{2}H
$$
This gives a left action of $G$ on $G / H$, and further gives a homomorphism $\phi: G\to S_{p}$. Since $|S_{p}|=p!$ has factor $p$ of multiplicity only $1$, thus $|\operatorname{im} \phi|=1\text{ or }p$. But $|\operatorname{im}\phi|\neq1$ because is not possible that every element in $G$ fix any coset of $H$. Thus $|\operatorname{im}\phi|=p$, and $|\operatorname{ker}\phi|=p^{2}$. Since $\operatorname{ker}\phi \subset H$ and $|H|=p^{2}$, we have $H=\operatorname{ker}\phi$, thus $H$ is normal.

To prove proposition 4, we consider the quotient map $\pi:G\to G / Z(G)$. This is a homomorphism because $Z(G)$ is normal. And $C/ Z(G)$ is abelian because it is of order $p^{2}$. Thus $\pi(x ^{-1} y^{-1} xy)=1$ for any $x,y \in G$, so $[G,G]\subset Z(G)$. For $(xy)^{k}=xyxy\dots xy$, transferring $yx$ into $xy$ generates a $[y,x]$, which is in $Z(G)$ so we can place it to the tail. We can do such transfer for $1+2+\dots k-1=k(k-1) / 2$ times to gather all $x$s and $y$s. Therefore we have $(xy)^{k}=x^{k}y^{k}[y,x]^{k(k-1) / 2}$.

Now we consider the situation when $p=2$:
Suppose all elements are of order $2$ (except the identity), then $xy=(xy)^{-1}=y^{-1}x ^{-1}=yx$ for any $x,y \in G$, contradicting to that $G$ is non-abelian. Therefore there exists an element $a$ of order $4$. Then by proposition 1,2 we have $Z(a)=\left< a \right> =\{ e,a,a^{2},a^{3} \}$ and $Z(G)=\{ e,a^{2} \}$. And $Z(a)$ is normal by proposition 3 (or simply because $[G:Z(a)]=2$).

- Suppose there exist a $2$-orderd element $b\in G\setminus Z(a)$, then $bab^{-1}=a^{3}$ (easily verify that this is the only possibility). Then $G= \left< a,b \mid a^{4}=b^{2}=1, bab^{-1}=a\right>$, which is isomorphic to $D_{8}$.

- Suppose any element $b\in G\setminus Z(a)$ is of order $4$, then take such a $b$. Since $ab \not\in$ and $Z(a)$, $ab$ is another element of order $4$. Let $c=ab$, then $\left< a \right>\cup\left< b \right>\cup \left< c \right>$ contains $8$ elements, thus $G= \left< a,b,c\mid a^{4}=1,a^{2}=b^{2}=c^{2}, ab=c \right>$, which is isomorphic to $Q_{8}$.

Finally, we consider the situation when $p>2$:
- Suppose there exists a $p^{2}$-ordered element $a$. Then $Z(a)=\left< a \right>$ is a normal subgroup by proposition 3. Let $z=a^{p}$, then $\left< z \right> = Z(G)$ by proposition 1. Take $b'\in G\setminus \left< a \right>$, and suppose ${b'}^{p}=z^{r}$ (the p-th power of any element lies in the center by proposition 1). Let $b=b'a^{-r}\notin \left< a \right>$, then $b^{p}={b'}^{p}a^{p}[a,b]^{p(p-1) / 2}=[a,b]^{p(p-1) / 2}$ by proposition 4. Again by proposition 4, we have $[a,b]\in Z(G)$, thus $[a,b]^{p(p-1) / 2}=e$ because $p \mid p(p-1)/2$ (this is the key difference between $p=2$ and $p>2$). Therefore $b^{p}=1$, and then $G=\left< a \right> \ltimes_{\varphi} \left< b \right>$. Any element in $\left< a \right>$ has the unique form $a^{np+r}$ where $n,r \in \{ 0,1,\dots,p-1 \}$. Since $(a^{np+r})^{p}=a^{rp}=z^{r}$, every element $z^{r}$ in $Z(G)$ has exactly $p$ distinct $p$-roots $a^{{np+r}}$,$n=0,1,\dots p-1$ in $\left< a \right>$. Since $bzb^{-1}=z$, we have $bab^{-1}=a^{np+1}$ for some $n \in \{ 1,2,\dots p-1\}$ (since $bab^{-1}$ is a $p$-th root of $z$). Let $m$ be the inverse of $n$ in $\mathbb{Z} / p \mathbb{Z}$, then $b^{r}ab^{-r}=a^{p+1}$ and we can replace $b^{r}$ with $b''$. Thus W.O.L.G we can assume $n=1$. Therefore we have $G=\left< a,b \mid a^{p^{2}}=b^{p}=1,bab^{-1}=a^{1+p}\right>$. We have a representation of this group:
$$
a=\begin{pmatrix}
\omega &&&&\\
&\omega^{1+p}&&&\\
&&\omega^{(1+p)^{2}}&& \\
&&&\ddots &\\
&&&&\omega^{(1+p)^{1-p}}
\end{pmatrix},
b=\begin{pmatrix}
0&I_{p-1} \\
1&0
\end{pmatrix}
$$
  where $a,b \in GL_{p}(\mathbb{C})$ and $\omega=e^{2\pi i / p^{2}}$.

 - Suppose all elements are of order $p$. Pick $a\in Z(G)$, $b\in G \setminus Z(G)$, and $c \in G\setminus Z(b)$. Then $Z(b)=\left< a \right>\times \left< b \right>$ is a normal subgroup by proposition 3. Suppose $cbc^{-1}=a^{i}b^{j}$, where $i,j \in \{ 0,1,\dots p-1 \}$, then by induction we have $c^{k}bc^{-k}=a^{i(1+p+\dots+p^{k-1})}b^{j^{k}}$ for $k\geq 1$. Thus $b=c^{p}bc^{-p}=a^{i(1+p+\dots p^{p-1})}b^{j^{p}}$. Therefore $p \mid j^{p}-1$, thus $j=1$. Since $a^{i}\neq e$, we can replace $a^{i}$ with $a$. Thus W.O.L.G we can assume $i=p-1$. Then $cbc^{-1}=a^{-1}b$, and then $b^{-1}c^{-1}bc=a$. Therefore we have $G=\left< a,b,c \mid a^{p}=b^{p}=c^{p}=e,[a,b]=[a,c]=1,[b,c]=a\right>$. We have a representation of this group:
$$
a=\begin{pmatrix}
1&0&1 \\
0&1&0 \\
0&0&1
\end{pmatrix},
b=\begin{pmatrix}
1&1&0 \\
0&1&0 \\
0&0&1
\end{pmatrix},
c=\begin{pmatrix}
1&1&0 \\
0&1&0 \\
0&0&1
\end{pmatrix}
$$
   where $a,b,c \in GL_{3}(F_{p})$. The elements in this group are all upper triangular matrices with all diagonal entries equal to $1$.

In conclusion, there are $5$ groups of order $p^{3}$ up to isomorphism for any prime $p$.
___

> [!problem] Problem 3
> Compute the centers of the groups $SO(n)$, $O(n)$, $SU(n)$, $U(n)$, $GL_{n}(\mathbb{R})$.

**Proof:**
**1.** $Z(GL_{n}(\mathbb{R}))$
A matrix $A$ commutes with all invertible matrices if and only if it is a scalar multiple of the identity. Thus,
$$Z(GL_{n}(\mathbb{R})) = \{\lambda I_n \mid \lambda \in \mathbb{R},\ \lambda \neq 0\}.$$

**2.** $Z(O(n))$
$O(n) = \{A \in M_{n}(\mathbb{R}) \mid A^T A = I\}$. Any $A \in Z(O(n))$ must commute with all orthogonal matrices. In particular, it must commute with all permutation matrices (which are orthogonal) and all rotation matrices in $SO(2)$ subgroups. This forces $A$ to be a scalar matrix. The only scalars $\lambda$ satisfying $(\lambda I)^T(\lambda I) = \lambda^2 I = I$ are $\lambda = \pm 1$. Therefore,
$$Z(O(n)) = \{I_n, -I_n\}.$$

**3. $Z(SO(n))$**
$SO(n) = \{A \in O(n) \mid \det A = 1\}$. The same scalar condition applies, but now we also require $\det(\lambda I) = \lambda^n = 1$.
- For $n$ even: $\lambda = \pm 1$, but $\det(-I) = (-1)^n = 1$, so both are in $SO(n)$. Thus $Z(SO(n)) = \{I_n, -I_n\}$ for even $n > 2$.
- For $n$ odd: $\lambda = \pm 1$, but $\det(-I) = (-1)^n = -1$, so $-I \notin SO(n)$. Thus $Z(SO(n)) = \{I_n\}$ for odd $n$.
- Special case $n=2$: $SO(2)$ is abelian, so $Z(SO(2)) = SO(2)$.

**4. $Z(U(n))$**
$U(n) = \{A \in M_{n}(\mathbb{C}) \mid A^* A = I\}$. A matrix that commutes with all unitary matrices must be a scalar matrix. Let $A = \lambda I$. The condition $(\lambda I)^*(\lambda I) = |\lambda|^2 I = I$ gives $|\lambda| = 1$. Therefore,
$$Z(U(n)) = \{\lambda I_n \mid \lambda \in \mathbb{C},\ |\lambda|=1\}.$$

**5. $Z(SU(n))$**
$SU(n) = \{A \in U(n) \mid \det A = 1\}$. Again, $A$ must be scalar: $A = \lambda I$. The conditions are $|\lambda| = 1$ (from unitarity) and $\det(\lambda I) = \lambda^n = 1$. Thus,
$$Z(SU(n)) = \{\lambda I_n \mid \lambda^n = 1,\ |\lambda|=1\} = \{\lambda I_n \mid \lambda^n = 1\} .$$
___

> [!problem] Problem 4
> The compact symplectic group is defined to be
>$$
>\operatorname{Sp}(n) := U(2n) \cap \operatorname{Sp}_{2n}(\mathbb{C})
>$$
>Compute its center.

**Proof:**
Let $G=\operatorname{Sp}(n)=U(2n)\cap\operatorname{Sp}_{2n}(\mathbb{C})$ with $J=\begin{pmatrix}0&I_n\\-I_n&0\end{pmatrix}$.
Find $Z(G)=\{A\in G\mid AB=BA\ \forall B\in G\}$.

**1. Form of central elements**

Write $A=\begin{pmatrix}X&Y\\Z&W\end{pmatrix}$.
For all $U\in U(n)$, $B_U=\begin{pmatrix}U&0\\0&\overline{U}\end{pmatrix}\in G$.
$AB_U=B_U A$ forces $X=\lambda I_n$, $W=\mu I_n$ (Schur).
Also $AJ=JA$ gives $W=X$, $Z=-Y$.
Thus $A=\begin{pmatrix}\lambda I_n&Y\\-Y&\lambda I_n\end{pmatrix}$.

**2. Symplectic condition**

$A^T J A=J$ gives $\lambda(Y^T-Y)=0$ and $\lambda^2 I_n+Y^T Y=I_n$.
Assume $\lambda\neq0$ for nontrivial center, then $Y=Y^T$.

**3. Unitarity**

$A^*A=I_{2n}$ gives $|\lambda|^2 I_n+Y^* Y=I_n$ and $\bar{\lambda}Y=\lambda Y^*$.
Since $Y=Y^T$, $Y^*=\overline{Y}$, so $\bar{\lambda}Y=\lambda\overline{Y}$.

**4. Solving**

From Step 2: $\lambda^2+Y^2=I_n$.
From Step 3: $|\lambda|^2+Y^*Y=I_n$ and $Y^*=Y^T$ (real symmetric).
Hence $Y^2$ is scalar, so $Y=t I_n$, $t\in\mathbb{R}$.
Then $\lambda^2+t^2=1$, and $\lambda$ real (from $\bar{\lambda}Y=\lambda\overline{Y}$).

**5. Result**

$A=\begin{pmatrix}\lambda I_n&t I_n\\-t I_n&\lambda I_n\end{pmatrix}$ with $\lambda,t\in\mathbb{R}$, $\lambda^2+t^2=1$.
Equivalently, $A=\cos\theta\cdot I_{2n}+\sin\theta\cdot J$.

Therefore
$$
Z(\operatorname{Sp}(n))=\{\lambda I_{2n}+\mu J\mid \lambda,\mu\in\mathbb{R},\ \lambda^2+\mu^2=1\}\cong U(1).
$$
___

> [!problem] Problem 5
> Prove that the center is always a normal subgroup.

**Proof:**
Let $G$ be a group. Take any $x \in G$ and $y \in Z(G)$. Then $xyx^{-1}=y \in Z(G)$ because $xy=yx$. Thus $Z(G)$ is a normal subgroup.
___

>[!problem] Problem 6
>Let $g \in SL_{2}(\mathbb{Z})$. Prove that the following statements are equivalent.  
>(i) The centralizer of $g$ is finite.  
>(ii) The trace of $g$ is in $\{-1, 0, 1\}$.  
>(iii) The element $g$ is not in the center of $SL_{2}(\mathbb{Z})$, and the order of $g$ is finite.

**Proof:**
**(i)$\Rightarrow$(iii):** Obvious.

**(iii)$\Rightarrow$(ii)**: Suppose $g^{k}=e$. Let $\lambda_{1},\lambda_{2}$ be the eigenvalue of $g$. Denote $\chi_{g}(z)=z^{2}-\operatorname{tr}g\cdot z+1$ the characteristic polynomial of $g$. That $g^{k}=g^{2k}=e$ indicates $\lambda_{1}^{k}+\lambda_{2}^{k}=2$ and $\lambda_{1}^{2k}+\lambda_{2}^{2k}=2$. Thus $\lambda_{1}^{k}=\lambda_{2}^{k}=1$, then we have $|\operatorname{tr}g|\leq|\lambda_{1}|+|\lambda_{2}|=2$. Since $\operatorname{tr}g$ is an integer and $\operatorname{tr}g=\pm 2$ yields $g=\pm e$ (which is in the center of $SL_{2}(\mathbb{Z})$), $\operatorname{tr}g$ must lie in $\{ -1,0,1 \}$.

**(ii)$\Rightarrow$(i):** Respectively, there exists $p \in SL_{2}(\mathbb{Z})$ such that $pgp ^{-1}$ is equal to $\begin{pmatrix}0&-1 \\ 1&-1\end{pmatrix}$, $\begin{pmatrix}0&-1 \\ 1&0\end{pmatrix}$,  $\begin{pmatrix}0&-1 \\ 1&1\end{pmatrix}$ if $\operatorname{tr}g=-1,0,1$ (conjugates in $\mathbb{C}$ iff in $\mathbb{Q}$ iff in $\mathbb{Z}$). Suppose $gh=hg$ and let $php^{-1}=\begin{pmatrix}a&b \\ c&d\end{pmatrix}\in SL_{2}(\mathbb{Z})$, then solving for $php^{-1}$ gives that there are only finite selections of $h$ (they are all powers of $g$).