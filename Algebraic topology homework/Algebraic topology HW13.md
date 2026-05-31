___

> [!problem] [HAT] 2.2.36
> Show that
> $$
> H_{i}(X \times S^{n}) \approx H_{i}(X) \oplus H_{i-n}(X)
> $$
> for all $i$ and $n$, where $H_{i} = 0$ for $i < 0$ by definition.
> Namely, show:
> $$
> H_{i}(X \times S^{n}) \approx H_{i}(X) \oplus H_{i}(X \times S^{n}, X \times \{x_0\})
> $$
> and
> $$
> H_{i}(X \times S^{n}, X \times \{x_0\}) \approx H_{i-1}(X \times S^{n-1}, X \times \{x_0\}).
> $$

**Proof:**
Let $x_0\in S^n$ be a base point.  From the long exact sequence of the pair $(X\times S^n,\;X\times\{x_0\})$ we obtain a split short exact sequence
$$
0\to H_i(X\times\{x_0\}) \xrightarrow{i_*} H_i(X\times S^n) \xrightarrow{j_*} H_i(X\times S^n,\;X\times\{x_0\}) \to 0,
$$
where the splitting is given by the retraction $r:X\times S^n\to X\times\{x_0\}$.  Hence
$$
H_i(X\times S^n) \cong H_i(X) \oplus H_i(X\times S^n,\;X\times\{x_0\}). \tag{1}
$$

Consider the decomposition $S^n = D^n_+\cup D^n_-$, where the two hemispheres overlap in a neighbourhood of the equator $S^{n-1}$.  Apply the relative Mayer–Vietoris sequence to the pair $(X\times S^n,\;X\times\{x_0\})$ with the cover
$$
A = X\times D^n_+,\qquad B = X\times D^n_-,
$$
and $A\cap B = X\times S^{n-1}$,  $A\cup B = X\times S^n$.

Since $X\times\{x_0\}$ is contained in both $A$ and $B$, we obtain a long exact sequence of triples.  Using that $(D^n_+, \{x_0\})$ and $(D^n_-, \{x_0\})$ are contractible pairs, the sequence collapses to an isomorphism
$$
H_i(X\times S^n,\;X\times\{x_0\}) \cong H_{i-1}(X\times S^{n-1},\;X\times\{x_0\}). \tag{2}
$$

Applying (2) repeatedly gives
$$
H_i(X\times S^n,\;X\times\{x_0\}) \cong H_{i-n}(X\times S^{0},\;X\times\{x_0\}),
$$
where $S^0$ consists of two points $\{p,q\}$ and we may take $x_0=p$.  
Now $(X\times S^0,\;X\times\{p\}) \cong (X,\;X)\sqcup (X,\;\varnothing)$, so
$$
H_{i-n}(X\times S^0,\;X\times\{p\}) \cong H_{i-n}(X). \tag{3}
$$
From (1), (2) and (3) we obtain
$$
H_i(X\times S^n) \cong H_i(X) \oplus H_{i-n}(X).
$$
Since $H_k=0$ for $k<0$ by definition, the second summand vanishes when $i-n<0$.
___


