___

> [!problem] [HAT] 1.2.15
> Given a space $X$ with basepoint $x_0 \in X$, we may construct a CW complex $L(X)$ having a single 0‑cell, a 1‑cell $e_\gamma^1$ for each loop $\gamma$ in $X$ based at $x_0$, and a 2‑cell $e_\tau^2$ for each map $\tau$ of a standard triangle $PQR$ into $X$ taking the three vertices $P$, $Q$, and $R$ of the triangle to $x_0$. The 2‑cell $e_\tau^2$ is attached to the three 1‑cells that are the loops obtained by restricting $\tau$ to the three oriented edges $PQ$, $PR$, and $QR$.
> 
> Show that the natural map $L(X) \to X$ induces an isomorphism
> $$\pi_1(L(X)) \approx \pi_1(X, x_0).$$

**Proof:** 
Let $f: L(X) \to X$ be the natural map.  

1. **$f_*$ is surjective.**  
   Every loop $\gamma$ in $X$ based at $x_0$ corresponds to a 1‑cell $e^1_\gamma$ in $L(X)$, so $[\gamma] = f_*([e^1_\gamma])$.  

2. **$f_*$ is injective.**  
   Suppose $\omega$ is a loop in $X$ that is null‑homotopic. Then there exists a homotopy $H: I\times I \to X$ contracting $\omega$ to the constant loop. Subdivide the homotopy into triangles; each triangle $\tau$ gives a 2‑cell $e^2_\tau$ in $L(X)$. The boundary of $\tau$ is a concatenation of three edges $PQ$, $QR$, $RP$, which represent a loop $\alpha$ in $L(X)$ with $f_*(\alpha) = [\omega]$. Because $e^2_\tau$ is attached along this boundary, $\alpha$ is trivial in $\pi_1(L(X))$. Hence $f_*^{-1}([\omega]) = 0$.

Thus $f_*: \pi_1(L(X)) \to \pi_1(X,x_0)$ is an isomorphism.
___

> [!problem] [HAT] 1.2.16
> Show that the fundamental group of the surface of infinite genus shown below is free on an infinite number of generators.

**Proof:**
Let $Y$ be a torus with two disks removed. Then $Y \simeq S^1 \vee S^1$, so $\pi_1(Y) \cong \mathbb{Z}*\mathbb{Z}$.

The infinite‑genus surface is obtained by gluing infinitely many copies $Y_1, Y_2, \dots$ of $Y$ along their boundary circles.  

By van Kampen’s theorem, gluing $Y_1$ and $Y_2$ identifies one generator from each, giving $\pi_1(Y_1\cup Y_2) \cong \mathbb{Z}*\mathbb{Z}*\mathbb{Z}$.  

Each additional $Y_n$ contributes one new free generator after gluing. Hence the colimit over all gluings is a free group on infinitely many generators.
___

> [!problem] [HAT] 1.2.7
> Let $X$ be the quotient space of $S^2$ obtained by identifying the north and south poles to a single point. Put a cell complex structure on $X$ and use this to compute $\pi_1(X)$.

**Solution:**
Construct the following CW structure on $X$:
- One 0‑cell $e^0$ corresponding to the identified pole point.
- One 1‑cell $e^1$ attached to $e^0$ at both ends, forming a circle $S^1$.
- One 2‑cell $e^2$ attached via the constant map to $e^0$ (or, equivalently, the 2‑cell is attached to the 1‑skeleton by a map that collapses its boundary to the 0‑cell).

Thus the 1‑skeleton is $S^1$ and the 2‑cell is attached trivially, so the space is homotopy equivalent to $S^1 \vee S^2$.

Hence
$$
\pi_1(X) \cong \pi_1(S^1 \vee S^2) \cong \pi_1(S^1) * \pi_1(S^2) \cong \mathbb{Z} * \{1\} = \mathbb{Z}.
$$

Therefore $\pi_1(X) \cong \mathbb{Z}$.
___

> [!problem]
> Let $X$ be a path‑connected topological space. Let $\Omega^{bf}(X)$ denote the set of all basepoint‑free loops in $X$, i.e. continuous maps $f:I\to X$ with $f(0)=f(1)$. Two loops $f,g\in\Omega^{bf}(X)$ are called **basepoint‑free homotopic** if there exists a continuous map $F:I\times I\to X$ such that
> - $F(-,0)=f$,
> - $F(-,1)=g$,
> - $F(0,t)=F(1,t)$ for all $t\in I$.
> 
> Let $\pi_1^{bf}(X)$ be the set of basepoint‑free homotopy classes of loops. Define the canonical map
> $$\Phi_X:\pi_1(X,x_0)\to\pi_1^{bf}(X),\qquad \Phi_X([f])=[f]^{bf}.$$
> 
> (i) Prove that $\Phi_X$ is surjective.
> 
> (ii) Prove that $\Phi_X$ is injective if $X$ is a topological group.
> 
> (iii) Let $\Omega(X,x_0)$ be the usual (based) loop space. Show that the natural map $\Omega(X,x_0)\to\Omega^{bf}(X)$ induces a bijection on the sets of connected components.

**Proof:**
**(i)** Let $[\gamma]^{bf}\in\pi_1^{bf}(X)$. Pick $\alpha$ from $x_0$ to $\gamma(0)$. Define $f=\alpha^{-1}*\gamma*\alpha\in\Omega(X,x_0)$. Then $f$ is basepoint‑free homotopic to $\gamma$ via a homotopy that shrinks $\alpha$ and $\alpha^{-1}$, so $\Phi_X([f])=[\gamma]^{bf}$.  

**(ii)** Let $\varphi(x) = x_0^{-1} \cdot x$. Then $\varphi$ is a homeomorphism with $\varphi(x_0) = e$, and induces isomorphisms on $\pi_1$ and $\pi_1^{bf}$. So WLOG assume $x_0 = e$.

Suppose $\Phi_X([f]) = \Phi_X([g])$, so $f,g$ are basepoint-free homotopic via $F$ with $F(0,t)=F(1,t)=\gamma(t)$. Define $H(s,t) = \gamma(t)^{-1} \cdot F(s,t).$ Then $H(0,t)=H(1,t)=e$, $H(s,0)=f(s)$, $H(s,1)=g(s)$. So $H$ is a based homotopy. Hence $\Phi_{X}$ is injective.

**(iii)** Take $X=S^1\vee S^1$, $\pi_1=\langle a,b\rangle$. Let $f=a$, $g=bab^{-1}$. In $\pi_1$, $[f]\neq[g]$, but $f$ and $g$ are basepoint‑free homotopic (by dragging the basepoint along $b$. More precise construction is in the following remark). Thus $\Phi_X$ is not injective.
___

>[!remark]
>$\Phi_X$ is injective if and only if $\pi_1(X,x_0)$ is abelian.

**Proof:**
($\Rightarrow$) Assume $\Phi_X$ is injective. Let $[f],[h] \in \pi_1(X,x_0)$ be arbitrary. We will show $[h][f] = [f][h]$.

Consider the loop $g = h f h^{-1}$. Construct a free homotopy $F: I \times I \to X$ between $f$ and $g$ as follows. For $(s,t) \in I \times I$, set
$$
F(s,t) =
\begin{cases}
h(3t\cdot s) & 0 \le s \le \frac{t}{3}, \\[4pt]
f\!\left(\dfrac{s - t/3}{1 - 2t/3}\right) & \dfrac{t}{3} \le s \le 1 - \dfrac{t}{3}, \\[8pt]
h^{-1}\!\bigl(3t(1-s)\bigr) & 1 - \dfrac{t}{3} \le s \le 1,
\end{cases}
$$
with the convention that for $t=0$ the middle expression is simply $f(s)$ and the outer branches are constant at $x_0$.

One checks that $F$ is continuous, $F(s,0) = f(s)$, $F(s,1) = g(s)$, and $F(0,t) = F(1,t) = h(t)$. Hence $[f]^{bf} = [g]^{bf}$.

Since $\Phi_X$ is injective, $[f] = [g] = [h][f][h]^{-1}$, i.e. $[h][f] = [f][h]$. As $[f],[h]$ were arbitrary, $\pi_1(X,x_0)$ is abelian.

($\Leftarrow$) Assume $\pi_1(X,x_0)$ is abelian. Let $[f],[g] \in \pi_1(X,x_0)$ with $\Phi_X([f]) = \Phi_X([g])$, i.e. $f$ and $g$ are freely homotopic. Let $F$ be such a free homotopy and put $\gamma(t) = F(0,t) = F(1,t)$. Then $\gamma$ is a loop based at $x_0$. Using the same construction as above (with $f$, $h = \gamma$, and the given $F$), one obtains a based homotopy between $g$ and $\gamma f \gamma^{-1}$. Hence $[g] = [\gamma][f][\gamma]^{-1}$. Because $\pi_1$ is abelian, $[\gamma][f][\gamma]^{-1} = [f]$, so $[g] = [f]$. Thus $\Phi_X$ is injective.