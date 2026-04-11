___

>[!problem] Problem 1
>Assume $X_{1}$, $X_{2}$ are a random sample from a population $N(0,\sigma^{2})$
>a. Show that $X_{1}+X_{2}$ and $X_{1}-X_{2}$ are independent.
>b. Show that $\frac{(X_{1}+X_{2})^{2}}{(X_{1}-X_{2})^{2}}\sim F(1,1)$.

**Proof:**
**a.** Let $Y_1 = X_1 + X_2$, $Y_2 = X_1 - X_2$.
The mgf:
$$
M_{(Y_{1},Y_{2})}(t_1, t_2) = E[\exp(t_1 Y_1 + t_2 Y_2)] = E[\exp((t_1+t_2)X_1 + (t_1-t_2)X_2)].
$$
By independence, $M_{(Y_{1},Y_{2})}(t_1, t_2) = E[e^{(t_1+t_2)X_1}] \cdot E[e^{(t_1-t_2)X_2}]$.
For $X \sim N(0, \sigma^2)$, $E[e^{tX}] = \exp(\frac{1}{2}\sigma^2 t^2)$.
Thus, $M_{(Y_{1},Y_{2})}(t_1, t_2) = \exp\left( \frac{1}{2}\sigma^2 (t_1+t_2)^2 \right) \cdot \exp\left( \frac{1}{2}\sigma^2 (t_1-t_2)^2 \right) = \exp(\sigma^2(t_1^2 + t_2^2))$.
This factors as $M(t_1, 0) \cdot M(0, t_2)$, implying $Y_1$ and $Y_2$ are independent.

**b.** From (a), $Y_1 \sim N(0, 2\sigma^2)$, $Y_2 \sim N(0, 2\sigma^2)$, and they are independent.
Thus, $\frac{Y_1^2}{(2\sigma^2)} \sim \chi^2_{(1)}$ and $\frac{Y_2^2}{(2\sigma^2)} \sim \chi^2_{(1)}$.
Therefore,
$$
\frac{(X_1+X_2)^2}{(X_1-X_2)^2} = \frac{Y_1^2 / (2\sigma^2)}{Y_2^2 / (2\sigma^2)} = \frac{\chi^2_{(1)}/1}{\chi^2_{(1)}/1} \sim F(1,1).
$$
___

>[!problem] Problem 2
>One characteristic of a car's storage console that is checked by the manufacturer is the time in seconds that it takes for the lower storage compartment door to open completely. A random sample of size $n = 5$ yielded the following times:
>$1.1, 0.9, 1.4, 1.1, 1.0$
>a. Find the order statistics.
>b. Find the empirical CDF.
>c. Find the sample mean, $\bar{x}(\bar{x}=\frac{1}{n}\sum_{i=1}^{n}x_{i})$.
>d. Find the sample variance, $s^{2}(\frac{1}{n-1}\sum_{i=1}^{n}(x_{i}-\bar{x})^{2})$.

**Proof:**
**a.** Order statistics: $x_{(1)} = 0.9, x_{(2)} = 1.0, x_{(3)} = 1.1, x_{(4)} = 1.1, x_{(5)} = 1.4$.

**b.** Empirical CDF:
$$
\hat{F}_n(t) = \begin{cases}
0, & t < 0.9 \\
1/5, & 0.9 \le t < 1.0 \\
2/5, & 1.0 \le t < 1.1 \\
4/5, & 1.1 \le t < 1.4 \\
1, & t \ge 1.4
\end{cases}
$$
**c.** Sample mean:
$$
\bar{x} = \frac{1}{5}(1.1+0.9+1.4+1.1+1.0) = \frac{5.5}{5} = 1.1.
$$

**d.** Sample variance:
$$s^2 = \frac{1}{5-1}[(1.1-1.1)^2 + (0.9-1.1)^2 + (1.4-1.1)^2 + (1.1-1.1)^2 + (1.0-1.1)^2]$$
$$= \frac{1}{4}[0 + 0.04 + 0.09 + 0 + 0.01] = \frac{0.14}{4} = 0.035.$$
___

>[!problem] Problem 3
>Let $Y_{1}<Y_{2}<\dots<Y_{n}$ be the order statistics of a random sample of size n from an exponential distribution with pdf $f(x)=e^{-x}$, $0<x<\infty$.
>Find the pdf of $Y_{r}$, $r=1,\dots,n$.

**Proof:**
The general formula for the pdf of the $r$-th order statistic $Y_r$ from a sample of size $n$ with pdf $f(x)$ and CDF $F(x)$ is
$$
g_r(y) = \frac{n!}{(r-1)!(n-r)!} [F(y)]^{r-1} [1-F(y)]^{n-r} f(y)
$$
for $y$ in the support of $f$.

For the given exponential distribution $X \sim \text{Exp}(1)$, we have $f(x) = e^{-x}$ and $F(x) = 1 - e^{-x}$, for $x > 0$.

Substitute $f(y)$ and $F(y)$ into the formula:
$$
g_r(y) = \frac{n!}{(r-1)!(n-r)!} \left[1 - e^{-y}\right]^{r-1} \left[e^{-y}\right]^{n-r} \cdot e^{-y} \quad \text{ for } y > 0.
$$

Simplify the exponent of $e$:
$$
g_r(y) = \frac{n!}{(r-1)!(n-r)!} \left(1 - e^{-y}\right)^{r-1} e^{-y(n-r+1)}\quad \text{ for } y > 0.
$$
___

>[!problem] Problem 4
>Let $X_1,X_2,...,X_n$ be a random sample of size n from the normal distribution with mean $\mu$ and variance $\sigma^2$.
>Denote $\bar{X}_n=\frac{1}{n}\sum_{i=1}^n X_i$, $S_n^2=\frac{1}{n-1}\sum_{i=1}^n(X_i-\bar{X}_n)^2$ the sample mean and variance respectively.
>Find the minimum value of n satisfies the following conditions.
>a. $P(S_n^2/\sigma^2 \le 1.5) \ge 0.95$.
>b. $P(|S_n^2/\sigma^2 - 1| \le \frac{1}{2}) \ge 0.8$.

**Proof:**
**a.** Since $\frac{(n-1)S_n^2}{\sigma^2} \sim \chi^2_{(n-1)}$, the inequality becomes:
$$
P\left( \chi^2_{(n-1)} \le 1.5(n-1) \right) \ge 0.95.
$$
This implies that $1.5(n-1)$ must be greater than or equal to the $0.95$ quantile of the $\chi^2$ distribution with $(n-1)$ degrees of freedom: $1.5(n-1) \ge \chi^2_{0.95, (n-1)}$.

Checking $\chi^2$ distribution tables, we find that: 
- For $n-1 = 26$, $1.5 \times 26 = 39 \ge \chi^2_{0.95, 26} \approx 38.885$.
- For $n-1 = 25$, $1.5 \times 25 = 37.5 < \chi^2_{0.95, 25} \approx 37.652$.
Therefore, the minimal $n-1$ is $26$, so the minimal $n$ is $27$.

**b.** We need the smallest $n$ such that $P\left(|S_n^2-\sigma^2| \le \frac{1}{2} \sigma^2 \right) \ge 0.8$.
This is equivalent to $P(0.5 \le S_n^2/\sigma^2 \le 1.5) \ge 0.8$.
Using the distribution $\frac{(n-1)S_n^2}{\sigma^2} \sim \chi^2_{(n-1)}$, the condition becomes:
$$
P\left( 0.5(n-1) \le \chi^2_{(n-1)} \le 1.5(n-1) \right) \ge 0.8.
$$
That is, $F_{\chi^2_{(n-1)}}(1.5(n-1)) - F_{\chi^2_{(n-1)}}(0.5(n-1)) \ge 0.8$.
By evaluating the cumulative distribution function for increasing degrees of freedom:
- For $n-1 = 12$, the probability is approximately $0.791 < 0.8$.
- For $n-1 = 13$, the probability is approximately $0.805 > 0.8$.
Therefore, the minimal $n-1$ is $13$, and the minimal $n$ is $14$.
___

>[!problem] Problem 5
>Assume $X_{i}\sim N(\mu,\sigma_{i}^{2})$, $i=1,\dots,n$, and are independent. Define
>$$U=\frac{\sum_{i=1}^{n}\frac{X_{i}}{\sigma_{i}^{2}}}{\sum_{i=1}^{n}\frac{1}{\sigma_{i}^{2}}}, V=\sum_{i=1}^{n}\left(\frac{X_{i}-U}{\sigma_{i}}\right)^{2}$$
>a. Show that $U$ is normally distributed.
>b. Show that $U$, $V$ are independent.
>c. Show that $V\sim\chi^{2}(n-1)$.

**Proof:**
**a.** $U$ is a linear combination of independent normal variables $X_i$, hence normal.

Futhermore, let $w = \sum_{i=1}^{n} \frac{1}{\sigma_i^2}$, then:
$$E[U]=\frac{\sum_{i=1}^{n}\frac{\mu}{\sigma_{i}^{2}}}{w}=\mu, \quad Var[U]=\frac{\sum_{i=1}^{n}\frac{\sigma_{i}^{2}}{\sigma_{i}^{2}}}{w}=\frac{n}{w}$$
Thus $U \sim  N\left( \mu,\frac{n}{w} \right)$.

**b.** Let $Y_i = X_i - U$, let $\boldsymbol{ X }=(X_{1},\dots,X_{n})^T$, let $\boldsymbol{ a }=(a_{1},\dots,a_{n})^T$ where $a_{j}=1 /w\sigma_{j}^2$, let $\boldsymbol{ b }_{i}=(b_{i1},\dots ,b_{in})$ where $b_{ij}=1-1 /w\sigma_{j}^2$ if $i=j$, otherwise $b_{ij}=-1 /w\sigma_{j}^2$.
Then $U,Y_{i}$ can be written as $U=\boldsymbol{ a }^T\boldsymbol{ X },Y_{i}=\boldsymbol{ b }_{i}^T\boldsymbol{ X }$. Note that:
$$
\sum_{j}a_{j}=1,\sum_{j}b_{ij}=0,\sum_{j}\sigma_{j}^2a_{j}=\dfrac{n}{w},\sum_{j}\sigma_{j}^2a_{j}b_{ij}=0\tag{\dagger}
$$
The mgf of $(U,Y_{1},\dots Y_{n})$ is:
$$
\begin{align}
M_{(U,Y_{1},\dots Y_{n})}(t,t_{1},\dots ,t_{n})&=E[\exp(tU+t_{1}Y_{1}+\dots+t_{n}Y_{n})] \\
&=E[\exp((t\boldsymbol{ a }^T+t_{1}\boldsymbol{ b }_{1}^T+\dots+t_{n}\boldsymbol{ b }_{n}^T)\boldsymbol{ X })]
\end{align}
$$
Let $t\boldsymbol{ a }^T+t_{1}\boldsymbol{ b }_{1}^T+\dots+t_{n}\boldsymbol{ b }_{n}^T=\boldsymbol{ s }^T=(s_{1},\dots,s_{n})$, where $s_{j}=ta_{j}+t_{1}b_{1j}+\dots+t_{n}b_{nj}$. Then
$(t\boldsymbol{ a }^T+t_{1}\boldsymbol{ b }_{1}^T+\dots+t_{n}\boldsymbol{ b }_{n}^T)\boldsymbol{ X }=\boldsymbol{ s }^T\boldsymbol{ X }$ is a linear combination of independent normal variables $X_i$, thus normal. Furthermore, according to $(\dagger)$:
$$
E[\boldsymbol{ s }^T\boldsymbol{ X }]=(s_{1}+\dots+s_{n})\mu=\mu t
$$
$$
Var[\boldsymbol{ s }^T\boldsymbol{ X }]=s_{1}^2\sigma_{1}^2+\dots+s_{n}^2\sigma_{n}^2= \dfrac{nt^2}{w}+F(t_{1},\dots,t_{n})
$$
where $F(t_{1},\dots,t_{n})$ is a function of vector $(t_{1},\dots,t_{n})$
Thus $\boldsymbol{ s }^T\boldsymbol{ X } \sim N\left(\mu t,\dfrac{nt^2}{w}+F(t_{1},\dots,t_{n}) \right)$, and
$$
\begin{align}
M_{(U,Y_{1},\dots Y_{n})}(t,t_{1},\dots ,t_{n})&=E[\exp(\boldsymbol{ s }^T\boldsymbol{ X })] \\
&=\exp \left(\mu t +1/2 \cdot \left( \dfrac{nt^2}{w}+F(t_{1},\dots,t_{n}) \right)  \right) \\
&=\exp(\mu t+ 1 /2 \cdot \dfrac{n}{w}t^2 )\cdot \exp(1 /2 \cdot F(t_{1},\dots,t_{n}))
\end{align}
$$
Let the mgf of $U$ be $M_{U}(t)$ and let the mgf of $(Y_{1},\dots,Y_{n})$ be $M_{(Y_{1},\dots,Y_{n})}(t_{1},\dots,t_{n})$. Since $U \sim  N\left( \mu,\frac{n}{w} \right),M_{U}(t)=\exp(\mu t+ 1 /2 \cdot \dfrac{n}{w}t^2 )$. Then
$$
\begin{align}
M_{(Y_{1},\dots,Y_{n})}(t_{1},\dots,t_{n})&=M_{(U,Y_{1},\dots,Y_{n})}(0,t_{1},\dots,t_{n}) \\
&=\exp(1 /2 \cdot F(t_{1},\dots,t_{n}))
\end{align}
$$
So $M_{(U,Y_{1},\dots,Y_{n})}(t,t_{1},\dots,t_{n})=M_{U}(t)\cdot M_{(Y_{1},\dots,Y_{n})}(t_{1},\dots,t_{n})$, indicating that $U$ and $(Y_{1},\dots,Y_{n})$ are independent. And since $V$ is a function of $(Y_{1},\dots,Y_{n})$, $U$ and $V$ are independent.

**c.** Let $W= \left( \dfrac{(U-\mu)}{\sqrt{ n /w }} \right)^2$, then $W\sim \chi^2(1),W+V=\sum_{i=1}^{n}\left( \dfrac{X_{i}-\mu}{\sigma_{i}} \right)^2\sim \chi^2(n)$ and the mgf of $W$ and $W+V$ is 
$$
M_{W}(t)=(1-2t)^{-1 /2},M_{W+V}(t)=(1-2t)^{-n /2}.
$$
Since $U$ and $V$ are independent, $W$ and $V$ are independent too. Hence, we have $M_{W+V}(t)=M_{W}(t)\cdot M_{V}(t)$, so the mgf of $V$ is $M_{V}(t)=(1-2t)^{-(n-1) /2}$. Therefore, we have $V\sim\chi^{2}(n-1)$.