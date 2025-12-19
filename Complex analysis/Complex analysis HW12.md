___

>[!problem] [GAM] V.5.2
>Suppose $f(z)$ is analytic at $\infty$, with series expansion
>$$
>f(z)=\sum_{k=0}^{\infty}\frac{b_{k}}{z^{k}}=b_{0}+\frac{b_{1}}{z}+\frac{b_{2}}{z^{2}}+\frac{b_{3}}{z^{3}}+\cdots,\quad|z|>\frac{1}{\rho}.
>$$
>With the notation $f(\infty)=b_{0}$ and $f^{\prime}(\infty)=b_{1}$, show that
>$$
>f^{\prime}(\infty)=\lim_{z\to\infty} z[f(z)-f(\infty)].
>$$

**Proof:**
Since $f(z)$ is analytic at $\infty$, we have
$$f(z)=b_0+\frac{b_1}{z}+O\left(\frac{1}{z^2}\right),\quad\text{as }z\to\infty.$$
Thus
$$z[f(z)-f(\infty)]=z\left[\left(b_0+\frac{b_1}{z}+O\left(\frac{1}{z^2}\right)\right)-b_0\right]=b_1+O\left(\frac{1}{z}\right).$$
Taking the limit as $z\to\infty$ gives
$$\lim_{z\to\infty}z[f(z)-f(\infty)]=b_1=f'(\infty).$$
Hence the formula is proven.
___

>[!problem] [GAM] VI.3.2
>Suppose that $f(z)$ is an entire function that is not a polynomial. What kind of singularity can $f(z)$ have at $\infty$?

**Solution:**
The entire function $f(z)$ has a Laurent expansion about $\infty$ (i.e., a power series in $1/z$). For an entire function, this expansion takes the form
$$
f(z)=\sum_{n=0}^{\infty} a_n z^n.
$$
Let $w=1/z$, then
$$
f(1/w)=\sum_{n=0}^{\infty} a_n w^{-n}.
$$

If $f$ is not a polynomial, then infinitely many $a_n$ for $n>0$ are non‑zero. Hence the expansion of $f(1/w)$ about $w=0$ contains infinitely many negative powers, which means $w=0$ (i.e., $z=\infty$) is an essential singularity of $f(1/w)$.

Therefore, $f(z)$ has an essential singularity at $\infty$.
___

>[!problem] [GAM] VI.3.3
>Show that if $f(z)$ is a nonconstant entire function, then $e^{f(z)}$ has an essential singularity at $z=\infty$.

**Proof:**
Assume for contradiction that $e^{f(z)}$ has a removable singularity or pole at $z=\infty$, then $e^{ f(z) }$ is meromorphic on $\hat{\mathbb{C}}$, thus $e^{ f(z) }$ must be a rational function. Since $e^{ f(z) }$ is an entire function, it must be a polynomial. A nonconstant polynomial must have a zero on $\mathbb{C}$, but $e^{ f(z) }\neq 0$, contradiction.

Therefore, $e^{f(z)}$ has an essential singularity at $z=\infty$.
___

>[!problem] [GAM] VI.3.4
>Show that each branch of the following function is meromorphic at $\infty$, and obtain the series expansion for each branch at $\infty$.
>$$
>\sqrt{z^{2}-\frac{1}{z}}
>$$

**Proof:**
Expansion of two branches:
$$
f(z)=z^2\sqrt{ 1-z^{-3} }=\pm z^2\cdot \sum_{k=0}^{\infty}\binom{1 /2}{n}\left( -z^{-3} \right)^k =\pm\sum_{k=0}^{\infty}\binom{1 /2}{n} (-z)^{2-3k}
$$
The principal part is $\pm z$ (a simple pole in $1/z$), so both branches is meromorphic at $\infty$ with a simple pole at $\infty$.
___

>[!problem] [GAM] VI.4.2
>Use the division algorithm to obtain the partial fractions decomposition of the following function.
>$$
>\frac{z^{6}}{(z^{2}+1)(z-1)^{2}}
>$$

**Solution:**
Let $q(z)=(z^{2}+1)(z-1)^{2}=z^{4}-2z^{3}+2z^{2}-2z+1$, then
$$
z^{6} = (z^{2}+2z+2)q(z) + (2z^{3}-z^2+2z-2),
$$
so $P_{\infty}(z)=z^{2}+2z+2$ and $r(z)=2z^{3}-z^2+2z-2$.

Partial‑fractions for $r(z)/q(z)$ (poles: $z=\pm i$, double pole at $z=1$):
$$
\frac{2z^{3}-z^2+2z-2}{(z^{2}+1)(z-1)^{2}}
= \frac{A}{z+i}+\frac{B}{z-i}+\frac{C}{z-1}+\frac{D}{(z-1)^{2}}.
$$
Multiply by $z+i$, set $z=-i$:
$$
A= \dfrac{2i+1-2i-2}{(-i-i)(-i-1)^2}= -\dfrac{1}{4}
$$
Multiply by $z-i$, set $z=i$:
$$
B= \dfrac{-2i+1+2i-2}{(i+i)(i-1)^2}= -\dfrac{1}{4}
$$
Multiply by $(z-1)^{2}$, set $z=1$:
$$
D=\frac{2-1+2-2}{1+1}= \dfrac{1}{2} .
$$
Differentiate after removing the factor for the double pole:
$$
C=\left.\frac{d}{dz}\!\left(\frac{2z^{3}-z^2+2z-2}{z^{2}+1}\right)\right|_{z=1}=- \dfrac{5}{4}.
$$
Therefore,
$$
\frac{z^{6}}{(z^{2}+1)(z-1)^{2}}
= z^{2}+2z+2-\frac{1}{4(z+i)}-\frac{1}{4(z-i)}-\frac{5}{4(z-1)}+\frac{1}{(z-1)^{2}}.
$$
___

>[!problem] [GAM] VII.1.1
>Evaluate the following residues.
>(d) $\operatorname{Res}\left[\dfrac{\sin z}{z^{2}},\,0\right]$
>
>(e) $\operatorname{Res}\left[\dfrac{\cos z}{z^{2}},\,0\right]$
>
>(g) $\operatorname{Res}\left[\dfrac{z}{\operatorname{Log}z},\,1\right]$

**Solution:**
**(d)** Expansion:
$$
\dfrac{\sin z}{z^2}=\dfrac{1}{z^2}\cdot(z- \dfrac{z^3}{6}+\cdots)=\dfrac{1}{z}- \dfrac{z}{6}+\cdots
$$
Thus $\operatorname{Res}\left[\dfrac{\sin z}{z^{2}},\,0\right]=1$.

**(e)** Expansion:
$$
\dfrac{\cos z}{z^2}=\dfrac{1}{z^2}\cdot(1- \dfrac{z^2}{2}+\cdots)=\dfrac{1}{z^2}- \dfrac{1}{2}+\cdots
$$
Thus $\operatorname{Res}\left[\dfrac{\cos z}{z^{2}},\,0\right]=0$.

**(g)** Since $1$ is a single zero of $\operatorname{Log}z$, we have
$$
\operatorname{Res}\left[\dfrac{z}{\log z},\,1\right]=\left. \dfrac{z}{(\operatorname{Log}z)'}\right|_{z=1}=1
$$
___

>[!problem] [GAM] VII.1.2
>Calculate the residue at each isolated singularity in the complex plane of the following functions.
>
>(b) $\tan z$
>
>(c) $\dfrac{z}{(z^{2}+1)^{2}}$

**Proof:**
**(b)** Since $\tan z= \dfrac{\sin{z}}{\cos{z}}$, the singularities are
$$
\pi /2 +k \pi,k\in \mathbb{Z}.
$$
And since $\pi /2 +k \pi,k\in \mathbb{Z}$ are single zeros of $\cos{z}$, we have
$$
\mathrm{Res}[ \dfrac{\sin{z}}{\cos{z}},\pi /2 +k \pi]=\left.\dfrac{\sin{z}}{(\cos{z})'}  \right|_{z=\pi /2 +k \pi} =-1.
$$
Therefore, the residue at any isolated singularity of $\tan z$ is $-1$.

**(c)** Find isolated singularities: $z^{2}+1=0$ gives $z = \pm i$, both are poles of order $2$.

At $z_0 = i$:
$$
\operatorname{Res}\left[  \dfrac{z}{(z^{2}+1)^{2}}, i \right]
= \lim_{z\to i} \frac{d}{dz}\!\left[ (z-i)^{2} \frac{z}{(z^{2}+1)^{2}} \right]
=\left. \frac{-z^{2}-1}{(z+i)^{4}} \right|_{z=i}=0 .
$$
Similarly, we also obtain
$$
\operatorname{Res}\left[  \dfrac{z}{(z^{2}+1)^{2}}, -i \right]
=0
$$
Therefore,
$$
\operatorname{Res}\!\left[\frac{z}{(z^{2}+1)^{2}},\; i\right] = 
\operatorname{Res}\!\left[\frac{z}{(z^{2}+1)^{2}},\; -i\right] = 0.
$$
___

>[!problem] [GAM] VII.1.3
>Evaluate the following integrals, using the residue theorem.
>
>(d) $\displaystyle \oint_{|z|=1}\frac{z^{4}}{\sin z}\,dz$
>
>(e) $\displaystyle \oint_{|z-1|=1}\frac{1}{z^{8}-1}\,dz$

**Solution:**
**(d)** Only $z=0$ satisfies $\sin z=0$ inside the unit circle, but $z=0$ is a removable singularity since $\lim_{ z \to 0 } \dfrac{z^4}{\sin z}=0$, also means the residue at $0$ is $0$.

By the residue theorem,
$$
\oint_{|z|=1}\frac{z^{4}}{\sin z}\,dz = 2\pi i \cdot 0 = 0.
$$
---

**(e)** Poles of $\dfrac{1}{z^{8}-1}$: $z^{8}-1=0 \Rightarrow z_k = e^{2\pi i k/8},\;k=0,1,\dots,7$, they are all simple poles. Among them only $z=1$, $z=e^{\pm i\pi/4}$ are inside the contour.

Compute residues:
$$
\operatorname{Res}\left[ \dfrac{1}{z^{8}-1} ,1\right]=\frac{1}{8\cdot1^{7}}=\frac{1}{8}.
$$
$$
\operatorname{Res}\left[\dfrac{1}{z^{8}-1} , e^{i\pi/4}\right]=\frac{1}{8\cdot(e^{i\pi/4})^{7}}=\frac{e^{i\pi/4}}{8}
$$
$$
\operatorname{Res}\left[ \dfrac{1}{z^{8}-1} ,e^{-i\pi/4}\right]=\frac{1}{8\cdot(e^{-i\pi/4})^{7}}=\frac{e^{-i\pi/4}}{8}
$$
By the residue theorem,
$$
\oint_{|z-1|=1}\frac{1}{z^{8}-1}\,dz
= 2\pi i \cdot \frac{1}{8} + \left( \frac{e^{i\pi/4}}{8} + \frac{e^{-i\pi/4}}{8}
 \right)
= \frac{\pi i}{4}\bigl(1+\sqrt{2}\bigr).
$$
___

>[!problem] [GAM] VII.1.5
>Let $f(z)$ be a meromorphic function on the complex plane that is doubly periodic, and suppose that none of the poles of $f(z)$ lie on the boundary of the period parallelogram $P$ constructed in Section VI.5. By integrating $f(z)$ around the boundary of $P$, show that the sum of the residues at the poles of $f(z)$ in $P$ is zero. Conclude that there is no doubly periodic meromorphic function with only one pole, a simple pole, in the period parallelogram.

**Proof:** Integrating $f(z)$ around the boundary of $P$ yields $0$. This is because, due to the double periodicity, the values of $f$ on opposite sides of the parallelogram are equal, but the orientations of opposite sides are opposite. Therefore, the integrals of falong opposite sides cancel each other out.

By the residue theorem, the integration around the boundary of $P$ equals to the sum of the residues at the poles of $f(z)$ in $P$, thus the sum equals $0$.

If there is only one simple pole in the period parallelogram, the sum of the residues at the poles of $f(z)$ in $P$ will equal to the residue of that simple pole, which is nonzero. Therefore, there is no doubly periodic meromorphic function with only one pole, a simple pole, in the period parallelogram.
___

>[!problem] [GAM] VII.1.6
>Consider the integral
>$$
>\int_{\partial D_{R}} \frac{e^{\pi i(z-1 / 2)^{2}}}{1-e^{-2 \pi i z}} d z,
>$$
>where $D_{R}$ is the parallelogram with vertices $\pm(\frac{1}{2}) \pm(1+i) R$.
>
>(a) Use the residue theorem to show that the integral is $(1+i) / \sqrt{2}$.
>
>(b) By parameterizing the sides of the parallelogram, show that the integral tends to
>$$
>(1+i) \int_{-\infty}^{\infty} e^{-2 \pi t^{2}} d t
>$$
>as $R \to \infty$.
>
>(c) Use (a) and (b) to show that
>$$
>\int_{-\infty}^{\infty} e^{-s^{2}} d s = \sqrt{\pi} .
>$$

**Proof:**
**(a)** Let $f(z)=\dfrac{e^{\pi i(z-1 / 2)^{2}}}{1-e^{-2 \pi i z}}$. Since $1-e^{-2\pi i z}=0$ implies $z$ is an integer and $e^{\pi i(z-1 / 2)^{2}}\neq 0$, $f(z)$ has poles at $z=k$, $k\in\mathbb{Z}$ (expansion of $e^z$ implies they are simple poles).

Inside the parallelogram $D_{R}$ with vertices $\pm\frac12\pm(1+i)R$, for $R$ large enough the only pole is $z=0$ (since $z=0$ lies inside, while other poles $z=\pm1,\pm2,\dots$ are outside for large $R$).  

Compute the residue at $z=0$:
Since the pole is simple,
$$
\operatorname{Res}[f,0]=\lim_{z\to0}z\,f(z)
 =\lim_{z\to0}\frac{z\,e^{\pi i(z-1/2)^{2}}}{1-e^{-2\pi i z}}=\frac{e^{i\pi/4}}{2\pi i}.
$$
Therefore, by the residue theorem,
$$
\int_{\partial D_{R}}f(z)\,dz = 2\pi i\cdot\operatorname{Res}[f,0]
 
 =\frac{1+i}{\sqrt2}.
$$

**(b)** The parallelogram $D_{R}$ has four vertices $A=-\frac12-(1+i)R$, $B=\frac12-(1+i)R$, $C=\frac12+(1+i)R$, $D=-\frac12+(1+i)R$. Parameterize the two slanted sides (parallel to $1+i$).  
On the right side $BC$: $z=\tfrac12-(1+i)R+(1+i)t$, $0\le t\le1$. Set $t-R=-s$, as $R\to\infty$, $s$ runs over $\mathbb{R}$. Then
$$z-\tfrac12=(1+i)(t-R)=-(1+i)s,$$
$$(z-\tfrac12)^2=-(1+i)^2s^2=-2is^2,$$
so $e^{\pi i(z-1/2)^2}=e^{-2\pi s^2}$.  
The denominator $1-e^{-2\pi i z}\to1$ as $R\to\infty$. The direction gives $dz=(1+i)ds$.  
Thus the integral on $BC$ tends to $(1+i)\int_{-\infty}^{\infty}e^{-2\pi s^2}ds$.  

The left side $DA$ gives the same contribution, while the horizontal sides $AB$ and $CD$ vanish because $e^{\pi i(z-1/2)^2}$ decays super‑exponentially there. Hence
$$\int_{\partial D_R}f(z)\,dz\;\longrightarrow\;(1+i)\int_{-\infty}^{\infty}e^{-2\pi t^{2}}dt\quad(R\to\infty).$$

**(c)** From (a) we have
$$
\int_{\partial D_{R}}f(z)\,dz=\frac{1+i}{\sqrt2}\quad\text{for all large }R.
$$
Hence, taking the limit $R\to\infty$ and using (b),
$$
\frac{1+i}{\sqrt2}=(1+i)\int_{-\infty}^{\infty}e^{-2\pi t^{2}}\,dt.
$$
Simplified to
$$
\frac{1}{\sqrt2}= \int_{-\infty}^{\infty}e^{-2\pi t^{2}}\,dt.
$$
Now set $s=t\sqrt{2\pi}$, so $ds=\sqrt{2\pi}\,dt$, and $e^{-2\pi t^{2}}=e^{-s^{2}}$. Then
$$
\int_{-\infty}^{\infty}e^{-2\pi t^{2}}\,dt
 =\frac{1}{\sqrt{2\pi}}\int_{-\infty}^{\infty}e^{-s^{2}}\,ds.
$$
Thus
$$
\frac{1}{\sqrt2}= \frac{1}{\sqrt{2\pi}}\int_{-\infty}^{\infty}e^{-s^{2}}\,ds,
$$
Therefore,
$$
\int_{-\infty}^{\infty}e^{-s^{2}}\,ds = \sqrt{\pi}.
$$
___

>[!problem]
>Let $f(z)$ and $g(z)$ be analytic functions at $z_{0}$.
>Suppose $z_{0}$ is a zero of order $n$ for $f(z)$, and a zero of order $m$ for $g(z)$.
>Show that:
>
>(a)  if $n>m$ then $z_{0}$ is a removable singularity of $\dfrac{f(z)}{g(z)}$ and after removing the singularity $z_{0}$ becomes a zero of order $n-m$;
>
>(b)  if $n=m$ then $z_{0}$ is a removable singularity of $\dfrac{f(z)}{g(z)}$ and $\displaystyle\lim_{z\to z_{0}}\frac{f(z)}{g(z)}\neq0$;
>
>(c)  if $n<m$ then $z_{0}$ is a pole of $\dfrac{f(z)}{g(z)}$ of order $m-n$.

**Proof.**  
Since $f(z)$ and $g(z)$ are analytic at $z_0$ and have zeros of orders $n$ and $m$ respectively, we can write
$$
f(z)=(z-z_0)^n\,F(z),\qquad
g(z)=(z-z_0)^m\,G(z),
$$
where $F(z)$ and $G(z)$ are analytic at $z_0$ and $F(z_0)\neq0$, $G(z_0)\neq0$.

Thus
$$
\frac{f(z)}{g(z)} = (z-z_0)^{\,n-m}\,\frac{F(z)}{G(z)},
\qquad \frac{F(z)}{G(z)}\ \text{analytic at }z_0,\ \frac{F(z_0)}{G(z_0)}\neq0.
$$

**(a)** If $n>m$, then $n-m>0$ and
$$
\frac{f(z)}{g(z)}=(z-z_0)^{\,n-m}\,H(z),
$$
with $H(z)=F(z)/G(z)$ analytic and $H(z_0)\neq0$.
Hence $f/g$ has a removable singularity at $z_0$ (after removing it, the value is $0$), and the resulting holomorphic function has a zero of order $n-m$ at $z_0$.

**(b)** If $n=m$, then
$$
\frac{f(z)}{g(z)}=\frac{F(z)}{G(z)},
$$
which is analytic at $z_0$ and satisfies
$$
\lim_{z\to z_0}\frac{f(z)}{g(z)}=\frac{F(z_0)}{G(z_0)}\neq0.
$$
Thus $z_0$ is a removable singularity of $f/g$, and the limit is a non‑zero constant.

**(c)** If $n<m$, then $n-m<0$; write $m-n>0$. Then
$$
\frac{f(z)}{g(z)}=(z-z_0)^{-(m-n)}\,\frac{F(z)}{G(z)},
$$
with $F(z)/G(z)$ analytic and non‑zero at $z_0$.  
Hence $f/g$ has a pole of order $m-n$ at $z_0$.
___

>[!problem]
>Let $f:\mathbb{C}\to\mathbb{C}$ be an entire function which is injective. Show that $f$ is of the form
>$$
>f(z)=az+b,\quad a\neq0,
>$$
>and deduce that $f$ is a bijective map from $\mathbb{C}$ to $\mathbb{C}$.
>
>Find all entire functions $f$ with $f(f(z))=z$ for any $z\in\mathbb{C}$.

**Proof:**
First, $f$ cannot have a removable singularity at $\infty$: if $f$ were bounded, by Liouville’s theorem it would be constant, contradicting injectivity.

 Second, $f$ cannot have an essential singularity at $\infty$. Suppose it did, then by the Casorati–Weierstrass theorem, in any neighbourhood of $\infty$, $f(z)$ takes values dense in $\mathbb{C}$. In particular, for the open unit disk $B(0,1)$, $f(B(0,1))$ is open (by the open mapping theorem) and non‑empty. Its complement $\mathbb{C}\setminus f(B(0,1))$ is not dense (since $f(B(0,1))$ is open). But if $f$ had an essential singularity at $\infty$, the image of the exterior of a large disk (i.e. a neighbourhood of $\infty$) would be dense, hence it would intersect $f(B(0,1))$. This would contradict injectivity, because two distinct points (one inside the disk, one outside) would be mapped to the same value. Therefore $\infty$ cannot be an essential singularity.

Hence $\infty$ is a pole of $f$. This means $f$ is a polynomial. If $\deg f\ge2$, then either $f$ has different roots (thus not injective) or has the form $(z-z_{0})^k$ (then $f=1$ will have different roots, thus also not injective). Therefore, $f$ has the form $f(z)=az+b$ ($a\neq{0}$ since $f$ is non-constant).

Such a linear function is clearly bijective on $\mathbb{C}$ (its inverse is $f^{-1}(w)=(w-b)/a$).

In conclusion, $f(z)=az+b$, $a\neq0$, and $f$ is a bijection from $\mathbb{C}$ to $\mathbb{C}$.

**Find all entire functions $f$ with $f(f(z))=z$ for any $z\in\mathbb{C}$:**
Note that $f\circ f=\operatorname{id}$ implies $f$ is injective: if $f(z_1)=f(z_2)$, applying $f$ gives $z_1=z_2$.  
By the statement above, any injective entire function is linear: $f(z)=az+b$ with $a\neq0$.

Now impose the condition $f(f(z))=z$:
$$
f(f(z))=a(az+b)+b=a^{2}z+ab+b=z\quad\text{for all }z.
$$
Thus
$$
a^{2}=1,\qquad ab+b=0.
$$
From $a^{2}=1$, $a=1$ or $a=-1$.

- If $a=1$, then $ab+b=b+b=2b=0\Rightarrow b=0$. Hence $f(z)=z$.
- If $a=-1$, then $ab+b=-b+b=0$ holds for any $b$. Thus $f(z)=-z+b$ with arbitrary $b\in\mathbb{C}$.

Therefore the only entire solutions of $f(f(z))=z$ are
$$
f(z)=z\qquad\text{or}\qquad f(z)=-z+b\;(b\in\mathbb{C}).
$$
___

>[!problem]
>Let $f$ be a meromorphic function on $\mathbb{C}$ which has a removable singularity or a pole at $\infty$. Let us view $f$ as a map from the extended complex plane $\widehat{\mathbb{C}}$ to itself. Show that if $f:\widehat{\mathbb{C}}\to\widehat{\mathbb{C}}$ is bijective (such an $f$ is called an automorphism of the extended complex plane $\widehat{\mathbb{C}}$), then $f$ is a fractional linear transformation.

**Proof:**
Since $f$ is bijective, we may assume $f(z_{0})=\infty$, then $f(z)\in \mathbb{C},\forall z\neq z_{0}$.

If $z_{0}=\infty$, then $f$ is an entire and bijective function restricted on $\mathbb{C}$. By the last problem $f$ is a linear transform (thus a fractional linear transformation).

If $z_{0}\neq \infty$, then $g(z)=f(z_{0}+1 /z)$ is an entire and bijective function restricted on $\mathbb{C}$. By the last problem $g$ is a linear transform. Suppose $g(z)=az+b,(a\neq 0)$, then
$$
f(z)=g\left(  \dfrac{1}{z-z_{0}}\right)= \dfrac{bz+a-bz_{0}}{z-z_{0}}
$$
is a linear transformation.

Therefore, an automorphism of the extended complex plane $\widehat{\mathbb{C}}$) is a fractional linear transformation.