___
*Using DeepSeek to help write markdown problem statements, and enhance writing conventions.*
___

> [!problem] Problem 1
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

Because $A_{\mathfrak{p}}$ is the smallest DVR containing $A$ with maximal ideal extending $\mathfrak{p}$, it must coincide with $R_v$ as subrings of $K$. Consequently, their valuations agree: $v = v_{\mathfrak{p}}$.

Thus $\Phi(\Psi(v)) = \Phi(\mathfrak{p}) = v_{\mathfrak{p}} = v$.
___

> [!problem] Problem 2
> Let $K=\mathbb{Q}$, $L=\mathbb{Q}(\zeta_p)$, where $\zeta_p$ is a primitive $p$-th root of unity. Set $A=\mathbb{Z}$. Let $B$ be the integral closure of $A$ in $L$.
>
> Prove the following:
>
> (1)
> $$
> p = \prod_{i=1}^{p-1}(1-\zeta_p^i)
> $$
> (2)
> Show that
> $$
> (p) = (1-\zeta_p)^{p-1}
> $$
> as ideals of $B$. From this deduce that $(p)$ is totally ramified in $\mathbb{Q}(\zeta_p)/\mathbb{Q}$.

**Proof:**
**(1)** Note that
$$
x^{p}-1=\prod_{i=1}^{p}(x-\zeta_p^i),
$$
divide both sides by $(x-1)$ yields
$$
\sum_{i=0}^{p-1}x^{i}=\prod_{i=1}^{p-1}(x-\zeta_p^i),
$$
substitute $x=1$ gives the equation required.

**(2)** Since $\zeta_{p}$ is the root of $x^{p}-1$, it is in $B$. For $1\leq i\leq p-1$, we have $1-\zeta_{p}^{i}=(1-\zeta_{p})(1+\zeta_{p}+\dots+\zeta_{p}^{i-1})$, and $1-\zeta_{p}=1-\zeta_{p}^{ij}=(1-\zeta_{p}^{i})(1+\zeta_{p}^{i}+\dots+\zeta_{p}^{i(j-1)})$, where $j$ is the inverse of $i$ in $\mathbb{F}_{p}$. Therefore, $(1-\zeta_{p})=(1-\zeta_{p}^{i})$ as ideals in $B$ for $1\leq i\leq p-1$.

Combined with **(a)**, we have:
$$
(p) =\prod_{i=1}^{p-1}(1-\zeta_p^i)= (1-\zeta_p)^{p-1}
$$
as ideals in $B$.

The fundamental identity forces the equation above to be the factorization of $(p)$, thus $(p)$ is totally ramified in $\mathbb{Q}(\zeta_p)/\mathbb{Q}$.
___

> [!problem] Problem 3
> Keep using the notation from Problem 2.
>
> (1) Show that for every positive integer $i$,
> $$
> B = \mathbb{Z}[\zeta_p] + (1-\zeta_p)^i B.
> $$
> (In words: every $b\in B$ can be written as $b=b'+b''$ with $b'\in\mathbb{Z}[\zeta_p]$ and $b''\in(1-\zeta_p)^i B$.)
>
> (2) Show that there exists a positive integer $m$ such that
> $$
> p^m B \subset \mathbb{Z}[\zeta_p].
> $$
>
> (3) Conclude from (1) and (2) that $B=\mathbb{Z}[\zeta_p]$.

**Proof:**
**(1)** We prove by induction on $i$. Let $\pi = 1 - \zeta_p$.

For $i = 1$: From Problem 2.(2), we know that $(p) = (\pi)^{p-1}$ as ideals of $B$. Consider the natural map $\phi: \mathbb{Z}[\zeta_p] \to B/\pi B$. Since $\mathbb{Z}[\zeta_p]/\pi \mathbb{Z}[\zeta_p] \cong \mathbb{F}_p$ and $B/\pi B \cong \mathbb{F}_p$ (both have dimension $1$ over $F_p$), the map is surjective. Hence $B = \mathbb{Z}[\zeta_p] + \pi B$.

Assume $B = \mathbb{Z}[\zeta_p] + \pi^i B$ for some $i \geq 1$. Take any $b$ in $B$. By induction hypothesis, $b = z + \pi^i b_0$ for some $z \in \mathbb{Z}[\zeta_p]$ and $b_0 \in B$. By the case $i=1$, $b_0 = z_0 + \pi b_1$ for some $z_0$ in $\mathbb{Z}[\zeta_p]$ and $b_1 \in B$. Then $b = z + \pi^i(z_0 + \pi b_1) = (z + \pi^i z_0) + \pi^{i+1} b_1 \in \mathbb{Z}[\zeta_p] + \pi^{i+1} B$. Thus $B = \mathbb{Z}[\zeta_p] + \pi^{i+1} B$. By induction, the statement holds for all positive integers $i$.

**(2)** From class note 4.2 we have $\mathbb{Z}[\zeta_p] \subset B \subset B^* \subset \mathbb{Z}[\zeta_p]^*$. It suffices to find $m$ such that $p^m \mathbb{Z}[\zeta_p]^* \subset \mathbb{Z}[\zeta_p]$.

Take the $\mathbb{Z}$-basis $\{\zeta_p, ..., \zeta_p^{p-1}\}$ of $\mathbb{Z}[\zeta_p]$. Let $f_{j}=(\zeta^{-j}-1)/p,\quad j=1,\dots p-1$. Note that $\operatorname{Tr}(\zeta_{p}^{i}\cdot f_{j})=\delta_{ij}$, so $\{ f_{1,\dots}f_{p-1} \}$ is the dual basis of $\{\zeta_p, ..., \zeta_p^{p-1}\}$. By class note 4.2, it is a basis of $\mathbb{Z}[\zeta_p]^*$.

Therefore, $\mathbb{Z}[\zeta_p]^*=1/p\,\mathbb{Z}[\zeta_{p}]$, which completes the proof.

**(3)** From **(2)**, there exists $m$ such that $p^m B \subset \mathbb{Z}[\zeta_p]$ (we can actually take $m=1$ by the proof of **(2)**). By Problem 2.(2) $p = u \cdot \pi^{p-1}$ for some unit $u \in B$, so we have $p^m = u^m \cdot \pi^{m(p-1)}$, so $\pi^{m(p-1)} B = p^m B\subset \mathbb{Z}[\zeta_p]$. Now apply **(1)** with $i = m(p-1)$, we get $B = \mathbb{Z}[\zeta_p] + \pi^{m(p-1)} B \subset \mathbb{Z}[\zeta_p] + \mathbb{Z}[\zeta_p] = \mathbb{Z}[\zeta_p]$. Since $Z[\zeta_p] \subset B$, we conclude that $B = \mathbb{Z}[\zeta_p]$.
___

>[!problem] Problem 4
>Let $d$ be a square-free number (which is either positive or negative) such that $d\neq 1$ and $d\equiv 1\pmod{4}$. Give a numerical condition for each (rational) prime $p$ to be split, inert, or ramified in $\mathbb{Q}(\sqrt{d})$.

**Proof:**
Let $d=4k+1$, then the integral closure of $\mathbb{Z}$ in $\mathbb{Q}(\sqrt{d})$ is $\mathbb{Z}[\dfrac{1+\sqrt{ d }}{2}]\cong \mathbb{Z}[x] / (x^{2}-x-k)$ by HW1 problem 4. Then 
$$
\mathbb{Z}[x] / (x^{2}-x-k) / (p)\cong\mathbb{F}_{p}[x]/(x^{2}-x-k).
$$
**1.** $p$ is split in $\mathbb{Q}(\sqrt{ d })$ if and only if $x^{2}-x-k$ splits into two distinct factors in $\mathbb{F}_{p}$.

- If $p=2$, then $p$ is split if and only if $2|k$ , i.e. $\dfrac{d-1}{4}$ is even.
- If $p\neq 2$, then write $x^{2}-x-k=(x-\dfrac{1+\sqrt{ d }}{2})(x-\dfrac{1-\sqrt{ d }}{2})$, the discriminant is $d$. Thus $p$ is split if and only if $d$ is a non-zero square in $\mathbb{F}_{p}$ (i.e. the Legendre symbol $\left( \dfrac{d}{p} \right)=1$ and $p\not\mid d$).

**2.** $p$ is ramified in $\mathbb{Q}(\sqrt{ d })$ if and only if $x^{2}-x-k$ splits into two identical factors in $\mathbb{F}_{p}$.

- If $p=2$, then $p$ is never ramified.
- If $p\neq 2$, then write $x^{2}-x-k=(x-\dfrac{1+\sqrt{ d }}{2})(x-\dfrac{1-\sqrt{ d }}{2})$, the discriminant is $d$. Thus $p$ is ramified if and only if $d$ is zero in $\mathbb{F}_{p}$ (i.e. $p|d$).

**3.** $p$ is inert in $\mathbb{Q}(\sqrt{ d })$ if and only if $x^{2}-x-k$ is irreducible in $\mathbb{F}_{p}$.

- If $p=2$, then $p$ is inert if and only if $2\not\mid k$ , i.e. $\dfrac{d-1}{4}$ is odd.
-  If $p\neq 2$, then write $x^{2}-x-k=(x-\dfrac{1+\sqrt{ d }}{2})(x-\dfrac{1-\sqrt{ d }}{2})$. Thus $p$ is inert if and only if $d$ is not a square in $\mathbb{F}_{p}$ (i.e. the Legendre symbol $\left( \dfrac{d}{p} \right)=-1$). 