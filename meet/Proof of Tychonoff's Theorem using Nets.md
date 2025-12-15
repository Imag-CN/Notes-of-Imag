___
>[!note] Tychonoff's Theorem
The product of any collection of compact topological spaces is compact in the product topology.

**Proof:**
We use a property of net: a space is compact if and only if every net has a convergent subnet.

Let $\{X_i\}_{i \in I}$ be compact spaces, $X = \prod X_i$.

Let $(x_\alpha)$ be a net in $X$ with index set $A$. We show it has a convergent subnet.

For each $i \in I$, the projection $(x_\alpha(i))$ is a net in compact $X_i$, hence has convergent subnet.

Let $\mathcal{F}=\{ J,(x_{h(\beta)})_{\beta \in B},L(i)_{i\in J} \}$, where $J\subseteq I$, $(x_{h(\beta)})_{\beta \in B}$ is a subnet of $(x_{\alpha})$ (i.e. $h:B\to A$ is an cofinal map), and $L(i)$ is the limit function on each coordinate of $J$ with $x_{h(\beta)}(i)\to L(i)$.

Define the partial order relation:
$\mathcal{F}=\{ J,(x_{h(\beta)})_{\beta \in B},L(i)_{i\in J} \}\preceq\mathcal{F}'=\{ J',(x_{h'(\beta)})_{\beta \in B'},L'(i)_{i\in J'} \}\iff$
- $J\subseteq J'$;
- $(x_{h'(\beta)})_{\beta \in B'}$ is a subnet of $(x_{h(\beta)})_{\beta \in B}$, i.e. exist an cofinal map $f:B'\to B$;
- For any $i\in J,L(i)=L'(i)$.

For any totally ordered ascending chain $\{ \mathcal{F}_{\lambda} \}_{\lambda \in\Lambda}$, we prove that it has an upper bound $\mathcal{F}^*$:
- Let $J^*=\bigcup_{\lambda \in\Lambda}J_{\lambda}$, then $J^*\supseteq J_{\lambda}$ for any $\lambda \in\Lambda$;
- For any $i\in J^*$, if $i\in J_{\lambda}$, then let $L^*(i)=L_{\lambda}(i)$;
- Choose direct set $D=\{ (\lambda,\beta):\lambda \in\Lambda,\beta \in B_{\lambda} \}$ with partial order: $(\lambda,\beta)\preceq(\lambda',\beta')\iff h_{\lambda}(\beta)\preceq h_{\lambda'}(\beta')$.
Define a map
$$
h^*:D\to A,h^*(\lambda,\beta)=h_{\lambda}(\beta)
$$
then $h^*$ is and cofinal, thus a subnet of $(x_{\alpha})$.
For any $\lambda_{0} \in\Lambda$, define a map:
$$f_{0}:D\to B_{\lambda_{0}},f(\lambda,\beta)=
\begin{cases}
\text{any fixed }\beta_{0}\in B_{\lambda_{0}} &,\text{ if }\lambda<\lambda_{0}\\
\beta &,\text{ if }\lambda=\lambda_{0} \\
f_{\lambda \to \lambda_{0}}(\beta)&,\text{ if }\lambda>\lambda_{0}
\end{cases}$$
where $f_{\lambda \to \lambda_{0}}:B_{\lambda}\to B_{\lambda_{0}}$ is a cofinal map.
Since $f_{0}$ is cofinal, $(x_{h^*(\lambda,\beta)})_{(\lambda,\beta)\in D}$ is a subnet of $(x_{h_{\lambda}(\beta)})_{\beta \in B_{\lambda}}$ for all $\lambda \in\Lambda$.

By Zorn's Lemma, there exists maximal family $\mathcal{F}=\{ J,(x_{h(\beta)})_{\beta \in B},L(i)_{i\in J} \}$.
If there exists $i \in I\setminus J$, then the projection $(x_{h(\beta)}(i))$ is a net in compact $X_i$, hence has convergent subnet, contradicting to maximality. Therefore $I=J$, $(x_{h(\beta)})_{\beta \in B}$ is a convergent subnet of $(x_{\alpha})$ on all coordinates.
___

>[!example] Compact but not sequentially compact space
>$X=\{ 0,1 \}^{[0,1]}$ endowed with product topology.

Tychonoff's Theorem shows that $X$ is a compact space. 

Let $f_{n}(x)= \text{ the } n\text{th digit of the }2\text{-adic expansion of }x$ (to ensure well-definedness, we do not allow the expansion to end with an infinite sequence of $1$s). Assume that $f_{n}$ has a convergent subsequence $f_{n_{k}}$. Let $t=\sum_{k\text{ odd}}2^{-n_{k}}$ , then $f_{n_{k}}(t)=[1-(-1)^k]/2$, not convergent, thus contradiction.

Since $X$ is compact, the sequence $(f_{n})$ has a convergent subnet. This shows a subnet of a sequence is not necessarily a subsequence; and a sequence without convergent subsequence may have a convergent subnet. However, we don't know if we can construct a convergent subnet of $(f_{n})$ explicitly since we prove its existence using the axiom of choice. If a sequence without convergent subsequence could have a convergent subnet remains a problem under ZF.
___
>[!tip] Two definitions of subnet
>1. **Willard's definition**
>Let $(x_\alpha)_{\alpha \in A}$ be a net in $X$. If there exists a function $\varphi: B \to A$ satisfying:
> - $\varphi$ is **order-preserving**: $\beta_1 \leq \beta_2 \Rightarrow \varphi(\beta_1) \leq \varphi(\beta_2)$
> - $\varphi$ is **cofinal**: for every $\alpha \in A$, there exists $\beta \in B$ such that $\varphi(\beta') \geq \alpha$ for all $\beta' \geq \beta$
>
>then the net $(x_{\varphi(\beta)})_{\beta \in B}$ is called a subnet of $(x_\alpha)_{\alpha \in A}$.
>
>2. **Kelley's definition**
>The same as the former definition except that $\varphi$ is not required to be order-preserving

In the proof we use the looser definition. It is convincing that to preserving limiting behavior requires only confinality.

Actually, every net has a convergent subnet $\Rightarrow$ compact can be proven under **ZF** alone with either definition, whereas its converse requires the **Axiom of Choice (AC)** under Kelly's definition and requires the **Boolean Prime Ideal (BPI) Theorem** under Willard's definition.

BPI is a proposition weaker then AC, and it's equivalent to that a space is compact if and only if every net has a convergent subnet under (Willard's definition), also equivalent to a weaker form of Tychonoff's Theorem: The product of any collection of compact Hausdorff topological spaces is compact in the product topology.

AC is equivalent to the general form of Tychonoff's Theorem.