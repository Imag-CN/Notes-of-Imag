___

>[!problem] [HAT] 3.1.2
>Show that the maps $G\xrightarrow{n} G$ and $H\xrightarrow{n} H$ multiplying each element by the integer $n$ induce multiplication by $n$ in $\operatorname{Ext}(H, G)$.

**Proof:**
Let $F_\bullet \to H$ be a free resolution of $H$. The induced map $H \xrightarrow{n} H$ lifts to a chain map $F_\bullet \xrightarrow{n} F_\bullet$ (multiplication by $n$ on each term).

Apply $\operatorname{Hom}(-, G)$ to obtain a cochain map $\operatorname{Hom}(F_\bullet, G) \xrightarrow{n^*} \operatorname{Hom}(F_\bullet, G)$. This induces multiplication by $n$ on the cohomology $H^1(\operatorname{Hom}(F_\bullet, G)) = \operatorname{Ext}(H, G)$.

The same reasoning applies to $G \xrightarrow{n} G$: take an injective resolution $G \to I^\bullet$, apply $\operatorname{Hom}(H, -)$ to get a cochain map $\operatorname{Hom}(H, I^\bullet) \xrightarrow{n_*} \operatorname{Hom}(H, I^\bullet)$, which also induces multiplication by $n$ on the cohomology $\operatorname{Ext}(H, G)$.

Alternatively, from the universal coefficient theorem for $\operatorname{Ext}$: for any exact sequence $0 \to A \to B \to C \to 0$, the functor $\operatorname{Ext}(-, G)$ is additive. Since $H \xrightarrow{n} H$ is the sum of $n$ copies of the identity map, its induced map on $\operatorname{Ext}(H, G)$ is $n$ times the identity.

Therefore, both maps induce multiplication by $n$ on $\operatorname{Ext}(H, G)$.
___

>[!problem] [HAT] 3.1.3
>Regarding $\mathbb{Z}_2$ as a module over the ring $\mathbb{Z}_4$, construct a resolution of $\mathbb{Z}_2$ by free modules over $\mathbb{Z}_4$ and use this to show that $\operatorname{Ext}_{\mathbb{Z}_4}^n(\mathbb{Z}_2, \mathbb{Z}_2)$ is nonzero for all $n$.

**Proof:**
A free resolution of $\mathbb{Z}_2$ over $\mathbb{Z}_4$ is:

$$
\cdots \xrightarrow{\times 2} \mathbb{Z}_4 \xrightarrow{\times 2} \mathbb{Z}_4 \xrightarrow{\pi} \mathbb{Z}_2 \to 0
$$

where $\pi$ is the quotient and all other maps are multiplication by $2$.

Apply $\operatorname{Hom}_{\mathbb{Z}_4}(-,\mathbb{Z}_2)$. Since $\operatorname{Hom}_{\mathbb{Z}_4}(\mathbb{Z}_4,\mathbb{Z}_2)\cong\mathbb{Z}_2$, the induced map $2^*$ is zero.  

Thus the cochain complex becomes:

$$
0 \to \mathbb{Z}_2 \xrightarrow{0} \mathbb{Z}_2 \xrightarrow{0} \mathbb{Z}_2 \xrightarrow{0} \cdots
$$

Hence
$$
\operatorname{Ext}^n_{\mathbb{Z}_4}(\mathbb{Z}_2,\mathbb{Z}_2) \cong \mathbb{Z}_2 \neq 0
$$
for all $n \ge 0$.
___

>[!problem] [HAT] 3.2.4
>What happens if one defines homology groups $h_n(X; G)$ as the homology groups of the chain complex 
>$$
>\cdots \to \text{Hom}(G, C_n(X)) \to \text{Hom}(G, C_{n-1}(X)) \to \cdots ?
>$$ 
>More specifically, what are the groups $h_n(X; G)$ when $G = \mathbb{Z}$, $\mathbb{Z}_m$, and $\mathbb{Q}$?

**Proof:**
The group $\operatorname{Hom}(G, C_n(X))$ consists of homomorphisms from $G$ to the free abelian group $C_n(X)$. Since $C_n(X)$ is free abelian, $\operatorname{Hom}(G, C_n(X)) \cong \bigoplus_{\alpha} \operatorname{Hom}(G, \mathbb{Z})$, where the sum runs over a basis of $C_n(X)$.

**Case 1: $G = \mathbb{Z}$**  
$\operatorname{Hom}(\mathbb{Z}, C_n(X)) \cong C_n(X)$ because a homomorphism $\mathbb{Z} \to C_n(X)$ is determined by the image of $1$. Thus the complex becomes $\cdots \to C_n(X) \to C_{n-1}(X) \to \cdots$, so $h_n(X; \mathbb{Z}) \cong H_n(X)$.

**Case 2: $G = \mathbb{Z}_m$**  
Since $\mathbb{Z}_m$ is finite, every homomorphism $\mathbb{Z}_m \to C_n(X)$ factors through the torsion part. But $C_n(X)$ is free, so $\operatorname{Hom}(\mathbb{Z}_m, C_n(X)) = 0$. Hence $h_n(X; \mathbb{Z}_m) = 0$ for all $n$.

**Case 3: $G = \mathbb{Q}$**  
$\operatorname{Hom}(\mathbb{Q}, C_n(X)) = 0$ because $C_n(X)$ is free abelian of finite rank (or at most countable), and there is no nonzero homomorphism from $\mathbb{Q}$ to a free abelian group of finite rank. Thus $h_n(X; \mathbb{Q}) = 0$.
___

>[!problem] [HAT] 3.2.5
>Regarding a cochain $\varphi \in C^{1}(X;G)$ as a function from paths in $X$ to $G$, show that if $\varphi$ is a cocycle, then
>
>(a) $\varphi(f \cdot g) = \varphi(f) + \varphi(g)$,
>
>(b) $\varphi$ takes the value 0 on constant paths,
>
>(c) $\varphi(f) = \varphi(g)$ if $f \simeq g$,
>
>(d) $\varphi$ is a coboundary iff $\varphi(f)$ depends only on the endpoints of $f$, for all $f$.

**Proof:**
**(a)** Take a 2-simplex $\sigma: \Delta^2 \to X$ with $\partial\sigma = f - (f\cdot g) + g$, where $f$, $g$ and $f\cdot g$ are the restrictions of $\sigma$ to the three edges. Since $\varphi$ is a cocycle, we have $0 = \delta\varphi(\sigma) = \varphi(\partial\sigma) = \varphi(f) - \varphi(f\cdot g) + \varphi(g)$. Therefore $\varphi(f\cdot g) = \varphi(f) + \varphi(g)$.

**(b)** Let $c$ be a constant path. For any path $f$, we have $c \cdot f = f$ (up to reparametrization). Applying (a) gives $\varphi(c) + \varphi(f) = \varphi(f)$, hence $\varphi(c) = 0$.

**(c)** Suppose $f \simeq g$ via a homotopy $H: I\times I \to X$.

View $H$ as a 2-simplex $\sigma$ with $\partial\sigma = f - h + g$, where $h$ is a constant path (the vertical edge of the square). Then $0 = \varphi(\partial\sigma) = \varphi(f) - \varphi(h) + \varphi(g)$. By (b), $\varphi(h) = 0$, so $\varphi(f) = \varphi(g)$.

**(d)** If $\varphi = \delta\psi$, then for any path $f$, $\varphi(f) = \delta\psi(f) = \psi(f(0)) - \psi(f(1))$, which depends only on the endpoints.

Conversely, suppose $\varphi(f)$ depends only on endpoints. Choose a basepoint $x_0$ in each path component and define $\psi(x)=\varphi(\gamma_x)$ where $\gamma_x$ is any path from $x_0$ to $x$. Then
$$
\delta\psi(f)=\psi(f(0))-\psi(f(1))=\varphi(\gamma_{f(0)})-\varphi(\gamma_{f(1)}).
$$
Since $\gamma_{f(0)}\cdot f$ and $\gamma_{f(1)}$ have the same endpoints, $\varphi(\gamma_{f(0)}\cdot f)=\varphi(\gamma_{f(1)})$. But $\varphi(\gamma_{f(0)}\cdot f)=\varphi(\gamma_{f(0)})+\varphi(f)$, hence $\delta\psi(f)=\varphi(\gamma_{f(0)})-\varphi(\gamma_{f(0)})-\varphi(f)=-\varphi(f)$. Thus $\varphi=-\delta\psi$ is a coboundary.