___

>[!problem] Problem 1
>Prove that an integral domain $R$ is a UFD if and only if the following two conditions hold:
>(i) every nonzero nonunit element of $R$ can be written as a product of irreducible elements of $R$.
>(ii) every irreducible element of $R$ is prime.

**Proof:**
$(\Rightarrow)$ If $R$ is a UFD, then (i) holds by definition. In a UFD, every irreducible is prime, so (ii) also holds.

$(\Rightarrow)$ Assume (i) and (ii) hold. We need to show uniqueness of factorization. Let $a \in R$ be nonzero and nonunit, with two factorizations into irreducibles:
$$a = p_1 \cdots p_m = q_1 \cdots q_n.$$
By (ii), each $p_i$ is prime. Since $p_1$ is prime and $p_1 \mid q_1 \cdots q_n$, we have $p_1 \mid q_j$ for some $j$. As $q_j$ is irreducible, $p_1$ and $q_j$ are associates: $q_j = u p_1$ for some unit $u$. Cancel $p_1$ to get
$$p_2 \cdots p_m = u q_1 \cdots q_{j-1} q_{j+1} \cdots q_n.$$
By induction on the number of factors, $m=n$ and after reordering, $p_i$ is associate to $q_i$ for all $i$. Hence $R$ is a UFD.
___

>[!problem] Problem 2
>Let $R$ be an integral domain and let $a \in R$. Determine which is stronger or neither is stronger than the other.
>(i) $a$ is irreducible.
>(ii) $a$ is prime.

**Proof:**
$(\text{ii})\Rightarrow(\text{i})$:
If $a$ is prime and $a=bc$, then $a \mid bc$. By the definition of prime, $a \mid b$ or $a \mid c$.  
Assume $a \mid b$, so $b=ad$. Substituting gives $a=adc$, hence $a(1-dc)=0$. Since $R$ is a domain and $a \neq 0$, we have $1-dc=0$, so $c$ is a unit. Therefore $a$ is irreducible.

$(\text{i})\not\Rightarrow(\text{ii})$  
In $\mathbb{Z}[\sqrt{-5}]$, the element $2$ is irreducible but not prime.  
Indeed, $2 \mid 6 = (1+\sqrt{-5})(1-\sqrt{-5})$ but $2$ divides neither factor. 
___

>[!problem] Problem 3
>Let $D$ be an integer such that $D \equiv 1 \pmod{4}$ and $D 
eq m^2$ for any $m \in \mathbb{Z}$.
>(i) Prove that $\mathbb{Z}[\sqrt{D}]$ is not a UFD.
>(ii) Find all elements of $\mathbb{Z}\left[\frac{1+\sqrt{D}}{2}\right]$.
>(iii) Prove that no prime number is a unit in $\mathbb{Z}\left[\frac{1+\sqrt{D}}{2}\right]$.

**Proof:**
**(i)** Let $D=4k+1$. Consider
$$
4(x^{2}-x-k)=(2x-1+\sqrt{ D })(2x-1-\sqrt{ D }),
$$
where LHS is not primitive but RHS is the product of two primitive polynomial. This contradicts to Gauss's Lemma.
**(ii)** All elements are of the form  
$$
a + b\cdot\frac{1+\sqrt{D}}{2}, \quad a,b\in\mathbb{Z}.
$$
**(iii)** This ring can be embedded in $\mathbb{C}$ , and the inverse of any prime in $\mathbb{C}$ is not in this ring, thus prime numbers are not unit.
___

>[!problem] Problem 4
>For $D=4n+3$ where $n=-2,-1,0,1,2$, determine whether $\mathbb{Z}[\sqrt{D}]$ is a UFD.

**Proof:**
1. $D=-5$: $\mathbb{Z}[\sqrt{-5}]$ is not a UFD, since we have factorization:
$$
6=2\cdot3=(1+\sqrt{-5})(1-\sqrt{-5}).
$$
2. $D=-1$: $\mathbb{Z}[i]$ is a Euclidean domain, hence a UFD.

3. $D=3$: $\mathbb{Z}[\sqrt{3}]$ is a UFD because $\mathbb{Q}(\sqrt{3})$ has class number $1$.

4. $D=7$: $\mathbb{Z}[\sqrt{7}]$ is a UFD because $\mathbb{Q}(\sqrt{7})$ has class number $1$.

5. $D=11$: $\mathbb{Z}[\sqrt{11}]$ is a UFD because $\mathbb{Q}(\sqrt{11})$ has class number $1$.
___

>[!problem] Problem 5
>Compute the number
>
>$$e^{\pi \sqrt{163}}$$
>
>to $14$ digits after the decimal point. Explain why it is so close to an integer.

**Proof:**
The number is:
$$
e^{\pi\sqrt{163}} \approx 262537412640768743.\underbrace{99999999999925}_{14\ \text{digits}}\dots
$$

Let $q = e^{\pi i\tau}$ and $\tau = \frac{-1+\sqrt{-163}}{2}$.  
The **j‑invariant** $j(\tau)$ is an integer when $\mathbb{Q}(\sqrt{-163})$ has class number $1$ (which it does).  

In fact,
$$j\!\left(\frac{-1+\sqrt{-163}}{2}\right) = -640320^3.$$

A standard formula gives
$$e^{\pi\sqrt{163}} = 640320^3 + 743.999999999999250\ldots$$

More precisely,
$$e^{\pi\sqrt{163}} = 640320^3 + 744 - \varepsilon,$$
where $\varepsilon \approx 0.000000000000749\ldots$ is extremely small.