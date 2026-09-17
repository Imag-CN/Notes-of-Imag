___

> [!problem] [MAR] 1.4.2
> a) Let $\mathcal{L} = \{\cdot, e\}$ be the language of groups. Show that there is a sentence $\phi$ such that $\mathcal{M} \models \phi$ if and only if $\mathcal{M} \cong \mathbb{Z}/2\mathbb{Z} \times \mathbb{Z}/2\mathbb{Z}$.
>
> b) Let $\mathcal{L}$ be any finite language and let $\mathcal{M}$ be a finite $\mathcal{L}$-structure. Show that there is an $\mathcal{L}$-sentence $\phi$ such that $\mathcal{N} \models \phi$ if and only if $\mathcal{N} \cong \mathcal{M}$.

**Proof:**
**a)** The group $\mathbb{Z}/2\mathbb{Z} \times \mathbb{Z}/2\mathbb{Z}$ is characterized up to isomorphism by being a group of size $4$ where every element has order $2$ except the identity. So define the $\mathcal{L}$-sentence:
$$ \phi := \phi_{\text{grp}} \wedge \phi_{4} \wedge \forall x (x \cdot x = e) $$
where $\phi_{\text{grp}}$ is the conjunction of standard group axioms, and $\phi_{4}$ asserts the universe has exactly $4$ elements ($\exists x_1 \dots x_4 (\bigwedge_{i<j} x_i \neq x_j \wedge \forall y \bigvee_i y = x_i)$). Then $\mathcal{M} \models \phi$ iff $\mathcal{M} \cong \mathbb{Z}/2\mathbb{Z} \times \mathbb{Z}/2\mathbb{Z}$.

**b)** Let $\mathcal{L}$ be a finite language and $\mathcal{M}$ a finite $\mathcal{L}$-structure with domain $\{a_1, \dots, a_n\}$. We construct a sentence $\phi$ capturing $\mathcal{M}$ up to isomorphism:

1. Let $\phi_{\text{size}}$ assert there are exactly $n$ elements.
2. Let $\Delta(x_1, \dots, x_n)$ be the conjunction of all atomic and negated atomic facts (involving relation, function, and constant symbols of $\mathcal{L}$) true in $\mathcal{M}$ on $a_1, \dots, a_n$.

Define $\phi := \phi_{\text{size}} \wedge \exists x_1 \dots \exists x_n \, \Delta(x_1, \dots, x_n)$.
If $\mathcal{N} \models \phi$, $\mathcal{N}$ has exactly $n$ elements and satisfies the same atomic diagram as $\mathcal{M}$; the map sending witnesses in $\mathcal{N}$ to $a_i$ is an isomorphism. Conversely, $\mathcal{N} \cong \mathcal{M}$ implies $\mathcal{N} \models \phi$. Thus $\mathcal{N} \models \phi$ iff $\mathcal{N} \cong \mathcal{M}$.
___

