___

> [!problem] Problem 1
> Let $A \in M_{n \times n}(\mathbb{C})$. Prove the following identities.
> 
> (i) $e^{tA} = (e^A)^t$.
> 
> (ii) $e^{\overline{A}} = \overline{e^A}$.
> 
> (iii) $e^{-A} = (e^A)^{-1}$.

**Proof:** All verified by applying Jordan's normal form.
___

> [!problem] Problem 2
> Let $A \in M_{n \times n}(\mathbb{C})$. Prove that $e^A$ is invertible.

**Proof:** See problem 1 (iii).
___

> [!problem] Problem 3
> Recall that
> $$ U(n) = \{ X \in GL_n(\mathbb{C}) \mid {}^t\overline{X}X = I \} $$
> We denote
> $$ \mathfrak{u}(n) = \{ A \in M_{n \times n}(\mathbb{C}) \mid e^{tA} \in U(n) (\forall t \in \mathbb{R}) \} $$
> and define the exponential map to be
> $$ \mathfrak{u}(n) \to U(n) $$
> $$ A \mapsto e^A $$
> 
> (i) Find all elements of $\mathfrak{u}(n)$.
> 
> (ii) Prove that $\mathfrak{u}(n)$ forms an $\mathbb{R}$-subspace of $M_{n \times n}(\mathbb{C})$ and compute its $\mathbb{R}$-dimension.
> 
> (iii) Show that the exponential map induces a homeomorphism between a small open neighborhood of $0 \in \mathfrak{u}(n)$ and a small open neighborhood of $I \in U(n)$.
> 
> (iv) Prove that the exponential map is surjective but not injective for all $n \ge 1$.

**Proof:**
**(i)** Let $A \in M_{n \times n}(\mathbb{C})$. $e^{tA} \in U(n) \ \forall t \in \mathbb{R} \iff (e^{tA})^* e^{tA} = I$.
Differentiating at $t=0$ gives $A^* + A = 0$, i.e., $A^* = -A$. Conversely, if $A^* = -A$, then $(e^{tA})^* = e^{tA^*} = e^{-tA} = (e^{tA})^{-1}$, so $e^{tA} \in U(n)$. Thus
$\mathfrak{u}(n) = \{A \in M_n(\mathbb{C}) \mid A^* = -A\}$ (skew-Hermitian matrices).

**(ii)** Check subspace: $0$ is skew-Hermitian. If $A, B$ skew-Hermitian, $(A+B)^* = A^*+B^* = -A-B = -(A+B)$. If $r \in \mathbb{R}$, $(rA)^* = rA^* = -rA$. So $\mathfrak{u}(n)$ is an $\mathbb{R}$-subspace.
Real dimension: Write $A = iH$ with $H$ Hermitian ($H^*=H$). Hermitian matrices have $n$ real diagonal entries and $\frac{n(n-1)}{2}$ complex off-diagonals (each has $2$ real d.o.f.), so real dim of Hermitian matrices is $n + 2 \cdot \frac{n(n-1)}{2} = n^2$. Thus dim$_{\mathbb{R}} \mathfrak{u}(n) = n^2$.

**(iii)** Use inverse function theorem. Exponential map $\exp: M_n(\mathbb{C}) \to GL_n(\mathbb{C})$ is smooth, $d\exp|_0 = \text{id}$. Restrict to $\mathfrak{u}(n) \to U(n)$: at $A=0$, derivative is inclusion $\mathfrak{u}(n) \hookrightarrow T_I U(n)$. $T_I U(n)$ is skew-Hermitian matrices $\mathfrak{u}(n)$ (tangent space to Lie group). So $d\exp|_0: \mathfrak{u}(n) \to \mathfrak{u}(n)$ is identity, invertible. By inverse function theorem, $\exp$ is local diffeomorphism near $0$.

**(iv) Surjective**: For any $U \in U(n)$, $U$ is unitarily diagonalizable: $U = VDV^*$, $D = \text{diag}(e^{i\theta_1}, \dots, e^{i\theta_n})$. Let $\Lambda = \text{diag}(i\theta_1, \dots, i\theta_n)$, then $e^\Lambda = D$, and $A = V\Lambda V^*$ is skew-Hermitian ($A^* = -A$) and $e^A = U$.

**Not injective**: For $n=1$, $U(1) = S^1$, $\mathfrak{u}(1) = i\mathbb{R}$. $e^{i\theta}$ maps $\theta$ and $\theta+2\pi$ to same point. For $n>1$, take $A = \text{diag}(2\pi i, 0, \dots, 0)$ and $B = \text{diag}(0, 2\pi i, 0, \dots, 0)$. Both are skew-Hermitian, $e^A = e^B = I$, but $A \ne B$.