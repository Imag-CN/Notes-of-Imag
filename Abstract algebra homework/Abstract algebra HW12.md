___

> [!problem] Problem 1
> Classify groups of order $8$ up to isomorphism. In particular, you need to show that the dihedral group $D_8$ is different from the quaternion group.


> [!problem] Problem 2
> Show that for all prime numbers $p$, the number of non-isomorphic groups of order $p^{3}$ is the same.

**Proof:**
We directly classify group $G$ of order $p^{3}$.

For $G$ abelian, we easily get three types: $C_{p^{3}},C_{p^{2}}\times C_{p},C_{p}\times C_{p}\times C_{p}$.

For $G$ non-abelian, we get several propositions:
1. $\lvert Z(G) \rvert=p$, and $Z(G)$ is the only subgroup of order $p$.
2. For any $g\in G\setminus Z(G)$, $Z(g)$ is a subgroup of order $p^{2}$; Reversely, for subgroup $H<G$ of order $p^{2}$, $H=Z(g)$ for any $g\in H \setminus Z(G)$.
3. Any subgroup $H<G$ of order $p^{2}$ is a normal subgroup.
4. $[G:G]\subset Z(G)$. Furthermore, $(xy)^{k}=x^{k}y^{k}[x,y]^{k(k-1) / 2}$ for any $x,y \in G$ and $k\geq 1$.

Proposition 1,2 is trivial (proof use the fact that groups of order $p^{2}$ is abelian). 

To prove proposition 3, we consider the left multiplication on $G / H$:
$$
G \circlearrowleft G / H: g_{1}(g_{g_{2}}H)=g_{1}g_{2}H
$$
This gives a left action of $G$ on $G / H$, and further gives a homomorphism $\phi: G\to S_{p}$. Since $|S_{p}|=p!$ has factor $p$ of multiplicity only $1$, thus $|\operatorname{im} \phi|=1\text{ or }p$. But $|\operatorname{im}\phi|\neq1$ because is not possible that every element in $G$ fix any coset of $H$. Thus $|\operatorname{im}\phi|=p$, and $|\operatorname{ker}\phi|=p^{2}$. Since $\operatorname{ker}\phi \subset H$ and $|H|=p^{2}$, we have $H=\operatorname{ker}\phi$, thus $H$ is normal.

To prove proposition 4, we consider the quotient map $\pi:G\to G / Z(G)$. This is a homomorphism because $Z(G)$ is normal. And $C/ Z(G)$ is abelian because Thus $\pi()$
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

