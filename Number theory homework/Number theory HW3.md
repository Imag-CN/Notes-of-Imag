___

>[!problem] Problem 1
>Let $L/\mathbb{Q}$ be a cubic field, namely $[L:\mathbb{Q}] = 3$, in which the prime $(2)$ splits completely.
>
>(i) Show that the ring of integers $\mathcal{O}_L$ (the integral closure of $\mathbb{Z}$ in $L$) is not monogenic, that is, $\mathcal{O}_L = \mathbb{Z}[\beta]$ for no element $\beta \in \mathcal{O}_L$.
>
>(ii) Consider $L = \mathbb{Q}(\alpha)$, where $\alpha$ is a root of $x^3 - x^2 - 2x - 8$. It is known that $\mathcal{O}_L = \mathbb{Z} \oplus \mathbb{Z}\alpha \oplus \mathbb{Z}\frac{\alpha^2+\alpha}{2}$ as a $\mathbb{Z}$-submodule of $L$. (We'll be able to prove this later but you need not check this in this homework.) Verify that the prime $(2)$ splits completely in $L$.

**Proof:**
**(i)** Assume for contradiction that $\mathcal{O}_L = \mathbb{Z}[\beta]$ for some $\beta \in \mathcal{O}_L$. Let $f(x) \in \mathbb{Z}[x]$ be the minimal polynomial of $\beta$, so $\deg f = 3$. Since $(2)$ splits completely in $L$, the reduction $\bar{f}(x) \in \mathbb{F}_2[x]$ factors into three distinct linear factors over $\mathbb{F}_2$. But $\mathbb{F}_2$ has only two distinct linear polynomials, namely $x$ and $x+1$, so it is impossible for $\bar{f}$ to have three distinct linear factors, contradiction. Hence $\mathcal{O}_L$ is not monogenic.

**(ii)** Let $\alpha$ be a root of $f(x) = x^3 - x^2 - 2x - 8$. We know
$$\mathcal{O}_L = \mathbb{Z} \oplus \mathbb{Z}\alpha \oplus \mathbb{Z}\frac{\alpha^2+\alpha}{2}.$$
From $f(\alpha)=0$ we obtain
$$\alpha^3 - \alpha^2 - 2\alpha = 8.$$
Factor the left-hand side:
$$\alpha(\alpha^2 - \alpha - 2) = \alpha(\alpha-2)(\alpha+1) = 8.$$
Thus
$$\alpha \cdot \frac{\alpha+1}{2} \cdot \frac{\alpha-2}{2} = 2.$$
Note that $\alpha$, $\frac{\alpha+1}{2}$, $\frac{\alpha-2}{2} \in \mathcal{O}_L$ (the latter two lie in $\mathcal{O}_L$ because they are $\mathbb{Z}$-linear combinations of the basis elements). Their product equals $2$, showing that $(2) = \mathfrak{p}_1 \mathfrak{p}_2 \mathfrak{p}_3$ where $\mathfrak{p}_1 = (\alpha)$, $\mathfrak{p}_2 = (\frac{\alpha+1}{2})$, $\mathfrak{p}_3 = (\frac{\alpha-2}{2})$ are distinct prime ideals. Hence $(2)$ splits completely in $L$.
___

