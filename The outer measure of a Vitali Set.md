___

>[!question] The outer measure of a Vitali Set
>What values can the outer measure of a Vitali set take?

A Vitali set is non-measurable, and hence its outer measure is nonzero. Since, for any $a>0$, a Vitali set can be constructed within the interval $[0,a]$, its outer measure must depend on the choice of representatives. In particular, one can construct a Vitali set contained in $[0,1]$ whose outer measure is exactly $1$.
___

>[!problem] A special case
>There exists a Vitali set on $[0,1]$ with outer measure $1$.

Let $\mathfrak{c}$ denote the cardinal of the continuum and wellorder the Borel subsets of $[0, 1]$ as $(B_\alpha)_{\alpha < \mathfrak{c}}$. We build by transfinite recursion a sequence $(x_\alpha)_{\alpha < c}$ of elements of $[0, 1]$ such that:

(a) $x_\alpha$ is Vitali inequivalent to $x_\beta$ for all $\beta < \alpha$, and

(b) $x_\alpha \in [0, 1] \setminus B_\alpha$ if $[0, 1] \setminus B_\alpha$ is uncountable.

Note that this process can't get stuck, since if the complement of $B_\alpha$ is uncountable then it has cardinality $c$, and thus it meets an unused Vitali equivalence class (since at most $|\alpha| < c$ have been used so far). Then by setting $X = \{x_\alpha : \alpha < \mathfrak{c}\}$ we obtain a set such that whenever $B$ is a Borel set with $X \subseteq B$, then $B$ has countable complement (and in particular has measure $1$). So $X$ has outer measure $1$ as desired.
___

Consider doing the similar process on $[0,a]$, we can also find a Vitali set with any given positive outer measure $a$.