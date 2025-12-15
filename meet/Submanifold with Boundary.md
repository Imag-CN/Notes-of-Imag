___

>[!definition] Definition (Submanifold)
>Let $M$ be an $m$-dimensional smooth manifold. A subset $N \subset M$ is called an $n$-dimensional **submanifold** of $M$ if for every point $p \in N$, there exists a coordinate chart $(U, \varphi)$ for $M$ around $p$ such that:
>$$
>\varphi(U \cap N) = \varphi(U) \cap (\mathbb{R}^n \times \{0\}^{m-n}),
>$$
>where $\mathbb{R}^n \times \{0\}^{m-n} := \{(x^1, \dots, x^n, 0, \dots, 0) \in \mathbb{R}^m\}$. In other words, locally in these coordinates, $N$ looks like a coordinate plane $\mathbb{R}^n$ in $\mathbb{R}^m$.

___

>[!note] Theorem
> Let $P$ be a submanifold of $N$, and $N$ a submanifold of $M$, then $P$ is a submanifold of $M$.

**Proof:** Let $\dim M = m$, $\dim N = n$, $\dim P = p$. Take $q \in P$.

Since $N$ is a submanifold of $M$, there exists a chart $(U_1, \varphi_1)$ of $M$ around $q$ such that
$$
\varphi_1(U_1 \cap N) = \varphi_1(U_1) \cap (\mathbb{R}^n \times \{0\}^{m-n}).
$$
Let $\tilde\varphi_1 = (\varphi_1^1, \dots, \varphi_1^n)$ on $\tilde U_1 = U_1 \cap N$. Then $(\tilde U_1, \tilde\varphi_1)$ is a chart for $N$.

Since $P$ is a submanifold of $N$, there exists a chart $(\tilde U_2, \tilde\varphi_2)$ of $N$ around $q$ with
$$
\tilde\varphi_2(\tilde U_2 \cap P) = \tilde\varphi_2(\tilde U_2) \cap (\mathbb{R}^p \times \{0\}^{n-p}).
$$
Let $U = U_1 \cap \tilde U_2$ (shrinking if necessary). Define $F: \varphi_1(U) \to \mathbb{R}^m$ by
$$
F(y) = \bigl( \tilde\varphi_2(\varphi_1^{-1}(y)),\, y^{n+1},\, \dots,\, y^m \bigr), \quad y = (y^1, \dots, y^m).
$$
Write $G(y) = \tilde\varphi_2(\varphi_1^{-1}(y))$, which depends only on $(y^1, \dots, y^n)$ because on $U$, $y^{n+1} = \dots = y^m = 0$. The Jacobian of $F$ at $\varphi_1(q)$ is
$$
dF =
\begin{pmatrix}
\frac{\partial G}{\partial y^1, \dots, y^n} & 0 \\
0 & I_{m-n}
\end{pmatrix},
$$
which is invertible since $\tilde\varphi_2 \circ \tilde\varphi_1^{-1}$ is a diffeomorphism.

By the Inverse Function Theorem, $F$ is a diffeomorphism on some neighborhood $W'$ of $\varphi_1(q)$. Set $W = \varphi_1^{-1}(W')$ and $\psi = F \circ \varphi_1|_W$. Then $(W, \psi)$ is a chart of $M$ around $q$.

For $x \in W$,
* If $x \in P$, then $\tilde\varphi_2(x) \in \mathbb{R}^p \times \{0\}^{n-p}$ and $x \in N$ gives $\varphi_1^{n+1}(x) = \dots = \varphi_1^m(x) = 0$. Thus $\psi(x) \in \mathbb{R}^p \times \{0\}^{m-p}$.
* If $\psi(x) \in \mathbb{R}^p \times \{0\}^{m-p}$, then its last $m-n$ components are zero, so $x \in N$. The first $n$ components are $\tilde\varphi_2(x)$, whose last $n-p$ components are zero, so $x \in P$.

Hence $\psi(W \cap P) = \psi(W) \cap (\mathbb{R}^p \times \{0\}^{m-p})$, so $P$ is a $p$-dimensional submanifold of $M$.
___

>[!notes] Definition (Manifold with Boundary).
>Let $M$ be a topological space. We say that $M$ is an **$n$-dimensional topological manifold with boundary** if it is Hausdorff, second-countable, and every point $p \in M$ has a neighborhood homeomorphic to either an open subset of $\mathbb{R}^n$ or an open subset of the closed upper half-space
>$$
>\mathbb{H}^n := \{(x^1, \dots, x^n) \in \mathbb{R}^n \mid x^n \ge 0\}.
>$$

A point $p$ is called a **boundary point** if there exists a chart $(U, \varphi)$ with $p \in U$ such that $\varphi(p) \in \partial \mathbb{H}^n := \{(x^1, \dots, x^n) \in \mathbb{R}^n \mid x^n = 0\}$. Otherwise, it is called an **interior point**. The set of all boundary points is denoted $\partial M$, and the set of interior points is denoted $\operatorname{Int} M$.

An $n$-dimensional **smooth** manifold with boundary is a topological manifold with boundary equipped with a **smooth structure**, i.e., an atlas of charts $(U_\alpha, \varphi_\alpha)$ mapping $U_\alpha$ to open subsets of $\mathbb{H}^n$, such that all transition maps $\varphi_\beta \circ \varphi_\alpha^{-1}$ are smooth.
___

>[!notes] Definition (Submanifold with Boundary).
>Let $M$ be an $m$-dimensional smooth manifold with boundary. A subset $N \subset M$ is called an $n$-dimensional **submanifold with boundary** of $M$ if for every point $p \in N$, there exists a coordinate chart $(U, \varphi)$ of $M$ around $p$ such that one of the following holds:
>
>1.  $\varphi(p) \in \operatorname{Int}(\mathbb{H}^m)$ and
>    $$
>   \varphi(U \cap N) = \varphi(U) \cap (\mathbb{R}^n \times \{0\}^{m-n}),
>   $$
>   where $\mathbb{R}^n$ is identified with $\operatorname{Int}(\mathbb{H}^n) \times \{0\}^{m-n} \subset \mathbb{H}^m$.
>
>2.  $\varphi(p) \in \partial \mathbb{H}^m$ and
>$$
>    \varphi(U \cap N) = \varphi(U) \cap (\mathbb{H}^n \times \{0\}^{m-n}),
>   $$
>    where $\mathbb{H}^n$ is embedded as the first $n$ coordinates of$\mathbb{H}^m$, i.e.,
>$$
>    \mathbb{H}^n \times \{0\}^{m-n} = \{(x^1, \dots, x^n, 0, \dots, 0) \in \mathbb{H}^m \mid x^n \ge 0\}.
>   $$

In case (2), the point $p$ is a **boundary point** of $N$. The boundary $\partial N$ consists of all such points. The submanifold with boundary $N$ inherits the structure of an $n$-dimensional smooth manifold with boundary from $M$.