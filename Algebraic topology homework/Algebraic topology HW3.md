___

>[!problem]

Let $f \in \Omega(x, x_0)$. Then there exists $0 = t_0 < t_1 < \dots < t_n = 1$ such that for each $\lambda \in \{0, \dots, n-1\}$, $f([t_{\lambda}, t_{\lambda+1}]) \subseteq A_{\lambda}$.

For $0 < i < n$, choose a path $\gamma_i$ in $A_{i-1} \cap A_i$ from $x_0$ to $f(t_i)$ and put $\gamma_0 = \gamma_n = C_{x_0}$ (constant path).

Then define $f_i := \gamma_{i-1} \cdot f|_{[t_{i-1}, t_i]} \cdot \overline{\gamma_i}$. Then $[f] = [f_1] \cdot [f_2] \cdots [f_n]$ in $\pi_1(X, x_0)$, and $f_i$ is a loop in $A_i$ based at $x_0$.

Thus, the homomorphism $*_{\lambda} \pi_1(A_{\lambda}, x_0) \to \pi_1(X, x_0)$ is surjective.
___

