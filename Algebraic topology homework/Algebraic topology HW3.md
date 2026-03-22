___

>[!problem]
>Let $X = \bigcup_{\lambda \in \Lambda} A_{\lambda}$, and let each $A_{\lambda}$ be path-connected.
>
>Suppose that for every $x \in A_{\lambda}$, there is a neighbourhood $V_x$ such that for each $\lambda$, $V_x \cap A_{\lambda}$ is path-connected and the map $\pi_1(V_x, x_0) \to \pi_1(A_{\lambda}, x_0)$ is surjective.
>
>Then the map
>$$*_{\lambda} \pi_1(A_{\lambda}, x_0) \longrightarrow \pi_1(X, x_0)$$
>is surjective.

**Proof:**
Let $f \in \Omega(x, x_0)$. Then there exists $0 = t_0 < t_1 < \dots < t_n = 1$ such that for each $\lambda \in \{0, \dots, n-1\}$, $f([t_{\lambda}, t_{\lambda+1}]) \subseteq A_{\lambda}$.

For $0 < i < n$, choose a path $\gamma_i$ in $A_{i-1} \cap A_i$ from $x_0$ to $f(t_i)$ and put $\gamma_0 = \gamma_n = C_{x_0}$ (constant path).

Then define $f_i := \gamma_{i-1} \cdot f|_{[t_{i-1}, t_i]} \cdot \overline{\gamma_i}$. Then $[f] = [f_1] \cdot [f_2] \cdots [f_n]$ in $\pi_1(X, x_0)$, and $f_i$ is a loop in $A_i$ based at $x_0$.

Thus, the homomorphism $*_{\lambda} \pi_1(A_{\lambda}, x_0) \to \pi_1(X, x_0)$ is surjective.
___

>[!problem] [HAT] 1.2.8
>Compute the fundamental group of the space obtained from two tori $S^{1} \times S^{1}$ by identifying a circle $S^{1} \times \{x_0\}$ in one torus with the corresponding circle $S^{1} \times \{x_0\}$ in the other torus.

**Solution:**
Let $X = T_1 \cup_{S^1} T_2$, where $T_i = S^1 \times S^1$. Applying Van Kampen gives:
$$
\pi_1(T_1) = \langle a, b \mid [a,b]=1 \rangle, \pi_1(T_2) = \langle c, d \mid [c,d]=1 \rangle, \pi_1(S^1) = \langle t \rangle.
$$
The glued circle in $T_1$ corresponds to $a$, in $T_2$ to $c$. Thus, the induced maps are $i_{1*}(t)=a$, $i_{2*}(t)=c$.

Applying Van Kampen gives:
$$
\pi_1(X) \cong \langle a, b, c, d \mid [a,b]=1,\ [c,d]=1,\ a=c \rangle.
$$
Set $g = a = c$. Then $[g, b]=1$, $[g, d]=1$, and $b$, $d$ are free.

Therefore, $\pi_1(X) \cong \langle g, b, d \mid [g,b]=1,\ [g,d]=1 \rangle \cong \mathbb{Z} \times F_2$.
___

