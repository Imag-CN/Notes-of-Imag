___

>[!problem]
>Given $V$ a linear space with $\mathrm{dim}V\geq 2$. Determine all the maximal right ideals of $\mathrm{Hom}(V,V)$.

**Proof:**
Let $I$ be a right ideal of $\operatorname{Hom}(V,V)$ and set $W=\sum_{f\in I}\operatorname{Im}f$. Clearly $I\subseteq\operatorname{Hom}(V,W)$. 

Conversely, take $g\in\operatorname{Hom}(V,W)$. For any $v\in V$, there exist finitely many $f_i\in I$ and $v_i\in V$ with $g(v)=\sum_i f_i(v_i)$ (this can be done by choosing $\{ f_{a}(v_{\alpha}) \}$ as a basis of $W$ and considering the decomposition of $g(v)$ under this basis). Fix a basis $\{e_\alpha\}$ of $V$. For each basis vector $e_\alpha$ with $g(e_\alpha)\neq0$, choose $f_{\alpha,j}\in I$ and $w_{\alpha,j}\in V$ such that $g(e_\alpha)=\sum_j f_{\alpha,j}(w_{\alpha,j})$. Define $h_{\alpha,j}\in\operatorname{Hom}(V,V)$ by $h_{\alpha,j}(e_\alpha)=w_{\alpha,j}$ and $h_{\alpha,j}(e_\beta)=0$ for $\beta\neq\alpha$. Then $F_{\alpha,j}:=f_{\alpha,j}\circ h_{\alpha,j}\in I$ satisfies $F_{\alpha,j}(e_\alpha)=f_{\alpha,j}(w_{\alpha,j})$ and $F_{\alpha,j}(e_\beta)=0$ for $\beta\neq\alpha$. Let $G_\alpha=\sum_j F_{\alpha,j}\in I$, so $G_\alpha(e_\beta)=0$ for $\beta\neq\alpha$ and $G_\alpha(e_\alpha)=g(e_\alpha)$. Since $g$ has finite‑dimensional image, only finitely many $e_\alpha$ have $g(e_\alpha)\neq0$. Hence $G:=\sum_\alpha G_\alpha$ is a finite sum in $I$, and $G(e_\alpha)=g(e_\alpha)$ for all $\alpha$, so $G=g$. Thus $g\in I$ and $I=\operatorname{Hom}(V,W)$.

Therefore every right ideal of $\operatorname{Hom}(V,V)$ is of the form $\operatorname{Hom}(V,W)$ for a subspace $W\subseteq V$. Since $\operatorname{Hom}(V,W_1)\subseteq\operatorname{Hom}(V,W_2)$ iff $W_1\subseteq W_2$, the maximal right ideals correspond exactly to those $W$ with $\operatorname{codim} W=1$.

