___
>[!definition] Differential forms
>On a smooth manifold $M$, a $k$-form is an antisymmetric $k$-covariant tensor field, locally expressed as:
  $$\omega = \sum f_{i_1 \dots i_k} dx^{i_1} \wedge \dots \wedge dx^{i_k}$$
  where $f_{i_1 \dots i_k}$ are smooth functions and $\wedge$ is the wedge product.

- **Exterior derivative ($d$)**: Maps $k$-forms to $(k+1)$-forms, satisfying:
  - $d^2 = 0$ (Poincaré lemma).
  - Leibniz rule: $d(\omega \wedge \eta) = d\omega \wedge \eta + (-1)^{\deg \omega} \omega \wedge d\eta$.

- **de Rham complex**: The chain complex $(\Omega^*(M), d)$:
  $$0 \to \Omega^0(M) \xrightarrow{d} \Omega^1(M) \xrightarrow{d} \dots \xrightarrow{d} \Omega^n(M) \to 0$$

## §2. de Rham Cohomology
- **Definition**: The $k$-th de Rham cohomology group is:
  $$H^k_{\text{dR}}(M) = \frac{\ker d: \Omega^k(M) \to \Omega^{k+1}(M)}{\operatorname{im} d: \Omega^{k-1}(M) \to \Omega^k(M)}$$
  - Measures "holes" in $M$ (e.g., $H^1(S^1) \cong \mathbb{R}$ for the circle).

- **Examples**:
  - $\mathbb{R}^n$: $H^k_{\text{dR}}(\mathbb{R}^n) = \mathbb{R}$ if $k=0$, else $0$.
  - Sphere $S^n$: $H^0(S^n) \cong H^n(S^n) \cong \mathbb{R}$, others zero.

## §3. Mayer-Vietoris Sequence
- **Construction**: For an open cover $M = U \cup V$, the sequence relates local and global cohomology:
  $$\cdots \to H^k(M) \to H^k(U) \oplus H^k(V) \to H^k(U \cap V) \xrightarrow{d^*} H^{k+1}(M) \to \cdots$$
  - **Key use**: Computes $H^*(M)$ by decomposing into simpler subsets.

- **Application to $S^1$**:
  - Cover $S^1$ with two open arcs $U$, $V$; $U \cap V$ is two intervals.
  - Yields $H^0(S^1) \cong \mathbb{R}$, $H^1(S^1) \cong \mathbb{R}$.

## §4. Homotopy Invariance
- **Theorem**: If $M$ and $N$ are homotopy equivalent, then:
  $$H^*_{\text{dR}}(M) \cong H^*_{\text{dR}}(N)$$
  - **Corollary**: $\mathbb{R}^n$ is contractible $\Rightarrow$ $H^k(\mathbb{R}^n) = 0$ for $k > 0$.

## §5. Compact Support Cohomology
- **Definition**: Forms with compact support $\Omega_c^*(M)$ yield cohomology $H_c^*(M)$.
  - For non-compact $M$, $H_c^*(M) \neq H^*(M)$ (e.g., $H_c^0(\mathbb{R}) = 0$).
  - For compact $M$, $H_c^*(M) \cong H^*(M)$.

## Key Results
1. **Poincaré Lemma**: On contractible $M$, $H^k_{\text{dR}}(M) = 0$ for $k > 0$.
2. **de Rham Theorem**: $H^*_{\text{dR}}(M) \cong H^*(M; \mathbb{R})$ (singular cohomology with real coefficients).
3. **Methodology**: Local-to-global (Mayer-Vietoris) and homotopy tools simplify computations.