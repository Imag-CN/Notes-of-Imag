___
*Using DeepSeek to help write markdown problem statements, provided ideas for problem 2 and 3, and enhance writing conventions.*
___

> [!problem]
> Let $A$ be a Dedekind domain and $K$ its fraction field. Show that the following two sets are in bijection
> (1) the set of nonzero prime ideals $\mathfrak{p}$ of $A$
> (2) the set of discrete valuations $v$ on $K$ which have nonnegative values on $A$
> via $\mathfrak{p} \mapsto v_{\mathfrak{p}}$ and $v \mapsto \mathfrak{p}_v := \{a \in A : v(a) > 0\}$.

**Proof:**
Let $\Phi$ be $\mathfrak{p} \mapsto v_{\mathfrak{p}}$, let $\Psi$ be $v \mapsto \mathfrak{p}_v := \{a \in A : v(a) > 0\}$.

**1. $\Psi \circ \Phi = \operatorname{id}$:**

Take any nonzero prime ideal $\mathfrak{p} \subset A$. Then $\Phi(\mathfrak{p}) = v_{\mathfrak{p}}$, and
$$
\Psi(v_{\mathfrak{p}}) = \{a \in A : v_{\mathfrak{p}}(a) > 0\}.
$$
Since $v_{\mathfrak{p}}(a) > 0$ iff $a \in \mathfrak{p}$, we get $\Psi(v_{\mathfrak{p}}) = \mathfrak{p}$. Hence $\Psi(\Phi(\mathfrak{p})) = \mathfrak{p}$.

**2. $\Phi \circ \Psi = \operatorname{id}$:**

Take any discrete valuation $v$ on $K$ with $v(A) \ge 0$. Set $\mathfrak{p} = \mathfrak{p}_v = \{a \in A : v(a) > 0\}$, which is a nonzero prime ideal of $A$. Consider the local ring $A_{\mathfrak{p}}$. Since $A$ is a Dedekind domain, $A_{\mathfrak{p}}$ is a DVR with maximal ideal $\mathfrak{p}A_{\mathfrak{p}}$, whose valuation is exactly $v_{\mathfrak{p}}$.

Now observe that $v$ gives rise to a valuation ring $R_v = \{x \in K : v(x) \ge 0\}$. Since $v(A) \ge 0$, we have $A \subset R_v$, and the maximal ideal of $R_v$ is $\mathfrak{m}_v = \{x \in K : v(x) > 0\}$. By construction, $\mathfrak{p} = A \cap \mathfrak{m}_v$.

Because $A_{\mathfrak{p}}$ is the smallest DVR containing $A$ with maximal ideal extending $\mathfrak{p}$, it must coincide with $R_v$ as subrings of $K$. Consequently, their normalized valuations agree, thus they are identical: $v = v_{\mathfrak{p}}$.

Thus $\Phi(\Psi(v)) = \Phi(\mathfrak{p}) = v_{\mathfrak{p}} = v$.
___

