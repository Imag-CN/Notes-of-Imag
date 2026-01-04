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

>[!problem] [GAM] IX.1.5
>Let $f(z)$ be analytic and satisfies $|f(z)|\leq 1$ for $|z|<1$. Show that if $|f(0)|\geq r$, then $|f(z)|\geq\dfrac{r-|z|}{1-r|z|}$ for $|z|<r$.
>
>Determine for which functions $f(z)$ equality holds at some point $z_{0}$ with $|z_{0}|<r$.

**Proof:**
We need to prove a lemma first:
___

>[!lemma]
>For $z,w\in \mathbb{D}$, we have
>$$
>\dfrac{||z|-|w||}{1-|z||w|}\leq \left| \dfrac{z-w}{1-\overline{ w }z} \right| \leq \dfrac{|z|+|w|}{1+|z||w|},
>$$
>and the first equality holds if and only if $z$ and $w$ are in the same directions; the second equality holds if and only if $z$ and $w$ are in opposite directions.

The statement is trivial when $z=0$ or $w=0$. When $z,w \neq 0$, we let $a=|z|,b=|w|$ and $\theta=\mathrm{Arg}\,z-w$.

Then
$$
\begin{align}
\left| \dfrac{z-w}{1-\overline{ w }z} \right|^2&= \dfrac{a^2+b^2-2ab\cos\theta}{1+a^2b^2-2ab\cos\theta} \\
&=1- \dfrac{a^2b^2+1-a^2-b^2}{1+a^2b^2-2ab\cos\theta} \\
&=1- \dfrac{(1-a^2)(1-b^2)}{1+a^2b^2-2ab\cos\theta}
\end{align}
$$
Since $(1-a^2)(1-b^2)>0$ and $1+a^2b^2-2ab\cos\theta=1+|z||w|>0$, $\left| \dfrac{z-w}{1-\overline{ w }z} \right|^2$ is monotonically decreasing with respect to $\cos\theta$, so it attains its maximal value when $\cos\theta=-1$ and attains its minimal value when $\cos\theta=1$. This proves the lemma.

>[!remark]
>This is a result on Poincare disk.

___
Continue the proof:
Let $a=f(0)$, $|a|\geq r$. Define $g(z)=\dfrac{f(z)-a}{1-\bar{a}f(z)}$. Then $g:\mathbb{D}\to\mathbb{D}$ analytic, $g(0)=0$.

By Schwarz lemma: $|g(z)|\leq|z|$, i.e.
$$
|z|\geq\left|\frac{f(z)-a}{1-\bar{a}f(z)}\right|.
$$
By lemma we have 
$$
\left|\frac{f(z)-a}{1-\bar{a}f(z)}\right|\geq \dfrac{||f(z)|-|a||}{1-|f(z)||a|}\geq\dfrac{|a|-|f(z)|}{1-|f(z)||a|}.
$$
Then
$$
|z|\geq\dfrac{|a|-|f(z)|}{1-|f(z)||a|}
$$
Rearranging gives
$$
|f(z)|\geq\frac{|a|-|z|}{1+|a||z|}\geq\frac{r-|z|}{1-r|z|}.
$$
**Equality:**
First we require $|f(0)|=|a|=r$. Then the equality holds for every $f$ at $z=0$.

Then we consider when the equality holds at some point other than $z=0$. By Schwarz lemma we have: $|g(z_0)|=|z_0|$ for some $z_0\neq0$ iff $g(z)=e^{i\theta}z$, i.e.
$$
f(z)=\frac{a+e^{i\theta}z}{1+\bar{a}e^{i\theta}z},\quad |a|\geq r.
$$
In other words, $f$ is any automorphism on unit disk.

By the lemma, equality also needs $f(z_{0})$ and $a$ are in the same direction; and the equality $||f(z_{0})|-|a||=|a|-|f(z_{0})|$ requires $|a|\geq |f(z_{0})|$.
___

>[!problem] [GAM] IX.1.6
>Let $f(z)$ be a conformal map of the open unit disk onto a domain $D$. Show that the distance from $f(0)$ to the boundary of $D$ is estimated by $\operatorname{dist}(f(0),\partial D)\leq |f^{\prime}(0)|$.

**Proof:**
Let $a = f(0)$ and $d = \operatorname{dist}(a, \partial D) = \inf_{w \in \partial D} |a-w| > 0$.

Consider the disk $B(a, d) = \{w \in \mathbb{C}: |w-a| < d\}$. By definition of $d$, we have $B(a, d) \subset D$.

Define the function
$$
g(z) = \frac{f(z) - a}{d}.
$$
Since $f: \mathbb{D} \to D$ is conformal and $B(a,d) \subset D$, we have $|f(z)-a| < d$ for all $z \in \mathbb{D}$ (strict inequality because $f(z)$ lies in the interior of $D$). Thus $|g(z)| < 1$ for all $z \in \mathbb{D}$.

Also $g(0) = (f(0)-a)/d = 0$.

Therefore, $g: \mathbb{D} \to \mathbb{D}$ is analytic and $g(0)=0$. By Schwarz's lemma,
$$
|g'(0)| \leq 1.
$$

But
$$
g'(z) = \frac{f'(z)}{d} \quad \Rightarrow \quad g'(0) = \frac{f'(0)}{d}.
$$
Hence
$$
\frac{|f'(0)|}{d} \leq 1 \quad \Rightarrow \quad |f'(0)| \leq d = \operatorname{dist}(f(0), \partial D).
$$

Thus we have proved the inequality
$$
|f'(0)| \leq \operatorname{dist}(f(0), \partial D).
$$
___

>[!problem] [SL] 4.5.12
>(Carathéodory 不等式) 设 $f\in H(B(0,R))\cap C(\overline{B(0,R)})$, $M(r)=\max_{|z|=r}|f(z)|$, $A(r)=\max_{|z|=r}\operatorname{Re}f(z)$ $(0\leqslant r\leqslant R)$. 证明:
>
>$$M(r)\leqslant\frac{2r}{R-r}A(R)+\frac{R+r}{R-r}|f(0)|,\quad\forall r\in[0,R).$$

**证明:**
不失一般性地, 设 $R=1$. 记 $B=A(1)=\max_{|z|=1}\operatorname{Re}f(z)$.

令 $g(z)=B-f(z)$, 则 $\operatorname{Re}g(z)\ge0$ 在 $|z|=1$ 上, 由最大模原理, 在 $|z|<1$ 内 $\operatorname{Re}g(z)\ge0$, 即 $g$ 将单位圆盘映到右半平面 $\{\operatorname{Re}w\ge0\}$.

$T(w)=\frac{w-1}{w+1}$ 将右半平面 $\{\operatorname{Re}w\ge0\}$ 映到单位圆盘 $|T(w)|\le1$, 且 $T(1)=0$.

令
$$h(z)=T(g(z))=\frac{g(z)-1}{g(z)+1}=\frac{B-f(z)-1}{B-f(z)+1}.$$
则 $h\in H(\mathbb{D})$, $|h(z)|\le1$, 且
$$
h(0)=\frac{B-f(0)-1}{B-f(0)+1}.
$$
对 $h$ 用 Schwarz 引理: $|h(z)|\le|z|$, 即
$$
\left|\frac{B-f(z)-1}{B-f(z)+1}\right|\le|z|.
$$
由此解得
$$
|B-f(z)|\le\frac{1+|z|}{1-|z|}|B-f(0)|-\frac{2|z|}{1-|z|}B.
$$

由三角不等式 $|f(z)|\le|B-f(z)|+B$, 代入上式得
$$|f(z)|\le\frac{1+|z|}{1-|z|}|B-f(0)|+\frac{1-|z|}{1-|z|}B.$$
但 $|B-f(0)|\le B+|f(0)|$, 故
$$|f(z)|\le\frac{1+|z|}{1-|z|}(B+|f(0)|)+B.$$

化简得
$$
|f(z)|\le\frac{2|z|}{1-|z|}B+\frac{1+|z|}{1-|z|}|f(0)|.
$$

此即 $R=1$ 时的 Carathéodory 不等式. 对一般的 $R$, 用 $f(Rz)$ 代 $f(z)$, 得
$$
M(r)\le\frac{2r}{R-r}A(R)+\frac{R+r}{R-r}|f(0)|.
$$
___

>[!problem]
>Suppose $f(z)$ and $g(z)$ are analytic on $\overline{B(z_{0},r)}$ and neither function has a zero on $|z-z_{0}|=r$. Let $Z_{f}$ (respectively $Z_{g}$) denote the number of zeros of $f$ (respectively $g$) inside $|z-z_{0}|<r$, counting multiplicities. Show that if
>
>$$
>|f(z)+g(z)|<|f(z)|+|g(z)|,\quad |z-z_{0}|=r,
>$$
>
>then $Z_{f}=Z_{g}$.

**Solution:**
Let $h(z) = \frac{f(z)}{g(z)}$, which is analytic on a neighbourhood of the circle $|z-z_0| = r$ (since $g(z) \neq 0$ on the circle).  

The condition  
$$|f(z)+g(z)| < |f(z)|+|g(z)|, \quad |z-z_0| = r,$$  
implies that on the circle, we have  
$$f(z) \neq t\, g(z) \quad \text{for any real } t \geq 0.$$  
Equivalently, $h(z) = f(z)/g(z)$ never takes a non‑negative real value on $|z-z_0| = r$.

Thus $h(z)$ is positive on the circle, then  
$$
\Delta_{|z|=r}\mathrm{Arg}\,h(z)= 0.
$$
And by the argument principle,
$$
\Delta_{|z|=r}\mathrm{Arg}\,h(z)= \Delta_{|z|=r}\mathrm{Arg}\,f(z)-\Delta_{|z|=r}\mathrm{Arg}\,g(z)= Z_f - Z_g,
$$
Hence $Z_f - Z_g = 0$, i.e. $Z_f = Z_g$.
___

>[!problem]
>Let $D\subset\mathbb{C}$ be a domain and let $f(z)$ be an injective analytic function on $D$. Suppose the closed disk $B(a,\rho)$ is contained in $D$. For $w\in f(B(a,\rho))$, apply the residue theorem to prove the following formula for the inverse function $f^{-1}$ of $f$:
>
>$$
>f^{-1}(w)=\frac{1}{2\pi i}\int_{|\xi-a|=\rho}\frac{\xi f^{\prime}(\xi)}{f(\xi)-w}\,d\xi.
>$$

**Proof:**
Let $w \in f(B(a,\rho))$. Since $f$ is injective analytic, there is a unique $z_0 \in B(a,\rho)$ with $f(z_0)=w$, i.e., $z_0 = f^{-1}(w)$.

Consider the meromorphic function $F(\xi)=\dfrac{\xi f'(\xi)}{f(\xi)-w}$ on $|\xi-a|\leq \rho$.  
Its only singularity inside the disk is a simple pole at $\xi=z_0$ (because $f(\xi)-w$ has a simple zero at $\xi=z_0$, and $f'(z_0)\neq0$ since $f$ is injective).

Residue at $\xi=z_0$:
$$
\operatorname{Res}(F,z_0)=\lim_{\xi\to z_0}(\xi-z_0)\frac{\xi f'(\xi)}{f(\xi)-w}=z_0\frac{f'(z_0)}{f'(z_0)}=z_0.
$$
By the residue theorem,
$$
\frac{1}{2\pi i}\int_{|\xi-a|=\rho}F(\xi)\,d\xi=z_0=f^{-1}(w).
$$