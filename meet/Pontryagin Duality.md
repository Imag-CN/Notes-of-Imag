___
>[!definition] Topological Group
>A set $G$ with both group and topological structures is a **topological group** if:
>1. **Continuity of multiplication**: The map $(x,y) \mapsto xy$ from $G \times G$ (product topology) to $G$ is continuous.
>2. **Continuity of inversion**: The map $x \mapsto x^{-1}$ from $G$ to $G$ is continuous.

**Examples**:
- $\mathbb{R}$ with addition and Euclidean topology.
- $\mathbb{T} = \{e^{2\pi ix} : x \in [0,1)\}$ (circle group) with multiplication.
- Any group with discrete or indiscrete topology.
___
>[!definition] Homogeneity
>A topological space $X$ is **homogeneous** if for any $x,y \in X$, there exists a homeomorphism $f: X \to X$ with $f(x)=y$.

**Key fact**: Every topological group is homogeneous (via left/right translations).
___
>[!problem] Proposition
>1. If $H$ is a subgroup of a topological group $G$, then its closure $\overline{H}$ is also a subgroup.
>2. If $H$ is a normal subgroup of $G$, the quotient group $G/H$ with quotient topology is a topological group.
>3. **Open Mapping Theorem**: For $G$ $\sigma$-compact, any continuous surjective homomorphism $G \to H$ is open.

---
>[!problem] Hausdorff Property
>1. A $T_1$ topological group is Hausdorff.
>2. Every topological group is **regular** (and completely regular if $T_0$).

---
>[!problem] Baire Category Theorem
>A locally compact Hausdorff space cannot be a countable union of nowhere dense closed sets.
>

**Corollary**: Countable locally compact Hausdorff groups are discrete.

### 4.2 Uniform Structures
- **Definition**: The left/right uniformities on $G$ make it a uniform space.
- **Proposition**: The topology induced by the uniformity agrees with the original topology.

---

## §5. Duality Preview
### 5.1 Character Group
- The **dual group** $\Gamma = G^*$ consists of continuous homomorphisms $\gamma: G \to \mathbb{T}$.
- **Example**: $\mathbb{Z}^* \cong \mathbb{T}$, $\mathbb{T}^* \cong \mathbb{Z}$.

### 5.2 Pontryagin Duality (Preview)
- **Theorem**: For LCA-groups, the canonical map $G \to \Gamma^*$ is a topological isomorphism.

---

## Key Results Summary
1. **Subgroup Structure**: Closed subgroups of $\mathbb{R}^n$ are isomorphic to $\mathbb{R}^a \times \mathbb{Z}^b$ (Theorem 4).
2. **Duality Foundation**: Compact/discrete groups satisfy duality (Theorems 15–16).
3. **Applications**: Kronecker’s theorem on Diophantine approximation (Theorem 28).