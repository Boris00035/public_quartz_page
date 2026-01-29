---
publish: true
---


$\mathbb{S^1} = \{ x,y \in \mathbb{R} | x^2 + y^2 = 1 \}$

A knot is a path in 3d space:
$k: \mathbb{S}^1 \to \mathbb{R}^3$.

Two knots $k,k'$ are considered equivalent if there exists a function
$F: [0,1] \times \mathbb{R}^3 \to \mathbb{R}^3$ with $F(0, \_)|_{\mathbb{S}^1} = k$ and $F(1, \_)|_{\mathbb{S}^1} = k'$

Fundamental group of a space $X$ at $p \in X$:
$\pi_1(X,p) = \{ [\gamma] | \gamma \in P(X) \}$, met $P(X)$ alle paden die op p beginnen en eindigen.

A knot invariant is a object $I(k)$ such that for two knots $k, k'$ which are equivalent, it holds that $I(k) \cong I(k')$. 

Example of a knot invariant:
$\pi_1(\mathbb{R}^3 \backslash k(\mathbb{S}^1),p)$

#### Category of pointed spaces ($Top_*$):
Objects:
$Ob_{Top_*} = (X, x)$ met $x \in X$

Morphisms tussen $(X,x)$, $(Y,y)$:
$Hom_{(X, x),(Y, y)} = f: X \to Y$ met $f(x) = y$.

#### Category of groups ($Grp$):
Objects: groups

Morphisms: group homomorphisms

een groepshomomorfisme tussen $G, H$ is een functie $\phi: G \to H$ met $\phi(a\cdot_G b) = \phi(a)\cdot_H\phi(b) \quad \forall a,b \in G$ 


### $\pi_1$ as a functor

On objects: 
$\pi_1: Ob_{Top_*} \to Ob_{Grp} \pi_1(X,x):$ fundamentaal groep

On morphisms:
$\pi_1: Hom_{(X, x),(Y, y)} \to Hom_{\pi_1(X, x),\pi_1(Y, y)}:
f \mapsto ([\gamma] \mapsto [f \circ \gamma]) $