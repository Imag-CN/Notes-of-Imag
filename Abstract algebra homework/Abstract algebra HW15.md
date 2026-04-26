___

> [!problem] Problem 1
> Prove that
> $$
> SL_{2}(\mathbb{Z})\cong\langle S,T|S^{4}=1,(ST)^{3}=S^{2}\rangle.
> $$

See 

___

> [!problem] Problem 2
> Let $S_n$ be the symmetric group. Let $s_i=(i,i+1)$ for $1\leq i\leq n-1$.
> (i) Prove that
> $$S_n=\left\langle s_1,\ldots,s_{n-1}\left|
> \begin{aligned}
> &s_i^2=1\quad&(1\leq i\leq n-1),\\
> &s_is_j=s_js_i\quad&(|i-j|\geq2),\\
> &s_is_{i+1}s_i=s_{i+1}s_is_{i+1}\quad&(1\leq i\leq n-2)
> \end{aligned}
> \right.\right\rangle.$$
> (ii) We have proved that $x=(1,2)$ and $y=(1,2,\ldots,n)$ generate $S_n$. Use the above relations to find complete relations between $x$ and $y$, and find a presentation of $S_n$ using 2 generators.

**Proof:**
**(i)** Let $G=\langle s_1,\ldots,s_{n-1}\mid R\rangle$ be the group with the given presentation, where $R$ consists of the three types of relations.

Define a homomorphism $\phi:G\to S_n$ by $\phi(s_i)=(i,i+1)$ for $1\leq i\leq n-1$. This is well-defined because the permutations $(i,i+1)$ satisfy the same relations in $S_n$.

Since the adjacent transpositions generate $S_n$, $\phi$ is surjective.

Consider the natural action of $G$ on $\{1,\ldots,n\}$ defined by letting $s_i$ act as $(i,i+1)$. The relations ensure this action is faithful. Since $S_n$ is the full symmetric group on $n$ letters and $|S_n|=n!$, we conclude $\phi$ is an isomorphism.

Thus $G\cong S_n$, proving the presentation.

**(ii)** Define $x=(1,2)$ and $y=(1,2,\ldots,n)$. 

Note that $s_i=y^{i-1}xy^{-(i+1)}$ for $1\leq i\leq n-1$.

Substituting into the relations from (i):

1. $s_i^2=1$ gives $x^2=1$ (since all other $s_i$ are conjugates of $x$).
2. The braid relation $s_is_{i+1}s_i=s_{i+1}s_is_{i+1}$ for $i=1$ gives $xyx=yxy$.
3. The commuting relations $s_is_j=s_js_i$ for $|i-j|\geq2$ give $x(y^jxy^{-j})=(y^jxy^{-j})x$ for $j=2,\ldots,n-2$.
4. We also have $y^n=1$ since $y$ is an $n$-cycle.

Thus a presentation for $S_n$ with generators $x,y$ is:

$$
S_n\cong\left\langle x,y\left|
\begin{aligned}
&x^2=1,\quad y^n=1,\\
&xyx=yxy,\\
&x(y^jxy^{-j})=(y^jxy^{-j})x\quad\text{for }j=2,\ldots,n-2
\end{aligned}
\right.\right\rangle
$$
