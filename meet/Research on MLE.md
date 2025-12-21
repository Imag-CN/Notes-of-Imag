___
## 1. Basic definitions

>[!definition] Likelihood Function
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

>[!definition] Maximum Likelihood Estimator (MLE)
>The **maximum likelihood estimator** $\hat{\theta}_{\text{MLE}}$ of $\theta$ is the parameter value that maximizes the likelihood function $L(\theta)$ (or equivalently, the log-likelihood function $\ell(\theta)$), i.e.,
>$$
>\hat{\theta}_{\text{MLE}} = \arg\max_{\theta \in \Theta} L(\theta) = \arg\max_{\theta \in \Theta} \ell(\theta).
>$$

___

>[!definition] Score Function
>The first derivative of the log-likelihood function with respect to $\theta$, denoted as:
>$$
>s(\theta) = \frac{\partial \ell(\theta)}{\partial \theta}.
>$$
>At the maximum, the first-order condition typically give $s(\hat{\theta}_{\text{MLE}}) = 0$.

___

>[!definition] Information Matrix
>**Observed Information Matrix:** The negative second derivative of the log-likelihood function, i.e.,
>$$
>J(\theta) = -\frac{\partial^2 \ell(\theta)}{\partial \theta \partial \theta^\top}.
>$$
>**Fisher Information Matrix:** The expected value of the observed information matrix, i.e.,
>$$
>I(\theta) = \mathbb{E}[J(\theta)] = -\mathbb{E}\left[ \frac{\partial^2 \ell(\theta)}{\partial \theta \partial \theta^\top} \right].
>$$
>Under regularity conditions, the asymptotic variance of the MLE is $I(\theta)^{-1}$.

___
## 2. Asymptotic Properties
With those basic definition above, we prove some desirable asymptotic properties of the MLE.
### 2.1 Consistency

>[!definition] Consistency
>$\hat{\theta}_n$ is **(weakly) consistent** for $\theta_0$ if $\hat{\theta}_n$ converges to $\theta_0$ by problability.
>
>If $\hat{\theta}_n$ **almost surely** converges to $\theta_0$, we say $\hat{\theta}_n$ is **strongly consistent** for $\theta_0$

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
>[!remark]
>Under (A1), (A3), and (A4), a uniform law of large numbers (e.g., via the theory of Glivenko–Cantelli classes) guarantees (A5).

---

To proof consistency we need the following lemma:

>[!lemma] Kullback–Leibler Inequality
>Under identifiability (A2) and integrability (A4), for any $\theta \in \Theta$,
>$$
M(\theta) \le M(\theta_0),
>$$
>with equality if and only if $\theta = \theta_0$ ($P_{\theta_0}$-a.s.). Hence, $\theta_0$ is the **unique global maximizer** of $M(\theta)$ on $\Theta$.

**Proof:** By Jensen's inequality,
$$
M(\theta) - M(\theta_0) = \mathbb{E}_{\theta_0} \left[ \log \frac{f(X|\theta)}{f(X|\theta_0)} \right] \le \log \mathbb{E}_{\theta_0} \left[ \frac{f(X|\theta)}{f(X|\theta_0)} \right] = \log 1 = 0.
$$
Equality holds iff $f(X|\theta)/f(X|\theta_0) = 1$ a.s., i.e., $\theta = \theta_0$.

---

>[!theorem]
>Under assumptions (A1)–(A5), the MLE $\hat{\theta}_n$ is strongly consistent:
>$$
>\hat{\theta}_n \xrightarrow{a.s.} \theta_0.
>$$

**Proof:**
By compactness of $\Theta$ (A1) and upper semicontinuity of $\log f(x|\theta)$ (A3), $M_n(\theta)$ is an upper semicontinuous function on a compact set, so its supremum is attained. Therefore, $\hat{\theta}_n$ exists.

By (A5), we have
$$
\sup_{\theta \in \Theta} |M_n(\theta) - M(\theta)| \xrightarrow{a.s.} 0.
$$

Define $\eta = \sup_{\theta \in \Theta} |M_n(\theta) - M(\theta)|$. Then $\eta \xrightarrow{a.s.} 0$. By definition of $\hat{\theta}_n$,
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
By continuity of $M(\theta)$ (which follows from (A3), (A4), and the dominated convergence theorem) and Kullback–Leibler Inequality ($\theta_0$ is the unique maximizer), combined with compactness of $\Theta$, we obtain $\hat{\theta}_n \xrightarrow{a.s.} \theta_0$. More rigorously: if $\hat{\theta}_n$ did not converge a.s. to $\theta_0$, there would exist a subsequence $\hat{\theta}_{n_k} \to \theta^* \neq \theta_0$. By upper semicontinuity, $\limsup M(\hat{\theta}_{n_k}) \le M(\theta^*)$. But from above, $M(\hat{\theta}_{n_k}) \to M(\theta_0)$, so $M(\theta^*) \ge M(\theta_0)$, contradicting Lemma 1. Hence $\hat{\theta}_n \xrightarrow{a.s.} \theta_0$.

>[!remark]
>Consistency of the MLE does not require differentiability. It only requires a compact parameter space, identifiability, some continuity (upper semicontinuity) of the log-likelihood, and an integrable envelope to guarantee uniform convergence of the sample average log-likelihood to its expectation. Once uniform convergence holds, the Kullback–Leibler inequality ensures $\theta_0$ is the unique maximizer, and the MLE naturally converges to it.

___

### 2.2 Asymptotic Normality

>[!definition] Asymptotic Normality
>Let $\{ \hat{\theta}_n \}$ be a sequence of estimators of a parameter $\theta_0 \in \mathbb{R}^k$.
>
>$\hat{\theta}_n$ is **asymptotically normal** if
>$$
>\sqrt{n} (\hat{\theta}_n - \theta_0) \xrightarrow{d} N(0, V),
>$$
>where $V$ is a positive semidefinite matrix called the **asymptotic variance matrix**.

Assume the MLE $\hat{\theta}_n$ is **consistent** ($\hat{\theta}_n \xrightarrow{p} \theta_0$) and the following regularity conditions hold in a neighborhood of $\theta_0$:

**(R1) Interior Point:** $\theta_0$ is an interior point of the parameter space $\Theta \subset \mathbb{R}^k$.

**(R2) Differentiability:** The log-likelihood $\ell(\theta) = \log f(x|\theta)$ is **twice continuously differentiable** in $\theta$.

**(R3) Interchange of Integration and Differentiation:** The score function $s(\theta) = \frac{\partial \ell(\theta)}{\partial \theta}$ satisfies
$$
\mathbb{E}_{\theta}[s(\theta)] = 0,
$$
and the Fisher information matrix
$$
I(\theta) = \operatorname{Var}_{\theta}(s(\theta)) = -\mathbb{E}_{\theta}\left[ \frac{\partial^2 \ell(\theta)}{\partial \theta \partial \theta^\top} \right]
$$
exists and is finite.

**(R4) Positive Definite Information:** $I(\theta_0)$ is **positive definite**.

**(R5) Dominance for the Second Derivative:** There exists an integrable function $M(x)$ such that
$$
\left\| \frac{\partial^2 \log f(x|\theta)}{\partial \theta \partial \theta^\top} \right\| \le M(x)
$$
for all $\theta$ in a neighborhood of $\theta_0$, where $\|\cdot\|$ is a matrix norm.

**(R6) Third-Derivative Control (Cramér's Condition):** $\log f(x|\theta)$ is three times differentiable, and there exists an integrable function $H(x)$ such that
$$
\left| \frac{\partial^3 \log f(x|\theta)}{\partial \theta_i \partial \theta_j \partial \theta_k} \right| \le H(x)
$$
for all $\theta$ in a neighborhood of $\theta_0$ and all $i, j, k$.
___

>[!theorem]
>If the regular conditions above hold, then the MLE is asymptotically normal:
>$$
>\sqrt{n} (\hat{\theta}_n - \theta_0) \xrightarrow{d} N(0, I(\theta_0)^{-1}).
>$$

**Proof:**
Since $\hat{\theta}_n$ is consistent and $\theta_0$ is an interior point (R1), for $n$ large enough $\hat{\theta}_n$ lies in the interior with probability approaching $1$. By (R2), the score function $s_n(\theta) = \frac{1}{n} \sum_{i=1}^n s(\theta; X_i)$ is differentiable, and at the maximum $\hat{\theta}_n$, we have the first-order condition:
$$
s_n(\hat{\theta}_n) = 0.
$$

Expand $s_n(\hat{\theta}_n)$ around $\theta_0$ using the mean value theorem (component-wise):
$$
0 = s_n(\hat{\theta}_n) = s_n(\theta_0) + J_n(\bar{\theta}_n) (\hat{\theta}_n - \theta_0),
$$
where $J_n(\theta) = \frac{1}{n} \sum_{i=1}^n \frac{\partial^2 \log f(X_i|\theta)}{\partial \theta \partial \theta^\top}$ is the sample average negative observed information, and $\bar{\theta}_n$ is a point on the line segment between $\hat{\theta}_n$ and $\theta_0$ (component-wise, so $\bar{\theta}_n \xrightarrow{p} \theta_0$ by consistency).

Rearranging gives:
$$
-J_n(\bar{\theta}_n) \cdot \sqrt{n} (\hat{\theta}_n - \theta_0) = \sqrt{n} \, s_n(\theta_0) = \frac{1}{\sqrt{n}} \sum_{i=1}^n s(\theta_0; X_i).
$$
The random vectors $s(\theta_0; X_i)$ are i.i.d. with $\mathbb{E}[s(\theta_0; X_i)] = 0$ (by R3) and $\operatorname{Var}(s(\theta_0; X_i)) = I(\theta_0)$ (by R3, R4). By the multivariate central limit theorem (CLT),
$$
\frac{1}{\sqrt{n}} \sum_{i=1}^n s(\theta_0; X_i) \xrightarrow{d} N(0, I(\theta_0)).
$$

By (R5) and the uniform law of large numbers (or the ergodic theorem with domination), $J_n(\theta)$ converges uniformly in probability to $-\mathbb{E}_{\theta_0}[\frac{\partial^2 \log f(X|\theta)}{\partial \theta \partial \theta^\top}] = I(\theta_0)$ in a neighborhood of $\theta_0$.

Since $\bar{\theta}_n \xrightarrow{p} \theta_0$, we have
$$
J_n(\bar{\theta}_n) \xrightarrow{p} -I(\theta_0).
$$
Therefore,
$$
-J_n(\bar{\theta}_n) \xrightarrow{p} I(\theta_0).
$$

Let $A_n = -J_n(\bar{\theta}_n)$ and $B_n = \frac{1}{\sqrt{n}} \sum s(\theta_0; X_i)$. We have
$$
A_n \xrightarrow{p} I(\theta_0) \quad \text{and} \quad B_n \xrightarrow{d} N(0, I(\theta_0)).
$$
From step 2, $\sqrt{n} (\hat{\theta}_n - \theta_0) = A_n^{-1} B_n$. By the continuous mapping theorem, $A_n^{-1} \xrightarrow{p} I(\theta_0)^{-1}$ (since matrix inversion is continuous at $I(\theta_0)$, which is positive definite by R4). Then by Slutsky's theorem,
$$
\sqrt{n} (\hat{\theta}_n - \theta_0) = A_n^{-1} B_n \xrightarrow{d} I(\theta_0)^{-1} \cdot N(0, I(\theta_0)).
$$
The distribution of $I(\theta_0)^{-1} Z$ for $Z \sim N(0, I(\theta_0))$ is $N(0, I(\theta_0)^{-1})$, because
$$
\operatorname{Cov}(I(\theta_0)^{-1} Z) = I(\theta_0)^{-1} \operatorname{Cov}(Z) I(\theta_0)^{-1} = I(\theta_0)^{-1} I(\theta_0) I(\theta_0)^{-1} = I(\theta_0)^{-1}.
$$

The mean value theorem expansion is technically valid component-wise, but to ensure the remainder is negligible, we use (R6). A second-order Taylor expansion of the log-likelihood $\ell_n(\theta)$ around $\theta_0$ yields
$$
 \ell_n(\hat{\theta}_n) - \ell_n(\theta_0) = s_n(\theta_0)^\top (\hat{\theta}_n - \theta_0) + \frac{1}{2} (\hat{\theta}_n - \theta_0)^\top \ell_n''(\tilde{\theta}_n) (\hat{\theta}_n - \theta_0),
    $$
where $\tilde{\theta}_n$ lies between $\hat{\theta}_n$ and $\theta_0$. Since $\hat{\theta}_n$ maximizes $\ell_n$, the left side is nonnegative. Dividing by $n$ and rearranging, combined with domination (R5) and consistency, shows that $s_n(\theta_0) = -J_n(\bar{\theta}_n)(\hat{\theta}_n - \theta_0) + o_p(n^{-1/2})$, which is sufficient for the argument.
___

### 2.3 Asymptotic Efficiency

>[!definition] Asymptotic Efficiency
>An estimator $\hat{\theta}_n$ of a parameter $\theta_0 \in \mathbb{R}^k$ is **asymptotically efficient** if it is:
>1.  **Consistent**: $\hat{\theta}_n \xrightarrow{p} \theta_0$.
>2.  **Asymptotically normal**: $\sqrt{n} (\hat{\theta}_n - \theta_0) \xrightarrow{d} N(0, V)$.
>3.  **Attains the Cramér–Rao lower bound (CRLB) asymptotically**: Its asymptotic variance matrix $\Sigma(\theta_0)$ equals the inverse of the Fisher information matrix per observation, i.e.,$$\Sigma(\theta_0) = I(\theta_0)^{-1},$$
>where $I(\theta_0) = \mathbb{E}_{\theta_0}[s(\theta_0) s(\theta_0)^\top]$ is the Fisher information matrix for a single observation, and $s(\theta) = \frac{\partial}{\partial \theta} \log f(X|\theta)$ is the score function.
>
>Equivalently, $\hat{\theta}_n$ is **asymptotically efficient** if, for any other consistent and asymptotically normal estimator $\tilde{\theta}_n$ with asymptotic variance $\tilde{\Sigma}(\theta_0)$, the difference $\tilde{\Sigma}(\theta_0) - I(\theta_0)^{-1}$ is positive semidefinite. This means $\hat{\theta}_n$ has the "smallest" asymptotic covariance matrix in the Loewner order.

---

>[!theorem]
>Under the same regularity conditions (R1)–(R6) as for asymptotic normality, the MLE $\hat{\theta}_n$ is asymptotically efficient.

**Proof:**
The asymptotic normality proof already gives the asymptotic distribution $N(0, I(\theta_0)^{-1})$. To establish efficiency, we need to show that $I(\theta_0)^{-1}$ is indeed the Cramér–Rao lower bound for any unbiased estimator, and that the MLE attains it asymptotically.


Under regularity conditions (R2)-(R3), for any unbiased estimator $\tilde{\theta}_n$ of $\theta_0$ based on $n$ i.i.d. observations, we have
$$
\operatorname{Cov}_{\theta_0}(\tilde{\theta}_n) \ge \frac{1}{n} I(\theta_0)^{-1},
$$
in the sense that $\operatorname{Cov}_{\theta_0}(\tilde{\theta}_n) - \frac{1}{n} I(\theta_0)^{-1}$ is positive semidefinite. Here $n I(\theta_0)$ is the Fisher information for the full sample.

From the asymptotic normality proof, we have
$$
\sqrt{n} (\hat{\theta}_n - \theta_0) \approx I(\theta_0)^{-1} \cdot \frac{1}{\sqrt{n}} \sum_{i=1}^n s(\theta_0; X_i),
$$
and $\frac{1}{\sqrt{n}} \sum s(\theta_0; X_i) \xrightarrow{d} N(0, I(\theta_0))$. This representation shows that the MLE is asymptotically linear with influence function $\psi(X_i) = I(\theta_0)^{-1} s(\theta_0; X_i)$.

The asymptotic variance of $\hat{\theta}_n$ is
$$
\operatorname{Var}(\psi(X_i)) = I(\theta_0)^{-1} \operatorname{Var}(s(\theta_0; X_i)) I(\theta_0)^{-1} = I(\theta_0)^{-1} I(\theta_0) I(\theta_0)^{-1} = I(\theta_0)^{-1}.
$$
Since $\sqrt{n} (\hat{\theta}_n - \theta_0)$ converges to $N(0, I(\theta_0)^{-1})$, the asymptotic variance is exactly the CRLB.

Consider any other consistent and asymptotically normal estimator $\tilde{\theta}_n$ with asymptotic variance $\tilde{\Sigma}(\theta_0)$. Under the same model, the convolution theorem (Hájek–Le Cam) implies that the asymptotic distribution of any regular estimator can be written as the convolution of $N(0, I(\theta_0)^{-1})$ with some other distribution, meaning its asymptotic covariance matrix is at least $I(\theta_0)^{-1}$ in positive semidefinite order:
$$
\tilde{\Sigma}(\theta_0) \ge I(\theta_0)^{-1}.
$$
Since the MLE achieves $I(\theta_0)^{-1}$, it is efficient.
>[!remark]
>Consistency conditions (compact parameter space, identifiability, upper semicontinuity) are **global and topological**, ensuring existence and convergence of the extremum. Asymptotic normality/efficiency conditions (interior point, second/third-order differentiability, positive definite information matrix) are **local and smooth**, enabling a local quadratic expansion.
>
Consistency allows the parameter to be on the boundary. Asymptotic normality **requires an interior point**; otherwise, the Taylor expansion fails and the limiting distribution is non-standard.