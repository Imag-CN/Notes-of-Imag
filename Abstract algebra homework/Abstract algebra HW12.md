___

> [!problem] Problem 1
> Classify groups of order $8$ up to isomorphism. In particular, you need to show that the dihedral group $D_8$ is different from the quaternion group.


> [!problem] Problem 2
> Show that for all prime numbers $p$, the number of non-isomorphic groups of order $p^{3}$ is the same.

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
$$Z(U(n)) = \{\lambda I_n \mid \lambda \in \mathbb{C},\ |\lambda| = 1\} \cong S^1.$$

**5. $Z(SU(n))$**
$SU(n) = \{A \in U(n) \mid \det A = 1\}$. Again, $A$ must be scalar: $A = \lambda I$. The conditions are $|\lambda| = 1$ (from unitarity) and $\det(\lambda I) = \lambda^n = 1$. Thus,
$$Z(SU(n)) = \{\lambda I_n \mid \lambda^n = 1,\ |\lambda|=1\} = \{\lambda I_n \mid \lambda^n = 1\} \cong \mathbb{Z}/n\mathbb{Z}.$$

**Summary**
- $Z(GL_{n}(\mathbb{R})) = \{\lambda I_n \mid \lambda \in \mathbb{R}^\times\}$
- $Z(O(n)) = \{I_n, -I_n\}$
- $Z(SO(n)) = 
\begin{cases}
SO(2), & n=2 \\
\{I_n, -I_n\}, & n \ \text{even}, n>2 \\
\{I_n\}, & n \ \text{odd}
\end{cases}$
- $Z(U(n)) = \{\lambda I_n \mid |\lambda| = 1\} \cong S^1$
- $Z(SU(n)) = \{\lambda I_n \mid \lambda^n = 1\} \cong \mathbb{Z}/n\mathbb{Z}$

___

