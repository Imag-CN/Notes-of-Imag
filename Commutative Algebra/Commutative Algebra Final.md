___

> [!problem] Problem 0
> Describe the maximal ideals of $\mathbb{C}[x_1, \ldots, x_n]$.

**Proof:**
Let $\mathfrak{m}$ be a maximal ideal of $\mathbb{C}[x_{1},\dots ,x_{n}]$, consider the natural quotient map:
$$
\pi:\mathbb{C}[x_{1},\dots,x_{n}]\to L, \text{ where }L\text{ is defined as } \mathbb{C}[x_{1},\dots ,x_{n}] / \mathfrak{m}.
$$
let $f_{1}=\pi(x_{1}),\dots,f_{n}=\pi(x_{n})$, then since $\pi$ is surjective, we have $L=\mathbb{C}[f_{1},\dots,f_{n}]$. Thus $L$ is a finite $\mathbb{C}$-algebra. By Corollary 5.24 (or Corollary 7.20), $L$ is a finite field extension of $\mathbb{C}$. And since $\mathbb{C}$ is algebraically closed (so has no proper finite field extension), $L=\mathbb{C}$. Therefore, $\mathfrak{m}=\operatorname{ker}\pi \supseteq (x_{1}-f_{1},\dots,x_{n}-f_{n})$. Also,  
___

