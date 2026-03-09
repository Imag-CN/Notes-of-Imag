___

>[!definition] Topology of fundamental groups
>1.  Let $(X, x_0)$ be a pointed topological space. The **loop space** $\Omega(X, x_0)$ is the set of all continuous maps $\gamma: (I, \{0,1\}) \to (X, x_0)$, where $I = [0,1]$, equipped with the **compact-open topology**.
>2.  The fundamental group $\pi_1(X, x_0)$ is the set of homotopy classes of loops, $\Omega(X, x_0)/\simeq$.
>3.  The quotient map $q: \Omega(X, x_0) \to \pi_1(X, x_0)$, sending a loop to its homotopy class, induces the **quotient topology** on $\pi_1(X, x_0)$. This topology is also called the **compact-open topology** on $\pi_1$.

**Why is this the most natural topology?**

This construction is natural for two key reasons:

•   **Continuity of Operations:** The standard group operations (concatenation, inversion) on $\Omega(X, x_0)$ are continuous in the compact-open topology. The quotient topology is the coarsest topology on $\pi_1$ that makes these induced operations continuous, turning $\pi_1(X, x_0)$ into a topological group.

•   **Functoriality:** It ensures that $\pi_1$ behaves well as a functor from pointed topological spaces to topological groups, as shown in the following theorem.
>___
>[!problem]
>**Continuity of the Induced Homomorphism**
>
>**Theorem:** Let $f: (X, x_0) \to (Y, y_0)$ be a continuous map of pointed spaces. The induced group homomorphism
>$f_*: \pi_1(X, x_0) \to \pi_1(Y, y_0)$
>is continuous with respect to the compact-open topologies on the fundamental groups.
>
>Thus, $\pi_1: \mathbf{Top}_* \to \mathbf{TopGrp}$ is a functor.
>
>**Proof Sketch:**
>
>4.  The map $f$ induces a map on the loop spaces: $\hat{f}: \Omega(X, x_0) \to \Omega(Y, y_0)$ by $\hat{f}(\gamma) = f \circ \gamma$.
>5.  **Key Fact:** Precomposition with a continuous map is continuous in the compact-open topology. Therefore, $\hat{f}$ is continuous.
>6.  The following diagram commutes:
>$$\begin{array}{ccc}
>\Omega(X, x_0) & \xrightarrow{\hat{f}} & \Omega(Y, y_0) \\
>q_X \downarrow & & \downarrow q_Y \\
>\pi_1(X, x_0) & \xrightarrow{f_*} & \pi_1(Y, y_0)
>\end{array}$$
>where $q_X, q_Y$ are the quotient maps.
>7.  Since $\hat{f}$ is continuous and $q_Y$ is a quotient map, the map $f_*$ is continuous. (If $h \circ q$ is continuous and $q$ is a quotient map, then $h$ is continuous; here, $f_* \circ q_X = q_Y \circ \hat{f}$).
>___
>[!problem]
>**The Product Problem: A Topological Counterexample**
>
>Algebraically, for path-connected spaces, we have an isomorphism:
>$\pi_1(X \times Y, (x_0, y_0)) \cong \pi_1(X, x_0) \times \pi_1(Y, y_0)$.
>
>However, when both sides are endowed with their natural topologies, this algebraic isomorphism is **not a homeomorphism** in general.
>
>**The Topologies Involved:**
>•   Left side ($\pi_1(X \times Y)$): The compact-open topology (quotient of $\Omega(X \times Y)$).
>•   Right side ($\pi_1(X) \times \pi_1(Y)$): The product topology of the compact-open topologies on each factor.
>
>**Why They Differ:**
>The discrepancy arises from the nature of the subbases defining these topologies.
>•   A subbasis for the compact-open topology on $\Omega(X \times Y)$ uses sets of the form $\langle K, U \rangle$, where $K \subset I$ is compact and $U \subset X \times Y$ is open.
>•   A subbasis for the product topology on $\Omega(X) \times \Omega(Y)$ effectively uses sets of the form $\langle K_X, U_X \rangle \times \langle K_Y, U_Y \rangle$, which corresponds to products of open sets in the factors.
>
>The family of open sets in $X \times Y$ is richer than just products of open sets from $X$ and $Y$. This difference is inherited by the quotient topologies on the fundamental groups.
>
>**Standard Counterexample:**
>Let $X = Y = \bigvee_{\mathbb{N}} S^1$, the wedge sum of countably infinitely many circles. Then:
>•   $\pi_1(X) \cong \pi_1(Y) \cong F_\infty$, the free group on countably many generators.
>•   Algebraically, $\pi_1(X \times Y) \cong F_\infty \times F_\infty \cong \pi_1(X) \times \pi_1(Y)$.
>•   Topologically, the compact-open topology on $\pi_1(X \times Y)$ is **strictly coarser** (has fewer open sets) than the product topology on $\pi_1(X) \times \pi_1(Y)$.
>•   Consequently, the algebraic isomorphism is not a homeomorphism. Typically, its inverse is not continuous.
>
>**Categorical Interpretation:** This shows that the functor $\pi_1: \mathbf{Top}_* \to \mathbf{TopGrp}$ does **not** preserve products. It only preserves products after forgetting the topology via the forgetful functor $U: \mathbf{TopGrp} \to \mathbf{Grp}$.