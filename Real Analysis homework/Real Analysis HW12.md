___

> [!problem] [SHE] 6C.14
> Suppose $U$ is a subspace of a normed vector space $V$. Suppose also that $W$ is a Banach space and $S: U \to W$ is a bounded linear map.
> (a) Prove that there exists a unique continuous function $T: \overline{U} \to W$ such that $\left.T\right|_{U} = S$.
> (b) Prove that the function $T$ in part (a) is a bounded linear map from $\overline{U}$ to $W$ and $\|T\| = \|S\|$.
> (c) Give an example to show that part (a) can fail if the assumption that $W$ is a Banach space is replaced by the assumption that $W$ is a normed vector space.

**Proof:**
**(a)** $S$ is bounded $\Rightarrow$ $S$ is uniformly continuous. For $x \in \overline{U}$, pick $u_n \in U$, $u_n \to x$. Then $\{S(u_n)\}$ is Cauchy in $W$. Since $W$ is complete, define
$$T(x) := \lim_{n\to\infty} S(u_n).$$
The limit is independent of the sequence. $T|_U = S$. Uniform continuity implies $T$ is continuous. Uniqueness follows from density of $U$.

**(b)** For $x,y \in \overline{U}$, $\alpha,\beta \in \mathbb{K}$, pick $u_n\to x$, $v_n\to y$ in $U$. Then
$$T(\alpha x+\beta y) = \lim S(\alpha u_n+\beta v_n) = \alpha T(x)+\beta T(y).$$
For $x \in \overline{U}$, $\|x\|=1$, pick $u_n\to x$:
$$\|T(x)\| = \lim \|S(u_n)\| \le \lim \|S\|\|u_n\| = \|S\|.$$
Thus $\|T\| \le \|S\|$. Since $T$ extends $S$, $\|T\| \ge \|S\|$. Hence $\|T\|=\|S\|$.

**(c)** Let $V = C[0,1]$ with sup norm $\|\cdot\|_\infty$, $U = \mathbb{P}[0,1]$ (real polynomials), and $W = (C[0,1], \|\cdot\|_1)$ with $\|f\|_1 = \int_0^1 |f|$. Define $S: U \to W$ by $S(p) = p$. Then $\|S(p)\|_1 \le \|p\|_\infty$, so $S$ is bounded.  
$\overline{U} = C[0,1]$ (Weierstrass approximation).  

Assume a continuous extension $T: C[0,1] \to W$ exists with $T|_U = S$. Then $T$ would extend the identity map $I: (C[0,1],\|\cdot\|_\infty) \to (C[0,1],\|\cdot\|_1)$ from the dense subspace $U$ to the whole space. But $I$ is not bounded: take $f_n(x)=x^n$; then $\|f_n\|_\infty=1$ while $\|I(f_n)\|_1 = 1/(n+1) \to 0$, which would imply $\|I\|=0$, a contradiction.

Therefore no such continuous $T$ exists. This shows completeness of $W$ is essential.
___

> [!problem] [ATI] 6C.17
>Suppose $U$, $V$, and $W$ are normed vector spaces and $T: U \rightarrow V$ and $S: V \rightarrow W$ are linear. Prove that $\|S \circ T\| \leq \|S\| \|T\|$.

**Proof:**  
For any $u \in U$, we have
$$ \|(S \circ T)(u)\|_W = \|S(T(u))\|_W \le \|S\| \|T(u)\|_V \le \|S\| \|T\| \|u\|_U. $$
Taking the supremum over all $u \in U$ with $\|u\|_U = 1$, we obtain
$$
\|S \circ T\| \le \|S\| \|T\|.
$$
___

> [!problem] [ATI] 6C.18
> Suppose $V$ and $W$ are normed vector spaces and $T: V \to W$ is a linear map. Prove that the following are equivalent:
> (a) $T$ is bounded.
> (b) There exists $f \in V$ such that $T$ is continuous at $f$.
> (c) $T$ is uniformly continuous (which means that for every $\varepsilon > 0$, there exists $\delta > 0$ such that $\|Tf - Tg\| < \varepsilon$ for all $f, g \in V$ with $\|f - g\| < \delta$).
> (d) $T^{-1}(B(0, r))$ is an open subset of $V$ for some $r > 0$.

**Proof:**
**(a)$\Rightarrow$(c).** Suppose $T$ is bounded, i.e., there exists $C\ge0$ such that $\|Tv\|\le C\|v\|$ for all $v\in V$.  
Given $\varepsilon>0$, take $\delta = \varepsilon/(C+1)$ (if $C=0$, any $\delta>0$ works). Then for any $f,g\in V$ with $\|f-g\|<\delta$,  
$$\|Tf-Tg\| = \|T(f-g)\| \le C\|f-g\| < C\delta \le \varepsilon.$$  
Hence $T$ is uniformly continuous.

**(c)$\Rightarrow$(b).** Uniform continuity implies continuity at every point, in particular at any $f_0$.

**(b)$\Rightarrow$(a).** Suppose $T$ is continuous at $f_0$. Then for $\varepsilon=1$, there exists $\delta>0$ such that $\|f-f_0\|<\delta$ implies $\|Tf-Tf_0\|<1$.  
For any $v\in V\setminus\{0\}$, set $h = \frac{\delta}{2\|v\|}v$. Then $\|(f_0+h)-f_0\| = \|h\| = \delta/2 < \delta$, so  
$$\|Th\| = \|T(f_0+h)-Tf_0\| < 1.$$  
But $Th = \frac{\delta}{2\|v\|}Tv$, hence $\frac{\delta}{2\|v\|}\|Tv\| < 1$, i.e., $\|Tv\| < \frac{2}{\delta}\|v\|$. Therefore $T$ is bounded with $\|T\|\le 2/\delta$.

**(a)$\Rightarrow$(d).** Assume $T$ is bounded. Take $r=1$. We show $U:=T^{-1}(B(0,1))$ is open.  
Let $f\in U$, so $\|Tf\|<1$. Let $\eta = 1-\|Tf\|>0$. Choose $\delta = \eta/(\|T\|+1)$.  
If $\|g-f\|<\delta$, then  
$$\|Tg\| \le \|T(g-f)\|+\|Tf\| \le \|T\|\|g-f\|+\|Tf\| < \|T\|\delta + \|Tf\| < \eta + \|Tf\| = 1.$$  
Thus $g\in U$, so $U$ is open.

**(d)$\Rightarrow$(a).** Suppose $U:=T^{-1}(B(0,r))$ is open for some $r>0$. Since $0\in U$, there exists $\delta>0$ such that $B(0,\delta)\subset U$. For any unit $v\in V$, we have $\|\frac{\delta}{2}v\| = \delta/2 < \delta$, so $\frac{\delta}{2}v \in B(0,\delta)\subset U$. Hence $T(\frac{\delta}{2}v) \in B(0,r)$, i.e., $\|T(\frac{\delta}{2}v)\| < r$. Thus $\|Tv\| < \frac{2r}{\delta}$ for all unit vectors $v$, so $T$ is bounded with $\|T\|\le 2r/\delta$.

Therefore (a), (b), (c), (d) are equivalent.
___

> [!problem] [ATI] 6D.5
> Suppose $n \in \mathbf{Z}^{+}$, $V$ is a normed vector space, and $T: \mathbf{F}^{n} \to V$ is a linear map that is one-to-one and onto $V$.
> (a) Show that
> $$\inf\left\{ \|Tx\| : x \in \mathbf{F}^{n} \text{ and } \|x\|_{\infty} = 1 \right\} > 0.$$
> (b) Prove that $T^{-1}: V \to \mathbf{F}^{n}$ is a bounded linear map.

**Proof:**
**(a)** Let $S = \{x \in \mathbf{F}^{n} : \|x\|_{\infty} = 1\}$. $S$ is compact (closed and bounded in a finite‑dimensional space). The map $x \mapsto \|Tx\|$ is continuous (composition of the continuous linear map $T$ and the norm). Therefore it attains its minimum on $S$, i.e., there exists $x_0 \in S$ such that
$$
m := \inf\{\|Tx\| : x \in S\} = \|Tx_0\|.
$$
Since $T$ is injective and $x_0 \neq 0$, we have $Tx_0 \neq 0$, hence $\|Tx_0\| > 0$. Thus $m > 0$.

**(b)** Because $T$ is bijective, $T^{-1}: V \to \mathbf{F}^{n}$ is a well‑defined linear map. For any $v \in V$, write $v = Tx$ with $x = T^{-1}v$. Let $m > 0$ be the constant from part (a). For $x \neq 0$, set $y = x/\|x\|_{\infty} \in S$. Then $\|Ty\| \ge m$, i.e.,
$$
\left\|T\!\left(\frac{x}{\|x\|_{\infty}}\right)\right\| = \frac{\|Tx\|}{\|x\|_{\infty}} \ge m.
$$
Hence $\|x\|_{\infty} \le \frac{1}{m}\|Tx\|$ for all $x \in \mathbf{F}^{n}$. Therefore, for any $v \in V$,
$$
\|T^{-1}v\|_{\infty} = \|x\|_{\infty} \le \frac{1}{m}\|Tx\| = \frac{1}{m}\|v\|,
$$
so $T^{-1}$ is bounded with $\|T^{-1}\| \le 1/m$.
___

> [!problem] [ATI] 6D.7
> Suppose $V$ and $W$ are normed vector spaces and $V$ is finite-dimensional. Prove that every linear map from $V$ to $W$ is continuous.

**Proof:**
Let $\dim V = n$, choose a basis $\{e_1,\dots,e_n\}$ of $V$. Define the maximum norm $\|x\|_{\max} = \max_i |a_i|$ for $x=\sum a_i e_i$.  
All norms on a finite‑dimensional space are equivalent, so $\exists\,c,C>0$ with
$$
c\|x\|_V \le \|x\|_{\max} \le C\|x\|_V \qquad\forall x\in V. \tag{1}
$$
For any $x=\sum a_i e_i$,
$$
\|Tx\|_W \le \sum_{i=1}^n |a_i|\,\|Te_i\|_W
\le \Bigl(\sum_{i=1}^n \|Te_i\|_W\Bigr) \|x\|_{\max}. \tag{2}
$$
Let $M = \sum_{i=1}^n \|Te_i\|_W$. From (1) and (2),
$$
\|Tx\|_W \le M \|x\|_{\max} \le MC \|x\|_V.
$$
Thus $T$ is bounded, hence continuous.
___

