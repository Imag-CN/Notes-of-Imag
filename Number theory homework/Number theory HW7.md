___

Fix an algebraic closure $\overline{\mathbb{Q}}_p$ of $\mathbb{Q}_p$, and choose a compatible system of $p$-power roots $p^{1/p},p^{1/p^2},\ldots$ in $\overline{\mathbb{Q}}_p$, so that
$$
(p^{1/p^{i+1}})^p=p^{1/p^i}\qquad(i\ge1).
$$
Similarly, choose compatible primitive $p$-power roots of unity $\zeta_p,\zeta_{p^2},\ldots$, so that $\zeta_{p^{i+1}}^p=\zeta_{p^i}$. Define
$$
\mathbb{Q}_p(p^{1/p^\infty}):=\bigcup_{i\ge1}\mathbb{Q}_p(p^{1/p^i}),\qquad
\mathbb{Q}_p(\zeta_{p^\infty}):=\bigcup_{i\ge1}\mathbb{Q}_p(\zeta_{p^i}).
$$
**[Fact]** You are encouraged to verify the following, but are welcome to take it for granted. These are infinite extensions of $\mathbb{Q}_p$ that are totally ramified, meaning that every finite subextension is totally ramified, or equivalently that their residue fields are still $\mathbb{F}_p$. Their completions
$$
\widehat{\mathbb{Q}_p(p^{1/p^\infty})},\qquad
\widehat{\mathbb{Q}_p(\zeta_{p^\infty})}
$$
are perfectoid fields.

On the other hand, the valuation on the complete discretely valued field $\mathbb{F}_p((t))$ extends uniquely to
$$
\mathbb{F}_p((t^{1/p^\infty})):=\bigcup_{i\ge1}\mathbb{F}_p((t^{1/p^i})),
$$
where $t^{1/p},t^{1/p^2},\ldots$ form a compatible system of $p$-power roots of $t$. Another way to think of $\mathbb{F}_p((t^{1/p^\infty}))$ is as the perfection of $\mathbb{F}_p((t))$, just as $\mathbb{F}_p[X^{p^{-\infty}}]$ is the perfection of $\mathbb{F}_p[X]$. The completion $\widehat{\mathbb{F}_p((t^{1/p^\infty}))}$ is also a perfectoid field, now of characteristic $p$.

You can identify the valuation rings of
$$
\mathbb{Q}_p(p^{1/p^\infty}),\qquad
\mathbb{Q}_p(\zeta_{p^\infty}),\qquad
\mathbb{F}_p((t^{1/p^\infty}))
$$
by applying [S, I, §6] to finite subextensions. The last case involves inseparable extensions, but the argument in [S, I, §6, (ii)] still applies; alternatively, compute its valuation ring directly as
$$
\bigcup_{i\ge1}\mathbb{F}_p[[t^{1/p^i}]].
$$
The valuation rings of the completions are obtained by taking closures.

>[!problem] Problem 1
> (1) Take $K:=\widehat{\mathbb{Q}_p(p^{1/p^\infty})}$. Show that, as topological fields,
> $$
> K^\flat\cong\widehat{\mathbb{F}_p((t^{1/p^\infty}))}.
> $$
>
> (2) For $K:=\widehat{\mathbb{Q}_p(\zeta_{p^\infty})}$, show that, as topological fields,
> $$
> K^\flat\cong\widehat{\mathbb{F}_p((t^{1/p^\infty}))}.
> $$
>
> (3) Show that the two fields
> $$
> \widehat{\mathbb{Q}_p(p^{1/p^\infty})},\qquad
> \widehat{\mathbb{Q}_p(\zeta_{p^\infty})}
> $$
> are not isomorphic over $\mathbb{Q}_p$.
>
> **[Remark]** Nonisomorphic perfectoid fields can have isomorphic tilts. The fields $\widehat{\mathbb{Q}_p(p^{1/p^\infty})}$ and $\widehat{\mathbb{Q}_p(\zeta_{p^\infty})}$ are different untilts of $\widehat{\mathbb{F}_p((t^{1/p^\infty}))}$.

