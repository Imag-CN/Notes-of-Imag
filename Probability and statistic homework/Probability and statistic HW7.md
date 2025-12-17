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

