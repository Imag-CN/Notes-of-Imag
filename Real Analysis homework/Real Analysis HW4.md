___

> [!problem] [SHE] 5A.3
> Let $\mathcal{B}$ denote the $\sigma$-algebra of Borel subsets of $\mathbb{R}$. Show that there exists a set $E \subset \mathbb{R} \times \mathbb{R}$ such that $[E]_a \in \mathcal{B}$ and $[E]^a \in \mathcal{B}$ for every $a \in \mathbb{R}$, but $E \notin \mathcal{B} \otimes \mathcal{B}$.

**Proof:**
Let $E$ be the graph of a bijection $\phi: \mathbb{R} \to \mathbb{R}$ that is not Borel measurable (such $\phi$ exists: there are $2^\mathfrak{c}$ bijections but only $\mathfrak{c}$ Borel sets in $\mathbb{R}^2$, so some graph is not in $\mathcal{B} \otimes \mathcal{B}$).

For any $a \in \mathbb{R}$:
- $[E]_a = \{y : (a,y) \in E\} = \{\phi(a)\}$ (singleton, Borel)
- $[E]^a = \{x : (x,a) \in E\} = \{\phi^{-1}(a)\}$ (singleton, Borel)

Thus all sections are Borel, but $E \notin \mathcal{B} \otimes \mathcal{B}$.
___

> [!problem] [SHE] 2D.2
>Prove that there exists a bounded set $A \subset \mathbf{R}$ such that $|F| \leq |A| - 1$ for every closed set $F \subset A$.

