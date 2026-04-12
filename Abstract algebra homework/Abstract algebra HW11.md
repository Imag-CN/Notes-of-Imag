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

Suppose we have a collection of balls in the following scenarios.
(i) n identical white balls.
(ii) n identical white balls and n identical black balls.
(iii) n identical white balls and 2n identical black balls.
Count the number of essentially different permutations in each case. You can express the results in formulas involving groups.