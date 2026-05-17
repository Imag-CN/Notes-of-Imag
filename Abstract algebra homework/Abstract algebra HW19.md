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

