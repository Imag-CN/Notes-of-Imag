>[!problem] Problem 1
>Let random variable $X$ follow the Cauchy distribution with probability density function $f(x)=\frac{1}{\pi}\frac{1}{1 + x^{2}},x\in(-\infty,\infty)$.
>
>a. Determine if the expectation of $X$ exists.
>
>b. Prove your conclusion.

**a.** The expectation of $X$ does not exist.

**b.** Proof:
$$E[|X|] = \int_{-\infty}^{\infty} |x| f(x)  dx = \frac{1}{\pi} \int_{-\infty}^{\infty} \frac{|x|}{1+x^2}  dx = \frac{2}{\pi} \int_{0}^{\infty} \frac{x}{1+x^2}  dx$$
Let $u = 1+x^2$, then $du = 2x  dx$, and as $x \to \infty$, $u \to \infty$.
$$\int_{0}^{\infty} \frac{x}{1+x^2}  dx = \frac{1}{2} \int_{1}^{\infty} \frac{1}{u}  du = \frac{1}{2} \lim_{b \to \infty} \ln u \big|_{1}^{b} = \infty$$
Since $E[|X|]$ diverges, $E[X]$ does not exist.

___

>[!problem] Problem 2
>Compute the expectation and variance for the following distributions.
>
>a. $X\sim Exp(\lambda)$.
>
>b. $X\sim Poisson(\lambda)$.

**a.** $X \sim Exp(\lambda)$, pdf is $f(x) = \lambda e^{-\lambda x}, x>0$.
- Expectation:
$$E[X] = \int_{0}^{\infty} x \lambda e^{-\lambda x}  dx = \frac{1}{\lambda}$$
- Variance: First find $E[X^2] = \int_{0}^{\infty} x^2 \lambda e^{-\lambda x}  dx = \frac{2}{\lambda^2}$
$$Var(X) = E[X^2] - (E[X])^2 = \frac{2}{\lambda^2} - \frac{1}{\lambda^2} = \frac{1}{\lambda^2}$$

**b.** $X \sim Poisson(\lambda)$, pmf is $P(X=k) = \frac{\lambda^k e^{-\lambda}}{k!}, k=0,1,2,\dots$
- Expectation:
$$E[X] = \sum_{k=0}^{\infty} k \frac{\lambda^k e^{-\lambda}}{k!} = \lambda e^{-\lambda} \sum_{k=1}^{\infty} \frac{\lambda^{k-1}}{(k-1)!} = \lambda e^{-\lambda} e^{\lambda} = \lambda$$
- Variance: First find $E[X(X-1)] = \sum_{k=0}^{\infty} k(k-1) \frac{\lambda^k e^{-\lambda}}{k!} = \lambda^2 e^{-\lambda} \sum_{k=2}^{\infty} \frac{\lambda^{k-2}}{(k-2)!} = \lambda^2$
$$E[X^2] = E[X(X-1)] + E[X] = \lambda^2 + \lambda$$
$$Var(X) = E[X^2] - (E[X])^2 = \lambda^2 + \lambda - \lambda^2 = \lambda$$

___

>[!problem] Problem 3
>Let $X\sim Gamma(\alpha,\lambda)$, $\alpha,\lambda > 0$, with probability density function $f(x)=\frac{\lambda^{\alpha}}{\Gamma(\alpha)}x^{\alpha - 1}e^{-\lambda x},\forall x\in(0,\infty)$.
>
>a. Find the moment generating function $M(t)$ of $X$.
>
>b. Use $M(t)$ to find the expectation of $X$.
>
>c. Use $M(t)$ to find the variance of $X$.
>
>d. Prove that if $X_k\sim Gamma(\alpha_k,\lambda)$, $k = 1,2,\ldots,n$ are mutually independent, then $Y=\sum_{k = 1}^{n}X_k\sim Gamma(\sum_{k}\alpha_k,\lambda)$.

**a.** Moment generating function:
$$M(t) = E[e^{tX}] = \int_{0}^{\infty} e^{tx} \frac{\lambda^{\alpha}}{\Gamma(\alpha)} x^{\alpha-1} e^{-\lambda x}  dx = \frac{\lambda^{\alpha}}{\Gamma(\alpha)} \int_{0}^{\infty} x^{\alpha-1} e^{-(\lambda-t)x}  dx$$
For $t < \lambda$, let $\beta = \lambda - t > 0$, then the integral becomes $\int_{0}^{\infty} x^{\alpha-1} e^{-\beta x}  dx = \frac{\Gamma(\alpha)}{\beta^{\alpha}}$
$$M(t) = \frac{\lambda^{\alpha}}{\Gamma(\alpha)} \cdot \frac{\Gamma(\alpha)}{(\lambda-t)^{\alpha}} = \left( \frac{\lambda}{\lambda-t} \right)^{\alpha}, \quad t < \lambda$$

**b.** Expectation:
$$M'(t) = \alpha \left( \frac{\lambda}{\lambda-t} \right)^{\alpha-1} \cdot \frac{\lambda}{(\lambda-t)^2} = \frac{\alpha \lambda^{\alpha}}{(\lambda-t)^{\alpha+1}}$$
$$E[X] = M'(0) = \frac{\alpha \lambda^{\alpha}}{\lambda^{\alpha+1}} = \frac{\alpha}{\lambda}$$

**c.** Variance:
$$M''(t) = \alpha(\alpha+1) \frac{\lambda^{\alpha}}{(\lambda-t)^{\alpha+2}}$$
$$E[X^2] = M''(0) = \frac{\alpha(\alpha+1)\lambda^{\alpha}}{\lambda^{\alpha+2}} = \frac{\alpha(\alpha+1)}{\lambda^2}$$
$$Var(X) = E[X^2] - (E[X])^2 = \frac{\alpha(\alpha+1)}{\lambda^2} - \frac{\alpha^2}{\lambda^2} = \frac{\alpha}{\lambda^2}$$

**d.** Proof: For $X_k \sim Gamma(\alpha_k, \lambda)$, its moment generating function is $M_{X_k}(t) = \left( \frac{\lambda}{\lambda-t} \right)^{\alpha_k}$
Due to independence, the moment generating function of $Y = \sum_{k=1}^n X_k$ is:
$$M_Y(t) = \prod_{k=1}^n M_{X_k}(t) = \prod_{k=1}^n \left( \frac{\lambda}{\lambda-t} \right)^{\alpha_k} = \left( \frac{\lambda}{\lambda-t} \right)^{\sum_{k=1}^n \alpha_k}$$
This is the moment generating function of a $Gamma(\sum_{k=1}^n \alpha_k, \lambda)$ distribution. By the uniqueness of moment generating functions, the result is proven.
___

>[!problem] Problem 4
>Let $f(x,y)=\frac{1}{2\pi}e^{-\frac{x^{2}+y^{2}}{2}}\left[1+xye^{-\frac{x^{2}+y^{2}}{2}}\right]$,$\forall x,y\in(-\infty,\infty)$.
>
>a. Show that $f(x,y)$ is a joint pdf (i.e. to show that $f(x,y)\geq 0,\forall x,y\in(-\infty,\infty)$ and $\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}f(x,y)dxdy=1$).
>
>b. Show that the marginal pdfs are each normal.
>
>c. Find $E(XY)$.

**a.** To show $f(x,y)$ is a joint pdf:
1. Non-negativity: Since $e^{-\frac{x^2+y^2}{2}} > 0$, it's clear that $f(x,y)\geq 0$ if $xy\geq{0}$. When $xy<0$, we have $1 + xye^{-\frac{x^2+y^2}{2}}\geq 1+xye^{-xy}\geq0$ (this is a result from AM-GM inequality, and $1+te^{-t}\geq{0}$ can be shown by studying its derivative). Thus we have $f(x,y) \geq 0$ for all $x,y$.
2. Integration to 1:
Let $\phi(x) = \frac{1}{\sqrt{2\pi}}e^{-x^2/2}$ be the standard normal pdf.
$$f(x,y) = \phi(x)\phi(y) + xy\phi(x)\phi(y)e^{-\frac{x^2+y^2}{2}}$$
$$\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}f(x,y)dxdy = \int\phi(x)dx\int\phi(y)dy + \int x\phi(x)e^{-x^2/2}dx\int y\phi(y)e^{-y^2/2}dy$$
Since $\int\phi(x)dx = 1$ and $\int x\phi(x)e^{-x^2/2}dx = \frac{1}{\sqrt{2\pi}}\int xe^{-x^2}dx = 0$, the integral equals $1 + 0 = 1$.

**b.** Marginal pdf of $X$:
$$f_X(x) = \int_{-\infty}^{\infty}f(x,y)dy = \phi(x)\int\phi(y)dy + x\phi(x)e^{-x^2/2}\int y\phi(y)e^{-y^2/2}dy$$
$$= \phi(x) \cdot 1 + x\phi(x)e^{-x^2/2} \cdot 0 = \phi(x)$$
Similarly, $f_Y(y) = \phi(y)$. Both are standard normal.

**c.** $E(XY) = \int_{-\infty}^{\infty}\int_{-\infty}^{\infty}xyf(x,y)dxdy$
$$= \int xy\phi(x)\phi(y)dxdy + \int x^2y^2\phi(x)\phi(y)e^{-\frac{x^2+y^2}{2}}dxdy$$
The first term is $E(X)E(Y) = 0 \cdot 0 = 0$.
The second term: $\left( \int x^2\phi(x)e^{-x^2/2}dx \right)^2 = \left( \frac{1}{\sqrt{2\pi}}\int x^2e^{-x^2}dx \right)^2=\left( \frac{1}{2\sqrt{2}} \right)^2=\dfrac{1}{8}$
So $E(XY) = \frac{1}{8}$.
___

>[!problem] Problem 5
>An obstetrician does ultrasound examinations on her patients between their $16$th and $25$th weeks of pregnancy to check the growth of each fetus. Let $X$ equal the widest diameter of the fetal head, and let $Y$ equal the length of the femur, both measurements in mm. Assume that $X$ and $Y$ have a bivariate normal distribution with $\mu_{1}=60.6,\sigma_{1}=11.2,\mu_{2}=46.8,\sigma_{2}=8.4$, and $\rho=0.94$.
>
>a. Find $P(40.5 < Y < 48.9)$.
>
>b. Find $P(40.5 < Y < 48.9|X = 68.6)$.

**a.** Since $Y \sim N(\mu_2=46.8, \sigma_2^2=8.4^2)$, standardize:
$$P(40.5 < Y < 48.9) = P\left(\frac{40.5-46.8}{8.4} < Z < \frac{48.9-46.8}{8.4}\right) = P(-0.75 < Z < 0.25)$$
$$= \Phi(0.25) - \Phi(-0.75) = \Phi(0.25) - [1 - \Phi(0.75)] = \Phi(0.25) + \Phi(0.75) - 1$$
Using standard normal table: $\Phi(0.25) \approx 0.5987$, $\Phi(0.75) \approx 0.7734$
$$P(40.5 < Y < 48.9) \approx 0.5987 + 0.7734 - 1 = 0.3721$$

**b.** For bivariate normal, the conditional distribution $Y|X=x \sim N(\mu_{Y|X}, \sigma_{Y|X}^2)$ where:
$$\mu_{Y|X} = \mu_2 + \rho\frac{\sigma_2}{\sigma_1}(x - \mu_1) = 46.8 + 0.94\cdot\frac{8.4}{11.2}(68.6 - 60.6) =52.44$$
$$\sigma_{Y|X}^2 = \sigma_2^2(1-\rho^2) = 8.4^2(1-0.94^2)\approx 8.21$$
So $\sigma_{Y|X} \approx \sqrt{8.21} \approx 2.865$
Now standardize:
$$P(40.5 < Y < 48.9|X=68.6) = P\left(\frac{40.5-52.44}{2.865} < Z < \frac{48.9-52.44}{2.865}\right) = P(-4.17 < Z < -1.24)$$
$$= \Phi(-1.24) - \Phi(-4.17) \approx  0.1075$$___

>[!problem] Problem 6
>A car dealer sells $X$ cars each day and always tries to sell an extended warranty on each of these cars.(In our opinion, most of these warranties are not good deals.) Let $Y$ be the number of extended warranties sold; then $Y\leq X$. The joint pmf of $X$ and $Y$ is given by
>
>$$
>f(x,y)=c(x+1)(4-x)(y+1)(3-y),x=0,1,2,3,y=0,1,2\text{ with}y\leq x.
>$$
>
>a. Find the value of $c$.
>
>b. Sketch the support of $X$ and $Y$.
>
>c. Get the marginal pmf of $X,Y$.
>
>d. Are $X,Y$ independent?
>
>e. Compute $E(X),Var(X)$.
>
>f. Compute $E(Y),Var(Y$).
>
>g. Compute $Cov(X,Y)$.
>
>h. Determine $\rho$.
>
>i. Find the best-fitting line and draw it on your figure.

**a.** Find $c$ such that $\sum_{x=0}^3 \sum_{y=0}^{\min(x,2)} f(x,y) = 1$.

Calculate sum:
- x=0: y=0 only: $c(1)(4)(1)(3) = 12c$

- x=1: y=0,1: $c(2)(3)[(1)(3)+(2)(2)] = 6c[3+4] = 42c$

- x=2: y=0,1,2: $c(3)(2)[(1)(3)+(2)(2)+(3)(1)] = 6c[3+4+3] = 60c$

- x=3: y=0,1,2: $c(4)(1)[(1)(3)+(2)(2)+(3)(1)] = 4c[3+4+3] = 40c$

Total = $12c + 42c + 60c + 40c = 154c = 1$ ⇒ $c = \frac{1}{154}$

**b.** Support: $\{(x,y): x=0,1,2,3; y=0,1,2; y\leq x\}$

Points: $(0,0), (1,0), (1,1), (2,0), (2,1), (2,2), (3,0), (3,1), (3,2)$

**c.** Marginal pmf:

$f_X(x) = \sum_{y=0}^{\min(x,2)} f(x,y)$

- $f_X(0) = \frac{12}{154} = \frac{6}{77}$

- $f_X(1) = \frac{42}{154} = \frac{21}{77}$

- $f_X(2) = \frac{60}{154} = \frac{30}{77}$

- $f_X(3) = \frac{40}{154} = \frac{20}{77}$

$f_Y(y) = \sum_{x=\max(y,0)}^3 f(x,y)$

- $f_Y(0) = f(0,0)+f(1,0)+f(2,0)+f(3,0) = \frac{12+18+18+12}{154} = \frac{60}{154} = \frac{30}{77}$

- $f_Y(1) = f(1,1)+f(2,1)+f(3,1) = \frac{24+24+16}{154} = \frac{64}{154} = \frac{32}{77}$

- $f_Y(2) = f(2,2)+f(3,2) = \frac{18+12}{154} = \frac{30}{154} = \frac{15}{77}$

**d.** Check independence: $f(0,0)=\frac{12}{154}$, $f_X(0)f_Y(0)=\frac{6}{77} \cdot \frac{30}{77} = \frac{180}{5929} \neq \frac{12}{154}$.

Thus not independent.

**e.** $E(X) = 0 \cdot \frac{6}{77} + 1 \cdot \frac{21}{77} + 2 \cdot \frac{30}{77} + 3 \cdot \frac{20}{77} = \frac{0+21+60+60}{77} = \frac{141}{77} \approx 1.831$

$E(X^2) = 0^2 \cdot \frac{6}{77} + 1^2 \cdot \frac{21}{77} + 2^2 \cdot \frac{30}{77} + 3^2 \cdot \frac{20}{77} = \frac{0+21+120+180}{77} = \frac{321}{77} \approx 4.169$

$Var(X) = E(X^2) - [E(X)]^2 = \frac{321}{77} - \left(\frac{141}{77}\right)^2 = \frac{321 \cdot 77 - 141^2}{77^2} = \frac{24717 - 19881}{5929} = \frac{4836}{5929} \approx 0.815$

**f.** $E(Y) = 0 \cdot \frac{30}{77} + 1 \cdot \frac{32}{77} + 2 \cdot \frac{15}{77} = \frac{0+32+30}{77} = \frac{62}{77} \approx 0.805$

$E(Y^2) = 0^2 \cdot \frac{30}{77} + 1^2 \cdot \frac{32}{77} + 2^2 \cdot \frac{15}{77} = \frac{0+32+60}{77} = \frac{92}{77} \approx 1.195$

$Var(Y) = E(Y^2) - [E(Y)]^2 = \frac{92}{77} - \left(\frac{62}{77}\right)^2 = \frac{92 \cdot 77 - 62^2}{77^2} = \frac{7084 - 3844}{5929} = \frac{3240}{5929} \approx 0.546$

**g.** $E(XY) = \sum xyf(x,y)$
$= 0 \cdot 0 \cdot \frac{12}{154} + 1 \cdot 0 \cdot \frac{18}{154} + 1 \cdot 1 \cdot \frac{24}{154} + 2 \cdot 0 \cdot \frac{18}{154} + 2 \cdot 1 \cdot \frac{24}{154} + 2 \cdot 2 \cdot \frac{18}{154} + 3 \cdot 0 \cdot \frac{12}{154} + 3 \cdot 1 \cdot \frac{16}{154} + 3 \cdot 2 \cdot \frac{12}{154}$$= \frac{0+0+24+0+48+72+0+48+72}{154} = \frac{264}{154} = \frac{132}{77} \approx 1.714$

$Cov(X,Y) = E(XY) - E(X)E(Y) = \frac{132}{77} - \frac{141}{77} \cdot \frac{62}{77} = \frac{132 \cdot 77 - 141 \cdot 62}{77^2} = \frac{10164 - 8742}{5929} = \frac{1422}{5929} \approx 0.240$

**h.** $\rho = \frac{Cov(X,Y)}{\sqrt{Var(X)Var(Y)}} = \frac{1422/5929}{\sqrt{(4836/5929)(3240/5929)}} = \frac{1422}{\sqrt{4836 \cdot 3240}}\approx 0.359$

**i.** Best-fitting line: $Y = a + bX$ where $b = \frac{Cov(X,Y)}{Var(X)} = \frac{1422/5929}{4836/5929} = \frac{1422}{4836} \approx 0.294$, 
$a = E(Y) - bE(X) = \frac{62}{77} - 0.294 \cdot \frac{141}{77} \approx 0.266$

Line: $Y = 0.266 + 0.294X$
![[Pasted image 20251106075329.png]]