___

> [!problem] [ATI] 5.1
> Let $f: A \to B$ be an integral homomorphism of rings. Show that $f^*: \operatorname{Spec}(B) \to \operatorname{Spec}(A)$ is a closed mapping, i.e., that it maps closed sets to closed sets.

**Proof:**
Take $V(I)$ a basic closed set in $\operatorname{Spec}(B)$, let $J=I^{c}$. We prove 

For any $\mathfrak{p}\in V(J)$, by 5.10, there exists some $\mathfrak{q}$ such that $\mathfrak{q}^{c}=\mathfrak{p}$, i.e. $f^{*}(\mathfrak{q})=\mathfrak{p}$. Since $\mathfrak{p}\supset J$, we have $\mathfrak{q}^{c}\supset I^{c}$, thus $\mathfrak{q}\supset I$, i.e. $\mathfrak{q}\in V(I)$. Therefore, $\mathfrak{p}=f^{*}(\mathfrak{q})\in f^{*}(V(J))$.

For any $\mathfrak{q}\in f^{*}(V(I))$, suppose $\mathfrak{q}=\mathfrak{p}^{c}$ where $\mathfrak{p}\in V(I)$, then $\mathfrak{p}\supset I$ implies $\mathfrak{q}\supset J$, i.e. $\mathfrak{q}\in V(J)$.

Therefore, $f^{*}(V(I))=V(J)$, thus $f^{*}$ is a closed map.
___

