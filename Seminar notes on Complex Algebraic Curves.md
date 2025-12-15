<center>
ZIXUAN TENG
</center>
# Chapter 4: Topological Properties

As a subset of the projective plane $P_2$, a complex projective curve has a natural topology, which means that it makes sense to talk about concepts such as continuous functions on $C$. In this chapter we shall investigate nonsingular complex projective curves from the topological point of view.

---

A nonsingular projective curve in $P^2$ is topologically a sphere with $g$ handles (see Figure 4.1 for a picture when $g=3$). This number $g$ is called the genus of the curve. Our aim is to show that it is related to the degree $d$ of the curve by the *degree-genus formula*:

$$
g = \frac{1}{2}(d-1)(d-2)
$$
![Figure 4.1: A sphere with three handles](CAC/Figures/Figure4.1.jpg)

*Figure 4.1: A sphere with three handles*

It is also possible to describe the topology of singular projective curves in $P_2$, although as might be expected the description is more complicated. It is enough to consider irreducible curves since any projective curve in $P_2$ is the union of finitely many irreducible curves meeting at finitely many points. An irreducible projective curve is the result of making a finite number of identifications of points on a sphere with $g$ handles (see Figure 4.2).

![Figure 4.2: A singular curve](CAC/Figures/Figure4.2.jpg)
*Figure 4.2: A singular curve*

The *degree-genus formula* can be generalized to singular curves. To each singular point $p_i$ there can be assigned a positive integer $\delta(p_i)$ such that

$$
g = \frac{1}{2}(d-1)(d-2) - \sum_{j=1}^r \delta(p_j)
$$

(called Noether's formula).

The proof of these facts about singular curves will be left to Chapter 7. The aim of this chapter is to prove the *degree-genus formula* for nonsingular projective curves.

---

# 4.1 Definition of Genus

Here are three equivalent ways in $P^2$ to define genus.

---

>[!notes] Definition 4.1.1 (Topological Definition)
>View $C$ as a compact Riemann surface. Then the genus is defined as
>
>$$
>g(C) := \frac{1}{2} \dim_{\mathbb{R}} H_1(C, \mathbb{R})
>$$
>
>- $H_1(C, \mathbb{R})$ is the first homology group of .  

---

>[!notes] Definition 4.1.2 (Analytic / Holomorphic Definition)
>From the complex analytic viewpoint, treating $C$ as a Riemann surface:
>
>$$
>g(C) := \dim_{\mathbb{C}} H^0(C, \Omega_C^1)
>$$
>
>- $\Omega_C^1$ is the sheaf of holomorphic 1-forms on $C$.  
>- $H^0(C, \Omega_C^1)$ is the space of global holomorphic 1-forms.  
>- The genus equals the complex dimension of this space.

---

>[!notes] Definition 4.1.3 (Algebraic-Geometric Definition)
>In algebraic geometry, define:
>
>$$
>g(C) := \dim_{\mathbb{C}} H^1(C, \mathcal{O}_C)
>$$
>
>- $\mathcal{O}_C$ is the structure sheaf of $C$.  
>- $H^1(C, \mathcal{O}_C)$ is the first cohomology group of the structure sheaf.  
>- This definition is equivalent to the analytic one via Serre duality.

---

>[!Question] 
>Why are these three definitions equivalent on $P^2$?
>
>**Hint:**  
>- $(1) \Leftrightarrow (2)$ via Hodge / Dolbeault decomposition  
>- $(2) \Leftrightarrow (3)$ via Serre duality / Dolbeault

---

The first method is intuitively appealing but it lies beyond the scope of this book to carry it through in detail.
## 4.2 The first method of proof

 The first step is to consider a (singular) complex projective curve $C_{0}$ which is a union of d projective lines in $P_{2}$, in "general position" in the sense that no point of $P_{2}$ lies on more than two of the lines. Thus there are exactly $\frac{1}{2} d(d-1)$ points of intersection of these lines, and these are the singular points of $C_{0}$.

---

>[!notes] Lemma 4.2
>A complex projective line L in $P_{2}$ is homeomorphic to the *two-dimensional unit sphere*
>
>$$
>S^{2}=\{(u,v,w)\in \mathbb{R}:u^2+v^2+w^2=1\}.
>$$

**Proof.** By applying a projective transformation (which is a homeomorphism be lemma 2.20) we may assume that $L$ is the line defined be $z=0$. Now define $$\phi:S^2\to L$$ by$$\phi(u,v,w)=\begin{cases}
[u+iv,1-w,0] & (u,v,w)\ne(0,0,1), \\[4pt]
[1,0,0], & (u,v,w)=(0,0,1).
\end{cases}$$ It is not difficult to check using the definition of homogeneous coordinates that $\phi$ is a bijection with inverse given by$$\phi^{-1}[x,y,0]=(\frac{2\operatorname{Re}(x\bar{y})}{\lvert x\rvert^2+\lvert y\rvert^2},\frac{2\operatorname{Im}(x\bar{y})}{\lvert x\rvert^2+\lvert y\rvert^2},\frac{\lvert x\rvert^2-\lvert y\rvert^2}{\lvert x\rvert^2+\lvert y\rvert^2}).$$Check that $\phi$ and $\phi^{-1}$ are continuous. $\square$  

---
This lemma shows that topologically our singular curve $C_{0}$ is homeomorphic to a union of d spheres meeting in $\frac{1}{2} d(d-1)$ points.

Note that:
- $C_p[x,y,z]$ ={homogeneous of polynomials of degree d in $x,y,z$ with complex coefficients}
- $C_p^{nonsing}[x,y,z]$ ={$C$ nonsingular: $C\in C_p[x,y,z]$}
- $C_p^{sing}[x,y,z]$ ={$C$ singular: $C\in C_p[x,y,z]$}

---
>[!notes] Lemma 4.3(Euler’s Theorem on Homogeneous Functions)
>Let
>$$
>f(x_1, x_2, \dots, x_n)
>$$
>be a **homogeneous polynomial (or function)** of degree $d$.  
>
>That is, for every scalar $\lambda \in \mathbb{C}$ (or $\mathbb{R}$),
>$$
>f(\lambda x_1, \lambda x_2, \dots, \lambda x_n) = \lambda^d f(x_1, x_2, \dots, x_n).
>$$
>
>Then the following **Euler’s equation** holds:
>
>$$
>x_1 \frac{\partial f}{\partial x_1} + x_2 \frac{\partial f}{\partial x_2} + \cdots + x_n \frac{\partial f}{\partial x_n} = d\, f(x_1, x_2, \dots, x_n).
>$$

**Proof.** Since $f$ is homogeneous of degree $d$, we have

$$
f(\lambda x_1, \lambda x_2, \dots, \lambda x_n) = \lambda^d f(x_1, x_2, \dots, x_n)
$$

for all $\lambda$.

**Step 1. Differentiate both sides with respect to $\lambda$**

Differentiate the above identity with respect to $\lambda$:

$$
\frac{d}{d\lambda} f(\lambda x_1, \lambda x_2, \dots, \lambda x_n)
= \frac{d}{d\lambda} \big( \lambda^d f(x_1, x_2, \dots, x_n) \big).
$$


**Step 2. Apply the chain rule to the left-hand side**

By the multivariable chain rule:

$$
\frac{d}{d\lambda} f(\lambda x_1, \dots, \lambda x_n)
= \sum_{i=1}^{n} \frac{\partial f}{\partial x_i}(\lambda x_1, \dots, \lambda x_n) \cdot \frac{d(\lambda x_i)}{d\lambda}
= \sum_{i=1}^{n} x_i \frac{\partial f}{\partial x_i}(\lambda x_1, \dots, \lambda x_n).
$$


**Step 3. Differentiate the right-hand side**

$$
\frac{d}{d\lambda} \big( \lambda^d f(x_1, \dots, x_n) \big)
= d \lambda^{d-1} f(x_1, \dots, x_n).
$$


**Step 4. Evaluate at $\lambda = 1$**

Setting $\lambda = 1$, we obtain

$$
\sum_{i=1}^{n} x_i \frac{\partial f}{\partial x_i}(x_1, \dots, x_n)
= d\, f(x_1, \dots, x_n).
$$


**Hence proved.**

$$
\boxed{ \displaystyle \sum_{i=1}^n x_i \frac{\partial f}{\partial x_i} = d f }
$$
---
>[!notes] Lemma 4.4
>$$
>\dim_{C}C_p[x,y,z]=\frac{1}{2}(d+1)(d+2):=N_d,
>$$
>$$\dim_C C_p^{sing}[x,y,z]=N_d-1.
>$$ 

**Informal Proof (Sketch)** 
Define the *incidence variety* $$I=\{(p,F)\in P^2\times C_d[x,y,z]:p\text{ is a singular point of }F\}$$and define $$Ip=\{F\in C_d[x,y,z]:F(p)=0,\nabla F(p)=0\}$$By [[#**Lemma 4.3(Euler’s Theorem on Homogeneous Functions)**|Lemma 4.3]],
$$
xF_x+yF_y+zF=dF.
$$
So
$$
\dim Ip=N_d-3.
$$
 Then we have
 $$
 \dim I=dim I_p+dimP^2=N_d-3+2=Nd-1.\square
 $$
 
---

>[!tip] Remark 4.5
>Take$$F(x,y,z)=y^2z^{(d-2)}-x^d,$$Then F only has one singular point at $[x,y,z]=[0,0,1]$.

---
By [[#**Lemma 4.4|Lemma 4.4]], the subset $C_{d}^{\text{nonsing}}[x, y, z]$ is dense in  $C_{d}[x, y, z]$ . 
It is in fact always possible to perturb the coefficients of the polynomial defining $C$ by an arbitrarily small amount to get a nonsingular projective curve $C^{'}$. 
Then take $C=C_0$.  It turns out that what happens on a topological level when such a perturbation takes place is that the singular points of intersection of the projective lines making up $C_{0}$ become very thin smooth "necks" or handles joining the projective lines (cf. Figure 4.3). Precisely $d-1$ of these handles are used to join the $d$ spheres together to form one sphere (topologically). Thus the nonsingular perturbation $C_{1}$ of $C_{0}$ is topologically equivalent to a sphere with $$\frac{1}{2}d(d-1)-(d-1)=\frac{1}{2}(d-1)(d-2)$$
handles. Thus we have at least one nonsingular curve with the right topology.
![Figure 4.3: A deformation of a singular curve](CAC/Figures/Figure4.3.jpg)
*Figure 4.3: A deformation of a singular curve*

The second step is to show that that if the coefficients of the polynomial defining a nonsingular curve are perturbed by a sufficiently small amount then the topology of the curve remains unchanged.

The third step is to show that the space $C_{d}^{\text{nonsing}}[x, y, z]$ of homogeneous polynomials of degree $d$ in $x,y,z$ defining nonsingular projective curves is path-connected. For $P(x,y,z),Q(x,y,z)\in C_{d}^{\text{nonsing}}[x, y, z]$  
Take$$P_t(x,y,z)=(1-t)P(x,y,z)+tQ(x,y,z)$$to get a path from $P(x, y, z)$ to $Q(x, y, z)$ in the space $C_{d}[x, y, z]$. Since such a path has real dimension one and the complement of $C_{d}^{\text{nonsing}}[x, y, z]$ in $C_{d}[x, y, z]$ has real codimension(By [[#**Lemma 4.4|Lemma 4.4]]) two we can always shift the path very slightly to ensure that it misses the complement of $C_{d}^{\text{nonsing}}[x, y, z]$ and hence defines a path in $C_{d}^{\text{nonsing}}[x, y, z]$ as required.

Now we can put these three steps together to obtain the result we want. Let C be any nonsingular projective curve of degree d in $P_{2}$. By the first step there exists a nonsingular projective curve $C_{1}$ of degree $d$ in $P_{2}$ which is topologically a sphere with $$g=\frac{1}{2}(d-1)(d-2)$$handles. By the third step there is a path$$t\mapsto C_t, t\in[0,1]$$from C to $C_{1}$ in the space of nonsingular projective curves of degree d in $P_{2}$. By the second step, given $t\in[0,1]$ there exists $\varepsilon(t)>0$ such that if $s\in[0,1]$ and $|t-s|<\varepsilon(t)$ then $C_{s}$ is homeomorphic to $C_{t}$. It is now easy to deduce that $C_{s}$ and $C_{t}$ are topologically equivalent for all $s, t\in[0,1]$. In particular C is homeomorphic to $C_{1}$ and hence is topologically a sphere with $$g=\frac{1}{2}(d-1)(d-2)$$handles. $\square$ 

---

To have the second method of proof, we first need to learn two things, **branched covers of $P_1$** and **Triangulation of a curve $C$**

#  **4.3 Branched covers of $P_1$** 

Let C be a nonsingular projective curve in $P_{2}$ defined by a homogeneous polynomial $P(x, y, z)$ of degree $d>1$. By applying a suitable projective transformation we may assume that $[0,1,0]\notin C$. Then we have a well-defined map $\phi: C\rightarrow P_{1}$ given by$$\phi[x,y,z]=[x,z]$$

---
>[!notes] Definition 4.3
The ramification index $\nu_{\phi}[a, b, c]$ of $\phi$ at a point $[a, b, c]\in C$ is the order of the zero of the polynomial $P(a, y, c)$ in y at $y=b$. The point $[a, b, c]$ is called a ramification point of $\phi$ if $\nu_{\phi}[a, b, c]>1$.

---
>[!tip] Remark 4.4
>(i) $\nu_{\phi}[a, b, c]>0$ if and only if $[a, b, c]\in C$.
>(ii) $\nu_{\phi}[a, b, c]>1$ if and only if
>$$
>P(a,b,c)=0=\frac{\partial P}{\partial y}(a,b,c)
>$$
>i.e. if and only if $[a, b, c]\in C$ and the tangent line to C at $[a, b, c]$ contains the point $[0,1,0]$.
>(iii) $\nu_{\phi}[a, b, c]>2$ if and only if
>$$
>P(a,b,c)=0=\frac{\partial P}{\partial y}(a,b,c)=\frac{\partial^2P}{\partial y^2}(a,b,c)
>$$

This happens if and only if $[a, b, c]$ is a point of *inflection* on C and the tangent line to C at $[a, b, c]$ contains the point $[0,1,0]$. To prove this, note that $[a, b, c]\neq[0,1,0]$ so $a\neq 0$ or $c\neq 0$. Let us assume that $c\neq 0$; the case $a\neq 0$ is similar. Suppose$$P(a,b,c,)=0=\frac{\partial P}{\partial y}(a,b,c)$$then by lemma 3.30 we have$$
H_P(a, b, c) = \frac{(d-1)^2}{c^2} \det \begin{pmatrix}
P_{xx} & P_{xy} & P_x \\
P_{yx} & P_{yy} & 0 \\
P_x & 0 & 0
\end{pmatrix}$$$$= -\frac{(d-1)^2}{c^2} (P_x)^2 P_{yy}
$$where the partial derivatives are evaluated at $(a, b, c)$. By Euler's relation (lemma 2.32) if$$\frac{\partial P}{\partial x}(a,b,c)=0$$then as $c\neq 0$ and $\frac{\partial P}{\partial y}(a, b, c)=0$ the point $[a, b, c]\in C$ would be singular, which contradicts the assumption that C is a nonsingular curve. Hence $\mathcal{H}_{P}(a, b, c)=0$ if and only if$$\frac{\partial^2 P}{\partial x^2}(a,b,c)=0$$as required.

---

Here we will an important example to understand the second methods.

---

>[!example] Example 4.3
>Let us consider the nonsingular curve $C$ defined by
>$$
>x^3+y^3+z^3=3yz^2.
>$$

Putting $z=1$ we obtain the equation$$x^3+y^3+1=3y$$which we can regard as defining y as a multivalued function of x; in fact$$y=(\frac{-(x^3+1)+\sqrt{x^6+2x^3-3}}{2})^{\frac{1}{3}}+(\frac{-(x^3+1)-\sqrt{x^6+2x^3-3}}{2})^{\frac{1}{3}}$$for appropriate choices of the cube roots (see\[Stewart 73\] pp. 161-163). Note that$$x^6+2x^3-3=0$$if and only if $x^{3}$ equals 1 or -3; i.e. x equals $1,\omega,\bar{\omega},-\sqrt[3]{3},-\omega\sqrt[3]{3}$ or $-\bar{\omega}\sqrt[3]{3}$ where $\omega=e^{\frac{2\pi i}{3}}$. To any value of x in$$C-\{1,\omega,\bar{\omega},-\sqrt[3]{3},-\omega\sqrt[3]{3},-\bar{\omega}\sqrt[3]{3}\}$$there correspond exactly three values of y, and locally these define three holomorphic functions of x called "branches" of the multivalued function $y(x)$. When x travels around any of the points$$\{1,\omega,\bar{\omega},-\sqrt[3]{3},-\omega\sqrt[3]{3},-\bar{\omega}\sqrt[3]{3}\}$$the value of y changes from one branch of the multivalued function to another. If we cut the complex plane C along the straight line segment $\left[1,-\omega\sqrt[3]{3}\right]$ from 1 to $-\omega\sqrt[3]{3}$ and along the straight line segments $\left[-\omega\sqrt[3]{3},\bar{\omega}\right],[\bar{\omega},-\sqrt[3]{3}],[-\sqrt[3]{3},\omega]$ and $\left[\omega,-\bar{\omega}\sqrt[3]{3}\right]$ (see Figure4.4) then we find that there are three (single-valued) holomorphic functions $f_{1}, f_{2}, f_{3}$ defined on the cut plane $D$ satisfying$$f_j(x)^3+x^3+1=3f_j(x)$$for $j=1,2,3$, and all $x\in D$.
![Figure 4.4: The cut plane $D$](CAC/Figures/Figure4.4.jpg)

*Figure 4.4: The cut plane $D$*
Therefore the subset$$\{[x,y,1]\in C:x\in D\}=\bigcup_{j=1}^3\{[x,y,1]\in \mathbf{P}_2:x\in D,y=f_j(x)\}$$of C is the disjoint union of three copies of the cut plane D. If we add in the three points at infinity this means that we can construct C topologically by taking three copies of $D\cup\{\infty\}$ and gluing the edges of the cuts together appropriately, corresponding to the way the multivalued function jumps from one branch $f_{j}$ to another as y crosses the cuts. 
![Figure 4.5: Three discs to be glued together](CAC/Figures/Figure4.5.jpg)*Figure 4.5: Three discs to be glued together*
![Figure 4.6: Annulus formed from second disc](CAC/Figures/Figure4.6.jpg)*Figure 4.6: Annulus formed from second disc*

Note that each copy of $D\cup\{\infty\}$ is topologically a disc, and its boundary is made up of ten line segments. One can check that the boundaries should be identified according to [[Figure4.5.jpg]], in which $a_{j}, b_{j}, c_{j}, d_{j}, e_{j}$ refer to cuts along $\left[1,-\omega\sqrt[3]{3}\right],[-\omega\sqrt[3]{3},\bar{\omega}],[\bar{\omega},-\sqrt[3]{3}],[-\sqrt[3]{3},\omega]$ and $\left[\omega,-\bar{\omega}\sqrt[3]{3}\right]$ respectively. The two copies of $c_{2}$ in the second disc can be identified to give an annulus whose boundary is given by figure 4.6. The two pairs $b_{1} c_{1}$ and $c_{3} d_{3}$ occurring in the first and third discs in [[Figure4.5.jpg]] can be identified to give another annulus whose boundary is given by [[Figure4.7.jpg]] . Note that the adjacent copies of $a_{3}$ and $e_{1}$ on this figure can be glued together and thus eliminated. Hence the two annuli given in figures [[Figure4.6.jpg]] and [[Figure4.7.jpg]] can be glued together to give a sphere with one handle, or torus ([[Figure4.8.jpg]]).

![Figure 4.7: Annulus formed from first and third discs](CAC/Figures/Figure4.7.jpg)*Figure 4.7: Annulus formed from first and third discs*
![Figure 4.8: Torus](CAC/Figures/Figure4.8.jpg)*Figure 4.8: Torus*

This agrees with the degree-genus formula when $d=3$ we get $g=1$.

---
>[!notes] Lemma 4.5
>The inverse image $\phi^{-1}([a, c])$ of any $[a, c]$ in $P_{1}$ under $\phi$ contains exactly
>$$
>d-\sum_{p\in\phi^{-1}({a,c})}(v_{\phi}(p)-1)
>$$
>points.
>
>In particular $\phi^{-1}([a, c])$ contains d points if and only if $\phi^{-1}([a, c])$ contains no ramification points of $\phi$.

 **Proof.** A point of C lies in $\phi^{-1}([a, c])$ i and only if it is of the form $[a, b, c]$ where $b\in C$ satisfies$$P(a,b,c)=0.$$By assumption $[0,1,0]\notin C$ so $P(0,1,0)\neq 0$. Hence we may assume that $P(0,1,0)=1$. Then $P(a, y, c)$ is a monic polynomial of degree d in y so$$P(a,b,c)=\Pi _{1\le i\le r}(y-b_i)^{m_i}$$where $b_{1},\ldots, b_{r}$ are distinct complex numbers and $m_{1},\ldots, m_{r}$ are positive integers such that$$m_1+…+m_r=d.$$Thus$$\phi^{-1}([a,c])=\{[a,b_i,c]:1\le i\le r\}$$and the ramification index of $\phi$ at $\left[a, b_{i}, c\right]$ is$$\nu_{\phi}[a,b_i,c]=m_i$$The result follows.$\square$

---
>[!notes] Definition 4.6
Let R be the set of ramification points of $\phi$. The image $\phi(R)$ of R under $\phi$ is called *the branch locus* of $\phi$, and $\phi: C\rightarrow P_{1}$ is called *a branched cove*r of $P_{1}$.

---
>[!notes] Lemma 4.7
(i) $\phi$ has at most $d(d-1)$ ramification points.  
(ii) If $\nu_\phi[a,b,c] \leq 2$ for all $[a,b,c] \in C$ then $C$ has exactly $d(d-1)$ ramification points.

**Proof.** Since $C$ is nonsingular it is irreducible (see corollary 3.10). By assumption $[0,1,0] \not\in C$ so the coefficient $P(0,1,0)$ of $y^d$ in $P(x,y,z)$ is nonzero. Thus the homogeneous polynomial  
$$
\frac{\partial P}{\partial y}(x,y,z)
$$  
is not identically zero and has degree $d-1$, so it cannot be divisible by $P(x,y,z)$. Hence the projective curve $D$ of degree $d-1$ defined by this polynomial has no component in common with $C$. Thus (i) follows from the weak form (theorem 3.9) of Bézout’s theorem, because the set $R$ of ramification points of $C$ is the intersection of $C$ and $D$.

Now suppose that  
$$
\nu_\phi[a,b,c] \leq 2
$$  
for all $[a,b,c] \in C$. By the corollary 3.25 to the strong form of Bézout’s theorem, in order to prove (ii) it suffices to show that if $[a,b,c]$ lies in $R = C \cap D$ then $[a,b,c]$ is a nonsingular point of $D$ and the tangent lines to $C$ and $D$ at $[a,b,c]$ are distinct. If not then $[a,b,c]$ satisfies  
$$
P(a,b,c) = 0 = P_y(a,b,c)
$$  
because it lies in $C$ and $D$, and the vector  
$$
(P_{xy}(a,b,c), P_{yy}(a,b,c), P_{zy}(a,b,c))
$$  
is either zero or a scalar multiple of the vector  
$$
(P_x(a,b,c), P_y(a,b,c), P_z(a,b,c)).
$$

This implies that  
$$
P(a,b,c) = 0 = P_y(a,b,c) = P_{yy}(a,b,c),
$$  
i.e.  
$$
\nu_\phi[a,b,c] > 2.
$$

This contradiction completes the proof. □

---
>[!notes] Lemma 4.8
>By applying a suitable projective transformation to $C$ we may assume that
>$$
>\nu_\phi[a,b,c] \leq 2
>$$
>for all $[a,b,c] \in C$.

**Proof.** By proposition 3.33 C has only a finite number (at most $3d(d-2)$) of points of inflection. Thus by applying a suitable projective transformation we may assume that $[0,1,0]$ does not lie on $C$ nor on any of the tangent lines to $C$ at its point of inflection. The result now follows remark 4.4(iii).$\square$

---