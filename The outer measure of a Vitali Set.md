___

>[!question] The outer measure of a Vitali Set
>What values can the outer measure of a Vitali set on $[0,1]$ take?

As 



Let $\mathfrak{c}$ denote the cardinal of the continuum and wellorder the Borel subsets of $[0, 1]$ as $(B_\alpha)_{\alpha < \mathfrak{c}}$. We build by transfinite recursion a sequence $(x_\alpha)_{\alpha < c}$ of elements of $[0, 1]$ such that:

(a) $x_\alpha$ is Vitali inequivalent to $x_\beta$ for all $\beta < \alpha$, and

(b) $x_\alpha \in [0, 1] \setminus B_\alpha$ if $[0, 1] \setminus B_\alpha$ is uncountable.

Note that this process can't get stuck, since if the complement of $B_\alpha$ is uncountable then it has cardinality $c$, and thus it meets an unused Vitali equivalence class (since at most $|\alpha| < c$ have been used so far). Then by setting $X = \{x_\alpha : \alpha < \mathfrak{c}\}$ we obtain a set such that whenever $B$ is a Borel set with $X \subseteq B$, then $B$ has countable complement (and in particular has measure $1$). So $X$ has outer measure $1$ as desired.