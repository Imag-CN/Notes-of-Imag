___

> [!problem] [HAT] 0.1.6
> (a) Let $X$ be the subspace of $\mathbb{R}^{2}$ consisting of the horizontal segment $[0,1]\times\{0\}$ together with all the vertical segments $\{r\}\times[0,1-r]$ for $r$ a rational number in $[0,1]$. Show that $X$ deformation retracts to any point in the segment $[0,1]\times\{0\}$, but not to any other point.
>
>(b) Let $Y$ be the subspace of $\mathbb{R}^{2}$ that is the union of an infinite number of copies of $X$ arranged as in the figure below. Show that $Y$ is contractible but does not deformation retract onto any point.
>
>(c) Let $Z$ be the zigzag subspace of $Y$ homeomorphic to $\mathbb{R}$, indicated by the heavier line. Show there is a deformation retraction in the weak sense (see Exercise 4) of $Y$ onto $Z$, but no true deformation retraction.

**Proof:**
**(a)** For a point $p=(x_0,0)$ on the base segment, define $F:X\times[0,1]\to X$ by:

1. On vertical segment $\{r\}\times[0,1-r]$: $F((r,y),t)=(r,(1-t)y)$
2. On base segment $[0,1]\times\{0\}$: $F((x,0),t)=((1-t)x+tx_0,0)$

These combine to give a deformation retraction onto $p$.

To see $X$ cannot deformation retract to any other point $q=(r,y_0)$ with $y_0>0$: any such deformation would have to move points on nearby vertical segments continuously to $q$, but rational points are dense and irrational points have no vertical segments, creating discontinuities.

**(b)** Each copy of $X$ deformation retracts to its base segment. Gluing these retractions gives a deformation retraction of $Y$ onto a line homeomorphic to $\mathbb{R}$, which is contractible. Thus $Y$ is contractible.

However, $Y$ cannot deformation retract onto any point $p$: the space is "infinitely branched" with gaps at irrationals, so any continuous deformation to a point would force distinct components to merge discontinuously.

**(c)** Define a weak deformation retraction $H:Y\times[0,1]\to Y$ by:

1. First contract each vertical segment linearly to its base
2. Then project each base point vertically onto the zigzag $Z$

This satisfies $H(y,0)=y$, $H(y,1)\in Z$, and $H(z,t)=z$ for $z\in Z$.

A true deformation retraction would require $H(y,1)=z_0$ (fixed point), making $Y$ contractible to a point, contradicting (b). Thus no true deformation retraction exists.
___

> [!problem] [HAT] 2.1.1
> What familiar space is the quotient $\Delta$-complex of a 2-simplex $[v_0, v_1, v_2]$ obtained by identifying the edges $[v_0, v_1]$ and $[v_1, v_2]$, preserving the ordering of vertices?

**Proof:** Klein bottle.
___

> [!problem] [HAT] 2.1.9
> Compute the homology groups of the $\Delta$-complex $X$ obtained from $\Delta^{n}$ by identifying all faces of the same dimension. Thus $X$ has a single $k$-simplex for each $k\le n$.

**Proof:**
Let $e_k$ be the unique $k$-simplex. Chain groups $C_k=\mathbb{Z}$ for $0\le k\le n$.

Boundary maps:
$$
\partial e_k=
\begin{cases}
0,&k\text{ odd},\\
e_{k-1},&k\text{ even, }k\ge1.
\end{cases}
$$

Thus the chain complex is
$$
0\to\mathbb{Z}\xrightarrow{\partial_n}\mathbb{Z}\xrightarrow{\partial_{n-1}}\cdots\xrightarrow{\partial_1}\mathbb{Z}\to0
$$
with $\partial_k=\begin{cases}0,&k\text{ odd}\\1,&k\text{ even}\end{cases}$ (multiplication by 1).

Hence
$$
H_k(X)\cong
\begin{cases}
\mathbb{Z},&k=0,\\
\mathbb{Z},&k=n\ \text{and}\ n\ \text{odd},\\
0,&\text{otherwise}.
\end{cases}
$$
___

> [!problem] [HAT] 2.1.16
> (a) Show that $H_0(X,A)=0$ iff $A$ meets each path-component of $X$.
> (b) Show that $H_1(X,A)=0$ iff the map $H_1(A)\to H_1(X)$ is surjective and each path-component of $X$ contains at most one path-component of $A$.

**Proof:**
**(a)** Recall the long exact sequence
$$
\cdots\to H_0(A)\xrightarrow{i_*}H_0(X)\xrightarrow{j_*}H_0(X,A)\to0.
$$
Since $H_0(X)$ is free abelian on the set of path-components of $X$, and $i_*$ sends the component of a point $a\in A$ to the component of $i(a)\in X$, we have
$$
H_0(X,A)=\operatorname{coker}i_*\cong\mathbb{Z}^{\{\text{components of }X\text{ not met by }A\}}.
$$
Thus $H_0(X,A)=0$ iff $A$ meets every path-component of $X$.

**(b)** From the long exact sequence
$$
H_1(A)\xrightarrow{i_*}H_1(X)\xrightarrow{j_*}H_1(X,A)\to H_0(A)\xrightarrow{i_*}H_0(X)
$$
we have $H_1(X,A)=0$ iff $i_*:H_1(A)\to H_1(X)$ is surjective and the map $H_0(A)\to H_0(X)$ is injective.

Now $H_0(A)\to H_0(X)$ is injective iff distinct components of $A$ are mapped to distinct components of $X$, i.e., each component of $X$ contains at most one component of $A$.

Hence $H_1(X,A)=0$ iff $i_*:H_1(A)\to H_1(X)$ is surjective and each component of $X$ contains at most one component of $A$.