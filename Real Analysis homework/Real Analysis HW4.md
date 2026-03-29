___

> [!problem] [SHE] 5A.3
> Let $\mathcal{B}$ denote the $\sigma$-algebra of Borel subsets of $\mathbb{R}$. Show that there exists a set $E \subset \mathbb{R} \times \mathbb{R}$ such that $[E]_a \in \mathcal{B}$ and $[E]^a \in \mathcal{B}$ for every $a \in \mathbb{R}$, but $E \notin \mathcal{B} \otimes \mathcal{B}$.

Let $\mathcal{L}$ be the $\sigma$-algebra of Lebesgue measurable subsets of $\mathbb{R}$ and $\mathcal{B}$ the Borel $\sigma$-algebra. There exists a set $A \subset \mathbb{R}$ with $A \in \mathcal{L} \setminus \mathcal{B}$ (e.g., a Lebesgue non-Borel set). Also, there exists a set $C \subset \mathbb{R}$ with $C \notin \mathcal{L}$ (e.g., a Vitali set). Define
$$E = (A \times \mathbb{R}) \cup (\mathbb{R} \times C).$$
Then for any $a \in \mathbb{R}$,
$$[E]_a = \{y : (a,y) \in E\} = \{y : a \in A \text{ or } y \in C\} = 
\begin{cases}
\mathbb{R} & \text{if } a \in A,\\
C & \text{if } a \notin A.
\end{cases}$$
Similarly,
$$[E]^a = \{x : (x,a) \in E\} = \{x : x \in A \text{ or } a \in C\} = 
\begin{cases}
\mathbb{R} & \text{if } a \in C,\\
A & \text{if } a \notin C.
\end{cases}$$
Thus for each $a$, $[E]_a$ is either $\mathbb{R}$ (Borel) or $C$ (not Lebesgue measurable, but that's allowed; we need to ensure it's Borel? This construction needs adjustment because $C$ is not Borel if we want $E \notin \mathcal{B} \otimes \mathcal{B}$.)

Better construction (classical): Take a bijection $\phi: \mathbb{R} \to \mathbb{R}$ whose graph $G = \{(x,\phi(x)) : x \in \mathbb{R}\}$ is not in $\mathcal{B} \otimes \mathcal{B}$ (exists by a cardinality argument: there are $\mathfrak{c}$ Borel sets in $\mathbb{R}^2$ but $2^{\mathfrak{c}}$ graphs of bijections). Let $E = G$. Then for any $a$, $[E]_a = \{\phi(a)\}$ (singleton, Borel) and $[E]^a = \{x : \phi(x) = a\} = \{\phi^{-1}(a)\}$ (singleton, Borel). But $E$ is the graph of a bijection not in $\mathcal{B} \otimes \mathcal{B}$.

Thus $E$ satisfies: all sections are Borel (singletons), but $E \notin \mathcal{B} \otimes \mathcal{B}$.