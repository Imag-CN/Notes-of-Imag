___
>[!problem] Problem 1
>If the distribution of $Y$ is $Binomial(n,0.25)$, give a lower bound for $P(|Y/n-0.25|<0.05)$ when
>
>a. $n=100$.
>
>b. $n=500$.
>
>c. $n=1000$.

**Solution:**
We use Chebyshev's inequality: $P(|Y/n - p| \geq \varepsilon) \leq \frac{p(1-p)}{n\varepsilon^2}$.
Thus, $P(|Y/n - p| < \varepsilon) \geq 1 - \frac{p(1-p)}{n\varepsilon^2}$.

Here $p = 0.25$, $\varepsilon = 0.05$.

**a.**
Lower bound: $1 - \frac{0.25 \times 0.75}{100 \times (0.05)^2} =0.25$

**b.**
Lower bound: $1 - \frac{0.1875}{500 \times 0.0025} = 0.85$

**c.**
Lower bound: $1 - \frac{0.1875}{1000 \times 0.0025} = 0.925$
___

>[!problem]
>Suppose that a fair coin is tossed $1000$ times.
>
>a. Approximate the probability of obtaining more than $500$ heads.
>
>b. Approximate the probability of obtaining more than $550$ heads.

**Solution:**
Let $X$ be the number of heads in $1000$ tosses. $X \sim \text{Binomial}(n=1000, p=0.5)$.
Using normal approximation: $X \approx N(\mu = np = 500, \sigma^2 = np(1-p) = 250)$.
Let $Z$ follows the standard normal distribution.
**a.**
We have
$$P(X > 500) \approx P\left(Z > \frac{500 - 500}{\sqrt{250}}\right)= P(Z > 0)$$
Using symmetry: $P(Z > 0) =0.5$. Thus $P(X > 500) \approx 0.5$.

**b.**
We have
$$P(X > 550) \approx P\left(Z > \frac{550 - 500}{\sqrt{250}}\right) = P(Z > 3.1623)$$
Using standard normal table: $P(Z > 3.1623) =1-P(Z \leq 3.1623) \approx 0.0008$.
___

>[!problem] Problem 3
>Let $Y=X_{1}+X_{2}+\cdots+X_{15}$ be the sum of a random sample of size $15$ from the distribution whose pdf is $f(x)=(3/2)x^{2}$, $-1<x<1$. Using the pdf of $Y$, we find that $P(-0.3\leq Y\leq 1.5)=0.22788$. Use the central limit theorem to approximate this probability.

**Solution:**
Compute expectation and variance:
$$E[X_i] = \int_{-1}^{1} x \cdot \frac{3}{2}x^2 \, dx= 0$$
$$E[X_i^2] = \int_{-1}^{1} x^2 \cdot \frac{3}{2}x^2 \, dx  = \frac{3}{5}$$
Thus, $\sigma^2 = E[X_i^2] - (E[X_i])^2 = \frac{3}{5} - 0 = 0.6$.

For the sum $Y = \sum_{i=1}^{15} X_i$:
- Mean: $\mu_Y = 15 \times 0 = 0$
- Variance: $\sigma_Y^2 = 15 \times 0.6 = 9$

By the CLT, $Y \approx N(0, 9)$. Then:
$$P(-0.3 \leq Y \leq 1.5) \approx P\left( \frac{-0.3 - 0}{3} \leq Z \leq \frac{1.5 - 0}{3} \right) = P(-0.1 \leq Z \leq 0.5)\approx 0.23129$$
where $Z$ is the standard normal distribution.

Therefore, the CLT approximation probability is $0.23129$.
___

>[!problem] Problem 4
>A company has a one-year group life policy as follows.
>
>| Probability of Death | Benefit | Insured number |
>| :--- | :--- | :--- |
>| 0.015 | $20,000 | 1000 |
>
>Assume that the occurrence of each individual's claim is independent.
>
>a. The insurance company wants to collect a premium that equals the $95$th percentile of the distribution of the total claims. What should that premium be?
>
>b. If the premium is $200 per individual, what’s the probability that the insurance company will lose money?
>
>c. What's the probability that the total claims is over 30?

**Solution:**
Let $N$ be the number of deaths. $N \sim \text{Binomial}(n=1000, p=0.015)$.
Total claims $S = N \times 20000$.

**a.**
Mean: $\mu_N = np = 1000 \times 0.015 = 15$
Variance: $\sigma_N^2 = np(1-p) = 1000 \times 0.015 \times 0.985 = 14.775$

Using normal approximation $N \approx N(15, 14.775)$:
95th percentile of $N$: $z_{0.95} = 1.645$
$N_{0.95} \approx 15 + 1.645 \times 3.844 \approx 15 + 6.32 = 21.32$
Premium = $21.32 \times 20000 = \$426,400$

**b.**
Total premium collected = $1000 \times 200 = \$200,000$
Lose money if $S > 200,000\Rightarrow N > 200000/20000 = 10$
$P(N > 10) \approx0.6325$.

**c.**
$S > 30\Rightarrow N > 30/20000 = 0.0015$
$P(N \geq 0.0015) \approx 0.8450$.
___

>[!problem] Problem 5
>Let $X$ equal the maximal oxygen intake of a human on a treadmill, where the measurements are in millilitres of oxygen per minute per kilogram of weight. Assume that, for a particular population, the mean of $X$ is $\mu = 54.03$ and the standard deviation is $\sigma = 5.8$. Let $\bar{X}_n$ be the sample mean of a random sample of size $n$.
>
>a. When $n = 49$, find $P(52.5 \leq \bar{X}_n \leq 55.4)$, approximately.
>
>b. How many individuals should be sampled to ensure $P(\bar{X}_n > 53) > 0.997$, approximately?

**Solution:**
**a.**
$z_1 = (52.5 - 54.03)/0.8286 \approx -1.846$  
$z_2 = (55.4 - 54.03)/0.8286 \approx 1.653$  

$P(52.5 \leq \bar{X}_n \leq 55.4) \approx \Phi(1.653) - \Phi(-1.846) \approx 0.9505 - 0.0325 = 0.918$
**a.**
Find $n$ such that $P(\bar{X}_n > 53) > 0.997$  
We need $P(Z > \frac{53 - 54.03}{5.8/\sqrt{n}}) > 0.997$  

Since $P(Z > -2.75) \approx 0.997$, we solve:  
$\frac{-1.03\sqrt{n}}{5.8} < -2.75$  
$\sqrt{n} > \frac{2.75 \times 5.8}{1.03} \approx 15.49$  
$n > 239.9$  

Thus, $n \geq 240$
___

>[!problem] Problem 6
>Let $X_{1},X_{2},...,X_{n}\sim Uniform(0,1)$. Let $Y_{n}=\bar{X}_{n}^{2}$. Find the limiting distribution of $Y_{n}$.

**Solution:**
Let $X_i \sim \text{Uniform}(0,1)$ i.i.d. with:
- $E[X_i] = \mu = 0.5$
- $\text{Var}(X_i) = \sigma^2 = 1/12$

Let $Y_n = g(\bar{X}_n) = (\bar{X}_n)^2$, where $g(t) = t^2$.

By CLT: $\sqrt{n}(\bar{X}_n - 0.5) \xrightarrow{d} N(0, 1/12)$

Using delta method with $g'(t) = 2t$:
$g'(0.5) = 2 \times 0.5 = 1$

Thus:
$$\sqrt{n}(Y_n - g(0.5)) = \sqrt{n}(\bar{X}_n^2 - 0.25) \xrightarrow{d} N(0, [g'(0.5)]^2 \cdot \sigma^2)$$
$$\sqrt{n}(\bar{X}_n^2 - 0.25) \xrightarrow{d} N(0, 1^2 \cdot 1/12) = N(0, 1/12)$$
Therefore, $Y_n \approx N(0.25, 1/(12n))$ for large $n$.
(Strictly speaking, the limiting distribution (convergent by probability) of $Y_{n}$ is degenerate as following:
$$
F_{Y}(y)=\begin{cases}
0,y<0.25 \\
1,y\geq 0.25
\end{cases}
$$
i.e. the probability that the variable equals $0.25$ is $1$.)
___

>[!problem] Problem 7
>Assume the pdf of $X_{n}$ ($n=1,2,3,\ldots$) takes the following form
>
>$$f_{X_{n}}(x)=\frac{n}{\pi(1+n^{2}x^{2})},\forall x\in\mathbb{R}.$$
>
>Show that $X_{n}\xrightarrow{P}0$.

**Proof:**
To show $X_n \xrightarrow{P} 0$, we prove $\lim_{n\to\infty} P(|X_n| \geq \varepsilon) = 0$ for any $\varepsilon > 0$.
$$P(|X_n| \geq \varepsilon) = 2\int_{\varepsilon}^{\infty} \frac{n}{\pi(1+n^2x^2)}dx$$
Substitute $u = nx$, $dx = du/n$:
$$= \frac{2}{\pi}\int_{n\varepsilon}^{\infty} \frac{1}{1+u^2}du = \frac{2}{\pi}\left[\frac{\pi}{2} - \arctan(n\varepsilon)\right] = 1 - \frac{2}{\pi}\arctan(n\varepsilon)$$
As $n \to \infty$, $\arctan(n\varepsilon) \to \frac{\pi}{2}$, so:
$$\lim_{n\to\infty} P(|X_n| \geq \varepsilon) = 1 - \frac{2}{\pi} \cdot \frac{\pi}{2} = 0$$

Thus, $X_n \xrightarrow{P} 0$.