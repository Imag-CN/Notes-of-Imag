>[!problem] Problem 1
On a metric space $(X,d)$, if $x_n \to x_0$ as $n \to +\infty$. Prove that for any $\epsilon > 0$, $B(x_0,\epsilon)$ contains all but finitely many $x_n$ for $n \in \mathbb{N}^+$.

$x_n \to x_0,n \to +\infty\Rightarrow \forall \epsilon>0, \exists N \in \mathbb{N}^+,s.t.\forall n>N,d(x_0,x_n)<\epsilon,i.e.x_n\in B(x_0,\epsilon).$
Therefore, there are at most $N$ $x_n$ not in $x_n\in B(x_0,\epsilon)$.
___
>[!problem] Problem 2
Construct a compact set of real numbers whose limit points form a countable set.

Let $A=\{2^{-n}+2^{-m}:n,m\in\mathbb{N}^+,m> n\}\cup\{2^{-n}:n,\in\mathbb{N}^+\}\cup\{0\}.$
$A\subseteq (0,1)$, thus $A$ is bounded.
$A'=\{2^{-n}:n,\in\mathbb{N}^+\}\cup\{0\}\subseteq A$, thus $A$ is closed, and $A'$ is countable.
$A$ is closed and bounded, so $A$ is compact.
___
>[!problem] Problem 3
Give an example of an open cover of the segment $(0,1)$ which has no finite subcover.

$$\bigcup_{k\in\mathbb{N},k\geq2}(0,1-k^{-1})$$
---
>[!problem] Problem 4
Prove that: if $\{K_\alpha\}$ is any collection of compact set such that any finite subcollection has non-empty intersection, then $\bigcap_\alpha K_\alpha \neq \varnothing.$

Suppose $(X,\tau)$ is the topology space concerned.
Assume, for the sake of contradictory, that $\bigcap_\alpha K_\alpha = \varnothing$.
Let $K_{\alpha_0}$ be an arbitrary set in $\bigcap_\alpha K_\alpha$, $K_{\alpha_0}$ is non-empty.
Then $K_{\alpha_0}\subseteq (\bigcap_{\alpha\neq\alpha_0} K_\alpha)^c=\bigcup_{\alpha\neq\alpha_0}(K_{\alpha})^{c}$.
$K_{\alpha}$ is compact, then closed, so $(K_{\alpha})^c$ is open.
So $\bigcup_{\alpha\neq\alpha_0}(K_{\alpha})^{c}$ is an open cover of $K_{\alpha_0}$.
$K_{\alpha_0}$ is compact, so $\bigcup_{\alpha\neq\alpha_0}(K_{\alpha})^{c}$ has a subcover $\bigcup_{\alpha\in F}(K_{\alpha})^{c}$, where $F$ is a finite set.
$K_{\alpha_0}\subseteq \bigcup_{\alpha\in F}(K_{\alpha})^{c} \Rightarrow K_{\alpha_0}\subseteq (\bigcap_{\alpha\in F} K_\alpha)^c\Rightarrow K_{\alpha_0}\cap\bigcap_{\alpha\in F} K_\alpha=\varnothing$, which is a contradiction.
Therefore, we conclude that $\bigcap_\alpha K_\alpha \neq \varnothing$.
>[!tip] 
Here we use the fact that any compact sets are closed in metric space, which is not right in general topology space. In fact, this proposition holds in topology space where compact sets are closed (KC-space), but has counterexample in general topology space.
Let $X=\mathbb{Z}_{\geq 0}$, and the topology are those subspaces whose complement are finite sets (cofinite topology). All sets in $X$ is compact. Let $K_n=\mathbb{Z}_{\geq k},k\in\mathbb{Z}_{\geq 0}$. Then any finite subcollection of $\{K_n\}$ has non-empty intersection (the intersection equals to the set with the highest index). However, $\bigcup_{n\in\mathbb{Z}_{\geq 0}}K_n=\varnothing$.

___
>[!problem] Problem 5
Let $X$ be the set of real valued continuous functions on $[0,1]$. For any pair of points $f,g\in X$, we define
$$ d(f,g)=\left(\int_{0}^{1}\left(f(x)-g(x)\right)^{2}\,dx\right)^{1/2}. $$
Prove
(a) $(X,d)$ is a metric space.
(b) there is an isometric embedding $\mathbb{R}\to X$.

#### (a)
- $\left(f(x)-g(x)\right)^{2}\geq0\Rightarrow \int_{0}^{1}\left(f(x)-g(x)\right)^{2}\,dx\geq0\Rightarrow d(f,g)\geq 0$
	If $f(x)-g(x)\neq 0$ for some $x\in[0,1]$, then there's an interval in $[0,1]$ where $(f(x)-g(x))^2>\epsilon$ for some positive $\epsilon$ all the time, because $f(x)-g(x)$ is continuous.
	So $d(f,g)=0\iff f=g$.
- $d(f,g)=d(g,f)$.
- Denote $(f|g)=\int_{0}^{1}f(x)\cdot g(x)\,dx,|f|=\sqrt{(f|f)}$.
	We know that $(X,(\cdot|\cdot))$ is an inner product space.
	Cauchy inequality implies $|f|\cdot|g|\geq (f|g)$, so we have
$$\begin{align}
|f|^2+2\cdot|f|\cdot|g|+|g|^2&\geq (f|f)+2(f|g)+(g|g)\\
(|f+|g|)^2&\geq(f+g|f+g)\\
|f|+|g|&\geq|f+g|
\end{align}$$
	Substitute $f$ with $f-g$, $g$ with $g-h$ yields $|f-g|+|g-h|\geq|f-h|,i.e.$ $$d(f,g)+d(g,h)\geq d(f,h).$$
#### (b)
Denote $f_t(x)=t,x\in[0,1]$, where $f_t(x)\in X$ and $t\in\mathbb{R}$.
Then
$$F:\mathbb{R}\rightarrow X,F(t)=f_t$$
is an isometric embedding.
___
>[!problem] Problem 6
Let $\mathcal{C}$ be the set of all continuous functions on $\mathbb{R}$. Construct any metric on $\mathcal{C}$ such that there exists an isometric embedding from $\mathbb{R}$ to $\mathcal{C}$.

Let $A$ be the collection of all constant functions.
Denote $f_t(x)=t$, where $f_t(x)\in A\subseteq\mathcal{C}$ and $t\in\mathbb{R}$.
Let$$d(f,g)=
\begin{cases}
&0&\text{if }f=g\\
&|f-g|&\text{if }f,g\in A\\
&|f|+1&\text{if }f\in A,g\notin A\\ 
&|g|+1&\text{if }g\in A,f\notin A\\ 
&1&\text{if }f,g\notin A, f\neq g\\
\end{cases}$$
Then $d(f,g)$ is a metric on $\mathcal{C}$, and
$$F:\mathbb{R}\rightarrow\mathcal{C},F(t)=f_t$$
is an isometric embedding from $\mathbb{R}$ to $\mathcal{C}$.
___

>[!problem] Problem 7
Let $\mathbb{Z}$ and $\mathbb{Z}^{2}$ are equipped with the standard Euclidean metric.
(a) Prove there exists a Lipschitz bijection $\Phi:\mathbb{Z}\to \mathbb{Z}^{2}$.
(b) Prove there exists no Lipschitz injection $\Psi:\mathbb{Z}^{2}\to \mathbb{Z}$.

Denote $(0,0)$ ad $O$, metric in $\mathbb{Z}$ as $d_1$, and metric in $\mathbb{Z}^2$ as $d_2$,
#### (a)
Construct $\Phi:\mathbb{Z}\rightarrow\mathbb{Z}^2$ as the following graph:
![[Pasted image 20251008154652.png]]
The polygonal line (denoted as $L$ ) extending in both directions passes through all lattice points without repetition; therefore, $\Phi$ is a bijection from $\mathbb{Z}$ to $\mathbb{Z}^2$.​
For all $A,B\in\mathbb{Z}^2$, $d_1(\Phi(A),\Phi(B))$ represents the shortest-path length from $A$ to $B$ along $L$, and $d_2(A,B)$ is the shortest-path length from $A$ to $B$ on $\mathbb{R}^2$ plane, so  we have$$d_1(\Phi(A),\Phi(B))\geq d_2(A,B).$$
In conclusion, $\Phi$ is an $1$-Lipschitz bijection.
#### (b)
Assume $\Psi:\mathbb{Z}^{2}\to \mathbb{Z}$ is an $C$-Lipschitz bijection, denote $\Psi(O)$ as $m$.
Let $N=\lceil C\rceil$, and let $\mathcal{A}=\{(a_1,a_2)\in\mathbb{Z}^2:|a_1|\leq N,|a_2|\leq N\}$.
$\forall A\in\mathcal{A},d_2(O,A)\leq\sqrt{2}N<2N$, so $d_1(m,\Psi(A))\leq C\cdot d_2(O,A)<2N^2$.
Let $\mathcal{B}=\{b\in\mathbb{Z}:|m-b|\leq 2N^2\}$, then $\Psi(\mathcal{A})\subseteq \mathcal{B}$.
Since $\#\mathcal{A}=(2N+1)^2,\#\mathcal{B}=4N^2+1$, we have $\#\mathcal{A}>\#\mathcal{B}\geq\#\Psi(\mathcal{A})$.
$\#\mathcal{A}>\#\Psi(\mathcal{A})$ contradicts to the assumption that $\Psi$ is a bijection, thus there exists no Lipschitz injection $\Psi:\mathbb{Z}^{2}\to \mathbb{Z}$.
___
>[!problem] Problem 8
Given a function $f:\mathbb{R}\to \mathbb{R}$, the graph $\mathcal{G}(f)$ is defined as $\mathcal{G}(f)=\{(x,f(x)):x\in \mathbb{R}\}\subseteq \mathbb{R}^{2}$. Endowed with the Euclidean metric of $\mathbb{R}^{2}$, $\mathcal{G}(f)$ is hence a metric space.
(a) Show the projection (onto the $x$-axis) map $p:\mathcal{G}(f)\to \mathbb{R}$ is 1-Lipschitz.
(b) Suppose $f$ is $C^{1}$-smooth and $f'(x)$ is uniformly bounded. Show the projection map is bi-Lipschitz.
(c) Prove the graph of sine function is bi-Lipschitz equivalent to $\mathbb{R}$.
#### (a)
Denote projection (onto the $y$-axis) map as $p_y:\mathcal{G}(f)\to \mathbb{R}$.
$\forall G_1,G_2 \in \mathcal{G}(f), d(G_1,G_2)=\sqrt{(d(p(G_1),p(G_2))^2+d(p_y (G_1),p_y (G_2))^2)}\geq d(p(G_1),p(G_2)$
Hence $p$ is 1-Lipschitz.
#### (b)
It's trivial that $p$ is bijection, and we have already proven that $p$ is Lipschitz, so we only have to prove that $p^{-1}$ is Lipschitz.
Suppose $|f'(x)|\leq M$ since $f'(x)$ is uniformly bounded.
$f$ is $C^{1}$-smooth $\Rightarrow f(x)-f(y)=\int_{y}^{x}f'(t)\,dt,\forall x,y\in\mathbb{R},x>y$.
$\Rightarrow |f(x)-f(y)|\leq\int_{y}^{x}|f'(t)|\,dt\leq M|x-y|\Rightarrow \sqrt{(|f(x)-f(y)|)^2+|x-y|^2}\leq\sqrt{1+M^2}|x-y|$.
Therefore, $p^{-1}$ is $(1+M^2)^{-1\2}$-Lipschitz, and $p$ is $\sqrt{1+M^2}$-bi-Lipschitz.
#### (c)
$\sin$ is $C^{1}$-smooth and $\sin'(x)=\cos{x}\in[-1,1]$, so the projection map is bi-Lipschitz.
Also the projection map is bijection, so the graph of sine function is bi-Lipschitz equivalent to $\mathbb{R}$.
___
>[!problem] Problem 9
Let $\mathcal{K}$ be the set of all non-empty compact subsets in $R^{n}$ where $R^{n}$ is with the standard Euclidean metric $d$. Given elements $K_{1},K_{2}\in\mathcal{K}$, we define the "Hausdorff distance" $d_{\mathcal{K}}$ to be
$$d_{\mathcal{K}}(K_{1},K_{2}):=\operatorname*{max}\{\operatorname*{sup}_{x\in K_{1}}d(x,K_{2}),\operatorname*{sup}_{y\in K_{2}}d(y,K_{1})\}.$$
(a) Draw a picture in $R^{2}$, find the Hausdorff distance between $K_{1},K_{2}$, where $K_{1}$ is a circle of radius 1 centered at the origin, and $K_{2}$ is a square whose vertices are $(0,0),(0,2),(2,0),(2,2)$.
(b) Prove $(\mathcal{K},d_{\mathcal{K}})$ is a metric space.
(c) Prove $(\mathcal{K},d_{\mathcal{K}})$ is complete.
(d) Prove the diameter function is continuous on $(\mathcal{K},d_{\mathcal{K}})$.
#### (a)
![[Pasted image 20251008231937.png]]
As shown in the picture, $\sup_{x\in K_{1}}d(x,K_{2})=2\sqrt{2}-1,\sup_{y\in K_{2}}d(y,K_{1})=1$.
So $d_{\mathcal{K}}(K_{1},K_{2})=2\sqrt{2}-1$.
#### (b)
$d_{\mathcal{K}}(K_1,K_2)\geq0,K_1=K_2\Rightarrow d_{\mathcal{K}}(K_1,K_2)=0$.

$d_{\mathcal{K}}(K_1,K_2)=0\Rightarrow \operatorname*{sup}_{x\in K_{1}}d(x,K_{2})=\operatorname*{sup}_{y\in K_{2}}d(y,K_{1})=0$
$\Rightarrow d(x,K_{2})=d(y,K_{1})=0,\forall x\in K_{1},\forall y\in K_{2}$.
$K_1$ is compact, so $d(y,K_{1})$ attains its minimum value of $0$ at some point on $K_1$, $i.e.y\in K_1\Rightarrow K_2\subseteq K_1$.
Similarly we have $K_1\subseteq K_2$, so $K_1=K_2$.

$d_{\mathcal{K}}(K_1,K_2)=d_{\mathcal{K}}(K_2,K_1)$.


Now we prove triangle inequality:
Let $\delta_{12} = d_{\mathcal{K}}(K_1, K_2)$, $\delta_{23} = d_{\mathcal{K}}(K_2, K_3)$.
For any $x \in K_1$:$$(x, K_3) \le d(x, K_2) + \sup_{y \in K_2} d(y, K_3) \le \delta_{12} + \delta_{23}.$$
   So $\sup_{x \in K_1} d(x, K_3) \le \delta_{12} + \delta_{23}$.
   Similarly, $\sup_{z \in K_3} d(z, K_1) \le \delta_{12} + \delta_{23}$, thus:$$   d_{\mathcal{K}}(K_1, K_3) \le \delta_{12} + \delta_{23}.$$Therefore, $d_{\mathcal{K}}$ is a metric on $\mathcal{K}$.
#### (c)
Let $\{K_m\}$ be a Cauchy sequence in $(\mathcal{K}, d_{\mathcal{K}})$. Define the limit set:
$$
K = \{ x \in \mathbb{R}^n : \exists x_{m_k} \in K_{m_k},x_{m_k} \to x \}.
$$
We shall prove $K\in\mathcal{K}$ and  in $d_{\mathcal{K}}$.

First we prove $K$ is non-empty：
Since $\{K_m\}$ is Cauchy, there exists $N$ such that for $m, n \ge N$, $d_{\mathcal{K}}(K_m, K_n) < 1$. Then all $K_m$ ($m \ge N$) are contained in the $1$-neighborhood of $K_N$, which is bounded, thus $\{K_m\}$ are uniformly bounded.
Pick any $x_m \in K_m$; this sequence is bounded and has a convergent subsequence, whose limit lies in $K$, so $K \neq \emptyset$.

Then we prove is compact by indicating it's closed and bounded:
- $K$ is closed: if $y_j \in K$ and $y_j \to y$, then each $y_j$ is limit of points in $K_m$, so by diagonal argument, $y$ is also such a limit.
- $K$ is bounded: $\{K_m\}$ are uniformly bounded, so $K$ is contained in a slight enlargement of a bounded set containing all $K_m$.

Finally, we prove $K_m \to K$ in $d_{\mathcal{K}}$:
$\forall\varepsilon > 0,\exists N \, s.t. \forall p, q \ge N$, $d_{\mathcal{K}}(K_p, K_q) < \varepsilon/2$.
For $m \ge N$:
For any $x \in K_m$, we can construct a sequence $x = x_m, x_{m+1}, \dots$ with $x_n \in K_n$ and $d(x_n, x_{n+1}) < \varepsilon/2^n$ (by the definition of $d_{\mathcal{K}}$).
This Cauchy sequence converges to some $y \in K$ with $d(x, y) \le \varepsilon$, so $\sup_{x \in K_m} d(x, K) \le \varepsilon$.
For any $y \in K$, there is a sequence $y_n \in K_n$ with $y_n \to y$.
For large $m$, $d(y_n, K_m)$ is small, and taking limits gives $d(y, K_m) \le \varepsilon$, so $\sup_{y \in K} d(y, K_m) \le \varepsilon$.
Thus $d_{\mathcal{K}}(K_m, K) \le \varepsilon$ for $m \ge N$. Hence $K_m \to K$.