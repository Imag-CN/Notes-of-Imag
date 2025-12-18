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
$\pi /2 +k \pi,k\in \mathbb{Z}$. And since $\pi /2 +k \pi,k\in \mathbb{Z}$ are single zeros of $\cos{z}$, we have
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

