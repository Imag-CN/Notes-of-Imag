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
Let $f(z)$ be a non‑constant entire function. Then $f(z)$ is either a polynomial of positive degree or a transcendental entire function.

**Case 1:** $f(z)$ is a polynomial of degree $n\ge 1$. Then
$$f(z)=a_n z^n + a_{n-1}z^{n-1}+\dots+a_0,\quad a_n\neq0.$$
Hence
$$e^{f(z)}=e^{a_n z^n}\,e^{a_{n-1}z^{n-1}+\dots+a_0}.$$
As $z\to\infty$, the factor $e^{a_n z^n}$ grows faster than any power of $z$ (if $a_n>0$) or oscillates wildly (if $a_n$ is not positive real). Consequently, $e^{f(z)}$ has an essential singularity at $\infty$.

*Case 2:* $f(z)$ is transcendental entire. Then $f(z)$ itself has an essential singularity at $\infty$ (see previous problem). The Great Picard theorem (or a simpler Casorati–Weierstrass argument) shows that $e^{f(z)}$ also has an essential singularity at $\infty$: for any $w\neq0$, the equation $e^{f(z)}=w$ has infinitely many solutions near $\infty$, which cannot happen for a pole or a removable singularity.

Alternatively, one can argue by contradiction: if $e^{f(z)}$ had a pole or a removable singularity at $\infty$, then $f(z)=\log e^{f(z)}$ would be meromorphic at $\infty$, hence a rational function. But a non‑constant rational function that is entire must be a polynomial, contradicting the transcendence of $f(z)$.

In both cases, $e^{f(z)}$ has an essential singularity at $\infty$.