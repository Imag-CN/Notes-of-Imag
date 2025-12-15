___

>[!problem] Problem 1
>Let $X$ be a topological space. We define a relation $\sim$ on $X$, by setting $x\sim y$ if there exists a connected subset $A\subset X$ containing both $x$ and $y$. Prove that it is an equivalence relation.

**Proof**:
- **Reflexive:** For any $x \in X$, $\{x\}$ is connected and contains $x$, so $x \sim x$.
- **Symmetric:** If $x \sim y$, then $\exists$ connected $A$ with $x, y \in A$, so $y \sim x$.
- **Transitive:** If $x \sim y$ and $y \sim z$, then $\exists$ connected sets $A,B$ with $x,y \in A$ and $y,z \in B$. Since $y \in A \cap B$, $A \cup B$ is connected and contains $x,z$, so $x \sim z$.
___

>[!problem] Problem 2
>Let $X$ be a topological space. Show that every connected component of $X$ is closed in $X$. Give an example of $X$ so that a connected component is not open.

**Proof**: Let $C$ be a connected component. Then $\overline{C}$ is connected and contains $C$, so by maximality $\overline{C} = C$. Thus $C$ is closed.

**Example**: $\mathbb{Q}$ with subspace topology from $\mathbb{R}$. Each component is a singleton $\{q\}$, which is closed but not open.
___

>[!problem] Problem 3
>Let $\mathcal{T}_{1},\mathcal{T}_{2}$ be two topologies on $X$. If $\mathcal{T}_{1}\subset\mathcal{T}_{2}$, what does connectedness of $X$ in one topology imply about connectedness in the other?

**Answer**: If $(X, \mathcal{T}_2)$ is connected, then $(X, \mathcal{T}_1)$ is connected. This is because every open set in $\mathcal{T}_{1}$ is open set in $\mathcal{T}_{2}$. If $X$ is the disjoint union of two open sets in $\mathcal{T}_{1}$, it is the disjoint union of two open sets in $\mathcal{T}_{2}$.

The converse is false. Counterexample: $\mathbb{R}$ with usual topology ($\mathcal{T}_1$, connected) vs discrete topology ($\mathcal{T}_2$, disconnected).
___

>[!problem] Problem 4
>Let $\{A_{n}\}$ be a sequence of connected subspaces of $X$, such that $A_{n}\cap A_{n+1}\neq\varnothing$ for all $n$. Show that $\bigcup A_{n}$ is connected.

**Proof**: Suppose $\bigcup A_n = U \cup V$ where $U,V$ are disjoint open sets in subspace topology. Each $A_n$ is connected, so each $A_n \subset U$ or $A_n \subset V$. Since $A_n \cap A_{n+1} \neq \varnothing$, all $A_n$ lie in the same set, contradicting that both $U$ and $V$ are nonempty.
___

>[!problem] Problem 5
>A space is totally disconnected if its only connected subspaces are one-point sets. Show that if $X$ has the discrete topology, then $X$ is totally disconnected. Does the converse hold?

**Proof**: In discrete topology, any subset with more than one point can be separated by its points, so only singletons are connected.

**Converse:** Doesn't hold. $\mathbb{Q}$ is totally disconnected but not discrete (singletons are not open).
___

>[!problem] Problem 6
>Recall $\mathbb{R}_{\ell}$ denotes the space $\mathbb{R}$ with the lower limit topology. Is the space $\mathbb{R}_{\ell}$ connected? Justify your answer.

**Answer**: $\mathbb{R}_{\ell}$ is not connected. This is because $(-\infty, 0) = \bigcup_{x<0}[x,0)$ is open, and $[0,\infty)$ is open. They are disjoint and cover $\mathbb{R}_{\ell}$.
___

>[!problem] Problem 7
>Let $A$ be a proper subset of $X$, and let $B$ be a proper subset of $Y$. If $X$ and $Y$ are connected, show that
>$$(X\times Y)-(A\times B)$$
>is connected.

**Proof**: Since $A \subsetneq X$ and $B \subsetneq Y$, pick $x_0 \in X \setminus A$ and $y_0 \in Y \setminus B$. Define:
- $C_x = \{x\} \times Y$ for $x \in X \setminus A$ (connected, since it is homeomorphic to $Y$)
- $C_y = X \times \{y\}$ for $y \in Y \setminus B$ (connected, since it is homeomorphic to $X$)

All $C_x$ and $C_y$ intersect the connected set $C_{x_0} \cup C_{y_0}$ at $(x_0,y_0)$, thus their union is connected.

Their union equals $(X \times Y) - (A \times B)$ because:
- If $(x,y) \notin A \times B$, then $x \notin A$ (so $(x,y) \in C_x$) or $y \notin B$ (so $(x,y) \in C_y$)
- Conversely, any point in the union satisfies $x \notin A$ or $y \notin B$

Since the union is connected, $(X\times Y)-(A\times B)$ is connected.
___

>[!problem] Problem 8
>Show that if $X$ is an infinite set, it is connected in the finite complement topology.

**Proof**：Assume for contradiction that $X$ is disconnected in the finite complement topology. Then $X$ is a disjoint union of two non-empty proper closed sets. But non-empty proper closed sets are finite sets in complement topology, and the union of two finite sets is finite, thus contradiction.
___

>[!problem] Problem 9
>(a) Is a product of path-connected spaces necessarily path connected?
>
>(b) If $A\subset X$ and $A$ is path connected, is $\overline{A}$ necessarily path connected?

**Answer**:
(a) Yes. The product of path-connected spaces is path connected. This is because if $f_{1}:[0,1]\to X, f_{2}:[0,1]\to Y$ is continuous, then $f:[0,1]\to X\times Y$ given by $f(a)=(f_{1}(a),f_{2}(a))$ is continuous. This is a result from the last homework, Problem 10.

(b) No. Counterexample: The topologist's sine curve $S = \{(x, \sin(1/x)) : 0 < x \leq 1\}$ is path connected, but its closure $\overline{S}$ is not path connected.
___

>[!problem] Problem 10
>Let $\mathcal{T}_{1},\mathcal{T}_{2}$ be two topologies on $X$. If $\mathcal{T}_{1}\subset\mathcal{T}_{2}$, what does compactness of $X$ in one topology imply about compactness in the other?

**Answer**:
- If $(X, \mathcal{T}_1)$ is compact, then $(X, \mathcal{T}_2)$ is compact. (Every open cover in $\mathcal{T}_2$ is also an open cover in $\mathcal{T}_1$, hence has a finite subcover).
- The converse is false. A space can be compact in the finer topology but not in the coarser topology.

___

>[!problem] Problem 11
>If $\mathbb{R}$ has the countably complement topology, is $[0,1]$ compact?

No.
**Proof**: Consider the open cover
$$
\bigcup_{n\in \mathbb{Z}^+}\mathbb{R}\setminus \{ \dfrac{1}{k}: k\in \mathbb{N},k\geq n \}
$$
If it has a finite subcover
$$
\bigcup_{n\in F}\mathbb{R}\setminus \{ \dfrac{1}{k}: k\in \mathbb{N},k\geq n \}
$$
where $F$ is a finite positive integer set, then $\dfrac{1}{\max{F}}$ is not in the subcover.
Therefore, $[0,1]$ is not compact in countably complement topology.
___

>[!problem] Problem 12
>Show that a finite union of compact subspaces of $X$ is compact.

**Proof**: Let $K_1, \dots, K_n$ be compact subspaces. Let $\{U_\alpha\}$ be an open cover of $\bigcup_{i=1}^n K_i$. For each $K_i$, there exists a finite subcover $\{U_{\alpha_{i1}}, \dots, U_{\alpha_{ik_i}}\}$ covering $K_i$. The union of these finite subcovers over all i is a finite subcover of $\bigcup K_i$.
___

>[!problem] Problem 13
>Show that if $Y$ is compact, then the projection $\pi_{1}:X\times Y\to X$ is a closed map.

**Proof**: Let $C \subset X \times Y$ be closed. To show $\pi_1(C)$ is closed, let $x \notin \pi_1(C)$. Then $\{x\} \times Y \subset (X \times Y) \setminus C$. Since Y is compact, by the tube lemma, there exists an open neighborhood U of x such that $U \times Y \subset (X \times Y) \setminus C$. Thus $U \cap \pi_1(C) = \varnothing$, so $\pi_1(C)$ is closed.
___

>[!problem] Problem 14
>Let $f:X\rightarrow Y$ be a map between two topological spaces, and assume $Y$ is compact Hausdorff.
>Prove that $f$ is continuous if and only if the graph of $f$,
>$$G_{f}:=\{(x,f(x))|\,x\in X\}$$
>is closed in $X \times Y$.

**Proof**:
($\Rightarrow$) If f is continuous, then the map $g: X \times Y \to Y \times Y$ defined by $g(x,y) = (f(x), y)$ is continuous. Since Y is Hausdorff, the diagonal $\Delta_Y$ is closed in $Y \times Y$. Then $G_f = g^{-1}(\Delta_Y)$ is closed.

($\Leftarrow$) Suppose $G_f$ is closed. Let $C \subset Y$ be closed. Since Y is compact, the projection $\pi_1: X \times Y \to X$ is closed. Note that $f^{-1}(C) = \pi_1(G_f \cap (X \times C))$. Since $G_f$ and $X \times C$ are closed, their intersection is closed, and its projection is closed. Thus $f^{-1}(C)$ is closed, so $f$ is continuous.
___

>[!problem] Problem 15
>Let $A,B$ be two disjoint compact subspaces of a Hausdorff space $X$. Show that there exist disjoint open sets $U$ and $V$ containing $A$ and $B$, respectively.

**Proof**: For each $a \in A$ and $b \in B$, since X is Hausdorff, there exist disjoint open sets $U_{ab}$ containing a and $V_{ab}$ containing b. For fixed a, $\{V_{ab}\}_{b \in B}$ covers B. By compactness, there is a finite subcover $\{V_{ab_1}, \dots, V_{ab_n}\}$. Let $U_a = \bigcap_{i=1}^n U_{ab_i}$ and $V_a = \bigcup_{i=1}^n V_{ab_i}$. Then $U_a$ and $V_a$ are disjoint open sets with $a \in U_a$ and $B \subset V_a$. Now $\{U_a\}_{a \in A}$ covers A. By compactness, there is a finite subcover $\{U_{a_1}, \dots, U_{a_m}\}$. Let $U = \bigcup_{j=1}^m U_{a_j}$ and $V = \bigcap_{j=1}^m V_{a_j}$. Then $U$ and $V$ are disjoint open sets containing $A$ and $B$ respectively.
___

>[!problem] Problem 16
>Let $p:X\rightarrow Y$ be a closed continuous surjective map such that $p^{-1}(\{y\})$ is compact, for each $y\in Y$. Show that if $Y$ is compact, then $X$ is compact.

**Proof**: Let $\{U_\alpha\}_{\alpha \in J}$ be an open cover of $X$. For each $y \in Y$, the fiber $p^{-1}(\{y\})$ is compact, so there exists a finite subset $J_y \subset J$ such that $p^{-1}(\{y\}) \subset \bigcup_{\alpha \in J_y} U_\alpha$. Let $W_y = \bigcup_{\alpha \in J_y} U_\alpha$. Since $p$ is closed and $X \setminus W_y$ is closed, $p(X \setminus W_y)$ is closed in $Y$. Note that $y \notin p(X \setminus W_y)$ because $p^{-1}(\{y\}) \subset W_y$. Thus, $V_y = Y \setminus p(X \setminus W_y)$ is an open neighborhood of $y$ in $Y$.

Now, $\{V_y\}_{y \in Y}$ is an open cover of the compact space $Y$, so there exists a finite set $\{y_1, \dots, y_n\}$ such that $Y = \bigcup_{i=1}^n V_{y_i}$. Then, $X = p^{-1}(Y) = \bigcup_{i=1}^n p^{-1}(V_{y_i})$. For each $i$, we have $p^{-1}(V_{y_i}) \subset W_{y_i} = \bigcup_{\alpha \in J_{y_i}} U_\alpha$ (since if $x \in p^{-1}(V_{y_i})$, then $p(x) \in V_{y_i}$, so $p(x) \notin p(X \setminus W_{y_i})$, implying $x \notin X \setminus W_{y_i}$, i.e., $x \in W_{y_i}$). Therefore, $X \subset \bigcup_{i=1}^n \bigcup_{\alpha \in J_{y_i}} U_\alpha$, which is a finite union of the $U_\alpha$'s. 

Hence, $X$ is compact.
___
