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

**Basic Steps:**
1. Write the likelihood function $L(\theta)$.
2. Take the logarithm to obtain $\ell(\theta)$.
3. Differentiate $\ell(\theta)$ with respect to $\theta$, set the derivative to zero, and solve for $\hat{\theta}_{\text{MLE}}$.
4. Verify second-order conditions to ensure a maximum.
5. Compute the information matrix for inference (e.g., constructing confidence intervals).