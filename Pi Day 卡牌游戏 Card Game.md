___
### 游戏规则

在本次 $\pi$ Day 数学游戏摊位中,你将通过扑克牌数字与特定运算组合,挑战构造最接近圆周率 $\pi$ 的表达式.具体规则如下:

1. **牌面数字**: 使用 $4$ 张扑克牌, $A=1$, $2-10$ 为对应数字, $J=11$, $Q=12$, $K=13$. 需用尽全部 4 个数字,每个数字仅可使用一次.
2. **允许运算**:
    
    - **二元运算**:加法 `+`、乘法 `*`、乘方 `a^b`、对数 `log_a(b)
        
    - **一元运算**:取倒数 `1/x`、取相反数 `-x`.
        
    - **括号**:可自由使用以明确运算顺序.

3. **目标**:用上述数字与运算构造合法表达式,使其数值结果尽可能接近 π(≈ 3.1415926535…).
4. **注意**:本游戏**禁止**使用开方 `√`、阶乘 `!`、排列 `P(n,k)`、组合 `C(n,k)`等运算.如需开方,请通过 `a^(1/2)`实现(即用幂运算与取倒数组合).
---

### Rules for the Game

At this Pi Day math game booth, you will use playing card numbers and a specific set of operations to construct an expression that approximates the mathematical constant π as closely as possible. The full rules are:

1. **Card Values**: Use 4 playing cards, where A=1, 2-10 equal their face values, J=11, Q=12, K=13. You must use all four numbers exactly once each, but digits may be concatenated to form multi-digit numbers (e.g., 1 and 2 may become 12 or 21).

2. **Allowed Operations**:
    
    - **Binary Operations**: Addition `+`, multiplication `*`, exponentiation `a^b`, and logarithm `log_a(b)`(logarithm of b to base a).
        
    - **Unary Operations**: Reciprocal `1/x`, and negation `-x`.
        
    - **Parentheses**: May be used freely to specify order of operations.
        
    
3. **Objective**: Using the numbers and operations above, construct a valid mathematical expression whose numerical result is as close as possible to π (≈ 3.1415926535…).
    
4. **Important**: The following operations are **explicitly forbidden**: square root `√`, factorial `!`, permutation `P(n,k)`, and combination `C(n,k)`. If a square root is needed, it must be implemented as `a^(1/2)`(i.e., via exponentiation and the reciprocal operation).

$$
3,4,4,7
$$