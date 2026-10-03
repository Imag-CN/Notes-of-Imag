___

> [!problem] Problem 1 ([SER] II.2.1)
> (Krasner's lemma) Let $E/K$ be a finite Galois extension of a complete field $K$. Prolong the valuation of $K$ to $E$. Let $x \in E$ and let $\{x_1, \dots, x_n\}$ be the set of conjugates of $x$ over $K$, with $x = x_1$. Let $y \in E$ be such that $\|y - x\| < \|y - x_i\|$ for $i \ge 2$. Show that $x$ belongs to the field $K(y)$.

**Proof:**
Since $E/K$ is Galois, for any $K$-automorphism $\sigma:E\to E$, we have $\sigma(x)=x_i$ for some $i$; and $E/K(y)$ is Galois. Suppose that $x\notin K(y)$. Then there is a $K(y)$-automorphism $\sigma$ $E$ such that $\sigma(x)\ne x$. In particular, $\sigma(x)=x_i$ for some $i\ge2$.

Because there is a unique way to prolong the valuation of $K$ to $E$, we have$\|y-x\|=\|\sigma(y-x)\|$. And because $\sigma$ fixes $y$, we have $\|\sigma(y-x)\|=\|y-\sigma(x)\|=\|y-x_i\|$, contradicting the assumption $\|y-x\|<\|y-x_i\| \quad (i\ge2)$.

Therefore $x$ has no conjugate over $K(y)$ other than itself, so $x\in K(y)$.
___

