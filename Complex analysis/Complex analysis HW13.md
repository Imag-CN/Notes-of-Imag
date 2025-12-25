___

>[!problem] [GAM] VII.2.4
>Using residue theory, show that
>$$
>\int_{-\infty}^{\infty} \frac{dx}{x^{4}+1} = \frac{\pi}{\sqrt{2}}.
>$$

**Prove:**
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

>[!problem] [GAM] VII.2.8
>Show that
>$$
>\int_{-\infty}^{\infty} \frac{\cos x}{(1+x^2)^2} \, dx = \frac{\pi}{e}.
>$$

**Proof:**
Consider the complex function
$$f(z) = \frac{e^{iz}}{(1+z^2)^2} = \frac{e^{iz}}{(z-i)^2 (z+i)^2}.$$

$f$ has double poles at $z = i$ and $z = -i$.
We integrate over a contour consisting of the real axis from $-R$ to $R$ and the upper semicircle $C_R$ of radius $R$.
For $z$ on $C_R$, $|e^{iz}| = e^{-\operatorname{Im} z} \le 1$, and $\dfrac{1}{(1+z^2)^2} \to 0$ as $|z| \to \infty$, so by Jordan's lemma the integral over $C_R$ vanishes as $R \to \infty$.
Thus,
$$
\int_{-\infty}^{\infty} \frac{\cos x}{(1+x^2)^2} \, dx= \operatorname{Re}\left( 2\pi i \operatorname{Res}(f; i) \right),
$$
since only the pole at $z = i$ (in the upper half-plane) contributes.

Compute the residue at the double pole $z = i$:
$$
\operatorname{Res}(f; i) = \left. \dfrac{d}{dz} (z-i)^2 g(z) \right|_{z=i}= \dfrac{1}{2ie}.
$$
Thus,
$$
\int_{-\infty}^{\infty} \frac{\cos x}{(1+x^2)^2} \, dx = \frac{\pi}{e}.
$$
___

>[!problem] [GAM] VII.2.9
>Show that
>$$
>\int_{-\infty}^{\infty} \frac{\sin^{2} x}{x^{2}+1} \, dx = \frac{\pi}{2} \left[ 1 - \frac{1}{e^{2}} \right].
>$$

**Proof:**
We have
$$\int_{-\infty}^{\infty} \frac{\sin^2 x}{x^2+1} dx = \int_{-\infty}^{\infty} \frac{1 - \cos 2x}{2(x^2+1)} dx = \frac12 \int_{-\infty}^{\infty} \frac{dx}{x^2+1} - \frac12 \int_{-\infty}^{\infty} \frac{\cos 2x}{x^2+1} dx.$$

First integral:
$$\int_{-\infty}^{\infty} \frac{dx}{x^2+1} = \left.\arctan x \right|_{-\infty}^{\infty} = \pi.$$

Second integral:
Consider $J = \int_{-\infty}^{\infty} \frac{\cos 2x}{x^2+1} dx$.
Write $\cos 2x = \operatorname{Re}(e^{2ix})$ and use the complex function
$$f(z) = \frac{e^{2iz}}{z^2+1} = \frac{e^{2iz}}{(z-i)(z+i)}.$$

Integrate $f$ over the real axis and the upper semicircle.
The only pole in the upper half-plane is $z = i$ (simple pole).
Residue at $z = i$:
$$\operatorname{Res}(f; i) = \frac{e^{2i \cdot i}}{i+i} = \frac{e^{-2}}{2i}.$$

By the residue theorem and Jordan's lemma,
$$\int_{-\infty}^{\infty} f(x) dx = 2\pi i \cdot \frac{e^{-2}}{2i} = \pi e^{-2}.$$
Taking the real part gives $J = \pi e^{-2}$.

Therefore,
$$
\int_{-\infty}^{\infty} \frac{\sin^2 x}{x^2+1} dx = \frac12 \cdot \pi - \frac12 \cdot \pi e^{-2}  = \frac{\pi}{2} \left[ 1 - \frac{1}{e^2} \right].
$$
___

