---
tags:
  - 分析
  - 不等式
  - 估计
  - Young不等式
  - Holder不等式
---
> [!problem] 哈代不等式
> 设$a_j\geq 0$, $j=1,2,\cdots$, 定义$$A_n=\frac{1}{n}\sum\limits_{k=1}^{n}a_k,\quad n=1,2,\cdots.$$
>证明$p>1$时$$ \sum\limits_{n=1}^{m}A_n^p\leq \left(\dfrac{p}{p-1}\right)^p\sum\limits_{n=1}^{m}a_n^p.$$

我们先证明引理：
> [!problem] 引理
> $$ \sum\limits_{n=1}^{m}A_n^p\leq \dfrac{p}{p-1}\sum\limits_{n=1}^{m}A_n^{p-1}a_n.$$

首先我们有$$\begin{align}
A_n^p - \frac{p}{p-1} A_n^{p-1} a_n &= A_n^p - \frac{p}{p-1} A_n^{p-1} \left( n A_n - (n-1) A_{n-1} \right) \\
&= A_n^p \left( 1 - \frac{n p}{p-1} \right) + \frac{(n-1) p}{p-1} A_n^{p-1} A_{n-1} \\
\text{(Young不等式)}&\leq A_n^p \left( 1 - \frac{n p}{p-1} \right) + \frac{(n-1) p}{p-1} \left( \frac{p-1}{p} A_n^p + \frac{1}{p} A_{n-1}^p \right) \\
&= A_n^p \left( 1 - \frac{n p}{p-1} \right) + (n-1) A_n^p + \frac{n-1}{p-1} A_{n-1}^p \\
&= \frac{n-1}{p-1} A_{n-1}^p - \frac{n}{p-1} A_n^p.
\end{align}$$
对不等式两边求和可得$$
 \sum\limits_{n=1}^{m}A_n^p-\dfrac{p}{p-1}\sum\limits_{n=1}^{m}A_n^{p-1}a_n\leq - \frac{n}{p-1} A_n^p\leq0.$$
 因此引理得证.
  >[!tip] 想法
 >在试验前几个$m$时, 我们发现不等式无法取等. 这可能意味着不等式要么过松(鉴于不等式较难我们认为并非如此), 要么取等条件在$m$趋于无穷时得到. 在这种情况下, 不等式通常是可以加强到在右边减去一个趋$0$的余项的, 并且通常可以加强归纳. 我们采用与加强归纳等价的方法, 即将两边的差的差分放缩到$f(n)-f(n-1)$形式来证明命题. 在实际处理过程中, 我们通过将$a_n$代换来减少变元, 并用Young不等式处理交叉项, 最终得出结论.
 >然而我们仍然不知道这个引理是如何被构造出来的.
 
 
 从引理出发, 我们有$$\begin{align}
 \sum\limits_{n=1}^{m}A_n^p &\leq \frac{p}{p-1}\sum\limits_{n=1}^{m}A_n^{p-1}a_n\\
 \text{Holder不等式}\Rightarrow \sum\limits_{n=1}^{m}A_n^p&\leq \frac{p}{p-1} \left( \sum\limits_{n=1}^{m}A_n^{p} \right)^{\frac{p-1}{p}} \left( \sum\limits_{n=1}^{m}a_n^p  \right)^{\frac{1}{p}}\\
 \text{两边同除以}\left( \sum\limits_{n=1}^{m}A_n^{p} \right)^{\frac{p-1}{p}}\Rightarrow \left( \sum\limits_{n=1}^{m}A_n^{p} \right)^{\frac{1}{p}}&\leq \frac{p}{p-1} \left( \sum\limits_{n=1}^{m}a_n^p  \right)^{\frac{1}{p}}\\
 \text{两边同时}p\text{次方}\Rightarrow \sum\limits_{n=1}^{m}A_n^p &\leq \left(\dfrac{p}{p-1}\right)^p\sum\limits_{n=1}^{m}a_n^p\\
 \end{align}.$$
 这样就证明了哈代不等式.


>[!tip] 想法与一些拓展
>依旧要处理交叉项, 但这次是交叉项的求和, 因此使用Holder不等式.
>
>$m$趋于$\infty$时不等式固然成立, 实际上趋等条件可以是$$a_k=k^{-\frac{1}{p}}.$$
>这个可以通过估阶的方式或stolz轻易验证, 且说明了$\left(\dfrac{p}{p-1}\right)^p$是最佳系数.
>另外不加证明地附哈代不等式的积分版本$$
\int_{0}^{a}\left(\frac{\int_{0}^{x} f(t)dt}{x}\right)^{p} dx\leqslant \left(\dfrac{p}{p-1}\right)^p\int_{0}^{a} f(x)^{p}dx.
$$.