___

>[!problem] Problem 1
>(i) List all subgroups of the $D_4$ and decide which ones are normal.  
>(ii) List all proper normal subgroups $N$ of $D_{15}$ and identify the quotient groups $D_{15}/N$.  
>(iii) List the subgroups of $D_6$ that do not contain $x^3$.

**Answer:**
Denote $D_{n}= \left< x,y|x^{n}=1,y^{2}=1,xy=yx^{-1} \right>$.
**(i)** Normal:
$$
\{ 1,x,x^{2},x^{4} \},\{ 1,x^{2} \},\{ 1,y,x^{2},x^{2}y \},\{ 1,xy,x^{2},x^{3}y \}.
$$
Non-normal:
$$
\{ 1,y \},\{ 1,xy \},\{ 1,x^{2}y \},\{ 1,x^3 y\}.
$$
**(ii)** List:
$$
N_{1}=\{ 1,x, \dots ,x^{14} \},D_{15}/N_{1}\simeq C_{2}.
$$
$$
N_{2}=\{ 1,x^{3}, \dots ,x^{12} \},D_{15}/N_{2}\simeq D_{3}.
$$
$$
N_{3}=\{ 1,x^{5},x^{10} \},D_{15}/N_{3}\simeq D_{5}.
$$
**(iii)** List:
$$
\{ {1,x^{2},x^{4}} \},\{ 1,y \},\{ 1,xy \},\dots\{ 1,x^{5}y \},\left< x^{2},y \right> =\{ 1,y,x^{2},x^{4},x^{2}y,x^{4}y \}, \left< x^{2},xy \right>,\dots \left< x^{2},x^{5y} \right>.
$$
___

>[!problem] Problem 2
>For $D_{10}$:
>(i) Compute the left cosets of the subgroup $H = \{1, x^5\}$.  
>(ii) Prove that $H$ is normal and $D_{10}/H$ is isomorphic to $D_5$.  
>(iii) Is $D_{10}$ isomorphic to $D_5 \times H$?

**Proof:**
**(i)** Compute:
$$
\{ 1,x^{5}\},\{ x,x^{6} \},\dots\{ x^{4},x^{9}\},\{ y,yx^{5}\},\{ yx,yx^{6}\},\dots,\{ yx^{4},yx^{9}\}.
$$
**(ii)** Normal because $xHx ^{-1}=yH y ^{-1}=H$. Seeing $\{ x,x^{6} \}$ as $x$ and $\{ y,yx^{5} \}$ as $y$ indicates that $D_{10}/H$ is isomorphic to $D_5$.
**(iii)** Yes. Because $D_{5}\simeq\{ 1,x^{2},\dots x^{8},y,yx^{2},\dots , yx^{8} \}\unlhd D_{10}$ and it has no intersection with $H$.
