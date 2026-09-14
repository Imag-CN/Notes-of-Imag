___

>[!problem] 1.1
> Let $L_n$ be the number of tilings of $n$ boxes arranged in a circle with dominoes and monominoes. For example $L_4 = 7$.
>
>(a) Prove that $L_n = F_{n-1} + F_{n+1}$ for $n \ge 1$.
>
>(b) Prove that $L_{m+n} = F_{m-1} L_n + F_m L_{n+1}$ for $m, n \ge 1$.
>
>(c) Prove that $F_{2n} = F_n L_n$.

**Proof:**
**(a)** Let $F_n$ be the standard Fibonacci numbers with $F_1 = F_2 = 1$ and $F_n = F_{n-1} + F_{n-2}$. Then $F_{n+1}$ counts the number of tilings of a line of $n$ boxes with dominoes and monominoes. Define $F_{0}=0$.

For a circle of $n$ boxes, consider whether boxes $n$ and $1$ are covered by a single domino:
 - If they are, remove this domino; the remaining $n-2$ boxes form a line, giving $F_{n-1}$ tilings.
 - If they are not, cut the circle between $n$ and $1$ to obtain a line of $n$ boxes, giving $F_{n+1}$ tilings.
 
Therefore, $L_n = F_{n-1} + F_{n+1}$ for $n \ge 1$.

**(b)** For a circle of $m+n$ boxes, consider whether boxes $n$ and $1$ are covered by a single domino:


**(c)** We do induction on $n$:
- If $n=1$, then $F_{2n}=F_{n}L_{n}=1$;
- Suppose $F_{2n} = F_n L_n$, then set $m=n+1$ in **(b)** gives $L_{2n+1}=F_{n}L_{n}+F_{n+1}L_{n+1}$. Substitute $L_{2n+1}=F_{2n}+F_{2n+2}$ by **(a)** and $F_{n}L_{n}=F_{2n}$ by induction hyphothesis gives $F_{2n}+F_{2n+2}=F_{2n}+F_{n+1}L_{n+1}$, thus $F_{2n+2}=F_{n+1}L_{n+1}$.

Therefore, $L_n = F_{n-1} + F_{n+1}$.