___

> [!problem] Problem 1 ([SER] II.2.1)
> (Krasner's lemma) Let $E/K$ be a finite Galois extension of a non-Archimedean complete field $K$. Prolong the valuation of $K$ to $E$. Let $x \in E$ and let $\{x_1, \dots, x_n\}$ be the set of conjugates of $x$ over $K$, with $x = x_1$. Let $y \in E$ be such that $\|y - x\| < \|y - x_i\|$ for $i \ge 2$. Show that $x$ belongs to the field $K(y)$.

**Proof:**
Since $E/K$ is Galois, for any $K$-automorphism $\sigma:E\to E$, we have $\sigma(x)=x_i$ for some $i$; and $E/K(y)$ is Galois. Suppose that $x\notin K(y)$. Then there is a $K(y)$-automorphism $\sigma$ $E$ such that $\sigma(x)\ne x$. In particular, $\sigma(x)=x_i$ for some $i\ge2$.

By the uniqueness of extension of valuations, we have$\|y-x\|=\|\sigma(y-x)\|$. Because $\sigma$ fixes $y$, we have $\|\sigma(y-x)\|=\|y-\sigma(x)\|=\|y-x_i\|$, contradicting the assumption $\|y-x\|<\|y-x_i\| \quad (i\ge2)$.

Therefore $x$ has no conjugate over $K(y)$ other than itself, so $x\in K(y)$.
___

> [!problem] Problem 2
> (i) ([SER II.2.1]) Let $K$ be a non-Archimedean complete field, and let $f(\mathrm{X}) \in \mathrm{K}[\mathrm{X}]$ be a separable irreducible polynomial of degree $n$. Let $\mathrm{L}/\mathrm{K}$ be the extension of degree $n$ defined by $f$. Show that for every polynomial $h(\mathrm{X})$ of degree $n$ that is close enough to $f$, $h(\mathrm{X})$ is irreducible and the extension $\mathrm{L}_h/\mathrm{K}$ defined by $h$ is isomorphic to $\mathrm{L}$.
>
> (ii) Note that the $p$-adic valuation on $\mathbb{Q}_p$ extends uniquely to a valuation on $\overline{\mathbb{Q}}_p$; the latter is still called the $p$-adic valuation. Complete $\overline{\mathbb{Q}}_p$ with respect to the $p$-adic valuation and call it $C$. Use (i) to prove that $C$ is algebraically closed. (People often write $\mathbb{C}_p$ for this $C$.)

**Proof:**
**(i)** Let $x_1,\dots,x_n$ be the roots of $f$. Since $f$ is separable, $\|x_i-x_j\|>0$ for $i\ne j$. Choose $\varepsilon>0$ such that
$$
\varepsilon<\min_{i\ne j}\|x_i-x_j\|.
$$
If $h$ is sufficiently close to $f$, its roots $y_1,\dots,y_n$ can be rearranged so that $\|y_i-x_i\|<\varepsilon$ for every $i$ (by the continuity of polynomial functions, if the coefficients are close enough, then so are the roots). In particular,
$$
\|y_1-x_1\|<\|y_1-x_i\| \qquad (i\ge2).
$$
By Krasner's lemma, $x_1\in K(y_1)$. Hence $K(x_1)\subseteq K(y_1)$. Both extensions have degree $n$, so $K(x_1)=K(y_1)$. Similarly, $K(x_i)=K(y_i)\quad(i\geq2)$. 

Therefore, $h$ is irreducible (since $K(x_{1})\cong K[X]/(f(X))\cong K(X)/(h(X)) \cong K(y_{1})$) and $L_h\cong L$ (since $L_h\cong K(y_{1},\dots, y_{n}) \cong K(x_{1},\dots ,x_{n})\cong L$).

**(ii)** Let $g\in C[X]$ be a nonconstant polynomial. Choose a polynomial $f\in\overline{\mathbb{Q}}_p[X]$ of the same degree whose coefficients are sufficiently close to those of $g$. By (i), if $f$ is separable and irreducible in $\overline{ \mathbb{Q}_{p} }$, then $g$ has a root in $C$.

Since $\operatorname{char}\overline{ \mathbb{Q}_{p} }=0$, $\overline{ \mathbb{Q}_{p} }$ is perfect, $f$ is also separable. More generally, factor $f$ over $\overline{\mathbb{Q}}_p$ and choose one factor $h$ corresponding to a root of $g$. By (i), a sufficiently small perturbation of $h$ has a root in $\overline{\mathbb{Q}}_p$. Since $\overline{\mathbb{Q}}_p$ is dense in $C$, every polynomial over $C$ can therefore be approximated by polynomials having roots in $C$. Applying (i) to a sufficiently close approximation shows that $g$ itself has a root in $C$.

Hence every nonconstant polynomial in $C[X]$ has a root in $C$, so $C$ is algebraically closed.

