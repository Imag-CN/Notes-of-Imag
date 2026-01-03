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

