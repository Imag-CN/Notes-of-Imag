___

>[!definition]
>Let $X$ and $Y$ be Banach spaces, and let $U$ be an open subset of $X$.
>
>**Gâteaux Differentiability**
>A function $f: U \to Y$ is said to be Gâteaux differentiable at a point $x \in U$ if for every direction $h \in X$, the directional derivative
>$$
>df(x; h) = \lim_{t \to 0} \frac{f(x + t h) - f(x)}{t}
>$$
>exists in $Y$. If the mapping $h \mapsto df(x; h)$ is a **continuous linear operator** from $X$ to $Y$, then this operator is called the **Gâteaux derivative** of $f$ at $x$, often denoted by $D_G f(x)$ or $\nabla f(x)$. In this case, we have
$$
D_G f(x) \in \mathcal{L}(X, Y), \quad \text{and} \quad df(x; h) = D_G f(x)(h) \quad \forall h \in X.
$$

### Fréchet Differentiability
A function $f: U \to Y$ is said to be **Fréchet differentiable** at a point $x \in U$ if there exists a **continuous linear operator** $A \in \mathcal{L}(X, Y)$ such that
$$
\lim_{h \to 0} \frac{\|f(x + h) - f(x) - A(h)\|_Y}{\|h\|_X} = 0.
$$
Equivalently,
$$
f(x + h) = f(x) + A(h) + o(\|h\|_X) \quad \text{as} \quad h \to 0.
$$
The operator $A$ is uniquely determined and is called the **Fréchet derivative** of $f$ at $x$, denoted by $D_F f(x)$ or simply $f'(x)$.

> **Key Relations**:
> 1. If $f$ is **Fréchet differentiable** at $x$, then it is also **Gâteaux differentiable** at $x$, and the two derivatives coincide: $D_F f(x) = D_G f(x)$.
> 2. The converse is **not** true in general. A function can be Gâteaux differentiable (with a linear Gâteaux derivative) but not Fréchet differentiable, as shown by the $l^1$ norm example.
> 3. A sufficient condition for Gâteaux differentiability to imply Fréchet differentiability is that the Gâteaux derivative $D_G f(x)$ exists in a neighborhood of $x$ and is **continuous at $x$** (i.e., the mapping $x \mapsto D_G f(x)$ is continuous in the operator norm).

# Counterexample: A Banach Space Norm Gâteaux Differentiable but Not Fréchet Differentiable at Some Point

We note that for a Banach space $l$, the norm $\|\cdot\|$ is Gâteaux differentiable at $x_0$ if and only if all coordinates of $x_0$ are nonzero; moreover, the norm $\|\cdot\|$ is not Fréchet differentiable at any point $x_0\in l$.

In fact,

**(i)** If for some $\xi_n=0$, where $x=\{\xi_n\}$, then
$$
\frac{\|x+te_n\|-\|x\|}{t}=\frac{|t|}{t},
$$
which has no limit as $t\to0$. Therefore, the norm $\|\cdot\|$ is not Gâteaux differentiable at such $x$.

---

**(ii)** If $x=\{\xi_n\}$, and all $\xi_n\neq0$, for any $y=\{\eta_n\}\in l$ and $\varepsilon>0$, choose $n_0$ sufficiently large so that
$$
\sum_{n\geq n_0}|\eta_n|<\frac{\varepsilon}{2}.
$$
Then choose $\delta>0$ such that for $1\leq n\leq n_0$ and $|t|<\delta$, we have $\operatorname{sgn}(\xi_n+t\eta_n)=\operatorname{sgn}\xi_n$.
Let $x^*=\{\operatorname{sgn}\xi_n\}$. Then for $|t|<\delta$, we have
$$
\left|\frac{\|x+ty\|-\|x\|}{t}-x^*(y)\right|=\left|\frac{\|x+ty\|-\|x\|}{t}-\sum_{n=1}^{\infty}\operatorname{sgn}\xi_n\cdot\eta_n\right|
$$
$$
\leq\left|\sum_{n=1}^{n_0}\frac{|\xi_n+t\eta_n|-|\xi_n|-t\eta_n\operatorname{sgn}\xi_n}{t}\right|+2\sum_{n=1}^{\infty}|\eta_n|
$$
$$
=2\sum_{n>n_0}|\eta_n|<\varepsilon.
$$
Therefore, the norm $\|\cdot\|$ is Gâteaux differentiable at $x=\{\xi_n\}$, and its Gâteaux derivative is $\{\operatorname{sgn}\xi_n\}$.

---

**(iii)** It suffices to consider $x=\{\xi_n\},\xi_n\neq0,n=1,2,\cdots$. Let
$$
y_m=(0,\cdots,0,-2\xi_m,-2\xi_{m+1},\cdots),
$$
then as $m\to\infty$, $\|y_m\|\to0$. Note that $x^*=\{\operatorname{sgn}\xi_n\}$ is the only possible Fréchet derivative. However,
$$
\lim_{y_m\to0}\frac{\|x+y_m\|-\|x\|-x^*(y_m)}{\|y_m\|}=\lim_{y_m\to0}\frac{\left|\sum_{n\geq m}-2|\xi_n|\right|}{\|y_m\|}=\lim_{y_m\to0}\frac{\|y_m\|}{\|y_m\|}=1,
$$
so the norm $\|\cdot\|$ is not Fréchet differentiable at $x=\{\xi_n\}$.

---

