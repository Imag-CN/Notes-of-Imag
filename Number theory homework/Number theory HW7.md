___

Fix an algebraic closure $\overline{\mathbb{Q}}_p$ of $\mathbb{Q}_p$, and choose a compatible system of $p$-power roots $p^{1/p},p^{1/p^2},\ldots$ in $\overline{\mathbb{Q}}_p$, so that
$$
(p^{1/p^{i+1}})^p=p^{1/p^i}\qquad(i\ge1).
$$
Similarly, choose compatible primitive $p$-power roots of unity $\zeta_p,\zeta_{p^2},\ldots$, so that $\zeta_{p^{i+1}}^p=\zeta_{p^i}$. Define
$$
\mathbb{Q}_p(p^{1/p^\infty}):=\bigcup_{i\ge1}\mathbb{Q}_p(p^{1/p^i}),\qquad
\mathbb{Q}_p(\zeta_{p^\infty}):=\bigcup_{i\ge1}\mathbb{Q}_p(\zeta_{p^i}).
$$
**[Fact]** You are encouraged to verify the following, but are welcome to take it for granted. These are infinite extensions of $\mathbb{Q}_p$ that are totally ramified, meaning that every finite subextension is totally ramified, or equivalently that their residue fields are still $\mathbb{F}_p$. Their completions
$$
\widehat{\mathbb{Q}_p(p^{1/p^\infty})},\qquad
\widehat{\mathbb{Q}_p(\zeta_{p^\infty})}
$$
are perfectoid fields.

On the other hand, the valuation on the complete discretely valued field $\mathbb{F}_p((t))$ extends uniquely to
$$
\mathbb{F}_p((t^{1/p^\infty})):=\bigcup_{i\ge1}\mathbb{F}_p((t^{1/p^i})),
$$
where $t^{1/p},t^{1/p^2},\ldots$ form a compatible system of $p$-power roots of $t$. Another way to think of $\mathbb{F}_p((t^{1/p^\infty}))$ is as the perfection of $\mathbb{F}_p((t))$, just as $\mathbb{F}_p[X^{p^{-\infty}}]$ is the perfection of $\mathbb{F}_p[X]$. The completion $\widehat{\mathbb{F}_p((t^{1/p^\infty}))}$ is also a perfectoid field, now of characteristic $p$.

You can identify the valuation rings of
$$
\mathbb{Q}_p(p^{1/p^\infty}),\qquad
\mathbb{Q}_p(\zeta_{p^\infty}),\qquad
\mathbb{F}_p((t^{1/p^\infty}))
$$
by applying [S, I, §6] to finite subextensions. The last case involves inseparable extensions, but the argument in [S, I, §6, (ii)] still applies; alternatively, compute its valuation ring directly as
$$
\bigcup_{i\ge1}\mathbb{F}_p[[t^{1/p^i}]].
$$
The valuation rings of the completions are obtained by taking closures.

>[!problem] Problem 1
> (1) Take $K:=\widehat{\mathbb{Q}_p(p^{1/p^\infty})}$. Show that, as topological fields,
> $$
> K^\flat\cong\widehat{\mathbb{F}_p((t^{1/p^\infty}))}.
> $$
>
> (2) For $K:=\widehat{\mathbb{Q}_p(\zeta_{p^\infty})}$, show that, as topological fields,
> $$
> K^\flat\cong\widehat{\mathbb{F}_p((t^{1/p^\infty}))}.
> $$
>
> (3) Show that the two fields
> $$
> \widehat{\mathbb{Q}_p(p^{1/p^\infty})},\qquad
> \widehat{\mathbb{Q}_p(\zeta_{p^\infty})}
> $$
> are not isomorphic over $\mathbb{Q}_p$.
>
> **[Remark]** Nonisomorphic perfectoid fields can have isomorphic tilts. The fields $\widehat{\mathbb{Q}_p(p^{1/p^\infty})}$ and $\widehat{\mathbb{Q}_p(\zeta_{p^\infty})}$ are different untilts of $\widehat{\mathbb{F}_p((t^{1/p^\infty}))}$.

**Proof:**
We use the previous homework's conclusions that
$$
\mathcal{O}_{K^\flat}\cong\varprojlim_{x\mapsto x^p}\mathcal{O}_K/p,
$$
and that $|x|_{K^\flat}=|x^\sharp|_K$.

Put $F=\widehat{\mathbb{F}_p((t^{1/p^\infty}))}$ and $R=\mathbb{F}_p[t^{1/p^\infty}]$. For any positive integer $e$,
$$
\mathcal{O}_F\cong\varprojlim_{x\mapsto x^p}R/(t^e).
$$
Indeed, $\mathcal{O}_F/(t^e)\cong R/(t^e)$ by density, and the map is $x\mapsto(x^{1/p^n}\bmod t^e)_{n\ge0}$. Conversely, if $(a_n)$ is a compatible sequence and $\widetilde a_n\in\mathcal{O}_F$ are lifts, then $\widetilde a_n^{p^n}$ converges: successive differences have valuation at least $ep^{n+1}$. These constructions are inverse.

**(1)** Let $A=\mathcal{O}_K$. Since $X^{p^n}-p$ is Eisenstein,
$$
\mathcal{O}_{\mathbb{Q}_p(p^{1/p^n})}=\mathbb{Z}_p[p^{1/p^n}].
$$
Completion does not change the quotient modulo $p$, so
$$
A/p\cong\varinjlim_n\mathbb{F}_p[X_n]/(X_n^{p^n})
\cong R/(t),
$$
where $X_n\mapsto t^{1/p^n}$ and the transition maps send $X_n$ to $X_{n+1}^p$. Taking inverse limits gives $\mathcal{O}_{K^\flat}\cong\mathcal{O}_F$, hence $K^\flat\cong F$.

Under this identification, $t$ corresponds to $(p,p^{1/p},p^{1/p^2},\ldots)$, whose sharp is $p$. Thus the isomorphism is topological.

**(2)** Write $\pi_n=\zeta_{p^n}-1$ and $A=\mathcal{O}_K$. The polynomial $\Phi_{p^n}(1+X)$ is Eisenstein, so
$$
\mathcal{O}_{\mathbb{Q}_p(\zeta_{p^n})}=\mathbb{Z}_p[\pi_n],
\qquad
\mathcal{O}_{\mathbb{Q}_p(\zeta_{p^n})}/p
\cong\mathbb{F}_p[X_n]/(X_n^{p^{n-1}(p-1)}).
$$
Moreover, $\pi_{n+1}^p\equiv\pi_n\pmod p$. Consequently,
$$
A/p\cong R/(t^{p-1}),
\qquad
\pi_n\longleftrightarrow t^{1/p^{n-1}}.
$$
Taking inverse limits again gives $\mathcal{O}_{K^\flat}\cong\mathcal{O}_F$ and hence $K^\flat\cong F$.

Here $t$ corresponds to $(\pi_1,\pi_2,\ldots)\bmod p$, whose tilt norm is $|\pi_1|=p^{-1/(p-1)}$. Thus this is also a topological isomorphism.

**(3)** Put $L=\bigcup_n\mathbb{Q}_p(\zeta_{p^n})$. Every element of $\widehat L$ algebraic over $\mathbb{Q}_p$ belongs to $L$: if $x$ is algebraic, choose $a\in L$ sufficiently close to $x$ and apply Krasner's lemma to obtain $\mathbb{Q}_p(x)\subseteq\mathbb{Q}_p(a)\subseteq L$.

Every finite subextension of $L/\mathbb{Q}_p$ is Galois, since $L/\mathbb{Q}_p$ is abelian.

- If $p$ is odd, $\mathbb{Q}_p(p^{1/p})/\mathbb{Q}_p$ is not Galois. Otherwise it would contain $\zeta_p$, forcing $p-1$ to divide $p$. Hence $\widehat L$ contains no root of $X^p-p$, whereas $\widehat{\mathbb{Q}_p(p^{1/p^\infty})}$ does.

- If $p=2$, use $X^4-2$ instead. The degree-four extension $E=\mathbb{Q}_2(2^{1/4})$ is not Galois. Indeed, normality would imply $i\in E$. Since $\mathbb{Q}_2(\sqrt2)\subset E$, this would give $E=\mathbb{Q}_2(\sqrt2,i)$, a biquadratic extension. But then $E$ would have an automorphism sending $\sqrt2$ to $-\sqrt2$ and fixing $i$; such an automorphism sends $2^{1/4}$ to $\pm i2^{1/4}$ and therefore has order four, a contradiction.

Thus in either case the two completed fields are not isomorphic over $\mathbb{Q}_p$.
___

> [!problem] Problem 2
> Let $C,C^\flat$ be the perfectoid fields from Problem Set 6, #1: $C$ is the completion of $\overline{\mathbb{Q}}_p$, and $C^\flat$ is its characteristic-$p$ tilt. Let $A,A^\flat$ be their valuation rings. The standard notation in the literature is $\mathcal{O}_C,\mathcal{O}_{C^\flat}$; adopt it if you like. As in the preceding homework, we have a multiplicative map
> $$
> f^\sharp:A^\flat\longrightarrow A,\qquad x\longmapsto x^\sharp.
> $$
> The field $C^\flat$ and the ring $A^\flat$ are perfect of characteristic $p$. The Witt-vector functor $\mathrm{W}$ gives the strict $p$-ring equipped with the reduction map
> $$
> \mathrm{W}(A^\flat)\twoheadrightarrow A^\flat,
> $$
> which admits a Teichmüller lift
> $$
> [\cdot]:A^\flat\longrightarrow\mathrm{W}(A^\flat).
> $$
>
> (1) Show that $x\mapsto x^\sharp\bmod p$ induces a ring isomorphism
> $$
> A^\flat/\varpi^\flat A^\flat\cong A/pA,
> $$
> where $\varpi^\flat\in A^\flat$ is an element as in Problem Set 6 satisfying $|(\varpi^\flat)^\sharp|=|p|$ (we are taking $\varpi=p$ here).
>
> **[Tip]** Freely use results from the previous homework; then you can do this without much extra work.
>
> (2) Prove that there is a unique ring homomorphism
> $$
> \theta:\mathrm{W}(A^\flat)\longrightarrow A
> $$
> such that $\theta([x])=x^\sharp$ for every $x\in A^\flat$.
>
> **[Remark]** It is not hard to see how to define $\theta$ uniquely; the main problem is to check the homomorphism property.
>
> (3) Show that $\theta$ is surjective.
>
> **[Note 1]** The ring $\mathrm{W}(A^\flat)$, equipped with $\theta$, is often called $A_{\inf}$. It plays a central role in $p$-adic Hodge theory and related topics. For examples, see the title of Morrow’s notes on $A_{\inf}$-cohomology and the first few lines of these lecture notes.
>
> **[Note 2]** Nothing is special about our choice of $C,C^\flat$: the assertions hold for any perfectoid field $C$ of characteristic zero and its characteristic-$p$ tilt $C^\flat$. Our choice is the most basic case for $p$-adic Hodge theory. In fact, $\mathrm{W}(A^\flat)$ encodes untilts of a given $C^\flat$: in general, many perfectoid fields have tilts isomorphic to $C^\flat$. See the paragraph below Lem. 2.2.3 on p. 17 of Weinstein’s notes for a discussion.

**Proof:**
Put $R=A^\flat$. We use the previous homework's identification $R\cong\varprojlim_{x\mapsto x^p}A/pA$, under which the first projection is $x\mapsto x^\sharp\bmod p$.

**(1)** Frobenius on $A/pA$ is surjective, so the first projection $\rho:R\to A/pA$ is a surjective ring homomorphism. Moreover,
$$
x\in\operatorname{ker}\rho
\iff |x^\sharp|\le|p|
\iff |x|\le|\varpi^\flat|
\iff x\in\varpi^\flat R.
$$
The last equivalence holds because $R$ is a valuation ring. Hence $R/\varpi^\flat R\cong A/pA$.

**(2)** We first construct the homomorphism using Witt coordinates. Recall the ghost polynomial
$$
w_n(X_0,\ldots,X_n)=\sum_{i=0}^np^iX_i^{p^{n-i}}.
$$
We will use the key lemma
$$
a\equiv b\pmod p
\implies a^{p^m}\equiv b^{p^m}\pmod{p^{m+1}},
$$
which follows by induction from the binomial theorem. Consequently, changing each input of $w_n$ modulo $p$ changes its value only modulo $p^{n+1}$.

For $z=(z_0,z_1,\ldots)\in\mathrm{W}(R)$, define
$$
\theta_n(z)=
\sum_{i=0}^np^i\bigl((z_i^{1/p^i})^\sharp\bigr)
\pmod{p^{n+1}A}.
$$
We claim that $\theta_n$ is a ring homomorphism. Since $R$ is perfect, coordinatewise inverse Frobenius $F^{-n}$ is a ring automorphism of $\mathrm{W}(R)$. Choose lifts $a_i\in A$ of $\rho(z_i^{1/p^n})$. Then
$$
w_n(a_0,\ldots,a_n)
\equiv\theta_n(z)\pmod{p^{n+1}A},
$$
as is seen by choosing $a_i=(z_i^{1/p^n})^\sharp$.

The Witt addition and multiplication polynomials, evaluated on these lifts, lift the coordinates of $F^{-n}(z+z')$ and $F^{-n}(zz')$ modulo $p$, because $\rho$ is a ring homomorphism. The ghost polynomial respects Witt addition and multiplication exactly. The preceding congruence therefore shows that $\theta_n$ respects both operations modulo $p^{n+1}$.

The maps $\theta_n$ are compatible under reduction. Since $A$ is $p$-adically complete and separated, they define a ring homomorphism
$$
\theta:\mathrm{W}(R)\longrightarrow A,\qquad
\theta(z)=\sum_{i\ge0}p^i(z_i^{1/p^i})^\sharp.
$$
In particular, $\theta([x])=x^\sharp$.

For uniqueness, every $z\in\mathrm{W}(R)$ has a unique Teichmüller expansion $z=\sum_{i\ge0}p^i[x_i]$. Any ring homomorphism $\psi:\mathrm{W}(R)\to A$ is $p$-adically continuous, since $\psi(p^n\mathrm{W}(R))\subseteq p^nA$. Thus the required condition forces
$$
\psi(z)=\sum_{i\ge0}p^ix_i^\sharp,
$$
so $\psi=\theta$.

**(3)** Given $a\in A$, part (1) allows us to choose $x_0\in R$ with $a-x_0^\sharp\in pA$. Recursively choose $x_n\in R$ and $a_{n+1}\in A$ such that
$$
a_0=a,\qquad a_n=x_n^\sharp+pa_{n+1}.
$$
Then $a=\sum_{i=0}^{N-1}p^ix_i^\sharp+p^Na_N$. Letting $N\to\infty$ gives
$$
a=\sum_{i\ge0}p^ix_i^\sharp
=\theta\left(\sum_{i\ge0}p^i[x_i]\right).
$$
Hence $\theta$ is surjective.
___

> [!problem] Problem 3
> Show that
> $$
> \left\{1,\theta,\frac{\theta+\theta^2}{2}\right\}
> $$
> is an integral basis (a $\mathbb{Z}$-basis of the ring of integers) of $\mathbb{Q}(\theta)$, where $\theta$ is a root of
> $$
> \theta^3-\theta-4=0.
> $$

**Proof:**
Let $K=\mathbb{Q}(\theta)$ and $\beta=(\theta+\theta^2)/2$. The polynomial $f(X)=X^3-X-4$ is irreducible over $\mathbb{Q}$, since its reduction modulo $3$ has no root.

Using $\theta^3=\theta+4$, we obtain $\beta^2=\beta+\theta+2$ and $\theta\beta=\beta+2$. Hence
$$
\beta^3-\beta^2-3\beta-2=0,
$$
so $\beta$ is integral. Thus $M=\mathbb{Z}\cdot1+\mathbb{Z}\cdot\theta+\mathbb{Z}\cdot\beta\subseteq\mathcal{O}_K$.

The discriminant of the power basis is
$$
\operatorname{disc}(1,\theta,\theta^2)
=-4(-1)^3-27(-4)^2=-428.
$$
The change-of-basis determinant is $1/2$, so
$$
\operatorname{disc}(M)=\frac{-428}{4}=-107.
$$
Since $\operatorname{disc}(M)=[\mathcal{O}_K:M]^2\operatorname{disc}(K)$ and $107$ is prime, the index must be $1$. Therefore $\{1,\theta,\beta\}$ is an integral basis.