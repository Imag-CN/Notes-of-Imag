___
> [!problem]
> Show that
> $$f(x) = \sum_{p=1}^\infty \frac{1}{p^2} \sin \left[ (2^{p^3} + 1) \frac{|x|}{2} \right],x \in[-\pi,\pi]$$
> is continuous, but has divergent Fourier series.

**Proof:** 
According to Weierstrass M-test, the series converges uniformly, thus $f$ is continuous.

As $f$ is even, the $b_n$ are all vanishing. Denote
$$
\lambda_{n,m}=\int_0^{\pi} \sin \left[ (2m + 1) \frac{t}{2} \right] \cos nt \ dt\quad \text{and} \quad\sigma_{n,m} = \sum_{k=0}^n \lambda_{k,m},
$$
then we will have:
$$ \begin{aligned} a_n &= \frac{2}{\pi} \int_0^{\pi} f(t) \cos nt \ dt\\
&= \frac{2}{\pi} \int_0^{\pi} \left(\sum_{p=1}^\infty \frac{1}{p^2} \sin \left[ (2^{p^3} + 1) \frac{x}{2} \right] \cos nt\right) \ dt\\
&=\frac{2}{\pi} \sum_{p=1}^\infty \frac{1}{p^2} \int_0^{\pi} \sin \left[ (2^{p^3} + 1) \frac{x}{2} \right] \cos nt \ dt\\
&=\frac{2}{\pi} \sum_{p=1}^\infty \frac{1}{p^2} \lambda_{n,2^{p^3-1}} \end{aligned}
$$
The $\int$ and $\sum$ signs can be switched because the series is uniformly convergent (by Weierstrass M-test).

Let $S_{n}$ be $\pi /2$ times of the Fourier series Let $S_n$​ be the value at $x=0$ of the $n$-th partial sum of the Fourier series of times $\dfrac{\pi}{2} \cdot f(x)$, then
$$
S_n = \frac{\pi}{2} \sum_{k=0}^n a_k = \sum_{p=1}^\infty \sum_{k=0}^n \frac{1}{p^2} \lambda_{k,2^{p^3-1}} =\sum_{p=1}^\infty \frac{1}{p^2} \sigma_{n,2^{p^3-1}}
$$
It is sufficient to show that $S_{n}$ diverges as $n\to \infty$. 

We have
$$
\lambda_{n,m} =\frac{m+1/2}{(m+1/2)^2-n^2}=\dfrac{1}{2}\cdot \ \left(\frac{1}{m+n+1/2}+\frac{1}{m-n+1/2}\ \right) .
$$
Therefore for $n \le m$ we get $\lambda_{n,m} \ge 0$ and $\sigma_{q,m} \ge 0$ for $q \le m$. While for $q \ge m$:
$$
\begin{aligned} 2 \sigma_{q,m} &= \sum_{k=0}^q \left(\frac{1}{m+k+1/2}+\frac{1}{m-k+1/2}\right)\\ &=\sum_{i=m}^{q+m} \frac{1}{i+1/2} + \sum_{i=m}^{m-q} \frac{1}{i+1/2}\\ &= \sum_{i=m}^{q+m} \frac{1}{i+1/2} + \frac{1}{m+1/2} + \sum_{i=m-q}^{m-1} \frac{1}{i+1/2}\\ &= \frac{1}{m+1/2} + \sum_{i=q-m}^{q+m} \frac{1}{i+1/2} \ge 0 \end{aligned}
$$
And for $q=m$:
$$
\begin{aligned} 2 \sigma_{m,m} &= \frac{1}{m+1/2} + \sum_{i=0}^{2m} \frac{1}{i+1/2}\\
&= \frac{1}{m+1/2}+\sum_{i=0}^{2m} \int_{i+1/2}^{i+3/2} \frac{dt}{i+1 /2}\\
&\ge \sum_{i=0}^{2m} \int_{i+1/2}^{i+3/2} \frac{dt}{t} = \int_{1/2}^{2m+3/2} \frac{dt}{t}\\ &= \ln(4m+3) \ge \ln m \end{aligned}
$$
Therefore,
$$
S_{2^{p^3-1}} \ge \frac{1}{p^2} \sigma_{2^{p^3-1},2^{p^3-1}} \ge \frac{1}{2p^2} \ln(2^{p^3-1}) = \frac{p^3-1}{2p^2} \ln 2\to \infty
$$
as $p\to \infty$. Hence $S_{n}$ diverges as $n\to \infty$, the conclusion holds.