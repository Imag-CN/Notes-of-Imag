>[!problem]
>Let $f$ be a $2\pi$-periodic function on $\mathbb{R}$.  
>For $n \geq 1$, define Fourier coefficients  
>$$
>a_n = \frac{1}{\pi} \int_{-\pi}^{\pi} f(x) \cos(nx)  dx
>$$  
>$$
>b_n = \frac{1}{\pi} \int_{-\pi}^{\pi} f(x) \sin(nx)  dx
>$$  
>Discuss the decay rate of $a_n$ and $b_n$ when  
>(i) $f$ is Riemann integrable.
>(ii) $f$ is continuous.  
>(iii) $f$ is $C^k$.
>(v) $f$ is of bounded variation.
>(vi) $f$ is Lipschitz.

**(i) Riemann integrable function**  
By Riemann-Lebesgue lemma: $a_n, b_n = o(1)$ (tend to 0, but no specific rate).

**(ii) Continuous function**  
Generally same as Riemann integrable case: $a_n, b_n = o(1)$.

**(iii) $C^k$ function**  
If $f \in C^k$, then $a_n, b_n = O(n^{-k})$.  
For $f \in C^k$ with $f^{(j)}$ periodic for $j < k$: $a_n, b_n = O(n^{-(k+1)})$.

**(v) Bounded variation function**  
If $f$ has bounded variation: $a_n, b_n = O(n^{-1})$.

**(vi) Lipschitz function**  
If $f$ is Lipschitz: $a_n, b_n = O(n^{-1})$.  
Lipschitz implies bounded variation, so same decay rate.