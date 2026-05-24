___

> [!problem] [COX] 1.2.4
> We say that a cubic $x^3+bx^2+cx+d$ has a multiple root if it can be written as $(x-r_1)^2(x-r_2)$.
> Prove that $x^3+bx^2+cx+d$ has a multiple root if and only if its discriminant is zero.

**Proof:**
Let the cubic be $p(x)=x^3+bx^2+cx+d$, and let $r_1,r_2,r_3$ be its (complex) roots, counting multiplicities. The discriminant is $\Delta=\prod_{i<j}(r_i-r_j)^2$.  

If $p$ has a multiple root, then two roots coincide, say $r_1=r_2$. Then $r_1-r_2=0$, so $\Delta=0$.  

Conversely, if $\Delta=0$, then $\prod_{i<j}(r_i-r_j)^2=0$, so at least one factor $r_i-r_j=0$. Hence $p$ has a multiple root.