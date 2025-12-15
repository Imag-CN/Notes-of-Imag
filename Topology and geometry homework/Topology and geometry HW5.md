___

>[!problem] Problem 1
>Show that if $A$ is closed in $X$ and $B$ is closed in $Y$, then $A\times B$ is closed in $X\times Y$.

**Proof**: Let $U = X \setminus A$ and $V = Y \setminus B$. Since $A$ and $B$ are closed, $U$ and $V$ are open. Then $(X \times Y) \setminus (A \times B) = (U \times Y) \cup (X \times V)$. Since $U \times Y$ and $X \times V$ are open, their union is open. Therefore, $A \times B$ is closed.
___

>[!problem] Problem 2
>Let $A, B$ and $A_{\alpha}$ denote subsets of a space $X$. Prove
>
>(a) If $A\subset B$, then $\overline{A}\subset\overline{B}$.
>
>(b) $\overline{A\cup B}=\overline{A}\cup\overline{B}$.
>
>(c) $\overline{\bigcup_{\alpha}A_{\alpha}}\supset\bigcup_{\alpha}\overline{A_{\alpha}}$. Give an example where equality fails.

**Proof**:
**(a)**
$\overline{B}$ is a closed set containing $B$, hence containing $A$.
Since $\overline{A}$ is the smallest closed set containing $A$, $\overline{A} \subset \overline{B}$.

**(b)**
Since $A \subset A \cup B$, $\overline{A} \subset \overline{A \cup B}$. Similarly, $\overline{B} \subset \overline{A \cup B}$. Thus $\overline{A} \cup \overline{B} \subset \overline{A \cup B}$.
$\overline{A} \cup \overline{B}$ is a closed set containing $A \cup B$. Since $\overline{A \cup B}$ is the smallest closed set containing $A \cup B$, $\overline{A \cup B} \subset \overline{A} \cup \overline{B}$.

**(c)**
 For any fixed $\alpha_0$, $A_{\alpha_0} \subset \bigcup_{\alpha} A_{\alpha}$, so $\overline{A_{\alpha_0}} \subset \overline{\bigcup_{\alpha} A_{\alpha}}$. This holds for all $\alpha$, so $\bigcup_{\alpha} \overline{A_{\alpha}} \subset \overline{\bigcup_{\alpha} A_{\alpha}}$.
 
**Counterexample of equality**: In $\mathbb{R}$ with the standard topology, let $A_n = \{\frac{1}{n}\}$ for $n \in \mathbb{Z}^+$.
- $\bigcup_{n} \overline{A_n} = \bigcup_{n} \{\frac{1}{n}\} = \{\frac{1}{n} \mid n \in \mathbb{Z}^+\}$.
- $\overline{\bigcup_{n} A_n} = \{\frac{1}{n} \mid n \in \mathbb{Z}^+\} \cup \{0\}$.
- Thus, $\overline{\bigcup_{n} A_n} \supsetneq \bigcup_{n} \overline{A_n}$.
___

>[!problem] Problem 3
>Let $A\subset X$ and $B\subset Y$. Show that in the space $X\times Y$, $\overline{A\times B}=\overline{A}\times\overline{B}$.

**Proof**:
Since $A \times B \subset \overline{A} \times \overline{B}$ and $\overline{A} \times \overline{B}$ is closed (by Problem 1), we have $\overline{A \times B} \subset \overline{A} \times \overline{B}$ (since closure of $A \times B$ is the smallest closed set containing $A \times B$).

Let $(x, y) \in \overline{A} \times \overline{B}$. There exist open sets $U \subset X$, $V \subset Y$ such that $(x, y) \in W$, where $W= U \times V$.
- Since $x \in \overline{A}$, $U \cap A \neq \varnothing$. Similarly, $V \cap B \neq \varnothing$.
- Thus, $(U \times V) \cap (A \times B) \neq \varnothing$, so $W \cap (A \times B) \neq \varnothing$.
- This shows $(x, y) \in \overline{A \times B}$.
Thus $\overline{A} \times \overline{B} \subset \overline{A \times B}$.

Therefore, $\overline{A \times B} = \overline{A} \times \overline{B}$.
___

>[!problem] Problem 4
>If $A\subset X$, we define the boundary of $A$ by
>
>$$ \operatorname{Bd}(A)=\overline{A}\cap\overline{(X-A)}. $$
>
>(a) Show that $\operatorname{Int}(A)$ and $\operatorname{Bd}(A)$ are disjoint, and $\overline{A}=\operatorname{Int}(A)\cup\operatorname{Bd}(A)$.
>
>(b) Show that $\operatorname{Bd}(A)=\varnothing$ if and only if A is both open and closed.
>
>(c) Show that $U$ is open if and only if $\operatorname{Bd}(U)=\overline{U}-U$.
>
>(d) If $U$ is open, is it true that $U=\operatorname{Int}(\overline{U})$?

**Proof**:
**(a)**
If $x \in \operatorname{Int}(A)$, there exists an open set $U$ such that $x \in U \subset A$. Then $U \cap (X \setminus A) = \varnothing$, so $x \notin \overline{X \setminus A}$, hence $x \notin \operatorname{Bd}(A)$. So $\operatorname{Int}(A) \cap \operatorname{Bd}(A) = \varnothing$.

Since $\operatorname{Int}(A) \subset A\subset \overline{A}$ and $\operatorname{Bd}(A) \subset \overline{A}$, we have $\operatorname{Int}(A) \cup \operatorname{Bd}(A) \subset \overline{A}$.
Let $x \in \overline{A}$. If $x \notin \operatorname{Int}(A)$, then every neighborhood of $x$ intersects $X \setminus A$, so $x \in \overline{X \setminus A}$. Thus $x \in \overline{A} \cap \overline{X \setminus A} = \operatorname{Bd}(A)$. So $\overline{A} \subset \operatorname{Int}(A) \cup \operatorname{Bd}(A)$. Therefore, $\overline{A}=\operatorname{Int}(A)\cup\operatorname{Bd}(A)$.

**(b)**
($\Rightarrow$): If $\operatorname{Bd}(A) = \varnothing$, then from (a), $\overline{A} = \operatorname{Int}(A)$. $\operatorname{Int}(A) \subset A \subset \overline{A} = \operatorname{Int}(A)$ implies $A = \operatorname{Int}(A)$, so $A$ is open. Since $A = \overline{A}$, $A$ is closed.
($\Leftarrow$): If $A$ is open and closed, then $\overline{A} = A$ and $X \setminus A$ is closed, so $\overline{X \setminus A} = X \setminus A$. Then $\operatorname{Bd}(A) = A \cap (X \setminus A) = \varnothing$.

**(c)**
($\Rightarrow$): If $U$ is open, then $\operatorname{Int}(U) = U$. From (a), $\overline{U} = U \cup \operatorname{Bd}(U)$ and this union is disjoint. So $\operatorname{Bd}(U) = \overline{U} \setminus U$.
($\Leftarrow$): If $\operatorname{Bd}(U) = \overline{U} \setminus U$, then from (a), $\overline{U} = \operatorname{Int}(U) \cup \operatorname{Bd}(U) = \operatorname{Int}(U) \cup (\overline{U} \setminus U)$. This implies $U \subset \operatorname{Int}(U)$ (since if $x \in U$, it cannot be in $\overline{U} \setminus U$, so it must be in $\operatorname{Int}(U)$). But $\operatorname{Int}(U) \subset U$, so $U = \operatorname{Int}(U)$, hence $U$ is open.

**(d)**
No.
Counterexample: Let $U = (0,1) \cup (1,2)$ in $\mathbb{R}$ with standard topology.
- $U$ is open.
- $\overline{U} = [0,2]$.
- $\operatorname{Int}(\overline{U}) = (0,2)$.
- But $U \neq (0,2)$.
___

>[!problem] Problem 5
>Find the boundary and the interior of each of the following subsets of $\mathbb{R}^{2}$:
>
>(a) $A=\{(x,y)\mid y=0\}$
>
>(b) $B=\{(x,y)\mid x>0\text{ and }y\neq0\}$
>
>(c) $C=A\cup B$
>
>(d) $D=\{(x,y)\mid x\text{ is rational}\}$
>
>(e) $E=\{(x,y)\mid 0<x^{2}-y^{2}\leq1\}$
>
>(f) $F=\{(x,y)\mid x\neq0\text{ and }y\leq 1/x\}$

**Proof**:
**(a)**
$Bd(A)=A,\operatorname{Int}(A)=\varnothing.$
**(b)**
$Bd(B)=\{ (0,y)\mid y\in \mathbb{R} \}\cup \{ (x,0)\mid x\geq{0} \},\operatorname{Int}(B)=B.$
**(c)**
$Bd(C)=\{ (0,y)\mid y\in \mathbb{R} \}\cup \{ (x,0)\mid x\leq{0} \},\operatorname{Int}(C)=\{ (x,y)\mid x\geq0,y \in \mathbb{R} \}.$
**(d)**
$Bd(D)=\mathbb{R}^2,\operatorname{Int}(D)=\varnothing.$
**(e)**
$Bd(E)=\{(x,y)\mid x^{2}-y^{2}=0\text{ or }1\},\operatorname{Int}(A)=\{(x,y)\mid 0< x^{2}-y^{2}<1\}.$
**(f)**
$Bd(F)=\{ (x,y)\mid xy=1\text{ or }x=0 \},\operatorname{Int}(F)=\{(x,y)\mid x\neq0\text{ and }y< 1/x\}.$
___

>[!problem] Problem 6
>Show that
>
>(a) the subspace of a Hausdorff space is Hausdorff,
>
>(b) the product of two Hausdorff spaces is Hausdorff.

**Proof**:
**(a)**
Let $Y$ be a subspace of a Hausdorff space $X$. Let $y_1, y_2 \in Y$, $y_1 \neq y_2$. In $X$, there exist disjoint open sets $U, V$ such that $y_1 \in U$, $y_2 \in V$. Then $U \cap Y$ and $V \cap Y$ are open in $Y$, disjoint, and contain $y_1$ and $y_2$ respectively. So $Y$ is Hausdorff.

**(b)**
Let $X$ and $Y$ be Hausdorff. Consider $(x_1, y_1), (x_2, y_2) \in X \times Y$ with $(x_1, y_1) \neq (x_2, y_2)$.
- If $x_1 \neq x_2$, find disjoint open $U_1, U_2$ in $X$ with $x_1 \in U_1, x_2 \in U_2$. Then $U_1 \times Y$ and $U_2 \times Y$ are disjoint open sets in the product containing the points.
- If $x_1 = x_2$, then $y_1 \neq y_2$. Find disjoint open $V_1, V_2$ in $Y$. Then $X \times V_1$ and $X \times V_2$ are the required sets.
So $X \times Y$ is Hausdorff.
___

>[!problem] Problem 7
>Show that $X$ is Hausdorff if and only if the diagonal $\Delta=\{(x,x)\mid x\in X\}$ is closed in $X\times X$.

**Proof**:
($\Rightarrow$): For any $(x,y)\in X\times X\setminus\Delta$, $x\neq y$, since Hausdorff, there exist $U,V\subseteq X$ such that $x\in U,y\in V,U\cap V=\varnothing$. Then $(x,y)\in U\times V\subseteq X\times X\setminus\Delta$. Since $U\times V$ is open, $X\times X\setminus\Delta$ is open in $X\times X$. Thus $\Delta$ is closed in $X\times X$.
($\Leftarrow$): For any $x,y\in X,x\neq y$, since $(x,y)\in X\times X\setminus\Delta$, which is an open set, there exsits a basis element $U\times V\ni(x,y)$ satisfying $U\times V\subseteq X\times X\setminus\Delta$. $U\times V\subseteq X\times X\setminus\Delta$ implies $U\cap V=\varnothing$, and $(x,y)\in U\times V$ implies $x \in U$ and $y\in V$, thus $X\times X$ is Hausdorff.
___

>[!problem] Problem 8
>Let $A\subset X$. Let $f:A\to Y$ be continuous and $Y$ be Hausdorff. Show that if $f$ may be extended to a continuous function $g:\overline{A}\to Y$, then $g$ is uniquely determined by $f$.

**Proof**: If $A=\overline{ A }$, the proof is done. If not, take any point $a\in \overline{ A }\setminus A$, then $a\in A'$.

Suppose $g_{1}, g_{2}: \overline{A} \to Y$ are two continuous extensions of $f$. Assume for contradiction that $g_{1}(a)\neq g_{2}(a)$, then by Hausdorff, there exist two open set $U,V\in Y$ such that $g_{1}(a)\in U\text{ and } g_{2}(a)\in V$. Since $g_{1},g_{2}$ are continuous, $g^{-1}(U),g^{-1}(V)$ are open, then $g^{-1}(U)\cap g^{-1}(V)$ (denoted as $W$) is open. While $W$ is an open neighborhood of $a$ and $a\in A'$, $W\cap (A\setminus \{ a \})\neq\varnothing$. Take a point $b\in W\cap (A\setminus \{ a \})$, then $g_{1}(b)\in U,g_{2}(b)\in V$, thus $g_{1}(b)\ne g_{2}(b)$. However, this contradicts to the fact that $g_{1}(b)= g_{2}(b)=f(b)$ (since $b\in A$). Therefore, $g_{1}(a)= g_{2}(a)$. And by arbitrariness of $a,g_{1}=g_{2}$. This implies the uniqueness of $g$. 
___

>[!problem] Problem 9
>Suppose $f:\mathbb{R}\to\mathbb{R}$ is continuous from the right, $i.e. \lim_{x\to a^{+}}f(x)=f(a)$ for all $a\in\mathbb{R}$. Show that $f$ is continous when viewed as a map from $\mathbb{R}_{\ell}$ to $\mathbb{R}$.

**Proof**:
To show $f$ is continuous, it's enough to show the preimage of any basis element $(c,d)$ in $\mathbb{R}$ is open in $\mathbb{R}_{\ell}$.

For any point $a \in f^{-1}((c,d))$, we have $c < f(a) < d$. By right-continuity, $\exists \delta > 0$ such that for $x \in (a, a+\delta)$, $f(x) \in (c,d)$. Thus $[a, a+\delta) \subset f^{-1}((c,d))$.

Since every point in $f^{-1}((c,d))$ has a neighborhood $[a, a+\delta)$ contained in it, $f^{-1}((c,d))$ is open in $\mathbb{R}_{\ell}$. Therefore, $f$ is continuous.
___

>[!problem] Problem 10
>Let $f:A\to X\times Y$ be given by $f(a)=(f_{1}(a),f_{2}(a))$. Prove that $f$ is continuous if and only if $f_{1},f_{2}$ are both continuous.

**Proof**:
Let $\pi_X: X \times Y \to X$ and $\pi_Y: X \times Y \to Y$ be the projection maps (they are continuous).
($\Rightarrow$): If $f$ is continuous, then $f_1 = \pi_X \circ f$ and $f_2 = \pi_Y \circ f$ are compositions of continuous maps, hence continuous.
($\Leftarrow$): Assume $f_1$ and $f_2$ are continuous. To show $f$ is continuous, it's enough to show the preimage of any basis element $U \times V$ (with $U$ open in $X$, $V$ open in $Y$) is open in $A$. $f^{-1}(U \times V) = \{a \in A \mid f_1(a) \in U \text{ and } f_2(a) \in V\} = f_1^{-1}(U) \cap f_2^{-1}(V)$. Since $f_1$ and $f_2$ are continuous, $f_1^{-1}(U)$ and $f_2^{-1}(V)$ are open in $A$. Their intersection is open in $A$. Thus, $f$ is continuous.