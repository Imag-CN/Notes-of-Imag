___

>[!problem] Exercise 1.1.2
>Classify $2$-dimensional $\mathbb{R}$-algebras. Here $\mathbb{R}$ is the field of real numbers.

**Proof:**
A $2$-dimensional $\mathbb{R}$-algebra $A$ is isomorphic to $\mathbb{R}[x]/(p(x))$ for some $p(x)\in \mathbb{R}[x]$ of degree $2$. 

Therefore:
 - If $p(x)$ has two multiple roots, then $A \cong \mathbb{R}[x]/(x^{2})$;
 - If $p(x)$ has two distinct real roots, then $A\cong\mathbb{R}\oplus \mathbb{R}$;
 - If $p(x)$ is irreducible in $\mathbb{R}$, then $A\cong\mathbb{C}$.
___

>[!problem] Exercise 1.1.6
>Suppose $k$ is algebraically closed. Is it true that every finite $k$-algebra is isomorphic to $k \oplus \cdots \oplus k$?

**Proof:**
No. Consider $A=k[x] / (x^{2})$, then $x^{2}=0$ but $x\neq 0$ in $A$. However, for $a\in k \oplus \cdots \oplus k$, $a^{2}=0\iff a=0$, thus $A$ is not isomorphic to $k \oplus \cdots \oplus k$.
___

>[!problem] Exercise 1.2.1
>Let $A, B$ be $k$-algebras. Prove that the multiplication
>$$
>(A \otimes_k B) \times (A \otimes_k B) \to A \otimes_k B
>$$
>$$
>(a \otimes_k b,\, a' \otimes_k b') \mapsto aa' \otimes_k bb'
>$$
>is well-defined.

**Proof:**
This can be induced by
$$
(A \otimes_k B) \otimes_{k} (A \otimes_k B) \cong A \otimes_k B \otimes_{k} A \otimes_k B \to A \otimes_k B
$$
which is define by applying universal property to $A \times B \times A \times B \overset{ (a,b,a',b')\mapsto aa' \otimes_k bb' }{ \longrightarrow } A \otimes_k B$.
___

>[!problem] Exercise 1.2.3
>Find an explicit isomorphism
>$$
>\mathbb{C} \otimes_{\mathbb{R}} \mathbb{C} \xrightarrow{\sim} \mathbb{C} \oplus \mathbb{C}
>$$
>of $\mathbb{R}$-algebras.

**Proof:**
Define the $\mathbb{R}$-algebra homomorphism $\Phi: \mathbb{C} \otimes_{\mathbb{R}} \mathbb{C} \to \mathbb{C} \oplus \mathbb{C}$ on elementary tensors by
$$
\Phi(z \otimes w) = (zw, z\bar{w}),
$$
where $\bar{w}$ denotes the complex conjugate of $w$, and extend $\mathbb{R}$-linearly.

Its inverse $\Psi: \mathbb{C} \oplus \mathbb{C} \to \mathbb{C} \otimes_{\mathbb{R}} \mathbb{C}$ is given by
$$
\Psi(u, v) = \frac12 \big(1 \otimes (u+v)\big) + \frac{i}{2} \big(i \otimes (u-v)\big).
$$
Then $\Phi$ and $\Psi$ are mutually inverse $\mathbb{R}$-algebra isomorphisms.
___

>[!problem] Exercise 1.2.4
>Let $A$ be a $k$-algebra. Prove that there is a canonical isomorphism
>$$
>A \otimes_k k[x]/(f(x)) \cong A[x]/(f(x))
>$$
>of $k$-algebras.

**Proof:**
Define the $k$-algebra homomorphism
$$
\varphi: A \otimes_k k[x]/(f(x)) \longrightarrow A[x]/(f(x))
$$
on elementary tensors by $\varphi(a \otimes g(x)) = a g(x) \pmod{f(x)}$, and extend $k$-linearly.

Define $\psi: A[x]/(f(x)) \longrightarrow A \otimes_k k[x]/(f(x))$ by $\psi\bigl(\sum_i a_i x^i \bigr) = \sum_i a_i \otimes x^i$.

One checks that $\varphi$ and $\psi$ are well-defined $k$-algebra homomorphisms, and
$$
\varphi(\psi(\sum_i a_i x^i)) = \sum_i a_i x^i,\qquad
\psi(\varphi(a \otimes g)) = a \otimes g
$$
for all $a \in A$, $g \in k[x]/(f(x))$. Hence they are mutually inverse isomorphisms of $k$-algebras.