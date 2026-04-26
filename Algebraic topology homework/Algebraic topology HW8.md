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

