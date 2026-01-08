___

>[!problem] Problem 1
For over 2000 years it has been known that there are only five regular polyhedra, namely, the regular tetrahedron, cube, octahedron, dodecahedron, and icosahedron. Prove this by considering subdivisions of the sphere into $n$-gons ($n$ fixed) such that exactly $m$ edges meet at each vertex ($m$ fixed, $m,n \geq 3$). Use the fact that $\chi(S^2) = 2$.

**Proof:**
For a regular polyhedron with $F$ faces, $E$ edges, and $V$ vertices:
- Each face is an $n$-gon: $nF = 2E$
- Each vertex has degree $m$: $mV = 2E$
- Euler's formula for sphere: $V - E + F = 2$

Substitute:
$$\frac{2E}{m} - E + \frac{2E}{n} = 2$$

Simplify to:
$$E(2n + 2m - mn) = 2mn$$

Since $E > 0$, we get:
$$2n + 2m - mn > 0$$
Then:
$$(m - 2)(n - 2) < 4$$
Possible integer solutions with $m,n \geq 3$:
$(m,n) = (3,3),(3,4),(3,5),(4,3),(5,3)$

These correspond to the five Platonic solids:
- $(3,3)$: tetrahedron (4 faces)
- $(3,4)$: cube (6 faces)  
- $(4,3)$: octahedron (8 faces)
- $(3,5)$: dodecahedron (12 faces)
- $(5,3)$: icosahedron (20 faces)
___

>[!problem] Problem 2
The sides of a regular octagon are identified in pairs in such a way as to obtain a compact surface. Prove that the Euler characteristic of this surface is $\geq -2$.

**Proof:**
Let the surface be obtained by identifying pairs of sides of a regular octagon.

For the octagon:
- Vertices: $V\geq 1$
- Edges: $E=4$
- Faces: $F=1$
So Euler characteristic: $\chi = V - E + F = V - 4 + 1 = V - 3\geq -2$.
___

>[!problem] Problem 3
Prove that any surface (orientable or nonorientable) of Euler characteristic $\geq -2$ can be obtained by suitable identifying in pairs the sides of a regular octagon.

**Proof:**
We classify surfaces with $\chi\geq -2$ by Euler characteristic and orientability and check all of them:

Orientable surfaces:
- Sphere: $\chi = 2,(aa^{-1}bb^{-1}cc^{-1}dd^{-1})$
- Torus: $\chi = 0,aba^{-1}b^{-1}(cc^{-1}dd^{-1})$
- Double torus: $\chi = -2,aba^{-1}b^{-1}cdc^{-1}d^{-1}$

Non-orientable surfaces:
- Projective plane: $\chi = 1,aa(bb^{-1}cc^{-1}dd^{-1})$
- Klein bottle: $\chi = 0,aabb(cc^{-1}dd^{-1})$
- Connected sum of 3 projective planes: $\chi = -1,aabbcc(dd^{-1})$
- Connected sum of 4 projective planes: $\chi = -2,aabbccdd$

Therefore, any surface with $\chi \geq -2$ can be obtained from an octagon.
___

>[!problem] Problem 4
Let $S_1$ be a surface that is the connected sum of $m$ tori, $m \geq 1$, and let $S_2$ be a surface that is the connected sum of $n$ projective planes, $n \geq 1$. Suppose two holes are cut in each of these surfaces, and the two surfaces are then glued together along the boundaries of the holes. What surface is obtained by this process?

**Solution:**
Let $S$ be the surface obtained.
The operation in the problem statement increase the number of vertices and edges by $6$ and decreases the number of faces by $4$ (suppose the holes are triangle). Since $\chi(S_1) = 2 - 2m$ and $\chi(S_2) = 2 - n$, we have $\chi(S)=-2m-n$.

- If $n$ is odd, then $\chi(S)$ thus $S$ is non-orientable. So $S$ is the connected sum of $-2m-n-2$ projective planes.
- If $n$ is even, then the way of gluing (forward and backward) may change the orientability. Thus $S$ is either the connected sum of $-2m-n-2$ projective planes or $-m-n/2-1$ tori.
___

>[!problem] Problem 5
What surface is represented by a regular 10-gon with the edges identified in pairs according to the symbol $abcdec^{-1}da^{-1}b^{-1}e^{-1}$.

**Solution:**
Compute Euler characteristic
- Vertices: $V = 1$ (all vertices are glued together)
- Edges: $E = 5$
- Faces: $F = 1$
Thus $\chi = V - E + F = 1 - 5 + 1 = -3$

Therefore the surface is the connected sum of $5$ projective planes.
___

>[!problem] Problem 6
What surface is represented by a regular $2n$-gon with the edges identified in pairs according to the symbol $a_1a_2\cdots a_na_1^{-1}a_2^{-1}\cdots a_{n-1}^{-1}a_n$.

**Solution:**
The term $a_{n}$ forms a Mobius band, thus the surface is non-orientable.
Compute Euler characteristic
- Vertices: $V = 1$ (all vertices are glued together)
- Edges: $E = n$
- Faces: $F = 1$
Thus $\chi = V - E + F = 2-n$.

Therefore the surface is the connected sum of $n$ projective planes.
___

>[!problem] Problem 7
What surface is represented by a regular $2n$-gon with the edges identified in pairs according to the symbol $a_1a_2\cdots a_na_1^{-1}a_2^{-1}\cdots a_{n-1}^{-1}a_n^{-1}$.

**Solution:**
The surface is orientable since it contains no Mobius bands.
Compute Euler characteristic
- Vertices: $V = \dfrac{(-1)^n+3}{2}$
- Edges: $E = n$
- Faces: $F = 1$
Thus $\chi = V - E + F = \dfrac{(-1)^n+5}{2}-n$.

Therefore the surface is the connected sum of $\lfloor \frac{n}{2} \rfloor$ tori (specifically a sphere if $n=1$).
___

>[!problem] Problem 8
>Let $\alpha: I\longrightarrow R^{3}$ be a parametrized curve and let $v\in R^{3}$ be a fixed vector. Assume that $\alpha^{\prime}(t)$ is orthogonal to $v$ for all $t\in I$ and that $\alpha(0)$ is also orthogonal to $v$.
>
>Prove that $\alpha(t)$ is orthogonal to $v$ for all $t\in I$.

**Proof:**
Define $f(t) = \alpha(t) \cdot v$.  
Differentiate: $f'(t) = \alpha'(t) \cdot v = 0$ (given $\alpha'(t) \perp v$).  
So $f(t)$ is constant.
Since $f(0) = \alpha(0) \cdot v = 0$, we have $f(t) = 0$ for all $t$.  
Thus $\alpha(t) \cdot v = 0$ for all $t$, i.e., $\alpha(t) \perp v$.
___

>[!problem] Problem 9
>Let $\alpha: I\longrightarrow R^{3}$ be a parametrized curve, with $\alpha^{\prime}(t)\neq 0$ for all $t\in I$. Show that $\vert\alpha(t)\vert$ is a nonzero constant if and only if $\alpha(t)$ is orthogonal to $\alpha^{\prime}(t)$ for all $t\in I$.

**Proof:**
($\Rightarrow$) If $|\alpha(t)| = c \neq 0$ constant, then:  
$|\alpha(t)|^2 = \alpha(t) \cdot \alpha(t) = c^2$.  
Differentiate: $2\alpha(t) \cdot \alpha'(t) = 0\Rightarrow\alpha(t) \cdot \alpha'(t) = 0$.

($\Leftarrow$) If $\alpha(t) \cdot \alpha'(t) = 0$ for all $t$, then:  
$\frac{d}{dt}|\alpha(t)|^2 = 2\alpha(t) \cdot \alpha'(t) = 0\Rightarrow|\alpha(t)|^2$ constant.  
Since $\alpha'(t) \neq 0$, $\alpha(t)$ is not constant, so $|\alpha(t)| \neq 0$.  
Thus $|\alpha(t)|$ is a nonzero constant.
___

>[!problem] Problem 10
>Let ${\alpha}: (0, \pi) \to \mathbb{R}^2$ be given by  
>$$
>{\alpha}(t) = \left( \sin t,\ \cos t + \log \tan \frac{t}{2} \right),
>$$  
>where $t$ is the angle that the $y$-axis makes with the vector ${\alpha}(t)$. The trace of $\boldsymbol{\alpha}$ is called the *tractrix* . Show that:
>
>a. $\alpha$ is a differentiable parametrized curve, regular except at $t = \frac{\pi}{2}$.
>
>b. The length of the segment of the tangent to the tractrix between the point of tangency and the $y$-axis is constantly equal to $1$.  

**Proof:**
**a.**
Compute derivative:
$$\alpha'(t) = \left(\cos t, -\sin t + \frac{1}{\sin t}\right)=\left(\cos t, \frac{\cos^2t}{\sin t}\right)$$
$\alpha'(t) = 0$ only when $\cos t = 0$ and $\cos^2 t/\sin t = 0$, which occurs only when $t = \pi/2$, thus the curve is regular except at $t = \pi/2$.
**b.**
Tangent line at $\alpha(t)$:
$$y - \alpha_2(t) = \frac{\alpha_2'(t)}{\alpha_1'(t)}(x - \alpha_1(t))$$
Slope:
$$\frac{\alpha_2'(t)}{\alpha_1'(t)} = \frac{\cos^2 t/\sin t}{\cos t} =\tan t$$
Intersection with $y$-axis ($x=0$):
$$y = \alpha_2(t) + \tan t \cdot \alpha_1(t)= \alpha_2(t) +\sin t$$
Distance between $\alpha(t)$ and $(0,y)$:
$$\sqrt{(\alpha_1(t))^2 + (\alpha_2(t)-y)^2}=\sqrt{\cos^2 t + \sin^2 t} = 1$$Therefore tangent segment length is constantly $1$.
___

>[!problem] Problem 11
>Let $\alpha:(-1,+\infty)\rightarrow R^{2}$ be given by
>
>$$ \alpha(t)=\left(\frac{3at}{1+t^{3}},\frac{3at^{2}}{1+t^{3}}\right). $$
>
>Prove that:
>
>a. For $t=0$, $\alpha$ is tangent to the $x$ axis.
>
>b. As $t\rightarrow+\infty$, $\alpha(t)\rightarrow(0,0)$ and $\alpha^{\prime}(t)\rightarrow(0,0)$.
>
>c. Take the curve with the opposite orientation. Now, as $t\rightarrow-1$, the curve and its tangent approach the line $x+y+a=0$.

**Proof:**
**a.**
Compute derivative:
$$\alpha'(t)=\left(\frac{3a(1-2t^3)}{(1+t^3)^2},\frac{3at(2-t^3)}{(1+t^3)^2}\right)$$
At $t=0$: $\alpha(0)=(0,0),\alpha'(0)=(3a,0)$
Tangent vector is horizontal, so tangent to x-axis

**b.**
As $t\to+\infty$:
$$\alpha(t)=\left(\frac{3a}{t^2+o(t^2)},\frac{3a}{t+o(t)}\right)\to(0,0)$$
and
$$\alpha'(t)=\left(\frac{3a}{t^4+o(t^4)},\frac{6a}{t^4+o(t^4)}\right)\to(0,0)$$

**c.**
Tangent line at $\alpha(t)$:
$$y - \alpha_2(t) = \frac{\alpha_2'(t)}{\alpha_1'(t)}(x - \alpha_1(t))$$
Simplify to:
$$
t(t^3-2)x+(1-2t^3)y+3at^2=0
$$
As $t \to 1^{-}$:
$$
t(t^3-2)\to 3,1-2t^3\to 3,3at^2\to 3a.
$$
Thus the tangent line approaches to $x+y+a=0$.
___

>[!problem] Problem 12
>Let $\alpha(t)=(ae^{bt}\cos t,ae^{bt}\sin t),t\in R,a$ and $b$ constants, $a>0,b<0$, be a parametrized curve.
>
>a. Show that as $t\to+\infty$, $\alpha(t)$ approaches the origin $0$, spiraling around it.
>
>b. Show that $\alpha^{\prime}(t)\to(0,0)$ as $t\to+\infty$ and that
>
>$$\lim_{t\to+\infty}\int_{t_0}^{t}|\alpha^{\prime}(t)|dt $$
>
>is finite; that is, $\alpha$ has finite arc length in $[t_{0},\infty)$.

**a.**
Polar coordinates: $r = ae^{bt}$, $\theta = t$.
As $t\to+\infty$, $r\to 0$ while $\theta$ increases continuously.
Therefore the curve spirals into origin.

**b.**
Compute derivative:
$$\alpha'(t) = (abe^{bt}\cos t - ae^{bt}\sin t, abe^{bt}\sin t + ae^{bt}\cos t)= ae^{bt}(b\cos t - \sin t, b\sin t + \cos t)$$
Arc length:
$$\int_{t_0}^{t}|\alpha'(t)|dt = \int_{t_0}^{t} ae^{bt}\sqrt{b^2+1}dt= \frac{a\sqrt{b^2+1}}{b}\cdot(e^{bt}-e^{bt_0})$$
Thus
$$\lim_{t\to+\infty}\int_{t_0}^{t}|\alpha^{\prime}(t)|dt=\frac{a\sqrt{b^2+1}}{b}\cdot(-e^{bt_0})$$
is finite.
___

>[!problem] Problem 13
>Let $\alpha: I\rightarrow R^{3}$ be a parametrized curve. Let $[a,b]\subset I$ and set $\alpha(a)=p$, $\alpha(b)=q$.
>
>a. Show that, for any constant vector $v$, $|v|=1$,
>
>$$ (q-p)\cdot v=\int_{a}^{b}\alpha^{\prime}(t)\cdot v  dt\leq\int_{a}^{b}|\alpha^{\prime}(t)|  dt. $$
>
>b. Set
>
>$$ v=\frac{q-p}{|q-p|} $$
>
>and show that
>
>$$ |\alpha(b)-\alpha(a)|\leq\int_{a}^{b}|\alpha^{\prime}(t)|  dt; $$
>
>that is, the curve of shortest length from $\alpha(a)$ to $\alpha(b)$ is the straight line joining these points.

**a.**
By Fundamental Theorem of Calculus:
$$q-p=\int_a^b\alpha'(t)dt$$
Take dot product with unit vector $v$:
$$(q-p)\cdot v=\int_a^b\alpha'(t)\cdot vdt$$
By Cauchy-Schwarz:
$$|\alpha'(t)\cdot v|\leq|\alpha'(t)||v|=|\alpha'(t)|$$
Therefore:
$$(q-p)\cdot v\leq\int_a^b|\alpha'(t)\cdot v|dt\leq\int_a^b|\alpha'(t)|dt$$

**b.**
From (a) we know:
$$(q-p)\cdot v\leq\int_a^b|\alpha'(t)|dt$$
And $(q-p)\cdot v=|q-p|=|\alpha(b)-\alpha(a)|$, so
$$|\alpha(b)-\alpha(a)|\leq\int_a^b|\alpha'(t)|dt$$
Equality holds only when $\alpha'(t)$ is parallel to $v$ for all $t$, which occurs only for straight line path.