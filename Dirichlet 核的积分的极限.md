___
>[!Question] 求Dirichlet 核的积分的极限
>证明下列积分的极限存在并求值.
>$$
>\lim_{n \to \infty} \int_{\delta}^{\pi} \left| \dfrac{\sin\left(\dfrac{2n+1}{2}t\right)}{\sin\left(\dfrac{1}{2}t\right)} \right|\, \mathrm{d}t
>$$
>其中 $\delta \in[0,2\pi]\setminus \{ \pi \}$.

让我们先回顾一下推广的 Riemann-Lebesgue 引理:

>[!theorem] 推广的 Riemann-Lebesgue 引理
>设 $g$ 是周期为 $T$ 的可积函数, 其均值为
>$$
>\overline{g}=\dfrac{1}{T}\int_{0}^{T}g(t)\,\mathrm{d}t,
>$$
>并且 $f \in L^{1}([a,b])$, 则
>$$
>\lim_{\lambda \rightarrow \infty} \int_{a}^{b} f(t) g(\lambda t) \, \mathrm{d}t = \overline{g} \int_{a}^{b} f(t) \, \mathrm{d}t.
>$$

应用到这个问题中, 则 $g(t)=|\sin{t}|,T=\pi,\overline{g}=\dfrac{2}{\pi},\lambda_{n}=\dfrac{2n+1}{2},f(t)=\dfrac{1}{\sin{\left( \dfrac{1}{2}t \right)}},[a,b]=[\delta,\pi]$.
因此原积分存在, 且它的值为
$$
\overline{g} \int_{\delta}^{\pi} f(t) \, \mathrm{d}t=\dfrac{2}{\pi}\int_{\delta}^{\pi} \dfrac{1}{\sin{\left( \dfrac{1}{2}t \right) }} \, \mathrm{d}t=\dfrac{2}{\pi}\cdot \left.   \left( 2\ln{\tan{\dfrac{t}{4}}} \right) \right|_{t=\delta}^{\pi}=-\dfrac{4}{\pi}\cdot\ln{\tan{\dfrac{\delta}{4}}}
$$
综上我们有结论:
$$
\lim_{n \to \infty} \int_{\delta}^{\pi} \left| \dfrac{\sin\left(\dfrac{2n+1}{2}t\right)}{\sin\left(\dfrac{1}{2}t\right)} \right|\, \mathrm{d}t=-\dfrac{4}{\pi}\cdot\ln{\tan{\dfrac{\delta}{4}}}
$$
并且当 $\delta\rightarrow\pi$ 时, 令 $h=\pi-\delta$, 则
$$
\begin{align}
\lim_{  \delta\rightarrow\pi^{-} } \dfrac{-\dfrac{4}{\pi}\cdot\ln{\tan{\dfrac{\delta}{4}}}}{\ln{\dfrac{\pi}{\delta}}}&=-\dfrac{4}{\pi}\cdot\lim_{ h \to 0 } \dfrac{\ln{\tan{(\dfrac{\pi-h}{4})}}}{\ln{(1+ \dfrac{h}{\pi-h})}} \\
&=-\dfrac{4}{\pi}\cdot\lim_{ h \to 0 } \ln{\dfrac{{1-\tan{\dfrac{h}{4}}}}{1+\tan{\dfrac{h}{4}}}}\cdot\left( \dfrac{\pi}{h} \right)  \\
&=-\dfrac{4}{\pi}\cdot\lim_{ h \to 0 } \ln{\left(  {1-\tan{\dfrac{h}{4}}} \right)}\cdot\left( \dfrac{\pi}{h} \right)  \\
&=-\dfrac{4}{\pi}\cdot\lim_{ h \to 0 } \left(  \dfrac{-h}{4} \right)\cdot\left( \dfrac{\pi}{h} \right)  \\
&=1.
\end{align}
$$
说明这个极限不仅是 $O(\ln{\dfrac{\pi}{\delta}})$ 的, 甚至在 $\delta\rightarrow\pi$ 时它与 $\ln{\dfrac{\pi}{\delta}}$ 等价.