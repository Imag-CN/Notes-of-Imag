___

>[!problem] Problem 1
>Let $X$ be a first countable topological space, $x\in X$ be any point, and $f:X\to Y$ be any map. Show that $f$ is continuous at $x$ if and only if $f$ preserves any convergent sequences at $x$.

**Proof:**
($\Rightarrow$) Suppose $f$ is continuous at $x$. Let $\{x_n\}$ be a sequence converging to $x$. For any neighborhood $V$ of $f(x)$, $f^{-1}(V)$ is a neighborhood of $x$. Thus there exists $N$ such that for all $n>N$, $x_n\in f^{-1}(V)$, so $f(x_n)\in V$. Hence $f(x_n)\to f(x)$.

($\Leftarrow$) Suppose $f$ preserves convergent sequences at $x$ but $f$ is not continuous at $x$. Then there exists a neighborhood $V$ of $f(x)$ such that for any neighborhood $U$ of $x$, $f(U)\not\subset V$. Since $X$ is first countable, let $\{U_n\}$ be a countable local basis at $x$ with $U_{n+1}\subset U_n$. For each $n$, pick $x_n\in U_n$ with $f(x_n)\notin V$. Then $x_n\to x$ but $f(x_n)\not\to f(x)$, contradiction.
___

>[!problem] Problem 2
>Prove that: Any subspace of a second countable space is second countable. Any Cartesian product of two second-countable spaces is second-countable.

**Proof:**
**Subspace case:**
Let $X$ be a second countable space with countable basis $\mathcal{B}$. Let $A$ be any subspace of $X$. Consider the collection:
$$\mathcal{B}_A = \{B \cap A : B \in \mathcal{B}\}$$
This collection is countable since $\mathcal{B}$ is countable.

We show $\mathcal{B}_A$ is a basis for the subspace topology on $A$:
For any open set $U$ in $A$ and any $x \in U$, there exists an open set $V$ in $X$ such that $U = V \cap A$. Since $\mathcal{B}$ is a basis for $X$, there exists $B \in \mathcal{B}$ such that $x \in B \subset V$. Then $x \in B \cap A \subset V \cap A = U$, and $B \cap A \in \mathcal{B}_A$.

Thus $A$ is second countable.

**Product case:**
Let $X$ and $Y$ be second countable spaces with countable bases $\mathcal{B}_X$ and $\mathcal{B}_Y$ respectively. Consider the collection:
$$\mathcal{B}_{X\times Y} = \{U \times V : U \in \mathcal{B}_X, V \in \mathcal{B}_Y\}$$
This collection is countable since it's the Cartesian product of two countable sets.

We show $\mathcal{B}_{X\times Y}$ is a basis for the product topology on $X \times Y$:
For any open set $W$ in $X\times Y$ and any $(x,y) \in W$, there exist open sets $U \subset X$ and $V \subset Y$ such that $(x,y) \in U\times V \subset W$. Since $\mathcal{B}_X$ and $\mathcal{B}_Y$ are bases, there exist $B_X \in \mathcal{B}_X$ and $B_Y \in \mathcal{B}_Y$ such that $x \in B_X \subset U$ and $y \in B_Y \subset V$. Then $(x,y) \in B_X \times B_Y \subset U\times V \subset W$, and $B_X \times B_Y \in \mathcal{B}_{X\times Y}$.

Thus $X\times Y$ is second countable.
___

>[!problem] Problem 3
>Let $X$ have a countable basis, and let $A$ be an uncountable subset of $X$. Show that uncountably many points of $A$ are limit points of $A$.

**Proof:**
Suppose only countably many points of $A$ are limit points. Let $A_0$ be the set of isolated points of $A$, then $A_0$ is uncountable. For each $a\in A_0$, $\{ a \}$ is an open set, thus $\{ a \}$ must be a basis element (since it is a singleton). However, $X$ has a countable basis, thus contradiction.
___

>[!problem] Problem 4
>Show that every compact metrizable space $X$ has a countable basis.

**Proof:**
Suppose $d$ is a metric on $X$ which generates the topology. By compactness, for any $n\in \mathbb{Z}^+$, the open cover $\bigcup_{x \in X}B(x, 1/n)$ has a finite subcover $\bigcup_{x \in F_{n}}B(x, 1/n)$ where $F_{n}$ is a finite subset of $X$. Then $\mathcal{B}=\{B(x,1 /n):n \in \mathbb{Z}^+,x \in F_{n}\}$ is a countable collection of open sets in $X$.

Next we shall show $\mathcal{B}$ is a basis. Since all the open balls form a basis, it is sufficient to show for any open ball $B_{0}=B(a,r)$ and any $x_{0}\in B_{0}$, there exists a $B_{1} \in \mathcal{B}$ such that $x_{0}\in B_{1} \subseteq B_{0}$. Let $n_{1}$ be a sufficiently large positive integer such that $2 /n_{1}<r-d(a,x_{0})$. Since $\bigcup_{x \in F_{n_{1}}}B(x, 1/n_{1})$ covers $X$, there exists a $B_{1}=B(a_{1},1/n_{1}) \in \mathcal{B}$ such that $x_{0}\in B_{1}$. For any $x_{1} \in B_{1}$, by triangle inequality we have $d(a,x_{1})\leq d(a,x_{0})+d(x_{0},a_{1})+d(a_{1},x_{1})<d(a,x_{0})+2 /n_{1}<r$, thus $B_{1}\subseteq B_{0}$. 

Therefore we have done the proof.
___

>[!problem] Problem 5
>Show that every metrizable space with a countable dense subset has a countable basis.

**Proof:**
Let $B$ be a countable dense subset of space $X$. Let $\mathcal{B}=\{ B(b,1/n):b \in B,n\in \mathbb{Z}^+ \}$. Then $\mathcal{B}$ is countable since it is a countable union of countable sets. 

Next we shall show $\mathcal{B}$ is a basis. Since all the open balls form a basis, it is sufficient to show for any open ball $B_{0}=B(a,r)$ and any $x_{0}\in B_{0}$, there exists a $B_{1} \in \mathcal{B}$ such that $x_{0}\in B_{1} \subseteq B_{0}$. Let $n_{1}$ be a sufficiently large positive integer such that $2 /n_{1}<r-d(a,x_{0})$. Since $B$ is dense in $X$, there exists a $b_{1}\in B$ such that $x_{0}\in B_{1}=B(b_{1},1/n_{1}) \in \mathcal{B}$. For any $x_{1} \in B_{1}$, by triangle inequality we have $d(a,x_{1})\leq d(a,x_{0})+d(x_{0},b_{1})+d(b_{1},x_{1})<d(a,x_{0})+2 /n_{1}<r$, thus $B_{1}\subseteq B_{0}$. 

Therefore we have done the proof.
___

>[!problem] Problem 6
>Let $f: X \rightarrow Y$ be a continuous open map. Show that if $X$ is first countable or second countable, then $f(X)$ is also first countable or second countable, respectively.

**Proof:**
**First countability case:**
Let $X$ be first countable. For any $y \in f(X)$, pick $x \in X$ with $f(x) = y$. Let $\{U_n\}_{n\in\mathbb{N}}$ be a countable neighborhood basis at $x$ in $X$. Since $f$ is continuous and open, $\{f(U_n)\}_{n\in\mathbb{N}}$ is a countable collection of open neighborhoods of $y$ in $f(X)$.

We show this is a neighborhood basis: For any open $V \subset f(X)$ with $y \in V$, $f^{-1}(V)$ is open in $X$ (by continuity) and contains $x$. So there exists $n$ with $U_n \subset f^{-1}(V)$, hence $f(U_n) \subset V$.
**Second countability case:**
Let $X$ be second countable with countable basis $\mathcal{B}$. Since $f$ is continuous and open, $\{f(B) : B \in \mathcal{B}\}$ is a countable collection of open sets in $f(X)$.

We show this is a basis: For any open $V \subset f(X)$ and $y \in V$, pick $x \in f^{-1}(y)$. Then $f^{-1}(V)$ is open in $X$ and contains $x$, so there exists $B \in \mathcal{B}$ with $x \in B \subset f^{-1}(V)$, hence $y \in f(B) \subset V$.
___

>[!problem] Problem 7
>Show that if $X$ has a countable dense subset, every collection of disjoint open sets in $X$ is countable.

**Proof:**
Let $D$ be a countable dense subset of $X$, and let $\mathcal{U}$ be a collection of disjoint nonempty open sets in $X$. For each $U\in\mathcal{U}$, since $D$ is dense, $U\cap D\neq\varnothing$. Pick $x_U\in U\cap D$. The mapping $U\mapsto x_U$ is injective because the sets in $\mathcal{U}$ are disjoint. Thus $\#\mathcal{U}\leq\# D$, so $\mathcal{U}$ is countable.
___

>[!problem] Problem 8
>Show that if $X$ is regular, every pair of points of $X$ have neighborhoods whose closures are disjoint.

**Proof:**
Let $x,y\in X$ with $x\neq y$. Since $X$ is regular (and in particular Hausdorff), there exist disjoint open sets $U,V$ such that $x\in U$ and $y\in V$. By regularity, there exist open sets $U_1,V_1$ such that $x\in U_1\subset\overline{U_1}\subset U$ and $y\in V_1\subset\overline{V_1}\subset V$. Then $\overline{U_1}\cap\overline{V_1}=\varnothing$ since $U\cap V=\varnothing$.
___

>[!problem] Problem 9
>Show that if $X$ is normal, every pair of disjoint closed sets have neighborhoods whose closures are disjoint.

**Proof:**
Let $A,B$ be disjoint closed sets in $X$. By normality, there exist disjoint open sets $U,V$ such that $A\subset U$ and $B\subset V$.

Since $U^c$ is closed, by normality there exists disjoint open sets $U_{1},U_{2}$ such that $A\subset U_{1}$ and $U^c \subset U_{2}$. Then $U_{2}^c$ is a closed set containing $U_{1}$, thus contains $\overline{ U_{1} }$. $U^c \subset U_{2}$ implies $U\supset U_{2}^c$, thus $U$ contains $\overline{ U_{1} }$. Therefore we have $A\subset U_1\subset\overline{U_1}\subset U$. Similarly we can find open set $V_{1}$ such that $B\subset V_1\subset\overline{V_1}\subset V$. $U$ and $V$ are disjoint implies $\overline{ U_{1} }$ and $\overline{ V_{1} }$ are disjoint. Therefore $U_{1}$ and $V_{1}$ are neighborhoods of $A$ and $B$ whose closures are disjoint.
___

>[!problem] Problem 10
>Show that a closed subspace of a normal space is normal.

**Proof:**
Let $X$ be normal and $A\subset X$ be closed. Let $E,F$ be disjoint closed sets in $A$. Since $A$ is closed, $E,F$ are closed in $X$. By normality of $X$, there exist disjoint open sets $U,V$ in $X$ such that $E\subset U$ and $F\subset V$. Then $U\cap A$ and $V\cap A$ are disjoint open sets in $A$ separating $E$ and $F$.
___

>[!problem] Problem 11
>Let $f, g: X → Y$ be continuous. Assume $Y$ is Hausdorff. Show that $\{x\mid f(x)=g(x)\}$ is closed in $X$.

**Proof:**
Let $A=\{x\in X\mid f(x)=g(x)\}$. Consider the map $h:X\to Y\times Y$ defined by $h(x)=(f(x),g(x))$, which is continuous. The set $\Delta=\{(y,y)\mid y\in Y\}$ is closed in $Y\times Y$ since $Y$ is Hausdorff. Then $A=h^{-1}(\Delta)$ is closed in $X$.
___

>[!problem] Problem 12
>Let $p: X → Y$ be a closed continuous surjective map. Show that if $X$ is normal, then so is $Y$.

**Proof:**
Let $A,B$ be disjoint closed sets in $Y$. Then $p^{-1}(A)$ and $p^{-1}(B)$ are disjoint closed sets in $X$. By normality, there exist disjoint open sets $U,V$ in $X$ such that $p^{-1}(A)\subset U$ and $p^{-1}(B)\subset V$. Let $U_1=Y\setminus p(X\setminus U)$ and $V_1=Y\setminus p(X\setminus V)$. Since $p$ is closed, $U_1,V_1$ are open in $Y$. We have $A\subset U_1$, $B\subset V_1$, and $U_1\cap V_1=\varnothing$.