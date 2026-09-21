___

>[!problem] Problem 1
>Let $L/\mathbb{Q}$ be a cubic field, namely $[L:\mathbb{Q}] = 3$, in which the prime $(2)$ splits completely.
>
>(i) Show that the ring of integers $\mathcal{O}_L$ (the integral closure of $\mathbb{Z}$ in $L$) is not monogenic, that is, $\mathcal{O}_L = \mathbb{Z}[\beta]$ for no element $\beta \in \mathcal{O}_L$.
>
>(ii) Consider $L = \mathbb{Q}(\alpha)$, where $\alpha$ is a root of $x^3 - x^2 - 2x - 8$. It is known that $\mathcal{O}_L = \mathbb{Z} \oplus \mathbb{Z}\alpha \oplus \mathbb{Z}\frac{\alpha^2+\alpha}{2}$ as a $\mathbb{Z}$-submodule of $L$. (We'll be able to prove this later but you need not check this in this homework.) Verify that the prime $(2)$ splits completely in $L$.

**Proof:**
**(i)** Assume for contradiction that $\mathcal{O}_L = \mathbb{Z}[\beta]$ for some $\beta \in \mathcal{O}_L$. Let $f(x) \in \mathbb{Z}[x]$ be the minimal polynomial of $\beta$, so $\deg f = 3$. Since $(2)$ splits completely in $L$, the reduction $\bar{f}(x) \in \mathbb{F}_2[x]$ factors into three distinct linear factors over $\mathbb{F}_2$. But $\mathbb{F}_2$ has only two distinct linear polynomials, namely $x$ and $x+1$, so it is impossible for $\bar{f}$ to have three distinct linear factors, contradiction. Hence $\mathcal{O}_L$ is not monogenic.

**(ii)** It suffices to prove $\mathcal{O}_L/(2) \cong \mathbb{F}_2^3$.

Let $\beta = \frac{\alpha^2 + \alpha}{2}$, so $\mathcal{O}_L = \{ x + y\alpha + z\beta \mid x,y,z \in \mathbb{Z} \}$.
From $\alpha^3 - \alpha^2 - 2\alpha - 8 = 0$ and $\beta = \frac{\alpha^2 + \alpha}{2}$, we obtain:
$$
\alpha^2 = -\alpha + 2\beta,\quad \alpha\beta = 2\beta + 4,\quad \beta^2 = 2\alpha + 3\beta + 2.
$$
Reducing modulo 2, we have:
$$
\overline{\alpha}^2 = \overline{\alpha},\quad \overline{\alpha}\,\overline{\beta} = \overline{0},\quad \overline{\beta}^2 = \overline{\beta}.
$$
Define a ring homomorphism $\varphi: \mathcal{O}_L/(2) \to \mathbb{F}_2 \oplus \mathbb{F}_2 \oplus \mathbb{F}_2$ by:
$$
\varphi(\overline{1}) = (1,1,1),\quad \varphi(\overline{\alpha}) = (1,0,0),\quad \varphi(\overline{\beta}) = (0,1,0).
$$
It is straightforward to verify that $\varphi$ is an isomorphism. Hence $\mathcal{O}_L/(2) \cong \mathbb{F}_2^3$, proving that $(2)$ splits completely in $L$.
___

> [!problem] Problem 2
> Consider $L = \mathbb{Q}(\sqrt{7}, \sqrt{10})$. Prove that $\mathcal{O}_L$ (notation as above) is not monogenic.



