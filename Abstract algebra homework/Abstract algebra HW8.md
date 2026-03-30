___

> [!problem] Problem 1
> Let $G$ be the group of rigid motions of $\mathbb{R}^3$. A map $f : \mathbb{R}^3 \to \mathbb{R}^3$ is called a rigid motion if $f$ satisfies $|f(x) - f(y)| = |x - y|$ for all $x, y \in \mathbb{R}^3$, where $|\cdot|$ is the standard Euclidean metric on $\mathbb{R}^3$. Write $G$ as a subgroup of $GL(4)$ and find a nontrivial normal subgroup of it.

**Proof:**
Write $G$:
$$
G=\{ \begin{pmatrix}
A&u \\
O&1
\end{pmatrix}:A\in SO_{3}(\mathbb{R}),u\in \mathbb{R}^{3}, O=(0,0,0)\},
$$
Normal subgroup $H$:
$$
H=\{ \begin{pmatrix}
A&O' \\
O&1
\end{pmatrix}:A\in SO_{3}(\mathbb{R}),O'=\begin{pmatrix}
0 \\
0 \\
0
\end{pmatrix}, O=(0,0,0)\},
$$
___

> [!problem] Problem 2
>Let $G$ be the group of rigid motions of $\mathbb{R}^2$. Prove that the map
>$$
>G\to O(2)
>$$
>$$
>T \mapsto (x \mapsto T(x) - T(0))
>$$
>is a group homomorphism.

**Proof:**
Let $G$ be the group of rigid motions of $\mathbb{R}^2$. Write any $T \in G$ as $T(x) = A x + b$ with $A \in O(2)$ and $b \in \mathbb{R}^2$.

Define $\varphi: G \to O(2)$ by $\varphi(T)(x) = T(x) - T(0)$. Then
$$
\varphi(T)(x) = (A x + b) - b = A x.
$$

For $T_1(x) = A_1 x + b_1$ and $T_2(x) = A_2 x + b_2$ in $G$, we have
$$
(T_1 \circ T_2)(x) = A_1 A_2 x + (A_1 b_2 + b_1).
$$

Therefore,
$$
\varphi(T_1 \circ T_2)(x) = (T_1 \circ T_2)(x) - (T_1 \circ T_2)(0) = A_1 A_2 x.
$$

On the other hand,
$$
\varphi(T_1)(x) = A_1 x, \quad \varphi(T_2)(x) = A_2 x
$$
so
$$
(\varphi(T_1) \circ \varphi(T_2))(x) = A_1 (A_2 x) = A_1 A_2 x.
$$

Thus $\varphi(T_1 \circ T_2)(x) = (\varphi(T_1) \circ \varphi(T_2))(x)$ for all $x$, hence $\varphi(T_1 \circ T_2) = \varphi(T_1) \circ \varphi(T_2)$, and $\varphi$ is a group homomorphism. 
___

> [!problem] Problem 3
>Let $\Omega$ be an open subset of $\mathbb{C}$. Denote
>$$
>\mathbb{D} = \{ z \in \mathbb{C} \mid |z| < 1 \}
>$$
>$$
>\mathbb{H} = \{ z \in \mathbb{C} \mid \operatorname{Im}(z) > 0 \}
>$$
> 
> (i) Show that if $f: \Omega \to \Omega$ is holomorphic and bijective, then it is biholomorphic, i.e., there exists a holomorphic function $g: \Omega \to \Omega$ such that $f \circ g = g \circ f = \operatorname{Id}$. This shows that holomorphic bijective maps $\Omega \to \Omega$ form a group, denoted by $\operatorname{Aut}(\Omega)$.
> 
> (ii) Compute $\operatorname{Aut}(\mathbb{C})$, $\operatorname{Aut}(\mathbb{D})$ and $\operatorname{Aut}(\mathbb{H})$ and relate them with matrix groups.

