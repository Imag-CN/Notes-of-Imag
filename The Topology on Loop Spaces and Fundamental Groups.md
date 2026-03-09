___

>[!definition] The Topology on Loop Spaces and Fundamental Groups
>
>Let $(X, x_0)$ and $(Y, y_0)$ be pointed topological spaces. We denote their loop spaces by $\Omega(X, x_0)$ and $\Omega(Y, y_0)$, both equipped with the **compact-open topology**.
>The fundamental groups are the quotient spaces $\pi_1(X, x_0) = \Omega(X, x_0)/\simeq$ and $\pi_1(Y, y_0) = \Omega(Y, y_0)/\simeq$, endowed with the corresponding quotient topologies (also called the compact-open topology).


>**1. Induced Maps on Loop Spaces**
>
>Let $f: (X, x_0) \to (Y, y_0)$ be a continuous map. It induces a map on the level of loop spaces:
>$\hat{f}: \Omega(X, x_0) \to \Omega(Y, y_0)$
>defined by $\hat{f}(\gamma) = f \circ \gamma$ for any $\gamma \in \Omega(X, x_0)$.
>
>**Key Property:** The map $\hat{f}$ is **continuous** in the compact-open topology.
>
>**Reason:** Precomposition with a continuous map is a continuous operation in the compact-open topology. More formally, for a subbasic open set $\langle K, V \rangle = \{ \alpha \in \Omega(Y, y_0) \mid \alpha(K) \subset V \}$ in $\Omega(Y, y_0)$, its preimage under $\hat{f}$ is $\hat{f}^{-1}(\langle K, V \rangle) = \langle K, f^{-1}(V) \rangle$, which is open in $\Omega(X, x_0)$.
>___
>[!problem]
>**2. Induced Homomorphisms on Fundamental Groups**
>
>The map $\hat{f}$ descends to a well-defined group homomorphism on the homotopy classes:
>$f_*: \pi_1(X, x_0) \to \pi_1(Y, y_0)$
>defined by $f_*([\gamma]) = [f \circ \gamma] = [\hat{f}(\gamma)]$.
>
>**Theorem (Continuity of $f_*$):** The induced homomorphism $f_*$ is continuous with respect to the compact-open (quotient) topologies on the fundamental groups.
>
>**Proof Sketch:** Consider the commutative diagram:
>$$\begin{array}{ccc}
>\Omega(X, x_0) & \xrightarrow{\hat{f}} & \Omega(Y, y_0) \\
>q_X \downarrow & & \downarrow q_Y \\
>\pi_1(X, x_0) & \xrightarrow{f_*} & \pi_1(Y, y_0)
>\end{array}$$
>where $q_X$ and $q_Y$ are the quotient maps. Since $\hat{f}$ is continuous and $q_Y$ is a quotient map, the map $f_*$ is continuous. (If $h \circ q$ is continuous and $q$ is a quotient map, then $h$ is continuous; apply this with $h = f_*$ and $q = q_X$, noting that $f_* \circ q_X = q_Y \circ \hat{f}$).
>
>**Conclusion:** This makes $\pi_1: \mathbf{Top}_* \to \mathbf{TopGrp}$ a functor to the category of topological groups.
>___
>[!problem]
>**3. The Product Case: Loop Spaces**
>
>For two spaces $X$ and $Y$, consider the product space $X \times Y$. There is a natural map between loop spaces:
>$\Psi: \Omega(X, x_0) \times \Omega(Y, y_0) \to \Omega(X \times Y, (x_0, y_0))$
>defined by $\Psi(\gamma, \eta)(t) = (\gamma(t), \eta(t))$.
>
>**Property:** The map $\Psi$ is a **homeomorphism** when the domain has the product topology (of the compact-open topologies) and the codomain has the compact-open topology.
>
>**Reason:** The compact-open topology on a mapping space $Z^I$ respects products nicely: $(X \times Y)^I$ is homeomorphic to $X^I \times Y^I$ with the product topology. The map $\Psi$ provides this explicit identification for the subspace of loops.
>___
>[!problem]
>**4. The Product Case: Fundamental Groups**
>
>Passing to homotopy classes, the homeomorphism $\Psi$ induces a group isomorphism on the fundamental groups:
>$\psi: \pi_1(X, x_0) \times \pi_1(Y, y_0) \to \pi_1(X \times Y, (x_0, y_0))$
>defined by $\psi([\gamma], [\eta]) = [(\gamma, \eta)]$, where $(\gamma, \eta)(t) = (\gamma(t), \eta(t))$.
>
>Algebraically, this is the standard isomorphism: $\pi_1(X \times Y) \cong \pi_1(X) \times \pi_1(Y)$.
>
>**The Topological Problem:** While $\Psi$ is a homeomorphism of loop spaces, the induced map $\psi$ on the quotients is **not a homeomorphism** in general.
>
>Let $\mathcal{T}_{\text{prod}}$ be the product topology on $\pi_1(X) \times \pi_1(Y)$ (each factor with its quotient compact-open topology).
>Let $\mathcal{T}_{\text{co}}$ be the compact-open (quotient) topology on $\pi_1(X \times Y)$.
>
>**The Key Discrepancy:** The topology $\mathcal{T}_{\text{co}}$ on $\pi_1(X \times Y)$ is **coarser** (i.e., has fewer open sets) than the topology obtained by transporting the product topology $\mathcal{T}_{\text{prod}}$ via the algebraic isomorphism $\psi$. In other words, $\psi: (\pi_1(X) \times \pi_1(Y), \mathcal{T}_{\text{prod}}) \to (\pi_1(X \times Y), \mathcal{T}_{\text{co}})$ is continuous, but its inverse is not.
>
>**Why?** The quotient map $q: \Omega(X \times Y) \to \pi_1(X \times Y)$ can identify more points (i.e., be a "larger" equivalence relation) than the product of the individual quotient maps $q_X \times q_Y: \Omega(X) \times \Omega(Y) \to \pi_1(X) \times \pi_1(Y)$. A set that is open in the product of the quotient topologies might not be the image of an open set from $\Omega(X \times Y)$.
>
>**Counterexample:** As before, take $X = Y = \bigvee_{\mathbb{N}} S^1$. The algebraic isomorphism $\psi$ is not a homeomorphism; the product topology $\mathcal{T}_{\text{prod}}$ is strictly finer than $\mathcal{T}_{\text{co}}$.
>
>**Categorical Consequence:** The functor $\pi_1: \mathbf{Top}_* \to \mathbf{TopGrp}$ does **not** preserve products. The product in $\mathbf{TopGrp}$ is the ordinary product topology, which is not homeomorphic to the topology $\pi_1$ assigns to the product space._