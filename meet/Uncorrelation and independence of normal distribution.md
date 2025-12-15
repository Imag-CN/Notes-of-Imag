___

>[!problem]
>If the random vector $(X, Y)$ follows a bivariate normal distribution, then $X$ and $Y$ are independent if and only if they are uncorrelated (i.e., $\operatorname{Cov}(X,Y)=\operatorname{Corr}(X,Y)=0$ or $E[XY]=E[X]E[Y]$).

**Proof:** Independent $\Rightarrow$ Uncorrelated holds for any distributions. So we only have to show Uncorrelated $\Rightarrow$ Independent.

Since $(X, Y)$ follows a bivariate normal distribution, its joint probability density function is given by:

$f(x, y) =$
$$
\frac{1}{2\pi\sigma_X\sigma_Y\sqrt{1-\rho^2}} \exp\left[ -\frac{1}{2(1-\rho^2)} \left( \frac{(x-\mu_X)^2}{\sigma_X^2} - 2\rho\frac{(x-\mu_X)(y-\mu_Y)}{\sigma_X\sigma_Y} + \frac{(y-\mu_Y)^2}{\sigma_Y^2} \right) \right]
$$

where:
- $\mu_X=E[X], \mu_Y=E[Y]$;
- $\sigma_X^2=D[X], \sigma_Y^2=D[X]$;
- $\rho=\operatorname{Corr}(X,Y)$.

And its marginal distributions follow:
$$
f_{X}(x)=\dfrac{1}{\sqrt{ 2\pi }\sigma_{x}}\exp\left[-\dfrac{(x-\mu_{x})^2}{2\sigma_{x}}  \right] 
$$
$$
f_{Y}(y)=\dfrac{1}{\sqrt{ 2\pi }\sigma_{y}}\exp\left[-\dfrac{(y-\mu_{y})^2}{2\sigma_{y}}  \right] 
$$

Since uncorrelated, $\rho=0$, thus
$$
f(x, y) = \frac{1}{2\pi\sigma_X\sigma_Y} \exp\left[ -\frac{1}{2} \left( \frac{(x-\mu_X)^2}{\sigma_X^2}  + \frac{(y-\mu_Y)^2}{\sigma_Y^2} \right) \right]=f_{X}(x)\cdot f_{Y}(y)
$$
Thus $X$ and $Y$ are independent.
___
>[!failure]
>If $X$ and $Y$ both follow normal distribution and are uncorrelated, then $X$ and $Y$ are independent.

This proposition fails because the random vector $(X, Y)$ doesn't necessarily follow a bivariate normal distribution; instead, it can be rather wired.

**Counterexample:**
Let $X \sim N(0,1),Z\sim U\{ -1,1 \}$ are independent, let $Y=XZ$.

Since
$$
Y=
\begin{cases}
X \sim N(0,1)&, Z=1,\\
-X \sim N(0,1)&,Z=-1,\\
\end{cases}
$$
we have $Y\sim N(0,1)$.

Since $X$ and $Z$ are independent, $X^2$ and $Z$ are also independent, so we have $E[XY]=E[XXZ]=E[X^2]E[Z]=0$. Considering $E[X]=0$, we obtain that $E[X]E[Y]=E[XY]=0$, thus $X$ and $Y$ are correlated.

Since $X,Y\sim N(0,1)$, we have $P(X>1)=P(Y>1)=1-\Phi(1)\approx 0.1587$. However, $P(X>1,Y>1)=P(X>1,Z=1)=P(X>1)\cdot P(Z=1)=\dfrac{1}{2}(1-\Phi(1))$, which implies $P(X>1)\cdot P(Y>1)\neq P(X>1,Y>1)$. Therefore, $X$ and $Y$ are not independent.
___

>[!tip] Remark
>The random vector $(X, Y)$ follows a bivariate normal distribution, if and only if any real linear combination of $X$ and $Y$ follows a normal distribution.

**Proof:** 
Denote $\mu_X = E[X]$, $\mu_Y = E[Y]$, $\sigma_X^2 = D[X]$, $\sigma_Y^2 = D[Y]$, $\sigma_{XY} = \operatorname{Cov}(X,Y)$.
**($\Rightarrow$)**
The joint MGF of $(X,Y)$ is:
$$M_{X,Y}(s, t) = E[e^{sX + tY}] = \exp\left( s\mu_X + t\mu_Y + \frac{1}{2}(s^2 \sigma_X^2 + 2st \sigma_{XY} + t^2 \sigma_Y^2) \right),$$
Now, for $Z = aX + bY$:
$$M_Z(t) = M_{X,Y}(a t, b t) = \exp\left( a t \mu_X + b t \mu_Y + \frac{1}{2}(a^2 t^2 \sigma_X^2 + 2ab t^2 \sigma_{XY} + b^2 t^2 \sigma_Y^2) \right).$$
This simplifies to:
$$M_Z(t) = \exp\left( t (a\mu_X + b\mu_Y) + \frac{1}{2} t^2 (a^2 \sigma_X^2 + 2ab \sigma_{XY} + b^2 \sigma_Y^2) \right).$$
This is the MGF of a normal distribution with mean $a\mu_X + b\mu_Y$ and variance $a^2 \sigma_X^2 + 2ab \sigma_{XY} + b^2 \sigma_Y^2$.  
Hence $Z$ is normal for all $a, b \in \mathbb{R}$.

**($\Leftarrow$)**
Let $Z = sX + tY$, then $Z$ is a normal distribution with mean $s\mu_X + t\mu_Y$ and variance $s^2 \sigma_X^2 + 2st \sigma_{XY} + t^2 \sigma_Y^2$.  
Thus the joint MGF of $(X,Y)$ is:
$$M_{X,Y}(s, t) = E[e^{sX + tY}] =E[e^{ Z }]= \exp\left( s\mu_X + t\mu_Y + \frac{1}{2}(s^2 \sigma_X^2 + 2st \sigma_{XY} + t^2 \sigma_Y^2) \right),$$
This is the MGF of a bivariate normal distribution, therefore the random vector follows a bivariate normal distribution.
