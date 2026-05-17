___

>[!problem] Problem 1
>Let $D$ be an integer which is not a perfect square. Let $K = \mathbb{Q}(\sqrt{D}) = \{a + b\sqrt{D} \mid a, b \in \mathbb{Q}\}$.
>(i) Find all elements $x \in K$ such that the identity $x^{n} + a_{n - 1} x^{n - 1} + \cdots + a_{1} x + a_{0} = 0$ holds for some $a_{0}, \dots, a_{n - 1} \in \mathbb{Z}$.
>(ii) Denote the elements in (i) as $\mathcal{O}_{K}$. Prove that $\mathcal{O}_{K}$ is a subring of $K$.
>(iii) Let $J$ be an ideal of $\mathcal{O}_{K}$. Let $\overline{J} = \{a + b\sqrt{D} \in \mathcal{O}_{K} \mid a - b\sqrt{D} \in J\}$. Prove that the product of ideals $J \cdot \overline{J}$ is a principal ideal.

**Proof:**
**(i)** The algebraic integers in $K$ are:
$$
\mathcal{O}_K = 
\begin{cases}
\mathbb{Z}\bigl[\frac{1+\sqrt{D}}{2}\bigr], & D \equiv 1 \pmod{4},\\
\mathbb{Z}[\sqrt{D}], & D \equiv 2,3 \pmod{4}.
\end{cases}
$$
Reason: For $x = a+b\sqrt{D}$ with $a,b\in\mathbb{Q}$, the minimal polynomial is $t^2-2at+(a^2-Db^2)$. For it to have integer coefficients, $2a\in\mathbb{Z}$ and $a^2-Db^2\in\mathbb{Z}$. Let $2a = A\in\mathbb{Z}$, then $a^2-Db^2 = (A^2-4Db^2)/4\in\mathbb{Z}$. Hence $A^2\equiv 4Db^2 \pmod{4}$. This forces $A$ and $2b$ to have same parity, yielding the two cases.

**(ii)** $\mathcal{O}_K$ contains $0,1$, is closed under $+$, $-$ and $\cdot$ (sum/product of algebraic integers is algebraic integer), hence a subring.

**(iii)** Norm map $N(a+b\sqrt{D}) = a^2-Db^2$ is multiplicative. For ideal $J$, $J\overline{J}$ consists of sums $\sum j_i\bar{k}_i$ with $j_i,k_i\in J$. 
- Every element of $J\overline{J}$ is an integer (since $j\bar{k} = N(j)k/j \in \mathbb{Z}$).
- Thus $J\overline{J} = (n)$ for some $n\in\mathbb{Z}_{\ge0}$.
- Taking norms: $N(J\overline{J}) = N(J)N(\overline{J}) = N(J)^2 = n^2$, so $n = N(J)$.
Hence $J\overline{J} = (N(J))$ is principal.
___



