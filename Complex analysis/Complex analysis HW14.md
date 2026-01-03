___

>[!problem] [GAM] VIII.1.1
>Show that $z^{4}+2z^{2}-z+1$ has exactly one root in each quadrant.

**Proof:**
Denote $z=x+iy$, $P(z)=z^{4}+2z^{2}-z+1$.
When $y=0$:
$$
P(z)=P(x)=x^4+2x^2-x+1=(x^2+1 /2)^2+(x-1 /2)^2+1 /2>0
$$
Thus $P(z)$ has no root on the real axis.
When $x=0$:
$$
P(z)=P(iy)=y^4-2y^2-iy+1=(y^4-2y^2+1)-iy
$$
Since $y^4-2y^2+1$ and $iy$ cannot be zero at the same time, $P(z)$ has no root on the imaginary axis.

Construct contour as the following graph:
![[Pasted image 20260103222321.png]]
where $R$ is a sufficiently large positive number.

Since $P(z)$ is positive on the real axis, $\Delta_{\gamma_{1}}\mathrm{Arg}\,P(z)=0$.

Write $P(z)=z^4Q(z)$, where $Q(z)=1+ \dfrac{2z^2-z+1}{z^4}$. When $|z|=R$ is sufficient large, $|Q(z)-1|$ can be arbitrarily small. This means $Q(z)$ is contained inside a circle centered at $1$ with arbitrarily small radius, so $\Delta_{\gamma_{2}}\mathrm{Arg}\,Q(z)$ can be arbitrarily small. Thus 
$$
\Delta_{\gamma_{2}}\mathrm{Arg}\,P(z)=\Delta_{\gamma_{2}}\mathrm{Arg}\,z^4+\Delta_{\gamma_{2}}\mathrm{Arg}\,Q(z)=2\pi\pm\epsilon.
$$
On $\gamma_{3}$:
$$
\begin{align}
\Delta_{\gamma_{3}}\mathrm{Arg}\,P(z)&=\mathrm{Arg}\,P(0)-\mathrm{Arg}\,P(iR) \\
&=\mathrm{Arg}\,1-\mathrm{Arg}\,(R^4-2R^2+iR+1) \\
&=-\mathrm{Arg}\left(  1+ i \dfrac{R}{R^4+ -2R^2+1} \right) \\
\end{align}
$$
When $R$ is sufficiently large, $\dfrac{R}{R^4+ -2R^2+1}$ could be arbitrarily small, thus $\Delta_{\gamma_{3}}\mathrm{Arg}\,P(z)=-\mathrm{Arg}\left(  1+ i \dfrac{R}{R^4+ -2R^2+1} \right)$ can be arbitrarily small.

Therefore, $\Delta_{\gamma_{1}\cup\gamma_{2}\cup\gamma_{3}}\mathrm{Arg}\,P(z)=2\pi$. By argument principle, $P(z)$ has exactly one root in the first quadrant.

$P(z)$ has no roots on the coordinate axes, and its roots occur in conjugate pairs (since it is a real coefficient polynomial), and since it has four roots, it has one root in each of the four quadrants.
___

>[!problem] [GAM] VIII.2.1
>Show that $2z^{5}+6z-1$ has one root in the interval $0<x<1$ and four roots in the annulus $\left\{1<|z|<2\right\}$.

**Proof:**
Denote $f(z) = 2z^5 + 6z - 1$. Then we have $f(0) = -1 < 0$ and $f(1) = 7 > 0$. Since $f$ is continuous, by the Intermediate Value Theorem there exists $c \in (0,1)$ such that $f(c) = 0$. On real axis we have $f'(x) = 10x^4 + 6 > 0$ for all $x$, so $f$ is strictly increasing.
Therefore, there is exactly one real root in $(0,1)$.

Let $g(z) = 2z^5$ and $h(z) = 6z - 1$.  
For $|z| = 2$:  
$|g(z)| = 2 \cdot 2^5 = 64$,  
$|h(z)| \le 6|z| + 1 = 13 < 64$.  
By Rouché's Theorem, $f(z) = g(z) + h(z)$ and $g(z)$ have the same number of roots inside $|z| < 2$.  
Since $g(z) = 2z^5$ has a root of multiplicity $5$ at $z=0$, $f(z)$ has $5$ roots in $|z| < 2$.

Let $G(z) = 6z$ and $H(z) = 2z^5 - 1$.  
For $|z| = 1$:  
$|G(z)| = 6$,  
$|H(z)| \le 2|z|^5 + 1 = 3 < 6$.  
By Rouché's Theorem, $f(z) = G(z) + H(z)$ and $G(z)$ have the same number of roots inside $|z| < 1$.  
$G(z) = 6z$ has one root at $z=0$, so $f(z)$ has $1$ root in $|z| < 1$.

Based on the three points above, we can see that $f(z)$ has exactly one real root in $0 < x < 1$ and exactly four roots in the annulus $1 < |z| < 2$.
___

>[!problem] [GAM] VIII.2.2
>How many roots does $z^{9}+z^{5}-8z^{3}+2z + 1$ have between the circles $\{|z| = 1\}$ and $\{|z| = 2\}$?

**Solution:**
Let $f(z) = z^9 + z^5 - 8z^3 + 2z + 1$.

**1. On $|z| = 2$:**
Let $g(z) = z^9$, $h(z) = z^5 - 8z^3 + 2z + 1$.
For $|z| = 2$:
$$
|g(z)| = 2^9 = 512,
$$
$$
|h(z)| \le 2^5 + 8\cdot 2^3 + 2\cdot 2 + 1 = 32 + 64 + 4 + 1 = 101.
$$
Since $|g(z)| > |h(z)|$ on $|z| = 2$, by Rouché's theorem, $f(z)$ and $g(z)$ have the same number of zeros inside $|z| < 2$. $g(z) = z^9$ has $9$ zeros (all at $z=0$, counting multiplicities), thus $f(z)$ has 9 zeros in $|z| < 2$.

**2. On $|z| = 1$:**
Let $G(z) = -8z^3$, $H(z) = z^9 + z^5 + 2z + 1$.
For $|z| = 1$:
$$
|G(z)| = 8,
$$
$$
|H(z)| \le 1 + 1 + 2 + 1 = 5.
$$
Since $|G(z)| > |H(z)|$ on $|z| = 1$, by Rouché's theorem, $f(z)$ and $G(z)$ have the same number of zeros inside $|z| < 1$. $G(z) = -8z^3$ has $3$ zeros, so $f(z)$ has $3$ zeros in $|z| < 1$.

The number of zeros in the annulus is:
$$
(\text{number of zeros in } |z| < 2) - (\text{number of zeros in } |z| < 1) = 9 - 3 = 6.
$$
In conclusion, $f(z)$ has 6 zeros (counting multiplicities) in the annulus $1 < |z| < 2$.
___

>[!problem] [GAM] VIII.2.4
>Fix a complex number $\lambda$ such that $|\lambda|<1$. For $n\geq 1$, show that $(z-1)^n e^{z}-\lambda$ has $n$ zeros satisfying $|z-1|<1$ and no other zeros in the right half-plane. Determine the multiplicity of the zeros.

**Solution:**
Let $f(z) = (z-1)^n e^z - \lambda$ with $|\lambda| < 1$, $n \geq 1$. Take $g(z) = (z-1)^n e^z$, $h(z) = -\lambda$。

On $|z-1| = 1$:
$|g(z)| = |z-1|^n |e^z| = e^{\operatorname{Re}(z)} \geq 1$ (minimum at $z=0$, $\operatorname{Re}(z)=0$).
Since $|\lambda| < 1$, $|h(z)| = |\lambda| < 1 \leq |g(z)|$.

By Rouché, $f$ and $g$ have the same number of zeros in $|z-1|<1$. $g(z)$ has a zero of order $n$ at $z=1$, so $f$ has $n$ zeros in $|z-1|<1$ (counting multiplicities).

For $\operatorname{Re}(z) > 0$ and $|z-1| \geq 1$:
$|(z-1)^n e^z| = |z-1|^n e^{\operatorname{Re}(z)} \geq 1 \cdot e^{\operatorname{Re}(z)} > 1 > |\lambda|$.
So $|f(z)| \geq |(z-1)^n e^z| - |\lambda| > 0$, thus $f(z)$ has no zeros for $\operatorname{Re}(z) > 0$.

Thus all zeros in $\operatorname{Re}(z) > 0$ satisfy $|z-1|<1$, and there are exactly $n$ of them.

Derivative: $f'(z) = (z-1)^{n-1}e^z[n + (z-1)]$.
If $f(z_0)=0$ with $\operatorname{Re}(z_0) > 0$, then $z_0 \neq 1$ (since $f(1) = -\lambda \neq 0$).  
If $n + (z_0-1) = 0$, then $z_0 = 1-n$, but $\operatorname{Re}(1-n) \leq 0$.  
Thus $f'(z_0) \neq 0$ for all zeros, so all $n$ zeros are simple.
___

>[!problem] [GAM] IX.1.1
>Let $f(z)$ be analytic and satisfy $|f(z)|\leq M$ for $|z-z_{0}|<R$. Show that if $f(z)$ has a zero of order $m$ at $z_{0}$, then
>
>$$
>|f(z)|\leq\frac{M}{R^{m}}|z-z_{0}|^{m},\quad|z-z_{0}|<R.
>$$
>
>Show that equality holds at some point $z\neq z_{0}$ only when $f(z)$ is a constant multiple of $(z-z_{0})^{m}$.

**Proof:**
Since $f(z)$ has a zero of order $m$ at $z_0$, we can write
$$
f(z) = (z-z_0)^m g(z)
$$
where $g(z)$ is analytic in $|z-z_0| < R$ and $g(z_0) \neq 0$.

For $0 < r < R$, on the circle $|z-z_0| = r$ we have
$$
|f(z)| = |z-z_0|^m |g(z)| = r^m |g(z)| \leq M
\quad\Rightarrow\quad |g(z)| \leq \frac{M}{r^m}.
$$
By the maximum modulus principle, this inequality holds for all $|z-z_0| \leq r$. Letting $r \to R^-$, we obtain
$$
|g(z)| \leq \frac{M}{R^m}, \quad |z-z_0| < R.
$$
Therefore,
$$
|f(z)| = |z-z_0|^m |g(z)| \leq \frac{M}{R^m} |z-z_0|^m, \quad |z-z_0| < R.
$$

If equality holds at some $z_1 \neq z_0$, i.e.,
$$
|f(z_1)| = \frac{M}{R^m} |z_1 - z_0|^m,
$$
then
$$
|g(z_1)| = \frac{M}{R^m}.
$$
Since $|g(z)| \leq M/R^m$ in $|z-z_0| < R$, the maximum modulus principle implies that $|g(z)|$ is constant, i.e., $g(z) \equiv c$ for some constant $c$ with $|c| = M/R^m$. Hence
$$
f(z) = c (z-z_0)^m.
$$
Conversely, if $f(z) = c (z-z_0)^m$ with $|c| = M/R^m$, then equality holds for all $z$.
___

>[!problem] [GAM] IX.1.1
>Let $f(z)$ be analytic on $|z|<1$ with $|f(z)|\leq 1$ and $|f(0)|=r>0$. Show that
>
>$$|f(z)|\geq\frac{r-|z|}{1-r|z|},\quad|z|<r.$$
>
>When does equality occur?

**Proof:**
Let $a = f(0)$, with $a = re^{i\theta}$.

Consider the automorphism of the unit disk:
$$
\phi(w) = \frac{w - a}{1 - \overline{ a } w}.
$$
Then $\phi(a) = 0$, and $|\phi(w)| \leq 1$ for $|w| \leq 1$.

Define $g(z) = \phi(f(z)) = \dfrac{f(z) - a}{1 - \overline{ a } f(z)}$, then:
- $g$ is analytic on $|z| < 1$ (since $|f(z)| \leq 1$).
- $|g(z)| \leq 1$ on $|z| < 1$ (as composition of disk self-maps).
- $g(0) = \phi(f(0)) = \phi(a) = 0$.

By Schwarz lemma, $|g(z)| \leq |z|$ for $|z| < 1$.

Thus
$$
\left|\frac{f(z) - a}{1 - \overline{ a } f(z)}\right| \leq |z|.
$$
By the triangle inequality we have
$$
|f(z)-a|\leq |f(z)|-|a|=|f(z)|-r\quad\text{and}\quad|1-\overline{ a }f(z)|\geq 1+|\overline{ a }f(z)|=1+r|f(z)|
$$
Thus
$$
\dfrac{|f(z)|-r}{1+r|f(z)|}\leq|z|
$$
Rearranging:
$$
|f(z)| \geq \frac{r - |z|}{1 - r|z|}.
$$

**Equality condition:**
Equality obvious holds for every $f$ at $z=0$.
Further, equality at other points requires $|g(z_0)| = |z_0|$ for some $z_0$ with $|z_0| < r$. By Schwarz lemma, this happens iff $g(z) = e^{i\theta_{0}} z$ for some real $\theta_{0}$. Then $\phi(f(z))=e^{i\theta_{0}} z$, $f(z)=e^{i\theta_{0}} z\,\circ \phi^{-1}(z)$. Therefore $f$ is any automorphisim on unit disk.