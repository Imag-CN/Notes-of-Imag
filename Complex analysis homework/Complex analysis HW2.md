### [GAM01]I.3.1
>[!problem] 
Sketch the image under the spherical projection of the following sets on the sphere:
**(a)** the lower hemisphere $Z \leq 0$  
**(b)** the polar cap $\frac{3}{4} \leq Z \leq 1$  
**(c)** lines of latitude  
$X = \sqrt{1 - Z^{2}} \cos\theta$,  
$Y = \sqrt{1 - Z^{2}} \sin\theta$,  
for $Z$ fixed and $0 \leq \theta \leq 2\pi$  
**(d)** lines of longitude  
$X = \sqrt{1 - Z^{2}} \cos\theta$,  
$Y = \sqrt{1 - Z^{2}} \sin\theta$,  
for $\theta$ fixed and $-1 \leq Z \leq 1$  

#### (a)
Unit closed disk $|z|\leq1$.![[Pasted image 20251009102038.png]]
#### (b)
$x^2+y^2=\dfrac{X^2+Y^2}{(1-Z)^2}=\dfrac{1-Z^2}{(1-Z)^2}=\dfrac{1+Z}{1-Z}\geq 7$.
So the image is $|z|\geq \sqrt{7}$ joint with $\infty$.![[Pasted image 20251009102233.png]]
#### (c)
- For $Z=1$, the image is $\infty$.
- For $Z\ne 1$, we have $$x^2+y^2=\dfrac{X^2+Y^2}{(1-Z)^2}=\dfrac{1-Z^2}{(1-Z)^2}=\dfrac{1+Z}{1-Z}.$$
In this case, the image is $|z|=\sqrt{\dfrac{1+Z}{1-Z}}$.![[Pasted image 20251009102434.png]]
#### (d)
We have $\dfrac{y}{x}=\dfrac{Y}{X}=\dfrac{\sin{\theta}}{\cos{\theta}}\Rightarrow x\sin{\theta}=y\cos{\theta}$.
Thus the image is $\operatorname{arg}z=\theta$ joint with $\infty$.![[Pasted image 20251009102508.png]]
___
### [GAM01]I.3.2
>[!problem] 
If the point $P$ on the sphere corresponds to $z$ under the stereographic projection, show that the antipodal point $-P$ on the sphere corresponds to $-1/\overline{z}$.

Let $P=(X,Y,Z),(X^2+Y^2+Z^2=1)$, and $z=x+iy$, then$$x=\frac{X}{1-Z},y=\frac{Y}{1-Z}.$$
Suppose $-P$ on the sphere corresponds to $z'=x'+iy'$, then$$x'=\frac{-X}{1+Z},y'=\frac{-Y}{1+Z}.$$
Together we have$$xx'+yy'=\frac{-X^2-Y^2}{1-Z^2}=-1,$$
$$xy'-x'y=\frac{XY-XY}{1-Z^2}=0.$$
Thus $\overline{z}z'=-1$, i.e. $z'=-1/\overline{z}$.
___
### [GAM01]I.3.4
>[!problem]
>Show that a rotation of the sphere of 180° about the X-axis corresponds under stereographic projection to the inversion $z \mapsto 1/z$ of C.

Let $P=(X,Y,Z)$ be an arbitrary point on the sphere $(X^2+Y^2+Z^2=1)$, and $P$ corresponds to $z=x+iy$, then$$x=\frac{X}{1-Z},y=\frac{Y}{1-Z}.$$
 Denote a rotation of the sphere of 180° about the X-axis on $P$ gives $P'$, then we have $P'=(X,-Y,-Z)$.
 Suppose $P'$ corresponds to $z'=x'+iy'$, then$$x'=\frac{X}{1+Z},y'=\frac{-Y}{1+Z}.$$
 Together we have$$xx'-yy'=\frac{X^2+Y^2}{1-Z^2}=1,$$
 $$xy'+x'y=\frac{-XY+XY}{1-Z^2}=0.$$
 Thus $zz'=-1$, i.e. $z'=1/{z}$.
 ___
### [GAM01]I.4.1
 >[!problem]
 >Sketch each curve in the $z$-plane, and sketch its image under $w=z^{2}$.
 >(a) $|z-1|=1$  
 >(b) $x=1$  
#### (a)
We have $$\begin{align}
|z-1|&=1\\
z\overline{z}-z-\overline{z}+1&=1\\
z\overline{z}&=z+\overline{z}\\
z^2\overline{z}^2&=z^2+2z\overline{z}+\overline{z}^2\\
|w|^2&=w+2|w|+\overline{w}\\
\end{align}$$![[Pasted image 20251009104608.png]]

#### (b)
We have $$\begin{align}
x&=1\\
z+\overline{z}&=2\\
z^2+2z\overline{z}+\overline{z}^2&=4\\
w+2|w|+\overline{w}&=4
\end{align}$$![[Pasted image 20251009104626.png]]
### [GAM01]I.4.2
>[!problem]
>Sketch the image of each curve in the preceding problem under the principal branch of $w = \sqrt{z}$, and also sketch, on the same grid but in a different color, the image of each curve under the other branch of $\sqrt{z}$.

#### (a)
$|z-1|=1\Rightarrow |w^2-1|=1$.
$\operatorname{Re}w\geq0$ under the principal branch, $\operatorname{Re}w\leq0$ under the other branch.![[Pasted image 20251009112200.png]]
#### (b)
$z+\overline{z}=2\Rightarrow w+\overline{w}^2=2$
$\operatorname{Re}w\geq0$ under the principal branch, $\operatorname{Re}w\leq0$ under the other branch.![[Pasted image 20251009112150.png]]
___
### [GAM01]I.5.1
>[!problem]
>Calculate and plot $e^{z}$ for the following points z:
>(a) $0$
>(b) $\pi i+1$
>(c) $\pi(i-1)/3$
>(d) $37\pi i$
>(e) $\pi i/m, m=1,2,3,\cdots$
>(f) $m(i-1) , m=1,2,3,\cdots$

#### (a)
$1$.
![[Pasted image 20251009214340.png]]
#### (b)
$-e$.
![[Pasted image 20251009214402.png]]
#### (c)
$e^{-\pi/3}(1\2+\sqrt{3}/2)$.
![[Pasted image 20251009214412.png]]
#### (d)
$-1$.
![[Pasted image 20251009214418.png]]
#### (e)
$\cos{(\pi/m)}+i\sin{(\pi/m)}$.
![[Pasted image 20251009214425.png]]
#### (f)
$e^{-m}(\cos{m}+i\sin{m})$.
![[Pasted image 20251009224235.png]]
___
### [GAM01]I.5.2
>[!problem]
>Sketch each of the following figures and its image under the exponential map $w=e^{z}$. Indicate the images of horizontal and vertical lines in your sketch.
>(c) the rectangle $0<x<1,0<y<\pi/4$,
>(d) the disk $|z|\leq\pi/2$,

#### (c)
Suppose $w=re^{i\theta}$, then $1<r<e,0<\theta<pi/4$.![[Pasted image 20251009141526.png]]
#### (d)
Suppose $z=x+iy$, then $w=e^x\cdot e^{iy},x^2+y^2\leq\pi ^2/4$.
Suppose, $w=re^{i\theta}$, then $e^{-\sqrt{\pi^2/4-\theta ^2}}\leq r\leq e^{\sqrt{\pi^2/4-\theta ^2}},-\pi/2\leq\theta \leq\pi/2$.

![[Pasted image 20251009145648.png]]
___
### [GAM01]I.5.3
>[!problem]
Show that $e^{\overline{z}}=\overline{e^{z}}$.

Let $z=x+iy$, then $\overline{z}=x-iy$.
$$\begin{align}
e^{\overline{z}}&=e^x(\cos{(-y)}+\sin{(-y)})\\
&=e^x(\cos{y}-\sin{y})\\
&=\overline{e^x(\cos{y}+\sin{y})}\\
&=\overline{e^{z}}\\
\end{align}$$
___
### [GAM01]I.5.4
>[!problem]
>Show that the only periods of $e^{z}$ are the integral multiples of $2\pi i$, that is, if $e^{z+\lambda}=e^{z}$ for all z, then $\lambda$ is an integer times $2\pi i$.

$e^{z+\lambda}=e^{z}\Rightarrow e^{z}e^{\lambda}=e^{z}\Rightarrow e^{\lambda}=1$.
Suppose $\lambda=x+iy$, then $e^x(\cos y+i\sin y)=1$.
$|e^x(\cos y+i\sin y)|=e^x=1\Rightarrow e^x=1\Rightarrow x=0$.
$\Rightarrow \cos y=1,\sin y=0\Rightarrow y=2k\pi,k\in \mathbb{Z}$.
Therefore, $z=k(2\pi i),k\in \mathbb{Z}$.
___
### [GAM01]I.6.1
>[!problem]
 Find and plot $\log z$ for the following complex numbers $z$. Specify the principal value.
 (a) $2$,
 (d) $\frac{1+i\sqrt{3}}{2}$.
 
#### (a)
 $\log2=\ln2+2k\pi i,k\in\mathbb{Z},\text{Log} 2=\ln2$.
#### (d)
 $\log(\frac{1+i\sqrt{3}}{2})=\pi i/3+2k\pi i,k\in\mathbb{Z},\text{Log} (\frac{1+i\sqrt{3}}{2})=\pi i/3$.![[Pasted image 20251009161842.png]]
 
### [GAM01]I.6.2
>[!problem]
Sketch the image under the map $w = \text{Log } z$ of each of the following figures.
 (b) the half-disk $|z| < 1$, $\text{Re } z > 0$,
 (d) the slit annulus $\sqrt{e} < |z| < e^2$, $z \notin (-e^2, -\sqrt{e})$,
 (e) the horizontal line $y = e$,

Suppose $z=re^{i\theta},w=u+iv$.
#### (b)
$u=\ln r\leq0,\theta=v\in(-\pi/2,\pi/2)$.
![[Pasted image 20251009193315.png]]
#### (d)
$u=\ln r\in(1/2,2),\theta=v\in(-\pi,\pi)$.
![[Pasted image 20251009193534.png]]
#### (e)
$r\sin\theta=e\Rightarrow u+\ln \sin v=1,\theta=v\in(0,\pi)$.
![[Pasted image 20251009194843.png]]
### [GAM01]I.6.3
>[!problem]
Define explicitly a continuous branch of $\log z$ in the complex plane slit along the negative imaginary axis, $\mathbb{C} \setminus [0, -i\infty)$.

Let $z=re^{i\theta},r\in(0,+\infty),\theta\in(-\pi/2,3\pi/2)$.
Define $\text{Log} z=\ln r +i\theta$ as a branch of $\log z$.
### [GAM01]I.6.4
>[!problem]
How would you make a branch cut to define a single-valued branch of the function $\log(z+i-1)$? How about $\log(z-z_0)$?

We directly define a branch of $\log(z-z_0)$, and we can let $z_0=1-i$.
Let $z-z_0=re^{i\theta},r\in(0,+\infty),\theta\in(-\pi,\pi)$, 
Define $\text{Log}(z-z_0)=\ln r+i\theta$, then $\text{Log}(z-z_0)=\ln r+i\theta$ is a branch on $\mathbb{C} \setminus (-\infty +z_0,z_0]$ which defines a single-valued branch of the function $\log(z-z_0)$.
___
### [GAM01]I.7.1
>[!problem]
>Find all values and plot:
>(c) $2^{-1/2}$,
>(d) $(1+i\sqrt{3})^{(1-i)}$.

#### (c)
$\pm 1/\sqrt{2}$.![[8fb08d026e433aa1775f26bcef2baa89.jpg]]
#### (d)
Compute $$(1+i\sqrt{3})^{(1-i)}=e^{(\ln2+i\frac{\pi}{3}+2ki\pi)(1-i)}=e^{(\ln2+\frac{\pi}{3}+2k\pi)+i(-ln2+\frac{\pi}{3})}.$$
They are all on a same ray.![[d0074f8415dbb4543626952df9d30574.jpg]]
___
### [GAM01]I.7.6
>[!problem]
Determine the phase factors of the function $z^{a}(1-z)^{b}$ at the branch points $z=0$ and $z=1$. What conditions on $a$ and $b$ guarantee that $z^{a}(1-z)^{b}$ can be defined as a (continuous) single-valued function on $\mathbb{C}\setminus[0,1]$?

The phase factors of the function $z^{a}(1-z)^{b}$ is $e^{2\pi ia}$ at the branch points $z=0$ and $e^{2\pi ib}$ at the branch points $z=1$.
Condition: $a+b\in\mathbb{Z}$.
___
### [GAM01]I.8.1
>[!problem]
>Establish the following addition formulae:
>(b) $\sin(z+w)=\sin z\cos w+\cos z\sin w$,
>(c) $\cosh(z+w)=\cosh z\cosh w+\sinh z\sinh w$.

#### (b)
Compute:
$$\begin{aligned}
\sin z\cos w + \cos z\sin w &= \frac{(e^{iz}-e^{-iz})(e^{iw}+e^{-iw})}{4i} + \frac{(e^{iz}+e^{-iz})(e^{iw}-e^{-iw})}{4i} \\
&= \frac{2e^{i(z+w)} - 2e^{-i(z+w)}}{4i} = \frac{e^{i(z+w)} - e^{-i(z+w)}}{2i} = \sin(z+w)
\end{aligned}$$
#### (c)
Compute:
$$\begin{aligned}
\cosh z\cosh w + \sinh z\sinh w &= \frac{(e^z+e^{-z})(e^w+e^{-w})}{4} + \frac{(e^z-e^{-z})(e^w-e^{-w})}{4} \\
&= \frac{2e^{z+w} + 2e^{-(z+w)}}{4} = \frac{e^{z+w} + e^{-(z+w)}}{2} = \cosh(z+w)
\end{aligned}$$
___
### [GAM01]I.8.2
>[!problem]
>Show that $|\cos z|^{2}=\cos^{2}x+\sinh^{2}y$, where $z=x+iy$. Find all zeros and periods of $\cos z$.
#### (1) Prove $|\cos z|^{2}=\cos^{2}x+\sinh^{2}y$
We have
$$\cos z = \cos(x+iy) = \cos x\cos(iy) - \sin x\sin(iy) = \cos x\cosh y - i\sin x\sinh y$$

Thus
$$\begin{aligned}
|\cos z|^2 &= (\cos x\cosh y)^2 + (\sin x\sinh y)^2 \\
&= \cos^2 x\cosh^2 y + \sin^2 x\sinh^2 y \\
&= \cos^2 x(1+\sinh^2 y) + \sin^2 x\sinh^2 y \\
&= \cos^2 x + \sinh^2 y(\cos^2 x + \sin^2 x) = \cos^2 x + \sinh^2 y
\end{aligned}$$

#### (2) Zeros of $\cos z$
Solve $\cos z = 0$:
$$\frac{e^{iz} + e^{-iz}}{2} = 0 \Rightarrow e^{2iz} = -1 = e^{i(\pi + 2k\pi)}$$
$$2iz = i(\pi + 2k\pi) \Rightarrow z = \frac{\pi}{2} + k\pi, \quad k \in \mathbb{Z}$$

#### (3) Periods of $\cos z$
A period $p$ satisfies $\cos(z+p) = \cos z$ for all $z$. From the exponential definition:
$$e^{i(z+p)} + e^{-i(z+p)} = e^{iz} + e^{-iz} \Rightarrow e^{ip} = 1$$
Thus $p = 2k\pi$, $k \in \mathbb{Z}$. Fundamental period is $2\pi$.
___
### [GAM01]I.8.4
>[!problem]
>Show that
>$$\tan^{-1}z=\frac{1}{2i}\log\left(\frac{1+iz}{1-iz}\right),$$
>where both sides of the identity are to be interpreted as subsets of the complex plane. In other words, show that $\tan w=z$ if and only if $2iw$ is one of the values of the logarithm featured on the right.

Let $w = \tan^{-1}z$, then $$z = \tan w = \frac{\sin w}{\cos w} = \frac{e^{iw}-e^{-iw}}{i(e^{iw}+e^{-iw})}.$$

Solve for $e^{2iw}$:
$$z = \frac{e^{2iw}-1}{i(e^{2iw}+1)} \Rightarrow iz(e^{2iw}+1) = e^{2iw}-1$$
$$ize^{2iw} + iz = e^{2iw} - 1 \Rightarrow e^{2iw}(1-iz) = 1+iz$$
$$e^{2iw} = \frac{1+iz}{1-iz} \Rightarrow 2iw = \log\left(\frac{1+iz}{1-iz}\right)$$
$$w = \frac{1}{2i}\log\left(\frac{1+iz}{1-iz}\right)$$

This shows $\tan w = z$ if and only if $2iw$ is one of the values of the logarithm.
___
### [GAM01]I.2.1
>[!problem]
 Establish the following:
 (d) $\lim_{n\to\infty}\frac{z^{n}}{n!}=0$, $z\in\mathbb{C}$.

Let $k=\lceil |z| \rceil$, then $\forall n>k, |\frac{z^{n}}{n!}|\leq\frac{|z|^{k}}{k!}\left(\frac{|z|}{k+1}\right)^{n-k}$.
$\frac{|z|^{k}}{k!}$ is a constant, while $\left(\frac{|z|}{k+1}\right)^{n-k}\rightarrow 0, n\rightarrow \infty$.
So $\lim_{n\to\infty}\frac{z^{n}}{n!}=0$, $z\in\mathbb{C}$.
### [GAM01]I.2.3
>[!problem]
>Show that $\{n^{n}z^{n}\}$ converges only for $z=0$.

Suppose $r=|z|\neq1$, then we only have to prove $\{n^{n}r^{n}\}$ doesn't converges.
For $n>2/r$, $n^{n}r^{n}>2^n\rightarrow +\infty,n\rightarrow \infty$, so $\{n^{n}r^{n}\}$ doesn't converges.
___
### [GAM01]I.2.5
>[!problem]
Show that the sequence $$b_{n}=1+\frac{1}{2}+\frac{1}{3}+\cdots+\frac{1}{n}-\log n,\quad n\geq 1,$$ is decreasing, while the sequence $a_{n}=b_{n}-1/n$ is increasing. Show that the sequences both converge to the same limit $\gamma$. Show that $\frac{1}{2}<\gamma<\frac{3}{5}$.

$b_{n+1}-b_n=1/(n+1)-\log(1+1/n)=1/(n+1)+\log(1-1/(n+1))\leq0$, so $\{b_n\}$ is decreasing.
$a_{n+1}-a_n=1/n-\log(1+1/n)\geq1/n-1/n\geq0$, so $\{a_n\}$ is increasing.
$|b_n-a_n|=1/n\rightarrow0,n\rightarrow\infty$, so $\{a_n\},\{b_n\}$ converge to the same limit.
$b_{100}<3/5,a_{100}>1/2$, so $\frac{1}{2}<\gamma<\frac{3}{5}$.
___
### [GAM01]I.2.9
>[!problem]
>Plot each sequence and determine its $\liminf$ and $\limsup$.
>(a) $s_{n}=1+\frac{1}{n}+(-1)^{n}$,
>(c) $s_{n}=\sin(\pi n/4)$.

#### (a)
$\liminf\,s_n=0$ and $\limsup\,s_n=2$.![[Pasted image 20251009231250.png]]
#### (c)
$\liminf\,s_n=-1$ and $\limsup\,s_n=1$.![[Pasted image 20251009231317.png]]

### Joukowsky function
>[!problem]
>In this exercise, we study the Joukowsky function defined by $$w=J(z):=\frac{1}{2}\left(z+\frac{1}{z}\right),\quad z\in\mathbb{C}\backslash\{0\}.$$
>(a) Suppose that $z_{1}\neq z_{2}$ satisfies $J(z_{1})=J(z_{2})$. Show that $z_{1}z_{2}=1$.
>(b) Let $z=re^{i\theta}$ and $w=J(z)$. Write $w=J(z)=u+iv$. Verify that
>$$u=\frac{1}{2}\left(r+\frac{1}{r}\right)\cos\theta,\quad v=\frac{1}{2}\left(r-\frac{1}{r}\right)\sin\theta.$$
>(c) Prove that the image of the unit circle $|z|=1$ under the mapping $J$ is the segment $[-1,1]$.
>(d) Show that the image of the circle $|z|=R\neq 1$ is the ellipse with equation
>$$\frac{u^{2}}{\left[\frac{1}{2}(R+R^{-1})\right]^{2}}+\frac{v^{2}}{\left[\frac{1}{2}(R-R^{-1})\right]^{2}}=1.$$
>(e) Verify that the image of the ray $\{z=re^{i\theta}\mid r>0\}$ under the Joukowsky function is given by $$\left\{\frac{1}{2}\left(r+\frac{1}{r}\right)\cos\theta+i\frac{1}{2}\left(r-\frac{1}{r}\right)\sin\theta\mid r>0\right\}.$$
>Describe this curve geometrically for $\theta\in[0,2\pi)$.
>(f) Determine the image of the exterior of the unit disk $|z|>1$ under the Joukowsky function $J$.

#### (a)
Prove: $$\begin{align}
J(z_1)=J(z_2)&\Rightarrow z_1+\frac{1}{z_1}= z_2+\frac{1}{z_2}\\
&\Rightarrow z_1-z_2=\frac{z_1-z_2}{z_1z_2}\\
&\Rightarrow (z_1-z_2)(1-\frac{1}{z_1z_2})=0\\
z_1\neq z_2&\Rightarrow 1-\frac{1}{z_1z_2}=0\\
&\Rightarrow z_1z_2=1\\
\end{align}$$
#### (b)
Prove: $$\begin{align}
J(z)&=\frac{1}{2}(z+\frac{1}{z})\\
&=\frac{1}{2}(re^{i\theta}+\frac{1}{r}e^{-i\theta})\\
&=\frac{1}{2}(r(\cos{\theta}+i\sin{\theta})+\frac{1}{r}(\cos{\theta}-i\sin{\theta}))\\
&=\frac{1}{2}(r\cos{\theta}+\frac{1}{r}\cos{\theta})+\frac{i}{2}(r\sin{\theta}-\frac{1}{r}\sin{\theta}))\\
\end{align}$$
Thus the conclusion holds.
#### (c)
$r=|z|=1$, so according to (b), $u=\cos{\theta},v=0$.
Thus the conclusion holds.
#### (d)
This is a direct corollary of (b).
#### (e)
This is also a direct corollary of (b).
#### (f)
From (d) we know that for a fixed $|z|$, the image is an ellipse.
The foci of the ellipse is $(-1,0)$ and $(1,0)$, and the major axis has length $|z|+|z|^{-1}>2$.
So a point is on the image if and only if it is on a ellipse with foci $(-1,0)$ and $(1,0)$.
Therefore, the image is $\mathbb{C}\setminus [-1,1]$.