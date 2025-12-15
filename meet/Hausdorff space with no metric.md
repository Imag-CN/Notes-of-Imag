---
tags:
  - 豪斯多夫
  - 分离公理
  - 度量
  - 第二可数
  - 拓扑
---

>[!example] Hausdorff space with no metric
>
$\mathbb{R}^{\mathbb{R}}$ with product topology is Hausdorff but not metrizable.
The topology basis of this space has the form$$\prod_{x\in \mathbb{R}}U_x$$
where $U_x$ is an open set in $\mathbb{R}$ and all but finitely many $U_x=\mathbb{R}$.

---
### 0. First-countability
A topological space $(X, \tau)$ is called **first-countable** if every point $p \in X$ has a **countable neighborhood basis**.

A **neighborhood basis** $\mathcal{B}_p$ at a point $p$ is a collection of neighborhoods of $p$ such that for every neighborhood $U$ of $p$, there exists some $B \in \mathcal{B}_p$ satisfying $B \subseteq U$.

By definition we can restrict every element in a neighborhood basis is a basis element. Furthermore, we can restrict $B_1 \supsetneq B_2 \supsetneq \cdots \supsetneq B_n \supsetneq \cdots$ by gradually substituting $B_{n+1}$ with $B_{n}\cap B_{n+1}$. Specifically, every neighborhood $U$ of $p$ should contain $\bigcap_{n\in\mathbb{Z}^+}B_n$.

A metric space $(X,\tau_d)$ is also first-countable because for every point $p\in X$, $B(p,n)_{n\in \mathbb{Z}^+}$ is a countable neighborhood basis of $p$.

---
### 1. Hausdorff
For any two distinct real functions $f \ne g$, $\exists x_0 \in \mathbb{R}$ where $f(x_0) \ne g(x_0)$
Take disjoint open intervals:
  $$U = (f(x_0)-\epsilon, f(x_0)+\epsilon)$$
  $$V = (g(x_0)-\epsilon, g(x_0)+\epsilon)$$
  where $\epsilon = \frac{|f(x_0)-g(x_0)|}{2}$
Their preimages:
$$\pi_{x_0}^{-1}(U) = \{ h \in \mathbb{R}^{\mathbb{R}} : h(x_0) \in U \}$$ $$\pi_{x_0}^{-1}(V) = \{ h \in \mathbb{R}^{\mathbb{R}} : h(x_0) \in V \}$$
  are disjoint open neighborhoods of $f$ and $g$.

---
### 2. Non-First-Countable
Consider the zero function $f(x)=0$.
Assume, for the sake of contradiction, that $\{B_n\}_{n\in\mathbb{N}}$ is a countable neighborhood basis of $f$ (suppose $B_n$ is an element of basis).
Then we have$$\bigcap_{n\in\mathbb{N}}B_n=\prod_{x\in \mathbb{R}}U_x$$
where there is only countably many $U_x\ne\mathbb{R}$.
Pick a $U_{x_0}=\mathbb{R}$, let $V=]-1,1[$, then $\pi_{x_0}^{-1}(V)$ is a neighborhood of $f$ but cannot  contained $\bigcap_{n\in\mathbb{N}}B_n$.
But this contradicts the fact that any neighborhood of $f$ should contain the intersection of the neighborhood basis of $f$.
Therefore, $\mathbb{R}^{\mathbb{R}}$ with product topology is non-first countable.



