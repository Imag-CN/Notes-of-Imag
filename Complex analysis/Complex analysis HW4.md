### [GAM01] II.2.5
>[!problem]
>If $f=u+iv$ is analytic, then $\left|\nabla u\right|=\left|\nabla v\right|=\left|f^{\prime}\right|$.

We have:
$$|\nabla u|^2 = \left(\frac{\partial u}{\partial x}\right)^2 + \left(\frac{\partial u}{\partial y}\right)^2$$

Since $f$ is analytic, the Cauchy-Riemann equations hold:
$$\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y}, \quad \frac{\partial u}{\partial y} = -\frac{\partial v}{\partial x}$$

Substituting gives:
$$|\nabla u|^2 = \left(\frac{\partial u}{\partial x}\right)^2 + \left(-\frac{\partial v}{\partial x}\right)^2 = \left(\frac{\partial u}{\partial x}\right)^2 + \left(\frac{\partial v}{\partial x}\right)^2$$

Since $f'(z) = \dfrac{\partial u}{\partial x} + i\dfrac{\partial v}{\partial x}$, we have:
$$|f'(z)|^2 = \left(\frac{\partial u}{\partial x}\right)^2 + \left(\frac{\partial v}{\partial x}\right)^2$$
Therefore, $|\nabla u| = |f'(z)|$
Similarly, we can prove that $|\nabla v| = |f'(z)|$. 
___
### [GAM01] II.2.6
>[!problem]
>If $f=u+iv$ is analytic on $D$, then $\nabla v$ is obtained by rotating $\nabla u$ by $90^\circ$. In particular, $\nabla u$ and $\nabla v$ are orthogonal.

We have:
$$\nabla u = \left(\frac{\partial u}{\partial x}, \frac{\partial u}{\partial y}\right),\nabla v = \left(\frac{\partial v}{\partial x}, \frac{\partial v}{\partial y}\right)$$
By Cauchy-Riemann equations:
$$\nabla v = \left(-\frac{\partial u}{\partial y}, \frac{\partial u}{\partial x}\right)$$
We compute dot product:
$$\nabla u \cdot \nabla v = \frac{\partial u}{\partial x}\left(-\frac{\partial u}{\partial y}\right) + \frac{\partial u}{\partial y}\left(\frac{\partial u}{\partial x}\right) = 0$$
Therefore $\nabla u$ and $\nabla v$ are orthogonal.
___
### [GAM01] II.2.8
>[!problem]
>Derive the polar form of the Cauchy-Riemann equations for $u$ and $v$:
>$$
>\frac{\partial u}{\partial r}=\frac{1}{r}\frac{\partial v}{\partial\theta},\quad\frac{\partial u}{\partial\theta}=-r\frac{\partial v}{\partial r}.
>$$
>Check that for any integer $m$, the functions $u(re^{i\theta})=r^{m}\cos(m\theta)$ and $v(re^{i\theta})=r^{m}\sin(m\theta)$ satisfy the Cauchy-Riemann equations.

Let $z = re^{i\theta}$, $f(z) = u(r,\theta) + iv(r,\theta)$.
By chain rule:
$$
\frac{\partial u}{\partial r} = \frac{\partial u}{\partial x}\frac{\partial x}{\partial r} + \frac{\partial u}{\partial y}\frac{\partial y}{\partial r} = \frac{\partial u}{\partial x}\cos\theta + \frac{\partial u}{\partial y}\sin\theta
$$
$$
\frac{\partial u}{\partial\theta} = \frac{\partial u}{\partial x}\frac{\partial x}{\partial\theta} + \frac{\partial u}{\partial y}\frac{\partial y}{\partial\theta} = \frac{\partial u}{\partial x}(-r\sin\theta) + \frac{\partial u}{\partial y}(r\cos\theta)
$$
Similarly for $v$. Using Cartesian Cauchy-Riemann equations $\dfrac{\partial u}{\partial x} = \dfrac{\partial v}{\partial y}$, $\dfrac{\partial u}{\partial y} = -\dfrac{\partial v}{\partial x}$:

$$
\frac{\partial u}{\partial r} = \frac{\partial v}{\partial y}\cos\theta - \frac{\partial v}{\partial x}\sin\theta = \frac{1}{r}\frac{\partial v}{\partial\theta}\Rightarrow\frac{\partial u}{\partial r}=\frac{1}{r}\frac{\partial v}{\partial\theta},
$$
$$
\frac{\partial u}{\partial\theta} = -r\frac{\partial v}{\partial y}\sin\theta - r\frac{\partial v}{\partial x}\cos\theta = -r\frac{\partial v}{\partial r}\Rightarrow\frac{\partial u}{\partial\theta}=-r\frac{\partial v}{\partial r}.
$$

Now check $u = r^m\cos(m\theta)$, $v = r^m\sin(m\theta)$:
$$
\frac{\partial u}{\partial r} = mr^{m-1}\cos(m\theta),
$$
$$
\frac{1}{r}\frac{\partial v}{\partial\theta} = \frac{1}{r}(mr^m\cos(m\theta)) = mr^{m-1}\cos(m\theta).
$$
$$
\frac{\partial u}{\partial\theta} = -mr^m\sin(m\theta),
$$
$$
-r\frac{\partial v}{\partial r} = -r(mr^{m-1}\sin(m\theta)) = -mr^m\sin(m\theta).
$$
___
### [GAM01] II.4.3
>[!problem]
>Consider the branch of $f(z)=\sqrt{z(1-z)}$ on $\mathbb{C} \backslash [0,1]$ that has positive imaginary part at $z=2$. What is $f^{\prime}(z)$? Be sure to specify the branch of the expression for $f^{\prime}(z)$.

Let $w = f(z)$, so $w^2 = z(1-z)$.
Differentiate implicitly with respect to $z$:
$$
2w \frac{dw}{dz} = \frac{dw^2}{dz}= 1 - 2z.
$$
Then
$$
f'(z) = \frac{dw}{dz} = \frac{1 - 2z}{2w}= \frac{1 - 2z}{2f(z)}
$$
Thus the branch of $f'(z)$ is determined by the branch of $f(z)$.
For $u = z(1-z)$, we write $t = re^{i\theta}$ with $r > 0$ and $-\pi < \theta \leq \pi$, then we define:
$$
\sqrt{z(1-z)} = \sqrt{r} e^{i\theta/2}
$$
The branch cut for $f(z)$ is $[0,1]$ because when $z$ crosses this interval, $z(1-z)$ becomes real and non-positive, causing a discontinuity in the chosen branch of the square root, and this definition also satisfies $f(2)=i\sqrt{ 2 }$.
Thus, we can define
$$
\sqrt{z(1-z)} = e^{ \frac{1}{2} \operatorname{Log}(z(1-z)). }
$$
Therefore,
$$
f'(z) = \frac{1 - 2z}{2\sqrt{z(1-z)}}
$$
where $\sqrt{z(1-z)}$ is the branch specified above.
___
### [GAM01] II.4.4
>[!problem]
>Recall that the principal branch of the inverse tangent function was defined on the complex plane with two slits on the imaginary axis by
>$$ \tan^{-1} z=\frac{1}{2 i} \log \left( \frac{1+i z}{1-i z} \right), \quad z \notin (-i \infty,-i] \cup [i, i \infty) . $$
>Find the derivative of $\tan^{-1} z$. Find the derivative of $\tan^{-1} z$ for any analytic branch of the function defined on a domain D.

By chain rule:
$$
\frac{d}{dz} \tan^{-1} z = \frac{1}{2i} \cdot \frac{1}{\frac{1+iz}{1-iz}} \cdot \frac{d}{dz} \left( \frac{1+iz}{1-iz} \right)= \frac{1}{2i} \cdot \frac{1}{\frac{1+iz}{1-iz}} \cdot\frac{2i}{(1-iz)^2}= \frac{1}{1+z^2}.
$$
For any analytic branch of $\tan^{-1} z$ defined on a domain $D$, the derivative is
$$
\frac{d}{dz} \tan^{-1} z = \frac{1}{1+z^2},
$$
This holds because different branches differ by an additive constant  (from the logarithm), which vanishes during differentiation.<div style="page-break-after: always;"></div>
___
### [GAM01] II.4.5
>[!problem]
>Recall that $\cos^{-1}(z)=-i \log \left[ z \pm \sqrt{z^{2}-1} \right]$. Suppose $g(z)$ is an analytic branch of $\cos^{-1}(z)$, defined on a domain $D$. Find $g^{\prime}(z)$. Do different branches of $\cos^{-1}(z)$ have the same derivative?

By chain rule:
$$
g'(z) = -i \cdot \frac{1}{z \pm \sqrt{z^2 - 1}} \cdot \left( 1 \pm \frac{1}{2\sqrt{z^2 - 1}} \cdot 2z \right)
= -i \cdot \frac{1}{z \pm \sqrt{z^2 - 1}} \cdot \left( 1 \pm \frac{z}{\sqrt{z^2 - 1}} \right)=\frac{i}{\sqrt{z^2 - 1}}.
$$
Thus
$$
g'(z) = \frac{i}{\sqrt{z^2 - 1}}.
$$
The square root have two branches (differ by a sign), thus $g'(z)$ have two branches (differ by a sign).
More preceisely, since $\cos z_{1}=\cos z_{2} \Leftrightarrow z_{1}=\pm z_{2}+2\pi k$, different branches of $\cos ^{-1}(z)$ may differ by a sign (remains during differentiation) or an additive constant $2\pi k$ (vanishes during differentiation).
Therefore, different branches of $\cos^{-1}(z)$ do not necessarily have the same derivative (they may differ by a sign).
___
### [GAM01] II.4.7
>[!problem]
>Let $f(z)$ be a bounded analytic function, defined on a bounded domain $D$ in the complex plane, and suppose that $f(z)$ is one-to-one. Show that the area of $f(D)$ is given by
>$$
>\text{Area}(f(D))=\iint_{D}\left|f'(z)\right|^{2}dxdy.
>$$

According to the substitution rule for multiple integrals:
$$\begin{align}
\text{Area}(f(D))&=\iint_{f(D)}dxdy\\
&=\iint_{f(D)}dudv \\
&=\iint_{D}\left| \frac{\partial(u,v)}{\partial(x,y)}  \right| dxdy \\
&=\iint_{D} \left|\frac{ \partial u }{ \partial x }\frac{ \partial v }{ \partial y }-  \frac{ \partial u }{ \partial y }\frac{ \partial v }{ \partial x }  \right| dxdy \\
\text{(By C-R)}&=\iint_{D}\left|f'(z)\right|^{2} dxdy
\end{align}
$$
Therefore,
$$
\text{Area}(f(D))=\iint_{D}\left|f'(z)\right|^{2}dxdy.
$$
___

### [GAM01] II.5.1
>[!problem]
>Show that the following functions are harmonic, and find harmonic conjugates:
>
>(a) $x^{2}-y^{2}$
>
>(c) $\sinh x\sin y$
>
>(f) $x/(x^{2}+y^{2})$

#### (a)

$\Delta u = 2 - 2 = 0$. Harmonic.
$v_y = u_x = 2x \Rightarrow v = 2xy + g(x)$
$-v_x = u_y = -2y \Rightarrow v_x = 2y$
$v_x = 2y + g'(x) = 2y \Rightarrow g'(x)=0$
$v = 2xy$.
___
#### (c)

$u_{xx} = \sinh x\sin y$, $u_{yy} = -\sinh x\sin y$, $\Delta u = 0$. Harmonic.
$v_y = u_x = \cosh x\sin y \Rightarrow v = -\cosh x\cos y + h(x)$
$-v_x = u_y = \sinh x\cos y \Rightarrow v_x = -\sinh x\cos y$
$v_x = -\sinh x\cos y + h'(x) = -\sinh x\cos y \Rightarrow h'(x)=0$
$v = -\cosh x\cos y$.
___
#### (f)

$u = \operatorname{Re}(1/z)$, harmonic for $z\neq0$ (since $1/z$ is analytic when $z \neq{0}$).
$1/z = \dfrac{x}{x^{2}+y^{2}} - i\dfrac{y}{x^{2}+y^{2}}$
Thus $v = -\dfrac{y}{x^{2}+y^{2}}$.
___
### [GAM01] II.5.4
>[!problem]
>Show that if $h(z)$ is a complex-valued harmonic function (solution of Laplace's equation) such that $zh(z)$ is also harmonic, then $h(z)$ is analytic.

Let $h(z)=h(x+iy)=u(x,y)+iv(x,y)$, where $x,y,u,v \in \mathbb{R}$.
$h(z)$ harmonic $\Rightarrow$  
$$
u_{xx}+u_{yy}=0,v_{xx}+v_{yy}=0,
$$
$zh(z)=xu-yv+i(xv+yu)$ harmonic $\Rightarrow$
$$
2u_{x}+xu_{xx}-yv_{xx}+xu_{yy}-2v_{y}-yv_{yy}=0,2v_{x}+xv_{xx}+yu_{xx}+xv_{yy}+2u_{y}+yu_{yy}=0.
$$
Combining the above four equations, it can be concluded that $u_{x}=v_{y},v_{x}=-u_{y}$.
While $u,v$ are real analytic, $h(z)$ is analytic.
___
### [GAM01] II.5.5
>[!problem]
>Show that Laplace's equation in polar coordinates is
>
>$$ \frac{\partial^{2}u}{\partial r^{2}}+\frac{1}{r}\frac{\partial u}{\partial r}+\frac{1}{r^{2}}\frac{\partial^{2}u}{\partial\theta^{2}}=0. $$

We have $x = r\cos\theta$, $y = r\sin\theta$, then by chain rule:
$$
\frac{\partial u}{\partial r} = \frac{\partial u}{\partial x}\frac{\partial x}{\partial r} + \frac{\partial u}{\partial y}\frac{\partial y}{\partial r} = u_x\cos\theta + u_y\sin\theta
$$
$$
\frac{\partial u}{\partial \theta} = \frac{\partial u}{\partial x}\frac{\partial x}{\partial \theta} + \frac{\partial u}{\partial y}\frac{\partial y}{\partial \theta} = -u_x r\sin\theta + u_y r\cos\theta
$$
Compute second derivatives:
$$
\frac{\partial^2 u}{\partial r^2} = \frac{\partial}{\partial r}(u_x\cos\theta + u_y\sin\theta) = u_{xx}\cos^2\theta + 2u_{xy}\sin\theta\cos\theta + u_{yy}\sin^2\theta
$$
$$
\frac{\partial^2 u}{\partial \theta^2} = \frac{\partial}{\partial \theta}(-u_x r\sin\theta + u_y r\cos\theta)
$$
$$
= -u_x r\cos\theta - u_y r\sin\theta + r^2(u_{xx}\sin^2\theta - 2u_{xy}\sin\theta\cos\theta + u_{yy}\cos^2\theta)
$$
Thus
$$
\frac{\partial^2 u}{\partial r^2} + \frac{1}{r}\frac{\partial u}{\partial r} + \frac{1}{r^2}\frac{\partial^2 u}{\partial \theta^2}$$
$$= [u_{xx}\cos^2\theta + 2u_{xy}\sin\theta\cos\theta + u_{yy}\sin^2\theta]$$
$$+ \frac{1}{r}[u_x\cos\theta + u_y\sin\theta]$$
$$+ \frac{1}{r^2}[-u_x r\cos\theta - u_y r\sin\theta + r^2(u_{xx}\sin^2\theta - 2u_{xy}\sin\theta\cos\theta + u_{yy}\cos^2\theta)]$$
$$
=u_{xx}(\cos^2\theta + \sin^2\theta) + u_{yy}(\sin^2\theta + \cos^2\theta) = u_{xx} + u_{yy}
$$
Therefore, Laplace's equation in polar coordinates is:
$$\frac{\partial^{2}u}{\partial r^{2}}+\frac{1}{r}\frac{\partial u}{\partial r}+\frac{1}{r^{2}}\frac{\partial^{2}u}{\partial\theta^{2}}=0$$
___
### [GAM01] II.5.7
>[!problem]
>Show that $\log|z|$ has no conjugate harmonic function on the punctured plane $\mathbb{C}\backslash\{0\}$, though it does have a conjugate harmonic function on the slit plane $\mathbb{C}\backslash(-\infty,0]$.

$\log |z|=\mathrm{Re}\operatorname{Log}z$ , and $\operatorname{Log}z$ is a analytic function on the slit plane $\mathbb{C}\backslash(-\infty,0]$, thus $\log z$ have a conjugate harmonic function $\operatorname{Arg} |z|=\mathrm{\mathrm{Im}}\operatorname{Log}z$ on $\mathbb{C}\backslash(-\infty,0]$.

Assume for contradiction $\log|z|$ has a conjugate harmonic function $v$ on the punctured plane $\mathbb{C}\backslash\{0\}$, and restrict $v$ onto $\mathbb{C} \setminus(-\infty,0]$.
We already know different conjugate harmonic functions differ an addictive constant, thus $v=\operatorname{Arg} |z|+C$, where $C$ is a constant.
However, $\lim_{ y \to 0^+ }v(-1+iy)=\pi,\lim_{ y \to 0^- }v(-1+iy)=-\pi,$ thus $v$ is not continuous, which comes to a contradiction.
___
### [GAM01] II.6.4
>[!problem]
>Find a conformal map of the horizontal strip $\{-A < \operatorname{Im} z < A\}$ onto the right half-plane $\{\operatorname{Re} w > 0\}$.

$$
f(z)=e^{ \frac{\pi }{2A} z}
$$
It is conformal because it is analytic.
___
### [SL98] 2.3.3
>[!problem] 习题
>设$f$在$B(0,1) \cup \{1\}$上全纯, 并且
>$$f(B(0,1)) \subset B(0,1), f(1)=1,$$
>证明$f^{\prime}(1) \geq 0$.

记 $f'(1)=r_{0}e^{ i\theta_{0} },r_{0}\geq 0,\theta_{0} \in(-\pi,\pi]$, 只需证明 $\theta_{0}=0$, 因此为了反证我们设 $\theta_{0}\neq 0$.
由于$f$在$B(0,1) \cup \{1\}$上全纯, 我们有:
$$
f(1+re^{i\theta})=f(1)+f'(1)r e^{ i\theta }+o(r)=1+rr_{0} e^{ i(\theta+\theta_{0}) }+o(r).
$$
限制 $\theta \in\left( \dfrac{\pi}{2}, \dfrac{3\pi}{2} \right)$, 则对足够小的 $r$, $1+re^{i\theta}\in B(0,1)$, 从而 $f(1+re^{i\theta})\in B(0,1)$.
$\theta+\theta_{0} \in\left( \dfrac{\pi}{2}+\theta_{0}, \dfrac{3\pi}{2}+\theta_{0} \right)$,而 $\theta_{0}\neq 0$, 故存在一个 $\theta \in\left( \dfrac{\pi}{2}, \dfrac{3\pi}{2} \right)$, 使得 $e^{ i(\theta+\theta_{0}) }$ 的实部为正.
不妨设 $r_{0} e^{ i(\theta+\theta_{0})}=x_{0}+iy_{0},x_{0}>0$.
对足够小的 $r$, 我们有 $\left| \frac{o(r)}{r} \right|<x_{0}$, 此时 $r(x_{0}+iy_{0})+o(r)$ 实部为正.
但 $f(1+re^{i\theta})=1+rr_{0} e^{ i(\theta+\theta_{0}) }+o(r)=1+r(x_{0}+iy_{0})+o(r)\in B(0,1)$, 矛盾.
因此原命题得证.
___
### [SL98] 2.3.4
>[!problem] 习题
>设$f \in H(B(0,1))$, 如果存在$z_{0} \in B(0,1) \backslash \{0\}$, 使得$f(z_{0}) \neq 0,f^{\prime}(z_{0}) \neq 0$, 且$|f(z_{0})| = \max_{|z| \leq |z_{0}|}|f(z)|$, 那么
>$$\frac{z_{0} f^{\prime}(z_{0})}{f(z_{0})} > 0.$$

令 $g(z)= \dfrac{f(z_{0}z)}{f(z_{0})}$, 则 $\max_{|z| \leq |1|}|g(z)|=\dfrac{\max_{|z| \leq |z_{0}|}|f(z)|}{|f(z_{0})|}$.
又因为 $|f(z_{0})| = \max_{|z| \leq |z_{0}|}|f(z)|$, 所以 $g(B(0,1)) \subset B(0,1)$.
而 $g(1)=1$, 因此根据上一问, $g'(1)=\dfrac{z_{0} f^{\prime}(z_{0})}{f(z_{0})} \geq 0$.
又因为 $f(z_{0}) \neq 0,f^{\prime}(z_{0}) \neq 0$, 所以 $\dfrac{z_{0} f^{\prime}(z_{0})}{f(z_{0})} \neq 0$, 故而 $\dfrac{z_{0} f^{\prime}(z_{0})}{f(z_{0})} > 0$.
___
### Partial operator
>[!problem]
>Let us introduce the following notations:
>$$\dfrac{\partial}{\partial z}:=\dfrac{1}{2}\left(\dfrac{\partial}{\partial x}-i\dfrac{\partial}{\partial y}\right),\quad\dfrac{\partial}{\partial\bar{z}}:=\dfrac{1}{2}\left(\dfrac{\partial}{\partial x}+i\dfrac{\partial}{\partial y}\right).$$
>More explicitly, let $f=u+iv$ be continuously differentiable function then $\dfrac{\partial f}{\partial z}=\dfrac{1}{2}\left(\dfrac{\partial f}{\partial x}-i\dfrac{\partial f}{\partial y}\right)=\dfrac{1}{2}\left(\dfrac{\partial u}{\partial x}+i\dfrac{\partial v}{\partial x}-i\dfrac{\partial u}{\partial y}+\dfrac{\partial v}{\partial y}\right)$ and a similar formula holds for $\dfrac{\partial f}{\partial\bar{z}}$.
>(a) Compute $\dfrac{\partial}{\partial z}\left(e^{z}\right),\dfrac{\partial}{\partial\bar{z}}\left(e^{z}\right),\dfrac{\partial}{\partial z}\left(\bar{z}\right)$ and $\dfrac{\partial}{\partial\bar{z}}\left(\bar{z}\right)$.
>(b) Let $f=u+iv$ be a continuously differentiable function on a domain $D$. Show that $f$ is analytic if and only if $\dfrac{\partial f}{\partial\bar{z}}=0$ for any $z\in D$.
>(c) Suppose $f$ is analytic on a domain $D$. Verify that the complex derivative of $f$ is given by $\dfrac{\partial f}{\partial z}$.

#### (a)
$$
\frac{\partial}{\partial z}(e^z) = \frac{1}{2}\left(\frac{\partial e^z}{\partial x} - i\frac{\partial e^z}{\partial y}\right)
= \frac{1}{2}\left(e^z - i(ie^z)\right)
= \frac{1}{2}(e^z + e^z) = e^z,
$$
$$
\frac{\partial}{\partial\bar{z}}(e^z) = \frac{1}{2}\left(\frac{\partial e^z}{\partial x} + i\frac{\partial e^z}{\partial y}\right)
= \frac{1}{2}\left(e^z + i(ie^z)\right)
= \frac{1}{2}(e^z - e^z) = 0,
$$
$$
\frac{\partial}{\partial z}(\bar{z}) = \frac{1}{2}\left(\frac{\partial \bar{z}}{\partial x} - i\frac{\partial \bar{z}}{\partial y}\right)
= \frac{1}{2}\left(1 - i(-i)\right)
= \frac{1}{2}(1 - 1) = 0,
$$
$$
\frac{\partial}{\partial\bar{z}}(\bar{z}) = \frac{1}{2}\left(\frac{\partial \bar{z}}{\partial x} + i\frac{\partial \bar{z}}{\partial y}\right)
= \frac{1}{2}\left(1 + i(-i)\right)
= \frac{1}{2}(1 + 1) = 1.
$$
#### (b)
$$
\frac{\partial f}{\partial\bar{z}} = \frac{1}{2}\left(\frac{\partial f}{\partial x} + i\frac{\partial f}{\partial y}\right)
= \frac{1}{2}\left(\frac{ \partial u }{ \partial x }  + i \frac{ \partial v }{ \partial x }  + i\left( \frac{ \partial u }{ \partial y }  + i \frac{ \partial v }{ \partial y }  \right)\right)
= \frac{1}{2}\left[(\frac{ \partial u }{ \partial x } - \frac{ \partial v }{ \partial y }) + i(\frac{ \partial v }{ \partial x }+ \frac{ \partial u }{ \partial y })\right]
$$
Thus $\dfrac{\partial f}{\partial\bar{z}} = 0$ if and only if:
$$
\frac{ \partial u }{ \partial x } - \frac{ \partial v }{ \partial y } = 0 \quad \text{and} \quad \frac{ \partial v }{ \partial x }+ \frac{ \partial u }{ \partial y } = 0.
$$
These are exactly the Cauchy-Riemann equations.
Therefore, $f$ is analytic if and only if $\dfrac{\partial f}{\partial\bar{z}} = 0$ for all $z \in D$.
#### (c)
Since $f$ is analytic on $D$, we have
$$
f'(z)=f'(x+iy)= \frac{ \partial u }{ \partial x } +i \frac{ \partial v }{ \partial x } 
$$
and C-R equations
$$
\frac{ \partial u }{ \partial x } = \frac{ \partial v }{ \partial y },\frac{ \partial v }{ \partial x }=- \frac{ \partial u }{ \partial y }.
$$
Thus
$$
f'(z)=\dfrac{1}{2}\left(\dfrac{\partial u}{\partial x}+\dfrac{\partial v}{\partial y}\right) +\dfrac{i}{2}\left(\dfrac{\partial v}{\partial x}-i\dfrac{\partial u}{\partial y}\right)=\dfrac{1}{2}\left(\dfrac{\partial u}{\partial x}+i\dfrac{\partial v}{\partial x}-i\dfrac{\partial u}{\partial y}+\dfrac{\partial v}{\partial y}\right)\dfrac{\partial f}{\partial z}
$$
Therefore, the complex derivative of $f$ is given by $\dfrac{\partial f}{\partial z}$.