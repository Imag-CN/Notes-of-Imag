___

> [!problem] Problem 1
> Let $p$ be a prime number.
> (i) Show that multiplication is well-defined on $\mathbb{Z}/p\mathbb{Z}$.
> (ii) Show that $(\mathbb{Z}/p\mathbb{Z})\setminus\{0\}$ forms a group under multiplication.
> (iii) Show that the group in (ii) is cyclic.

**Proof:**
**(i)** Trivial
**(ii)** Use Bezout's Theorem or the fact that $p\mathbb{Z}$ is a maximal ideal of $\mathbb{Z}$ (thus $\mathbb{Z} / p\mathbb{Z}$ is a field).
**(iii)** Denote $G=(\mathbb{Z} /p \mathbb{Z})\setminus\{ 0 \}$, and denote $\psi(d)$ as the number of elements of order $d$ in $G$ ($d$ is a divisor of $p-1$). Then by Lagrange' Theorem we have
$$
p-1=\sum_{d\mid p-1}\psi(d).
$$
Suppose $b$ is a $d$-ordered element, then $b^{i},i=1,2,\dots d$ satisfies $(b^{i})^{d}=1$, thus they are the entire and distinct roots of $x^{d}-1$ ($\mathbb{Z}/ p \mathbb{Z}$ is a field, thus this polynomial has at most $d$ roots).
Also, we have $\operatorname{ord}(b^{i})=d / \operatorname{gcd}(i,d)$. Let $\phi(d)$ be the Euler's function, i.e. the number of integers less than and coprime with $d$. Then we have $\psi(d)=\phi(d)$ if $\psi(d)>0$, thus $\psi(d)\leq \phi(d)$.

On the other hand, consider $p-1$ fractions:
$$
\dfrac{1}{p-1}, \dfrac{2}{p-1}, \dots , \dfrac{p-1}{p-1},
$$
and write them into reduced form. The number of $d$ appearing in the denominator is $\phi(d)$. Therefore, we have
$$
p-1=\sum_{d \mid p-1} \phi(d).
$$
So $\psi(d)=\phi(d)$, and specifically $\phi(p-1)=\psi(p-1)>0$. Therefore, $G$ is cyclic.
___

> [!problem] Problem 2
> For $1 \le n \le 60$, classify groups of order $n$ up to isomorphism.