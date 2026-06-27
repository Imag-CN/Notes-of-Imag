___

> [!problem] Problem 0
> Describe the maximal ideals of $\mathbb{C}[x_1, \ldots, x_n]$.

**Proof:**
Let $\mathfrak{m}$ be a maximal ideal of $\mathbb{C}[x_{1},\dots ,x_{n}]$, consider the natural quotient map:
$$
\pi:\mathbb{C}[x_{1},\dots,x_{n}]\to L, \text{ where }L\text{ is defined as } \mathbb{C}[x_{1},\dots ,x_{n}] / \mathfrak{m}\text{ (thus $L$ is a field)}.
$$
let $f_{1}=\pi(x_{1}),\dots,f_{n}=\pi(x_{n})$, then since $\pi$ is surjective, we have $L=\mathbb{C}[f_{1},\dots,f_{n}]$. Thus $L$ is a finite $\mathbb{C}$-algebra. By Corollary 5.24 (or Corollary 7.20), $L$ is a finite field extension of $\mathbb{C}$, thus $f_{1},\dots,f_{n}$ is algebraic over $\mathbb{C}$. And since $\mathbb{C}$ is algebraically closed, $f_{1},\dots,f_{n}\in \mathbb{C}$. Therefore, $(x_{1}-f_{1},\dots,x_{n}-f_{n})$ is an ideal of $\mathbb{C}[x_{1},\dots,x_{n}]$, and it is a maximal ideal because $\mathbb{C}[x_{1},\dots,x_{n}] / (x_{1}-f_{1},\dots,x_{n}-f_{n})\cong \mathbb{C}$. Since $\pi(x_{1}-f_{1})=\dots=\pi(x_{n}-f_{n})=0$, we have $\mathfrak{m}=\operatorname{ker}\pi \supseteq (x_{1}-f_{1},\dots,x_{n}-f_{n})$. And since $(x_{1}-f_{1},\dots,x_{n}-f_{n})$ is maximal, $\mathfrak{m}=(x_{1}-f_{1},\dots,x_{n}-f_{n})$.

In conclusion, any maximal ideal of $\mathbb{C}[x_1, \ldots, x_n]$ has the form $(x_{1}-f_{1},\dots,x_{n}-f_{n})$ for some $f_{1},\dots f_{n}\in \mathbb{C}$. (Also, for any $f_{1},\dots f_{n}\in \mathbb{C}$, $(x_{1}-f_{1},\dots,x_{n}-f_{n})$ is a maximal ideal, because the quotient is $\mathbb{C}$).
___

> [!problem] Problem 1
> Using group action on rings, show that $R := \mathbb{C}[x,y,z,w]/(xy - zw)$ is integrally closed. Is this a Noetherian ring? Is the localization of this ring at every prime ideal $R_{\mathfrak{p}}$ a Regular Local Ring? Is $R_{\mathfrak{p}}$ Cohen-Macaulay?

