___

>[!problem] Problem 1
>Let $L/\mathbb{Q}$ be a cubic field, namely $[L:\mathbb{Q}] = 3$, in which the prime $(2)$ splits completely.
>
>(i) Show that the ring of integers $\mathcal{O}_L$ (the integral closure of $\mathbb{Z}$ in $L$) is not monogenic, that is, $\mathcal{O}_L = \mathbb{Z}[\beta]$ for no element $\beta \in \mathcal{O}_L$.
>
>(ii) Consider $L = \mathbb{Q}(\alpha)$, where $\alpha$ is a root of $x^3 - x^2 - 2x - 8$. It is known that $\mathcal{O}_L = \mathbb{Z} \oplus \mathbb{Z}\alpha \oplus \mathbb{Z}\frac{\alpha^2+\alpha}{2}$ as a $\mathbb{Z}$-submodule of $L$. (We'll be able to prove this later but you need not check this in this homework.) Verify that the prime $(2)$ splits completely in $L$.

**Proof:**
**(i)** Suppose $\mathcal{O}_L = \mathbb{Z}[\beta]=\mathbb{Z}[x]/(f)$ for some element $\beta \in \mathcal{O}_L$ with minimal polynomial $f\in \mathbb{Z}[x]$, clearly $\operatorname{deg} f=3$. Then the prime $(2)$ splits completely implies $f$ splits into $3$ distinct linear factors when $\operatorname{Mod}2$. This is not possible since there are only $2$ distinct polynomial of $\operatorname{deg}1$ in $\mathbb{F}_{2}[x]$ ($x$ and $x+1$).

**(ii)** $\alpha^{3}-\alpha^{2}-2\alpha-8=0$ implies $2=\alpha \cdot \dfrac{\alpha+1}{2}\cdot \dfrac{\alpha-2}{2}$