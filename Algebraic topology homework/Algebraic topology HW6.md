___

>[!problem] Problem 1
>According to Proposition 90 compute $H$, $N(H)$, and $G(\tilde{X})$ for Example 89 (ii). You can choose one of the vertexes as the base point for $\tilde{X}$.

**Proof:**
We choose the top-left vertex as the base point. Then
$$
H=\left< a^{2},b^{4},ab^{3},b^{3}ab^{2},b^{2}ab \right> ,
$$
$$
N(H)=\left< a^{2},b^{2},ab\right>.
$$
$$
G(\tilde{X})=\mathbb{Z}/2\mathbb{Z}.
$$
___

>[!problem] Problem 2
>Finish the proof of Proposition 90(ii): More precisely, show that the constructed map is a group homomorphism with kernel $H$.

**Proof:**
**($\subseteq$):** Let $[\gamma] \in \ker(\varphi)$. Then $\varphi([\gamma]) = \text{id}_{\widetilde{X}}$, so $\tau(\widetilde{x}_0) = \widetilde{x}_0$, i.e., $\widetilde{x}_1 = \widetilde{x}_0$. Thus, the lift $\widetilde{\gamma}$ is a loop in $\widetilde{X}$ based at $\widetilde{x}_0$, so $[\widetilde{\gamma}] \in \pi_1(\widetilde{X}, \widetilde{x}_0)$ and $[\gamma] = p_*([\widetilde{\gamma}]) \in H$.

**($\supseteq$):** Let $[\gamma] \in H$. Then $\exists [\widetilde{\gamma}] \in \pi_1(\widetilde{X}, \widetilde{x}_0)$ such that $[\gamma] = p_*([\widetilde{\gamma}])$. Since $\widetilde{\gamma}$ is a loop, its endpoint is $\widetilde{x}_0$. Thus, $\varphi([\gamma])(\widetilde{x}_0) = \widetilde{x}_0$. In a path-connected covering space, a deck transformation fixing a point must be the identity. Hence $\varphi([\gamma]) = \text{id}_{\widetilde{X}}$, so $[\gamma] \in \ker(\varphi)$.

Therefore, $\ker(\varphi) = H$.
___

