___

> [!problem] Problem 1
> (1) Show that the inclusion $\mathcal{O}_{\overline{\mathbb{Q}}_p}\subset\mathcal{O}_C$ induces isomorphisms
> $$
> \mathcal{O}_{\overline{\mathbb{Q}}_p}/p\mathcal{O}_{\overline{\mathbb{Q}}_p}\cong\mathcal{O}_C/p\mathcal{O}_C
> \quad\text{and}\quad
> \mathcal{O}_{\overline{\mathbb{Q}}_p}/\mathfrak{m}_{\overline{\mathbb{Q}}_p}\cong\mathcal{O}_C/\mathfrak{m}_C.
> $$
> (It is not hard to see that the residue field $\mathcal{O}_{\overline{\mathbb{Q}}_p}/\mathfrak{m}_{\overline{\mathbb{Q}}_p}$ is $\overline{\mathbb{F}}_p$ since it is an algebraic extension of $\mathbb{F}_p$ containing an arbitrary finite extension of $\mathbb{F}_p$ in light of Problem Set 06, #3.)
>
> (2) Show that $\Gamma=p^{\mathbb{Q}}=\{p^a:a\in\mathbb{Q}\}$ in this case, if we normalize the valuation such that $|p|=1/p$.
>
> (3) Check that the Frobenius map $\mathcal{O}_C/p\mathcal{O}_C\longrightarrow\mathcal{O}_C/p\mathcal{O}_C$ is surjective.

**Proof:**
Write $F=\overline{\mathbb{Q}}_p$.

**(1)** In either valuation ring, $p\mathcal{O}=\{x:|x|\le|p|\}$ and $\mathfrak{m}=\{x:|x|<1\}$. Hence
$$
\mathcal{O}_F\cap p\mathcal{O}_C=p\mathcal{O}_F,
\qquad
\mathcal{O}_F\cap\mathfrak{m}_C=\mathfrak{m}_F,
$$
so both induced maps are injective.

For any $x\in\mathcal{O}_C$, density of $F$ in $C$ gives $y\in F$ with $|x-y|<|p|$. The ultrametric inequality gives $|y|\le1$, so $y\in\mathcal{O}_F$. Since $x-y\in p\mathcal{O}_C\subset\mathfrak{m}_C$, both maps are surjective.

**(2)** Every $y\in F^\times$ lies in a finite extension $L/\mathbb{Q}_p$. If its ramification index is $e$, then $|L^\times|=p^{(1/e)\mathbb{Z}}\subset p^{\mathbb{Q}}$. Conversely, $|p^{1/n}|=p^{-1/n}$ for every $n\ge1$, so $|F^\times|=p^{\mathbb{Q}}$.

For $x\in C^\times$, choose $y\in F$ with $|x-y|<|x|$. Then $|y|=|x|$, so completion adds no new values. Thus $\Gamma=p^{\mathbb{Q}}$.

**(3)** Given $x\in\mathcal{O}_C$, choose $y\in\mathcal{O}_F$ with $x-y\in p\mathcal{O}_C$ by (1). Since $F$ is algebraically closed, there exists $z\in F$ with $z^p=y$. Then $|z|^p=|y|\le1$, so $z\in\mathcal{O}_F$, and $z^p\equiv x\pmod{p\mathcal{O}_C}$. Therefore Frobenius is surjective.
___

