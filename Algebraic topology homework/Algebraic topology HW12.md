___

> [!problem] Problem 1
> Compute the singular homology groups for the quotient space $\mathbb{RP}^n/\mathbb{RP}^{n-2}$ for $n>2$.

**Proof:**
Since $\mathbb{RP}^{n-2}$ is the $n-2$ skeleton of $\mathbb{RP}^{n}$, $(\mathbb{RP}^{n},\mathbb{RP}^{n-2})$ is a good pair. Therefore, we have long exact sequence:
$$
\cdots \to \widetilde{H}_k(\mathbb{RP}^{n-2}) \to \widetilde{H}_k(\mathbb{RP}^n) \to \widetilde{H}_k(\mathbb{RP}^n/\mathbb{RP}^{n-2}) \to \widetilde{H}_{k-1}(\mathbb{RP}^{n-2}) \to \cdots
$$
For $\mathbb{RP}^m$:

$$
\widetilde{H}_k(\mathbb{RP}^m) = 
\begin{cases}
\mathbb{Z} & k=m \text{ and } m \text{ odd} \\
\mathbb{Z}/2\mathbb{Z} & 0<k<m \text{ and } k \text{ odd} \\
0 & \text{otherwise}
\end{cases}
$$

**Case 1: $n$ odd**
The LES yields:
- $k=n$: $0 \to \mathbb{Z} \to \widetilde{H}_n \to 0\Rightarrow\widetilde{H}_n = \mathbb{Z}$.
- $k=n-1$: $0 \to \widetilde{H}_{n-1} \to \mathbb{Z} \to 0\Rightarrow\widetilde{H}_{n-1} = \mathbb{Z}$.
- All other $\widetilde{H}_k = 0$.

Thus for $n$ odd: $\widetilde{H}_k = 0$ for $k\neq n-1,n$, and $\widetilde{H}_{n-1} = \mathbb{Z}$, $\widetilde{H}_n = \mathbb{Z}$.

**Case 2: $n$ even**  
The only possibly nonzero maps in LES are between $\mathbb{Z}/2$ groups. The LES splits into short exact sequences $0 \to \mathbb{Z}/2 \to \mathbb{Z}/2 \oplus \mathbb{Z}/2 \to \mathbb{Z}/2 \to 0$ etc, giving $\widetilde{H}_k=0$ for $k<n-1$.

At $k=n$: The quotient space is $S^{n-1} \cup_\eta e^n$ with $\eta$ degree $2$, giving cellular chain $0 \to \mathbb{Z} \xrightarrow{\times 2} \mathbb{Z} \to 0$ for degrees $n$ and $n-1$. Thus $\widetilde{H}_n =  \mathbb{Z}/2\mathbb{Z}$.

In conclusion:
For $n>2$:
- $n$ odd:
$$
\widetilde{H}_k(\mathbb{RP}^n/\mathbb{RP}^{n-2}) = 
\begin{cases}
\mathbb{Z} & k=n-1,n \\
0 & \text{otherwise}
\end{cases}
$$

- $n$ even:
$$
\widetilde{H}_k(\mathbb{RP}^n/\mathbb{RP}^{n-2}) = 
\begin{cases}
\mathbb{Z}/2\mathbb{Z} & k=n \\
0 & \text{otherwise}
\end{cases}
$$
___

> [!problem] Problem 2
> Is there a topological space $X$ such that for all non-negative integers $n$ the $n$th singular homology group is isomorphic to $\mathbb{Z}/n\mathbb{Z}$? If yes construct $X$, if no, then give a proof for the non-existence.

**Proof:**
Let $X_{n}$ be $S^{n}$ with a cell $e^{n+1}$ attached by a map $S_{n}\to S_{n}$ with degree $n$. Then the homology group $H_{k}(X_{n})$ of $X_{n}$ is $\mathbb{Z}/n\mathbb{Z}$ for $k=n$ and $0$ for $k\neq n$. Take $X=\wedge_{n\in \mathbb{N}^{+}}X_{n}$, where the base point is chosen as the $0$-skeleton of each $X_{n}$. Then such $X$ suffices.
___

> [!problem] Problem 3
> Let $K$ be the Kleinian bottle, $T$ be the $2$ dimensional torus and $P$ be the real projective plane. Is the Cartesian product $K\times K$ homeomorphic to $P\times T$? Prove your answer.

**Proof:**
The universal cover of $T$ and $K$ is $\mathbb{R}^{2}$, and the universal cover of $P$ is $S^{2}$. Thus the universal cover of $K\times K$ is $\mathbb{R}^{2}\times \mathbb{R}^{2}$, and the universal cover of $P\times T$ is $\mathbb{R}^{2}\times S^{2}$. Since $\mathbb{R}^{2}\times \mathbb{R}^{2}$ is contractible, while $\mathbb{R}^{2}\times S^{2}$ is not (because it is homotopy equivalent to $S^{2}$), $K\times K$ and $P\times T$ are not homeomorphic.
___

>[!problem] Problem 4
>Compute the Euler characteristic for the spaces $K\times K$ and $P\times T$ in Problem 3.

**Proof:**
Since we have:

|     | $0$-cells | $1$-cells | $2$-cells |
|:---:|:---------:|:---------:|:---------:|
| $K$ |    $1$    |    $2$    |    $1$    |
| $T$ |    $1$    |    $2$    |    $1$    |
| $P$ |    $2$    |    $2$    |    $1$    |

thus,

|             | $0$-cells | $1$-cells | $2$-cells | $3$-cells | $4$-cells |
| ----------- |:---------:|:---------:|:---------:|:---------:|:---------:|
| $K\times K$ |    $1$    |    $4$    |    $6$    |    $4$    |    $1$    |
| $P\times T$ |    $2$    |    $6$    |    $7$    |    $4$    |    $1$    |
Therefore, the Euler characteristic for the spaces $K\times K$ is $1-4+6-4+1=0$, and that for the space $P\times T$ is $2-6+7-4+1=0$.
