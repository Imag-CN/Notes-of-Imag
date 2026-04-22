___

>[!problem]
>Show the the Cayley complex (constructed in Example 100) is simply connected.

**Proof:** 
$\tilde{X}_G$ is connected, because its 1‑skeleton is the Cayley graph of $G$, which is connected because every $g \in G$ is a word in the generators.

The projection $p: \tilde{X}_G \to X_G$ is a covering map, with $G$ acting freely by left multiplication as deck transformations. Hence $p_*: \pi_1(\tilde{X}_G) \to \pi_1(X_G)$ is injective. $\pi_1(X_G) \cong G$ via the isomorphism $\varphi$ sending the homotopy class of the loop $e_\alpha$ to the generator $g_\alpha$.

Let $H = p_*(\pi_1(\tilde{X}_G)) \subset \pi_1(X_G)$. Under $\varphi$, an element of $\varphi(H)$ corresponds to a word in the generators that equals $1_G$. Such a word is, by definition of the presentation, a product of conjugates of the relators $r_\beta$.  

In $\tilde{X}_G$, any loop whose edge‑label is a product of conjugates of relators is already filled by the attached 2‑cells (one 2‑cell for each conjugate of a relator appearing in the word). Hence any such loop is null‑homotopic in $\tilde{X}_G$.

Therefore $H$ is trivial. Since $p_*$ is injective, $\pi_1(\tilde{X}_G)=0$, i.e., $\tilde{X}_G$ is simply connected. Consequently, as a simply‑connected covering space, it is the universal cover of $X_G$.
___

>[!problem] [HAT] 1.3.17
>Given a group $G$ and a normal subgroup $N$, show that there exists a normal covering space $\widetilde{X} \to X$ with $\pi_1(X) \approx G$, $\pi_1(\widetilde{X}) \approx N$, and deck transformation group $G(\widetilde{X}) \approx G/N$.

**Proof:**
By Corollary 1.28, for any group $G$ there exists a connected CW‑complex $X$ with $\pi_1(X) \cong G$. Fix such an $X$ and choose a base point $x_0 \in X$.

For any subgroup $H \le \pi_1(X,x_0)$ there exists a covering space $p: (\tilde{X},\tilde{x}_0) \to (X,x_0)$ such that $p_*(\pi_1(\tilde{X},\tilde{x}_0)) = H$.  

Take $H = N \le G = \pi_1(X)$. Then we obtain a covering $p: \tilde{X} \to X$ with $p_*(\pi_1(\tilde{X})) = N$.

A covering is normal iff $p_*(\pi_1(\tilde{X}))$ is a normal subgroup of $\pi_1(X)$. Since $N \trianglelefteq G$, the covering $\tilde{X} \to X$ is normal.

For a normal covering, the deck‑transformation group is isomorphic to the quotient:
$$
G(\widetilde{X}) \cong \pi_1(X,x_0) \,/\, p_*(\pi_1(\tilde{X},\tilde{x}_0)) = G/N.
$$
___

>[!problem] [HAT] 1.3.18
>Let $X$ be a path-connected, locally path-connected, and semilocally simply-connected space.  
>A path-connected covering space $\tilde{X} \to X$ is called abelian if it is a normal covering and its deck transformation group is abelian.
>
>Prove $X$ has an abelian covering space that covers every other abelian covering space;
>and that such a **universal abelian covering space** is unique up to isomorphism.
>
>Describe this covering space explicitly for $X = S^1 \vee S^1$ and $X = S^1 \vee S^1 \vee S^1$.

**Proof:**
**1. Universal abelian covering exists.**
Let $\tilde{X}_0 \to X$ be the universal covering. Then $\operatorname{Deck}(\tilde{X}_0/X) \cong \pi_1(X)$.

Let $H = [\pi_1(X),\pi_1(X)]$ be the commutator subgroup.  
By the Galois correspondence, there exists a covering space $p: \tilde{X} \to X$ with
$$
p_*(\pi_1(\tilde{X})) = H.
$$
Since $H$ is normal in $\pi_1(X)$ (commutator subgroup is always normal), Prop. 1.39 implies that $\tilde{X} \to X$ is a normal covering and
$$
\operatorname{Deck}(\tilde{X}/X) \cong \pi_1(X)/H = \pi_1(X)_{\text{ab}},
$$
which is abelian. Hence $\tilde{X}$ is an abelian covering.

**2. $\tilde{X}$ covers every other abelian covering.**
Let $q: Y \to X$ be any abelian covering. Then $\operatorname{Deck}(Y/X)$ is abelian, so $q_*(\pi_1(Y))$ is a normal subgroup of $\pi_1(X)$ with abelian quotient.  
The universal property of abelianization gives
$$
H = [\pi_1(X),\pi_1(X)] \le q_*(\pi_1(Y)).
$$
Therefore $p_*(\pi_1(\tilde{X})) = H \le q_*(\pi_1(Y))$, and by the lifting criterion (Hatcher Prop. 1.33) the map $p: \tilde{X} \to X$ lifts to a map $\tilde{X} \to Y$ making
$$
\begin{CD}
\tilde{X} @>>> Y \\
@VpVV @VVqV \\
X @= X
\end{CD}
$$
commute. Hence $\tilde{X}$ covers $Y$.

**3. Uniqueness up to isomorphism.**

If $\tilde{X}'$ is another abelian covering that covers every abelian covering, then in particular $\tilde{X}$ covers $\tilde{X}'$ and $\tilde{X}'$ covers $\tilde{X}$. Two normal coverings of $X$ that cover each other are isomorphic (Hatcher Prop. 1.37). Hence $\tilde{X}$ is unique up to isomorphism.

---

**Explicit description for $X = S^1 \vee S^1$.**
$\pi_1(X) = \langle a,b \rangle$ (free group of rank 2).  
$[\pi_1,\pi_1]$ is the commutator subgroup, and $\pi_1(X)_{\text{ab}} \cong \mathbb{Z} \times \mathbb{Z}$.  
The universal abelian covering $\tilde{X}$ is the **infinite square grid** in $\mathbb{R}^2$: vertices = integer lattice points $\mathbb{Z} \times \mathbb{Z}$, edges horizontal and vertical segments of length 1.  
The projection $\tilde{X} \to X$ maps each vertex to the wedge point, each horizontal edge to the loop $a$, each vertical edge to the loop $b$.

**For $X = S^1 \vee S^1 \vee S^1$.**
$\pi_1(X) = \langle a,b,c \rangle$, $\pi_1(X)_{\text{ab}} \cong \mathbb{Z} \times \mathbb{Z} \times \mathbb{Z}$.  
The universal abelian covering is the **infinite cubic lattice** in $\mathbb{R}^3$: vertices = $\mathbb{Z}^3$, edges parallel to the three coordinate axes.  
Projection sends edges to loops $a$, $b$, $c$ respectively.
___

> [!problem] [HAT] 1.3.30
> Draw the Cayley graph of the group
> $$
> \mathbb{Z} * \mathbb{Z}_2 = \langle a, b \mid b^2 \rangle.
> $$

**Proof:**
![[8e55d3658a72a18c7ac1dc070b068865.jpg]]