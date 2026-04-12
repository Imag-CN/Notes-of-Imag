___

>[!problem] Problem 1
>Consider the symmetric group $S_{n}$.
>(i) Compute the cardinality of each conjugacy class of $S_{n}$ for small $n$.
>(ii) Conjugation gives a left action of $S_{n}$ on itself, and each orbit corresponds to a conjugacy class. Compute the cardinality of stabilizers for small $n$.
>(iii) Check the counting formula for small $n$.

**Proof:**
For $n=3$:
*   **Conjugacy Classes & Sizes:**
    1.  Type (1)(2)(3): $\{(1)\}$, size $= 1$.
    2.  Type (ab)(c): $\{(12),\ (13),\ (23)\}$, size $= 3$.
    3.  Type (abc): $\{(123),\ (132)\}$, size $= 2$.
*   **Stabilizer (Centralizer) Sizes:**
    1.  For identity: $|C_{S_3}((1))| = |S_3| = 6$.
    2.  For a transposition, e.g., (12): $|C_{S_3}((12))| = 2$ $\{e,\ (12)\}$.
    3.  For a 3-cycle, e.g., (123): $|C_{S_3}((123))| = 3$ $\{e,\ (123),\ (132)\}$.
*   **Check Counting Formula $|\text{Orbit}| = |G| / |\text{Stab}|$:**
    $1 = 6/6$ , $3 = 6/2$ , $2 = 6/3$ .

---
For $n=4$:
*   **Conjugacy Classes & Sizes:**
    1.  (1)(2)(3)(4): size $= 1$.
    2.  (ab)(c)(d): size $=4! / (2^1\cdot1! \cdot 1^2\cdot2!) = 6$.
    3.  (ab)(cd): size $=4! / (2^2\cdot2!) = 3$.
    4.  (abc)(d): size $=4! / (3^1\cdot1! \cdot 1^1\cdot1!) = 8$.
    5.  (abcd): size $=4! / (4^1\cdot1!) = 6$.
*   **Stabilizer (Centralizer) Sizes:** $|C_{S_n}(g)| = \prod (i^{m_i} m_i!)$
    1.  For identity: $1^4 \cdot 4! = 24$.
    2.  For (ab)(c)(d): $2^1\cdot1! \cdot 1^2\cdot2! = 4$.
    3.  For (ab)(cd): $2^2\cdot2! = 8$.
    4.  For (abc)(d): $3^1\cdot1! \cdot 1^1\cdot1! = 3$.
    5.  For (abcd): $4^1\cdot1! = 4$.
*   **Check Counting Formula:**
    $1=24/24$, $6=24/4$, $3=24/8$, $8=24/3$, $6=24/4$.
___

>[!problem] Problem 2
>Suppose we have a pool of balls containing:  
>(i) $n$ identical white balls.  
>(ii) $n$ identical white balls and $n$ identical black balls.  
>(iii) $n$ identical white balls and $2n$ identical black balls.  
>Count how many essentially different permutations are there for each case. You can first express the result as a formula concerning groups.

**Proof:**
**(i)** The number of orbits of the conjugation action of $S_{n}$ on $S_{n}$.
**(ii)** The number of orbits of the conjugation action of $S_{n}\times S_{n}\leq S_{2n}$ (i.e. the permutations send white balls to white balls and black balls to black balls) on $S_{2n}$.
**(iii)** The number of orbits of the conjugation action of $S_{n}\times S_{2n}\leq S_{3n}$ (i.e. the permutations send white balls to white balls and black balls to black balls) on $S_{2n}$.
___

>[!problem] Problem 3
>Jordan normal forms give representatives of conjugacy classes of $M_{n\times n}(\mathbb{C})$. We equip $M_{n\times n}(\mathbb{C})$ with the standard topology by identifying it with $\mathbb{C}^{n^{2}}$.
>(i) Prove that each conjugacy class of $M_{n\times n}(\mathbb{C})$ is locally closed, i.e., is a closed subset of an open subset of $M_{n\times n}(\mathbb{C})$.
>(ii) Find conjugacy classes of $M_{n\times n}(\mathbb{C})$ which are closed.
>(iii) Find conjugacy classes of $M_{n\times n}(\mathbb{C})$ which are open.
>(iv) Prove that each conjugacy class of $M_{n\times n}(\mathbb{C})$ is a manifold. Find its dimension.

**Proof:**
(i) Let $G=\operatorname{GL}_n(\mathbb{C})$ act on $X=M_{n\times n}(\mathbb{C})$ by conjugation. The map $f_A:g\mapsto gAg^{-1}$ is a smooth morphism. Its image $\mathcal{O}_A$ is locally closed because it is a constructible set in the Zariski topology (Chevalley) and an orbit of a Lie group action in the classical topology. Equivalently, $\mathcal{O}_A$ is the intersection of the closed set defined by the characteristic polynomial of $A$ with the open set where the minimal polynomial equals the characteristic polynomial.

(ii) A conjugacy class is closed iff it consists of semisimple (diagonalizable) matrices. In the Jordan – Chevalley decomposition $A = A_s + A_n$, the orbit of $A$ contains the orbit of $A_s$ in its closure; if $A_n\neq0$ the orbit is not closed. Closed classes are those of diagonalizable matrices with a given eigenvalue spectrum.

(iii) A conjugacy class is open iff it consists of matrices with $n$ distinct eigenvalues. Such matrices form a Zariski‑open dense set (complement of the discriminant), and two matrices with the same $n$ distinct eigenvalues are conjugate. Hence the class is the whole connected component of matrices with that characteristic polynomial, which is open.

(iv) $\mathcal{O}_A$ is the image of the smooth map $f_A$, so it is an immersed submanifold. Its dimension equals
$$
\dim\mathcal{O}_A = n^2 - \dim\mathfrak{z}(A),
$$
where $\mathfrak{z}(A)$ is the centralizer Lie algebra of $A$. If $A$ has Jordan blocks of sizes $m_1,\dots,m_k$, then
$$
\dim\mathfrak{z}(A)=\sum_{i=1}^k m_i^2,

$$
so
$$
\dim\mathcal{O}_A = n^2 - \sum_{i=1}^k m_i^2.
$$
___

>[!problem] Problem 4
>The counting formula expresses the relation between the group, the orbit and the stabilizer in terms of their cardinalities. For continuous groups with infinitely elements, try to find a similar formular involving dimensions instead of cardinalities. Check the formula using the above problem, in which the group $GL_n(\mathbb{C})$ acts on itself via conjugation, and you have already computed the dimension of the orbits.

**Proof:**
For a Lie group $G$ acting smoothly on a manifold $M$, the dimension version of the orbit-stabilizer theorem holds:
$$
\dim G = \dim \mathcal{O}_x + \dim G_x,

$$
where $\mathcal{O}_x$ is the orbit of $x$ and $G_x$ is its stabilizer.

Check for $G = \operatorname{GL}_n(\mathbb{C})$ acting on itself by conjugation:
1. $\dim G = n^2$.
2. For a matrix $A$ with Jordan blocks of sizes $m_1,\dots,m_k$, we computed in Problem 3:
   $$ \dim \mathcal{O}_A = n^2 - \sum_{i=1}^k m_i^2. $$
3. The stabilizer $G_A$ (centralizer of $A$) is a Lie subgroup whose dimension equals $\dim G_A = \sum_{i=1}^k m_i^2$.
4. Substituting:
$$
\dim G_A + \dim \mathcal{O}_A = \bigl(\sum m_i^2\bigr) + \bigl(n^2 - \sum m_i^2\bigr) = n^2 = \dim G.
$$
The formula holds for every $A$.