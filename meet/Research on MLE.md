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

>[!note] Consistency
>$\hat{\theta}_n$ is **consistent** for $\theta_0$ if, for every $\epsilon > 0$,
>$$
>\lim_{n \to \infty} P( |\hat{\theta}_n - \theta_0| > \epsilon ) = 0.
>$$
>

To assure consistency of MLE, we need several assumptions:

**(A1) Compact Parameter Space**: $\Theta$ is a **compact** subset of $\mathbb{R}^k$.

**(A2) Identifiability:** For any $\theta_1 \neq \theta_2$, $P_{\theta_1} \neq P_{\theta_2}$. That is,
$$
\theta_1 \neq \theta_2 \quad \Longrightarrow \quad f(x|\theta_1) \neq f(x|\theta_2) \quad \text{on a set of positive measure}.
$$

**(A3) Continuity:** For each $x$, the function $\theta \mapsto \log f(x|\theta)$ is **upper semicontinuous** on $\Theta$.

**(A4) Integrable Envelope:** There exists an integrable function $m(x)$ (w.r.t. $P_{\theta_0}$) such that for all $\theta \in \Theta$,
$$
|\log f(x|\theta)| \le m(x).
$$
Furthermore, $\mathbb{E}_{\theta_0}[\log f(X|\theta_0)] > -\infty$.

**(A5) Uniform Convergence of Sample Averages:**
$$
\sup_{\theta \in \Theta} |M_n(\theta) - M(\theta)| \xrightarrow{a.s.} 0.
$$
>[!tip]
> Contents Remark
>Under (A1), (A3), and (A4), a uniform law of large numbers (e.g., via the theory of Glivenko–Cantelli classes) guarantees (A5).

---

To 

**Lemma 1 (Kullback–Leibler Inequality):**
Under identifiability (A2) and integrability (A4), for any $\theta \in \Theta$,
$$
M(\theta) \le M(\theta_0),
$$
with equality if and only if $\theta = \theta_0$ ($P_{\theta_0}$-a.s.). Hence, $\theta_0$ is the **unique global maximizer** of $M(\theta)$ on $\Theta$.

*Proof Sketch:* By Jensen's inequality,
$$
M(\theta) - M(\theta_0) = \mathbb{E}_{\theta_0} \left[ \log \frac{f(X|\theta)}{f(X|\theta_0)} \right] \le \log \mathbb{E}_{\theta_0} \left[ \frac{f(X|\theta)}{f(X|\theta_0)} \right] = \log 1 = 0.
$$
Equality holds iff $f(X|\theta)/f(X|\theta_0) = 1$ a.s., i.e., $\theta = \theta_0$.

---

### 4. Consistency Proof

**Theorem:** Under assumptions (A1)–(A5), the MLE $\hat{\theta}_n$ is strongly consistent:
$$
\hat{\theta}_n \xrightarrow{a.s.} \theta_0.
$$

*Proof:*

1.  **Existence:** By compactness of $\Theta$ (A1) and upper semicontinuity of $\log f(x|\theta)$ (A3), $M_n(\theta)$ is an upper semicontinuous function on a compact set, so its supremum is attained. Therefore, $\hat{\theta}_n$ exists.

2.  **Uniform Convergence:** By (A5),
    $$
    \sup_{\theta \in \Theta} |M_n(\theta) - M(\theta)| \xrightarrow{a.s.} 0.
    $$

3.  **Consistency of Extremum Estimators:** Define $\eta = \sup_{\theta \in \Theta} |M_n(\theta) - M(\theta)|$. Then $\eta \xrightarrow{a.s.} 0$. By definition of $\hat{\theta}_n$,
    $$
    M_n(\hat{\theta}_n) \ge M_n(\theta_0).
    $$
    Thus,
    $$
    M(\hat{\theta}_n) \ge M_n(\hat{\theta}_n) - \eta \ge M_n(\theta_0) - \eta \ge M(\theta_0) - 2\eta.
    $$
    Consequently,
    $$
    M(\theta_0) - M(\hat{\theta}_n) \le 2\eta \xrightarrow{a.s.} 0.
    $$
    By continuity of $M(\theta)$ (which follows from (A3), (A4), and the dominated convergence theorem) and Lemma 1 ($\theta_0$ is the unique maximizer), combined with compactness of $\Theta$, we obtain $\hat{\theta}_n \xrightarrow{a.s.} \theta_0$. More rigorously: if $\hat{\theta}_n$ did not converge a.s. to $\theta_0$, there would exist a subsequence $\hat{\theta}_{n_k} \to \theta^* \neq \theta_0$. By upper semicontinuity, $\limsup M(\hat{\theta}_{n_k}) \le M(\theta^*)$. But from above, $M(\hat{\theta}_{n_k}) \to M(\theta_0)$, so $M(\theta^*) \ge M(\theta_0)$, contradicting Lemma 1. Hence $\hat{\theta}_n \xrightarrow{a.s.} \theta_0$.

---

### 5. Weak Consistency Version

If (A5) is replaced by uniform convergence in probability,
$$
\sup_{\theta \in \Theta} |M_n(\theta) - M(\theta)| \xrightarrow{p} 0,
$$
then weak consistency follows: $\hat{\theta}_n \xrightarrow{p} \theta_0$. The proof is analogous, replacing almost sure convergence with convergence in probability.

---

### 6. Remarks

*   **Upper Semicontinuity vs. Continuity:** If $\log f(x|\theta)$ is continuous in $\theta$, (A3) holds automatically. Upper semicontinuity is weaker and allows for some boundary points.
*   **Integrable Envelope (A4):** Crucial for the uniform law of large numbers. It controls tail behavior, ensuring uniform convergence.
*   **Compactness (A1):** Essential; otherwise, the maximizer of $M_n(\theta)$ may not exist or may escape to infinity. Some generalizations to non-compact $\Theta$ require additional assumptions that $\theta_0$ is a "well-separated" maximizer and control the behavior of $M(\theta)$ as $\|\theta\| \to \infty$.
*   **Identifiability (A2):** Without it, $\theta_0$ is not unique, and consistency is meaningless.

**Summary:** Consistency of the MLE does not require differentiability. It only requires a compact parameter space, identifiability, some continuity (upper semicontinuity) of the log-likelihood, and an integrable envelope to guarantee uniform convergence of the sample average log-likelihood to its expectation. Once uniform convergence holds, the Kullback–Leibler inequality ensures $\theta_0$ is the unique maximizer, and the MLE naturally converges to it.