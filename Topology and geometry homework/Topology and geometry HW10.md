___

>[!problem] Problem 1
>Show that the cylinder $\{(x, y, z) \in \mathbb{R}^3;\ x^2 + y^2 = 1\}$ is a regular surface, and find parametrizations whose coordinate neighborhoods cover it.

**Proof:** 
Parametrization 1:
- **Domain:** $U_1 = (0, 2\pi) \times \mathbb{R}$
- **Map:** $\mathbf{x}(u,v) = (\cos u, \sin u, v)$
- **Covers:** $S \setminus \{(1,0,z)\}$

Parametrization 2:
- **Domain:** $U_2 = (-\pi, \pi) \times \mathbb{R}$
- **Map:** $\mathbf{y}(\tilde{u},\tilde{v}) = (\cos \tilde{u}, \sin \tilde{u}, \tilde{v})$
- **Covers:** $S \setminus \{(-1,0,z)\}$

Each parametrization satisfies:
1. **Smoothness:** $C^\infty$ (elementary functions).
2. **Homeomorphism:** Bijective with continuous inverse.
3. **Regularity:** $\mathbf{x}_u = (-\sin u, \cos u, 0)$, $\mathbf{x}_v = (0, 0, 1)$ are linearly independent (similar for $\mathbf{y}$).

And $\mathbf{x}(U_1) \cup \mathbf{y}(U_2) = S$.

Therefore, $S$ is a regular surface.
___

>[!problem] Problem 2
>Show that the two-sheeted cone, with its vertex at the origin, that is, the set $\{(x, y, z) \in \mathbb{R}^{3} ;\ x^{2} + y^{2} - z^{2} = 0\}$, is not a regular surface.

**Proof:** Denote the set $\{(x, y, z) \in \mathbb{R}^{3} ;\ x^{2} + y^{2} - z^{2} = 0\}$ as $S$.

Assume for contradiction that $S$ is a regular surface. Then there exists a neighborhood $V \subset S$ of $(0,0,0)$ and a homeomorphism $\mathbf{x}: U \subset \mathbb{R}^2 \to V$ with $\mathbf{x}(u_0,v_0) = (0,0,0)$.

Suppose $V$ is connected (otherwise substitute $V$ with the connected component containing $(0,0,0)$ ), then $U$ is connected because a homeomorphism would preserve connectedness. Consider the set $V \setminus \{(0,0,0)\}$. This set is disconnected (it consists of two separate sheets of the cone, which are both open and non-empty). However the set $U \setminus \{(u_0,v_0)\}$ is connected, thus contradiction.

Therefore, $S$ is not a regular surface.
___

>[!problem] Problem 3
>Let $f(x, y, z) = (x + y + z - 1)^2$.
>
>a. Locate the critical points and critical values of $f$.
>
>b. For what values of $c$ is the set $f(x, y, z) = c$ a regular surface?
>
>c. Answer the questions of parts $a$ and $b$ for the function $f(x, y, z) = xyz^2$.

**Proof:**
**a.** Compute the Gradient: $\nabla f = 2(x+y+z-1)(1,1,1)$. So $\nabla f=0\iff x+y+z-1=0$.
Thus Critical points: $\{(x,y,z) : x + y + z = 1\}$ (plane);
And Critical value: $c = 0$.

**b.** Discuss three cases:
- $c > 0$: $c=(\sqrt{ c }+1+0-1)^2\Rightarrow c\in f(\mathbb{R}^3)$, and $c$ is a regular value, thus the surface is regular.
- $c = 0$: Single plane, thus regular.
- $c < 0$: Empty set, not surface.

Therefore $f(x,y,z) = c$ is a regular surface iff $c \geq 0$.

**c.**
Compute the Gradient: $\nabla f = (yz^2, xz^2, 2xyz)$. So $\nabla f=0\iff z=0\text{ or }x=y=0$
Thus Critical points: $xy$-plane and $z$-axis
And Critical value: $c = 0$.

- $c \neq 0$: $c=c\cdot1\cdot 1^2 \Rightarrow c\in f(\mathbb{R}^3)$, and $c$ is a regular value, thus the surface is regular.
- $c = 0$: The surface becomes the union of $xy$-plane, $yz$-plane and $xz$-plane, thus not regular (it has no tangent plane at $(0,0,0)$).

Therefore, $f(x,y,z) = c$ is a regular surface iff $c \neq 0$.
___

>[!problem] Problem 4
>Show that the set $S = \{(x, y, z) \in \mathbb{R}^{3} ;\ z = x^{2} - y^{2}\}$ is a regular surface and check that parts $a$ and $b$ are parametrizations for $S$:
>
>a. $\mathbf{x}(u, v) = (u + v, u - v, 4uv),\ (u, v) \in \mathbb{R}^{2}$.
>
>b. $\mathbf{x}(u, v) = (u\cosh v, u\sinh v, u^{2}),\ (u, v) \in \mathbb{R}^{2},\ u \neq 0$.
>
>What parts of $S$ do these parametrizations cover?

**Proof:**
**a.** Check:
- Smooth because it is polynomial.
- Homeomorphic:
  First check injective:
  Suppose $(u+v, u-v, 4uv) = (u'+v', u'-v', 4u'v')$
  Then $u+v = u'+v'$ and $u-v = u'-v'$
  Adding: $2u = 2u' \Rightarrow u = u'$
  Subtracting: $2v = 2v' \Rightarrow v = v'$
  So injective.
  The map is continuous, and inverse $(x,y,z)\mapsto((x+y) /2,(x-y) /2)$ is continuous. Therefore homeomorphic.
- Regular: $\mathbf{x}_u = (1, 1, 4v)$, $\mathbf{x}_v = (1, -1, 4u)$. These are linearly independent.

The map $(u,v) \mapsto (x,y) = (u+v, u-v)$ is surjective onto $\mathbb{R}^2$.
Thus $\mathbf{x}$ covers all of $S$.

Therefore, $S$ is regular.

**b.** Check:
- Smooth because it is fundamental.
- Homeomorphic:
  First check injective:
  If $(u\cosh v, u\sinh v, u^2) = (u'\cosh v', u'\sinh v', (u')^2)$
  Then $u^2 = (u')^2 \Rightarrow u' = \pm u$
  And $\cosh v = \pm \cosh v'$, $\sinh v = \pm \sinh v'$
  For $u>0$ and $v\in\mathbb{R}$, it's injective; similarly for $u<0$.
  The map is continuous, and inverse $(x,y,z)\mapsto(x / \cosh(\operatorname{arctanh}(y /x)),\operatorname{arctanh}(y /x))$ is continuous. Therefore homeomorphic.
- Regular: $\mathbf{x}_u = (\cosh v, \sinh v, 2u)$, $\mathbf{x}_v = (u\sinh v, u\cosh v, 0)$
  Cross product: $(2u^2\cosh v, 2u^2\sinh v, -u)$
  For $u\neq0$, this is never $(0,0,0)$, So regular.

Cover:
- For $u>0$: $x = u\cosh v > 0$ (since $\cosh v \ge 1$)
  Covers $\{(x,y,z)\in S : x>0\}$ (right sheet)
- For $u<0$: $x = u\cosh v < 0$
  Covers $\{(x,y,z)\in S : x<0\}$ (left sheet)
- Missing: $x=0$ implies $u=0$, excluded from domain
  $x=0$ in $S$ means $z=-y^2$ (parabola in $y$-$z$ plane)

Therefore, parametrization covers $S \setminus \{x=0\}$ (two separate maps for $u>0$ and $u<0$).
___

>[!problem] Problem 5
>One way to define a system of coordinates for the sphere $S^{2}$, given by $x^{2}+y^{2}+(z-1)^{2}=1$, is to consider the so-called stereographic projection $\pi\colon S^{2}\setminus\{N\}\rightarrow \mathbb{R}^{2}$ which carries a point $p=(x,y,z)$ of the sphere $S^{2}$ minus the north pole $N=(0,0,2)$ onto the intersection of the $xy$ plane with the straight line which connects $N$ to $p$ (Fig. 2-12). Let $(u,v)=\pi(x,y,z)$, where $(x,y,z)\in S^{2}\setminus\{N\}$ and $(u,v)\in xy$ plane.
>
>a. Show that $\pi^{-1}\colon \mathbb{R}^{2}\rightarrow S^{2}$ is given by
>$$ \pi^{-1}\left\{\begin{aligned}&x=\frac{4u}{u^2+v^2+4},\\ &y=\frac{4v}{u^2+v^2+4},\\ &z=\frac{2(u^2+v^2)}{u^2+v^2+4}.\end{aligned}\right. $$
>
>b. Show that it is possible, using stereographic projection, to cover the sphere with two coordinate neighborhoods.

**Proof:**
**a.** Line through $N$ and $p=(x,y,z)$:
$$
(X,Y,Z) = (0,0,2) + t(x,y,z-2)
$$
Intersection with $xy$-plane ($Z=0$):
$$
t = \frac{-2}{z-2}
$$
Projection coordinates:
$$
u = \frac{-2x}{z-2},\quad v = \frac{-2y}{z-2}
$$
Inverse mapping:
$$
\pi^{-1}(u,v) = \left(\frac{4u}{u^{2}+v^{2}+4},\ \frac{4v}{u^{2}+v^{2}+4},\ \frac{2(u^{2}+v^{2})}{u^{2}+v^{2}+4}\right)
$$
*Verification:* Direct substitution shows $\pi^{-1}(u,v) \in S^{2}$

**b.** Use two Coordinate Charts:
1. North pole projection: $\pi_N: S^{2}\setminus\{N\}\rightarrow \mathbb{R}^{2}$
2. South pole projection: $\pi_S: S^{2}\setminus\{S\}\rightarrow \mathbb{R}^{2}$ where $S=(0,0,0)$

 Then $\pi_N$ covers all points except north pole, $\pi_S$ covers all points except south pole, thus  union covers entire sphere: $S^{2} = (S^{2}\setminus\{N\}) \cup (S^{2}\setminus\{S\})$.
___

>[!problem] Problem 6
>Let $S^{2}=\left\{(x,y,z)\in R^{3};x^{2}+y^{2}+z^{2}=1\right\}$ be the unit sphere and let $A:S^{2}\longrightarrow S^{2}$ be the (antipodal) map $A(x,y,z)=(-x,-y,-z)$. Prove that $A$ is a diffeomorphism.

**Proof:** 
Bijectivity:
- Injective: $A(p) = A(q) \Rightarrow (-x_p,-y_p,-z_p) = (-x_q,-y_q,-z_q) \Rightarrow p = q$
- Surjective: $\forall q \in S^2$, take $p = -q$, then $A(p) = q$

Differentiability (Local Coordinates):
Use stereographic projection $\pi: S^2\setminus\{N\} \to \mathbb{R}^2$, then local expression: $A_{\text{loc}} = \pi \circ A \circ \pi^{-1}$

Compute:
- $\pi^{-1}(u,v) = \left(\frac{2u}{D}, \frac{2v}{D}, \frac{u^2+v^2-1}{D}\right)$, $D = u^2+v^2+1$
- Apply $A$: multiply by $-1$
- Apply $\pi$: $A_{\text{loc}}(u,v) = \left(-\frac{u}{u^2+v^2}, -\frac{v}{u^2+v^2}\right)$
This is a rational function, thus smooth.

Inverse Differentiability:
$A^{-1} = A$ since $A \circ A = \text{id}$, and $A$ is differentiable.

Therefore, $A$ is a diffeomorphism.
___

>[!problem] Problem 7
>Show that the paraboloid $z = x^{2} + y^{2}$ is diffeomorphic to a plane.

**Proof:**
Define $F: P \to \mathbb{R}^2$ by projection:
$$F(x,y,z) = (x, y)$$
Inverse $F^{-1}: \mathbb{R}^2 \to P$:
$$F^{-1}(u,v) = (u, v, u^2 + v^2)$$
- **Injective**: $F(p_1) = F(p_2) \Rightarrow (x_1,y_1) = (x_2,y_2)$
  Since $z_i = x_i^2 + y_i^2$, $p_1 = p_2$
- **Surjective**: $\forall (u,v) \in \mathbb{R}^2$, $F(u,v,u^2+v^2) = (u,v)$

Smoothness:
- $F$ is linear projection, thus smooth.
- $F^{-1}$ has polynomial components, thus smooth.

Global parametrization $\phi(u,v) = (u,v,u^2+v^2)$:
- $F \circ \phi(u,v) = (u,v)$ (identity)
- $\phi^{-1} \circ F^{-1}(u,v) = (u,v)$ (identity)

Therefore $F$ and $F^{-1}$ are smooth bijections, thus diffeomorphism.
___

>[!problem] Problem 8
>Let $S\subset \mathbb{R}^{3}$ be a regular surface, and let $d: S\longrightarrow \mathbb{R}$ be given by $d(p)=|p-p_{0}|$, where $p\in S,\ p_{0}\in \mathbb{R}^{3},\ p_{0}\notin S$; that is, $d$ is the distance from $p$ to a fixed point $p_{0}$ not in $S$. Prove that $d$ is differentiable.

**Proof:**
Define $D: \mathbb{R}^3 \to \mathbb{R}$ as $D(q) = |q-p_0|$.

$D$ is differentiable on $\mathbb{R}^3 \setminus \{p_0\}$ (composition of polynomials and square root). Since $p_0 \notin S$, $D > 0$ on $S$.

$d = D|_S$ is restriction of differentiable function to regular surface, thus $d$ is differentiable.
___

>[!problem] Problem 9
>Prove that the rotations of a surface of revolution $S$ about its axis are diffeomorphisms of $S$.

**Proof:** Let $S$ be generated by rotating profile curve $(f(v), 0, g(v))$ about $z$-axis:
$$\mathbf{x}(u,v) = (f(v)\cos u, f(v)\sin u, g(v))$$
Rotation by angle $\theta$ about $z$-axis:
$$R_\theta(x,y,z) = (x\cos\theta - y\sin\theta, x\sin\theta + y\cos\theta, z)$$
On $S$, $R_\theta$ acts as:
$$R_\theta(\mathbf{x}(u,v)) = (f(v)\cos(u+\theta), f(v)\sin(u+\theta), g(v)) = \mathbf{x}(u+\theta, v)$$
Check $R_\theta$:
- **Bijective**: $R_\theta$ and $R_{-\theta}$ are mutual inverses
- **Smooth**: Component functions are trigonometric polynomials
- **Regular**: Jacobian has full rank (preserves geometry)

Therefore, $R_\theta: S \to S$ is a diffeomorphism for all $\theta$.
___

>[!problem] Problem 10
>Let $\mathbb{R}^{2}=\{(x, y, z)\in \mathbb{R}^{3};z=-1\}$ be identified with the complex plane $\mathbb{C}$ by setting $(x,y,-1)=x+iy=\zeta\in\mathbb{C}$. Let $P:\mathbb{C}\to\mathbb{C}$ be the complex polynomial
>
>$$ P(\zeta)=a_{0}\zeta^{n}+a_{1}\zeta^{n-1}+\cdots+a_{n},\quad a_{0}\neq 0,a_{i}\in\mathbb{C}, i=1,\ldots, n. $$
>
>Denote by $\pi_{N}$ the stereographic projection of $S^{2}=\{(x, y,z)\in \mathbb{R}^{3};x^{2}+y^{2}+z^{2}=1\}$ from the north pole $N=(0,0,1)$ onto $\mathbb{R}^{2}$. Prove that the map $F\colon S^{2}\to S^{2}$ given by
>
>$$ \begin{align*}
F(p)&=\pi_{N}^{-1}\circ P\circ\pi_{N}(p),\quad\text{if }p\in S^{2}-\{N\},\\
F(N)&=N
\end{align*} $$
>
>is differentiable.

**Proof:**
First, we know about stereographic projection from Problem 5 that:
- $\pi_N: S^2\setminus\{N\} \to \mathbb{C}$ is diffeomorphism
- $\pi_N^{-1}: \mathbb{C} \to S^2\setminus\{N\}$ is diffeomorphism

$P(\zeta)$ is polynomial, thus smooth.

For $p \neq N$:
- $\pi_N$ differentiable (stereographic projection)
- $P$ smooth (polynomial)
- $\pi_N^{-1}$ differentiable
Composition: $F = \pi_N^{-1} \circ P \circ \pi_N$ is differentiable on $S^2\setminus\{N\}$

For $p = N$:
Use south pole stereographic projection $\pi_S$ as alternative chart:
$$F = \pi_S^{-1} \circ (\pi_S \circ \pi_N^{-1}) \circ P \circ (\pi_N \circ \pi_S^{-1}) \circ \pi_S$$
$\pi_S \circ \pi_N^{-1}$ is Möbius transformation $\zeta \mapsto 1/\zeta$.
Rational function $\circ$ Polynomial $\circ$ Rational function = Rational function $\Rightarrow$ $F$ differentiable at $N$.

In conclusion, $F$ is differentiable on entire $S^2$
___

>[!problem] Problem 11
>Determine the tangent planes of $x^{2}+y^{2}-z^{2}=1$ at the points $(x,y,0)$ and show that they are all parallel to the $z$ axis.

**Proof:**
Surface: $f(x,y,z) = x^2 + y^2 - z^2 - 1 = 0$.
At $(x,y,0)$: $\nabla f = (2x, 2y, 0)$, thus normal vector: $\mathbf{n} = (x, y, 0)$.

At $(x_0, y_0, 0)$ where $x_0^2 + y_0^2 = 1$, we have tangent plane: $x_0x + y_0y = 1$.

Normal vector is perpendicular to $z$ axis, so the planes are all parallel to the $z$ axis.
___

>[!problem] Problem 12
>Show that the tangent planes of a surface given by $z = x\,f\!\left(\dfrac{y}{x}\right)$, $x \neq 0$, where $f$ is a differentiable function, all pass through the origin $(0, 0, 0)$.

**Proof:**
Let $u = \dfrac{y}{x}$, then $y = xu$. Then surface equation: $z = x f(u)$

Let $F(x,y,z) = z - x f(y/x) = 0$, then
$\frac{\partial F}{\partial x} = -f(u) + \frac{y}{x} f'(u)$
$\frac{\partial F}{\partial y} = -f'(u)$
$\frac{\partial F}{\partial z} = 1$
Thus normal vector: $\mathbf{n} = \left(-f(u) + u f'(u),\ -f'(u),\ 1\right)$.

At point $p_0 = (x_0, y_0, z_0)$ with $u_0 = y_0/x_0$, $z_0 = x_0 f(u_0)$:
Tangent plane: $\mathbf{n} \cdot (p - p_0) = 0\Rightarrow$
$\left[-f(u_0) + u_0 f'(u_0)\right](x - x_0) - f'(u_0)(y - y_0) + (z - z_0) = 0$

Substitute $(0,0,0)$ into plane equation:

LHS = $\left[-f(u_0) + u_0 f'(u_0)\right](-x_0) - f'(u_0)(-y_0) + (-z_0)$
= $x_0 f(u_0) - x_0 u_0 f'(u_0) + y_0 f'(u_0) - z_0$
Since $y_0 = x_0 u_0$ and $z_0 = x_0 f(u_0)$:
LHS = $x_0 f(u_0) - x_0 u_0 f'(u_0) + x_0 u_0 f'(u_0) - x_0 f(u_0) = 0$

Therefore, all tangent planes of $z = x f(y/x)$ contain origin $(0,0,0)$.
___

>[!problem] Problem 13
>Let $\alpha:I\longrightarrow R^{3}$ be a regular parametrized curve with nonzero curvature everywhere and arc length as parameter. Let
>
>$$ \mathbf{x}(s, v)=\alpha(s)+r(n(s)\cos v+b(s)\sin v),\quad r=\text{const.}\neq 0,s\in I, $$
>
>be a parametrized surface (the tube of radius r around $\alpha$), where n is the normal vector and b is the binormal vector of $\alpha$. Show that, when $x$ is regular, its unit normal vector is
>
>$$ N(s,v)=-(n(s)\cos v+b(s)\sin v). $$

**Proof:**
Tangent vectors at $s$-direction: $\mathbf{x}_s = t + r(n'\cos v + b'\sin v)$.
Using Frenet formulas:
- $n' = -\kappa t + \tau b$
- $b' = -\tau n$
Then $\mathbf{x}_s = (1 - r\kappa\cos v)t - r\tau\sin v\ n + r\tau\cos v\ b$
Tangent vectors at $s$-direction: $\mathbf{x}_v = r(-n\sin v + b\cos v)$.
Compute cross product: $\mathbf{x}_s \times \mathbf{x}_v = -r(1 - r\kappa\cos v)(n\cos v + b\sin v)$.
($t$-components vanish due to symmetry.)

Magnitude: $|\mathbf{x}_s \times \mathbf{x}_v| = |r(1 - r\kappa\cos v)|$.
Therefore, $N(s,v) = \dfrac{\mathbf{x}_s \times \mathbf{x}_v}{|\mathbf{x}_s \times \mathbf{x}_v|} = -(n(s)\cos v+b(s)\sin v)$.
___

>[!problem] Problem 14
>Show that each of the equations $(a, b, c \neq 0)$ 
>
>$$x^{2}+y^{2}+z^{2}=ax,$$
>$$x^{2}+y^{2}+z^{2}=by,$$
>$$x^{2}+y^{2}+z^{2}=cz$$
>
>define a regular surface and that they all intersect orthogonally.

**Proof:**
The first equation:
$$
x^{2}+y^{2}+z^{2}=ax \iff (x-a/2)^{2}+y^{2}+z^{2}=a^{2}/4
$$
This is a sphere centered at $C_1=(a/2,0,0)$ with radius $R_1=|a|/2>0$.

Similarly, the second equation defines a sphere centered at $C_2=(0,b/2,0)$ with radius $R_2=|b|/2$, and the third equation defines a sphere centered at $C_3=(0,0,c/2)$ with radius $R_3=|c|/2$.

All are spheres with positive radii, thus they are all regular surfaces.

All spheres pass through origin $(0,0,0)$. so all three spheres intersect.

Two spheres intersect orthogonally at a point if their tangent planes at that point are perpendicular $\iff$ radius vectors at intersection point are perpendicular.

Equivalently: For spheres intersecting at origin $O=(0,0,0)$, orthogonality condition is:
$$
|C_1C_2|^2 = R_1^2 + R_2^2
$$
where $C_i$ are centers, $R_i$ are radii.

Verify for spheres 1 and 2:
- $|C_1C_2|^2 = (a/2)^2 + (b/2)^2 = (a^2+b^2)/4$
- $R_1^2 + R_2^2 = (a^2/4) + (b^2/4) = (a^2+b^2)/4$

Similarly the other pairs also holds $|C_1C_2|^2 = R_1^2 + R_2^2$, thus they all intersect orthogonally.
___

>[!problem] Problem 15
>Let $w$ be a tangent vector to a regular surface $S$ at a point $p \in S$ and let $\mathbf{x}(u, v)$ and $\bar{\mathbf{x}}(\bar{u}, \bar{v})$ be two parametrizations at $p$. Suppose that the expressions of $w$ in the bases associated to $\mathbf{x}(u, v)$ and $\bar{\mathbf{x}}(\bar{u}, \bar{v})$ are
>
>$$ w = \alpha_{1} \mathbf{x}_{u} + \alpha_{2} \mathbf{x}_{v} $$
>
>and
>
>$$ w = \beta_{1} \bar{\mathbf{x}}_{\bar{u}} + \beta_{2} \bar{\mathbf{x}}_{\bar{v}}. $$
>
>Show that the coordinates of $w$ are related by
>
>$$ 
>\begin{aligned}
>\beta_{1} &= \alpha_{1} \frac{\partial \bar{u}}{\partial u} + \alpha_{2} \frac{\partial \bar{u}}{\partial v} \\[4pt]
>\beta_{2} &= \alpha_{1} \frac{\partial \bar{v}}{\partial u} + \alpha_{2} \frac{\partial \bar{v}}{\partial v}
>\end{aligned}
>$$
>
>where $\bar{u} = \bar{u}(u, v)$ and $\bar{v} = \bar{v}(u, v)$ are the expressions of the change of coordinates.

**Proof:**
From $\bar{\mathbf{x}}(\bar{u}(u,v), \bar{v}(u,v)) = \mathbf{x}(u,v)$:
$$
\begin{aligned}
\mathbf{x}_u &= \bar{\mathbf{x}}_{\bar{u}} \frac{\partial \bar{u}}{\partial u} + \bar{\mathbf{x}}_{\bar{v}} \frac{\partial \bar{v}}{\partial u} \\
\mathbf{x}_v &= \bar{\mathbf{x}}_{\bar{u}} \frac{\partial \bar{u}}{\partial v} + \bar{\mathbf{x}}_{\bar{v}} \frac{\partial \bar{v}}{\partial v}
\end{aligned}
$$
Substitute into $w = \alpha_1 \mathbf{x}_u + \alpha_2 \mathbf{x}_v$:

$$
w = \left(\alpha_1 \frac{\partial \bar{u}}{\partial u} + \alpha_2 \frac{\partial \bar{u}}{\partial v}\right) \bar{\mathbf{x}}_{\bar{u}} + \left(\alpha_1 \frac{\partial \bar{v}}{\partial u} + \alpha_2 \frac{\partial \bar{v}}{\partial v}\right) \bar{\mathbf{x}}_{\bar{v}}
$$
Since $w = \beta_1 \bar{\mathbf{x}}_{\bar{u}} + \beta_2 \bar{\mathbf{x}}_{\bar{v}}$ and basis is linearly independent:
$$
\begin{aligned}
\beta_1 &= \alpha_1 \frac{\partial \bar{u}}{\partial u} + \alpha_2 \frac{\partial \bar{u}}{\partial v} \\
\beta_2 &= \alpha_1 \frac{\partial \bar{v}}{\partial u} + \alpha_2 \frac{\partial \bar{v}}{\partial v}
\end{aligned}
$$
Therefore, the conclusion holds.



