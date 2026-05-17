___

>[!problem] Problem 1
>Let $D$ be a positive integer such that $D \equiv 1 \mod 4$. Let $R = \mathbb{Z}[\sqrt{-D}]$.
>(i) Let $I$ be a nonzero ideal of $R$. Prove that $R/I$ is finite.
>(ii) Prove that $R$ has Krull dimension $1$.
>(iii) Suppose $R$ is a UFD. Prove that $R$ is a PID.

**Proof:**
**(i)** Let $I$ be a nonzero ideal of $R$. Choose a nonzero element $a \in I$. Since $R$ is a free $\mathbb{Z}$-module of rank $2$, the additive subgroup $\mathbb{Z}a$ has finite index in $R$. The inclusion $\mathbb{Z}a \subset I \subset R$ implies that $|R/I|$ divides $|R/(a)|$, which is finite. Hence $R/I$ is finite.

**(ii)** For any nonzero prime ideal $\mathfrak{p}$, the quotient $R/\mathfrak{p}$ is a finite integral domain, hence a field. Thus $\mathfrak{p}$ is maximal. Therefore every nonzero prime ideal is maximal, so $\dim R = 1$.

**(iii)** Assume $R$ is a UFD. Let $I$ be a nonzero ideal. Since $R$ is Noetherian (every ideal is finitely generated), we can pick a nonzero element $a \in I$ with minimal norm $N(a)$ (where $N(x+y\sqrt{-D}) = x^{2}+Dy^{2}$). For any $b \in I$, write $b = aq + r$ in the fraction field $\mathbb{Q}(\sqrt{-D})$ with $N(r) < N(a)$. But $r = b - aq \in I$, so minimality of $N(a)$ forces $r = 0$. Hence $b = aq$. Since $R$ is a UFD, $q$ must belong to $R$ (otherwise denominators would appear). Therefore $I = (a)$ is principal. Thus $R$ is a PID.