___

>[!example] An interesting non-noetherian ring
>Let
>$$
>R^{*}= \Pi_{k=1}^{\infty}\mathbb{F}_{2},
>$$
>$$
>R_{0}=\{ r\in R^{*}:\text{all but finitely many entries of R is }0 \} \subset R^{*},
>$$
>$$
>R_{1}=1+R_{0}=\{ r\in R^{*}:\text{all but finitely many entries of R is }1 \} \subset R^{*},
>$$
>$$
>R=R_{0}\sqcup R_{1} \subset R^{*}.
>$$
>Note that $R$ is 'genuine' subring of $R^{*}$, $R_{0}$ is a 'subring' without identity, and $R_{1}$ is not a ring.
>
>Every element in $R$ can be uniquely written as $\delta+r$ where $\delta=0\text{ or }1$ and $r\in R$.

We first determine some notations:
Denote $r[n]$ as the $n$-th entry of $r$, $n \in \mathbb{Z}^{+}$, $r\in R^{*}$. Denote $e_{n}$ as the element where $n$-th entry is $1$, and all other entries are $0$. Denote $E_{n}=\{ r\in R_{0}:r[n]=0 \}$, and its complement in $R_{0}$ as $F_{n}=R\setminus E_{n}=\{ r\in R_{0}:r[n]=1 \}$.

And we list some basic properties:
$R^{*}$ is a boolean ring, who has properties that $r+r=0$ and $r^{2}=r$, $\forall r\in R^{*}$. These properties are inherited by $R$. Suppose $\mathfrak{p}\in \operatorname{Spec}R$. For any $r\in R_{0}$, $r(1+r)=0\in \mathfrak{p}$ and $1=r+(1+r)\not\in \mathfrak{p}$, thus one and only one of $r$ and $1+r$ is in $\mathfrak{p}$. Thus $\mathfrak{p}$ is maximal, and $R\setminus\mathfrak{p}=1+\mathfrak{p}$.
___

>[!problem] Injectivity is not a local property for $R$
>$R$ as an $R$-module is not injective, but any of its localization is injective.

**Proof:**
Take $\mathfrak{m}$ as an maximal ideal. Take $\dfrac{r}{m} \in R_{\mathfrak{m}}$, where $r\in R, m \in \mathfrak{m}$.

If $r \in \mathfrak{m}$, then $(1+r)r=0$ and $1+r \in R\setminus \mathfrak{m}$, thus $\dfrac{r}{m} = \dfrac{0}{1}$. If $r \in R\setminus \mathfrak{m}$, then $(1+r-m)(r-m)=0$, thus $\dfrac{r}{m}= \dfrac{1}{1}$. And since $0 \not\in R\setminus \mathfrak{m}$, $\dfrac{0}{1} \neq \dfrac{1}{1}$. Therefore, $R_{\mathfrak{m}}\cong \mathbb{F}_{2}$ is a field. So $R_{\mathfrak{m}}$ is injective as an $R_{\mathfrak{m}}$-module (it is easy to show that any module over a field is injective because it becomes a vector space).

Assume for contradiction that $R$ is injective. Since $R$ is a subring and $R$-submodule of $R^{*}$, the identity map on $R$ can be extended to be an $R$-homomorphism from $R^{*}$ to $R$. Equivalently, there exists an $R$-homomorphism $f:R^{*}\to R$ such that $f \mid_{R}=\operatorname{id}_{R}$.

Take $x \in R^{*}\setminus R$, then $1+x\in R^{*}/R$. Since $f(1+x)=1+f(x)$, one and only one of $x$ and $1+x$ is in $R_{0}$. W.L.O.G. suppose $f(x) \in R_{0}$. Since $x$ has infinitely many entries equal to $1$, $f(x)$ has only finitely many entries equal to $1$, by the pigeonhole principle, there exist some $k\in Z^{+}$ such that $x[k]=1$ and $f(x)[k]=0$. Then on one hand $f(e_{k})f(x)=f(e_{k}\cdot x)=f(e_{k})=e_{k}$, but on the other hand $f(e_{k})f(x)=e_{k}f(x)=0$, thus contradiction.
___

>[!problem] No primary decomposition for the zero ideal.
>The zero ideal of $R$ has no primary decomposition.

**Proof:**
To show this, we study the structure of prime ideals.

Since $r=r^{2}$ for any $r \in R$, any primary ideal is actually a prime ideal. So it is sufficient to show that $(0)$ cannot be written as the finite intersection of some prime ideals.

Take any $\mathfrak{p}\in \operatorname{Spec} R$. We have already shown that for any $r\in R_{0}$, one and only one of $r$ and $1+r$ is in $\mathfrak{p}$.

If $r \in \mathfrak{p}$ for any $r \in R_{0}$, then obviously $\mathfrak{p}=R_{0}$.

If $1+r\in\mathfrak{p}$ for some $r \in R_{0}$, then choose such an $r$ with fewest entries equal to $1$. Since $r\neq 0$, there exists some $k\in \mathbb{Z}^{+}$ such that $r[k]=1$. Assume that $r\neq e_{k}$. Since $r$ was chosen to have the fewest entries equal to $1$, $1+e_{k}$ is not in $\mathfrak{p}$. So $e_{k}$ is in $\mathfrak{p}$, then $1+(r-e_{k})$ is in $\mathfrak{p}$. But $1+(r-e_{k})$ has fewer entries equal to $1$ compared to $1+r$, thus contradiction. Therefore, $1+e_{k}\in \mathfrak{p}$, and then it is easy to check $\mathfrak{p}=(1+E_{k})\sqcup F_{k}$.

Denote $\mathfrak{p}_{0}=R_{0}$ and $\mathfrak{p}_{k}=(1+E_{k})\cup F_{k}$. Assume $(0)$ can be written as the finite intersection of some prime ideals, W.O.L.G we can assume $(0)=\cap_{k=0}^{m}\mathfrak{p}_{k}$. Then $(0)\supset \cap_{k=1}^{m}F_{k}$. But we have $0\neq e_{m+1}\in \cap_{k=1}^{m}F_{k}$, thus contradiction.