>[!problem]
>Randomly pick a triangle $\Delta ABC$ in a region $K$: points $A$, $B$, and $C$ are independent and uniformly distributed over region $K$. $f(\Delta ABC)$ is a function with variables $x_a,y_a,x_b,y_b,x_c,y_c$. What's the expectation of $f$？


Since points $A$, $B$, and $C$ are independent and uniformly distributed over region $K$, the probability density function for each point is:

$$
p(x, y) = \frac{1}{S},
$$

where $S = \iint_K 1 \, dx \, dy$ is the area of $K$.

The joint probability density for the three points is:

$$
p(A, B, C) = \frac{1}{S^3}.
$$

The expectation of $f$ is then:

$$
\mathbb{E}[f] = \frac{1}{S^3} \iiint_{K^3} f(A, B, C) \, dA \, dB \, dC,
$$

where $dA = dx_A \, dy_A$, $dB = dx_B \, dy_B$, and $dC = dx_C \, dy_C$.

We can use mathematica to compute:

```mathematica
(* define region *)
K = Disk[{0, 0}, 1];
areaK = Area[K];

(* define f *)
(* e.g.area *)
f[{{xA_, yA_}, {xB_, yB_}, {xC_, yC_}}] := 
  Abs[(xB - xA)(yC - yA) - (xC - xA)(yB - yA)]/2;

(* compute expactation *)
expectation = NIntegrate[
  f[{{xA, yA}, {xB, yB}, {xC, yC}}] / areaK^3,
  {xA, yA} ∈ K,
  {xB, yB} ∈ K,
  {xC, yC} ∈ K,
]

```

For $f$ as area function, we have:
$$\mathbb{E}[f]=\frac{11}{144}\text{, if }K\text{ is a unit square.}$$
$$\mathbb{E}[f]=\frac{4}{\pi ^2}-\frac{1}{8}\text{, if }K\text{ is a unit disk.}$$
$$\mathbb{E}[f]=\frac{1}{12}\text{, if }K\text{ is a triangle with unit area.}$$

See [Square Triangle Picking -- from Wolfram MathWorld](https://mathworld.wolfram.com/SquareTrianglePicking.html), [Disk Triangle Picking -- from Wolfram MathWorld](https://mathworld.wolfram.com/DiskTrianglePicking.html) , and [Triangle Triangle Picking -- from Wolfram MathWorld](https://mathworld.wolfram.com/TriangleTrianglePicking.html).

$$
\lim_{ n \to \infty } \int_{\delta}^{\pi} \left| \dfrac{\sin{\dfrac{2n+1}{2}t}}{\sin{\dfrac{1}{2}t}} \right| \mathrm{d}x
$$