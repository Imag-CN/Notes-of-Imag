___

>[!note] Likelihood Function
>For independent and identically distributed (i.i.d.) samples $X_1, X_2, \dots, X_n$ from a distribution with parameter $\theta$ and probability density (or mass) function $f(x|\theta)$, the **likelihood function** given observed data $x_1, x_2, \dots, x_n$ is defined as:
>$$
>L(\theta) = \prod_{i=1}^{n} f(x_i|\theta).
>$$
>
>To simplify calculations, the natural logarithm is often taken, yielding the **log-likelihood function**:
>$$
>\ell(\theta) = \log L(\theta) = \sum_{i=1}^{n} \log f(x_i|\theta).
>$$

___

>[!note] Maximum Likelihood Estimator (MLE)
>The **maximum likelihood estimator** $\hat{\theta}_{\text{MLE}}$ of $\theta$ is the parameter value that maximizes the likelihood function $L(\theta)$ (or equivalently, the log-likelihood function $\ell(\theta)$), i.e.,
>$$
>\hat{\theta}_{\text{MLE}} = \arg\max_{\theta \in \Theta} L(\theta) = \arg\max_{\theta \in \Theta} \ell(\theta).
>$$

___

>[!note] Score Function
>The first derivative of the log-likelihood function with respect to $\theta$, denoted as:
>$$
>s(\theta) = \frac{\partial \ell(\theta)}{\partial \theta}.
>$$
>At the maximum, the first-order condition typically give $s(\hat{\theta}_{\text{MLE}}) = 0$.

___

>[!note] Information Matrix
>**Observed Information Matrix:** The negative second derivative of the log-likelihood function, i.e.,
>$$
>J(\theta) = -\frac{\partial^2 \ell(\theta)}{\partial \theta \partial \theta^\top}.
>$$
>**Fisher Information Matrix:** The expected value of the observed information matrix, i.e.,
>$$
>I(\theta) = \mathbb{E}[J(\theta)] = -\mathbb{E}\left[ \frac{\partial^2 \ell(\theta)}{\partial \theta \partial \theta^\top} \right].
>$$
>Under regularity conditions, the asymptotic variance of the MLE is $I(\theta)^{-1}$.

To ensure desirable asymptotic properties of the MLE (e.g., consistency, asymptotic normality, efficiency), the following **regularity conditions** are typically assumed:

1.  **Identifiability:** The parameter $\theta$ is **identifiable**. That is, for $\theta_1 \neq \theta_2$, we have $f(x|\theta_1) \neq f(x|\theta_2)$ for some $x$.

2.  **Common Support:** The support of the density $f(x|\theta)$ (i.e., the set $\{x: f(x|\theta) > 0\}$) does **not depend on $\theta$**. This ensures that the likelihood ratio is well-defined.

3.  **Differentiability:** The log-likelihood $\ell(\theta) = \log f(x|\theta)$ is **at least twice differentiable** with respect to $\theta$ in the interior of the parameter space $\Theta$.

4.  **Interchangeability:** The operations of **integration (or summation) and differentiation can be interchanged** with respect to $\theta$.

5.  **Finite Information:** The **Fisher Information Matrix** $I(\theta)$ is **finite and positive definite** for all $\theta$ in the interior of $\Theta$.

6. **Parameter Space:** $\Theta$ is a **compact** subset of $\mathbb{R}^k$ (to ensure the **existence** of the MLE). The true parameter $\theta_0$ is an **interior point** of $\Theta$ (to ensure that, for large $n$, the consistent estimator $\hat{\theta}_{\text{MLE}}$ lies in a neighborhood of $\theta_0$ where the log-likelihood is differentiable.).

7.  **Uniqueness of MLE:** The maximum of the likelihood function is **unique** in the interior of $\Theta$.
___

>[!note] Coefficiency
>$\hat{\theta}_n$ is **consistent** for $\theta_0$ if, for every $\epsilon > 0$,
>$$
>\lim_{n \to \infty} P( |\hat{\theta}_n - \theta_0| > \epsilon ) = 0.
>$$
>

**Proof:**
Define the sample and population criteria:
$$
M_n(\theta) = \frac{1}{n} \sum_{i=1}^n \log f(X_i|\theta), \quad M(\theta) = \mathbb{E}_{\theta_0}[\log f(X|\theta)].
$$
By the Kullback-Leibler inequality, $M(\theta) \le M(\theta_0)$ with equality **iff** $\theta = \theta_0$ (identifiability). So $\theta_0$ uniquely maximizes $M(\theta)$.

By compactness and a uniform law of large numbers:
$$
\sup_{\theta \in \Theta} |M_n(\theta) - M(\theta)| \xrightarrow{p} 0.
$$

Since $\hat{\theta}_n$ maximizes $M_n(\theta)$ and $\theta_0$ uniquely maximizes $M(\theta)$, a standard extremum estimator result implies:
$$
\hat{\theta}_n \xrightarrow{p} \theta_0.
$$
