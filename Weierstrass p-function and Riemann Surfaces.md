___
 Let $\Lambda = \{ n\omega_1 + m\omega_2 : n, m \in \mathbb{Z} \}$ be a lattice in $\mathbb{C}$, where $\omega_1, \omega_2$ are linearly independent over $\mathbb{R}$.

>[!definition]
>The Weierstrass $\wp$-function associated to $\Lambda$ is defined by
> $$\wp(z) = \frac{1}{z^2} + \sum_{\omega \in \Lambda \setminus \{0\}} \left[ \frac{1}{(z-\omega)^2} - \frac{1}{\omega^2} \right].$$
> Its derivative is
> $$\wp'(z) = -2 \sum_{\omega \in \Lambda} \frac{1}{(z-\omega)^3}.$$

 **Properties**:
- $\wp(z)$ is meromorphic.
- $\wp(z)$ is an even function; $\wp'(z)$ is an odd function.
- **Double Periodicity**: $\wp(z+\omega) = \wp(z)$ and $\wp'(z+\omega) = \wp'(z)$ for all $\omega \in \Lambda$.
- **Differential Equation**: It satisfies the fundamental relation
$$
\wp'(z)^2 = 4\wp(z)^3 - g_2(\Lambda) \wp(z) - g_3(\Lambda),
$$
 where $g_2(\Lambda) = 60 \sum_{\omega \in \Lambda \setminus \{0\}} \omega^{-4}$ and $g_3(\Lambda) = 140 \sum_{\omega \in \Lambda \setminus \{0\}} \omega^{-6}$.
- $\wp(z):\mathbb{C} \setminus \Lambda\to \mathbb{C}$ is surjective. Also $\wp(w)=\wp(z)$ if and only if $w\in z+\Lambda$.
___
> [!definition]
> The projective curve associated to the lattice $\Lambda$ is defined by
> $$
> C_\Lambda = \{ [x, y, z] \in \mathbb{P}_2 : y^2 z = 4x^3 - g_2 x z^2 - g_3 z^3 \}.
> $$

This curve is nonsingular.

The map $u: \mathbb{C}/\Lambda \to C_\Lambda$ defined by
$$
u(\Lambda + z) = \begin{cases} [\wp(z), \wp'(z), 1] & \text{if } z \notin \Lambda \\ [0, 1, 0] & \text{if } z \in \Lambda \end{cases}
$$
is a homeomorphism (and in fact a biholomorphism), establishing an equivalence between the complex torus $\mathbb{C}/\Lambda$ and the elliptic curve $C_\Lambda$.
___

>[!definition]
> A **Riemann surface** is a surface $S$ equipped with an equivalence class $\mathcal{H}$ of **holomorphic atlases**.
> - An **atlas** is a collection $\Phi = \{ \phi_\alpha: U_\alpha \to V_\alpha \subset \mathbb{C} \}$ of charts covering $S$ such that the transition functions $\phi_\beta \circ \phi_\alpha^{-1}$ are holomorphic.
> - Two atlases are **compatible** if their union is also a holomorphic atlas. A **holomorphic atlas** is one whose transition functions are holomorphic.



>[!example]
>1.  **Open subsets of $\mathbb{C}$**: The trivial atlas $\{1_U: U \to U\}$ makes any open $U \subset \mathbb{C}$ a Riemann surface.
>2.  **The Riemann Sphere $\mathbb{P}_1 = \mathbb{C} \cup \{\infty\}$**: Defined by two charts, $\phi: U=\mathbb{P}_1\setminus\{\infty\} \to \mathbb{C}, \phi[z,1]=z$ and $\psi: V=\mathbb{P}_1\setminus\{0\} \to \mathbb{C}, \psi[1,w]=w$. The transition function $\phi \circ \psi^{-1}(w) = 1/w$ is holomorphic.
>3.  **Polygons**: e.g. cube.
>4. **Square root**
>5.  **Nonsingular projective curves**: The set of nonsingular points of an irreducible projective curve forms a Riemann surface (by the implicit function theorem).
>6.  **Complex Tori $\mathbb{C}/\Lambda$**: The quotient map $\pi: \mathbb{C} \to \mathbb{C}/\Lambda$ is a local homeomorphism, giving $\mathbb{C}/\Lambda$ a Riemann surface structure. It is biholomorphic to the elliptic curve $C_\Lambda$ (Proposition 5.43).

>[!definition]
 >A continuous map $f: S \to T$ between Riemann surfaces is **holomorphic** if for every pair of charts $\phi_\alpha$ on $S$ and $\psi_\beta$ on $T$, the map $\psi_\beta \circ f \circ \phi_\alpha^{-1}$ is holomorphic on its domain.
