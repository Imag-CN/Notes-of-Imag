### 1. Problem 1
> [!problem] 
For  $x, y \in \mathbb{R}$, define
$$d_1(x, y) = (x - y)^2,$$
$$d_2(x, y) = \sqrt{|x - y|},$$
$$d_3(x, y) = |x^2 - y^2|,$$
$$d_4(x, y) = |x - 2y|,$$
$$d_5(x, y) = \frac{|x - y|}{1 + |x - y|}.$$
Determine for each whether it is a metric or not.

#### 1.1 $d_1$ is not a metric
$d_1(0,1)+d_1(1,2)=2<d_1(0,2)=4$.
#### 1.2 $d_2$ is a metric
(a)$d_2(x,y)= \sqrt{|x - y|} \geq 0, d_2(x,y)=0 \Leftrightarrow \sqrt{|x - y|}=0 \Leftrightarrow x=y$,
(b)$d_2(x,y)= \sqrt{|x - y|}= \sqrt{|y - x|}=d_2(y,x)$,
(c)
$$
\begin{aligned}
&d_2(x,y)+d_2(y,z) \geq d_2(x,z)\\
\Leftrightarrow & (d_2(x,y)+d_2(y,z))^2 \geq d_2(x,z)^2\\
\Leftrightarrow & |x-y|+|y-z|+\sqrt{|x-y|\cdot |y-z|} \geq |x-z|
\end{aligned}
$$
This inequility holds since $|x-y|+|y-z| \geq |x-z|$ and $\sqrt{|x-y|\cdot |y-z|}\geq 0$.
#### 1.3 $d_3$ is not a metric
$d(1,-1)=0$ but $1\ne -1$.
#### 1.4 $d_4$ is not a metric
$d(0,1)=2 \ne 1 =d(1,0)$.
#### 1.5 $d_5$ is a metric 
(a)$d_5(x,y)= \dfrac{|x - y|}{1 + |x - y|} \geq 0, d_5(x,y)=0 \Leftrightarrow \dfrac{|x - y|}{1 + |x - y|}=0 \Leftrightarrow |x-y|=0 \Leftrightarrow x=y$,
(b)$d_5(x,y)= \dfrac{|x - y|}{1 + |x - y|}= \dfrac{|y-x|}{1 + |y - x|}=d_5(y,x)$,
(c)
$$
\begin{aligned}
d_5(x,y)+d_5(y,z)&= \dfrac{|x-y|+|y-z|+2|x-y|\cdot |y-z|}{1+|x-y|+|y-z|+|x-y|\cdot |y-z|}\\
&\geq \dfrac{|x-y|+|y-z|+|x-y|\cdot |y-z|}{1+|x-y|+|y-z|+|x-y|\cdot |y-z|}\\
&= 1-\dfrac{1}{1+|x-y|+|y-z|+|x-y|\cdot |y-z|}\\
&\geq1-\dfrac{1}{1+|x-y|+|y-z|}\\
&=\dfrac{|x-y|+|y-z|}{1+|x-y|+|y-z|}\\
&=\dfrac{1}{\frac{1}{|x-y|+|y-z|}+1}\\
&\geq \dfrac{1}{\frac{1}{|x-z|}+1}=\frac{|x-z|}{1+|x-z|}=d_5(x,z)\\
\end{aligned}
$$
### 2. Problem 2
>[!problem]
Let $(X, d)$ be a metric space. Suppose every bounded closed set is complete. Show that $(X, d)$ is complete.

Take an arbitrary Cauchy sequence $\{ x_n \}$ in $(X,d)$.
Take $\epsilon=1$, there exsists $N \in \mathbb{Z}^+$,s.t. for all $i,j > N$, we have $d(x_i,x_j)<1$.
Fix $i=N+1$, and let $r=max \{ d(x_i,x_1),d(x_i,x_2),\cdots d(x_i,x_N),1 \}$.
Then $d(x_i,x_n) \leq r, \forall n \in \mathbb{Z}^+$, i.e. $x_n \in \overline{B(x_i,r)},\forall n \in \mathbb{Z}^+$.
Since $\overline{B(x_i,r)}$ is a bounded closed set, $\{ x_n \}$ convergents.
Therefore, $(X,d)$ is complete.
### 3. Problem 3
>[!problem] 
>Prove that $E$ is bounded if and only if $\text{diam } E < +\infty$.

The proposition holds trivially for the empty set, so we assume that $E$ is non-empty. 
First prove necessity:
Take an arbitrary point $t\in E$, note $r=1+\text{diam }E$.
$\forall a \in E,d(t,a)\leq \text{sup}\{d(x,y):x,y \in E\}<r \Rightarrow E\subseteq B(t,r)$,
Thus $E$ is bounded.
Then prove sufficiency:
Suppose $E\subseteq B(t,r),t\in E,r \in \mathbb{R}^+$.
$\forall x,y\in E,x,y\in B(t,r)\Rightarrow d(x,t)<r,d(y,t)＜r\Rightarrow d(x,y)\leq d(x,t)+d(y,t)<2r$
$\Rightarrow \text{diam }E=\text{sup}\{d(x,y):x,y \in E\}\leq 2r<+\infty$.
Thus $\text{diam } E < +\infty$.
### 4. Problem 4
>[!problem]
Prove that $E'$ is closed. Do $E$ and $E'$ always have the same limit points.
#### 4.1 Proof
We use the equivalent definition that $A$ is closed if and if only $A' \subseteq A$. We will show that $(E')' \subseteq E'$. Suppose $x$ is a limit point of $E'$, we will show that $x\in E'$.
 $\forall \epsilon > 0$, since $x$ is a limit point of $E'$, we have$$(B(x,\frac{\epsilon}{2})\textbackslash \{x\})\cap E'\ne \emptyset,$$
i.e. there exists a point $x_1 \in E'$ s.t. $d(x,x_1)<\frac{\epsilon}{2},x\ne x_1$.
Since $x_1$ is a limit point of $E'$, we can similarly obtain that there exsits a point $x_2 \in E$ s.t.   $d(x_1,x_2)<\frac{\epsilon}{2},x_1 \ne x_2$ .
Further more, there exsits a point $x_3 \in E$ s.t. $d(x_1,x_3)<d(x_1,x_2)<\frac{\epsilon}{2},x_1 \ne x_3$.
$d(x_1,x_3)<d(x_1,x_2)$ promises that $x_2\ne x_3$, thus $x \ne x_2$ or $x\ne x_3$.
We may assume that $x \ne x_2$.
By triangle inequility, we have $d(x,x_2)<d(x,x_1)+d(x_1,x_2)<\epsilon$, i.e.
$$x_2 \in (B(x,\epsilon)\textbackslash \{x\})\cap E\ne \emptyset,$$
Thus $x$ is a limit point of $E$, i.e. $x \in E'$.
#### 4.2 The statement is false.
Let $E= \{ \dfrac{1}{n}:n\in \mathbb{Z}^+ \}$.
The limit point of $E$ is $\{0\}$,
i.e. $E'=\{0\}$.
Since $E'$ has no limit point, the statement is false.

### 5. Problem 5
>[!problem]
Let $X$ be a metric space, and $\{A_i\}_{i=1}^\infty$ be a countable family of subsets of $X$. Prove:
(a) $\bigcup_{i=1}^n \overline{A_i} =\overline{\bigcup_{i=1}^n A_i}$
(b) $\bigcup_{i=1}^\infty \overline{A_i} \subseteq \overline{\bigcup_{i=1}^\infty A_i}$
(c) Give an example where (b) is a proper subset.

#### 5.1（a）
We shall use a property: $A\subseteq B \Rightarrow \overline{A} \subseteq \overline{B}$.
This is because any sequence in $A$ is also in $B$, so a limit point of $A$ is also a limit point of $B$, i.e. $A' \subseteq B'$.
Using this property, we have $A_i \subseteq \bigcup_{i=1}^n A_i \Rightarrow \overline{A_i} \subseteq \overline{\bigcup_{i=1}^n A_i},i\in \mathbb{Z}^+$.
According to the property of unions, we have $\bigcup_{k=1}^n\overline{A_k} \subseteq \overline{\bigcup_{i=1}^n A_i}$.

On the other hand, we by definition have $A_i \subseteq \overline{A_i}$.
According to the property of unions, we have $\bigcup_{i=1}^n A_i \subseteq \bigcup_{i=1}^n \overline{A_i}$.
Since the finite union of closed sets is closed, $\bigcup_{i=1}^n \overline{A_i}$ is closed.
While $\overline{\bigcup_{i=1}^n A_i }$ is the smallest closed set that contains $\bigcup_{i=1}^n A_i$,  $\overline{\bigcup_{i=1}^n A_i} \subseteq \bigcup_{i=1}^n \overline{A_i}$

In conclusion, $\bigcup_{i=1}^n \overline{A_i} =\overline{\bigcup_{i=1}^n A_i}$.
#### 5.2(b)
We already have $\overline{A_i} \subseteq \overline{\bigcup_{i=1}^n A_i},i\in \mathbb{Z}^+$ from above.
According to the property of unions, we have $\bigcup_{i=1}^{\infty} \overline{A_i} =\overline{\bigcup_{i=1}^n A_i}$
#### 5.3 (c)
Let $A_i=(-\dfrac{n}{n+1},\dfrac{n}{n+1})$.
Then $\bigcup_{i=1}^\infty \overline{A_i} =(-1,1), \overline{\bigcup_{i=1}^\infty A_i}=[-1,1]$.
>[!tip] Strethen
>$\{A_\alpha\}$ could be uncountably infinite.

### 6. Problem 6
>[!problem]
Let $X$ be a infinite set with discrete metric. Describe all open sets, closed sets and compact sets in $(X, d)$.

#### 6.1 Open sets
First, empty set is open.
Take an arbitrary non-empty set $A\subseteq X$.
$\forall a \in A, B(a,0.9)\cap A=\{a\}\subseteq A$.
Therefore, any point of $A$ is an interior point, which means $A$ is an open set.
In conclusion, all sets in $X$ are open sets.
#### 6.2 Closed sets
Since all sets in $X$ are open sets, the completments of all sets are open.
In conclusion, all sets in $X$ are closed sets.
#### 6.3 Compact sets
First, empty set is compact.
Take an arbitrary non-empty finite set $A=\{x_k:1\leq k \leq n\}\subseteq X$, and $\cup_\alpha G_\alpha$ is an arbitratry open cover of $A$.
$\cup_\alpha G_\alpha \supseteq A \Rightarrow \forall k,1\leq k \leq n, \exists \alpha_k,s.t.x_k \in G_{{\alpha}_k}$.
Then $\cup_{1\leq k\leq n} G_{\alpha_k}$ is a finite subcover of $\cup_\alpha G_\alpha$.
Thus $A$ is compact.

Take an arbitrary infinite set $B=\{ x_{\alpha}:\alpha \in I \}\subseteq X$.
Then $\cup_\alpha \{ x_\alpha \}$ is an open cover of $B$ (we have showed that every set in $X$ is open). 
However, $\cup_\alpha \{ x_\alpha \}$ has no subcover except itself.
Thus $B$ is non-empty.

In conclusion, compact sets in $X$ are all the finite sets in $X$.
### 7. Problem 7
>[!problem]
Consider the following new metric $d$ on the set of rational numbers $\mathbb{Q}$.
(a) We first define a valuation function $v : \mathbb{Z}\backslash\{0\} \to \mathbb{N}$ by $$v(n) = k \text{ if } 2^k \mid n \text{ but } 2^{k+1} \nmid n.$$
Compute $v(3), v(16), v(-24), v(1000), v(1001)$.
(b) We extend the valuation function on $\mathbb{Q}\backslash\{0\}$ by
$$v\left(\frac{p}{q}\right) = v(p) - v(q), \text{ for } p, q \text{ non-zero integers}.$$
Compute $v(3/2), v(0.512), v(-0.03125)$.
(c) Given any pair of rational numbers $r, s \in \mathbb{Q}$, we define$$d(r, s) = 
\begin{cases} 
0 & r = s \\ 
\frac{1}{2^{v(r-s)}} & r \neq s 
\end{cases}$$
Compute $d(11, -53)$ and $d(9.99, 10.0525)$.
(d) Prove the sequence $\{1, 2, 2^2, ..., 2^n, ...\}$ is a Cauchy sequence.
(e) Prove $(\mathbb{Q}, d)$ is a metric space, and it is non-complete.
#### 7.1 (a)
By definition we have $v(3)=0, v(16)=4, v(-24)=3, v(1000)=3, v(1001)=0$.
#### 7.2 (b)
By definition we have $v(3/2)=-1, v(0.512)=6, v(-0.03125)=-5$.

Due to the existence and uniqueness of the prime factorization of an integer (Fundamental Theorem of Arithmetic), we have $v(p)=v(-p)$ and $v(pq) = v(p) + v(q)$ for $p,q\in \mathbb{Z}\textbackslash\{0\}.$
This ensures the well-definedness of $v\left(\frac{p}{q}\right)$.
### 7.3 (c)
By definition we have $d(11, -53)=1/64$ and $d(9.99, 10.0525)=16$.
#### 7.4 (d)
Note that $a_n=2^n,n\in \mathbb{Z}_{\geq 0}$.
$\forall \epsilon > 0$, let $N=max \{1,\lceil-\log_{2}\epsilon \rceil \}$, then $\forall i,j > N(i \ne j),d(a_i,a_j)=2^{-max \{i,j\}} < 2^{-N} \leq \epsilon$.
Thus $\{a_n\}_{n\in \mathbb{Z}_{\geq 0}}$ is a Cauchy sequence.
>[!tip] 
>It's also easy to show that $\{a_n\}$ converges to $0$.
#### 7.5 (e)
##### 7.5.1 Metric space
$\forall r,s,t \in \mathbb{Q}$
(1) By definition we have $d(r,s)\geq0, d(r,s)=0 \Leftrightarrow r=s$,
(2) We already have $v(r)=v(-r)$, so $d(r,s)=d(s,r)$,
(3) According to the Fundamental Theorem of Arithmetic we have $v(r-s)\geq min\{v(r),v(s)\}$ if $r \ne s$.
Therefore, we have $max\{ d(r,s) , d(s,t) \} \geq d(r,t)$.
Since $d(r,s) + d(s,t)\geq max\{ d(r,s) , d(s,t) \}$, we have $d(r,s) + d(s,t)\geq d(r,t)$.
In conclusion, $(\mathbb{Q}, d)$ is a metric space.
##### 7.5.2 Non-complete
Let $$a_1=1,a_{n+1}=\begin{cases} 
a_n & 2^{n+1} \mid a_{n}^2-17 \\ 
a_n+2^{n-1} &  2^{n+1} \nmid a_{n}^2-17\\ 
\end{cases}$$We wish to prove that $2^{n} \mid a_{n}^2-17,n \in \mathbb{Z}^+$ .
The statement is true when $n=1,2,3$.
Assume that the statement holds for $n=k,k\geq 3$, i.e. $2^{k} \mid a_{k}^2-17$.
If $2^{k+1} \mid a_{k}^2-17$, then $a_{k+1}=a_{k}$, so $2^{k+1} \mid a_{k+1}^2-17$.
If $2^{k+1} \nmid a_{k}^2-17$, then $a_{k+1}=a_k+2^{k-1}$, and $2^{k+1} \mid a_{k}^2-17-2^k$.
Next we obtain $2^{k+1} \mid {(a_{k+1}-2^{k-1})}^2-17-2^k=a_{k+1}^2-17+2^{2k-2}-(a_{k+1}+1)2^k$.
Since $2^{k+1} \mid 2^{2k-2}-(a_{k+1}+1)2^k$  (as $k+1 \leq 2k-2$ and $a_{k+1}$ is odd), $2^{k+1} \mid a_{k+1}^2-17$.
Therefore, by the principle of mathematical induction, $2^{n} \mid a_{n}^2-17,n \in \mathbb{Z}^+$.

Now we look at $\{a_n\}$, we shall show that ${a_n}$ is a non-convergent Cauchy sequence in $\mathbb{Q}$.

By definition we have $a_1=a_2=1$, and $a_n=\sum_{k=0}^{n-2}c_k2^{k},c_k\in\{0,1\},n\geq 3$.
$\forall \epsilon > 0$, let $N=2+max \{2,\lceil-\log_{2}\epsilon \rceil \}$, then $\forall i,j > N(i \ne j),d(a_i,a_j)<2^{-max \{i-2,j-2\}} < 2^{-(N-2)} \leq \epsilon$.
So $\{a_n\}$ is a Cauchy sequence.

Assume, for sake of contradiction, that $\{a_n\}$ converges to $q\in \mathbb{Q}$.
Then by the property of Cauchy sequence, $\{a_n^2\}$ converges to $q^2$.
We have already proven $2^{n} \mid a_{n}^2-17$ , which means $d(a_n^2,17)\leq 2^{-n}$.
That suggests $d(a_n^2,17)\rightarrow 0, n \rightarrow +\infty$, i.e. $\{a_n^2\}$ converges to $17$.
However, $17$ is not a square in $\mathbb{Q}$.
Hence, our assumption must be false, $\{a_n\}$ doesn't converge in $\mathbb{Q}$.

In conclusion, $(\mathbb{Q}, d)$ is non-complete.
>[!tip] Thinking
>In $\mathbb{R}$, we know three basic examples to prove irrationality:
>1. Non-periodic decimal,
>2. $\sqrt{2}$ ,
>3. $e=\sum_{k=0}^{\infty}\dfrac{1}{k!}$.
>
>My first thought is to show that a number in $\mathbb{Q}_p$ is in $\mathbb{Q}$ if and if only its $p$-adic expansion repeats, which is easy to prove but too complicated to be written here. Then I tried to prove that$\sum_{k=0}^{\infty}n!$ or $\sum_{k=0}^{\infty}2^{n!}$ is not rational (it's true), but also had some trouble making it short. I come up with the final construction according to the fact (related to Hensel's lemma) that in $\mathbb{Q}_2$, a nonzero element $x = 2^n u, u \in \mathbb{Z}_2^*$ is a square if and if only: $n$ is even, and $u \equiv 1 \pmod{8}$. So $17$ is a good example that is a square in $\mathbb{Q}_2$ but not square in $\mathbb{Q}$. Then we only have to find the $2$-adic expansion of $\sqrt{17}$ , which is written at the beginning. 

