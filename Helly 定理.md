___

>[!theorem] Helly 定理 - 有限维版本
>设 $\mathcal{F}$ 是 $\mathbb{R}^d$ 中的一族凸集, 且 $\mathcal{F}$ 的任意 $d+1$ 个成员的交集都非空, 则 $\bigcap_{F \in \mathcal{F}} F \neq \varnothing$.

**证明**:
对维数 $d$ 进行归纳. 当 $d=1$ 时, 凸集即为区间, 任意两个区间交集非空, 故整体交集非空.

假设结论对 $\mathbb{R}^{d-1}$ 成立. 对每个 $i=1, \dots, d$, 考虑第 $i$ 个坐标超平面 $H_i=\{x\in\mathbb{R}^d:x_i=0\}$. 对 $F\in\mathcal{F}$, 记其在 $H_i$ 上的投影为 $F_i=\pi_i(F)$, 则 $F_i$ 为凸集.

由于 $\mathcal{F}$ 的任意 $d+1$ 个成员交集非空, 投影族 $\{F_i:F\in\mathcal{F}\}$ 也满足此性质. 由归纳假设, $\bigcap_{F\in\mathcal{F}}F_i\neq\varnothing$.

取 $x^{(i)}\in\bigcap_{F\in\mathcal{F}}F_i$, 则对每个 $F\in\mathcal{F}$, 存在 $x_F^{(i)}\in F$ 使得 $\pi_i(x_F^{(i)})=x^{(i)}$. 考虑 $\{x_F^{(i)}:i=1, \dots, d\}$ 的凸包, 该凸包含于每个 $F$, 故 $\bigcap_{F\in\mathcal{F}}F\neq\varnothing$.

>[!remark] Helly 定理 - 无限维推广
>设 $X$ 是一个线性空间, $\mathcal{F}$ 是 $X$ 中的一族凸集, 且 $\mathcal{F}$ 满足：
>1. $\mathcal{F}$ 的任意有限子族的交集都非空；
>2. $\bigcap_{F \in \mathcal{F}} \text{cl}(F) \neq \varnothing$（其中 $\text{cl}(F)$ 表示 $F$ 的闭包）.
>
>则 $\bigcap_{F \in \mathcal{F}} F \neq \varnothing$.
