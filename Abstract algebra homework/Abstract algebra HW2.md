___

>[!problem] Problem 1
>Denote $a_n$ to be the number of subgroups of the symmetric group $S_n$. Write computer programs to find values of $a_n$ until $n$ is so large that the program no longer stops. Give estimates of $a_n$ when $n$ tends to infinity.

>[!note] Mathematica code:
>```mathematica
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


