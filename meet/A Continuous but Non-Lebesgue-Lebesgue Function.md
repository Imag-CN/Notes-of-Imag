___

>[!problem]
>Let 
>$$
>f:[0,1]\to[0,1] , f(x)= \dfrac{\phi(x)+x}{2},
>$$
>where $\phi(x)$ is the Cantor function. Denote $\mu$ the Lebesgue measure.
>
>(i) Prove that $f$ is a continuous strictly increasing bijection.
>
>(ii) Let $C$ be the Cantor set, evaluate $\mu(f(C))$.

**Proof:**
**(i)** We know $\phi$ is a continuous and increasing, $x$ is continuous and strictly increasing, thus $f$ is continuous and strictly increasing. Since $f(0)=0$ and $f(1)=1$, $f$ is a bijection (injectivity by strictly increasing and surjectivity by Intermediate Value Theorem).

**(ii)** Let $D$ be the complement of $C$ in $[0,1]$, then $\mu (D)=\mu([0,1])-\mu(C)=1$, and $D$ has the form $D=\bigsqcup_{k=1}^{\infty} I_k$ where
$$
\begin{aligned}
I_1 &= \left(\frac{1}{3}, \frac{2}{3}\right), \\
I_2 &= \left(\frac{1}{9}, \frac{2}{9}\right) \cup \left(\frac{7}{9}, \frac{8}{9}\right), \\
I_3 &= \left(\frac{1}{27}, \frac{2}{27}\right) \cup \left(\frac{7}{27}, \frac{8}{27}\right) \cup \left(\frac{19}{27}, \frac{20}{27}\right) \cup \left(\frac{25}{27}, \frac{26}{27}\right), \\
& \vdots
\end{aligned}
$$
Because $f$ is a bijection, $f(D)=\bigsqcup_{k=1}^{\infty} I_k$. Since $\phi$ is constant restricted on each $I_{k}$ , we have
$$
\mu(f(D))=\sum_{k=1}^{\infty}\mu(f(I_{k}))=\sum_{k=1}^{\infty}\mu(I_{k} /2)=\mu(D) /2= 1 /2.
$$
Therefore, $\mu(f(C))=1-\mu(f(D))= 1 /2$.
___

Through the problem above we are able to construct a continuous but non-Lebesgue-Lebesgue function.

>[!example] 
>Let $g$ be the inverse function of $f$ where $f$ is the same $f$ of the previous problem. Then $g$ is continuous. Let $W$ be a non-measurable subset of $f(C)$ (we can also take a non-measurable subset from a set with positive outer measure through the similar construction with Vitali set). Then $g(W)$ is a Lebesgue set (since it is a subset of the Cantor set, thus a null set), but $g^{-1}(g(W))=W$ is not a Lebesgue set.

