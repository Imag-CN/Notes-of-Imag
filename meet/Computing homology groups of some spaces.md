___

>[!problem] 
>For integers $m, n \geq 2$, let $X_{m,n}$ be the quotient space of a cylinder $S^1 \times I$ under the identifications $(z,0) \sim (e^{2\pi i/m} z, 0)$ and $(z,1) \sim (e^{2\pi i/n} z, 1)$.
>
>Compute the simplicial homology groups of $X_{m,n}$.

**Proof:**
Do triangulation as follows (take $X_{4,3}$ for example):

![[X_{4,3}.png]]

Then:
$$
\partial_{1}=0,
$$
$$
\partial_{2} a=\partial_{2} b=0,\quad \partial_{2} u_{i}=\partial_{2} v_{j}=B-A\quad (i=0,\dots,m,\quad j=0,\dots,n),
$$
$$
\partial_{3}U_{i}=u_{i-1}-a+u_{i},\quad \partial_{3}V_{j}=v_{j-1}-b+u_{j}\quad (i=0,\dots,m,\quad j=0,\dots,n).
$$
Thus
$$
\operatorname{im} \partial_{0}=0,\quad \operatorname{ker} \partial_{0}=\left< A,B \right>,
$$
$$
\operatorname{im}\partial_{1}=\left< B-A \right> ,\quad \operatorname{ker} \partial_{1}=\left<a,b, u_{i+1}-u_{i},v_{j+1}-v_{j}\mid i=0,\dots m-1, j=0,\dots n-1 \right> ,
$$
$$
\operatorname{im}\partial_{2}=\left< u_{i-1}-a+u_{i},v_{j-1}-b+u_{j}\mid i=0,\dots,m,\quad j=0,\dots,n \right> ,
$$
$$
\operatorname{ker} \partial_{2}=\begin{cases}
\left< U_{1}-U_{2}+\cdots-U_{m}+V_{1}-V_{2}+\dots-V_{n} \right> &, \text{if }m,n \text{ are both even}, \\
0&,\text{if } m \text{ or }n\text{ is odd}.
\end{cases}
$$

Therefore,
$$
H_{0}(X_{m,n})= \mathbb{Z},
$$
$$
H_{1}(X_{m,n})=
\mathbb{Z}\oplus \mathbb{Z}_{\operatorname{gcd}(m,n)},
$$
$$
H_{k}(X_{{m,n}})=0,\quad k\geq 2.
$$