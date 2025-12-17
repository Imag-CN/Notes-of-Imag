___

>[!problem] Problem 1
>Assume $X_{1},X_{2},...,X_{n}$ are a random sample from a population $N(0,\sigma^{2})$.
>
>a.  Find the method of moment estimator of $\sigma^{2}$. Justify whether it is an unbiased estimator.
>
>b.  Find the maximum likelihood estimator of $\sigma^{2}$.

**Solution:**
**a.** The population mean is $\mu = 0$, and the population variance is $\sigma^2 = E(X^2) - (E(X))^2 = E(X^2)$.

Equate the first population moment ($E(X^2)$) to the corresponding sample moment:
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
Therefore, $\hat{\sigma}^2_{\text{MM}}$ is an **unbiased** estimator of $\sigma^2$.

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

