>[!problem] Topologist's sine curve
>Let
>$$
>A=\{ (x,\sin{1/x}):x \in(0,1] \},B=\{ (0,y): y \in [-1,1] \},S=A\cup B
>$$
>$S$ is called topologist's sine curve. It is connected but not path connected.
#### 1. Connected

The set $A$ is the image of the connected interval $(0,1]$ under the continuous function $f: (0,1] \to \mathbb{R}^2$ defined by $f(x) = (x, \sin(1/x))$. Since the continuous image of a connected set is connected, $A$ is connected.

The closure of a connected set is connected. Since $S = \overline{A}$, it follows that $S$ is connected.
___
#### 2. Not path-connected

Assume, for contradiction, that there exists a continuous path $\gamma: [0,1] \to S$ such that $\gamma(0) = (0,0)$ and $\gamma(1) = (1, \sin(1))$.

Write $\gamma(t) = (x(t), y(t))$. Since $\gamma$ is continuous, $x(t)$ and $y(t)$ are continuous.

By definition, we have $x(0)=0,x(1)=1$ and $y(t)=\sin{\left( \dfrac{1}{x(t)} \right)},t>0$.

We recursively define a sequence $\{ t_{n} \}$:
- Choose $t_{1} \in(0,1)$ such that $x(t_{1})=\dfrac{1}{(1+1 /2)\pi}$;
- Choose $t_{n}\in(0,t_{n-1})$ such that $x(t_{n})=\dfrac{1}{(n+1 /2)\pi}$.
The Intermediate Value Theorem ensures the feasibility of these choices.

Since $\{ t_{n} \}$ is decreasing and bounded, it converges. However, $y(t_{n})=(-1)^n$ is divergent, which comes to a contradiction.