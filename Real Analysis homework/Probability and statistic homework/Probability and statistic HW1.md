
>[!problem] Problem 1
>If $P(A)=0.6, P(B)=0.5$, and $P(A\cup B)=0.8$, are $A$ and $B$ independent events? Why or why not?

$P(A\cup B)=P(A)+P(B)-P(A\cap B)=0.6+0.5-0.8=0.3$.
Since we have $P(A\cup B)=P(A)\cdot P(B)$, $A$ and $B$ are independent.
___

>[!problem] Problem 2
>Toss a fair coin 3 times, and the occurrence of each outcome is equally likely.
a. What's sample space $\Omega$?  
b. Let A, B, C, D be the events given by  
$A=\{$ at least 2 heads $\}$,  
$B=\{$ at most 2 tails $\}$,  
$C=\{$ heads on the third toss $\}$, and  
$D=\{$ $2$ heads and 1 tail $\}$.  
Find the $P(A), P(B), P(C), P(D), P(A\cap B), P(A\cup C), P(A\cap C)$, and $P(B\cap D)$.
#### a.
We use $H$ for head and $T$ for tail.
$$
\Omega = \{ HHH, HHT, HTH, HTT, THH, THT, TTH, TTT \}
$$
#### b.
First, let's define the events explicitly:
$$A = \{HHH, HHT, HTH, THH\},$$
$$B=\{HHH, HHT, HTH, HTT, THH, THT, TTH\},$$
$$C=\{HHH, HTH, THH, TTH\},$$
$$D=\{HHT, HTH, THH\}.$$
Then we have:
$$A\cap B=A,$$
$$A\cap C=\{HHH, HTH, THH\},$$
$$A\cup C=\{HHH,HHT, HTH, THH,TTH\},$$
$$B\cap D=D$$
Thus, we can compute that
$P(A)=4/8=1/2,P(B)=7/8,P(C)=4/8=1/2,P(D)=3/8,$
$P(A\cap B)=P(A)=1/2, P(A\cup C)=5/8,P(A\cap C)=3/8,P(B\cap D)=P(D)=3/8$.
___
>[!problem] Problem 3
>Divide a line segment into two parts by selecting a point at random. What's the probability that the length of longer segment is at least three times the shorter segment?
>

Let the line segment be $[0,1]$, then the length of longer segment is at least three times the shorter segment if and only if the random point sits on $[0,0.25]\cup[0.75,1]$, so the probability is $0.5$.
___
>[!problem] Problem 4
> There are $n+1$ apples, $n$ is positive and even, and distribute them to Tom and Jerry. Assume each apple is equally likely being assigned to Tom or Jerry.
a. What's the probability that Tom gets less apples than Jerry?  
b. What's the probability that Tom receive at least one apple, and Jerry receive at least two apples?
#### a.
Since each apple is equally likely being assigned to Tom or Jerry, the probability that Tom gets less apples than Jerry equals to the probability that Jerry gets less apples than Tom.
Since $n$ is even, Tom and Jerry cannot get the same number of apples, so Jerry gets less apples than Tom means Tom gets more apples than Jerry, and Tom gets more apples than Jerry is the complement event of Tom gets less apples than Jerry.
Therefore, the probability that Tom gets less apples than Jerry is $1/2$.
#### b.
The complement event of that Tom receive at least one apple, and Jerry receive at least two apples is that Tom receive no apple, or Jerry receive at most one apple, and these two events are mutually exclusive. 
That Tom receive no apple and that Jerry receive at most one apple are mutually exclusive, and their probability is $1/2^{n+1}$ and $(n+2)/2^{n+1}$.
So the probability that Tom receive at least one apple, and Jerry receive at least two apples $1-1/2^{n+1}-(n+2)/2^{n+1}$, which is $(2^{n+1}-n-3)/2^{n+1}$.

___
>[!problem] Problem 5
> Let $A$ and $B$ be two events.
a. If the events $A$ and $B$ are mutually exclusive, are $A$ and $B$ always independent? If the answer is no, can they ever be independent? Explain.  
b. If $A\subset B$, can $A$ and $B$ ever be independent events? Explain.
#### a.
$A$ and $B$ are mutually exclusive means $A\cap B=\varnothing$, so $P(A\cap B)$ is always $0$. 
Therefore, $P(A\cap B)=P(A)\cdot P(B)$ ($A$ and $B$ are independent) if and only if $P(A)=0$ or $P(B)=0$.
#### b.
$A\subset B$ means $A\cap B=B$, so $P(A\cap B)=P(B)$.
Therefore, $P(A\cap B)=P(A)\cdot P(B)$ ($A$ and $B$ are independent) if and only if $P(A)=1$ or $P(B)=0$.
___

>[!problem] Problem 6
> A test indicates the presence of a particular disease $95\%$ of the time when the disease is present and the presence of the disease $3\%$ of the time when the disease is not present. If $0.4\%$ of the population has the disease, calculate the conditional probability that a person selected at random has the disease if the test indicates the presence of the disease.

First, compute the probability of testing positive:

$$
\begin{aligned}
P(\text{Test Positive}) &= P(\text{Test Positive} \mid \text{Disease}) \cdot P(\text{Disease}) \\
&+ P(\text{Test Positive} \mid \text{No Disease}) \cdot P(\text{No Disease}) \\
&= (0.95)(0.004) + (0.03)(1 - 0.004) \\
&= 0.0038 + 0.02988 \\
&= 0.03368
\end{aligned}
$$

Then we have:

$$
\begin{aligned}
P(\text{Disease} \mid \text{Test Positive}) &= \frac{(0.95)(0.004)}{0.03368} \\
&= \frac{0.0038}{0.03368} \\
&\approx 0.1128
\end{aligned}
$$
Therefore, the conditional probability that a person selected at random has the disease if the test indicates the presence of the disease is about 0.1128.
___
>[!problem] Problem 7
> A common test for AIDS is called the ELISA (enzyme-linked immunosorbent assay) test. Among 1 million people who are given the ELISA test, we can expect results similar to those given in the following table:
> 
|       | Has AIDS (B1) | Does Not Have AIDS (B2) | **Totals** |
| :---------------------: | :-----------: | :---------------------: | :--------: |
| **Test Positive (A1)** |     4,885     |         73,630          |   78,515   |
| **Test Negative (A2)** |      115      |         921,370         |  921,485   |
| **Totals**             |     5,000     |         995,000         | 1,000,000  |
If one of these 1 million people is selected randomly, find the following probabilities:
a. $P(B1)$.  
b. $P(A1)$.  
c. $P(A1|B2)$.  
d. $P(B1| A1)$.  
e. In words, what do parts (c) and (d) say?
#### a.
$P(B1)=5,000/1,000,000=0.005$.
#### b.
$P(A1)=78,515/1,000,000=0.078515$.
#### c.
$P(A1|B2)=73,630/995,000=0.074$.
#### d.
$P(B1| A1)=4,885/78,515\approx 0.0622$.
#### e.
(c) represents the false positive rate, which means the probability that a person tests positive ​given that they do not actually have the disease.
(d) represents the positive predictive value, which means the probability that a person ​actually has the disease given that their test result is positive.
