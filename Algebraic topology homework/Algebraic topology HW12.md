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

**Case 1: $n$ odd ($n=2l+1$).**  
Then $\widetilde{H}_*(\mathbb{RP}^{n-2})$: $\mathbb{Z}$ in degree $n-2$, $0$ elsewhere.  
$\widetilde{H}_*(\mathbb{RP}^n)$: $\mathbb{Z}$ in degree $n$, $0$ elsewhere.

The LES yields:
- $k=n$: $0 \to \mathbb{Z} \to \widetilde{H}_n \to 0$ ⇒ $\widetilde{H}_n = \mathbb{Z}$.
- $k=n-1$: $0 \to \widetilde{H}_{n-1} \to \mathbb{Z} \to 0$ ⇒ $\widetilde{H}_{n-1} = \mathbb{Z}$.
- All other $\widetilde{H}_k = 0$.

Thus for $n$ odd: $\widetilde{H}_k = 0$ for $k\neq n-1,n$, and $\widetilde{H}_{n-1} = \mathbb{Z}$, $\widetilde{H}_n = \mathbb{Z}$.

**Case 2: $n$ even ($n=2l$).**  
Then $\widetilde{H}_*(\mathbb{RP}^{n-2})$: $\mathbb{Z}/2$ in degrees odd $<n-2$, 0 elsewhere. 
$\widetilde{H}_*(\mathbb{RP}^n)$: $\mathbb{Z}/2$ in degrees odd $<n$, 0 elsewhere.

The only possibly nonzero maps in LES are between $\mathbb{Z}/2$ groups. The LES splits into short exact sequences $0 \to \mathbb{Z}/2 \to \mathbb{Z}/2 \oplus \mathbb{Z}/2 \to \mathbb{Z}/2 \to 0$ etc, giving $\widetilde{H}_k=0$ for $k<n-1$.

At $k=n$: $0 \to \widetilde{H}_n \to 0$ ⇒ $\widetilde{H}_n = 0$ initially, but wait — careful: $\widetilde{H}_n(\mathbb{RP}^n)=0$ since $n$ even. But the quotient space is $S^{n-1} \cup_\eta e^n$ with $\eta$ degree 2, giving cellular chain $0 \to \mathbb{Z} \xrightarrow{\times 2} \mathbb{Z} \to 0$ for degrees $n$ and $n-1$.

Thus $\widetilde{H}_n =  \mathbb{Z}/2\mathbb{Z}$.

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