___

>[!problem] [GAM] V.7.1
>Find the zeros and orders of zeros of the following functions.
>
>(e) $\dfrac{\cos z-1}{z}$
>
>(f) $\dfrac{\cos z-1}{z^{2}}$
>
>(i) $\dfrac{\operatorname{Log} z}{z}$(Principal value)

**Solution:**
**(e)** $\dfrac{\cos z-1}{z}=0\Rightarrow\cos z-1=0\iff z=2k\pi,k\in \mathbb{Z}$.
Taylor expansion at $z_{0}=0$:
$$
\cos z-1=\dfrac{z^2}{2}- \dfrac{z^4}{24}+\dots
$$
Thus the zeros are $z=2k\pi,k\in \mathbb{Z}$, the order is $1$ for $k=0$ while the order is $2$ (by periodicity) for $k \neq0$.

**(f)** Similar to **(e)**, the zeros are $z=2k\pi,k\in \mathbb{Z} \neq 0$ while the order is $2$ ($z=0$ is no longer a zero).

**(i)** $\dfrac{\operatorname{Log} z}{z}=0\Rightarrow\operatorname{Log}z=0\iff z=1$
Taylor expansion at $z_{0}=1$:
$$\operatorname{Log}z=(z-1)- \dfrac{(z-1)^2}{2}+\dots$$
Thus the zero is $z=1$ with order $1$.
___

>[!problem] [GAM] V.7.5
>Show that
>
>$$ \int_{-\infty}^{\infty} e^{-z t^{2}+2 w t} d t=\sqrt{\frac{\pi}{z}} e^{w^{2} / z}, \quad z, w \in \mathbb{C}, \operatorname{Re} z>0, $$
>
>where we take the principal branch of the square root. Compare the result to Exercise IV.3.1.

**Proof:**
Let $F(z,w) = \int_{-\infty}^{\infty} e^{-z t^{2}+2 w t} dt$.

For fixed $t$, the integrand $e^{-z t^{2}+2 w t}$ is analytic in $z$ and $w$. For $\operatorname{Re} z > 0$, the integral converges absolutely and uniformly on compact sets. Thus, $F(z,w)$ is analytic in $z$ and $w$ for $\operatorname{Re} z > 0$.

Complete the square in the exponent:
$$-x t^2 + 2 w t = -x \left(t^2 - \frac{2w}{x}t\right) = -x \left[\left(t - \frac{w}{x}\right)^2 - \frac{w^2}{x^2}\right] = -x \left(t - \frac{w}{x}\right)^2 + \frac{w^2}{x}.$$
Substitute $u = \sqrt{x}(t - w/x)$, so $du = \sqrt{x}  dt$.
$$F(x,w) = \int_{-\infty}^{\infty} e^{-x (t - w/x)^2 + w^2/x} dt = e^{w^2/x} \int_{-\infty}^{\infty} e^{-x (t - w/x)^2} dt = \frac{e^{w^2/x}}{\sqrt{x}} \int_{-\infty}^{\infty} e^{-u^2} du.$$
Using the known Gaussian integral $\int_{-\infty}^{\infty} e^{-u^2} du = \sqrt{\pi}$, we get:
$$F(x,w) = \sqrt{\frac{\pi}{x}} e^{w^2/x}.$$
The function $\sqrt{\pi/z}  e^{w^2/z}$ is analytic for $\operatorname{Re} z > 0$ (taking the principal branch). Since $F(z,w)$ and $\sqrt{\pi/z}  e^{w^2/z}$ are analytic in $z$ and $w$ for $\operatorname{Re} z > 0$ and agree for $z=x>0$, $w \in \mathbb{R}$, they agree for all $z,w \in \mathbb{C}$ with $\operatorname{Re} z > 0$ by the identity theorem.

Exercise IV.3.1 likely evaluates the Fourier transform of a Gaussian, $\int_{-\infty}^{\infty} e^{-t^2} e^{-i\xi t} dt$, which is a special case of this result with $z=1$ and $w=-i\xi/2$. 
___

>[!problem] [GAM] V.7.6
>Suppose $f(z)$ is analytic on a domain $D$ and $z_0 \in D$. Show that if $f^{(m)}(z_0)=0$ for $m \geq 1$, then $f(z)$ is constant on $D$.

**Proof:**
Since $f$ is analytic at $z_0$, it has a Taylor expansion valid in some disk $B_R(z_0) \subset D$:
$$f(z) = \sum_{n=0}^\infty a_n (z - z_0)^n, \quad a_n = \frac{f^{(n)}(z_0)}{n!}.$$
Given that $f^{(m)}(z_0) = 0$ for all $m \geq 1$, we have $a_m = 0$ for all $m \geq 1$.
Therefore, in the disk $B_R(z_0)$,
$$f(z) = a_0 = f(z_0),$$
By the identity theorem, the equality holds for the whole $D$.
___

>[!problem] [GAM] V.7.9
>Show that if the analytic function $f(z)$ has a zero of order $N$ at $z_{0}$, then $f(z)=g(z)^{N}$ for some function $g(z)$ analytic near $z_{0}$ and satisfying $g^{\prime}(z_{0})\neq 0$.

**Proof:**
Since $f$ is analytic and has a zero of order $N$ at $z_0$, in a neighborhood of $z_0$ it can be written as
$$f(z) = (z - z_0)^N h(z),$$
where $h(z)$ is analytic near $z_0$ and $h(z_0) \ne 0$.

Because $h(z_0) \ne 0$ and $h$ is analytic, we can define an analytic $N$-th root of $h(z)$ near $z_0$. Let
$$k(z) = h(z)^{1/N}= \exp((1/N)\operatorname{Log} h(z)),$$
where we choose the branch such that $k(z_0) = (h(z_0))^{1/N} \ne 0$. The function $k(z)$ is analytic near $z_0$.

Now define
$$g(z) = (z - z_0) \, k(z).$$
Then $g$ is analytic near $z_0$ (product of analytic functions) and
$$g(z)^N = (z - z_0)^N \, k(z)^N = (z - z_0)^N \, h(z) = f(z).$$

Finally, we check the derivative condition:
$$g'(z) = k(z) + (z - z_0) k'(z).$$
Thus $g'(z_0) = k(z_0) \ne 0$. Therefore, $g(z)$ satisfies all the required conditions.
___

>[!problem] [GAM] V.7.10
>Show that if $f(z)$ is a continuous function on a domain $D$ such that $f(z)^{N}$ is analytic on $D$ for some integer $N$, then $f(z)$ is analytic on $D$.

**Proof:**
Let $F(z)=f(z)^N$, analytic on $D$. $f$ is continuous on $D$.
If $F\equiv0$, then $f\equiv0$ and is analytic. Otherwise, the zeros of $F$ are isolated.

On $D' = D \setminus \{ \text{zeros of } F \}$, define $g(z) = \exp((1/N)\operatorname{Log} F(z))$ locally. Then $g$ is analytic, $g^N=F$, and $f^N = g^N$. Thus $(f/g)^N=1$, so $f/g$ is locally constant (an $N$th root of unity). Since $f$ is continuous, on each component of $D'$, $f = k g$ for some constant $k$, so $f$ is analytic on $D'$.

Now let $z_0$ be a zero of $F$. Since $f$ is continuous, $f(z_0)=0$. In a punctured neighborhood of $z_0$, $f$ is analytic (as shown above) and bounded (since $f^N=F$ is analytic, hence bounded near $z_0$). So $z_{0}$ is a removable singularity, $f$ extends analytically to $z_0$.

Therefore, $f$ is analytic on all of $D$.
___

>[!problem] [GAM] VI.1.1
>Find all possible Laurent expansions centered at $0$ of the following functions:
>
>(a) $\frac{1}{z^2-z}$
>
>(b) $\frac{z-1}{z+1}$

**Solution:**
**(a)** Singularity: $z=0$ and $z=1$.

Region 1: $|z| > 1$
$$
\frac{1}{z^2-z} =  \frac{1}{z^2} \cdot \frac{1}{1 - \frac{1}{z}} = \frac{1}{z^2} \sum_{n=0}^{\infty} \left( \frac{1}{z} \right)^n = \sum_{n=0}^{\infty} \frac{1}{z^{n+2}}
$$

Region 2: $0 < |z| < 1$
$$
\frac{1}{z^2-z} =  -\frac{1}{z} \cdot \frac{1}{1-z} = -\frac{1}{z} \sum_{n=0}^{\infty} z^n = -\frac{1}{z} - \sum_{n=0}^{\infty} z^n
$$

**(b)** Singularity: $z=-1$.

Region 1: $|z| > 1$
$$
\frac{z-1}{z+1} =-1+ \dfrac{2}{1-(- 1/z )} = -1 + 2 \sum_{n=0}^{\infty}  \frac{(-1)^n}{z^{n}} = 1 + 2 \sum_{n=1}^{\infty}  \frac{(-1)^n}{z^{n}} 
$$

Region 2: $0 \leq |z| < 1$
$$
\frac{z-1}{z+1} =1- \dfrac{2}{1-(-z)} = 1 - 2 \sum_{n=0}^{\infty} (-1)^n z^n=-1 - 2 \sum_{n=1}^{\infty} (-1)^n z^n
$$
___

>[!problem] [GAM] VI.1.2
>For 
>$$
>f(z)=\frac{1}{(z^2-1)(z^2-4)}
>$$
>find the Laurent expansion centered at $z = -1$ that converges at $z = \frac{1}{2}$. Determine the largest open set on which each series converges.

**Solution:**
Singularities at $z = \pm 1, \pm 2$.
Simplify yields:
$$
f(z) = -\frac{1}{6} \cdot \frac{1}{z-1} + \frac{1}{6} \cdot \frac{1}{z+1} + \frac{1}{12} \cdot \frac{1}{z-2} - \frac{1}{12} \cdot \frac{1}{z+2}
$$
Let $w = z+1$, then:
$$
f(z) = -\frac{1}{6} \cdot \frac{1}{w-2} + \frac{1}{6} \cdot \frac{1}{w} + \frac{1}{12} \cdot \frac{1}{w-3} - \frac{1}{12} \cdot \frac{1}{w+1}
$$
Convergence Point $z = 1/2$ corresponds to $w = z+1 = 3/2$.

$\dfrac{1}{w}$: Already a Laurent term $\frac{1}{w}$.
$\dfrac{1}{w-2}$: 
$$
\frac{1}{w-2} = -\frac{1}{2} \cdot \frac{1}{1 - w/2} = -\frac{1}{2} \sum_{n=0}^{\infty} \left( \frac{w}{2} \right)^n = -\sum_{n=0}^{\infty} \frac{w^n}{2^{n+1}}, \quad |w| < 2
$$
$\dfrac{1}{w-3}$:
$$
\frac{1}{w-3} = -\frac{1}{3} \cdot \frac{1}{1 - w/3} = -\frac{1}{3} \sum_{n=0}^{\infty} \left( \frac{w}{3} \right)^n = -\sum_{n=0}^{\infty} \frac{w^n}{3^{n+1}}, \quad |w| < 3
$$
$\frac{1}{w+1}$:
$$
\frac{1}{w+1} = \frac{1}{w} \cdot \frac{1}{1 + 1/w} = \frac{1}{w} \sum_{n=0}^{\infty} (-1)^n \frac{1}{w^n} = \sum_{n=0}^{\infty} (-1)^n \frac{1}{w^{n+1}}, \quad |w| > 1
$$
So overall:
$$
\begin{aligned}
f(z) &= -\frac{1}{6} \left( -\sum_{n=0}^{\infty} \frac{w^n}{2^{n+1}} \right) + \frac{1}{6} \cdot \frac{1}{w} + \frac{1}{12} \left( -\sum_{n=0}^{\infty} \frac{w^n}{3^{n+1}} \right) - \frac{1}{12} \left( \sum_{n=0}^{\infty} (-1)^n \frac{1}{w^{n+1}} \right) \\
&=  \frac{1}{12} w^{-1} + \sum_{k=1}^{\infty} \frac{(-1)^{k+1}}{12} w^{-k-1} + \sum_{n=0}^{\infty} \frac{1}{12} \left( \frac{1}{2^n} - \frac{1}{3^{n+1}} \right) w^n, \quad 1 < |w| < 2
\end{aligned}
$$
Therefore, the Laurent expansion centered at $z=-1$ that converges at $z=1/2$ is:
$$
f(z) = \frac{1}{12(z+1)} + \sum_{k=1}^{\infty} \frac{(-1)^{k+1}}{12 (z+1)^{k+1}}(z+1)^{-k-1} + \sum_{n=0}^{\infty} \frac{1}{12} \left( \frac{1}{2^n} - \frac{1}{3^{n+1}} \right) (z+1)^n
$$
The largest open set on which each series converges is $\{ z\in \mathbb{C}: 1<|z+1|<2\}$.
___

>[!problem] [GAM] VI.1.5
>Suppose $f(z)$ is analytic on the punctured plane $D = \mathbb{C} \setminus \{0\}$. Show that there is a constant $c$ such that $f(z) - c/z$ has a primitive in $D$. Give a formula for $c$ in terms of an integral of $f(z)$.

**Proof:**
Since $f$ is analytic on the annulus $0 < |z| < \infty$, it has a Laurent expansion
$$
f(z) = \sum_{n=-\infty}^{\infty} a_n z^n, \quad 0 < |z| < \infty,
$$
A function $g$ analytic on $D$ has a primitive if and only if $\int_{\gamma} g(z) dz = 0$ for every closed curve $\gamma$ in $D$. It suffices to check the integral over a circle $L: |z|=1$.

For $f$, compute
$$
\oint_{L} f(z) dz = \oint_{L} \left( \sum_{n=-\infty}^{\infty} a_n z^n \right) dz.
$$
Since the Laurent series converges uniformly on the compact circle $C_r$, we can interchange summation and integration:
$$
\oint_{L} f(z) dz = \sum_{n=-\infty}^{\infty} a_n \oint_{L} z^n dz.
$$
But $\int_{C_r} z^n dz = 0$ for $n \ne -1$, and equals $2\pi i$ for $n=-1$. Therefore
$$
\oint_{L} f(z) dz = a_{-1} \cdot 2\pi i.
$$
Hence $f$ has a primitive on $D$ if and only if $a_{-1}=0$. Let $c=a_{-1}$ then $f(z) - c/z$ has a primitive in $D$.

We can use an integral to compute $c$:
$$
c=a_{-1}=\dfrac{1}{2\pi i} \oint_{L} f(z) dz  .
$$
___

>[!problem]
>Let $f,g:\mathbb{C}\to\mathbb{C}$ be two analytic functions. Assume $f(g(z))=0$ for all $z\in\mathbb{C}$. Show that: if $g$ is non-constant, then $f\equiv0$.

**Proof:** By the open mapping theorem, $g(\mathbb{C})$ is open. Then $f\equiv0$ on an open set. By the identity theorem, $f\equiv0$ on the whole $\mathbb{C}$.
___

>[!problem]
>Fix $r>0$ and consider the closed disk $\overline{B(0,r)}=\{z\in\mathbb{C}\mid|z|\leq r\}$. Let $f,g:\overline{B(0,r)}\to\mathbb{C}$ be continuous functions which are analytic on the open disk $B(0,r)=\{z\in\mathbb{C}\mid|z|<r\}$. Also assume that $|f(z)|=|g(z)|$ for all $|z|=r$. Show that: if $f$ and $g$ have no zeros in $\overline{B(0,r)}$, then $f=\lambda g$ for a constant $\lambda$ with $|\lambda|=1$.

**Proof**: Since $f$ and $g$ have no zeros in $\overline{B(0,r)}$, $f/g$ and $f /g$ are also analytic on $B(0,r)$ and continuous on $\overline{ B(0,r) }$. $|f(z)|=|g(z)|$ for all $|z|=r$ implies $|f /g|=|g /f|=1$ for all $|z|=r$. The the maximum principle shows that $|f /g|\leq1$ and $|g /f|\leq 1$ for all $z\in \overline{ B(0,r) }$, thus $|f(z)|=|g(z)|$ for all $z\in \overline{ B(0,r) }$. So ${f}/{g}$ is not an open mapping since it maps $B(0,r)$ to a non-empty subset of unit circle $\{ z\in C:|z|=1 \}$ (which can never be open). By the open mapping theorem, $f/g$ is a constant (denote as $\lambda$). Since $|f /g|=1$ for all $|z|=r$, $|\lambda|=1$.

Therefore, $f=\lambda g$ for a constant $\lambda$ with $|\lambda|=1$.