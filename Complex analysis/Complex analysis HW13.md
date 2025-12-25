___

>[!problem] [GAM] VII.2.4
>Using residue theory, show that
>$$
>\int_{-\infty}^{\infty} \frac{dx}{x^{4}+1} = \frac{\pi}{\sqrt{2}}.
>$$

**Solution:**
Let $f(z) = \dfrac{1}{z^4 + 1}$.
The poles of $f$ are the solutions of $z^4 = -1 = e^{i\pi(1+2k)}$ for $k \in \mathbb{Z}$.
Thus, $z_k = e^{i\pi(1+2k)/4}$ for $k = 0, 1, 2, 3$.

The four simple poles are:
$z_0 = e^{i\pi/4}, \quad z_1 = e^{i3\pi/4}, \quad z_2 = e^{i5\pi/4}, \quad z_3 = e^{i7\pi/4}$.

The ones in the upper half-plane ($\operatorname{Im} z > 0$) are $z_0$ and $z_1$.

$\operatorname{Res}(f; z_0) = -\frac{1}{4} e^{i\pi/4}$,
$\operatorname{Res}(f; z_1) = -\frac{1}{4} e^{i3\pi/4}$.

For the contour consisting of the real axis from $-R$ to $R$ and the upper semicircle $C_R$ of radius $R$, and taking $R \to \infty$, the integral over $C_R$ vanishes because $|zf(z)| \sim 1/|z|^3 \to 0$.
Thus,
$$
\int_{-\infty}^{\infty} f(x)\,dx = 2\pi i \sum \operatorname{Res} = 2\pi i \left( -\frac{i\sqrt{2}}{4} \right) = 2\pi i \cdot (-i)\frac{\sqrt{2}}{4} = 2\pi \cdot \frac{\sqrt{2}}{4} = \frac{\pi\sqrt{2}}{2}.
$$
Therefore,
$$
\int_{-\infty}^{\infty} \frac{dx}{x^4+1} = \frac{\pi}{\sqrt{2}}.
$$
___

