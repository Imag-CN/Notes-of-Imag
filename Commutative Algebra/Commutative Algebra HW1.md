___

>[!problem] [ATI] 1.22
>Let $A = \prod_{i=1}^{n} A_{i}$ be the direct product of rings $A_{i}$. Show that $\operatorname{Spec}(A)$ is the disjoint union of open (and closed) subspaces $X_{i}$, where $X_{i}$ is canonically homeomorphic with $\operatorname{Spec}(A_{i})$.
>
>Conversely, let $A$ be any ring. Show that the following statements are equivalent:
>i) $X = \operatorname{Spec}(A)$ is disconnected.
>ii) $A \cong A_{1} \times A_{2}$ where neither of the rings $A_{1}, A_{2}$ is the zero ring.
>iii) $A$ contains an idempotent $\neq 0, 1$.
>In particular, the spectrum of a local ring is always connected.

**Proof:**
Consider the projection maps $\pi_i: A \rightarrow A_i$. Then the map $i \mapsto \mathfrak{p} \leftrightarrow \pi_i^{-1}(\mathfrak{p})$ gives a bijection between $\operatorname{Spec}(A_i)$ and the set of prime ideals of $A$ containing $I_i = \operatorname{Ker}(\pi_i)$. The $I_i$ are mutually orthogonal idempotent ideals ($I_i I_j = 0$ for $i \neq j$ and $I_i^2 = I_i$) and $\sum_{i=1}^n I_i = A$. Hence, $\operatorname{Spec}(A)$ is the disjoint union of the closed (and open) sets $V(I_i)^c = D(I_i)$, each homeomorphic to $\operatorname{Spec}(A_i)$ via the map induced by $\pi_i$.
___
i) $\Rightarrow$ ii): If $\operatorname{Spec}(A) = U_1 \cup U_2$ is a disconnection, then $U_i = D(e_i)$ for some idempotents $e_1, e_2$ with $e_1 + e_2 = 1$ and $e_1 e_2 = 0$. The map $A \rightarrow A/(e_1) \times A/(e_2)$ is an isomorphism. Since $U_i$ are non-empty, $(e_i) \neq (1)$, so $A/(e_i)$ are non-zero rings.

ii) $\Rightarrow$ iii): Let $\psi: A \rightarrow A_1 \times A_2$ be an isomorphism. Let $e = \psi^{-1}(1,0)$. Then $e$ is a non-trivial idempotent ($e^2 = e$, $e \neq 0,1$).

iii) $\Rightarrow$ i): If $e \in A$ is an idempotent with $e \neq 0,1$, then $\operatorname{Spec}(A) = D(e) \cup D(1-e)$ is a disconnection, as $D(e) \cap D(1-e) = D(e(1-e)) = D(0) = \varnothing$ and both are non-empty (since $e$ and $1-e$ are not units).
___

