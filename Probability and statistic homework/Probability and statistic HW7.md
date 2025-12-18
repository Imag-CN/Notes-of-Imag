___

>[!problem] Problem 1
>Assume $X_{1},X_{2},...,X_{n}$ are a random sample from a population $N(0,\sigma^{2})$.
>
>a.  Find the method of moment estimator of $\sigma^{2}$. Justify whether it is an unbiased estimator.
>
>b.  Find the maximum likelihood estimator of $\sigma^{2}$.

**Solution:**
**a.** The population mean is $\mu = 0$, and the population variance is $\sigma^2 = E(X^2) - (E(X))^2 = E(X^2)$.

Since the first moment doesn't contain information about $\sigma^2$, we equate the second moment ($E(X^2)$) to the corresponding sample moment:
$$
E(X^2) = \frac{1}{n} \sum_{i=1}^n X_i^2
$$
$$
\sigma^2 = \frac{1}{n} \sum_{i=1}^n X_i^2
$$
Therefore, the Method of Moment (MoM) estimator is:
$$
\hat{\sigma}^2_{\text{MM}} = \frac{1}{n} \sum_{i=1}^n X_i^2
$$
Check unbiasedness:
$$
E(\hat{\sigma}^2_{\text{MM}}) = E\left( \frac{1}{n} \sum_{i=1}^n X_i^2 \right) = \frac{1}{n} \sum_{i=1}^n E(X_i^2) = \frac{1}{n} \sum_{i=1}^n \sigma^2 = \sigma^2
$$
Therefore, $\hat{\sigma}^2_{\text{MM}}$ is an unbiased estimator of $\sigma^2$.

**b.** The joint density is 
$$
f(x_1,...,x_n; \sigma^2) = \prod_{i=1}^n \frac{1}{\sqrt{2\pi\sigma^2}} e^{-\frac{x_i^2}{2\sigma^2}}.
$$
The log-likelihood function is:
$$
\ell(\sigma^2) = -\frac{n}{2} \log(2\pi) - \frac{n}{2} \log(\sigma^2) - \frac{1}{2\sigma^2} \sum_{i=1}^n x_i^2
$$
Differentiate with respect to $\sigma^2$ (treating $\sigma^2$ as the variable $\theta$):
$$
\frac{\partial \ell}{\partial (\sigma^2)} = -\frac{n}{2\sigma^2} + \frac{1}{2(\sigma^2)^2} \sum_{i=1}^n x_i^2
$$
Set the derivative to zero:
$$ -\frac{n}{2\sigma^2} + \frac{1}{2(\sigma^2)^2} \sum_{i=1}^n x_i^2 = 0 $$
Solving for $\sigma^2$ gives the maximum likelihood estimator (MLE):
$$
\hat{\sigma}^2_{\text{MLE}} = \frac{1}{n} \sum_{i=1}^n X_i^2
$$
___

>[!problem] Problem 2
>Assume $X_{1},X_{2},...,X_{n}$ are a random sample from a uniformly distributed population Uniform ($\theta,\theta+1$).
>
>Show that the maximum likelihood estimator (MLE) of $\theta$ is not unique. For example, $X_{(1)},X_{(n)}-1$ and $\dfrac{X_{(1)}+X_{(n)}-1}{2}$ are the MLE of $\theta$.

**Proof:**
The probability density function (pdf) for $X_i \sim \text{Uniform}(\theta, \theta+1)$ is:
$$ f(x_i; \theta) = \begin{cases} 1, & \theta \le x_i \le \theta + 1 \\ 0, & \text{otherwise} \end{cases} $$
The joint pdf (the likelihood function) is:
$$ L(\theta) = \prod_{i=1}^n f(x_i; \theta) = \begin{cases} 1, & \theta \le x_i \le \theta+1 \text{ for all } i=1,...,n \\ 0, & \text{otherwise} \end{cases} $$
Let $X_{(1)} = \min\{X_1,...,X_n\}$ and $X_{(n)} = \max\{X_1,...,X_n\}$. Since the population is uniform ($\theta,\theta+1$), $X_{(1)}$ and $X_{(n)} - 1$ cannot be equal.

For the likelihood to be $1$, we need every $x_i$ to satisfy $\theta \le x_i \le \theta+1$. This condition is equivalent to:
$$
\theta \le X_{(1)} \quad \text{and} \quad X_{(n)} \le \theta + 1, \quad \text{i.e.} \quad X_{(n)} - 1 \le \theta \le X_{(1)}.
$$
So we can rewrite the likelihood function:
$$
L(\theta) = \begin{cases} 1, & \text{if } X_{(n)} - 1 \le \theta \le X_{(1)} \\ 0, & \text{otherwise} \end{cases}
$$
To maximizing $L(\theta)$ is equivalent to letting $L(\theta) = 1$, so we can take any $\theta$ in the interval $[X_{(n)} - 1, \; X_{(1)}]$ as the maximum likelihood estimator. So MLE is not unique (because $X_{(1)}$ and $X_{(n)} - 1$ cannot be equal). Specifically we can take $X_{(1)},X_{(n)}-1$ and $\dfrac{X_{(1)}+X_{(n)}-1}{2}$ as the MLE of $\theta$.
___

>[!problem] Problem 3
>Assume $X_{1},X_{2},\ldots,X_{n}$ are a random sample from a population with pdf $f(x)=(\alpha + 1)x^{\alpha}$, for $0 < x < 1$. Otherwise $f(x)=0$.
>
>a. Find the method of moment estimator of $\alpha$.
>
>b. Find the maximum likelihood estimator of $\alpha$.

**Solution:**
**a.** The first moment (mean) of the distribution is:
$$
E(X) = \int_0^1 x \cdot (\alpha+1) x^{\alpha} dx = (\alpha+1) \int_0^1 x^{\alpha+1} dx = (\alpha+1) \left[ \frac{x^{\alpha+2}}{\alpha+2} \right]_0^1 = \frac{\alpha+1}{\alpha+2}
$$
Equate the population mean to the sample mean $\bar{X} = \frac{1}{n}\sum_{i=1}^n X_i$:
$$
\frac{\alpha+1}{\alpha+2} = \bar{X}
$$

Solve for $\alpha$ gives:
$$
\hat{\alpha}_{\text{MM}} = \frac{2\bar{X} - 1}{1 - \bar{X}}
$$

**b.** Write the likelihood function:
$$
L(\alpha) = \prod_{i=1}^n f(x_i; \alpha) = \prod_{i=1}^n (\alpha+1)x_i^{\alpha} = (\alpha+1)^n \left( \prod_{i=1}^n x_i \right)^{\alpha}
$$
Write the log-likelihood function:
$$
\ell(\alpha) = \ln L(\alpha) = n \ln(\alpha+1) + \alpha \sum_{i=1}^n \ln x_i
$$
Differentiate with respect to $\alpha$:
$$
\frac{\partial \ell}{\partial \alpha} = \frac{n}{\alpha+1} + \sum_{i=1}^n \ln x_i \
$$
Set the derivative to zero:
$$
\frac{n}{\alpha+1} + \sum_{i=1}^n \ln X_i = 0
$$
Solve for $\alpha$ gives:
$$
\hat{\alpha}_{\text{MLE}} = -\frac{n}{\sum_{i=1}^n \ln X_i} - 1
$$
___

>[!problem] Problem 4
>Assume $X_{1},X_{2},...,X_{n}$ are a random sample from a uniformly distributed population Uniform($\theta-\frac{1}{2},\theta+\frac{1}{2}$). Denote $\hat{\theta}_{1}=\frac{1}{n}\sum_{i=1}^{n}X_{i}$, and $\hat{\theta}_{2}=\frac{1}{2}(X_{(1)}+X_{(n)})$.
>
>a.  Show that $\hat{\theta}_{1},\hat{\theta}_{2}$ are unbiased estimator of $\theta$.
>
>b.  Which one has a smaller variance?

**Proof:**
**a.** For $\hat{\theta}_1 = \frac{1}{n}\sum_{i=1}^{n}X_i$:
$$
E(\hat{\theta}_1) = E\left( \frac{1}{n}\sum_{i=1}^{n}X_i \right) = \frac{1}{n}\sum_{i=1}^{n}E(X_i) = \frac{1}{n} \cdot n\theta = \theta
$$
The pdf of the minimum $X_{(1)}$ is:
$$
f_{(1)}(x) = n[1-F(x)]^{n-1}f(x)  = n(\theta+\frac{1}{2}-x)^{n-1}
$$
The pdf of the maximum $X_{(n)}$ is:
$$
f_{(n)}(x) = n[F(x)]^{n-1}f(x) = n(x-\theta+\frac{1}{2})^{n-1}
$$

Compute their expectations:
$$
E(X_{(1)}) = \int_{\theta-\frac{1}{2}}^{\theta+\frac{1}{2}} x \cdot n(\theta+\frac{1}{2}-x)^{n-1} dx=\theta+\frac{1}{2} - \frac{n}{n+1}
$$
$$
E(X_{(n)}) = \int_{\theta-\frac{1}{2}}^{\theta+\frac{1}{2}} x \cdot n(x-\theta+\frac{1}{2})^{n-1} dx= \theta-\frac{1}{2} + \frac{n}{n+1}
$$
Therefore, the expectation of $\hat{\theta}_2$ is:
$$
E(\hat{\theta}_2) = \frac{1}{2}\left[ E(X_{(1)}) + E(X_{(n)}) \right] = \theta
$$

Hence, both $\hat{\theta}_1$ and $\hat{\theta}_2$ are unbiased estimators of $\theta$.

**b.**
For $X_{i}$:
$$
Var(X_i) = \frac{[(\theta+\frac{1}{2}) - (\theta-\frac{1}{2})]^2}{12} = \frac{1^2}{12} = \frac{1}{12}
$$
Therefore,
$$
Var(\hat{\theta}_1) = Var\left( \frac{1}{n}\sum_{i=1}^{n}X_i \right) = \frac{1}{n^2} \sum_{i=1}^{n} Var(X_i) = \frac{1}{n^2} \cdot n \cdot \frac{1}{12} = \frac{1}{12n}
$$

Compute $E(X_{(1)}^2)$:
$$
E(X_{(1)}^2) = \int_{\theta-\frac{1}{2}}^{\theta+\frac{1}{2}} x^2 \cdot n(\theta+\frac{1}{2}-x)^{n-1} dx = (\theta+\frac{1}{2})^2 - \frac{2n}{n+1}(\theta+\frac{1}{2}) + \frac{n}{n+2} 
$$
Similarly, for $E(X_{(n)}^2)$:
$$
E(X_{(n)}^2) = \int_{0}^{1} x^2\cdot n(x-\theta+\frac{1}{2})^{n-1}dx = (\theta-\frac{1}{2})^2 + \frac{2n}{n+1}(\theta-\frac{1}{2}) + \frac{n}{n+2} 
$$
Therefore,
$$
Var(X_{(1)}) = E(X_{(1)}^2) - [E(X_{(1)})]^2= \frac{n}{(n+1)^2(n+2)}
$$
$$
Var(X_{(n)}) = E(X_{(n)}^2) - [E(X_{(n)})]^2= \frac{n}{(n+1)^2(n+2)}
$$
$E(X_{(1)}X_{(n)})$ requires the joint pdf of the minimum and maximum. For i.i.d. samples, the joint pdf is:
$$
f_{(1),(n)}(x,y) = n(n-1)(y-x)^{n-2}, \quad \theta-\frac{1}{2} < x < y < \theta+\frac{1}{2}
$$
So,
$$
E(X_{(1)}X_{(n)}) = \int_{\theta-\frac{1}{2}}^{\theta+\frac{1}{2}} \int_{x}^{\theta+\frac{1}{2}} xy \cdot n(n-1)(y-x)^{n-2} \, dy \, dx=\theta^2 - \frac{1}{4} - \frac{1}{(n+1)(n+2)}
$$
Therefore,
$$
Cov(X_{(1)}, X_{(n)}) = E(X_{(1)}X_{(n)}) - E(X_{(1)})E(X_{(n)})=\frac{1}{(n+1)^2(n+2)}
$$
Now compute $Var(\hat{\theta}_2)$:
$$
Var(\hat{\theta}_2) = \frac{1}{4} \left[ Var(X_{(1)}) + Var(X_{(n)}) + 2Cov(X_{(1)}, X_{(n)}) \right]=\frac{1}{2(n+1)(n+2)}
$$
Consider the ratio between $Var(\hat{\theta}_1) = \frac{1}{12n}$ and $Var(\hat{\theta}_2) = \frac{1}{2(n+1)(n+2)}$:
$$
\frac{Var(\hat{\theta}_2)}{Var(\hat{\theta}_1)} = \frac{\frac{1}{2(n+1)(n+2)}}{\frac{1}{12n}} = \frac{12n}{2(n+1)(n+2)} = \frac{6n}{(n+1)(n+2)}
$$

*   For $n=1$: Ratio = $6/(2\cdot3)=1$, so variances are equal.
*   For $n=2$: Ratio = $12/(3\cdot4)=1$, so variances are equal.
*   For $n \ge 3$: $(n+1)(n+2) = n^2+3n+2 > 6n$, so the ratio is less than $1$, meaning $Var(\hat{\theta}_2) < Var(\hat{\theta}_1)$.

In conclusion:
*   For $n=1$ and $n=2$, $Var(\hat{\theta}_1) = Var(\hat{\theta}_2)$.
*   For $n \ge 3$, $Var(\hat{\theta}_2) < Var(\hat{\theta}_1)$.
___

>[!problem] Problem 5
>Assume $X_{1},X_{2},\dots,X_{n}$ are a random sample from an Exponential distribution with pdf $f(x)=\lambda e^{-\lambda x}$ for $x>0$. Otherwise, $f(x)=0$. Show that $\bar{X}_{n}$ is an unbiased estimator of $\frac{1}{\lambda}$.

**Proof:**
The expectation of a single random variable $X_i$ is:
$$
E(X_i) = \int_{0}^{\infty} x \cdot \lambda e^{-\lambda x} \, dx = \frac{1}{\lambda}. $$
The expectation of $\bar{X}_{n}$:
$$
E(\bar{X}_n) = E\left( \frac{1}{n} \sum_{i=1}^{n} X_i \right) = \frac{1}{n} \sum_{i=1}^{n} E(X_i)=\dfrac{1}{\lambda}.
$$
Therefore, $\bar{X}_{n}$ is an unbiased estimator of $\frac{1}{\lambda}$.
___

>[!problem] Problem 6
>Assume $X_{1},X_{2},...,X_{n}$ are a random sample from a population $N(\mu,\sigma^{2})$ where $\mu$ is unknown and $\sigma^{2}$ is known. Find the minimum value of $n$ such that the length of a $1-\alpha$ confidence interval of $\mu$ is less or equal to $L$.

**Solution:**
Since $\sigma^2$ is known, the $(1-\alpha)$ confidence interval for $\mu$ is based on the sample mean $\bar{X}$ and the standard normal distribution. The interval is given by:
$$
\bar{X} \pm z_{\alpha/2} \cdot \frac{\sigma}{\sqrt{n}}
$$
Here, $z_{\alpha/2}$ is the upper $\alpha/2$ quantile of the standard normal distribution, defined by $P(Z > z_{\alpha/2}) = \alpha/2$.

The total length $W$ of this two-sided interval is twice the margin of error:
$$
W = 2 \cdot z_{\alpha/2} \cdot \frac{\sigma}{\sqrt{n}}
$$
We require the length $W$ to be at most $L$. This gives the inequality:
$$
2 z_{\alpha/2} \cdot \frac{\sigma}{\sqrt{n}} \le L
$$
Rearrange the inequality:
$$
n \ge \left( \frac{2 z_{\alpha/2} \sigma}{L} \right)^2
$$
Therefore:
$$
n_{\min} = \left\lceil \left( \frac{2 z_{\alpha/2} \sigma}{L} \right)^2 \right\rceil
$$
___

>[!problem] Problem 7
>Assume the online time (in hours) of college students follows the normal distribution $N(\mu,\sigma^{2})$, where $\mu$ is unknown and $\sigma = 2$. A survey was conducted among $100$ randomly selected students, the sample mean is $6.5$. Find a $1-\alpha$ confidence interval of $\mu$.


**Solution:**
Since the population is normal and $\sigma$ is known, the appropriate pivotal quantity for inference about $\mu$ is:
$$ Z = \frac{\bar{X} - \mu}{\sigma / \sqrt{n}} \sim N(0, 1) $$
For a confidence level of $1-\alpha$, we have:
$$ P\left( -z_{\alpha/2} \le \frac{\bar{X} - \mu}{\sigma / \sqrt{n}} \le z_{\alpha/2} \right) = 1 - \alpha $$
where $z_{\alpha/2}$ is the upper $\alpha/2$ critical value of the standard normal distribution, satisfying $P(Z > z_{\alpha/2}) = \alpha/2$.

Manipulate the inequality inside the probability statement:
$$
-z_{\alpha/2} \le \frac{\bar{X} - \mu}{\sigma / \sqrt{n}} \le z_{\alpha/2}
$$
Rearrange to:
$$ \bar{X} + z_{\alpha/2} \cdot \frac{\sigma}{\sqrt{n}} \ge \mu \ge \bar{X} - z_{\alpha/2} \cdot \frac{\sigma}{\sqrt{n}} $$
This gives the general form of the $(1-\alpha)$ confidence interval for $\mu$:
$$ \left( \bar{X} - z_{\alpha/2} \cdot \frac{\sigma}{\sqrt{n}}, \; \bar{X} + z_{\alpha/2} \cdot \frac{\sigma}{\sqrt{n}} \right) $$
Substitute the given  values gives the interval:
$$
(6.5 - 0.2 \, z_{\alpha/2}, \; 6.5 + 0.2 \, z_{\alpha/2})
$$
___

>[!problem] Problem 8
>Let $X$ equal the amount of orange juice (in grams per day) consumed by an American. To estimate the mean $\mu$ of $X$, an orange growers' association took a random sample of $n = 16$ Americans and found that the sample mean is $\overline{x}_{n}= 144$ grams of orange juice per day, the sample standard deviation is $s_{n}  = 100$. Thus, find a $90\%$ confidence interval for $\mu$.

**Solution:**
Since the population standard deviation $\sigma$ is unknown and we are using the sample standard deviation $s$ as an estimate, and the sample size is small ($n=16 < 30$), we should use the $t$-distribution to construct the confidence interval for the population mean $\mu$.

- Degrees of freedom: $n - 1 =15$.
- Confidence level:  $\alpha = 1 - 0.90 = 0.10$ and $\alpha/2 = 0.05$.
- The critical $t$-value, denoted $t_{\alpha/2, \, \text{df}}$, satisfies $P(T > t_{\alpha/2, \, \text{df}}) = \alpha/2$, where $T \sim t(\text{df})$.
- From $t$-distribution tables, we find:
$$
t_{0.05, \, 15} \approx 1.753
$$
The general formula for a $(1-\alpha) \times 100\%$ confidence interval for $\mu$ when $\sigma$ is unknown is:
$$ \bar{x} \pm t_{\alpha/2, \, n-1} \cdot \frac{s}{\sqrt{n}} $$
First, compute the margin of error (ME):
$$ \text{ME} = t_{\alpha/2, \, n-1} \cdot \frac{s}{\sqrt{n}} = 1.753 \times \frac{100}{4} = 1.753 \times 25 = 43.825 $$
Now, construct the interval:
- Lower bound: $\bar{x} - \text{ME} = 144 - 43.825 = 100.175$
- Upper bound: $\bar{x} + \text{ME} = 144 + 43.825 = 187.825$

Therefore, the 90% confidence interval for the population mean daily orange juice consumption $\mu$ is:
$$
(100.175,\; 187.825)
\quad \text{(in grams)}
$$