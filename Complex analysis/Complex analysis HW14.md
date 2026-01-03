___

>[!problem] [GAM] VIII.1.1
>Show that $z^{4}+2z^{2}-z+1$ has exactly one root in each quadrant.

**Proof:**
Denote $z=x+iy$, $P(z)=z^{4}+2z^{2}-z+1$.
When $y=0$:
$$
P(z)=P(x)=x^4+2x^2-x+1=(x^2+1 /2)^2+(x-1 /2)^2+1 /2>0
$$
Thus $P(z)$ has no root on the real axis.
When $x=0$:
$$
P(z)=P(iy)=y^4-2y^2-iy+1=(y^4-2y^2+1)-iy
$$
Since $y^4-2y^2+1$ and $iy$ cannot be zero at the same time, $P(z)$ has no root on the imaginary axis.

Construct contour as the following graph:
![[Pasted image 20260103222321.png]]
where $R$ is a sufficiently large positive number.

Since $P(z)$ is positive on the real axis, $\Delta_{\gamma_{1}}\mathrm{Arg}\,P(z)=0$.

Write $P(z)=z^4Q(z)$, where $Q(z)=1+ \dfrac{2z^2-z+1}{z^4}$. When $|z|=R$ is sufficient large, $|Q(z)-1|<1/2$, so $\Delta_{\gamma_{2}}\mathrm{Arg}\,Q(z)=0$. Thus 
$$
\Delta_{\gamma_{2}}\mathrm{Arg}\,P(z)=\Delta_{\gamma_{2}}\mathrm{Arg}\,z^4+\Delta_{\gamma_{2}}\mathrm{Arg}\,Q(z)=2\pi.
$$
On $\gamma_{3}$:
$$
\begin{align}
\Delta_{\gamma_{3}}\mathrm{Arg}\,P(z)&=\mathrm{Arg}\,P(0)-\mathrm{Arg}\,P(iR) \\

\end{align}
$$
