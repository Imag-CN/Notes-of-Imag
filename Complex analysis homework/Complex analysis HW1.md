### [Gam01]I.1.1


>[!problem]
Identify and sketch the set of points satisfying:
(a) $|z-1-i|=1$,
(b) $1<|2z-6|<2$,
(c) $|z-1|^{2}+|z+1|^{2}<8$,
(d) $|z-1|+|z+1|\leq2$,
(e) $|z-1|<|z|$,
(i) $\operatorname{Re}(iz+2)>0$.

<div style="page-break-after: always;"></div>
#### (a)
A circle centered at $1 + i$ with radius $1$.
#### (b)
Simplified to $\frac{1}{2} < |z - 3| < 1$.
Open region between circles centered at $3$ with radii $0.5$ and $1$.
#### (c)
Simplified to $|z|<3$.
Interior of circle centered at origin with radius $\sqrt{3}$.
#### (d)
Segment connecting $-1$ to $1$.
#### (e)
Simplified to $\operatorname{Re}z > \frac{1}{2}$.
Right half-plane to the line $\operatorname{Re}z = \frac{1}{2}$.
#### (i)
Simplified to $\operatorname{Im}z < 2$.
Lower half-plane below the line $\operatorname{Im}z = 2$.
![[8ee6a5ae-2640-44c5-8443-260ae0dc8349.png]]
### [Gam01]I.1.3
>[!problem]
>Show that the equation $|z|^{2}-2\operatorname{Re}(\bar{a}z)+|a|^{2}=\rho^{2}$ represents a circle centered at a with radius $\rho$.

($\rho$ should be positive.)
Simplify:<div style="page-break-after: always;"></div>

$$\begin{align}
|z|^{2}-2\operatorname{Re}(\bar{a}z)+|a|^{2}&=\bar{z}z-(\bar{a}z+a\bar{z})+\bar{a}a\\
&=\bar{z}(z-a)-\bar{a}(z-a)\\
&=(\bar{z}-\bar{a})(z-a)\\
&=|z-a|^2
\end{align}$$
Thus the equation is equivalent to $|z-a|=\rho$, which represents a circle centered at a with radius $\rho$.
### [Gam01]I.1.6
>[!problem]
 For fixed $a\in \mathbb{C}$, show that $\frac{|z-a|}{|1-\bar{a}z|} = 1$ if $|z| = 1$ and $1-\bar{a}z \neq 0$.

$$\begin{align}
|z|=1 &\Rightarrow \bar{z}z = 1\\
&\Rightarrow \bar{z}z+\bar{a}a = 1+\bar{z}z\bar{a}a\\
&\Rightarrow \bar{z}z-\bar{a}z-a\bar{z}+\bar{a}a = 1-\bar{a}z-a\bar{z}+\bar{z}z\bar{a}a\\
&\Rightarrow (\bar{z}-\bar{a})(z-a)=(1-a\bar{z})(1-\bar{a}z)\\
&\Rightarrow |z-a|=|1-\bar{a}z|\\
1-\bar{a}z \neq 0 \Rightarrow |1-\bar{a}z|\ne0 &\Rightarrow \frac{|z-a|}{|1-\bar{a}z|} = 1
\end{align}$$
>[!tip]
>The inverse doesn't hold, $\frac{|z-a|}{|1-\bar{a}z|} = 1$ only derives $|z| = 1$ or $|a| = 1$.
### [Gam01]I.2.1
>[!problem] 
>Express all values of the following expressions in both polar and cartesian coordinates, and plot them.
(b) $\sqrt{i-1}$
(c) $\sqrt[4]{-1}$
(e) $(-8)^{1/3}$
(f) $(3-4i)^{1/8}$
(h) $\left(\frac{1+i}{\sqrt{2}}\right)^{25}$

#### (b)
 $i = \sqrt{2}e^{i(3\pi/4+2k\pi)}\Rightarrow \sqrt{i-1} = \sqrt[4]{2}e^{i(3\pi/8 + k\pi)},k=0,1$.
- For $k=0,\sqrt{i-1} = \sqrt{\frac{2-\sqrt{2}}{2}} + i\sqrt{\frac{2+\sqrt{2}}{2}}$,
- For $k=1,\sqrt{i-1} = -\sqrt{\frac{2-\sqrt{2}}{2}} -i\sqrt{\frac{2+\sqrt{2}}{2}}$.![[Pasted image 20250926105539.png]]
#### (c)
$-1 = e^{i(\pi + 2k\pi)} \Rightarrow \sqrt[4]{-1} = e^{i(\pi/4 + k\pi/2)},k=0,1,2,3$.
- For $k=0 ,\sqrt[4]{-1} = \frac{\sqrt{2}}{2} + i\frac{\sqrt{2}}{2}$,
- For $k=1,\sqrt[4]{-1} = -\frac{\sqrt{2}}{2} + i\frac{\sqrt{2}}{2}$,
- For $k=2,\sqrt[4]{-1} = -\frac{\sqrt{2}}{2} - i\frac{\sqrt{2}}{2}$,
- For $k=3,\sqrt[4]{-1} = \frac{\sqrt{2}}{2} - i\frac{\sqrt{2}}{2}$.![[image-2025-09-21T14-00-14Z.png]]
#### (e)
$-8 = 8e^{i(\pi + 2k\pi)}\Rightarrow (-8)^{1/3} = 2e^{i(\pi/3 + 2k\pi/3)},k=0,1,2$
- For $k=0,(-8)^{1/3} = 1 + i\sqrt{3}$,
- For $k=1,(-8)^{1/3} = -2$,
- For $k=2,(-8)^{1/3} = 1 - i\sqrt{3}$.![[image-2025-09-21T14-15-21Z.png]]
#### (f)
 $3-4i = 5e^{-i\arctan(4/3)}\Rightarrow (3-4i)^{1/8} = 5^{1/8}e^{-i(\arctan(4/3) + 2k\pi)/8},k=0,1,...,7$,
 $\Rightarrow (3-4i)^{1/8}=5^{1/8}\cos{((\arctan(4/3) + 2k\pi)/8)}+i5^{1/8}\sin{((\arctan(4/3) + 2k\pi)/8)},k=0,1,...,7$.![[Pasted image 20250921221718.png]]
#### (g)
$\left( \dfrac{1+i}{\sqrt{2}} \right)^{25}=\left(e^{i\pi/4}\right)^{25} = e^{i25\pi/4} = e^{i(6\pi + \pi/4)} = e^{i\pi/4} = \dfrac{1+i}{\sqrt{2}}$.![[Pasted image 20250921222052.png]]
### [Gam01]I.2.1
>[!problem]
For a fixed complex number $b$, sketch the curve $\left\{e^{i\theta}+be^{-i\theta}:0\le\theta\le 2\pi\right\}$. Differentiate between the cases $|b|<1$, $|b|=1$ and $|b|>1$.

Let $z=e^{i\theta}+be^{-i\theta}, b=re^{i\rho},\theta ' = \theta -\rho / 2,z'=e^{i\theta'}+re^{-i\theta'}$.
Then $z=e^{\frac{i\rho}{2}}(e^{i\theta'}+re^{-i\theta'})=e^{\frac{i\rho}{2}}z'$, which means $z$ is obtained by rotating $\frac{\rho}{2}$ about the origin to get $z'$.
According to Euler's formula, $z'=(1+r)\cos{\theta'}+(1-r)\sin{\theta'}$
- For $|b|=r=1$, the curve is the segment connecting $2e^{\frac{i\rho}{2}}$ and $-2e^{\frac{i\rho}{2}}$,
- For $|b| =r \ne 1$, we have $\left( \dfrac{\operatorname{Re}z'}{1+r} \right)^2+\left( \dfrac{\operatorname{Im}z'}{1-r} \right)^2=1$, thus the curve is an ellipse.
Specifically, $|b|=0$ gives a circle. And in other cases we have
- For $0<|b| =r < 1$, the semi-major axis of the ellipse is $1+r$, and the semi-minor axis is $1-r$.
- - For $|b| =r > 1$, the semi-major axis of the ellipse is $1+r$, and the semi-minor axis is $r-1$.
![[Pasted image 20250926114909.png]]
### [Gam01] I.2.5
 >[!problem]
 For $n\ge1$, show that
(a) $1+z+z^{2}+\cdots+z^{n}=\left(1-z^{n+1}\right)/\left(1-z\right)$, $z\neq1$,
(b) $1+\cos\theta+\cos 2\theta+\cdots+\cos n\theta=\frac{1}{2}+\frac{\sin\left(n+\frac{1}{2}\right)\theta}{2\sin\theta/2}$.
#### (a)
Let $S=1+z+z^{2}+\cdots+z^{n}$, then$$\begin{align}
zS&=z+z^{2}+z^{3}+\cdots+z^{n+1}\\
(1-z)S&=(1+z+z^{2}+\cdots+z^{n})-(z+z^{2}+z^{3}+\cdots+z^{n+1})\\
(1-z)S&=1-z^{n+1}
\end{align}$$Since $z\ne 1$, we have $S=\dfrac{1-z^{n+1}}{1-z}$.
#### (b)
Let $A=1+\cos\theta+\cos 2\theta+\cdots+\cos n\theta,B=\sin \theta+\sin 2\theta+\cdots+\sin n\theta$, then $$\begin{align}
A+iB&=1+e^{i\theta}+\cdots+e^{in\theta}\\
\text{by (a) }\Rightarrow A+iB&=\frac{1-e^{i(n+1)\theta}}{1-e^{i\theta}}\tag{1}\\
A-iB&=1+e^{-i\theta}+\cdots+e^{-in\theta}\\
\text{by (a) }\Rightarrow A-iB&=\frac{1-e^{-i(n+1)\theta}}{1-e^{-i\theta}}\tag{2}\\
\end{align}$$
$\dfrac{(1)+(2)}{2}$ yields $A=\frac{1}{2}+\frac{\sin\left(n+\frac{1}{2}\right)\theta}{2\sin\theta/2}$.


### [Gam01] I.2.6
>[!problem] 
>Fix $n\ge1$. Show that the $n$th roots of unity $\omega_{0},\ldots,\omega_{n-1}$ satisfy:
(a) $(z-\omega_{0})(z-\omega_{1})\cdots(z-\omega_{n-1})=z^{n}-1$,
(b) $\omega_{0}+\cdots+\omega_{n-1}=0$ if $n\ge2$,
(c) $\omega_{0}\cdots\omega_{n-1}=(-1)^{n-1}$,
(d) $\sum_{j=0}^{n-1}\omega_{j}^{k}=\begin{cases}0, & 1\le k\le n-1, \\ n, & k=n. \end{cases}$
#### (a)
$\omega_j（1\leq j\leq n-1$） is a root of $z^n-1$，thus $z-\omega_j\mid z^n-1$.
$\omega_j\ne\omega_l,j\ne l$, thus $(z-\omega_{0})(z-\omega_{1})\cdots(z-\omega_{n-1})\mid z^{n}-1$,
$(z-\omega_{0})(z-\omega_{1})\cdots(z-\omega_{n-1})$ and $z^{n}-1$ are both monic and have the same degree $n$, so $(z-\omega_{0})(z-\omega_{1})\cdots(z-\omega_{n-1})=z^{n}-1$.
#### (b)
Compare the coefficient of $z^{n−1}$ on both sides of the equation yields this equality.
#### (c)
Compare the constant term on both sides of the equation yields this equality.
#### (d)
If $k=n$, we have $\omega_{j}^{k}=1$ since $\omega_{j}$ is the $n$th root of unity.
In this case, $\sum_{j=0}^{n-1}\omega_{j}^{k}=n$.
If $1\leq k \leq n$, we have $e^{\frac{2k\pi i}{n}}\ne1$,and $$
\begin{align}
\sum_{j=0}^{n-1}\omega_{j}^{k}&=\sum_{j=0}^{n-1}e^{\frac{2jk\pi i}{n}}\\
&=\frac{1-e^{\frac{2nk\pi i}{n}}}{1-e^{\frac{2k\pi i}{n}}}\\
&=0
\end{align}$$
So in this case,  $\sum_{j=0}^{n-1}\omega_{j}^{k}=0$.
### [SL98] 1.1.7
>[!problem] 习题
设 $z_{1},\cdots,z_{n},w_{1},\cdots,w_{n}$ 是任意 $2n$ 个复数, 证明复数形式的 Lagrange 等式:
$$ \left|\sum_{j=1}^{n}z_{j}w_{j}\right|^{2}=\left(\sum_{j=1}^{n}|z_{j}|^{2}\right)\left(\sum_{j=1}^{n}|w_{j}|^{2}\right)-\sum_{1\leq j<k\leq n}|z_{j}\overline{w}_{k}-z_{k}\overline{w}_{j}|^{2}, $$
并由此推出 Cauchy 不等式:
$$ \left|\sum_{j=1}^{n}z_{j}w_{j}\right|^{2}\leq\left(\sum_{j=1}^{n}|z_{j}|^{2}\right)\left(\sum_{j=1}^{n}|w_{j}|^{2}\right). $$
不等式中等号成立的条件是什么?

#### Lagrange 等式
将等式改写为
$$ \left( \sum_{j=1}^{n}z_{j}w_{j}\right) \left(  \sum_{j=1}^{n}\overline{z_{j}w_{j}}\right)=\left(\sum_{j=1}^{n}z_{j}\overline{z_{j}}\right)\left(\sum_{j=1}^{n}w_{j}\overline{w_{j}}\right)-\sum_{1\leq j<k\leq n}(z_{j}\overline{w}_{k}-z_{k}\overline{w}_{j})(\overline{z_{j}}w_{k}-\overline{z_{k}}w_j), $$
使用数学归纳法进行证明.
当 $n=1$ 时, 等式平凡.
假设当 $n=m$ 时等式成立, 则 $n=m+1$ 时,
$$\begin{align}
\left( \sum_{j=1}^{m+1}z_{j}w_{j}\right) \left( \sum_{j=1}^{m+1}\overline{z_{j}w_{j}}\right) =& \left(z_{m+1}w_{m+1}+\sum_{j=1}^{m}z_{j}w_{j} \right) \left( \overline{z_{m+1}w_{m+1}}+\sum_{j=1}^{m}\overline{z_{j}w_{j}}\right)\\
=& \left( z_{m+1}w_{m+1}\cdot \sum_{j=1}^{m}\overline{z_{j}w_{j}} \right) +\left( \overline{z_{m+1}w_{m+1}}\cdot \sum_{j=1}^{m}\overline{z_{j}w_{j}}\right)\\
&+\overline{z_{m+1}w_{m+1}}z_{m+1}w_{m+1}+
\left( \sum_{j=1}^{m}z_{j}w_{j}\right) \left(  \sum_{j=1}^{m}\overline{z_{j}w_{j}}\right)\\
\text{(归纳假设)}=&\left( z_{m+1}w_{m+1}\cdot \sum_{j=1}^{m}\overline{z_{j}w_{j}} \right) +\left( \overline{z_{m+1}w_{m+1}}\cdot \sum_{j=1}^{m}\overline{z_{j}w_{j}}\right)+\overline{z_{m+1}w_{m+1}}z_{m+1}w_{m+1}\\
&+\left(\sum_{j=1}^{m}z_{j}\overline{z_{j}}\right)\left(\sum_{j=1}^{m}w_{j}\overline{w_{j}}\right)-\sum_{1\leq j<k\leq m}(z_{j}\overline{w}_{k}-z_{k}\overline{w}_{j})(\overline{z_{j}}w_{k}-\overline{z_{k}}w_j)\\
&=\left(\sum_{j=1}^{m+1}z_{j}\overline{z_{j}}\right)\left(\sum_{j=1}^{m+1}w_{j}\overline{w_{j}}\right)-\sum_{1\leq j<k\leq m+1}(z_{j}\overline{w}_{k}-z_{k}\overline{w}_{j})(\overline{z_{j}}w_{k}-\overline{z_{k}}w_j)

\end{align}$$
因此 Lagrange 等式成立.
#### Cauchy 不等式
由于$\sum_{1\leq j<k\leq n}|z_{j}\overline{w}_{k}-z_{k}\overline{w}_{j}|^{2}\geq 0$, 根据 Lagrange 等式, 有$$ \left|\sum_{j=1}^{n}z_{j}w_{j}\right|^{2}\leq\left(\sum_{j=1}^{n}|z_{j}|^{2}\right)\left(\sum_{j=1}^{n}|w_{j}|^{2}\right). $$
当且仅当$\sum_{1\leq j<k\leq n}|z_{j}\overline{w}_{k}-z_{k}\overline{w}_{j}|^{2}= 0$, 即 $z_{j}\overline{w}_{k}=z_{k}\overline{w}_{j}, 1\leq j<k\leq n$ 时取等.
### [SL98] 1.1.8
>[!problem] 习题
设 $z_{1},\cdots,z_{n}$ 是任意 $n$ 个复数, 证明必有 $\{1,2,\cdots,n\}$ 的子集 $E$, 使得
$$ \left|\sum_{j\in E}z_{j}\right|\geq \frac{1}{6}\sum_{j=1}^{n}|z_{j}|. $$

记 $Z_k=\{z \in \mathbb{C}:\dfrac{k\pi}{4}<z\text{ 的某个辐角} \leq \dfrac{(k+2)\pi}{4} \}$ , 则 $\mathbb{C}\textbackslash\{0\}$是 $Z_1,\cdots,Z_4$ 的无交并.
不失一般性地, 设 $\sum_{j=1}^{n}|z_{j}|=1$, 且不妨假设 $z_{1},\cdots,z_{n}$ 都不为0.
我们可以得到 $1=\sum_{j=1}^{n}|z_{j}|=\sum_{k=1,2,3,4}\sum_{z_j\in Z_k}|z_{j}|$.
根据抽屉原理, 存在一个 $k\in\{1,2,3,4\}$ , 使得$\sum_{z_j\in Z_k}|z_{j}|\geq \frac{1}{4}$, 不妨设这个 $k$ 为 $1$.
$z\in Z_1 \Rightarrow \operatorname{Im}z >0,\operatorname{Im}z\geq \operatorname{Re}z  \Rightarrow \operatorname{Im}z>\dfrac{|z|}{\sqrt{2}}$ .
$\left|\sum_{j\in Z_1}z_{j}\right|\geq \sum_{j\in Z_1}\operatorname{Im}z_{j}>\sum_{j\in Z_1}\dfrac{|z|}{\sqrt{2}}\geq\dfrac{1}{4\sqrt{2}}>\dfrac{1}{6}$.
因此$\left|\sum_{j\in Z_1}z_{j}\right|\geq \dfrac{1}{6}\sum_{j=1}^{n}|z_{j}|$.
>[!tip] 加强与推广
>1. $v_{1},\cdots,v_{n} \in \mathbb{R}^2$ 且满足$\sum_{j=1}^{n}|v_{j}|=1$, 证明必有 $\{1,2,\cdots,n\}$ 的子集 $E$, 
$$ \left|\sum_{j\in E}v_{j}\right|> \frac{1}{\pi}.$$且$\dfrac{1}{\pi}$是最佳系数.
>2.  $v_{1},\cdots,v_{n} \in \mathbb{R}^d$ 且满足$\sum_{j=1}^{n}|v_{j}|=1$, 证明必有 $\{1,2,\cdots,n\}$ 的子集 $E$, 使得
$$ \left|\sum_{j\in E}v_{j}\right| > \frac{\Gamma \left( \frac{d}{2}\right) }{2\sqrt{\pi}\Gamma \left( \frac{d+1}{2} \right)}.$$且$\frac{\Gamma \left( \frac{d}{2}\right) }{2\sqrt{\pi}\Gamma \left( \frac{d+1}{2} \right)}$是最佳系数.
#### 1. 命题的加强
##### 方法1 周长与直径
令 $v_{n+1}=-(v_1+\cdots+v_n)$.
将 $v_1,\cdots,v_{n+1}$ 中的非零向量按辐角主值升序排列, 首尾相接, 得到一个周长大于等于 $1$ 的凸多边形.
我们根据以下两个事实:
(1) 任何凸集被包含在一个与它直径相同等宽曲线中 (可以直接构造); 
(2) 如果一个凸集包含另一个凸集, 则它的半径不会更小 (根据弧长积分推导);
得到: 平面凸集的周长与直径最小比值为 $\pi$ (当且仅当该凸集为等宽曲线时取等) 
而凸多边形的直径总是两个顶点的距离,所以 $v_1,\cdots,v_{n+1}$ 中一定存在一些向量的加和的模长大于$\dfrac{1}{\pi}$.
如果这些向量中包含 $v_{n+1}$, 则取剩下的向量, 它们的和具有相同的模长.
##### 方法2 积分与期望
应当选取处于同一个半平面的向量, 但选取哪个半平面是不确定的, 因此考虑遍历所有半平面.
等价地考虑任取一个单位向量, 与其同向 (内积非负) 的向量之和的模长的期望.
$$
\begin{aligned}
\mathbb{E}(\|v_{\theta}\|) & \geq \mathbb{E}\left(\sum_{k \in S_{\theta}}\left\langle v_{k}, u_{\theta}\right\rangle\right) \\
& =\mathbb{E}\left(\sum_{k \in S_{\theta}}\left\|v_{k}\right\| \cos \left(\theta_{k}-\theta\right)\right) \\
& =\mathbb{E}\left(\sum_{k=1}^{n}\left\|v_{k}\right\| \max \left\{0, \cos \left(\theta_{k}-\theta\right)\right\}\right) \\
& =\sum_{k=1}^{n}\left\|v_{k}\right\| \mathbb{E}\left(\max \left\{0, \cos \left(\theta_{k}-\theta\right)\right\}\right) \\
& =\frac{1}{\pi} \sum_{k=1}^{n}\left\|v_{k}\right\| \\
& =\frac{1}{\pi}
\end{aligned}$$
##### 最佳系数
考虑等周分布的单位向量, n趋于无穷时的情况即可.
#### 2. 命题的推广
沿用方法2即可.
### [SL98] 1.2.8
>[!problem] 习题
>图 1.6 中, $ABED, ACFG$ 是正方形, $AH\bot BC$, $M$ 是 $DG$ 的中点. 证明: $M, A, H$ 三点共线.
>![[4ccff81599c79cdd74c2c0917b37c08e.jpg]]



以 $A$ 为原点, 任意方向为实轴正方向建立复平面, 以点代表复数.
由于 $ABED, ACFG$ 是正方形, 结合图像, 有 $D=-iB,G=iC$.
$M$ 是 $DG$ 的中点, 所以 $M=\dfrac{i}{2}(C-B)$, 即 $\dfrac{M-A}{C-B}=\dfrac{i}{2}$.
因此 $MA\bot CB$, 即 $M, A, H$ 三点共线.
