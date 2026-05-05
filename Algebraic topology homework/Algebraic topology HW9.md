___

>[!problem] [HAT] 2.1.24
>Show that each $n$-simplex in the barycentric subdivision of $\Delta^n$ is defined by $n$ inequalities
>$$
>t_{i_0}\leq t_{i_1}\leq\cdots\leq t_{i_n}
>$$
>in its barycentric coordinates, where $(i_0,\dots,i_n)$ is a permutation of $(0,\dots,n)$.

**Proof:**
Let $\Delta^n=[v_0,\dots,v_n]$ with barycentric coordinates $(t_0,\dots,t_n)$ where $t_i\ge0$ and $\sum_i t_i=1$. For $n=0$, the statement is trivial. Assume the statement holds for dimension $n-1$.

Let $b=(\frac1{n+1},\dots,\frac1{n+1})$ be the barycenter. Each $n$-simplex in the subdivision is of the form $[b,w_0,\dots,w_{n-1}]$, where $[w_0,\dots,w_{n-1}]$ is an $(n-1)$-simplex in the barycentric subdivision of a face $\sigma=[v_0,\dots,\hat v_i,\dots,v_n]$. In $\sigma$, $t_i=0$.

By induction, $[w_0,\dots,w_{n-1}]$ is described by a permutation $(j_1,\dots,j_n)$ of $\{0,\dots,n\}\setminus\{i\}$ satisfying $t_{j_1}\le\dots\le t_{j_n}$, with $t_{j_1}=0$. For any $p=\lambda b+(1-\lambda)q$ ($0\le\lambda\le1$, $q\in[w_0,\dots,w_{n-1}]$), we have $t_k=\frac{\lambda}{n+1}+(1-\lambda)s_k$ where $(s_0,\dots,s_n)$ are the barycentric coordinates of $q$ with $s_i=0$. Then $t_k-t_i=(1-\lambda)s_k\ge0$, so $t_k\ge t_i$ for all $k\neq i$, with equality iff $s_k=0$. In particular, $t_{j_1}=t_i$. Thus we obtain a permutation $(i_0,\dots,i_n)$ of $\{0,\dots,n\}$ (by setting $i_0=i$ and suitably ordering the rest) such that $t_{i_0}\le t_{i_1}\le\dots\le t_{i_n}$.

Conversely, given such a permutation, let $i=i_0$; then $t_{i_0}=0$ corresponds to the face omitting $v_{i_0}$, and the remaining permutation describes an $(n-1)$-simplex in the subdivision of that face, which together with $b$ yields the desired $n$-simplex. This completes the induction.
___

>[!problem] [HAT] 2.1.25
>Find an explicit, noninductive formula for the barycentric subdivision operator $S:C_n(X)\to C_n(X)$.

**Proof:**
The barycentric subdivision operator $S_n:C_n(X)\to C_n(X)$ is defined on a singular $n$-simplex $\sigma$ by
$$
S_n(\sigma)=\sum_{\pi\in \mathfrak{S}_{n+1}}\operatorname{sgn}(\pi)\,\sigma_{b_\pi},
$$
where $\sigma_{b_\pi}:\Delta^n\to X$ is the affine map sending the vertices of $\Delta^n$ in order to the vertices of the simplex $b_\pi$ in $\Delta^n$ and then composed with $\sigma$. (The sign accounts for orientation consistency.)
