>[!problem] Gambler's ruin problem
>Consider the following game: You begin with $n$ coins. In each round of the game, you win a coin have with probability $p$ and lose a coin with $1-p$. The game continues infinitely until you lose all the coins. What' s the probability $p_n$ that the game ends?

We have recursive relation and boundary condition:
$$p_n=p\cdot p_{n+1}+(1-p)\cdot p_{n-1},p_0=1.$$
Solve the characteristic equation:
$$
x=px^2+1-p\Rightarrow x_1=1,x_2=\frac{1-p}{p}.
$$
Thus
$$
p_n=c_1+c_2\left(\frac{1-p}{p}\right)^n,p_0=c_1+c_2=1.
$$
When $p=1/2$, $p_n=c_1+c_2=1$.

When $p<1/2$, then $\left(\dfrac{1-p}{p}\right)^n$ is boundless, but $p_n$ is bounded, so $c_2=0$.Thus $p_n=p_0=1$.

When $p>1/2$, then the expectation of the coins you gain in each round is $p-1/2>0$, so for $n$ sufficiently large, you tend to always win coins in the long run. This is to say $\lim_{n\rightarrow\infty}p_n=0$, so $c_1=0,c_2=1,p_n=\left(\dfrac{1-p}{p}\right)^n$.

In conclusion,
$$
p_n=\begin{cases}
1&,p\leq1/2,\\
\left(\dfrac{1-p}{p}\right)^n&,p>1/2.\\
\end{cases}
$$
___
We need a more solid prove to illustrate that when $p>1/2$, $\lim_{n\rightarrow\infty}p_n=0$.

To simplify, let $n$ be even (if not, start at the second round), and substitute $n$ with $2n$.

Let $Q_{k}$ be the probability that you lose at exactly the $k$th round, then we have:
$$
Q_{k}=
\begin{cases}
0&,\text{ if }k<2n\text{ or }k\text{ is odd}, \\
\binom{2n+2m}{m} \dfrac{2n+1}{2n+m+1} p^m (1-p)^{2n+m}=0 &,\text{ where }m=1,2,\dots
\end{cases}
$$
The probability that the game ends is $\sum_{k\geq 1}Q_{k}$.
Thus we only have to show that 
$$
\lim_{ n \to \infty } \sum_{m\geq 0} \binom{2n+2m}{m} \dfrac{2n+1}{2n+m+1} p^m (1-p)^{2n+m}=0.
$$
Consider generate function. Let
$$
f(x)=\sum_{m\geq 0} \binom{2n+2m}{m} \dfrac{2n+1}{2n+m+1} x^m
$$
By taking the limit of the ratio of consecutive terms, we can determine that $R=\dfrac{1}{4}$ is the radius of convergence.​

By generalized binomial theorem, we have
$$
f(x)=\dfrac{1}{\sqrt{ 1-4x }}\left( \dfrac{1+\sqrt{ 1-4x }}{2x} \right)^{2n+1}.
$$
Thus
$$
\sum_{m\geq 0} \binom{2n+2m}{m} \dfrac{2n+1}{2n+m+1} p^m (1-p)^{2n+m}=f(p(1-p))(1-p)^{2n}=\left( \dfrac{1+|2p-1|}{2p} \right)^{2n} .
$$
We acually directly derive the answer, no need to illustrate that when $p>1/2$, $\lim_{n\rightarrow\infty}p_n=0$.

