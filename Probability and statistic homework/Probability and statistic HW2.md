>[!problem] Problem 1
> Give a sequence of Bernoulli trials of size $n$. For each Bernoulli trial, assume $P(\text{Success})=p$. Let $X$ be the number of successes of this Bernoulli sequence. Denote $\mathbb{X}$, the support of $X$.
>a. List $\mathbb{X}$.
>b. Find the pmf of $X$, i.e. $\forall x\in\mathbb{X}$, find $f(x)$.
>c. Verify that $\sum_{x\in\mathbb{X}}f(x)=1$.
#### a.
$$\mathbb{X}=\{0,1,\cdots,n\}.$$
#### b.
$$f(x)=P(X=x)=\binom{n}{x}p^{x}(1-p)^{n-x}.$$
#### c.
According to Newton's Binomial Theorem: $$\sum_{x\in\mathbb{X}}f(x)=\sum_{x=0}^{n}\binom{n}{x}p^{x}(1-p)^{n-x}=(p+1-p)^n=1.$$
___
>[!problem] Problem 2
>Determine if the following variables are continuous or discrete. Denote $f(\cdot)$, $F(\cdot)$ be the pdf (or pmf), CDF.
>a. A random variable $X$ with $P(X=1)=0.4$, $P(X=2)=0.3$, $P(X=3)=0.3$.
>b. A random variable $X$ with $f(x)=2x$, $\forall x\in[0,1]$, otherwise $f(x)=0$.
>c. A random variable $X$ with $$F(x)=\begin{cases}0, &\text{if }x<a,\\
\frac{x-a}{b-a},&\text{if }a\leq x\leq b,\\
1,&\text{if }x>b\end{cases}$$
>where $a,b\in\mathbb{R}$ and $a<b$.
>d. A random variable $X$ with $$F(x)=\begin{cases}0, &\text{if }x<1,\\
\frac{k}{6},&\text{if }k\leq x<(k+1),k=1,2\ldots,5,\\
1,&\text{if }x\geq6\end{cases}$$
>e. A random variable $X$ with $\mathbb{X}=\{1,2,\ldots,m\}$.
>f.  A random variable $X$ with $\mathbb{X}=(a,b)$, where $a,b\in\mathbb{R}$ and $a<b$.

Continuous: b, c, f.
Discrete: a, d, e.
___
>[!problem] Problem 3
> Roll a fair four-sided die twice. The sample space for this experiment is $\Omega^{2}=\{(\omega_{1},\omega_{2}):\omega_{1},\omega_{2}\in\Omega\}$, $\Omega=\{1,2,3,4\}$. Assume the occurrence of each of these outcomes is equally likely. Let $X$ be the maximum of the two numbers facing up. What's the distribution of $X$?

Let $f(x)$ be the distribution of $X$, then
$$f(k)=P(X=k)=\frac{2k-1}{16},k=1,2,3,4.$$
___
>[!problem] Problem 4
>Let $X$ be the random variable with pdf $f(x)=x^{2}e^{-\frac{x^{3}}{3}}$, $\forall x\in(0,\infty)$.
>a. Let $Y=\log(X)$, find the pdf of $Y$.
>b. Let $Y=X^{2}+1$, find the pdf of $Y$.

Denote the pdf of $X$ as $f_X(x)$, the pdf of $Y$ as $f_Y(y)$, the cdf of  as $F_X(x)$, and the cdf of  as $F_Y(y)$.
$$F_X(x)=\int_{0}^{x}x^2e^{-\frac{x^{3}}{3}}\,dx=1-e^{-\frac{x^{3}}{3}}.$$
#### a.
$$X\in(0,\infty)\Rightarrow Y=\log(X)\in(-\infty,+\infty),X=e^Y.$$
$$F_Y(y)=P(Y\leq y)=P(X\leq e^y)=F_X(e^y)=1-e^{-\frac{e^{3y}}{3}}.$$
$$f_Y(y)=\frac{dF_Y(y)}{dy}=e^{3y}\cdot e^{-\frac{e^{3y}}{3}},y\in(-\infty,+\infty).$$
#### b.
$$X\in(0,\infty)\Rightarrow Y=X^2+1\in(1,+\infty),X=\sqrt{Y-1}.$$
$$F_Y(y)=P(Y\leq y)=P(X\leq \sqrt{y-1})=F_X(\sqrt{y-1})=1-e^{-\frac{(y-1)^{3/2}}{3}}.$$
$$f_Y(y)=\frac{dF_Y(y)}{dy}=\frac{\sqrt{y-1}}{2}\cdot e^{-\frac{(y-1)^{3/2}}{3}},y\in(1,+\infty).$$
___
>[!problem] Problem 5
 >Let $X$ be the random variable with pdf $f(x)=\frac{3x^{2}}{2}$, $\forall x\in(-1,1)$.
>a. Let $Y=-X$, find the pdf of $Y$.
>b. Let $Y=X^{2}$, find the pdf of $Y$.

Denote the pdf of $X$ as $f_X(x)$, the pdf of $Y$ as $f_Y(y)$, the cdf of  as $F_X(x)$, and the cdf of  as $F_Y(y)$.
$$F_X(x)=\int_{-1}^{x}\frac{3x^{2}}{2}\,dx=\frac{x^3+1}{2}.$$
#### a.
$$X\in(-1,1)\Rightarrow Y=-X\in(-1,1),X=-Y.$$
$$F_Y(y)=P(Y\leq y)=P(X\geq -y)=1-F_X(-y)=\frac{y^3+1}{2}.$$
$$f_Y(y)=\frac{dF_Y(y)}{dy}=\frac{3y^2}{2},y\in(-1,1).$$
#### b.
$$X\in(-1,1)\Rightarrow Y=X^2\in(0,1),X=\begin{cases}
\sqrt{Y}&,X\geq0,\\
-\sqrt{Y}&,X<0.\\
\end{cases}$$
$$F_Y(y)=P(Y\leq y)=P(-\sqrt{Y}\leq X \leq \sqrt{Y})=F_X(\sqrt{y})-F_X(-\sqrt{y})=y^{3/2}.$$
$$f_Y(y)=\frac{dF_Y(y)}{dy}=\frac{3 \sqrt{y}}{2}.$$
___
>[!problem] Problem 6
>Assume $X_{n}$ follows a Binomial distribution, $X_{n}\sim\text{Bin}(n,p_{n})$ with $p_{n}=\frac{2}{n}$, $n=100$.
>a. Find $P(X_{n}=3)$.
>b. Approximate $P(X_{n}=3)$ with a Poisson distribution.

#### a.
$$P(X_{n}=3)=\binom{100}{3}{p_n}^{3}(1-p_n)^{97}=\binom{100}{3}{0.02}^{3}(1-0.02)^{97}\approx0.1823.$$
#### b.
$$P(X_{n}=3)\approx \frac{e^{np_n}\cdot (np_n)^3}{3!}=\frac{e^{-2}\cdot 2^3}{3!} \approx0.1804.$$
___
>[!problem] Problem 7
> Assume X follows a Poisson distribution with $\lambda=3$.
>a. Find $P(2<X<6)$.
>b. Find $P(X\geq3)$.
>c. Find $P(X\leq3)$.
>d. Let $Y=X^3$, find the pdf of $Y$.

#### a.
$$P(2<X<6)=P(X=3)+P(X=4)+P(X=5)=e^{-\lambda}(\frac{\lambda^3}{3!}+\frac{\lambda^4}{4!}+\frac{\lambda^5}{5!})\approx0.4929.$$
#### b.
$$P(X\geq3)=1-P(X=0,1,2)=1-e^{-\lambda}(\frac{\lambda^0}{0!}+\frac{\lambda^1}{1!}+\frac{\lambda^2}{2!})\approx0.5768.$$
#### c.
$$P(X\leq3)=P(X=0)+\cdots+P(X=3)=e^{-\lambda}(\frac{\lambda^0}{0!}+\cdots+\frac{\lambda^3}{3!})\approx0.6472.$$
#### d.
Denote the pdf of $X$ as $f_X(x)$, and the pdf of $Y$ as $f_Y(y)$.
$$f_Y(y)=P(Y=y)=P(X=y^{1/3})=f_X(y^{1/3})=e^{-\lambda}\frac{\lambda^{y^{1/3}}}{(y^{1/3})!},y=0,^31^3,2^3\cdots.$$
___
>[!problem] Problem 8
>Denote $X$ the lifetime (in days) of an electronic component. Assume $X$ follow an exponential distribution with $\lambda=1/100$.
>a. If $P(X<a)=0.25$. What's the probability that the component operates longer than $a$.
>b. Find $P(X>a+b|X>b)$, $\forall b>0$.

#### a.
0.75.
#### b.
$$P(X>a+b|X>b)=\frac{e^{-\lambda (a+b)}}{e^{-\lambda b}}=e^{-\lambda a}=P(X>a),\forall b>0.$$
___
>[!problem] Problem 9
Assume $Z$ follows the standard normal distribution. Let $X=\sigma Z+\mu$, where $\sigma>0$, $\mu\in\mathbb{R}$, i.e., $X\sim N(\mu,\sigma^2)$. Denote $\Phi(z)=P(Z\leq z)$, find the following probabilities.
a. $P(X>1)$.
b. $P(4<X<5)$.

#### a.
$$\begin{align*}
P(X > 1) &= P(\sigma Z + \mu > 1) \\
&= P\left(Z > \frac{1 - \mu}{\sigma}\right) \\
&= 1 - \Phi\left(\frac{1 - \mu}{\sigma}\right)
\end{align*}$$

#### b.
$$\begin{align*}
P(4 < X < 5) &= P\left(\frac{4 - \mu}{\sigma} < Z < \frac{5 - \mu}{\sigma}\right) \\
&= \Phi\left(\frac{5 - \mu}{\sigma}\right) - \Phi\left(\frac{4 - \mu}{\sigma}\right)
\end{align*}$$