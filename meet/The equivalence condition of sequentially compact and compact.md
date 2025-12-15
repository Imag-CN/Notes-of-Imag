>[!note] Theorem
>If $X$ is a first-countable topological space, then $X$ is compact gives that $X$ is sequentially compact. If $X$ is a second countable topological space, then $X$ is compact gives that $X$ is compact.

We clarify some concepts for the beginning:
>[!note] Definition
>(1) **Compact (Heine-Borel compact)**: Any open cover has finite subcover.
>(2) **Sequentially compact**: Any sequence has a convergent subsequence.
>(3) **Countably compact (limit compact)**: Any countable open cover has finite subcover, or equivalently, any infinite subset has limit point.
>(4) **Lindelöf**: Any infinite open cover has countable (or finite) subcover.

We trivially have (3)(4) $\Leftrightarrow$ (1) in general topological space, and we aim to prove (1) $\Leftrightarrow$ (2) in a second-countable space.
___
### (1) $\Rightarrow$ (2) in a first-countable space
We prove a lemma first:
>[!problem] Lemma
In a first-countable space $X$, if $p$ is a limit point of $A = \{x:x\in\{x_n\}\}$, then $p$ is a limit point of the sequence $\{x_n\}$.

Let $\{U_m\}$ be a nested countable neighborhood base at $p$.
Since $p$ is a limit point of $A$, each $U_m$ contains infinitely many points of $A \setminus \{p\}$.
Select $n_k$ recursively:
- $n_1$ = minimal index with $x_{n_1} \in U_1$,
- $n_k$ = smallest index > $n_{k-1}$ with $x_{n_k} \in U_k$.

For any neighborhood $V$ of $p$, there exists $m$ s.t. $U_m \subset V$.  
Then for all $k ≥ m,x_{n_k} \in U_k \subset V$, thus $x_{n_k} \to p$.
>[!tip] Remark
The inverse doesn't holds. Consider $\{x_n\}=x$ where $x$ is open.
>The lemma also doesn't holds without first-countable condition. Consider $[0,1]^{[0,1]}$ equipped with product topology. This is also a counterexample illustrating that (1) $\nRightarrow$ (2) and (3) $\nRightarrow$ (2) without first-countable condition.

___
Assume for contradiction that $\{x_n\}$ has no limit points, where $\{x_n\}$ is a sequence in $X$.
Let $A=\{x:x\in\{x_n\}\}$, by lemma $A$ has no limit points.
Then for every $y \in X$, there exists an open neighborhood $U_y$ such that:
$$U_y \cap A \subseteq \{y\}$$
(if $y \in A$, $U_y \cap A = \{y\}$; if $y \notin A$, then $U_y \cap A = \varnothing$).

The collection $\{U_y : y \in X\}$ is an open cover of $X$.  
By compactness, there is a finite subcover $\{U_{y_1}, \dots, U_{y_k}\}$.
Then
$$A \subseteq \bigcup_{i=1}^k U_{y_i} \cap A \subseteq \{y_1, \dots, y_k\},$$
so $A$ is finite.
However, by the principle of pigeon hole, $\{x_n\}$ would have a constant subsequence, which comes to a contradiction.
___
### (3) $\Rightarrow$ (2) in a first-countable space
Let $\{x_n\}$ be any sequence in $X$, and let $A=\{x:x\in\{x_n\}\}$.
Since $X$ is countably compact, $A$ has a limit point $p$.  
By lemma, $p$ is a limit point of $\{x_n\}$.
___
### (2) $\Rightarrow$ (3) in a general topology space
Assume for contradiction, that $X$ is not countably compact, then there exists an infinite set $A$ with no limit point.
Let $\{a_n\}$ be a sequence in $A$ and $a_i\neq a_j$ if $i\neq j$.
$X$ is sequentially compact, thus $\{a_n\}$ have a limit point $a$.
Then $a$ is a limit point of $A$, contradiction.
___
>[!tip] Remark
>In a first-countable space, (1) $\Rightarrow$ (3) $\Rightarrow$ (2) gives (1) $\Rightarrow$ (2).

___
### Second-countable $\Rightarrow$ (4)
Let $\mathcal{B}=\{B_n\}_{n\in\mathbb{Z}^+}$ be a countable basis of $X$.
Let $\mathcal{U}=\{U_{\alpha}\}_{\alpha\in I}$ be an open cover of $X$.
For any $x\in X$, there exists a $U_{\alpha_x}\ni x$, and a $B_{n_x}\subseteq U_{\alpha_x}$.  
Let $J=\{n_x:x\in X\}$, then $J$ is at most countable.
For all $k\in J$, choose an $x_k\in X,s.t.n_{x_k}=k$.
Then $\mathcal{U'}=\{U_{\alpha_{x_k}}\}_{k\in J}$ is a countable (or finite) subcover of $\mathcal{U}$.
Therefore, $X$ is Lindelöf.
>[!tip] Remark
>With only first-countable, (2) $\nRightarrow$ (1). According to the proof, we need to add Lindelöf, and second-countable is not necessary. In fact, first-countable Lindelöf space is not necessarily second-countable (see [Lower limit topology - Wikipedia](https://en.wikipedia.org/wiki/Lower_limit_topology)).
>
>The space $[0,\omega_1​)$ (the set of countable ordinals with the order topology) is:
>**First-countable**: At each point α, a local basis is $\{(\beta,\alpha+1):\beta<\alpha\}$, which is countable.
>​**Sequentially compact**: Any sequence in $[0,\omega_1​)$ is contained in some compact segment $[0,\gamma]$ with $\gamma<ω_1$​, hence has a convergent subsequence.
>**Non-compact and non-Lindelöf**: The open cover $\bigcup_{\alpha<\omega_1}[0,\alpha)$ has no countable or finite subcover.
