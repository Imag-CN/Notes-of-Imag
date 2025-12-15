>[!problem] Problem 1
>Show that if $X$ is a subspace of $Y$, and $A$ is a subset of $X$, then the topology $A$ inherits from $X$ is the same as the topology it inherits from $Y$.

Let $\mathcal{T}_X$ be the topology on $A$ from $X$, $\mathcal{T}_Y$ from $Y$.

-   Let $U \in \mathcal{T}_X$. Then $U = V \cap A$ for some open $V$ in $X$.
    Since $X \subset Y$, $V = W \cap X$ for some open $W$ in $Y$.
    Thus, $U = (W \cap X) \cap A = W \cap A \in \mathcal{T}_Y$.

-   Let $U \in \mathcal{T}_Y$. Then $U = W \cap A$ for some open $W$ in $Y$.
    Then $U = (W \cap X) \cap A$, and $W \cap X$ is open in $X$.
    Thus, $U \in \mathcal{T}_X$.

Hence, $\mathcal{T}_X = \mathcal{T}_Y$.
___
>[!problem] Problem 2
>Consider the set $Y=[-1,1]$ as a subspace of $\mathbb{R}$. Which of the following sets are open in $Y$? Which are open in $\mathbb{R}$?
>$$A=\{x\mid\frac{1}{2}<|x|<1\},$$
>$$B=\{x\mid\frac{1}{2}<|x|\leq 1\},$$
>$$C=\{x\mid\frac{1}{2}\leq|x|<1\},$$
>$$D=\{x\mid\frac{1}{2}\leq|x|\leq 1\},$$
>$$E=\{x\mid 0<|x|<1\text{ and}\frac{1}{x}\notin Z_{+}\}.$$

Open in $Y:A,B,E;$
Open in $\mathbb{R}:A,E$.
___
>[!problem] Problem 3
>Let $X,Y$ be two topological spaces, and $X\times Y$ be the product space. Show that the projections $\pi_{1}:X\times Y\to X$ and $\pi_{2}:X\times Y\to Y$ are open maps. That is, it sends open sets to open sets.

Let $U \subset X \times Y$ be an open set, we show $\pi_1(U)$ is open in $X$.

Take an arbitrary $x\in\pi_1(U)$,$(x,y) \in U$, then there exists some $y\in Y,s.t.(x,y) \in U$.
Since $U$ is open, there exists a basis open set $V \times W \subset U$ with $(x, y) \in V \times W$, where $V$ is open in $X$ and $W$ is open in $Y$.
Then $x=\pi_{1}(x,y) \in \pi_{1}(V \times W)=V$. because 
For any $x' \in V$, we have $(x', y) \in V \times W \subset U$, so $x' \in \pi_1(U)$.
Thus $V \subset \pi_1(U),i.e.$ $\pi_1(U)$ contains a neighborhood of $x$.
Since $x$ is arbitrary, $\pi_1(U)$ is open.
Therefore, $\pi_{1}$ is an open map.

Similarily, $\pi_{2}$ is an open map.

>[!tip] Remark
>Projection maps are continous (let $U$ be an open set in $X$, then $\pi_{1}(U)=U\times Y$, which is open).
>When it comes to infinite dimensions, under both the product topology and the box topology, the projection maps are stills continuous and open maps (proofs are similar).
>However, projection maps don't necessarily send closed set to closed set (for example, $\{ (x,y)\in \mathbb{R}^2: xy\geq 1 \}$).

___
>[!problem] Problem 4
>Let $(X,d)$ be a metric space. Let $A\subset X$. Prove the restricted metric on A is a metric that induces the subspace topology on A.

The restricted metric $d_A$ on $A$ is defined by $d_A(a,b) = d(a,b)$ for all $a,b \in A$.
Inherited from $d$, $d_A$ is a metric on $A$.
We need to show that the metric topology $\mathcal{T}_{d_A}$ induced by $d_A$ equals the subspace topology $\mathcal{T}_A$ on $A$

Any basis element of $\mathcal{T}_{d_A}$ is of form $B_{d_A}(a,r) = \{x \in A \mid d_A(a,x) < r\} = B_d(a,r) \cap A$, which is open in $\mathcal{T}_A$, thus $\mathcal{T}_{d_A} \subseteq \mathcal{T}_A$.

Any open set in $\mathcal{T}_A$ is of form $U \cap A$ where $U$ is open in $X$.
For any $a \in U \cap A$, there exists $r>0$ such that $B_d(a,r) \subset U$.
Then $B_{d_A}(a,r) = B_d(a,r) \cap A \subseteq U \cap A$, thus $\mathcal{T}_A \subseteq \mathcal{T}_{d_A}$.

Therefore, $\mathcal{T}_A = \mathcal{T}_{d_A}$.
___
>[!problem] Problem 5
>Let $f:X\to Y$ be a surjective map, then there exists an equivalence relation $\sim$ on $X$ such that $X/\sim$ can be naturally identified with $Y$.

Since $f: X \to Y$ is surjective, we can define an equivalence relation $\sim$ on $X$ by:
$$x_1 \sim x_2 \iff f(x_1) = f(x_2).$$
Verifying equivalence relation:
- Reflexive: $f(x) = f(x)$ so $x \sim x$
- Symmetric: If $f(x_1) = f(x_2)$ then $f(x_2) = f(x_1)$
- Transitive: If $f(x_1) = f(x_2)$ and $f(x_2) = f(x_3)$ then $f(x_1) = f(x_3)$

Let $\pi: X \to X/{\sim}$ be the quotient map.
Define $\tilde{f}: X/{\sim} \to Y$ by:
$$\tilde{f}([x]) = f(x).$$
This is well-defined because if $[x] = [y]$, then $x \sim y$, so $f(x) = f(y)$.

The map $\tilde{f}$ is:
- Injective: If $\tilde{f}([x]) = \tilde{f}([y])$, then $f(x) = f(y)$, so $x \sim y$, hence $[x] = [y]$
- Surjective: For any $y \in Y$, since $f$ is surjective, there exists $x \in X$ with $f(x) = y$, so $\tilde{f}([x]) = y$.

Thus $\tilde{f}$ is a bijection, providing a natural identification between $X/{\sim}$ and $Y$.
___
>[!problem] Problem 6
>Describe an equivalence relation $\sim$ on $Z\times(Z\backslash\{0\})$ such that the set of rational numbers can be naturally identified with $Z\times(Z\backslash\{0\})/\sim$.

Define the equivalence relation $\sim$ on $\mathbb{Z} \times (\mathbb{Z} \setminus \{0\})$ by:
$$(a, b) \sim (c, d) \iff ad = bc$$

Verifying equivalence relation:
- Reflexive: $(a, b) \sim (a, b)$ since $ab = ab$
- Symmetric: If $(a, b) \sim (c, d)$ then $ad = bc$, so $cb = da$, hence $(c, d) \sim (a, b)$
- Transitive: If $(a, b) \sim (c, d)$ and $(c, d) \sim (e, f)$, then $ad = bc$ and $cf = de$. Multiply the first equality by $f$ yields $adf = bcf$. Substitute $cf = de$: $adf = bde$. Since $d \neq 0$, we get $af = be$, so $(a, b) \sim (e, f)$

Define the map $\phi: \mathbb{Z} \times (\mathbb{Z} \setminus \{0\})/{\sim} \to \mathbb{Q}$ by:
$$\phi([(a, b)]) = \frac{a}{b}$$

This is well-defined because if $(a, b) \sim (c, d)$, then $ad = bc$, so $\frac{a}{b} = \frac{c}{d}$.

The map $\phi$ is:
- Injective: If $\phi([(a, b)]) = \phi([(c, d)])$, then $\frac{a}{b} = \frac{c}{d}$, so $ad = bc$, hence $[(a, b)] = [(c, d)]$.
- Surjective: Any rational number $q \in \mathbb{Q}$ can be written as $q = \frac{a}{b}$ with $b \neq 0$, so $q = \phi([(a, b)])$.

Thus $\phi$ is a bijection, providing the natural identification.
___
>[!problem] Problem 7
>Define an equivalence relation $\sim$ on $\mathbb{R}^{2}$ by the following
>$$(x_{1},y_{1})\sim(x_{2},y_{2})\text{ if }x_{1}+y_{1}^{2}=x_{2}+y_{2}^{2}.$$
>Describe the quotient space.

Suppose the quotient map is $\pi: \mathbb{R}^2\to \mathbb{R}^2/\sim$.

We shall show that the quotient space is homeomorphic to $\mathbb{R}$ (equiped with standard Euclidean topology).
Define the map $\phi: \mathbb{R}^2/{\sim} \to \mathbb{R}$ by:
$$\phi([(x, y)]) = x+y^2.$$
This is well-defined because if $(x_{1}, y_{1}) \sim (x_{2}, y_{2})$, then $x_{1}+y_{1}^{2}=x_{2}+y_{2}^{2}$, so $\phi([(x_{1},y_{1} )]) = \phi([(x_{2}, y_{2})])$.

The map $\phi$ is:
- Injective: If $\phi([(x_{1},y_{1} )]) = \phi([(x_{2}, y_{2})])$, then $x_{1}+y_{1}^{2}=x_{2}+y_{2}^{2}$, hence $[(x_{1}, y_{1})] = [(x_{2}, y_{2})]$.
- Surjective: For any $C \in \mathbb{R}$ we have $\phi([(C,0)])=C$.

To show homeomorphism, we also need to show that both $\phi$ and $\phi ^{-1}$ are continuous:
- $\phi$ is continuous: Let $U \subset \mathbb{R}$ be open. Then $\phi^{-1}(U) = \{[ (x,y) ] : x+y^2 \in U\}$. Its preimage under the quotient map $\pi$ is $\{(x,y) : x+y^2 \in U\}$, which is open in $\mathbb{R}^2$ because it is the inverse image of the open set $U$ under the continuous function $(x,y) \to x+y^2$. By definition of quotient topology, $\phi^{-1}(U)$ is open in $\mathbb{R}^2/{\sim}$.
- $\phi^{-1}$ is continuous: Define inclusion map: $i:\mathbb{R}\to \mathbb{R}^2,C\to(C,0)$. Since projection maps are open maps (proven in Problem 3), inclusion map $i$ is continuous. By definition $\pi$ is continuous. Therefore, $\phi^{-1}=\pi \circ i$ is continuous for it is a composition of continuous maps.
Thus, $\phi$ is a homeomorphism, and $\mathbb{R}^2/{\sim} \cong \mathbb{R}$.
___
>[!problem] Problem 8
>Define an equivalence relation $\sim$ on $\mathbb{R}^{2}$ by the following
>$$(x_{1},y_{1})\sim(x_{2},y_{2})\text{ if }x_{1}^{2}+y_{1}^{2}=x_{2}^{2}+y_{2}^{2}.$$
>Describe the quotient space.

Suppose the quotient map is $\pi: \mathbb{R}^2\to \mathbb{R}^2/\sim$.

We shall show that the quotient space homeomorphic to $\mathbb{R}_{\geq 0}$ (as subspace of $\mathbb{R}$ equiped with standard Euclidean topology).

Define the map $\phi: \mathbb{R}^2/{\sim} \to \mathbb{R}_{\geq 0}$ by:
$$\phi([(x, y)]) = x^2+y^2.$$
This is well-defined because if $(x_{1}, y_{1}) \sim (x_{2}, y_{2})$, then $x_{1}^2+y_{1}^{2}=x_{2}^2+y_{2}^{2}$, so $\phi([(x_{1},y_{1} )]) = \phi([(x_{2}, y_{2})])$.

The map $\phi$ is:
- Injective: If $\phi([(x_{1},y_{1} )]) = \phi([(x_{2}, y_{2})])$, then $x_{1}^{2}+y_{1}^{2}=x_{2}^{2}+y_{2}^{2}$, hence $[(x_{1}, y_{1})] = [(x_{2}, y_{2})]$.
- Surjective: For any $C \in \mathbb{R}_{\geq 0}$ we have $\phi([(\sqrt{ C },0)])=C$.

To show homeomorphism, we also need to show that both $\phi$ and $\phi ^{-1}$ are continuous:
- $\phi$ is continuous: Let $U \subset \mathbb{R}_{\geq 0}$ be open. Then $\phi^{-1}(U) = \{[ (x,y) ] : x^2+y^2 \in U\}$. Its preimage under the quotient map $\pi$ is $\{(x,y) : x^2+y^2 \in U\}$, which is open in $\mathbb{R}^2$ because it is the inverse image of the open set $U$ under the continuous function $(x,y) \to x^2+y^2$. By definition of quotient topology, $\phi^{-1}(U)$ is open in $\mathbb{R}^2/{\sim}$.
- $\phi^{-1}$ is continuous: Define square root map $s: \mathbb{R}_{\geq 0}\to \mathbb{R}, C \to \sqrt{ C }$, we already know square root map is continuous. Define inclusion map: $i:\mathbb{R}\to \mathbb{R}^2,C\to(C,0)$. Since projection maps are open maps (proven in Problem 3), inclusion map $i$ is continuous. By definition $\pi$ is continuous. Therefore, $\phi^{-1}=\pi \circ i\circ s$ is continuous for it is a composition of continuous maps.

Thus, $\phi$ is a homeomorphism, and $\mathbb{R}^2/{\sim} \cong \mathbb{R}_{\geq 0}$.
>[!tip] Remark
>To illustrate continuity of $\phi$ in Problem 7 and Problem 8, the better (and more nature) way is to use universal property.
>
>Let $X$ be a topological space with an equivalence relation $\sim$, and let $\pi: X \to X/{\sim}$ be the quotient map. The universal property states: If $Y$ is any topological space, a function $g: X/{\sim} \to Y$ is continuous if and only if the composition $g \circ \pi: X \to Y$ is continuous.
>
>Take Problem 7 for example.  $(\phi \circ \pi)(x, y) = \phi([(x, y)]) = x + y^2$ is continous, thus by universal property, $\phi$ is continuous. 
>
>The proof in the main text essentially amounts to reproving the universal property.

