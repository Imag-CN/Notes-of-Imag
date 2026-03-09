___

>[!problem] Problem 1
>Denote $a_n$ to be the number of subgroups of the symmetric group $S_n$. Write computer programs to find values of $a_n$ until $n$ is so large that the program no longer stops. Give estimates of $a_n$ when $n$ tends to infinity.

**Mathematica code:**
```mathematica
>SubgroupsOfSn[n_] := 
 Module[{elements, id, mul, inv, subgrps, stack, closure, canonical, 
   getClosure, getCanonical, isSubgroup, subgrpSet, count, g, h, 
   newSet},(*1. 生成 S_n 的所有元素*)elements = Permutations[Range[n]];
  id = Range[n];(*2. 群乘法函数*)mul[p1_, p2_] := Permute[p1, p2];
  (*3. 逆元素函数*)inv[p_] := Ordering[p];
  (*4. 计算集合的闭包*)
  getClosure[set_] := 
   Module[{closed = set, oldSize = 0, newSize = Length[set], prod}, While[oldSize != newSize, oldSize = newSize;
   closed = Union[closed, Flatten[Table[mul[closed[[i]], closed[[j]]], {i, newSize}, {j, newSize}], 1], inv /@ closed]; newSize = Length[closed];]; closed];
  (*5. 规范表示：将子群元素排序后转换为字符串，用于去重*)
  getCanonical[set_] := ToString[Sort[set]];
  (*6. 初始化*)subgrpSet = <||>; stack = {{id}}; count = 0;
  (*7. 主循环：深度优先搜索*)While[Length[stack] > 0, current = Last[stack];
   stack = Most[stack];
   closure = getClosure[current];
   canon = getCanonical[closure];
   If[! KeyExistsQ[subgrpSet, canon], subgrpSet[canon] = True; count++; For[i = 1, i <= Length[elements], i++, g = elements[[i]]; If[! MemberQ[closure, g, 1], newSet = Union[closure, {g}]; stack = Append[stack, newSet];]]]];
  count]
Print[subgrpCount]
```

**Results:** $a_{1}=1,a_{2}=2,a_{3}=6,a_{4}=30,a_{5}=156$.
**Estimate:** $2^n\leq a_{n}\leq 2^{n!-1}$.
___

>[!problem] Problem 2
>Try to find the definition of topological groups. A topological group is both a topological space and a group, and the topological structure and the group structure are compatible.

**Answer:** A topological group is a group endowed with topology such that multiplication and taking inverse are continuous maps.
___

>[!problem] Problem 3
>Write the quaternion group in matrices over the real numbers.

**Answer:**
$$
1=\begin{pmatrix}
1&0&0&0 \\
0&1&0&0 \\
0&0&1&0 \\
0&0&0&1
\end{pmatrix},
i=\begin{pmatrix}
0&-1&0&0 \\
1&0&0&0 \\
0&0&0&-1 \\
0&0&1&0
\end{pmatrix},
$$
$$
j=\begin{pmatrix}
0&0&-1&0 \\
0&0&0&-1 \\
1&0&0&0 \\
0&1&0&0
\end{pmatrix},
k=\begin{pmatrix}
0&0&0&-1 \\
0&0&1&0 \\
0&-1&0&0 \\
1&0&0&0
\end{pmatrix}.
$$
___

>[!problem] Problem 4
>Classify groups of order $6$.

**Answer:** $C_{6}$ and $S_{3}$. (Consider order of group elements.)
___

>[!problem] Problem 5
>Let $\pi(x)$ be the number of prime numbers less than $x$. Write computer programs to find the shape of the function $\pi(x)$.

**Mathematica code:**
```mathematica
Plot[{PrimePi[x], x/Log[x]}, {x, 2, 200},
 PlotLegends -> {"\[Pi](x)", "x/log(x)"}]
```

**Graph:**
![[Pasted image 20260309212035.png]]
