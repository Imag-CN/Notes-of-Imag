___

>[!problem] [SHE] 2C.4
>Give an example of a measure space $(X, \mathcal{S}, \mu)$ such that  
>$$
>\{\mu(E) : E \in \mathcal{S}\} = \{\infty\} \cup \bigcup_{k=0}^{\infty} [3k, 3k + 1].
>$$

**Proof:**
Let $X = [0,1] \cup \{2,3,\dots\}$. Define $\mathcal{S}$:
$$
\mathcal{S} = \{ E \subset X : E \cap [0,1] \text{ is a Borel set in }\mathbb{R} \}.
$$
Define $\mu: \mathcal{S} \to [0,\infty]$ by
$$
\mu(E) =\lambda([0,1] \cap E)+3\cdot\#(E\setminus [0,1])
$$
where $\lambda$ is Lebesgue measure on $[0,1]$.
___

>[!problem] [SHE] 2C.5
>Suppose $(X, \mathcal{S}, \mu)$ is a measure space such that $\mu(X) < \infty$. Prove that if $\mathcal{A}$ is a set of disjoint sets in $\mathcal{S}$ such that $\mu(A) > 0$ for every $A \in \mathcal{A}$, then $\mathcal{A}$ is a countable set.

**Proof.**
Let $\mathcal{A} = \{A_i\}_{i \in I}$ be an uncountable family of disjoint measurable sets with $\mu(A_i) > 0$ for all $i$.

For each $n \in \mathbb{N}^*$, define
$$
I_n = \left\{ i \in I : \mu(A_i) \geq \frac{1}{n} \right\}.
$$
Then $I = \bigcup_{n=1}^{\infty} I_n$.

If $I$ is uncountable, then at least one $I_n$ is infinite, take such an $n$, and let $J \subset I_n$ be a countable subset. Then
$$
\mu\left(\bigcup_{j \in J} A_j\right) = \sum_{j \in J} \mu(A_j) \geq \sum_{j \in J} \frac{1}{n} = \infty,
$$
but the union $\bigcup_{j \in J} A_j$ is a subset of $X$, so $\mu\left(\bigcup_{j \in J} A_j\right) \le \mu(X) < \infty$, a contradiction.

Hence $I$ must be countable.
___


>[!problem] [SHE] 2C.6
>Find all $c \in [3,\infty)$ such that there exists a measure space $(X,\mathcal{S},\mu)$ with
>$$
>\{\mu(E) : E \in \mathcal{S}\} = [0,1] \cup [3,c].
>$$

**Proof:**
If $c>4$, then take $E\in \mathcal{S}$ such that $\mu(E)\in(c-3,c-1)$. Then $\mu(X-E)\in(1,3)$, contradiction.

If $c<4$, then take $E\in \mathcal{S}$ such that $\mu(E)=1$. Then $\mu(X-E)=c-1\in(1,3)$, contradiction.

So $c=4$ is the only possible answer. We see a construction for $c=4$:
Let $X = [0,1] \cup \{2\}$. Define $\mathcal{S}$:
$$
\mathcal{S} = \{ E \subset X : E \cap [0,1] \text{ is a Borel set in }\mathbb{R} \}.
$$
Define $\mu: \mathcal{S} \to [0,\infty]$ by
$$
\mu(E) =\lambda([0,1] \cap E)+3\cdot\#(E\setminus [0,1])
$$
where $\lambda$ is Lebesgue measure on $[0,1]$.
___

>[!problem] [SHE] 2C.8
>Give an example of a set $X$, a $\sigma$-algebra $\mathcal{S}$ of subsets of $X$, a set $\mathcal{A}$ of subsets of $X$ such that the smallest $\sigma$-algebra on $X$ containing $\mathcal{A}$ is $\mathcal{S}$, and two measures $\mu$ and $\nu$ on $(X, \mathcal{S})$ such that
>$$
>\mu(A) = \nu(A)\text{ for all }A \in \mathcal{A}\text{ and }\mu(X) = \nu(X) < \infty,
>$$
>but $\mu \neq \nu$.

**Example.**
Let $X = \{1,2,3,4\}$, $\mathcal{S} = 2^X$. Let $\mathcal{A} = \{ \{1,2\}, \{2,3\}, \{3,4\} \}$. Then $\mathcal{S}$ is the smallest $\sigma$-algebra containing $\mathcal{A}$.

Define two probability measures $\mu$ and $\nu$ by:

$\mu(i) = \frac14$ for $i=1,2,3,4$.

$\nu(1)=\frac18,\; \nu(2)=\frac38,\; \nu(3)=\frac18,\; \nu(4)=\frac38$.

Then $\mu(X)=1=\nu(X)$, and
- $\mu(\{1,2\}) = \frac12 = \nu(\{1,2\})$
- $\mu(\{2,3\}) = \frac12 = \nu(\{2,3\})$
- $\mu(\{3,4\}) = \frac12 = \nu(\{3,4\})$

Thus $\mu(A)=\nu(A)$ for all $A \in \mathcal{A}$, but $\mu \ne \nu$.
___

>[!problem] [SHE] 2C.12
>Suppose $X$ is a set and $\mathcal{S}$ is the $\sigma$-algebra of all subsets $E$ of $X$ such that $E$ is countable or $X \setminus E$ is countable. Give a complete description of the set of all measures on $(X, \mathcal{S})$.

**Solution:**
Let $\mu$ be a measure on $(X,\mathcal{S})$. Let $X_0 = \{x \in X : \mu(\{x\}) > 0\}$, this set is countable. Define $a_x = \mu(\{x\})$ for $x \in X_0$, and let $\beta = \mu(X \setminus X_0)$.

Then for any $E \in \mathcal{S}$:
1. If $E$ is countable, $\mu(E) = \sum_{x \in E \cap X_0} a_x$.
2. If $E$ is co-countable, $\mu(E) = \beta + \sum_{x \in E \cap X_0} a_x$.
3. 
Equivalently, for all $E \in \mathcal{S}$,
$$
\mu(E) = \sum_{x \in E \cap X_0} a_x + \beta \cdot 1_{E \text{ is co-countable}}.
$$
Here $\beta \in [0,\infty]$, $a_x \in [0,\infty]$, and $\sum_{x \in X_0} a_x$ can be finite or infinite independently of $\beta$.

Thus, every measure on $(X,\mathcal{S})$ is of this form.
___

>[!problem] [SHE] 5A.2
>Suppose $(X, \mathcal{S})$ is a measurable space. Prove that if $E \in \mathcal{S} \otimes \mathcal{S}$, then
>$$
>\{x \in X : (x, x) \in E\} \in \mathcal{S}.
>$$

**Proof:**
Let $\mathcal{E} = \{ F \subset X \times X : \{x : (x,x) \in F\} \in \mathcal{S} \}$.  

Check $\mathcal{E}$ is a $\sigma$-algebra:  
- $X \times X \in \mathcal{E}$ since $\{x : (x,x) \in X\times X\} = X \in \mathcal{S}$.  
- If $F \in \mathcal{E}$, its complement is in $\mathcal{E}$ because $\{x : (x,x) \in F^c\} = X \setminus \{x : (x,x) \in F\} \in \mathcal{S}$.  
- Countable unions: $\{x : (x,x) \in \bigcup_n F_n\} = \bigcup_n \{x : (x,x) \in F_n\} \in \mathcal{S}$.

If $F = A \times B$ with $A,B \in \mathcal{S}$, then $\{x : (x,x) \in A \times B\} = A \cap B \in \mathcal{S}$, so $F \in \mathcal{E}$.  

Thus $\mathcal{E}$ is a $\sigma$-algebra containing all measurable rectangles, hence $\mathcal{S} \otimes \mathcal{S} \subset \mathcal{E}$.  

Therefore for any $E \in \mathcal{S} \otimes \mathcal{S}$, we have $E \in \mathcal{E}$, i.e. $D := \{x : (x,x) \in E\} \in \mathcal{S}$.
___

>[!problem] [SHE] 5A.8
>Suppose $\mu$ is a measure on a measurable space $(X,\mathcal{S})$. Prove that the following are equivalent:
>
>(a) The measure $\mu$ is $\sigma$-finite.
>
>(b) There exists an increasing sequence $X_{1} \subset X_{2} \subset \cdots$ of sets in $\mathcal{S}$ such that
>$X = \bigcup_{k=1}^{\infty} X_{k}$ and $\mu(X_{k}) < \infty$ for every $k \in \mathbf{Z}^{+}$.
>
>(c) There exists a disjoint sequence $X_{1}, X_{2}, X_{3}, \ldots$ of sets in $\mathcal{S}$ such that
>$X = \bigcup_{k=1}^{\infty} X_{k}$ and $\mu(X_{k}) < \infty$ for every $k \in \mathbf{Z}^{+}$.

**Proof:**
**$(a)\Rightarrow(b)$** Since $\mu$ is $\sigma$-finite, there exist $A_1, A_2, \dots \in \mathcal{S}$ with $X = \bigcup_{n=1}^{\infty} A_n$ and $\mu(A_n) < \infty$ for all $n$. Define $X_k = \bigcup_{n=1}^k A_n$. Then $X_1 \subset X_2 \subset \cdots$, $X = \bigcup_{k=1}^{\infty} X_k$, and by subadditivity,
$$
\mu(X_k) \le \sum_{n=1}^k \mu(A_n) < \infty.
$$
**$(b)\Rightarrow(c)$** Given $X_1 \subset X_2 \subset \cdots$ as in (b), define
$$
Y_1 = X_1, \quad Y_k = X_k \setminus X_{k-1} \ (k \ge 2).
$$
Then $\{Y_k\}$ is disjoint, $X = \bigcup_{k=1}^{\infty} Y_k$, and
$$
\mu(Y_k) \le \mu(X_k) < \infty.
$$

**$(b)\Rightarrow(a)$** Immediate from the definition of $\sigma$-finiteness.
___

>[!problem] [SHE] 5A.5
>Verify the assertion in Example 5.11 that the collection of finite unions of intervals of $\mathbb{R}$ is closed under complementation.

**Proof:**
Let $A = I_1 \cup \dots \cup I_n \in \mathcal{A}$, where each $I_j$ is an interval. Then
$$
A^c = \bigcap_{j=1}^n I_j^c.
$$
For any interval $I$, its complement $I^c$ is a finite union of at most two intervals (check cases: e.g., $[a,b)^c = (-\infty,a) \cup [b,\infty)$, etc.).

Thus each $I_j^c$ is in $\mathcal{A}$. Since $\mathcal{A}$ is closed under finite unions and intersections of intervals are intervals, $A^c$ is a finite union of intervals, so $A^c \in \mathcal{A}$.
___

>[!problem] [SHE] 5A.6
>Verify the assertion in Example 5.12 that the collection of countable unions of intervals of $\mathbb{R}$ is not closed under complementation.

**Proof:**
Let $\mathcal{A}$ be the collection of all countable unions of intervals in $\mathbb{R}$.  
Consider the set $\mathbb{Q}$, which is a countable union of singletons $\{q\}$ (each singleton is a closed interval). Thus $\mathbb{Q} \in \mathcal{A}$.

Its complement $\mathbb{Q}^c = \mathbb{R} \setminus \mathbb{Q}$ is the set of irrational numbers.  
We claim $\mathbb{Q}^c \notin \mathcal{A}$.

Indeed, suppose $\mathbb{Q}^c = \bigcup_{n=1}^{\infty} I_n$ where each $I_n$ is an interval. Since each $I_n$ contains uncountably many points, and intervals are connected, the only way to cover all irrationals by countably many intervals is if one of the intervals, say $I_k$, contains two rational numbers $r_1 < r_2$. But then $I_k$ contains the entire interval $[r_1, r_2]$, which includes infinitely many rationals, contradicting that $I_k \subset \mathbb{Q}^c$.  

Thus $\mathbb{Q}^c$ cannot be written as a countable union of intervals. Hence $\mathcal{A}$ is not closed under complementation.
___

>[!problem]
>Let $(X, \mathcal{S}, \mu)$ be a measure space with $\mu(X) = 1$. Let $\mathcal{A}$ and $\mathcal{A}'$ be two algebras on $X$ that both generate $\mathcal{S}$. Suppose that
>$$
>\mu(E \cap E') = \mu(E)\mu(E') \quad \text{for all } E \in \mathcal{A},\, E' \in \mathcal{A}'.
>$$
>Prove that
>$$
>\mu(E \cap E') = \mu(E)\mu(E') \quad \text{for all } E, E' \in \mathcal{S}.
>$$

**Proof:**
Fix $E' \in \mathcal{A}'$, and define
$$
\mathcal{L}_{E'} = \{ E \in \mathcal{S} : \mu(E \cap E') = \mu(E)\mu(E') \}.
$$
- By hypothesis, $\mathcal{A} \subset \mathcal{L}_{E'}$.
- $\mathcal{L}_{E'}$ is a $\lambda$-system: $X \in \mathcal{L}_{E'}$, closed under proper differences, and closed under increasing unions (by continuity of measure).
- Since $\mathcal{A}$ is a $\pi$-system (algebra) and $\sigma(\mathcal{A}) = \mathcal{S}$, Dynkin’s $\pi$-$\lambda$ theorem yields $\mathcal{L}_{E'} = \mathcal{S}$.

Thus, for all $E' \in \mathcal{A}'$ and all $E \in \mathcal{S}$, the identity holds.

Now fix $E \in \mathcal{S}$ and define
$$
\mathcal{L}_E = \{ E' \in \mathcal{S} : \mu(E \cap E') = \mu(E)\mu(E') \}.
$$
- From the previous step, $\mathcal{A}' \subset \mathcal{L}_E$.
- $\mathcal{L}_E$ is a $\lambda$-system similarly.
- $\mathcal{A}'$ is a $\pi$-system generating $\mathcal{S}$, so $\mathcal{L}_E = \mathcal{S}$.

Hence $\mu(E \cap E') = \mu(E)\mu(E')$ for all $E, E' \in \mathcal{S}$.