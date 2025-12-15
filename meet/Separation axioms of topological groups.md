>[!notes]  Theorem
>Let $G$ be a topological group and $H$ a subgroup of $G$. The left coset space $G/H$, endowed with the quotient topology, is a Hausdorff ($T_{2}$) space if and only if $H$ is a closed subgroup of $G$.

 **Proof**:
 ($\Rightarrow$)
Since $G/H$ is Hausdorff, the point $\pi(H)$ is closed. Since the quotient map $\pi: G \to G/H$ is continuous, $\pi^{-1}(\pi(H)) = H$ is closed in $G$.

 ($\Leftarrow$)
 If $H=G$, the statement is trivial. So we assume that $H$ is a proper subgroup.
 
Arbitrarily take two distinct left coset $xH \neq yH$, then $y^{-1}x \notin H$. Since $H$ is closed, $H^c$ is an open neighbourhood of $y^{-1}x$. The map 
$$
\phi:G\times G \to G,\phi(g,k)=k^{-1}y^{-1}xg
$$
is continunous, thus $\phi^{-1}(H^c)$ is open. Since $(e,e)\in \phi^{-1}(H^c)$, there exists an open neighbourhood $U$ of $e$ such that $U\times U\subseteq\phi^{-1}(H^c)$ (because open set $\times$ open set is a basis of $G\times G$). 

The sets $\pi(xU)$ and $\pi(yU)$ are open in $G/H$ since $\pi$ is an open map (because $\pi(U)=\pi (UH)$ is open). $xU$ contains $x$, so $\pi(xU)$ contains $\pi(x)=\pi(xH)$, and similarly $\pi(yU)$ contains $\pi(yH)$. 

Now we shall show  $\pi(xU)\cap\pi(yU)=\varnothing$. Assume for contradiction that $\pi(zH) \in \pi(xU) \cap \pi(yU)$for some $z\in G$. Then $zH = xu_1H = yu_2H$ for some $u_1, u_2 \in U$, implying that $xu_1 = yu_2h$ for some $h \in H,i.e.h=u_{2}^{-1}y^{-1}xu_{1}$. However, we have $h=\phi(u_{1},u_{2})\in H^c$, which comes to a contradiction.