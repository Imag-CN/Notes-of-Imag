___

> [!problem] Problem 1
> Prove that
> $$
> SL_{2}(\mathbb{Z})\cong\langle S,T|S^{4}=1,(ST)^{3}=S^{2}\rangle.
> $$

**Proof:**
See Christion Kassel, Vladimir Yuraev, *Braid Groups*, p327.

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
**(i)** See Christion Kassel, Vladimir Yuraev, *Braid Groups*, p151.

**(ii)** Define $x=(1,2)$ and $y=(1,2,\ldots,n)$. 

Note that $s_i=y^{i-1}xy^{-(i+1)}$ for $1\leq i\leq n-1$.

Substituting into the relations from (i) yields the solution.
