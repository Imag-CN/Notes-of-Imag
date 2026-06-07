___

>[!problem] Problem 1
>Suppose $X \in M_{n \times n}(K)$ is not nilpotent and not invertible. Prove that there exists a polynomial $P(t) \in K[t]$ such that $P(X) \neq 0$, $P(X) \neq 1$, and $P(X)^2 = P(X)$.

**Proof:**
$X \in M_{n \times n}(K)$ is not nilpotent and not invertible means $X$ has some but not all eigenvalues equal to $0$. Therefore $X$ is similar to some $\operatorname{diag}\{ A,B \}$ where $A$ is nilpotent and $B$ is invertible. Let $f(x)=x^{k}+\dots+a_{0}$ be the minimal polynomial of $B^{n}$ ($a_{0}=\pm \det B^{n}\neq{0}$, let $g(x)=-f(x) /a_{0}+1$, then $g(B^{n})=I$. Let $P(x)=g(x^{n})$, then $P(A)=0$, $P(B)=1$. Therefore $P(x)$ suffices the given condition.
___

>[!problem] Problem 2
>Let $A$ be a $K$-algebra such that $\dim_K A$ is finite. Suppose $A$ is not a field. Prove that $A$ is a direct sum of two nonzero $K$-algebras.

**Proof:**
This is not true.

Let $A=K[x] / (x^{2})$, then $\dim_K A = 2$ and $A$ is not a field (since it has nilpotent $x$). If $A$ is a direct sum of two nonzero $K$-algebras, it will have some idempotent other than $0$ or $1$. Suppose $(a+bx)^{2}=a+bx$, then $a^{2}=a$, $2ab=b$, thus $a+bx=0$ or $a+bx=1$, contradiction.
___

>[!problem] Problem 3
>Let $A$ be a $K$-algebra such that $\dim_K A$ is finite. Prove that $A$ is isomorphic to a direct sum of fields.

**Proof:**
This is also not true. Just apply the example above.
___

>[!problem] Problem 4
>Let $L/K$ be a field extension of finite degree. Suppose $L = K(\alpha)$ and the minimal polynomial of $\alpha$ has multiple roots. Prove that $L \otimes_K L$ is not reduced.

**Proof:**
Since $f$ has a multiple root, write $f(t) = (t-\alpha)^2 h(t)$ in $\overline{K}[t]$. Let $x = \alpha \otimes 1 - 1 \otimes \alpha \in L \otimes_K L$.  
In $L \otimes_K \overline{K} \cong \overline{K}[t]/(f(t))$, the element $x$ corresponds to $t-\alpha$. Because $(t-\alpha)^2 = 0$ in $\overline{K}[t]/(f(t))$, we have $x^2 = 0$ in $L \otimes_K L$. Clearly $x \neq 0$, so $x$ is a nonzero nilpotent. Hence $L \otimes_K L$ is not reduced.