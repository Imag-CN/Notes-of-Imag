___

>[!problem] [SHE] 6E.1
>Suppose $U$ is a subset of a metric space $V$. Show that $U$ is dense in $V$ if and only if every nonempty open subset of $V$ contains at least one element of $U$.

**Proof:**
$(\Rightarrow)$ Assume $\overline{U}=V$. Let $O$ be any nonempty open subset of $V$. If $O \cap U = \varnothing$, then $O \subset V \setminus U \subset V \setminus \overline{U}$. But $V \setminus \overline{U} = \varnothing$ since $\overline{U}=V$, contradicting that $O$ is nonempty. Therefore, $O \cap U \neq \varnothing$.

$(\Leftarrow)$ Assume every nonempty open subset of $V$ contains at least one point of $U$. For any $x \in V$ and any $\varepsilon > 0$, the open ball $B(x, \varepsilon)$ is a nonempty open subset. By assumption, $B(x, \varepsilon) \cap U \neq \varnothing$. Hence, $x$ is a limit point of $U$ (or $x \in U$ itself), so $x \in \overline{U}$. Since $x$ was arbitrary, $V \subset \overline{U}$, implying $\overline{U}=V$. Thus, $U$ is dense in $V$.
___

>[!problem] [SHE] 6E.8
>Suppose $(X,d)$ is a complete metric space and $G_1, G_2, \ldots$ is a sequence of dense open subsets of $X$. Prove that $\bigcap_{k=1}^{\infty} G_k$ is a dense subset of $X$.

**Proof:**
Suppose there exists $x\not\in\overline{ \bigcap_{k=1}^{\infty} G_k }$