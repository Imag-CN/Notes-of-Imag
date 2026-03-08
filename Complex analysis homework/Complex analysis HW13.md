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

>[!problem] [GAM] VII.3.3
>Show using residue theory that
>$$
>\int_{0}^{\pi} \frac{\sin^2 \theta}{a + \cos \theta} \, d\theta = \pi \left[ a - \sqrt{a^2 - 1} \right], \quad a > 1.
>$$

**Proof:**
Let $I = \int_{0}^{\pi} \frac{\sin^2 \theta}{a + \cos \theta} d\theta$, $a>1$.

Set $z = e^{i\theta}$, then $d\theta = \frac{dz}{iz}$,$\cos \theta = \frac{z + z^{-1}}{2} = \frac{z^2+1}{2z}$,$\sin \theta = \frac{z - z^{-1}}{2i} = \frac{z^2-1}{2iz}$.
Thus
$$I = \int_{0}^{\pi} \frac{\sin^2 \theta}{a+\cos\theta} d\theta =\dfrac{1}{2} \int_{-\pi}^{\pi} \frac{\sin^2 \theta}{a+\cos\theta} d\theta= \frac{i}{4} \int_{|z|=1} \frac{(z^2-1)^2}{z^2(z^2+2az+1)} \, dz.$$
Let $g=\frac{(z^2-1)^2}{z^2(z^2+2az+1)}$. $z^2(z^2+2az+1)=0$ gives $z=0$ or $z = -a \pm \sqrt{a^2-1}$. $z=0$ and $z_{1}=-a+\sqrt{ a^2-1 }$ are both inside the contour, but $z_{2}=-a-\sqrt{ a^2-1 }$ is not.

Compute residue:
$$
\operatorname{Res}(g; 0) =\left. \dfrac{d}{dz} z^2 g(z) \right|_{z=0}= -2a
$$
$$
\operatorname{Res}(g; z_1) = \left. (z-z_{1})g(z) \right|_{z=z_{1}} = \frac{2 (a z_1 + 1)^2}{z_1^2 (z_1+a)}=2z_{1}+2a.
$$
Therefore, by the residue theorem,
$$
\int_{|z|=1} g(z) dz = 2\pi i \cdot (\operatorname{Res}(g; 0)+\operatorname{Res}(g; z_{1}))  = 4\pi i z_{1}.
$$

Then
$$
I = \frac{i}{4} \int_{|z|=1} g(z) dz = \frac{i}{4} \cdot 4\pi i z_{1} = -\pi z_{1}
$$
Substituting $z_{1}=-a+\sqrt{ a^2-1 }$ gives the conclusion:
$$
\int_{0}^{\pi} \frac{\sin^2 \theta}{a + \cos \theta} \, d\theta = \pi \left[ a - \sqrt{a^2 - 1} \right].
$$
___

>[!problem] [GAM] VII.4.3
>By integrating around the keyhole contour, show that
>$$
>\int_{0}^{\infty}\frac{\log x}{x^{a}(x+1)}dx=\frac{\pi^{2}\cos (\pi a)}{\sin ^{2}(\pi a)},\quad 0<a<1.
>$$

**Proof:**
Define $g(z) = \frac{\log z}{z^a (z+1)}$ with branch $0 < \arg z < 2\pi$.
Consider $g(z)$ on a keyhole contour consisting of:
- large circle $C_R: |z|=R$,
- small circle $C_\varepsilon: |z|=\varepsilon$,
- two line segments just above and below the positive real axis.

**On $C_R$:** $|z| = R \to \infty$. Take branch $\log z = \ln|z| + i\arg z$, so $|\log z| \le \ln R + 2\pi$. Also $|z^a| = |e^{a \log z}| = e^{a \ln R} = R^a$, and $|z+1| \sim R$ for large $R$. Thus $|g(z)| \le \frac{\ln R + 2\pi}{R^a \cdot R} = O\left( \frac{\ln R}{R^{1+a}} \right)$. Since $a>0$, $1+a > 1$, length of $C_R$ is $2\pi R$, so integral $\to 0$ as $R \to \infty$.

**On $C_\varepsilon$:** $|z| = \varepsilon \to 0$. Then $|\log z| \sim |\ln \varepsilon| \to \infty$, but $|z^a| = \varepsilon^a$. Also $|z+1| \to 1$. Thus $|g(z)| \le \frac{|\ln \varepsilon|}{\varepsilon^a} \cdot 1 = O( \varepsilon^{-a} |\ln \varepsilon| )$. Length of $C_\varepsilon$ is $2\pi \varepsilon$, so the integral is bounded by $O( \varepsilon^{1-a} |\ln \varepsilon| )$. Since $a<1$, $1-a>0$, and $\varepsilon^{1-a} |\ln \varepsilon| \to 0$ as $\varepsilon \to 0$. Hence the integral over $C_\varepsilon$ vanishes.

Therefore, only the contributions from the two sides of the real axis remain, leading to the residue equation as before.

Above real axis: $g=\frac{\ln x}{x^a (x+1)}$, below: $g=\frac{\ln x + 2\pi i}{x^a e^{2\pi i a} (x+1)}$.
Residue at $z=-1$: $\log(-1) = i\pi$, $(-1)^a = e^{i\pi a}$, so $\operatorname{Res}(g; -1) = \frac{i\pi}{e^{i\pi a}}$.
Let $J = \int_0^{\infty} \frac{\ln x}{x^a (x+1)} dx$, $K = \int_0^{\infty} \frac{dx}{x^a (x+1)} = \frac{\pi}{\sin \pi a}$.
By residue theorem,
$$J - e^{-2\pi i a}(J + 2\pi i K) = 2\pi i \cdot \frac{i\pi}{e^{i\pi a}} = -2\pi^2 e^{-i\pi a}.$$
Thus
$$(1 - e^{-2\pi i a}) J = 2\pi i e^{-2\pi i a} K - 2\pi^2 e^{-i\pi a}.$$
Use $1 - e^{-2\pi i a} = 2i e^{-i\pi a} \sin(\pi a)$,
$$J = \frac{2\pi i e^{-2\pi i a} \cdot \frac{\pi}{\sin \pi a} - 2\pi^2 e^{-i\pi a}}{2i e^{-i\pi a} \sin \pi a} = \frac{\pi^2 ( i e^{-i\pi a} \csc \pi a - 1)}{i \sin \pi a}.$$
Since $i e^{-i\pi a} = i \cos \pi a + \sin \pi a$, numerator becomes $\pi^2 i \cos \pi a \csc \pi a$.
Therefore $J = \frac{\pi^2 \cos \pi a}{\sin^2 \pi a}$.
___

>[!problem] [GAM] VII.7.2
>Show that
>$$
>\lim_{R\rightarrow\infty}\int_{-R}^{R}\frac{x^{3}\sin x}{\left(x^{2}+1\right)^{2}} dx=\frac{\pi}{2 e}.
>$$

**Proof:**
Denote
$$
I = \lim_{R\to\infty} \int_{-R}^{R} \frac{x^3 \sin x}{(x^2+1)^2} dx.
$$
Write $\sin x = \operatorname{Im}(e^{ix})$ and define
$$f(z) = \frac{z^3 e^{iz}}{(z^2+1)^2} = \frac{z^3 e^{iz}}{(z-i)^2 (z+i)^2}.$$

We integrate $f(z)$ over the contour consisting of the real axis from $-R$ to $R$ and the upper semicircle $C_R$ of radius $R$.
On $C_R$, $|z^3/(z^2+1)^2| \to 0$ as $|z|\to\infty$, so by Jordan's lemma the integral over $C_R$ vanishes as $R\to\infty$.
Thus
$$
I = \operatorname{Im} \left( 2\pi i \sum \text{Residues in upper half-plane} \right).
$$
$f$ has double poles at $z=i$ and $z=-i$, and only $z=i$ lies in the upper half-plane.

Compute residue:
$$
\operatorname{Res}(f; i) = \left. \dfrac{d}{dz} (z-i)^2 f(z) \right|_{z=i}=\dfrac{1}{4e}.
$$
Hence
$$
2\pi i \cdot \operatorname{Res}(f; i) = 2\pi i \cdot \frac{1}{4e} = \frac{\pi i}{2e}.
$$
Therefore,
$$
\lim_{R\to\infty} \int_{-R}^{R} \frac{x^3 \sin x}{(x^2+1)^2} dx = \frac{\pi}{2e}.
$$
___

>[!problem] [GAM] VII.8.1
>Evaluate the residue at $\infty$ of the following functions.
>
>(a) $\frac{z}{z^2-1}$
>
>(f) $\sqrt{\frac{z-a}{z-b}}$

**Proof:**
Use $\operatorname{Res}(f; \infty) = -\operatorname{Res}(f(1/z)/z^2; 0)$.

**(a)** $f(z) = \frac{z}{z^2-1}$.
Set $w = 1/z$, then $z = 1/w$.
$$
f(1/w) = \frac{1/w}{(1/w)^2 - 1} = \frac{1/w}{1/w^2 - 1} = \frac{1/w}{\frac{1 - w^2}{w^2}} = \frac{w}{1-w^2}.
$$
Thus
$$
\frac{f(1/w)}{w^2} = \frac{w}{1-w^2} \cdot \frac{1}{w^2} = \frac{1}{w(1-w^2)} = \frac{1}{w}(1 + w^2 + w^4 + \cdots) = \frac{1}{w} + w + w^3 + \cdots.
$$
The coefficient of $1/w$ is $1$, so $\operatorname{Res}(f(1/w)/w^2; 0) = 1$.
Hence $\operatorname{Res}(f; \infty) = -1$.

**(f)** $f(z) = \sqrt{\frac{z-a}{z-b}}$, where we choose a branch of the square root.
Let $w = 1/z$, so $z = 1/w$.
Then
$$
f(1/w) = \sqrt{\frac{1/w - a}{1/w - b}} = \sqrt{\frac{1 - a w}{1 - b w}}.
$$
Thus
$$
\frac{f(1/w)}{w^2} = \frac{1}{w^2} \sqrt{\frac{1 - a w}{1 - b w}}.
$$
We expand $\sqrt{\frac{1 - a w}{1 - b w}}$ for small $w$ (choose the principal branch near $w=0$, i.e., $\sqrt{1}=1$):
$$
\sqrt{\frac{1 - a w}{1 - b w}} = (1 - a w)^{1/2} (1 - b w)^{-1/2} = \left(1 - \frac{a}{2}w - \frac{a^2}{8}w^2 + \cdots \right) \left(1 + \frac{b}{2}w + \frac{3b^2}{8}w^2 + \cdots \right).
$$
Multiplying,
$$
= 1 + \frac{b - a}{2} w + \left( \frac{3b^2}{8} - \frac{ab}{4} - \frac{a^2}{8} \right) w^2 + \cdots.
$$
Hence
$$
\frac{f(1/w)}{w^2} = \frac{1}{w^2} + \frac{b - a}{2} \cdot \frac{1}{w} + \text{holomorphic terms}.
$$
The coefficient of $1/w$ is $\dfrac{b-a}{2}$, so $\operatorname{Res}(f(1/w)/w^2; 0) = \dfrac{b-a}{2}$
Hence $\operatorname{Res}(f; \infty) = \dfrac{a-b}{2}$.

For the other branch of the square root, we take the negative of the above expansion, so the residue at $\infty$ becomes $\dfrac{b-a}{2}$.
___

>[!problem] [SL] 4.4.1
>设 $D$ 是由有限条可求长简单闭曲线围成的域. 证明: 若 $f,g\in H(D)$, $f$ 在 $\partial D$ 上没有零点, $f$ 在 $D$ 中的全部彼此不同的零点为 $z_{1},z_{2}, \cdots ,z_{n}$, 其相应的阶数分别为 $k_{1},k_{2}, \cdots ,k_{n}$, 则
>$$
>\frac{1}{2\pi i}\int_{\partial D}g(z)\frac{f^{\prime}(z)}{f(z)}dz=\sum_{j=1}^{n}k_{j}g(z_{j}).
>$$

**证明:**
对任意的零点$z_{j}$, 由零点阶数的性质, 在 $z_j$ 的某个去心邻域内, 有
$$
f(z) = (z - z_j)^{k_j} h_j(z),
$$
其中 $h_j \in H(D)$ 且 $h_j(z_j) \neq 0$.

由此得
$$
\frac{f'(z)}{f(z)} = \frac{k_j}{z - z_j} + \frac{h_j'(z)}{h_j(z)}.
$$
因 $h_j(z_j) \neq 0$, 故 $h_j'/h_j$ 在 $z_j$ 处全纯.

对 $g(z) \frac{f'(z)}{f(z)}$ 在每个 $z_j$ 附近应用留数定理:
$$
\operatorname{Res}\left(g(z)\frac{f'(z)}{f(z)}; z_j\right) = k_j g(z_j),
$$
因 $\dfrac{k_j g(z)}{z - z_j}$ 在 $z_{j}$ 附近的 Laurent 展开为 $\dfrac{k_j g(z_j)}{z - z_j} + \text{全纯项}$.

由 $f$ 在 $\partial D$ 上无零点, 知 $g(z) f'(z)/f(z)$ 在 $D$ 内除 $z_1, \dots, z_n$ 外全纯, 在 $z_j$ 处有一阶极点, 留数为 $k_j g(z_j)$.

由留数定理,
$$
\frac{1}{2\pi i} \int_{\partial D} g(z) \frac{f'(z)}{f(z)} dz = \sum_{j=1}^n \operatorname{Res}\left(g(z)\frac{f'(z)}{f(z)}; z_j\right) = \sum_{j=1}^n k_j g(z_j).
$$
证毕.