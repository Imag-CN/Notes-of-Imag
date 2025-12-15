>[!problem] Problem 1
>Roll a pair of four-sided dice. Denote $Z_{i}$, the outcome of die $i$, $i=1,2$. Assume $P(Z_{i}=1)=\frac{6}{12}$, $P(Z_{i}=2)=\frac{1}{12}$, $P(Z_{i}=3)=\frac{2}{12}$, $P(Z_{i}=4)=\frac{3}{12}$. Let $X$ denote the smaller and $Y$ the larger outcome on the dice, i.e., $X=\min\{Z_{1},Z_{2}\}$, $Y=\max\{Z_{1},Z_{2}\}$.
>
>a. Find the joint pmf of $(X,Y)$.
>
>b. Derive the marginal pmfs of $X,Y$ from their joint pmf.
>
>c. Find the conditional pmf of $X$ given $Y=3$.
>
>d. Determine if $X,Y$ are independent or not.
#### a.
The sample space is $\{1,2,3,4\}^2$.
For $x < y$ we have:
$$
P(X=x, Y=y) = P(Z_1=x, Z_2=y) + P(Z_1=y, Z_2=x) = 2P(Z=x)P(Z=y).
$$
For $x = y$ we have:
$$
P(X=x, Y=x) = P(Z_1=x, Z_2=x) = P(Z=x)^2.
$$
   Using $P(Z=1)=6/12$, $P(Z=2)=1/12$, $P(Z=3)=2/12$, $P(Z=4)=3/12$:
   - $P(X=1,Y=1) = (6/12)^2 = 36/144$
   - $P(X=1,Y=2) = 2×(6/12)×(1/12) = 12/144$
   - $P(X=1,Y=3) = 2×(6/12)×(2/12) = 24/144$
   - $P(X=1,Y=4) = 2×(6/12)×(3/12) = 36/144$
   - $P(X=2,Y=2) = (1/12)^2 = 1/144$
   - $P(X=2,Y=3) = 2×(1/12)×(2/12) = 4/144$
   - $P(X=2,Y=4) = 2×(1/12)×(3/12) = 6/144$
   - $P(X=3,Y=3) = (2/12)^2 = 4/144$
   - $P(X=3,Y=4) = 2×(2/12)×(3/12) = 12/144$
   - $P(X=4,Y=4) = (3/12)^2 =9/144$
   All other probabilities are 0.
#### b.
   - $P(X=1) = 36/144 + 12/144 + 24/144 + 36/144 = 108/144$
   - $P(X=2) = 1/144 + 4/144 + 6/144 = 11/144$
   - $P(X=3) = 4/144 + 12/144 = 16/144$
   - $P(X=4) = 9/144$
   - $P(Y=1) = 36/144$
   - $P(Y=2) = 12/144 + 1/144 = 13/144$
   - $P(Y=3) = 24/144 + 4/144 + 4/144 = 32/144$
   - $P(Y=4) = 36/144 + 6/144 + 12/144 + 9/144 = 63/144$
#### c.
$$
P(X=x|Y=3) = \frac{P(X=x,Y=3)}{P(Y=3)}.
$$
   - $P(X=1|Y=3) = (24/144)/(32/144) = 3/4$
   - $P(X=2|Y=3) = (4/144)/(32/144) = 1/8$
   - $P(X=3|Y=3) = (4/144)/(32/144) = 1/8$
   - $P(X=4|Y=3) = 0$
#### d.
$$
P(X=4,Y=1) =0, P(X=4)P(Y=1) \neq 0
$$
$$
\Rightarrow P(X=4,Y=1) \neq P(X=4)P(Y=1).
$$
So $X$ and $Y$ are dependent.
___
>[!problem] Problem 2
>Let the joint pdf of $X$ and $Y$ take the form
>$$f(x,y)=\left\{\begin{array}{ll}c,&\text {if }0\leq x\leq y\leq 4\\ 0,&\text{otherwise}\end{array}\right.$$
>
>a. Determine the value of constant $c$.
>
>b. Find the marginal pdfs of $X,Y$.
>
>c. Determine if $X,Y$ are independent or not.
>
>d. Find the conditional pdf of $X$ given $Y=3$.
#### a.
$$
\int_0^4\int_x^4 c\,dy\,dx = 1 \Rightarrow c\int_0^4(4-x)dx = 1 \Rightarrow c[4x - x^2/2]_0^4 = 1,
$$
$$
c(16 - 8) = 1 \Rightarrow 8c = 1 \Rightarrow c = 1/8.
$$
#### b.
$$f_X(x) = \int_x^4 (1/8)dy = (4-x)/8,\text{ for }0 \leq x \leq 4,$$
$$f_Y(y) = \int_0^y (1/8)dx = y/8, \text{ for }0 \leq y \leq 4.$$
#### c.
$$
f(0,0) =1/8, f_X(0)f_Y(0)=0\Rightarrow f(0,0)\neq f_X(0)f_Y(0).
$$
So $X$ and $Y$ are dependent.
#### d.
$$
f_{X|Y}(x|3) = \frac{f(x,3)}{f_Y(3)} = \frac{1/8}{3/8} = 1/3,\text{ for } 0 \leq x \leq y=3,
$$
$$
f_{X|Y}(x|3)=0, \text{ for } x>y=3.
$$
___
>[!problem] Problem 3
>Let $X$ and $Y$ be independent identical distributed random variables with pdf $f(x)=e^{-x}$, $0<x<\infty$.
>
>a. Find the joint pdf of $X,Y$.
>
>b. Let $U=X+Y$, $W=X-Y$. Find the joint pdf of $U,W$.
>
>c. Find the marginal pdf of $W$.
>
>d. Find the marginal pdf of $U$.
>
>e. Determine if $U,W$ are independent or not.
#### a.
Since $X$ and $Y$ are independent:
$$
f_{X,Y}(x,y) = f_X(x)f_Y(y) =  e^{-(x+y)}, \quad 0<x<\infty, 0<y<\infty.
$$
#### b.
Inverse: $X = \frac{U+W}{2}$, $Y = \frac{U-W}{2}$.
Jacobian: $J = \left|\frac{\partial(x,y)}{\partial(u,w)}\right| = \begin{vmatrix}1/2 & 1/2 \\ 1/2 & -1/2\end{vmatrix} = -1/4 - 1/4 = -1/2 \Rightarrow |J| = 1/2$.
Support: $x>0 \Rightarrow u+w>0$, $y>0 \Rightarrow u-w>0\Rightarrow|w|<u$, $u>0$
$$
f_{U,W}(u,w) = f_{X,Y}(x,y)|J| = e^{-u} \cdot \frac{1}{2} = \frac{1}{2}e^{-u}, \quad u>0, |w|<u.
$$
#### c.
$$f_W(w) = \int_{|w|}^{\infty} f_{U,W}(u,w)du = \int_{|w|}^{\infty} \frac{1}{2}e^{-u}du = \frac{1}{2}e^{-|w|}, \quad -\infty<w<\infty$$
#### d.
$$
f_U(u) = \int_{-u}^{u} f_{U,W}(u,w)dw = \int_{-u}^{u} \frac{1}{2}e^{-u}dw = \frac{1}{2}e^{-u} \cdot 2u = ue^{-u}, \quad u>0.
$$
#### e.
$$
f_{U,W}(0,0) =\dfrac{1}{2},f_U(0)f_W(0) =0\Rightarrow f_{U,W}(0,0)\neq f_U(0)f_W(0).
$$
So $U$ and $W$ are dependent.
___

>[!problem] Problem 4
>Assume distributions of the incomes in two cities follow the two Pareto-type pdfs
>$$f_X(x)=\frac{2}{x^3},\quad 1\leq x<\infty$$
>$$f_Y(y)=\frac{3}{y^4},\quad 1\leq y<\infty$$
>Here one unit represents $\$20,000$. One person with income is selected at random from each city. Let $X$ and $Y$ be their respective incomes.
>
>a. Find the joint pdf of $X,Y$.
>
>b. Compute $P(Y<X)$.
#### a.
Since $X$ and $Y$ are independent:
$$
f_{X,Y}(x,y) = f_X(x)f_Y(y) = \frac{2}{x^3} \cdot \frac{3}{y^4} = \frac{6}{x^3y^4}, \quad x\geq1, y\geq1.
$$
#### b.
$$
\begin{align}
P(Y<X) &= \int_{1}^{\infty}\int_{1}^{x} \frac{6}{x^3y^4}dydx  \\
&= \int_{1}^{\infty}\frac{6}{x^3}\left[\int_{1}^{x}\frac{1}{y^4}dy\right]dx \\
&=\int_{1}^{\infty}\frac{6}{x^3} \cdot \frac{1}{3}\left(1 - \frac{1}{x^3}\right)dx\\
&=\frac{3}{5}. \\
\end{align}
$$
___
>[!problem] Problem 5
>Three drugs are being tested for use as the treatment of a certain disease. Let $p_{1},p_{2}$, and $p_{3}$ represent the probabilities of success for the respective drugs. As three patients come in, each is given one of the drugs in a random order. After n=10 "triples" and assuming independence, compute the probability that the maximum number of successes with one of the drugs exceeds eight if, in fact, $p_{1}=p_{2}=p_{3}=0.7$.

Let $M = \max(S_1, S_2, S_3)$ where $S_i \sim \text{Binomial}(10, 0.7)$ are independent.
We want $P(M > 8)$, so we use complement: $P(M > 8) = 1 - P(M \leq 8)$

$P(M \leq 8) = P(S_1 \leq 8, S_2 \leq 8, S_3 \leq 8) = [P(S_i \leq 8)]^3$

For $S_i \sim \text{Binomial}(10, 0.7)$:
- $P(S_i \leq 8) = 1 - P(S_i = 9) - P(S_i = 10)$
- $P(S_i = 9) = \binom{10}{9}(0.7)^9(0.3)^1 = 10 \cdot 0.04035 \cdot 0.3 = 0.12106$
- $P(S_i = 10) = (0.7)^{10} = 0.02825$
- $P(S_i \leq 8) = 1 - 0.12106 - 0.02825 = 0.85069$

$P(M \leq 8) = (0.85069)^3 = 0.6156$
$P(M > 8) = 1 - 0.6156 = 0.3844$
___
>[!problem] Problem 6
>The alleles for eye colour in a certain male fruit fly are (R, W). The alleles for eye colour in the mating female fruit fly are (R, W). Their offspring receive one allele for eye colour from each parent. If an offspring ends up with either (W, W), (R, W), or (W, R), its eyes will look white. Let X equal the number of offspring having white eyes. Let Y equal the number of white-eyed offspring having (R, W) or (W, R) alleles.
>
>a. If the total number of offspring is n=500, how is X distributed?
>
>b. Given that X=400, how is Y distributed?

#### a. 
Possible allele combinations from parents (R,W) × (R,W):
- RR: probability 1/4 (red eyes)
- RW: probability 1/4 (white eyes)  
- WR: probability 1/4 (white eyes)
- WW: probability 1/4 (white eyes)

$P(\text{white eyes}) = 1/4 + 1/4 + 1/4 = 3/4$

Since offspring are independent, $X \sim \text{Binomial}(500, 3/4)$
#### b.

Given white eyes, the conditional probabilities are:
- $P(\text{RW or WR} | \text{white}) = \frac{1/4 + 1/4}{3/4} = \frac{1/2}{3/4} = 2/3$
- $P(\text{WW} | \text{white}) = \frac{1/4}{3/4} = 1/3$

Since the 400 white-eyed offspring are independent, $Y | X=400 \sim \text{Binomial}(400, 2/3)$