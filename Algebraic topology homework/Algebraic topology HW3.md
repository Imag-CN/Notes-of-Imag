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

>[!problem] [HAT] 1.2.10
>Consider two arcs $\alpha$ and $\beta$ embedded in $D^{2} \times I$ as shown in the picture. The loop $\gamma$ is obviously nullhomotopic in $D^{2} \times I$, but show that there is no nullhomotopy of $\gamma$ in the complement of $\alpha \cup \beta$.

**Proof:**
We observe that the space $D^2 \times I \setminus (\alpha \cup \beta)$ is homeomorphic to a cube $I^3$ minus two disjoint straight arcs — achievable by “straightening” the arcs via ambient isotopy. This space deformation retracts to a square $I \times I$ minus two points, which is homotopy equivalent to $S^1 \vee S^1$. Thus, its fundamental group is the free group on two generators:  
$$
\pi_1(X) \cong \mathbb{Z} * \mathbb{Z} = \langle a \rangle * \langle b \rangle.
$$
Under this identification, the loop $\gamma$ corresponds to the word $abab$  in $\pi_1(X)$. Since this is a nontrivial element, $\gamma$ is not nullhomotopic in the complement.

Hence, while $\gamma$ bounds a disk in $D^2 \times I$, it cannot be shrunk to a point without crossing $\alpha \cup \beta$.
___

>[!problem] [HAT] 1.2.17
>Show that $\pi_1(\mathbb{R}^2 - \mathbb{Q}^2)$ is uncountable.

**Proof:**
Let $X = \mathbb{R}^2 \setminus \mathbb{Q}^2$, fix basepoint $p_0 = (\sqrt{2}, \sqrt{2})$.

For each irrational $t$, define the loop $\gamma_t$ as the boundary of the axis-aligned square centered at $p_0$ with side length $2|t|$. Since $t$ is irrational, $\gamma_t$ contains no rational points, so $\gamma_t \subset X$.

If $t \ne s$ are irrational, the squares differ. One can show $[\gamma_t] \ne [\gamma_s]$ in $\pi_1(X)$: for example, $\gamma_t$ is not homotopic to a constant in the complement of the point $(\sqrt{2}+t, \sqrt{2}) \in X$, while $\gamma_s$ is. Hence homotopy classes are distinct.

Thus $\{\,[\gamma_t] : t \in \mathbb{R}\setminus\mathbb{Q}\,\}$ is an uncountable subset of $\pi_1(X)$.
___

>[!problem] [HAT] 1.2.21
>Show that the join $X * Y$ of two nonempty spaces $X$ and $Y$ is simply-connected if $X$ is path-connected.

**Proof:**
Let $X$ be path-connected and $Y$ nonempty. The join $X * Y$ can be viewed as the union of cones:
$$
X * Y \; \simeq \; (CX \times Y) \; \cup_{X \times Y} \; (X \times CY),
$$
where $CX$ and $CY$ are cones over $X$ and $Y$. Both $CX \times Y$ and $X \times CY$ are contractible (since each contains a cone factor), and their intersection is $X \times Y$.

Take a basepoint in $X \times Y \subset X * Y$. Apply the Van Kampen theorem. Because $X$ is path-connected, $X \times Y$ is path-connected. The two pieces $CX \times Y$ and $X \times CY$ are simply-connected (they are contractible), and their intersection $X \times Y$ is path-connected.

Thus $\pi_1(X * Y)$ is the amalgamated product of two trivial groups over $\pi_1(X \times Y)$, which is trivial. Hence $X * Y$ is simply-connected.

