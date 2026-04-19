___

> [!problem] Problem 1
> Let $p$ be a prime number.
> (i) Show that multiplication is well-defined on $\mathbb{Z}/p\mathbb{Z}$.
> (ii) Show that $(\mathbb{Z}/p\mathbb{Z})\setminus\{0\}$ forms a group under multiplication.
> (iii) Show that the group in (ii) is cyclic.

**Proof:**
**(i)** Trivial
**(ii)** Use Bezout's Theorem or the fact that $p\mathbb{Z}$ is a maximal ideal of $\mathbb{Z}$ (thus $\mathbb{Z} / p\mathbb{Z}$ is a field).
**(iii)** Denote $G=(\mathbb{Z} /p \mathbb{Z})\setminus\{ 0 \}$, and denote $\psi(d)$ as the number of elements of order $d$ in $G$. Then by Lagrange' Theorem we have
$$
p-1=\sum_{d\mid p-1}\psi(d).
$$
Let $\phi(d)$ be the Euler's function, i.e. the number of integers less than and coprime with $d$. Then 

___

> [!problem] Problem 2
> For $1 \le n \le 60$, classify groups of order $n$ up to isomorphism.