___
> [!problem] [GAM] V.2.7
> Let $a_n$ be a bounded sequence of complex numbers. Show that for each $\epsilon > 0$, the series $\sum_{n=1}^{\infty} a_n n^{-z}$ converges uniformly for $\operatorname{Re} z \geq 1 + \epsilon$. Here we choose the principal branch of $n^{-z}$.

**Proof:**
Since $a_n$ is bounded, there exists $M > 0$ such that $|a_n| \leq M$ for all $n$.

For $\operatorname{Re} z \geq 1 + \epsilon$, we have:
$$
|a_n n^{-z}| = |a_n| \cdot |n^{-z}| \leq M \cdot n^{-\operatorname{Re} z} \leq M \cdot n^{-(1+\epsilon)}
$$
The series $\sum_{n=1}^{\infty} M n^{-(1+\epsilon)}$ converges by the p-test ($p = 1+\epsilon > 1$).

By the Weierstrass M-test, $\sum_{n=1}^{\infty} a_n n^{-z}$ converges uniformly for $\operatorname{Re} z \geq 1 + \epsilon$.
___
> [!problem] [GAM] V.2.8
> Show that $\sum_{k=1}^{\infty} \frac{z^{k}}{k^{2}}$ converges uniformly for $|z|<1$.

**Proof:**
For $|z|<1$, we have:
$$
\left|\frac{z^{k}}{k^{2}}\right| \leq \frac{1}{k^{2}}
$$

The series $\sum_{k=1}^{\infty} \frac{1}{k^{2}}$ converges.

By the Weierstrass M-test, $\sum_{k=1}^{\infty} \frac{z^{k}}{k^{2}}$ converges uniformly for $|z|<1$.
___

> [!problem] [GAM] V.2.9
> Show that $\sum_{k=1}^{\infty} \frac{z^{k}}{k}$ does not converge uniformly for $|z|<1$.

**Proof:**
Consider the partial sum $S_n(z) = \sum_{k=1}^{n} \frac{z^{k}}{k}$.
For $z = 1 - \frac{1}{n}$, we have:
$$
S_n\left(1-\frac{1}{n}\right) - S_{n-1}\left(1-\frac{1}{n}\right) = \frac{(1-\frac{1}{n})^{n}}{n}
$$
As $n \to \infty$, $(1-\frac{1}{n})^{n} \to e^{-1}$, so:
$$
\frac{(1-\frac{1}{n})^{n}}{n} \sim \frac{e^{-1}}{n}
$$
The remainder does not tend to 0 uniformly, hence the series does not converge uniformly for $|z|<1$.
___
>[!problem] [SL] 3.4.8
>设 $f\in H(B(0,R))\cap C(\overline{B(0,R)}),f=u+iv$. 证明: $f$ 可用实部表示为
>$$f(z)=\frac{1}{2\pi}\int_{0}^{2\pi}\frac{R\mathrm{e}^{\mathrm{i}\theta}+z}{R\mathrm{e}^{\mathrm{i}\theta}-z}u\left(R\mathrm{e}^{\mathrm{i}\theta}\right)\mathrm{d}\theta+\mathrm{i} v(0).$$

**证明:** 
$z=0$ 时由平均值定理即可得到结论. 下假设 $z \neq0$.

由柯西积分公式, 对 $|z|<R$ 有
$$f(z) = \frac{1}{2\pi i}\oint_{|w|=R} \frac{f(w)}{w - z}dw.$$
令 $w=Re^{i\theta},\theta \in [0,2\pi]$, 则有
$$
f(z)=\dfrac{1}{2\pi i}\int_{0}^{2\pi} \dfrac{f(Re^{i\theta})}{Re^{i\theta}-z}\cdot iR e^{i \theta}d\theta\tag{1}
$$
考虑反演点 $z^* = R^2/\bar{z}$, 由于 $|z^*|>R$, 函数 $\frac{f(w)}{w - z^*}$ 在 $|w|\leq R$ 上解析, 故
$$0 = \frac{1}{2\pi i}\oint_{|w|=R} \frac{f(w)}{w - z^*}dw.$$
令 $w=Re^{i\theta},\theta \in [0,2\pi]$, 则有
$$
0=\dfrac{1}{2\pi i}\int_{0}^{2\pi} \dfrac{f(Re^{i\theta})}{Re^{i\theta}-z^*}\cdot iR e^{i \theta}d\theta
$$
根据 $z^*$ 的定义, 再对上式取共轭, 化简可得
$$
0=\dfrac{1}{2\pi i}\int_{0}^{2\pi} \dfrac{\overline{ f(Re^{i\theta}) }}{Re^{i\theta}-z}\cdot (-iz)d\theta\tag{2}
$$
$(1)-(2)$ 并化简得
$$
f(z)=\frac{1}{2\pi}\int_{0}^{2\pi}\frac{R\mathrm{e}^{\mathrm{i}\theta}+z}{R\mathrm{e}^{\mathrm{i}\theta}-z}\cdot \left( \dfrac{f(Re^{i\theta})+\overline{ f(Re^{i\theta}) }}{2} \right) \mathrm{d}\theta+\frac{i}{2\pi} \int_{0}^{2\pi} \dfrac{f(Re^{i\theta})-\overline{ f(Re^{i\theta}) }}{2}\mathrm{d}\theta.
$$
利用 $u = (f+\bar{f})/2, v= (f+\overline{ f })/2$ 以及平均值定理, 可得结论.
___

>[!problem] [SL] 3.4.9
>设 $f\in H(B(0,R))\cap C(\overline{B(0,R)}),f=u+iv$, 则对任意 $0<r\leq R$, 有
>$$f^{\prime}(0)=\frac{1}{\pi r}\int_{0}^{2\pi} u\left(r\mathrm{e}^{\mathrm{i}\theta}\right)\mathrm{e}^{-\mathrm{i}\theta}\mathrm{d}\theta.$$

**证明:** 
由于 $f(z)\in H(B(0,R))\cap C(\overline{B(0,R)})$, 故 $g(z)=zf(z)\in H(B(0,R))\cap C(\overline{B(0,R)})$.
由平均值定理
$$
g(0)=\dfrac{1}{2\pi}\int_{0}^{2\pi}g(re^{i\theta})d\theta
$$
即
$$
0=\dfrac{1}{2\pi}\int_{0}^{2\pi}f(re^{i\theta})re^{i\theta}d\theta
$$
两边同时取共轭, 并同时除以 $r^2$ 可得
$$
0=\dfrac{1}{2\pi r}\int_{0}^{2\pi}\overline{ f(re^{i\theta}) }e^{-i\theta}d\theta\tag{1}
$$
另一方面, 由柯西积分公式
$$f'(0) = \frac{1}{2\pi i}\oint_{|w|=r} \frac{f(w)}{w^2}dw.$$
令 $w=Re^{i\theta},\theta \in [0,2\pi]$, 则有
$$
f'(0)=\frac{1}{2\pi i}\int_{0}^{2\pi} \frac{f(re^{i\theta})}{(re^{i\theta})^2}\cdot ire^{i\theta}d\theta.
$$
化简得
$$
f'(0)=\frac{1}{2\pi r}\int_{0}^{2\pi} f(re^{i\theta})e^{-i\theta}d\theta\tag{2}
$$
将 $(1)(2)$ 相加, 并利用 $u = (f+\bar{f})/2$ 即可得到结论.
___
**法二:**
只需在上一题结论的基础上, 在两边同时对 $z$ 求偏导, 再代入 $z=0$ 即可.

验证等式右边求导与积分可交换:
1. 被积函数 $K(z,\theta)=\frac{r\mathrm{e}^{\mathrm{i}\theta}+z}{r\mathrm{e}^{\mathrm{i}\theta}-z}u\left(r\mathrm{e}^{\mathrm{i}\theta}\right)$ 在 $|z|<r$ 上关于 $z$ 解析
2. 对固定 $r>0$, 当 $|z|\leq r_0<r$ 时, 被积函数及其导数一致有界
3. 由控制收敛定理, 可在积分号下求导
___

>[!problem] Problem 3
>Prove the following version of Morera's theorem: let $f(z)$ be a continuous function on a domain $D\subset\mathbb{C}$. If $\int_{\partial T}f(z)dz=0$ for every triangle $T\subset D$, then $f(z)$ is analytic on $D$.

**Proof:**
For any $z_{0}\in D$, suppose $z_{0}\in B(z_{0},r_{0}) \subset D$.

Since every rectangle path can be written as two triangle paths in $B(z_{0},r_{0})$, $f$ is analytic on $B(z_{0},r_{0})$ according to the rectangle version of Morera's theorem. Thus $f$ is analytic on $z_{0}$. Due to the arbitrariness of $z_{0}$, we obtain that $f(z)$ is analytic on $D$.
___

>[!problem] Problem 4
>Let $f$ be a continuous function on the interval $[a,b]$. Show that the function defined by
>$$F(z)=\int_{a}^{b}e^{-zt}f(t)dt$$
>is an entire function, and
>$$F^{\prime}(z)=-\int_{a}^{b}e^{-zt}tf(t)dt.$$

**Proof:**
Since $h(t,z)=-e^{-zt}tf(t)$ is a continuous complex-valued function, defined for $a\leq t\leq b$ and $z\in \mathbb{C}$, by Theorem on [GAM] P121, $H(z)=\int_{a}^{b}h(t,z)dt$ is an entire function.

Since $h(t,z)$ is continuous, we have 
$$
\int_{0}^{z_{0}}H(z)dz=\int_{0}^{z_{0}}\int_{a}^{b}h(t,z)dtdz=\int_{a}^{b}\int_{0}^{z_{0}}h(t,z)dzdt=\int_{a}^{b}e^{-z_{0}t}f(t)dt=F(z_{0})-F(0)
$$
where $z_{0}$ is any complex number.
Thus $\int_{0}^{z}H(w)dw=F(z)-F(0)$.

Since $H(z)$ is an entire function, $F(z)=\int_{0}^{z}H(w)dw+F(0)$ is an entire function, and $F'(z)=H(z),i.e.F^{\prime}(z)=-\int_{a}^{b}e^{-zt}tf(t)dt.$
___
>[!problem] Problem 5
>Prove the following Schwarz reflection principle which gives an example of analytic continuation. Let $D\subset\mathbb{C}$ be a domain which is symmetric with respect to the real axis (i.e. $z\in D\Rightarrow\bar{z}\in D$). Consider the following subsets of $D$:
>$$D_{+}:=\{z\in D\mid\operatorname{Im}(z)>0\},$$
>$$D_{-}:=\{z\in D\mid\operatorname{Im}(z)<0\},$$
>$$D_{0}:=\{z\in D\mid\operatorname{Im}(z)=0\}=D\cap\mathbb{R}.$$
>If $f:D_{+}\cup D_{0}\rightarrow\mathbb{C}$ is continuous, $f|_{D_{+}}$ is analytic and $f(D_{0})\subset\mathbb{R}$, then the following function
>$$F(z)=\left\{\begin{array}{ll}f(z)&\text{for}\quad z\in D_{+}\cup D_{0}\\ \overline{f(\bar{z})}&\text{for}\quad z\in D_{-}\end{array}\right.$$
>is analytic on $D$.

**Proof:** 
Let $f=u+iv$.
On $D_+$, $F(z)=f(z)$ is analytic by given condition.
On $D_-$, $F(z)=\overline{f(\bar{z})}$. Let $g(z)=\overline{f(\bar{z})}$, then
$$
g(x+iy)=\overline{f(x-iy)}=u(x,-y)-iv(x,-y).
$$
  Compute partial derivatives:
  $$
  \frac{\partial g}{\partial x}=\frac{\partial u}{\partial x}(x,-y)-i\frac{\partial v}{\partial x}(x,-y),
  $$ $$
\frac{\partial g}{\partial y}=-\frac{\partial u}{\partial y}(x,-y)+i\frac{\partial v}{\partial y}(x,-y).
$$
Since $f$ is analytic on $D_+$, it satisfies Cauchy-Riemann equations: $\frac{\partial u}{\partial x}=\frac{\partial v}{\partial y}$, $\frac{\partial u}{\partial y}=-\frac{\partial v}{\partial x}$.
Substituting gives 
$$
i\frac{\partial g}{\partial x}=\frac{\partial g}{\partial y},
$$

so $g$ is analytic. Then $F(z)$ is analytic on $D\setminus\mathbb{R}=D_+\cup D_-$.

For $x_0\in D_0$, since $f$ is continuous on $D_+\cup D_0$,
$$\lim_{z\to x_0^+}F(z)=\lim_{z\to x_0^+}f(z)=f(x_0).$$
For $z\to x_0^-$,
$$\lim_{z\to x_0^-}F(z)=\lim_{z\to x_0^-}\overline{f(\bar{z})}=\overline{f(x_0)}=f(x_0),$$
since $f(x_0)\in\mathbb{R}$. Therefore $F$ is continuous on $D_0$.

$F$ is continuous on $D$ and analytic on $D\setminus\mathbb{R}=D_+\cup D_-$. By HW6 Problem (6), $F$ is analytic on $D$.
___
>[!problem] Problem 6
>Determine all pairs $(f(z),g(z))$ of entire functions with the property $f^{2}(z)+g^{2}(z)=1$.

**Proof:** 
Since $f^{2}(z)+g^{2}(z)=1$, we have
$$(f(z)+ig(z))(f(z)-ig(z)) = 1.$$

Let $F(z) = f(z) + ig(z)$ and $G(z) = f(z) - ig(z)$. Then $F(z)G(z) = 1$.

Since $f$ and $g$ are entire, both $F$ and $G$ are entire functions. From $F(z)G(z) = 1$, we get that $F(z)$ is never zero.

By HW5 Problem (5a), since $F(z)$ is entire and never zero, there exists an entire function $h(z)$ such that:
$$F(z) = e^{h(z)}.$$

Then $G(z) = \frac{1}{F(z)} = e^{-h(z)}$.

Now we can solve for $f(z)$ and $g(z)$:
$$f(z) = \frac{F(z) + G(z)}{2} = \frac{e^{h(z)} + e^{-h(z)}}{2} = \cosh(h(z)),$$
$$g(z) = \frac{F(z) - G(z)}{2i} = \frac{e^{h(z)} - e^{-h(z)}}{2i} = -i\sinh(h(z)).$$

Using trigonometric functions instead of hyperbolic functions:
$$f(z) = \cos(-ih(z)), \quad g(z) = \sin(-ih(z)).$$
Let $H(z) = -ih(z)$, then $H(z)$ is entire and:
$$f(z) = \cos(H(z)), \quad g(z) = \sin(H(z)).$$
Therefore, all pairs of entire functions satisfying $f^2(z) + g^2(z) = 1$ are of the form:
$$f(z) = \cos(h(z)), \quad g(z) = \sin(h(z)),$$
where $h(z)$ is an arbitrary entire function.
___
>[!problem] Problem 7
>Suppose $f(z)$ is continuous on the sector $D=\{z=a+\rho e^{i\theta}\mid 0<\rho\leq\rho_0,\theta_0\leq\theta\leq\theta_0+\alpha\}$. Let $\gamma_\rho=\{z=a+\rho e^{i\theta}\mid\theta_0\leq\theta\leq\theta_0+\alpha\}$. If $\lim_{z\to a}(z-a)f(z)=A$, then $\lim_{\rho\to 0}\int_{\gamma_\rho}f(z)dz=iA\alpha$.

**Proof:** Given $\lim_{z\to a}(z-a)f(z)=A$, for $\rho$ small enough, $|(z-a)f(z)-A|<\epsilon$ when $|z-a|=\rho$.

Parameterize $\gamma_\rho: z=a+\rho e^{i\theta}$, then:
$$\int_{\gamma_\rho}f(z)dz=\int_{\theta_0}^{\theta_0+\alpha}f(a+\rho e^{i\theta})i\rho e^{i\theta}d\theta.$$
Write:
$$\int_{\gamma_\rho}f(z)dz=iA\alpha+\int_{\theta_0}^{\theta_0+\alpha}[f(a+\rho e^{i\theta})\rho e^{i\theta}-A]id\theta.$$

The error term is bounded by $\alpha\epsilon$, hence the result.

**Application:** Compute $\int_{0}^{\infty}\frac{1-\cos x}{x^2}dx$.

Consider the function $f(z)=\frac{1-e^{iz}}{z^2}$ and the contour $\gamma$ consisting of:
- Real axis: from $\epsilon$ to $R$
- Large circular arc $\gamma_R$: from $R$ to $-R$ (radius $R$)
- Real axis: from $-R$ to $-\epsilon$
- Small circular arc $\gamma_\epsilon$: from $-\epsilon$ to $\epsilon$ around 0

By Cauchy's theorem, $\oint_{\gamma} f(z)dz=0$.

***On $\gamma_{R}$:***
Since $|1-e^{iz}|\leq 2$ and $|f(z)|\leq\frac{2}{R^2}$, $\oint_{\gamma_{R}} f(z)dz\rightarrow0$ as $R\to\infty$.

***On $\gamma_{\rho}$:***
Near $z=0$, by differentiability we have 
$$
1-e^{iz}=\left. \dfrac{d}{dz} (1-e^{iz})\right|_{z=0}+o(|z|)=-iz+o(|z|),$$
so $\lim_{z\to 0}zf(z)=-i$.
By the claim with $\alpha=-\pi$: $\lim_{\rho\to 0}\int_{\gamma_\rho}f(z)dz=i(-i)(-\pi)=-\pi$.

***On real axis:***
As $R\to\infty$ and $\epsilon\to 0$, the integral on real axis tends to
$$
\int_{-\infty}^{+\infty}\frac{1- e^{iz}}{z^2}dz=-\int_{\gamma_{R}+\gamma_{\rho}}\frac{1- e^{iz}}{z^2}dz=\pi
$$
Taking real parts and using symmetry:
$$2\int_{0}^{\infty}\frac{1-\cos x}{x^2}dx=\pi,$$
hence
$$\int_{0}^{\infty}\frac{1-\cos x}{x^2}dx=\frac{\pi}{2}.$$