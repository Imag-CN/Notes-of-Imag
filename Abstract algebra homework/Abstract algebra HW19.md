___

>[!problem] Problem 1
>Let $D$ be a positive integer such that $D \equiv 1 \mod 4$. Let $R = \mathbb{Z}[\sqrt{-D}]$.
>(i) Let $I$ be a nonzero ideal of $R$. Prove that $R/I$ is finite.
>(ii) Prove that $R$ has Krull dimension $1$.
>(iii) Suppose $R$ is a UFD. Prove that $R$ is a PID.

**Proof:**
**(i)** Let $I$ be a nonzero ideal of $R$. Choose a nonzero element $a \in I$. Since $R$ is a free $\mathbb{Z}$-module of rank $2$, the additive subgroup $\mathbb{Z}a$ has finite index in $R$. The inclusion $\mathbb{Z}a \subset I \subset R$ implies that $|R/I|$ divides $|R/(a)|$, which is finite. Hence $R/I$ is finite.

**(ii)** For any nonzero prime ideal $\mathfrak{p}$, the quotient $R/\mathfrak{p}$ is a finite integral domain, hence a field. Thus $\mathfrak{p}$ is maximal. Therefore every nonzero prime ideal is maximal, so $\dim R = 1$.

**(iii)** We have already proven that $R$ is a Dedekind domain, i.e. every prime ideal in $R$ is maximal. Thus if $R$ is a UFD, it must be a PID.
___

>[!problem] Problem 2
>Let $D$ be a positive integer such that $D \equiv 1 \mod 4$. Assume $D$ is not divisible by $\ell^2$ for any prime number $\ell$. Let $R = \mathbb{Z}[\frac{1+\sqrt{D}}{2}]$.
>(i) Prove that $p \ne R^{\times}$ for any prime number $p$.
>(ii) Let $Q$ be the fraction field of $R$. Let $S$ be a subring of $Q$ containing $R$. Prove that there exists a prime number $p \in S^{\times}$.
>(iii) Let $p$ be a prime number. Assume $R/(p)$ is an integral domain. Find the cardinality of the ring $R/(p)$.

**Proof:**
**(i)** If $p \in R^{\times}$, then $p^{-1} \in R$. Write $p^{-1} = m + n\omega$ with $m, n \in \mathbb{Z}$ and $\omega = \frac{1+\sqrt{D}}{2}$. Then $1 = p(m + n\omega) = pm + pn\omega$, which forces $pn = 0$ (since $1, \omega$ are linearly independent over $\mathbb{Q}$). Hence $n=0$ and $pm=1$, impossible for integer $m$. Thus $p \notin R^{\times}$.

**(ii)** Since $R \subset S \subset Q$, the ring $S$ is an overring of $R$ inside $Q$. For any nonzero $a \in R$, consider the ideal $aR$. Because $R$ is a Dedekind domain (it is the ring of integers of $\mathbb{Q}(\sqrt{D})$), the overring $S$ is obtained by inverting some set of primes of $R$. Since $S$ properly contains $R$, at least one prime ideal of $R$ is inverted. Let $\mathfrak{p}$ be a prime ideal of $R$ with $\mathfrak{p} \cap \mathbb{Z} = (p)$ for a rational prime $p$. If $\mathfrak{p}$ is inverted in $S$, then $p \in \mathfrak{p} \subset R$ and $p$ becomes a unit in $S$. Hence $p \in S^{\times}$.

**(iii)** $R/(p)$ is an integral domain $\iff (p)$ is a prime ideal in $R$. Since $R$ is the ring of integers of $\mathbb{Q}(\sqrt{D})$, the factorization of $(p)$ depends on the Legendre symbol $\big(\frac{D}{p}\big)$. The condition $R/(p)$ integral domain means $(p)$ is inert, i.e., $\big(\frac{D}{p}\big) = -1$. Then $R/(p) \cong \mathbb{F}_{p^2}$. Hence $|R/(p)| = p^2$.
___

>[!problem] Problem 3
>Let $R=\mathbb{C}[x,y]/(y^{2}-x^{3}-1)$.
>(i) Prove that $R$ is an integral domain.
>(ii) Prove that $R$ is not a UFD.

**Proof:**
**(i)** $f(x,y)=y^2-x^3-1$ is irreducible in $\mathbb{C}[x,y]$. Hence $(f)$ is prime, so $R=\mathbb{C}[x,y]/(f)$ is an integral domain.

**(ii)** In $R$, let $X=x+(f), Y=y+(f)$; they satisfy $Y^2=X^3+1=(X+1)(X^2-X+1)$.
- $X+1$ is irreducible: if $X+1=\alpha\beta$, taking norms leads to contradiction in $\mathbb{C}[X]$.
- $X+1$ does not divide $Y$ (since $Y/(X+1)\notin R$).
Thus $Y^2$ factors as $Y\cdot Y$ and as $(X+1)(X^2-X+1)$, two distinct factorizations into irreducibles, so $R$ is not a UFD.
