### [GAM01] II.1.11
>[!problem]
>At what points does the function $\operatorname{Arg} z$ have a limit? Where is $\operatorname{Arg} z$ continuous? Justify your answer.
>

**Claim:** $\operatorname{Arg}z$ has a limit (and is continuous) at $z_0$ iff $z_0\in\mathbb{C}\setminus(-\infty,0]$.

**Proof:**
- For $z_0\in(-\infty,0)$, approaching from above/below gives $\pi$/$-\pi$ ⇒ no limit.
- At $z_0=0$, undefined ⇒ no limit.
- Elsewhere, $\operatorname{Arg}z$ equals a continuous branch of $\arg z$ ⇒ limit exists and equals $\operatorname{Arg}z_0$.
___
### [GAM01] II.1.13
>[!problem]
>For which complex values of $\alpha$ does the principal value of $z^{\alpha}$ have a limit as $z$ tends to $0$? Justify your answer.

$\lim_{z\to 0}z^{\alpha}=0\Leftrightarrow\lim_{|z|\to 0}|z|^{\alpha}=0\Leftrightarrow \alpha>0$, thus $\lim_{z\to 0}z^{\alpha}=0\Leftrightarrow \alpha>0$.
___
### [GAM01] II.1.15
>[!problem]
>Which of the following sets are open subsets of $\mathbb{C}$? Which are closed? Sketch the sets.
>(a) The punctured plane $\mathbb{C}\backslash\{0\}$,
>(b) the exterior of the open unit disk in the plane, $\{|z|\geq 1\}$,
>(c) the exterior of the closed unit disk in the plane, $\{|z|>1\}$,
>(d) the plane with the open unit interval removed, $\mathbb{C}\backslash(0,1)$,
>(e) the plane with the closed unit interval removed, $\mathbb{C}\backslash[0,1]$,
>(f) the semidisk $\{|z|<1, \operatorname{Im}(z)\geq 0\}$,
>(g) the complex plane $\mathbb{C}$.

Open: (a)(c)(e)(g)
Closed: (b)(g)![[Pasted image 20251017114611.png]]
___
### [GAM01] II.1.16
>[!problem]
>Show that the slit plane $\mathbb{C}\backslash(-\infty,0]$ is star-shaped but not convex. Show that the slit plane $\mathbb{C}\backslash[-1,1]$ is not star-shaped. Show that a punctured disk is not star-shaped.

For any $x\in\mathbb{C}\backslash(-\infty,0]$, the segment connecting $x$ and $1$ lies in  $x\in\mathbb{C}\backslash(-\infty,0]$ , thus  $\mathbb{C}\backslash(-\infty,0]$ is star-shaped.
The segment $[-1-i,-1+i]$ goes through $-1\notin\mathbb{C}\backslash(-\infty,0]$, thus $\mathbb{C}\backslash(-\infty,0]$ is not convex.

For any $x\in\mathbb{C}\backslash[-1,1]$, we have $-x\in\mathbb{C}\backslash[-1,1]$.
The segment connecting $x$ and $-x$ goes through $0\notin\mathbb{C}\backslash[-1,1]$, thus $\mathbb{C}\backslash[-1,1]$ is not star-shaped.

$W.L.O.G$, let the punctured disk be $D=\{z:0<|z|<R\}$.
The segment connecting $x$ and $-x$ goes through $0\notin D$, thus $D$ is not star-shaped.
___
### [GAM01] II.2.3
>[!problem]
>Show from the definition that the functions $x=\operatorname{Re}z$ and $y=\operatorname{Im}z$ are not complex differentiable at any point.

For any $z_0\in\mathbb{C},x,y\in\mathbb{R}$, $$\lim_{x\to0}\frac{\operatorname{Re}(z_0+x)-\operatorname{Re}(z_0)}{x}=1,\lim_{y\to0}\frac{\operatorname{Re}(z_0+iy)-\operatorname{Re}(z_0)}{iy}=0,1\neq0,$$thus $\operatorname{Re}z$ complex differentiable at any point.
$$\lim_{x\to0}\frac{\operatorname{Im}(z_0+x)-\operatorname{Im}(z_0)}{x}=0,\lim_{y\to0}\frac{\operatorname{Im}(z_0+iy)-\operatorname{Im}(z_0)}{iy}=1,0\neq1,$$thus $\operatorname{Im}z$ complex differentiable at any point.
___
### [GAM01] II.2.4
>[!problem]
>Suppose $f(z)=az^{2}+bz\bar{z}+c\bar{z}^{2}$, where $a,b,$ and $c$ are fixed complex numbers. By differentiating $f(z)$ by hand, show that $f(z)$ is complex differentiable at $z$ if and only if $bz+2c\bar{z}=0$. Where is $f(z)$ analytic?
  
Difference quotient: $$\frac{f(z+h)-f(z)}{h} = a(2z +h)+ b\left(z\frac{\bar{h}}{h} + \bar{z}+\bar{h}\right) + c\left(2\bar{z}\frac{\bar{h}}{h}+\frac{\bar{h}^2}{h}\right).$$
When $h\to 0$, limit exists iff coefficient of $\bar{h}/h$ vanishes, $i.e.bz + 2c\bar{z} = 0$.  
Analytic only if $b=0, c=0$ ($f(z)=az^2$ is analytic on $\mathbb{C}$).
___
### [GAM01] II.2.5
>[!problem]
>Show that if $f$ is analytic on D, then $g(z)=\overline{f(\bar{z})}$ is analytic on the reflected domain $D^{*}=\{\bar{z}:z\in D\}$, and $g^{\prime}(z)=\overline{f^{\prime}(\bar{z})}$.

Let $U(x,y)=u(x,-y)$, $V(x,y)=-v(x,-y)$.
$u,v$ real differentiable $\Rightarrow$ $U,V$ real differentiable.

$f$ analytic, thus by C-R$$\frac{\partial u}{\partial x}(x,y)=\frac{\partial v}{\partial y}(x,y),\frac{\partial v}{\partial x}(x,y)=-\frac{\partial u}{\partial y}(x,y).$$
Check C-R of $U,V$:
$$\frac{\partial U}{\partial x}(x,y)=\frac{\partial u}{\partial x}(x,-y), \frac{\partial V}{\partial y}(x,y)=\frac{\partial v}{\partial y}(x,-y)\Rightarrow\frac{\partial U}{\partial x}(x,y)=\frac{\partial V}{\partial y}(x,y),$$ $$\frac{\partial V}{\partial x}(x,y)=-\frac{\partial v}{\partial x}(x,-y), \frac{\partial U}{\partial y}(x,y)=-\frac{\partial u}{\partial y}(x,-y)\Rightarrow\frac{\partial V}{\partial x}(x,y)=-\frac{\partial U}{\partial y}(x,y).$$
So $g$ analytic on $D^*$.

For derivative:
$$
g'(z)=\lim_{h\to0}\frac{\overline{f(\bar{z}+\bar{h})}-\overline{f(\bar{z})}}{h}
=\overline{\lim_{h\to0}\frac{f(\bar{z}+\bar{h})-f(\bar{z})}{\bar{h}}}
=\overline{f'(\bar{z})}.
$$
___
### [GAM01] II.3.2
>[!problem]
>Show that $u=\sin x\cosh y$ and $v=\cos x\cosh y$ satisfy the Cauchy-Riemann equations. Do you recognize the analytic function $f=u+iv$? (Determine its complex form.)

$u,v$ are real differentiable.
Compute partial derivatives:  
$$u_x = \cos x \sinh y,\quad u_y = \sin x \cosh y$$
$$v_x = -\sin x \cosh y,\quad v_y = \cos x \sinh y$$
Thus $u_x =  v_y,u_y  = -v_x$, satisfies C-R equation.
Therefore $f = u + iv$ is analytic.
Since $\cos z = \cos x \cosh y - i \sin x \sinh y$, we have $f(z) = -i\cos z$.
___
### [GAM01] II.3.3
>[!problem]
>Show that if $f$ and $\overline{f}$ are both analytic on a domain $D$, then $f$ is constant.

We already know that an analytic and real-valued function is constant
Since $f$ and $\overline{f}$ are analytic on $D$, we have:  
$$\frac{1}{2}(f + \overline{f}) = \operatorname{Re}(f) \quad \text{analytic and real-valued} \Rightarrow \operatorname{Re}(f) \text{ is constant,}$$
$$\frac{1}{2i}(f - \overline{f}) = \operatorname{Im}(f) \quad \text{analytic and real-valued} \Rightarrow \operatorname{Im}(f)\text{ is constant,}$$
Therefore, $f$ is constant.
___
### [GAM01] II.3.4
>[!problem]
Show that if $f$ is analytic on a domain $D$, and if $|f|$ is constant, then $f$ is constant.  

Let $|f| = c$ constant on $D$.  
If $c = 0$: $f \equiv 0$ constant.  
If $c > 0$: $\overline{f} = c^2/f$ is analytic (since $f \neq 0$).  
Then by the previous problem, $f$ constant.
___
### [SL98] 1.4.5
>[!problem] 习题
>设无穷三角阵 $$\begin{matrix}
>a_{11}&      &&      \\
>a_{21}&a_{22}&&      \\
>a_{31}&a_{32}&a_{33}&\\
>\vdots & \vdots  & \vdots & \ddots \\
>\end{matrix}$$
>满足
>(1) 对任意固定的$k,\lim_{n\to\infty}a_{nk}=a_{k}$存在;
>(2) $\lim_{n\to\infty}\sum_{k=1}^{n}a_{nk}$存在;
>(3) $\sum_{k=1}^{n}|a_{nk}|\le M<\infty,\forall n\in\mathbb{N}$.
>证明：若复数列$\{z_{n}\}$收敛, 则$\lim_{n\to\infty}\sum_{k=1}^{n}a_{nk}z_{k}$存在.

设 $w_k = z_k - z$, 则 $w_k \to 0$. 分解:
$$
\sum_{k=1}^n a_{nk} z_k = z S_n + T_n,
$$
其中 $S_n = \sum_{k=1}^n a_{nk}$, $T_n = \sum_{k=1}^n a_{nk} w_k$.

由条件(2), $S_n \to S$, 故第一项收敛. 只需证 $T_n$ 收敛.

对任意 $\epsilon > 0$, 取 $N$ 使得当 $k > N$ 时 $|w_k| < \epsilon$. 对任意 $n, m > N$, 将 $T_n - T_m$ 拆分为: $$
T_n - T_m = \sum_{k=1}^N (a_{nk} - a_{mk}) w_k + \sum_{k=N+1}^n a_{nk} w_k - \sum_{k=N+1}^m a_{mk} w_k.$$
由条件(1), 第一项可小于 $\epsilon$; 由条件(3), 后两项各 $\le \epsilon M$. 于是
$$
|T_n - T_m| < \epsilon(1 + 2M),
$$
故 $T_n$ 收敛.
___
### [SL98] 2.4.26
>[!problem] 习题
>设$D$是$z$平面上去掉线段$[-1,i]$, $[1,i]$和射线$z=it(1\leq t<\infty)$后所得的域, 证明函数$\mathrm{Log}(1-z^{2})$能在$D$上分出单值全纯分支. 设$f$是满足$f(0)=0$的那个分支, 试计算$f(2)$的值.

先证明 $\operatorname{Log}(1-z)$ 在 $D$ 上能分出单值全纯分支:
设 $1-z=re^{i\theta}$, 其中 $$r=|1-z|, \theta \in
\begin{cases}
(-\frac{13}{4}\pi,\frac{3}{4}\pi)&,  |1-z|\leq\sqrt{2},\\
(\arcsin{\frac{1}{|1-z|}}-\frac{3\pi}{2},\arcsin{\frac{1}{|1-z|}}+\frac{\pi}{2})&,  |1-z|>\sqrt{2}.\\
\end{cases}$$

定义 $\operatorname{Log}(1-z)=\ln r +i\theta$, 则其为单值分支.
记 $z=x+iy,\operatorname{Log}(1-z)=u+iv$, 则
$$u=\frac{1}{2}\ln((x-1)^2+y^2),v=\arctan{\frac{-y}{1-x}}+C(x,y),$$
其中 $C(x,y)$ 在 $D$ 上任意一点的某个邻域中是某个常数 ($\pi$ 的某个整数倍).
$u,v$ 都是实可微函数, 且$$\frac{\partial u}{\partial x}=\frac{\partial v}{\partial y}=\frac{x-1}{(x-1)^2+y^2},\frac{\partial v}{\partial x}=-\frac{\partial u}{\partial y}=\frac{-y}{(x-1)^2+y^2}.$$
故 $\operatorname{Log}(1-z)$ 全纯, 其为单值全纯分支.
同理, $\operatorname{Log}(1+z)$ 在 $D$ 上能分出单值全纯分支.
令 $\operatorname{Log}(1-z^2)=\operatorname{Log}(1-z)+\operatorname{Log}(1+z)$ 即可定义 $\operatorname{Log}(1-z^2)$ 的单值全纯分支.
下计算是满足$f(0)=0$的那个分支下的 $f(2)$ :
$\operatorname{Log}(1)=0\Rightarrow\operatorname{Log}(1+2)=\ln 3,\operatorname{Log}(1-2)=(\ln 1)-\pi=-\pi,$
故 $\operatorname{Log}(1-2^2)=\ln 3-\pi$, 即 $f(2)=\ln 3-\pi$.
___
>[!problem]
>Let $D\subset \mathbb{C}$ be a nonempty open subset. Suppose $z_{0}\in D$. Let $S\subset D$ be the subset consisting of point $z\in D$ which can be joined to $z_{0}$ by broken lines in $D$. Show that both $S$ and $D\setminus S$ are open in $\mathbb{C}$.

For any $z_1\in D$, let $B(z_1,r)\supseteq D$ be a neighborhood of $z_1$ in $D$.
For any $z_2\in B(z_1,r)$, the segment connecting $z_1$ and $z_2$ is contained in $B(z_1,r)$, thus in $D$.
Therefore, $z_1$ can be joined to $z_{0}$ by broken lines in $D$ if and if only $z_1$ can be joined to $z_{0}$ by broken lines in $D$.
This is to say, $z_1\in S\iff z_2\in S, i.e.$ for any $z_1\in S \text{ (or }D\setminus S$), there exists a neighborhood of $z_1$ contained in $S \text{ (or }D\setminus S$).
Hence, both $S$ and $D\setminus S$ are open in $\mathbb{C}$.
___
>[!problem]
>Let $D\subset \mathbb{C}$ be a nonempty open subset. Let $\gamma:[a,b]\to D$ be a continuous path.
>(a) Show that there exist a partition $$a=a_{0}<a_{1}<\cdots<a_{n}=b$$ and a number $r>0$ such that the open disk $B(\gamma(a_{i}),r)\subset D$ ($0\leq i\leq n$) and $$\gamma([a_{j},a_{j+1}])\subset B(\gamma(a_{j}),r)\cap B(\gamma(a_{j+1}),r)$$ for $0\leq j<n$.
>(b) Use (a) to prove the following claim: suppose two points $z_{0},z_{1}\in D$ can be joined by a continuous curve $\gamma:[0,1]\to D$ then they can also be joined by broken lines in D.
#### (a)
$\gamma$ and $\partial D$ are compact, so $\gamma\times\partial D$ is compact.
Let $$d(x,y)=|x-y|,x\in\gamma,y\in\partial D.$$
Since $d(x,y)$ is continuous on $\gamma\times\partial D$ and $\gamma\times\partial D$ is compact, $d(x,y)$ can attain its minimum value.
However, $\gamma\cap\partial D=\varnothing$ (since $D$ is open), thus $\min d(x,y)>0$.
Let $r=1/2\min d(x,y)$, then for any $t \in [a,b]$, we have $B(\gamma(t), r) \subset D$.
Now, since $\gamma$ is uniformly continuous on $[a,b]$, there exists $\delta > 0$ such that for all $s, t \in [a,b]$ with $|s - t| < \delta$, we have $|\gamma(s) - \gamma(t)| < r$.
Choose a partition $a = a_0 < a_1 < \cdots < a_n = b$ such that $|a_{j+1} - a_j| < \delta$ for all $j$. Then for any $t \in [a_j, a_{j+1}]$, we have:
- $|\gamma(t) - \gamma(a_j)| < r$ (so $\gamma(t) \in B(\gamma(a_j), r)$),
- $|\gamma(t) - \gamma(a_{j+1})| \le |\gamma(t) - \gamma(a_j)| + |\gamma(a_j) - \gamma(a_{j+1})| < r + r = 2r = r'$ (ensuring $\gamma(t) \in B(\gamma(a_{j+1}), r)$ since $r' > r$).
Thus, $\gamma([a_j, a_{j+1}]) \subset B(\gamma(a_j), r) \cap B(\gamma(a_{j+1}), r)$.
#### (b)
Given $\gamma: [0,1] \to D$ with $\gamma(0)=z_0$ and $\gamma(1)=z_1$, apply part (a) to obtain a partition $0=t_0 < t_1 < \cdots < t_n=1$ and $r>0$ such that:
$$
\gamma([t_j, t_{j+1}]) \subset B(\gamma(t_j), r) \cap B(\gamma(t_{j+1}), r) \subset D.
$$
Since both $\gamma(t_j)$ and $\gamma(t_{j+1})$ lie in the disk $B(\gamma(t_j), r)$, the straight line segment connecting them is entirely contained in this disk, and hence in $D$.
Therefore, the polygonal line connecting the points $z_0 = \gamma(t_0), \gamma(t_1), \dots, \gamma(t_n) = z_1$ is a broken line in $D$ joining $z_0$ to $z_1$.