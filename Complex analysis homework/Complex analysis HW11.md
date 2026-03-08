___

>[!problem] [GAM] V.5.1
>Expand the following functions in power series about $\infty$:
>
>(a) $\frac{1}{z^{2}+1}$
>
>(c) $e^{1/z^{2}}$

**Solution:** 
**(a)** Use geometric series:
$$\frac{1}{z^2+1} =\frac{z^{-2}}{1+z^{-2}}= z^{-2}\sum_{n=0}^{\infty}{(-z^2)^{n}}=\sum_{n=1}^{\infty}\frac{(-1)^{n-1}}{z^{2n}} .$$
**(c)** Let $w = 1/z^2$. Then $e^{1/z^2} = e^{w}$, which has the Taylor expansion about $w=0$ valid for all $w$ (i.e., $z \neq 0$):
$$e^{w} = \sum_{n=0}^{\infty} \frac{w^n}{n!}.$$
Hence,
$$e^{1/z^2} = \sum_{n=0}^{\infty} \frac{1}{n! \, z^{2n}}.$$
___

>[!problem] [GAM] VI.2.1
>Find the isolated singularities of the following functions, and determine whether they are removable, essential, or poles. Determine the order of any pole, and find the principal part at each pole.
>
>(c) $\frac{e^{2z}-1}{z}$
>
>(e) $z^{2}\sin (\frac{1}{z})$
>
>(h) $\frac{\mathrm{Log}\, z}{(z-1)^{3}}$

**Solution:**
**(c)** Isolated singularity: $z = 0$.
Since $\lim_{z \to 0} f(z) = \lim_{z \to 0} \frac{2z + O(z^2)}{z} = 2$ exists and is finite, $z=0$ is a removable singularity.

**(e)** Isolated singularity: $z = 0$.
Using the Laurent expansion:
$$
f(z) = z^{2} \left( \frac{1}{z} - \frac{1}{3! z^{3}} + \frac{1}{5! z^{5}} - \cdots \right) = z - \frac{1}{6z} + \frac{1}{120 z^{3}} - \cdots
$$
The Laurent series contains infinitely many negative powers of $z$. Therefore, $z=0$ is an essential singularity.

**(h)** Isolated singularity: $z=1$.
Expand $\mathrm{Log}\, z$ about $z=1$: 
$$
\mathrm{Log\,} z = (z-1) - \frac{(z-1)^{2}}{2} + \frac{(z-1)^{3}}{3} - \cdots
$$
Then,
$$
f(z)  = \frac{1}{(z-1)^{2}} - \frac{1}{2(z-1)} + \frac{1}{3} - \cdots
$$
The highest negative power is $(z-1)^{-2}$. Therefore, $z=1$ is a pole of order $2$, and principal part: $\frac{1}{(z-1)^{2}} - \frac{1}{2(z-1)}$.
___

>[!problem] [GAM] VI.2.3
>Consider the function $f(z) = \tan z$ in the annulus $\{3 < |z| < 4\}$. Let $f(z)=f_{0}(z)+f_{1}(z)$ be the Laurent decomposition of $f(z)$, so that $f_{0}(z)$ is analytic for $|z|<4$, and $f_{1}(z)$ is analytic for $|z|>3$ and vanishes at $\infty$.
>
>(a) Obtain an explicit expression for $f_{1}(z)$.
>
>(b) Write down the series expansion for $f_{1}(z)$, and determine the largest domain on which it converges.
>
>(c) Obtain the coefficients $a_{0}$, $a_{1}$, and $a_{2}$ of the power series expansion of $f_{0}(z)$.
>
>(d) What is the radius of convergence of the power series expansion for $f_{0}(z)$?

**Solution:**
**(a)** Poles of $\tan z$ inside $|z| < 4$ are at $z = \pm \pi/2$, and
$$
\lim_{ z \to \pm\pi /2 } (z\mp \pi /2)\tan z=-1. 
$$
Thus the function $f_1(z)$ is the sum of their principal parts:
$$
f_1(z) = -\frac{1}{z-\pi/2} - \frac{1}{z+\pi/2} = -\frac{2z}{z^2 - (\pi/2)^2}.
$$

**(b)** For $|z| > \pi/2$, expand as a Laurent series:
$$
f_1(z) = -\sum_{n=0}^{\infty} \frac{2(\pi/2)^{2n}}{z^{2n+1}}.
$$
The series converges for $|z| > \pi/2$.

**(c)** $f_0(z) = f(z) - f_1(z)$ is analytic for $|z| < 4$. Its Taylor series at $z=0$ is computed from $\tan z = z + z^3/3 + 2z^5/15 + \cdots$ and the expansion of $f_1(z)$ in powers of $z$ (valid near $0$):
$$
f_1(z) = -\frac{8z}{\pi^2} - \frac{32z^3}{\pi^4} - \frac{128z^5}{\pi^6} + \cdots.
$$
Thus,
$$
f_0(z) = \left(1 - \frac{8}{\pi^2}\right)z + \left(\frac{1}{3} - \frac{32}{\pi^4}\right)z^3 + \left(\frac{2}{15} - \frac{128}{\pi^6}\right)z^5 + \cdots.
$$
So
$$
a_0 = 0,\quad a_1 = 1 - \frac{8}{\pi^2},\quad a_2 = 0.
$$

**(d)** The nearest singularities of $f_0(z)$ are the poles of $\tan z$ that are not removed, i.e., at $z = \pm 3\pi/2$. The distance from $0$ to these points is $3\pi/2$. Hence the radius of convergence is $R = \frac{3\pi}{2}$.
___

>[!problem] [GAM] VI.2.4
>Suppose $f(z)$ is meromorphic on the disk $\{ |z|<s\}$, with only a finite number of poles in the disk. Show that the Laurent decomposition of $f(z)$ with respect to the annulus $\{ s-\varepsilon<|z|<s\}$ has the form $f(z)=f_{0}(z)+f_{1}(z)$, where $f_{1}(z)$ is the sum of the principal parts of $f(z)$ at its poles.

**Proof:**
Let the poles of $f(z)$ in the disk $|z| < s$ be $p_1, p_2, \dots, p_m$, with corresponding principal parts $P_k(z)$ at $z = p_k$, where each $P_k(z)$ is a finite sum of negative powers of $(z - p_k)$.

Define
$$
f_1(z) = \sum_{k=1}^m P_k(z).
$$
Then $f_1(z)$ is a rational function whose poles are exactly $\{p_1, \dots, p_m\}$, and it is analytic for $|z| > \max_k |p_k|$.

Now define
$$
f_0(z) = f(z) - f_1(z).
$$
Since $f(z)$ and $f_1(z)$ are both meromorphic in $|z| < s$, so is $f_0(z)$. Moreover, at each pole $p_k$, the principal part of $f$ is exactly cancelled by the corresponding term in $f_1$, so $f_0$ has at most a removable singularity at $p_k$. After removing these singularities, $f_0$ becomes analytic in the whole disk $|z| < s$.

Consider the annulus $A = \{ s-\varepsilon < |z| < s \}$. Choose $\varepsilon=s - \max_k |p_k|$ small so that $s - \varepsilon=\max_k |p_k|$. Then in $A$:
* $f_1(z)$ is analytic on $|z| > s - \varepsilon$ (since all its poles satisfy $|p_k| < s - \varepsilon$), and
* $f_0(z)$ is analytic on $|z| < s$.

Therefore, on $A$, we have a decomposition $f(z) = f_0(z) + f_1(z)$ with $f_0$ analytic for $|z| < s$ and $f_1$ analytic for $|z| > s - \varepsilon$ (and vanishing at $\infty$).
___

>[!problem] [GAM] VI.2.6
>Show that if $f(z)$ is continuous on a domain $D$, and if $f(z)^{8}$ is analytic on $D$, then $f(z)$ is analytic on $D$.

**Proof:** This is a special case of [GAM] V.7.10, which was already assigned last time.
___

>[!problem] [GAM] VI.2.8
>A meromorphic function $f$ at $z_{0}$ is said to have order $N$ at $z_{0}$ if $f(z)=(z-z_{0})^{N}g(z)$ for some analytic function $g$ at $z_{0}$ such that $g(z_{0})\neq 0$. The order of the function $0$ is defined to be $+\infty$. Show that
>
>(a) $\operatorname{order}(fg,z_{0})=\operatorname{order}(f,z_{0})+\operatorname{order}(g,z_{0})$,
>
>(b) $\operatorname{order}(1/f,z_{0})=-\operatorname{order}(f,z_{0})$,
>
>(c) $\operatorname{order}(f+g,z_{0}) \geq \min\{\operatorname{order}(f,z_{0}),\operatorname{order}(g,z_{0})\}$.
>
>Show that strict inequality can occur in (c), but that equality holds in (c) whenever $f$ and $g$ have different orders at $z_{0}$.

**Proof:** 
Denote $\operatorname{ord}(f) = \operatorname{order}(f, z_0)$.

**(a)** Let $\operatorname{ord}(f) = m$, $\operatorname{ord}(g) = n$. Then
$$f(z) = (z-z_0)^m F(z),\quad g(z) = (z-z_0)^n G(z),$$
where $F$ and $G$ are analytic at $z_0$ with $F(z_0) \neq 0$, $G(z_0) \neq 0$.
Thus
$$
f(z)g(z) = (z-z_0)^{m+n} [F(z)G(z)],
$$
and $H(z) = F(z)G(z)$ is analytic at $z_0$ with $H(z_0) = F(z_0)G(z_0) \neq 0$.
Hence $\operatorname{ord}(fg) = m+n = \operatorname{ord}(f) + \operatorname{ord}(g)$.

**(b)** If $\operatorname{ord}(f) = m$, write $f(z) = (z-z_0)^m F(z)$ as above. Then
$$
\frac{1}{f(z)} = (z-z_0)^{-m} \frac{1}{F(z)}.
$$
Since $1/F(z)$ is analytic near $z_0$ (because $F(z_0)\neq 0$) and nonzero at $z_0$, we have $\operatorname{ord}(1/f) = -m = -\operatorname{ord}(f)$.

If $f \equiv 0$, $\operatorname{ord}(0) = +\infty$ and $1/0$ is undefined. We can define $1 /0=\infty$ and $\operatorname{ord}(\infty) = -\infty$).

**(c)** Let $\operatorname{ord}(f) = m$, $\operatorname{ord}(g) = n$, and assume (without loss of generality) that $m \le n$.
Then
$$
f(z) = (z-z_0)^m F(z),\quad g(z) = (z-z_0)^n G(z) = (z-z_0)^m \cdot (z-z_0)^{n-m} G(z),
$$
with $F$, $G$ analytic and nonzero at $z_0$. Hence
$$
f(z)+g(z) = (z-z_0)^m \left[ F(z) + (z-z_0)^{n-m} G(z) \right].
$$
Let $h(z) = F(z) + (z-z_0)^{n-m} G(z)$, then $h$ is analytic at $z_0$, so $\operatorname{ord}(h) \geq 0$. Thus
$$
\operatorname{ord}(f(z)+g(z))  = \operatorname{ord}((z-z_0)^m h(z))=\operatorname{ord}((z-z_0)^m)+\operatorname{ord}( h(z))
$$
$$
=m+\operatorname{ord}( h(z))\geq m=\min\{ \operatorname{ord}( f(z)),\operatorname{ord}( g(z)) \}
$$
Therefore, $\operatorname{ord}(f+g)\geq \min\{ \operatorname{ord}( f),\operatorname{ord}( g) \}$.

If $m\neq n$, i.e. $f$ and $g$ have different orders at $z_{0}$, then $(z-z_0)^{n-m}=0$ if $z=z_{0}$, thus $h(z_0) = F(z_0)\neq 0$. In this case $\operatorname{ord}(f+g) = m$, the equality always holds.

Strict inequality example:
Take $f(z)=z$, $g(z)=-z$ at $z_0=0$. Then $\operatorname{ord}(f)=\operatorname{ord}(g)=1$, but $f(z)+g(z)\equiv 0$, so $\operatorname{ord}(f+g)=+\infty > 1$.
___

>[!problem] [GAM] VI.2.9
>Recall that “$f(z) = O(h(z))$ as $z \to z_0$” means that there is a constant $C$ such that $|f(z)| \leq C|h(z)|$ for $z$ near $z_{0}$. Show that if $z_{0}$ is an isolated singularity of an analytic function $f(z)$, and if $f(z)=O((z-z_{0})^{m})$ as $z \to z_{0}$, then the Laurent coefficients of $f(z)$ are $0$ for $k < m$, that is, the Laurent series of $f(z)$ has the form
>
>$$ f(z)=a_{m}(z-z_{0})^{m}+a_{m+1}(z-z_{0})^{m+1}+\cdots. $$

**Proof:**
Let $f(z)$ be analytic in a punctured disk $0 < |z - z_0| < R$, with Laurent expansion
$$
f(z) = \sum_{k=-\infty}^{\infty} a_k (z - z_0)^k.
$$
The coefficients are given by
$$
a_k = \frac{1}{2\pi i} \int_{|\zeta - z_0| = r} \frac{f(\zeta)}{(\zeta - z_0)^{k+1}} \, d\zeta, \quad 0 < r < R.
$$

By hypothesis, there exists $C > 0$ and $\delta > 0$ such that
$$
|f(z)| \leq C |z - z_0|^m \quad \text{for } 0 < |z - z_0| < \delta.
$$
Fix $r$ with $0 < r < \min\{R, \delta\}$. Then for $k < m$, we estimate
$$
\begin{aligned}
|a_k| 
&= \left| \frac{1}{2\pi i} \int_{|\zeta - z_0| = r} \frac{f(\zeta)}{(\zeta - z_0)^{k+1}} \, d\zeta \right| \\
&\leq \frac{1}{2\pi} \int_{|\zeta - z_0| = r} \frac{|f(\zeta)|}{|\zeta - z_0|^{k+1}} \, |d\zeta| \\
&\leq \frac{1}{2\pi} \int_{|\zeta - z_0| = r} \frac{C |\zeta - z_0|^m}{r^{k+1}} \, |d\zeta| \\
&= \frac{C r^m}{2\pi r^{k+1}} \cdot 2\pi r \\
&= C r^{m-k}.
\end{aligned}
$$
Since $m - k > 0$, letting $r \to 0^+$ shows that $a_k = 0$ for each $k < m$.

Therefore, the Laurent series of $f(z)$ has the form
$$
f(z) = a_m (z - z_0)^m + a_{m+1} (z - z_0)^{m+1} + \cdots.
$$
___

>[!problem] [GAM] VI.2.11
>Suppose $f(z)=\sum a_{k}z^{k}$ is analytic for $|z|<R$, and suppose that $f(z)$ extends to be meromorphic for $|z|<R+\varepsilon$, with only one pole $z_{0}$ on the circle $|z|=R$. Show that $a_{k}/a_{k+1}\to z_{0}$ as $k\to\infty$.

**Proof:**
Denote the order of the pole at $z_0$ by $p \ge 1$. Write $f(z)$ as the sum of its principal part at $z_0$ and a function analytic in $|z| < R+\varepsilon$:
$$
f(z) = \frac{P(z)}{(z - z_0)^p} + h(z),
$$
where $P(z)$ is a polynomial of degree $< p$ and $h(z)$ is analytic for $|z| < R+\varepsilon$.

For $|z| < |z_0| = R$, we can expand
$$
\frac{1}{(z - z_0)^m} = \frac{(-1)^m}{z_0^m} \cdot \frac{1}{(1 - z/z_0)^m}
   = \frac{(-1)^m}{z_0^m} \sum_{k=0}^\infty \binom{m-1+k}{m-1} \left(\frac{z}{z_0}\right)^k.
$$
Since $P(z)$ is a polynomial, the principal part $\frac{P(z)}{(z - z_0)^p}$ has a power series $\sum d_k z^k$ whose coefficients satisfy
$$
d_k = C \, z_0^{-k} \, k^{\,p-1} + o\big(z_0^{-k} k^{\,p-1}\big) \quad (k \to \infty),
$$
where $C \neq 0$ is a constant depending on $P$ and $p$.

The function $h(z) = \sum B_k z^k$ is analytic in $|z| < R+\varepsilon$; hence its radius of convergence is larger than $R$. Consequently,
$$
\limsup_{k\to\infty} |B_k|^{1/k} \le \frac{1}{R+\delta} \quad \text{for some } \delta > 0,
$$
which implies $B_k = o(R^{-k})$.

Since $f(z) = \frac{P(z)}{(z - z_0)^p} + h(z)$, we have $a_k = d_k + B_k$. Using the estimates above,
$$
a_k = C \, z_0^{-k} \, k^{\,p-1} \big(1 + o(1)\big) \quad \text{as } k \to \infty.
$$

Thus:
$$
\frac{a_k}{a_{k+1}}= \frac{C \, z_0^{-k} \, k^{\,p-1} \big(1 + o(1)\big)}
{C \, z_0^{-k-1} \, (k+1)^{\,p-1} \big(1 + o(1)\big)}= z_0 \cdot \left(\frac{k}{k+1}\right)^{\!p-1} \cdot \frac{1 + o(1)}{1 + o(1)}
\longrightarrow z_0
$$
as $k \to \infty$.

Therefore, $\displaystyle \lim_{k\to\infty} \frac{a_k}{a_{k+1}} = z_0$.
___

>[!problem] [GAM] VI.2.13
>Let $S$ be a sequence converging to a point $z_{0}\in C$, and let $f(z)$ be analytic on some disk centered at $z_{0}$ except possibly at the points of $S$ and at $z_{0}$.
>
>Show that either $f(z)$ extends to be meromorphic on some neighborhood of $z_{0}$, or else for any complex number $L$ there is a sequence $\{w_{j}\}$ such that $w_{j}\to z_{0}$ and $f(w_{j})\to L$.

**Proof:** Since $S$ be a sequence converging to a point $z_{0}\in C$, every point in $S$ is an isolated singularity. Suppose $f(z)$ is analytic on $D$.

**Case 1:** $\exists p \in \mathbb{N},s.t.(z-z_{0})^pf(z)$ is bounded in $D \cap B(z_{0},r)$, where $B(z_{0},r)$ is some neighborhood of $z_{0}$.

By Riemann's removable singularity theorem, every point in $S$ and $B(z_{0},r)$ is a removable singularity. Thus $(z-z_{0})^pf(z)$ can be extended to be analytic on $B(z_{0},r)\setminus \{ z_{0} \}$ . Then $z_{0}$ becomes an isolated singularity. Applying Riemann's removable singularity theorem again gives that $(z-z_{0})^pf(z)$ can be extended to be analytic on $B(z_{0},r)$ .

Therefore, $f(z)$ can be extended to be meromorphic on $B(z_{0},r)$.

**Case 2:** $\forall p \in \mathbb{N},(z-z_{0})^pf(z)$ is not bounded in $D \cap B(z_{0},r)$, where $B(z_{0},r)$ is any neighborhood of $z_{0}$.

For any $L\in \mathbb{C}$, assume for contradiction that for any sequence $\{w_{j}\}$ such that $w_{j}\to z_{0}$, we have $f(w_{j})\not \to L$. Then $\exists \epsilon,\delta>0,s.t.\forall z\in D \cap B(z_{0},\delta),|f(z)-L|>\epsilon$. Let $g(z)=\dfrac{1}{f(z)-L}$, then $|g(z)|<1/\epsilon$ on $D \cap B(z_{0},\delta)$. Since $g(z)$ is bounded on $D \cap B(z_{0},\delta)$, by case 1 we know that $g(z)$ can be extended to be analytic on $B(z_{0},\delta)$. We can restrict $g(z)$ to a smaller neighborhood $B(z_{0},l)$ to assure that $g(z)\neq0$ except possibly when $z=z_0$ according to the isolation of zeros of analytic functions. Suppose $z=z_{0}$ is a zero of $g(z)$ with order $m$ (here we allow $m$ to be $0$, representing that $g(z_{0})\neq0$), then $\dfrac{(z-z_{0})^m}{g(z)}=(z-z_{0})^m(f(z)-L)$ is analytic on $B(z_{0},l)$. However, $(z-z_{0})^m(f(z)-L)$ is not bounded on $B(z_{0},l)$ based on the classification criterion, contradiction.

Therefore, for any complex number $L$ there is a sequence $\{w_{j}\}$ such that $w_{j}\to z_{0}$ and $f(w_{j})\to L$.
___

>[!problem]
>Let $f(z)$ be an analytic function in the strip
>
>$$ S = \{ z \in \mathbb{C} \mid a < \operatorname{Im} z < b \} \quad (-\infty \leq a < b \leq +\infty) $$
>
>which is $1$-periodic (namely, $f(z+1)=f(z)$ for any $z \in S$). Show that $f(z)$ can be expressed as a normally convergent complex Fourier series
>
>$$ f(z) = \sum_{n=-\infty}^{\infty} a_{n} e^{2\pi i n z} $$
>
>with the Fourier coefficient $a_{n}$ given by the following formula
>
>$$ a_{n} = \int_{iy}^{1+iy} f(z) e^{-2\pi i n z} \, dz $$
>
>where $y$ is arbitrarily chosen in $(a,b)$.

**Proof:**
Consider the transformation $\zeta = e^{2\pi i z}$, which maps the strip
$$
S = \{z \in \mathbb{C} : a < \operatorname{Im} z < b\}
$$
onto the annulus
$$
A = \{\zeta \in \mathbb{C} : e^{-2\pi b} < |\zeta| < e^{-2\pi a}\}.
$$
If $a = -\infty$ (resp. $b = +\infty$), the corresponding bound becomes $0$ (resp. $+\infty$), so $A$ is a punctured disk (resp. the exterior of a disk).

The function $f(z)$ is $1$-periodic, so it descends to a well-defined function $g$ on the annulus $A$ via
$$
g(\zeta) = f\!\left(\frac{\log \zeta}{2\pi i}\right),
$$
where any branch of the logarithm can be used because $f$ is $1$-periodic.

Moreover, $f$ is analytic on $S$, and the map $z \mapsto \zeta$ is locally biholomorphic, so $g(\zeta)$ is analytic on $A$.

Since $g$ is analytic on the annulus $A$, it admits a Laurent expansion that converges normally on $A$:
$$
g(\zeta) = \sum_{n=-\infty}^{\infty} a_n \zeta^{\,n}, \qquad \zeta \in A.
$$
The Laurent coefficients are given by
$$
a_n = \frac{1}{2\pi i} \int_{|\zeta|=r} \frac{g(\zeta)}{\zeta^{\,n+1}} \, d\zeta,
$$
where $r$ is any radius satisfying $e^{-2\pi b} < r < e^{-2\pi a}$.

Now change variables back to $z$. Substitute $\zeta = e^{2\pi i z}$ and choose the path $\gamma_y: [0,1] \to S$ defined by $\gamma_y(t) = t + iy$ for a fixed $y \in (a,b)$. Then $|\zeta| = e^{-2\pi y}$ is constant, and $d\zeta = 2\pi i e^{2\pi i z} dz = 2\pi i \zeta \, dz$. The coefficient formula becomes
$$
\begin{aligned}
a_n &= \frac{1}{2\pi i} \int_{|\zeta|=e^{-2\pi y}} \frac{f(z)}{\zeta^{\,n+1}} \, d\zeta \\
&= \frac{1}{2\pi i} \int_{iy}^{1+iy} \frac{f(z)}{e^{2\pi i (n+1)z}} \cdot 2\pi i e^{2\pi i z} \, dz \\
&= \int_{iy}^{1+iy} f(z) e^{-2\pi i n z} \, dz.
\end{aligned}
$$

Finally, substituting $\zeta = e^{2\pi i z}$ back into the Laurent series for $g$ gives
$$
f(z) = g(e^{2\pi i z}) = \sum_{n=-\infty}^{\infty} a_n e^{2\pi i n z},
$$
and the convergence is normal on $S$ because the Laurent series converges normally on $A$ and the map $z \mapsto e^{2\pi i z}$ is a local biholomorphism.