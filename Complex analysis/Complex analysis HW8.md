___

>[!problem] Problem 1
>Show that the series $\sum_{n=1}^{\infty}\frac{z^{2n}}{1-z^{n}}$ converges normally in the open unit disk $\mathbb{D}:=\{z\in\mathbb{C}\mid|z|<1\}$.

**Proof:**
Take any $r$ with $0 < r < 1$. For any $|z| \leq r$, we have

$$\frac{|z|^{2n}}{|1-z|^n}\leq\frac{|z|^{2n}}{1-|z|^n} \leq \frac{|z|^{2n}}{1-|z|}\leq \frac{r^{2n}}{1-r}$$
The series $\sum_{n=1}^{\infty} \dfrac{r^{2n}}{1-r}$ converges (geometric series with ratio $r^2 < 1$).

By the Weierstrass M-test, the original series converges uniformly on closed disk $\overline{ B(0,r) }$, thus converges normally in $\mathbb{D}$.
___

>[!problem] Problem 2
>Show that the series 
>$$
>\sum_{n=1}^{\infty}\frac{1}{z^2-(2n+1)z+n(n+1)}
>$$
>converges normally in $\mathbb{C}-\mathbb{Z}_{\geq0}$, and determine the limit function. Does it converge uniformly in $\mathbb{C}-\mathbb{Z}_{\geq0}$?

**Proof:**
The partial sum $S_{N}(z)$ is
$$
\begin{align}
S_N(z) &= \sum_{n=1}^{N}\frac{1}{z^2-(2n+1)z+n(n+1)}\\
&=\sum_{n=1}^{N}\frac{1}{(z-n)(z-(n+1))}\\
&=\sum_{n=1}^{N}\frac{1}{z-(n+1)}-\frac{1}{z-n} \\
&=\frac{1}{z-(N+1)} - \frac{1}{z-1} 
\end{align}
$$
Then for any $z\in\mathbb{C}-\mathbb{Z}_{\geq0}$
$$\lim_{N\to\infty} S_N(z) = \frac{1}{z-1}  \lim_{N\to\infty}\frac{1}{z-(N+1)}-\frac{1}{z-1}  = -\frac{1}{z-1}$$
So the limit function is $f(z) =- \frac{1}{z-1}$.

Let $K \subset \mathbb{C}-\mathbb{Z}_{\geq0}$ be compact. Since $K$ is bounded, there exists $M>0$ such that for any $z\in K$, $|z|<M$. Then for any $z\in K$, take $N>M$, then
$$
|S_{N}(z)-f(z)|=\frac{1}{|z-(N+1)|}\leq \dfrac{1}{N+1-|z|}<\dfrac{1}{N+1-M}
$$
$\dfrac{1}{N+1-M}\to 0$ as $N\to \infty$, thus $S_{N}(z)$ convergent uniformly to $f(z)$ in $K$, so  $S_{N}(z)$ convergent normally to $f(z)$ in $\mathbb{C}-\mathbb{Z}_{\geq0}$.

Let $\epsilon=1$, then for any $N>0$, let $z=N+0.9$, then
$$
|S_{N}(z)-f(z)|=\frac{1}{|z-(N+1)|}=10>\epsilon
$$
Therefore, then series doesn't converge uniformly in $\mathbb{C}-\mathbb{Z}_{\geq0}$.
___

>[!problem] Problem 3
>In what domain $D \subset \mathbb{C}$ does the following series define an analytic function?
>
>(a) The series is
>$$
>\sum_{n=1}^{\infty} \frac{\sin(nz)}{2^n}.
>$$
>
>(b) The series is
>$$
>\sum_{n=1}^{\infty} \frac{\sin(nz)}{n^2}.
>$$

**Solution:**
Let $z=x+iy$, then $\sin(nz)=\sin(nx)\cosh(ny)+i\cos (nx)\sinh(ny)$.

**(a)**
For $|y|\geq \log 2$, $\sin(nx)$ and $\cos(nx)$ cannot be zero functions at the same time. W.L.O.G, suppose $\sin(nx)$ is not a zero function, then there are infinitely many $n\geq1$ such that $|\sin(nx)|>r$, where $r$ is a positive number. However, $\left|\dfrac{\cosh(ny)}{2^n} \right|> \dfrac{e^{n|y|}}{2\cdot 2^n} > \dfrac{1}{2}$, thus $\dfrac{\sin(nx)\cosh(ny)}{2^n} \not\to 0$, the series does convergent.

For $|y|<\log 2$, we have
$$
\begin{align}
\left| \dfrac{\sin(nz)}{2^n} \right| &= \dfrac{\sqrt{ \sin^2(nx)\cosh^2(ny)+\cos^2(nx)\sinh^2(ny) }}{2^n} \\
&\leq \dfrac{\sqrt{ \cosh^2(ny)+\sinh^2(ny) }}{2^n} \\
&=\dfrac{\sqrt{ \dfrac{e^{ 2ny }+e^{ -2ny }}{2} }}{2^n} \\
&\leq \dfrac{\sqrt{ e^{ 2n|y| } }}{2^n} \\
&=\left( \dfrac{e^{|y|}}{2} \right)^n 
\end{align}
$$
Since $0<\dfrac{e^{|y|}}{2}<1$, $\sum_{n\geq 1}\left( \dfrac{e^{|y|}}{2} \right)^n$ converges. By Weierstrass M-Test, the series converges uniformly. Considering $\dfrac{\sin(nz)}{2^n}$ is analytic, the series converges to an analytic function.

In conclusion, the original series define an analytic function on domain $\{ z: \left| \mathrm{Im}\,z \right|<\log 2\}$.
___
**(b)** 
For $y\neq0$, we suppose $\cos(nx)$ is a not zero function this time, then there are infinitely many $n\geq1$ such that $|\cos(nx)|>r$, where $r$ is a positive number. However, for sufficiently large $n$, we have $e^{n|y|}>2e^{-n|y|}$$\left| \dfrac{\sinh(ny)}{n^2} \right|> \dfrac{e^{n|y|}}{4\cdot n^2} \to +\infty$ as $n\to \infty$, thus $\dfrac{\cos(nx)\sinh(ny)}{n^2} \not\to 0$, the series does convergent.

Then the series doesn't converges in any domain, (because $y$ can be also $0$ in a domain). Therefore, the original series cannot define any analytic function in any domain.
___

>[!problem] Problem 4
>Let $\{z_n\}_{n=1}^\infty$ be a sequence of complex numbers. We say that the product
>$$
>\prod_{n=1}^\infty (1 + z_n)
>$$
>converges if the limit
>$$
>\lim_{N \to \infty} \prod_{n=1}^N (1 + z_n)
>$$
>of the partial products exists. Now suppose the series $\sum_{n=1}^\infty z_n$ converges absolutely. Show that the product $\prod_{n=1}^\infty (1 + z_n)$ converges.

**Proof:**
Since $\sum_{n=1}^\infty z_n$ converges, we can assume $|z_{n}|<1/3$ for there are only finitely many $z_{n}$ such that $|z_{n}|\geq 1/3$.

$$
\prod_{n=1}^N (1 + z_n)= \prod_{n=1}^N \exp{(\operatorname{Log}(1 + z_n))}=\exp \left( \sum_{n=1}^{N}\operatorname{Log}(1 + z_n) \right)
$$
Since $\exp$ is a continuous function, it is sufficient to show
$$
\lim_{N \to \infty}\left( \sum_{n=1}^{N}\operatorname{Log}(1 + z_n) \right)
$$
exist, i.e. $\sum_{n=1}^{+\infty}\operatorname{Log}(1 + z_n)$ converges.

Let $z_{n}=x_{n}+iy_{n}$, then since $|z_{n}|<1/3$, we have $|x_{n}|,|y_{n}|<1/3$; and since $\sum_{n=1}^\infty z_n$ converges absolutely, we have $\sum_{n=1}^\infty x_n,\sum_{n=1}^\infty y_n$ converges absolutely.

We have
$$\operatorname{Log}(1 + z_n)=\dfrac{1}{2}\log((1+x_{n})^2+y_{n}^2)+i\arctan \dfrac{y_{n}}{1+x_{n}}.$$

$\log((1+x_{n})^2+y_{n}^2)\leq 2x_{n}+x_{n}^2+y_{n}^2\leq2|x_{n}|+x_{n}^2+y_{n}^2<3|x_{n}|+|y_{n}|$, and $\log((1+x_{n})^2+y_{n}^2)\geq - \dfrac{2x_{n}+x_{n}^2+y_{n}^2}{1-(2x_{n}+x_{n}^2+y_{n}^2)}\geq- \dfrac{2x_{n}+x_{n}^2+y_{n}^2}{1 /9}\geq-9(3|x_{n}|+|y_{n}|)$, so $\sum_{n=1}^{\infty}\dfrac{1}{2}\log((1+x_{n})^2+y_{n}^2)$ converges.

$\left| \arctan \dfrac{y_{n}}{1+x_{n}} \right|=\arctan \dfrac{|y_{n}|}{1+x_{n}}\leq\dfrac{|y_{n}|}{1+x_{n}}\leq 2|y_{n}|$, so $\sum_{n=1}^{\infty}\arctan \dfrac{y_{n}}{1+x_{n}}$ converges.

Therefore, $\sum_{n=1}^{\infty}\operatorname{Log}(1 + z_n)$ converges. Hence we have done the proof.

