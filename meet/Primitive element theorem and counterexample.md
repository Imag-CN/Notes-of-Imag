---
tags:
  - 本原元
  - 伽罗瓦理论
  - 单扩张
  - 可分扩张
  - 正规扩张
---

>[!problem] Primitive Element Theorem
>Let $E/F$ be a finite field extension. The following are equivalent:
>(1) $E/F$ is a **simple extension**, i.e. there exists $\alpha \in E$ such that $E = F(\alpha)$. Such an $\alpha$ is called a **primitive element**.
>(2) There are only finitely many** intermediate fields **$K$ with $F \subseteq K \subseteq E$.
Moreover, if $E/F$ is **separable**, then these conditions hold.

___
### 1. (1) $\Rightarrow$ (2)
Assume $E = F(\alpha)$.
Let $m(x) \in F[x]$ be the minimal polynomial of $\alpha$ over $F$.
For any intermediate field $F \subseteq K \subseteq E$, let $m_K(x) \in K[x]$ be the minimal polynomial of $\alpha$ over $K$, then $m_K(x) \mid m(x)$ in $E[x]$.

Define a map:
$$\phi: \{\text{Intermediate fields } K\} \to \{\text{Monic divisors of } m(x) \text{ in } E[x]\}$$
by $\phi(K) = m_K(x)$.

Denote $m_K(x)$ as $x^d+a_{d-1}x^{d-1}+\cdots+a_0$, let $K_0=F(a_{d-1},\cdots,a_0)$, then $K_0 \subseteq K$.
Since $E=K(\alpha)=K_0(\alpha)$ and $m_K(x)$ is the minimal polynomial of $\alpha$ in both $K$ and $K_0$, we have $[E:K]=[E:K_0]$.
Since $[E:F]= [E:K][K:F]=[E:K_0][K_0:F]$, we have $[K:F]=[K_0:F]$.
On the other hand, $K_0\subseteq K$, so $K_0=K$.
This guarantees that $\phi (K)$ is injective.
Since $m(x)$ has only finitely many monic divisors in $E[x]$, there are only finitely many intermediate fields.
___
### 2. (2) $\Rightarrow$ (1)

#### Case 1: $F$ is finite.
Then $E$ is finite. The multiplicative group $E^\times$ is cyclic. Let $\alpha$ be a generator. Then $E = F(\alpha)$.
#### Case 2: $F$ is infinite.
Since $E/F$ is finite, we can write $E = F(\beta_1, \dots, \beta_m)$. 
By induction, it suffices to show: If $E = F(\alpha, \beta)$ and there are finitely many intermediate fields, then $E/F$ is simple.
Consider the fields $K_c = F(\alpha + c\beta)$ for $c \in F$. 
Since $F$ is infinite and there are only finitely many intermediate fields, by the pigeonhole principle, there exist distinct $c, d \in F$ such that $K_c = K_d$.
Let $\gamma = \alpha + c\beta$. Then $\alpha + d\beta \in K_c$. Subtracting, we get:
$$(c - d)\beta = (\alpha + c\beta) - (\alpha + d\beta) \in K_c$$
Since $c \neq d$, $c-d$ is invertible, so $\beta \in K_c,\alpha = \gamma - c\beta \in K_c$.
Hence $F(\alpha, \beta) \subseteq K_c \subseteq F(\alpha, \beta)$, so $E = F(\gamma)$.

---

### 3. Separable extension ⇒ (2) (Steinitz Theorem)

Assume $E/F$ is finite and separable.
Let $L$ be the normal closure of $E/F$, then $L/F$ is finite Galois.
By the Fundamental Theorem of Galois Theory, the intermediate fields $F \subseteq K \subseteq E$ correspond to subgroups of $\text{Gal}(L/F)$ containing $\text{Gal}(L/E)$.
Since $\text{Gal}(L/F)$ is finite, it has finitely many subgroups.
Hence there are finitely many intermediate fields between $F$ and $E$.

---

### 4. Example of the theorem

Let $F = \mathbb{Q}$, $E = \mathbb{Q}(\sqrt{2}, \sqrt{3})$. This is separable since $\text{char}(\mathbb{Q}) = 0$. The theorem guarantees a primitive element. In fact, $\gamma = \sqrt{2} + \sqrt{3}$ is one.
___
### 5. Counterexample showing (1)(2) $\not\Rightarrow$ separable
Let $F = \mathbb{F}_p(t)$, $E = F(t^{1/p})$.
Then $x^{1/p}$ is a primitive element.
This extension is inseparable because the minimal polynomial of $t^{1/p}$ over $F$ is $x^p - t$, which has derivative $0$ in characteristic $p$.
___
### 6. Counterexample in Inseparable Case
Let $F = \mathbb{F}_p(u, v)$, $E = F(u^{1/p}, v^{1/p})$, then $[E:F] = p^2$.
The reason why this extension is inseparable is the same as the last counterexample.
For any $\theta \in E$, $\theta^p \in F$, so $[F(\theta):F] \leq p$.
Hence no primitive element exists.
