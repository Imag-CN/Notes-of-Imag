___

>[!problem] [GAM] V.3.2
>Determine for which $z$ the following series converge.
>
>(a) $\sum_{k=1}^{\infty}(z-1)^{k}$
>
>(b) $\sum_{k=10}^{\infty}\frac{(z-i)^{k}}{k!}$
>
>(c) $\sum_{m=0}^{\infty}2^{m}(z-2)^{m}$
>
>(d) $\sum_{m=1}^{\infty}\frac{(z+i)^{m}}{m^{2}}$
>
>(e) $\sum_{n=1}^{\infty}n^{n}(z-3)^{n}$
>
>(f) $\sum_{n=3}^{\infty}\frac{2^{n}}{n^{2}}(z-2-i)^{n}$

**(a)**
This is a geometric series with common ratio $r = z - 1$. Thus it converges if and only if $|z-1| < 1$.
**(b)**
Use the ratio test:

$$ \lim_{k \to \infty} \left| \frac{1/(k+1)!}{1/k!} \right| = \lim_{k \to \infty} \frac{1}{k + 1} = 0$$

Therefore the series converges for all $z \in \mathbb{C}$.
**(c)**
This is a geometric series with common ratio $r = 2(z - 2)$. Thus it converges if and only if $|z-2| < 1/2$.
**(d)**
Use the ratio test:
$$\lim_{m \to \infty} \left| \frac{m}{m + 1} \right|^2 = 1$$
Thus the convergence radius is $1$.
If $|z + i| = 1$, series (absolute value) becomes $\sum_{m=1}^{\infty} \frac{1}{m^2}$ which converges.

Thus it converges if and only if $|z-2| \leq 1/2$.
**(e)**
Use the root test:
$$\lim_{n \to \infty} \sqrt[n]{|n^n|} = \lim_{n \to \infty} |n| = \infty$$
Thus it converges only at $z = 3$
**(f)**
Use the ratio test:
$$\lim_{n \to \infty} \left| \frac{2^{n+1}/(n+1)^2}{2^n/n^2} \right| = 2\cdot \lim_{n \to \infty} \left( \frac{n}{n + 1} \right)^2 = 2$$
If $|z - 2 - i| = \frac{1}{2}$: series (absolute value) becomes $\sum_{n=3}^{\infty} \frac{1}{n^2}$ which converges

Thus it converges if and only if $|z - 2 - i| \leq \frac{1}{2}$.
___

>[!problem] [GAM] V.3.5
>What functions are represented by the following power series?  
>
>(a) $\sum_{k=1}^{\infty} k z^k$,  
>(b) $\sum_{k=1}^{\infty} k^2 z^k$.  

**(a)**
From geometric series: $\sum_{k=0}^{\infty} z^k = \frac{1}{1-z}$

Differentiate: $\sum_{k=1}^{\infty} k z^{k-1} = \frac{1}{(1-z)^2}$

Multiply by $z$: $\sum_{k=1}^{\infty} k z^k = \frac{z}{(1-z)^2}$, $|z|<1$
**(b)**
From (a): $\sum_{k=1}^{\infty} k z^k = \frac{z}{(1-z)^2}$

Differentiate: $\sum_{k=1}^{\infty} k^2 z^{k-1} = \frac{1+z}{(1-z)^3}$

Multiply by $z$: $\sum_{k=1}^{\infty} k^2 z^k = \frac{z(1+z)}{(1-z)^3}$, $|z|<1$
___

>[!problem] [GAM] V.3.6
>Show the series $\sum_{k=0}^{\infty} a_k z^k$, the differentiated series $\sum_{k=1}^{\infty} k a_k z^{k-1}$, and the integrated series $\sum_{k=0}^{\infty} \frac{a_k}{k+1} z^{k+1}$ all have the same radius of convergence.

**Proof:**
For $\sum a_k z^k$, radius $R$ satisfies $\frac{1}{R} = \limsup |a_k|^{1/k}$

Differentiated series $\sum k a_k z^{k-1}$:
  $\limsup |k a_k|^{1/k} = \limsup k^{1/k} \cdot |a_k|^{1/k} = \limsup |a_k|^{1/k}$
  (since $\lim k^{1/k} = 1$)

Integrated series $\sum \frac{a_k}{k+1} z^{k+1}$:
  $\limsup \left|\frac{a_k}{k+1}\right|^{1/k} = \limsup \frac{|a_k|^{1/k}}{(k+1)^{1/k}} = \limsup |a_k|^{1/k}$
  (since $\lim (k+1)^{1/k} = 1$)

All three series have the same radius of convergence.
___

>[!problem] [GAM] V.4.1
>Find the radius of convergence of the power series for the following functions, expanded about the indicated point.
>
>(b) $\frac{1}{\cos z}$, about $z=0$
>
>(e) $z^{3/2}$, about $z=3$
>
>(f) $\frac{z-i}{z^{3}-z}$, about $z=2i$

Radius of convergence (denote as $R$) is distance to nearest singularity.
**(b)**
Singularities occur when $\cos z = 0$, i.e., $z = \frac{\pi}{2} + k\pi$

Nearest singularity to $z=0$ is at $z = \pm\frac{\pi}{2}$

Therefore $R = \frac{\pi}{2}$.
**(e)**
$z^{3/2}$ has branch point at $z=0$.

Distance from expansion point $z=3$ to branch point $z=0$ is $3$.

Therefore $R = 3$.
**(f)**
Factor denominator: $z^{3}-z = z(z-1)(z+1)$

Singularities at $z=0$, $z=1$, $z=-1$

Distance from $z=2i$ to:
- $z=0$: $|2i-0| = 2$
- $z=1$: $|2i-1| = \sqrt{1^2+2^2} = \sqrt{5}$
- $z=-1$: $|2i-(-1)| = \sqrt{1^2+2^2} = \sqrt{5}$

Nearest singularity is at $z=0$, distance $R = 2$.
___

>[!problem] [GAM] V.4.3
>Find the power series expansion of $\operatorname{Log} z$ about the point $z = i - 2$. Show that the radius of convergence of the series is $R = \sqrt{5}$. Explain why this does not contradict the discontinuity of $\operatorname{Log} z$ at $z = -2$.

**Solution:**
Let $z_0 = i - 2$, then:
$$\operatorname{Log} z = \operatorname{Log}(z_0) + \operatorname{Log}\left(1 + \frac{z - z_0}{z_0}\right)$$
For $|w| < 1$: $\operatorname{Log}(1 + w) = w - \frac{w^2}{2} + \frac{w^3}{3} - \cdots$
Let $w = \frac{z - z_0}{z_0}$, then:
$$\operatorname{Log} z = \operatorname{Log}(z_0) + \sum_{n=1}^{\infty} \frac{(-1)^{n-1}}{nz_{0}^n} \left({z - z_0}\right)^n$$
Series converges when $|w| < 1$, i.e., $\left|\frac{z - z_0}{z_0}\right| < 1,|z - z_0| < |z_0|$.

Thus radius of convergence: $|z_{0}| = \sqrt{5}$.

Branch cut of $\operatorname{Log} z$ is typically along negative real axis, which goes through the convergence disk; but the principle value can be defined by other branch cut, which doesn't go through the convergence disk (e.g. along positive real axis).

In fact, the series take value as $\operatorname{Log} z+2\pi i$ when $\operatorname{\mathrm{Im}}z\leq 0$, which remains the continuity.
___

>[!problem] [GAM] V.4.4
>Suppose $f(z)$ is analytic at $z = 0$ and satisfies $f(z) = z + f(z)^2$. What is the radius of convergence of the power series expansion of $f(z)$ about $z = 0$?

**Solution:**
From $f(z) = z + f(z)^2$, rearrange:
$$f(z)^2 - f(z) + z = 0$$

Solve quadratic:
$$f(z) = \frac{1 \pm \sqrt{1 - 4z}}{2}$$

The branch point is $z=1 /4$, thus the radius of convergence $R$ is:
$$R = \left|\frac{1}{4} - 0\right| = \frac{1}{4}$$
___

>[!problem] [GAM] V.4.7
>Find the power series expansion of the principal branch $\tan^{-1}(z)$ of the inverse tangent function about $z=0$. What is the radius of convergence of the series?

**Solution:**
We have
$$\frac{d}{dz}\tan^{-1}(z) = \frac{1}{1+z^2}$$
For $|z| < 1$:
$$\frac{1}{1+z^2} = \sum_{n=0}^{\infty} (-1)^n z^{2n}$$
Integrate term by term:
$$\tan^{-1}(z) = \int_0^z \frac{1}{1+w^2} dw = \sum_{n=0}^{\infty} (-1)^n \int_0^z w^{2n} dw= \sum_{n=0}^{\infty} (-1)^n \frac{z^{2n+1}}{2n+1}$$

Integral doesn't change convergence radius, thus:
$$\tan^{-1}(z) = \sum_{n=0}^{\infty} (-1)^n \frac{z^{2n+1}}{2n+1}, \quad |z| < 1$$
___

>[!problem] [GAM] V.4.8
>Expand $\log(1+iz)$ and $\log(1-iz)$ in power series about $z=0$.
>
>By comparing power series expansions, establish the identity
>
>$$\tan^{-1}z=\frac{1}{2i}\log\left(\frac{1+iz}{1-iz}\right).$$

**Proof:**
For $|z|<1$, we have
$$\log(1+iz) = iz + \frac{z^2}{2} - i\frac{z^3}{3} - \frac{z^4}{4} + i\frac{z^5}{5} + \cdots$$
$$\log(1-iz) = -iz + \frac{z^2}{2} + i\frac{z^3}{3} - \frac{z^4}{4} - i\frac{z^5}{5} + \cdots$$
Thus
$$\log\left(\frac{1+iz}{1-iz}\right)= z - \frac{z^3}{3} + \frac{z^5}{5} - \cdots$$
Therefore,
$$\frac{1}{2i}\log\left(\frac{1+iz}{1-iz}\right)=\sum_{n=0}^{\infty} (-1)^n \frac{z^{2n+1}}{2n+1}$$
$$\tan^{-1}z=\frac{1}{2i}\log\left(\frac{1+iz}{1-iz}\right)$$
___

>[!problem] [GAM] V.4.11
>For fixed $n \geq 0$, the Bessel function of the first kind $J_n(z)$ is defined by the power series:
>$$
>J_n(z) = \sum_{k=0}^{\infty} \frac{(-1)^k z^{n+2k}}{k! (n+k)! 2^{n+2k}}
>$$
>Show that $J_n(z)$ is an entire function. Show $J_n(z)$ satisfies the Bessel differential equation
>$$
>w'' + \frac{1}{z}w' + \left(1 - \frac{n^2}{z^2}\right)w = 0
>$$

**Proof:**
Using the ratio test:
$$\lim_{k \to \infty} \left| \frac{a_{k+1}}{a_k} \right| = \lim_{k \to \infty} \frac{k!(n+k)!2^{n+2k}}{(k+1)!(n+k+1)!2^{n+2k+2}} = \lim_{k \to \infty} \frac{1}{(k+1)(n+k+1) \cdot 4} = 0$$
Since the limit is $0$, the radius of convergence $R = \infty$. Thus, $J_n(z)$ is entire.

Let $w = J_n(z) = \sum_{k=0}^{\infty} a_k z^{n+2k}$, where $a_k = \frac{(-1)^k}{k!(n+k)!2^{n+2k}}$. Then
$$w' = \sum_{k=0}^{\infty} a_k(n+2k)z^{n+2k-1}$$
$$w'' = \sum_{k=0}^{\infty} a_k(n+2k)(n+2k-1)z^{n+2k-2}$$
Substitute into the differential equation:
$$w'' + \frac{1}{z}w' + \left(1 - \frac{n^2}{z^2}\right)w = \sum_{k=0}^{\infty} (a_k((n+2k)(n+2k-1) + (n+2k) -n^2)-a_{k+1})z^{n+2k-2}$$
Since $a_k((n+2k)(n+2k-1) + (n+2k) -n^2)-a_{k+1}=a_{k}(4nk+4k^2)-a_{k+1}=0$, the conclusion holds.
___

>[!problem] [GAM] V.4.13
>Prove the following version of L'Hospital's rule. If $f(z)$ and $g(z)$ are analytic, $f(z_0) = g(z_0) = 0$, and $g(z)$ is not identically zero, then
>$$
>\lim_{z \to z_0} \frac{f(z)}{g(z)} = \lim_{z \to z_0} \frac{f'(z)}{g'(z)},
>$$
>in the sense that either both limits are finite and equal, or both limits are infinite.

**Proof:**
If $f(z)$ is identically zero, the statement is trivial. We assume that $f(z)$ is not identically zero.

Since $f(z)$ and $g(z)$ are analytic at $z_0$, they have convergent power series expansions:
$$f(z) = \sum_{n=m}^{\infty} a_n(z - z_0)^n \quad \text{where } a_m \neq 0$$
$$g(z) = \sum_{n=k}^{\infty} b_n(z - z_0)^n \quad \text{where } b_k \neq 0$$

Here $m, k \geq 1$ since $f(z_0) = g(z_0) = 0$.
**Case 1: $m = k$**  
Then near $z_0$:

$$\frac{f(z)}{g(z)} = \frac{a_m(z - z_0)^m + \cdots}{b_m(z - z_0)^m + \cdots} = \frac{a_m + a_{m+1}(z - z_0) + \cdots}{b_m + b_{m+1}(z - z_0) + \cdots}$$
Taking limit as $z \to z_0$:

$$\lim_{z \to z_0} \frac{f(z)}{g(z)} = \frac{a_m}{b_m}$$
Now compute derivatives:

$$f'(z) = ma_m(z - z_0)^{m-1} + \cdots$$
$$g'(z) = mb_m(z - z_0)^{m-1} + \cdots$$

So:

$$\frac{f'(z)}{g'(z)} = \frac{ma_m(z - z_0)^{m-1} + \cdots}{mb_m(z - z_0)^{m-1} + \cdots} = \frac{a_m + \cdots}{b_m + \cdots}$$

Taking limit:

$$\lim_{z \to z_0} \frac{f'(z)}{g'(z)} = \frac{a_m}{b_m}$$

Thus both limits equal $\frac{a_m}{b_m}$.
**Case 2: $m > k$**  
Then:

$$\frac{f(z)}{g(z)} = \frac{a_m(z - z_0)^m + \cdots}{b_k(z - z_0)^k + \cdots} = (z - z_0)^{m-k} \cdot \frac{a_m + \cdots}{b_k + \cdots} \to 0$$

And:

$$\frac{f'(z)}{g'(z)} = \frac{ma_m(z - z_0)^{m-1} + \cdots}{kb_k(z - z_0)^{k-1} + \cdots} = (z - z_0)^{m-k} \cdot \frac{ma_m + \cdots}{kb_k + \cdots} \to 0$$

**Case 3: $m < k$**  
Then both $\frac{f(z)}{g(z)} \to \infty$ and $\frac{f'(z)}{g'(z)} \to \infty$.

In all cases, the limits are equal (finite or infinite).
___

>[!problem] [GAM] V.6.2
>Calculate the terms through order five of the power series expansion about $z=0$ of the function $z/\sin z$.

**Soulution:**
Expand:
$$\sin z = z - \frac{z^3}{3!} + \frac{z^5}{5!} - \cdots = z - \frac{z^3}{6} + \frac{z^5}{120} - \cdots$$
$$\frac{\sin z}{z} = 1 - \frac{z^2}{6} + \frac{z^4}{120} - \cdots$$

Let $w = \frac{z^2}{6} - \frac{z^4}{120} + \cdots$, then:
$$\frac{z}{\sin z} = \frac{1}{1 - w} = 1 + w + w^2 + w^3 + \cdots$$
Compute:
- $w = \frac{z^2}{6} - \frac{z^4}{120} + O(z^6)$
- $w^2 = \frac{z^4}{36} + O(z^6)$
- $w^3 = O(z^6)$
So:
$$\frac{z}{\sin z} = 1 + \left(\frac{z^2}{6} - \frac{z^4}{120}\right) + \left( \frac{z^4}{36} \right)^2= 1 + \frac{1}{6}z^2 + \frac{7}{360}z^4 + O(z^6)$$
Therefore:
$$\frac{z}{\sin z} = 1 + \frac{1}{6}z^2 + \frac{7}{360}z^4 + O(z^6)$$
___

>[!problem] [GAM] V.6.3
>Show that
>
>$$\frac{e^{z}}{1+z}=1+\frac{1}{2}z^{2}-\frac{1}{3}z^{3}+\frac{3}{8}z^{4}-\frac{11}{30}z^{5}+\cdots.$$
>
>Show that the general term of the power series is given by
>
>$$a_{n}=(-1)^{n}\left[\frac{1}{2!}-\frac{1}{3!}+\cdots+\frac{(-1)^{n}}{n!}\right],\quad n\geq 2.$$
>
>What is the radius of convergence of the series?

**Proof:**
$$e^z = 1 + z + \frac{z^2}{2!} + \frac{z^3}{3!} + \frac{z^4}{4!} + \frac{z^5}{5!} + \cdots$$
$$\frac{1}{1+z} = 1 - z + z^2 - z^3 + z^4 - z^5 + \cdots$$
Multiply term by term:
- Constant: $1 \cdot 1 = 1$
- $z$ term: $1 \cdot (-1) + 1 \cdot 1 = 0$
- $z^2$ term: $1 \cdot 1 + 1 \cdot (-1) + \frac{1}{2} \cdot 1 = \frac{1}{2}$
- $z^3$ term: $1 \cdot (-1) + 1 \cdot 1 + \frac{1}{2} \cdot (-1) + \frac{1}{6} \cdot 1 = -\frac{1}{3}$
- $z^4$ term: $1 \cdot 1 + 1 \cdot (-1) + \frac{1}{2} \cdot 1 + \frac{1}{6} \cdot (-1) + \frac{1}{24} \cdot 1 = \frac{3}{8}$
- $z^5$ term: $1 \cdot (-1) + 1 \cdot 1 + \frac{1}{2} \cdot (-1) + \frac{1}{6} \cdot 1 + \frac{1}{24} \cdot (-1) + \frac{1}{120} \cdot 1 = -\frac{11}{30}$
Therefore:
$$\frac{e^{z}}{1+z}=1+\frac{1}{2}z^{2}-\frac{1}{3}z^{3}+\frac{3}{8}z^{4}-\frac{11}{30}z^{5}+\cdots.$$

From the product $e^z \cdot \frac{1}{1+z}$, the coefficient $a_n$ is:
$$a_n = \sum_{k=0}^n \frac{1}{k!} \cdot (-1)^{n-k}$$
Therefore:
$$a_n = (-1)^n\left[\frac{1}{2!} - \frac{1}{3!} + \cdots + \frac{(-1)^n}{n!}\right]$$

Distance from expansion point $z = 0$ to nearest singularity $z = -1$ is $1$.

Therefore, the radius of convergence is $R = 1$.
___

>[!problem] [GAM] V.6.6
>Show that the coefficients of a power series "depend continuously" on the function they represent, in the following sense. If $\{f_m(z)\}$ is a sequence of analytic functions that converges uniformly to $f(z)$ for $|z| < \rho$, and
>$$
>f_m(z) = \sum_{k=0}^{\infty} a_{k,m} z^k, \quad f(z) = \sum_{k=0}^{\infty} a_k z^k,
>$$
>then for each $k \geq 0$, we have $a_{k,m} \to a_k$ as $m \to \infty$.

**Proof:**
By generalized CIF, for any analytic function $g(z)$ with power series $g(z) = \sum_{n=0}^\infty b_n z^n$ valid for $|z| < \rho$, the coefficient $b_k$ is given by:

$$b_k = \frac{1}{2\pi i} \oint_C \frac{g(\zeta)}{\zeta^{k+1}} d\zeta$$

where $C$ is a positively oriented circle of radius $r < \rho$.

Fix $r < \rho$ and let $C$ be the circle $|\zeta| = r$. Then:
$$a_{k,m} = \frac{1}{2\pi i} \oint_C \frac{f_m(\zeta)}{\zeta^{k+1}} d\zeta$$
$$a_k = \frac{1}{2\pi i} \oint_C \frac{f(\zeta)}{\zeta^{k+1}} d\zeta$$Estimate the Difference:
$$|a_{k,m} - a_k| = \left| \frac{1}{2\pi i} \oint_C \frac{f_m(\zeta) - f(\zeta)}{\zeta^{k+1}} d\zeta \right|$$
Using the ML-inequality:

$$|a_{k,m} - a_k| \leq \frac{1}{2\pi} \cdot \max_{\zeta \in C} \left| \frac{f_m(\zeta) - f(\zeta)}{\zeta^{k+1}} \right| \cdot 2\pi r$$
Since $|\zeta| = r$ on $C$, we have $|\zeta^{k+1}| = r^{k+1}$, so:
$$|a_{k,m} - a_k| \leq \frac{1}{r^k} \max_{|\zeta| = r} |f_m(\zeta) - f(\zeta)|$$
Since $f_m \to f$ uniformly on $|z| \leq r$, for any $\epsilon > 0$, there exists $M$ such that for all $m > M$:

$$\max_{|\zeta| = r} |f_m(\zeta) - f(\zeta)| < \epsilon r^k$$
Therefore, for $m > M$:

$$|a_{k,m} - a_k| < \epsilon$$
This proves that $\lim_{m \to \infty} a_{k,m} = a_k$ for each fixed $k \geq 0$.
___

>[!problem] [SL] 4.2.10
>设 $f(z) = \sum_{n=0}^{\infty} a_n z^n$ 将 $B(0, R)$ 一一地映为域 $G$. 证明: $G$ 的面积为 $\pi \sum_{n=1}^{\infty} n |a_n|^2 R^{2n}$.

**证明:**
对于共形映射 $w = f(z) = u(x,y) + iv(x,y)$, 像域的面积公式为:

$$\text{Area}(G) = \iint_{B(0,R)} |f'(z)|^2 dxdy$$
使用极坐标 $z = re^{i\theta}$, $dxdy = rdrd\theta$:
$$\text{Area}(G) = \int_0^{2\pi} \int_0^R |f'(re^{i\theta})|^2 r dr d\theta$$
其中
$$f'(z) = \sum_{n=1}^{\infty} n a_n z^{n-1}$$
而在极坐标下 $z = re^{i\theta}$:

$$f'(re^{i\theta}) = \sum_{n=1}^{\infty} n a_n r^{n-1} e^{i(n-1)\theta}$$
于是模的平方为:

$$|f'(re^{i\theta})|^2 = \sum_{n=1}^{\infty} \sum_{m=1}^{\infty} n m a_n \overline{a_m} r^{n+m-2} e^{i(n-m)\theta}$$
对角度 $\theta$ 积分:
$$\int_0^{2\pi} |f'(re^{i\theta})|^2 d\theta = 2\pi \sum_{n=1}^{\infty} n^2 |a_n|^2 r^{2n-2}$$
于是:
$$\text{Area}(G) = \int_0^R r \left[ \int_0^{2\pi} |f'(re^{i\theta})|^2 d\theta \right] dr= 2\pi \sum_{n=1}^{\infty} n^2 |a_n|^2 \int_0^R r^{2n-1} dr$$
其中:

$$\int_0^R r^{2n-1} dr = \frac{R^{2n}}{2n}$$
因此:
$$\text{Area}(G) = \pi \sum_{n=1}^{\infty} n |a_n|^2 R^{2n}$$
___

>[!problem]
Let $f : D \to \mathbb{C}$ be an analytic function defined on a domain $D \subset \mathbb{C}$. Let $a \in D$ and suppose $B(a,R)$ is the largest open disk inside $D$. Prove that if $f$ is not bounded in $B(a,R)$, then $R$ is the radius of convergence of the Taylor series of $f$ at $a$.

**Proof:**
Let $R_T$ be the radius of convergence of the Taylor series of $f$ at $a$.

Since $B(a,R)$ is the largest disk contained in $D$, the Taylor series cannot converge on a disk larger than $B(a,R)$ without analytic continuation beyond $D$. Thus $R_T \leq R$.

Assume $R_T < R$. Then there exists $r$ such that $R_T < r < R$ where the Taylor series converges absolutely and uniformly on $\overline{B(a,r)}$. Since $f$ equals its Taylor series on $B(a,r)$, $f$ is bounded on $\overline{B(a,r)}$ (as a continuous function on a compact set). But $B(a,r) \subset B(a,R)$, so $f$ is bounded on $B(a,R)$ - contradiction. Thus $R_T \geq R$.

Therefore $R_T = R$.
___

>[!problem]
>Let $f(z) = \sum_{n=0}^{\infty} a_n z^n$ be a power series with convergence radius $R > 0$. Show that for each $0 < \rho < R$ the following *Gutzmer's inequality* holds:  
>$$
>\sum_{n=0}^{\infty} |a_n|^2 \rho^{2n} \leq M(\rho)
>$$ 
>where $M(\rho) = \sup\bigl\{|f(z)| \mid |z| = \rho\bigr\}$. Derive from the Gutzmer's inequality the Cauchy estimate
>$$
>|a_n| \leq \frac{M_\rho}{\rho^n}, \quad n \in \mathbb{Z}_{\geq 0}.
>$$

**Proof:**
On the circle $|z| = \rho$, parameterize $z = \rho e^{i\theta}$, $\theta \in [0,2\pi]$. Then:
$$\overline{f(z)} = \sum_{m=0}^\infty \overline{a_m}\overline{z}^m = \sum_{m=0}^\infty \overline{a_m}\rho^m e^{-im\theta}$$
Compute the integral $I(\rho)$ using the parameterization:
$$I(\rho):=\frac{1}{2\pi i}\oint_{|z|=\rho} \frac{f(z)\overline{f(z)}}{z}dz = \frac{1}{2\pi}\int_0^{2\pi} f(\rho e^{i\theta})\overline{f(\rho e^{i\theta})}d\theta$$
$$= \frac{1}{2\pi}\int_0^{2\pi} \left(\sum_{n=0}^\infty a_n \rho^n e^{in\theta}\right)\left(\sum_{m=0}^\infty \overline{a_m}\rho^m e^{-im\theta}\right)d\theta$$
By uniform convergence, interchange summation and integration:
$$= \sum_{n=0}^\infty \sum_{m=0}^\infty a_n\overline{a_m}\rho^{n+m} \cdot \frac{1}{2\pi}\int_0^{2\pi} e^{i(n-m)\theta}d\theta$$
The integral $\frac{1}{2\pi}\int_0^{2\pi} e^{i(n-m)\theta}d\theta$ equals $1$ when $n=m$ and $0$ otherwise (orthogonality of exponentials), so:
$$I(\rho)= \sum_{n=0}^\infty |a_n|^2\rho^{2n}$$
On the other hand, since $|f(z)| \leq M(\rho)$ on $|z| = \rho$, we have:
$$\left|\frac{1}{2\pi}\int_0^{2\pi} f(\rho e^{i\theta})\overline{f(\rho e^{i\theta})}d\theta\right| \leq \frac{1}{2\pi}\int_0^{2\pi} |f(\rho e^{i\theta})|^2 d\theta \leq M(\rho)^2$$
Therefore:
$$\sum_{n=0}^\infty |a_n|^2\rho^{2n} \leq M(\rho)^2$$

From Gutzmer's inequality, for each fixed $n$, the term $|a_n|^2\rho^{2n}$ is bounded by the entire sum:
$$|a_n|^2\rho^{2n} \leq \sum_{k=0}^\infty |a_k|^2\rho^{2k} \leq M(\rho)^2$$

Taking square roots gives:
$$|a_n| \leq \frac{M(\rho)}{\rho^n}, \quad n \in \mathbb{Z}_{\geq 0}$$