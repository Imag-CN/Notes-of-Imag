___

> [!problem] Problem 1 ([SER] II.2.1)
> (Krasner's lemma) Let $E/K$ be a finite Galois extension of a non-Archimedean complete field $K$. Prolong the valuation of $K$ to $E$. Let $x \in E$ and let $\{x_1, \dots, x_n\}$ be the set of conjugates of $x$ over $K$, with $x = x_1$. Let $y \in E$ be such that $\|y - x\| < \|y - x_i\|$ for $i \ge 2$. Show that $x$ belongs to the field $K(y)$.

**Proof:**
Since $E/K$ is Galois, for any $K$-automorphism $\sigma:E\to E$, we have $\sigma(x)=x_i$ for some $i$; and $E/K(y)$ is Galois. Suppose that $x\notin K(y)$. Then there is a $K(y)$-automorphism $\sigma$ $E$ such that $\sigma(x)\ne x$. In particular, $\sigma(x)=x_i$ for some $i\ge2$.

By the uniqueness of extension of valuations, we have$\|y-x\|=\|\sigma(y-x)\|$. Because $\sigma$ fixes $y$, we have $\|\sigma(y-x)\|=\|y-\sigma(x)\|=\|y-x_i\|$, contradicting the assumption $\|y-x\|<\|y-x_i\| \quad (i\ge2)$.

Therefore $x$ has no conjugate over $K(y)$ other than itself, so $x\in K(y)$.
___

> [!problem] Problem 2
> (i) ([SER II.2.1]) Let $K$ be a non-Archimedean complete field, and let $f(\mathrm{X}) \in \mathrm{K}[\mathrm{X}]$ be a separable irreducible polynomial of degree $n$. Let $\mathrm{L}/\mathrm{K}$ be the extension of degree $n$ defined by $f$. Show that for every polynomial $h(\mathrm{X})$ of degree $n$ that is close enough to $f$, $h(\mathrm{X})$ is irreducible and the extension $\mathrm{L}_h/\mathrm{K}$ defined by $h$ is isomorphic to $\mathrm{L}$. (Apply exer. 1 to the roots $x_i$ of $f$ and to a root $y$ of $h$.)
>
> (ii) Note that the $p$-adic valuation on $\mathbb{Q}_p$ extends uniquely to a valuation on $\overline{\mathbb{Q}}_p$; the latter is still called the $p$-adic valuation. Complete $\overline{\mathbb{Q}}_p$ with respect to the $p$-adic valuation and call it $C$. Use (i) to prove that $C$ is algebraically closed. (People often write $\mathbb{C}_p$ for this $C$.)