___
*Using DeepSeek to help write markdown problem statements, provided ideas for problem 2 and 3, and enhance writing conventions.*
___

> [!problem] Problem 1
> Elaborate on the proof of [S], I.3, Proposition 5 on p.11; in particular, check that
> $$
>(\mathfrak{a}\cdot\mathfrak{b})_{\mathfrak{p}}=\mathfrak{a}_{\mathfrak{p}}\cdot\mathfrak{b}_{\mathfrak{p}},\qquad(\mathfrak{a}:\mathfrak{b})_{\mathfrak{p}}=(\mathfrak{a}_{\mathfrak{p}}:\mathfrak{b}_{\mathfrak{p}}),
>$$
> and explain how “The proposition follows from this by localisation.” (We admit that the proof when $A$ is a DVR is understood; no need to provide any details on this case. Also, you need not check that
> $$
>(\mathfrak{a}+\mathfrak{b})_{\mathfrak{p}}=\mathfrak{a}_{\mathfrak{p}}+\mathfrak{b}_{\mathfrak{p}},
>$$
> as this is basically the same deal.) $^1$
> 
> The following two problems are taken from exercises in Chapter 9 of [AM].

**Proof:**
Let $A$ be a DVR, $\mathfrak{p} \subset A$ a prime ideal, and $\mathfrak{a}, \mathfrak{b} \subset A$ two ideals. We verify the two identities. 

**1. $(\mathfrak{a} \cdot \mathfrak{b})_{\mathfrak{p}} = \mathfrak{a}_{\mathfrak{p}} \cdot \mathfrak{b}_{\mathfrak{p}}$**

$(\subseteq)$: Take $\dfrac{\sum a_i b_i}{s} \in (\mathfrak{a} \cdot \mathfrak{b})_{\mathfrak{p}}$ with $a_i \in \mathfrak{a}$, $b_i \in \mathfrak{b}$, $s \notin \mathfrak{p}$. Write it as $\sum \dfrac{a_i}{1} \cdot \dfrac{b_i}{s} \in \mathfrak{a}_{\mathfrak{p}} \cdot \mathfrak{b}_{\mathfrak{p}}$.

$(\supseteq)$: Take a generator $\dfrac{a}{s} \cdot \dfrac{b}{t} \in \mathfrak{a}_{\mathfrak{p}} \cdot \mathfrak{b}_{\mathfrak{p}}$. Then $\dfrac{a}{s} \cdot \dfrac{b}{t} = \dfrac{ab}{st}$ with $ab \in \mathfrak{a} \cdot \mathfrak{b}$ and $st \notin \mathfrak{p}$, so it lies in $(\mathfrak{a} \cdot \mathfrak{b})_{\mathfrak{p}}$. Finite sums follow similarly.

Thus equality holds.

**2. $(\mathfrak{a} : \mathfrak{b})_{\mathfrak{p}} = (\mathfrak{a}_{\mathfrak{p}} : \mathfrak{b}_{\mathfrak{p}})$**

$(\subseteq)$: Take $\dfrac{x}{s} \in (\mathfrak{a} : \mathfrak{b})_{\mathfrak{p}}$ with $x \in (\mathfrak{a} : \mathfrak{b})$, $s \notin \mathfrak{p}$. For any $\dfrac{b}{t} \in \mathfrak{b}_{\mathfrak{p}}$, we have $\dfrac{x}{s} \cdot \dfrac{b}{t} = \dfrac{xb}{st}$. Since $xb \in \mathfrak{a}$, $st\not\in \mathfrak{p}$, we have $\dfrac{xb}{st}$ lies in $\mathfrak{a}_{\mathfrak{p}}$, hence $\dfrac{x}{s} \in (\mathfrak{a}_{\mathfrak{p}} : \mathfrak{b}_{\mathfrak{p}})$.

$(\supseteq)$: Take $\dfrac{x}{s} \in (\mathfrak{a}_{\mathfrak{p}} : \mathfrak{b}_{\mathfrak{p}})$. For each $b \in \mathfrak{b}$, consider $\dfrac{x}{s} \cdot \dfrac{b}{1} = \dfrac{xb}{s} \in \mathfrak{a}_{\mathfrak{p}}$, so there exists $u_b \notin \mathfrak{p}$ with $u_b x b \in \mathfrak{a}$. Since $\mathfrak{b}$ is finitely generated (as $A$ is a DVR, DVRs are Noetherian, and every ideal of a Noetherian ring is finitely generated), take generators $b_1,\dots,b_n$ and let $t = u_{b_1}\cdots u_{b_n} \notin \mathfrak{p}$. Then $t x b_i \in \mathfrak{a}$ for all $i$, so $t x \mathfrak{b} \subseteq \mathfrak{a}$, i.e., $t x \in (\mathfrak{a} : \mathfrak{b})$. Hence $\dfrac{x}{s} = \dfrac{t x}{t s} \in (\mathfrak{a} : \mathfrak{b})_{\mathfrak{p}}$.

Thus equality holds.

**3. Why "The proposition follows from this by localisation"**

In a Dedekind domain, localising at any prime ideal gives a DVR. It is known that every nonzero fractional ideal of a DVR is invertible. The three identities verified above show that the operations of product, sum, and ideal of quotient commute with localisation. Consequently, a fractional ideal is invertible globally iff it is invertible at every localisation.

Therefore, for any nonzero fractional ideal of a Dedekind domain, localising at each prime yields an invertible ideal in the corresponding DVR, and by the local-global principle, the original ideal must be invertible.
___

> [!problem] Problem 2
> Let $A$ be a Dedekind domain, $S$ a multiplicatively closed subset such that $S^{-1}A$ is not a field.
> (i) Show that $S^{-1}A$ is a Dedekind domain.
> (ii) Show that the extension of ideals (and similarly for fractional ideals) induces a surjection from the ideal class group of $A$ to that of $S^{-1}A$.

**Proof:**
**(i)** A Dedekind domain is Noetherian, integrally closed, and of Krull dimension $\le 1$. Since $A$ is Noetherian, $S^{-1}A$ is Noetherian.

Since $A$ is integrally closed in its fraction field $K$, any element $x\in K$ integral over $S^{-1}A$ is also integral over $A$, hence $x\in A\subset S^{-1}A$; thus $S^{-1}A$ is integrally closed.

Prime ideals of $S^{-1}A$ correspond bijectively to primes $\mathfrak{p}\subset A$ with $\mathfrak{p}\cap S=\varnothing$ (followed from [AM] 3.13). As $A$ is Dedekind, every nonzero such $\mathfrak{p}$ is maximal, so its image in $S^{-1}A$ is also maximal. Hence $\dim S^{-1}A\le 1$. Since $S^{-1}A$ is not a field, it has a nonzero prime ideal, so $\dim S^{-1}A=1$.

Therefore $S^{-1}A$ is a Dedekind domain.

**(ii)** Let $\varphi:I(A)\to I(S^{-1}A)$ be the extension map $\mathfrak{a}\mapsto S^{-1}\mathfrak{a}$. This sends principal ideals to principal ideals, hence induces a homomorphism $\overline{\varphi}:\operatorname{Cl}(A)\to\operatorname{Cl}(S^{-1}A)$.

To show surjectivity, take any fractional ideal $\mathfrak{b}\subset S^{-1}A$. Its contraction $\mathfrak{a}=\mathfrak{b}\cap A$ is a fractional ideal of $A$, and by standard localization theory we have $\mathfrak{b}=S^{-1}\mathfrak{a}$. Thus every fractional ideal of $S^{-1}A$ is extended from $A$, so $\varphi$ is surjective on fractional ideals. Consequently $\overline{\varphi}$ is surjective on class groups.
___

> [!problem] Problem 3
> Let $A$ be a Dedekind domain. Consider a nonzero ideal $\mathfrak{a}$ in $A$. Show that every ideal in the quotient ring $A/\mathfrak{a}$ is principal. Deduce that every ideal of $A$ is generated by at most two elements.

**Proof:**
Since $A$ is a Dedekind domain, every nonzero ideal factors uniquely into a product of prime ideals. Write $\mathfrak{a} = \mathfrak{p}_1^{e_1}\cdots\mathfrak{p}_n^{e_n}$ with distinct primes $\mathfrak{p}_i$ ([AM] 9.4).

Consider the natural projection $\pi: A \to A/\mathfrak{a}$. Any ideal of $A/\mathfrak{a}$ is of the form $\mathfrak{b}/\mathfrak{a}$ for some ideal $\mathfrak{b}$ of $A$ with $\mathfrak{a}\subseteq\mathfrak{b}$. Since $A$ is Dedekind, we can write $\mathfrak{b} = \mathfrak{p}_1^{f_1}\cdots\mathfrak{p}_n^{f_n}\cdot\mathfrak{c}$ where $0\leq f_i\leq e_i$ and $\mathfrak{c}$ is coprime to each $\mathfrak{p}_i$ (i.e., $\mathfrak{c}+\mathfrak{p}_i=A$ for all $i$). By the Chinese remainder theorem,
$$A/\mathfrak{a} \cong \prod_{i=1}^n A/\mathfrak{p}_i^{e_i}.$$
Under this isomorphism, $\mathfrak{b}/\mathfrak{a}$ corresponds to $\prod_{i=1}^n \mathfrak{p}_i^{f_i}/\mathfrak{p}_i^{e_i}$.

Now fix a prime power $\mathfrak{p}^e$. Choose an element $x\in\mathfrak{p}^{e-1}\setminus\mathfrak{p}^e$ (such an element exists because $\mathfrak{p}^{e-1}\supsetneq\mathfrak{p}^e$). Then the image of $x$ generates the unique maximal ideal $\mathfrak{p}/\mathfrak{p}^e$ of $A/\mathfrak{p}^e$. Since $A/\mathfrak{p}^e$ is a local Artinian ring with principal maximal ideal, every ideal of $A/\mathfrak{p}^e$ is a power of this maximal ideal, hence principal ([AM] 8.8).

Returning to the product decomposition, each factor $A/\mathfrak{p}_i^{e_i}$ has only principal ideals, so their product $A/\mathfrak{a}$ also has only principal ideals.

**Every ideal of $A$ is generated by at most two elements:**

Let $\mathfrak{b}\subseteq A$ be any nonzero ideal. Pick any nonzero $a\in\mathfrak{b}$. Consider the quotient map $\pi: A\to A/(a)$. The image $\pi(\mathfrak{b}) = \mathfrak{b}/(a)$ is an ideal of $A/(a)$. By the argument above, $A/(a)$ is a principal ideal ring, so $\mathfrak{b}/(a)$ is generated by a single element, say the class of $b\in A$. That is,
$$\mathfrak{b}/(a) = (b + (a)).$$
Lifting back to $A$, we obtain
$$\mathfrak{b} = (a,b).$$
Thus $\mathfrak{b}$ is generated by the two elements $a$ and $b$.

>[!remark] Remark
>The conclusion is the next best thing as not every ideal of a DD is generated by one element in general, e.g., $A = \mathbb{Z}[\sqrt{-5}]$.

___

> [!problem] Problem 4
> Let $d\neq 1$ be a square free integer (which is either positive or negative). Determine the integral closure of $\mathbb{Z}$ (a.k.a. the ring of integers) in $\mathbb{Q}(\sqrt{d})$; for example, give an explicit $\mathbb{Z}$-basis for the integral closure.$^2$

**Proof:**
Take any $\alpha \in \mathcal{O}_{\mathbb{Q}(\sqrt{ d })}$, write $\alpha=a+b\sqrt{d}\in K$ with $a,b\in\mathbb{Q}$. Let $\overline{ \alpha }=a-b\sqrt{ d }$, then $\overline{ \alpha }$ also suffices the minimal polynomial of $\alpha$ (taking conjugation commutes with polynomial). Thus $\alpha+\overline{ \alpha }=2a\in\mathbb{Z}$ and $\alpha \cdot \overline{ \alpha }=a^2-db^2\in\mathbb{Z}$.

If $a\in \mathbb{Z}$, then $b^{2}\in \mathbb{Z}$, thus $b\in \mathbb{Z}$. If $a\not\in \mathbb{Z}$, then $m=2a$ and $n=2b$ are integers, so $m^2\equiv dn^2\pmod 4$.

Now consider cases:

- If $d\equiv 2,3\pmod 4$, then $m^2\equiv dn^2\pmod 4$ forces $m$ and $n$ both even. Hence $a,b\in\mathbb{Z}$, so $\alpha\in\mathbb{Z}[\sqrt{d}]$. Conversely, any element of $\mathbb{Z}[\sqrt{d}]$ is clearly integral. Thus $\mathcal{O}_K=\mathbb{Z}[\sqrt{d}]$ with basis $\{1,\sqrt{d}\}$.

- If $d\equiv 1\pmod 4$, then $m^2\equiv dn^2\pmod 4$ allows $m,n$ both odd. Hence $a,b\in\frac{1}{2}\mathbb{Z}$, and $\alpha=(m+n\sqrt{d})/2$. Writing $m-n=2t$, we have $\alpha=t+n\cdot(1+\sqrt{d})/2$, so $\alpha\in\mathbb{Z}[(1+\sqrt{d})/2]$. Conversely, $(1+\sqrt{d})/2$ has minimal polynomial $x^2-x+(1-d)/4\in\mathbb{Z}[x]$, so it is integral. Thus $\mathcal{O}_K=\mathbb{Z}[(1+\sqrt{d})/2]$ with basis $\{1,(1+\sqrt{d})/2\}$.
