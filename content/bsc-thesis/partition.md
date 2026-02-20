---
publish: true
title: Cells as preimages
---

## Sketch

What we want to to look at is a function $f: \mathbb{R}^3 \to \mathbb{R}^n$, where $n$ is the number of "colours" we consider. (This is actually an interesting parameter, would this induce some sort of homology?) This function signifies how close each point is to being that colour. We then can partition $\mathbb{R}^3$ into the following: $U_k := \{ p \in \mathbb{R}^3 | \; \text{max}_i(f(p)_i) = k \}$. This is actually a pullback of a partition defined on $\mathbb{R}^n$ by: $V_k := \{ p \in \mathbb{R}^n | \; p_k > p_i \}$. 

We can define the boundary space as being: $B = \{ p \in \mathbb{R}^3 \; | \; \exist i,j, \; i \not= j, \; s.t. \; f(p)_i = f(p)_j \}$. Then the graph on the surface of the sphere would be $G := B \cap \mathbb{S^2}$.

If we define the $V_k$'s with $\geq$ instead, we could replace the above definition for the boundary space with the union of pairs of intersections. (do we want the preimages to be open or closed? does it matter?)

To find the evolution of the function, we can define a pointwise recurrence relation. (How would this be continuous (differentiable?)). Can we get a pde / vector field on $\mathbb{R}^3$ out of this? Or, should the evolution of this function be some sort of (discrete?) homotopy which we get out of some other pde? 

What can we say about generic points in this partition? Generic points on the graph are where 2 colours meet. 

Something with stratifications

The zero colour is the colour of the outside, thus if we initially partition the knot in $n$ colours, we have $n + 1$ total colours.

Maybe we could / should define something like a colour bundle?

Should it be written as a partition of $N$ being pulled back to a partition on $M$?

## Formal

#### Definition
For a generic continuous function $f: M \to N$, (with $\dim(N) = n$) we define: 
* The _colours of a point_ $p \in M$, to be the set of colours $i$ for which $f_i(p)$ is maximal, i.e.:
$$
C_{f, p} := \{i \in 0\dots n \; | \; f_i(p) = \max_{j \in 0 \dots n}(f_j(p)) \}.
$$
* We call $|C_{f,p}|$ the _colour degree_ of the point. We say $p$ is a _colour boundary point_ if $|C_{f,p}| > 1$.
* If $|C_{f,p}| = 1$, we say this is _the_ colour of the point.  
* We define the _colour boundary_ by $\partial_C M := \{ p \in M \; | \; |C_{f,p}| > 1\}$.

[^1]: needs work, $C_{f,p}$ is still a set strictly speaking. it can safely be unwrapped since it is garuanteed to have size 1 but I dont quite know how to type this

#### Definition (Colour partition)[^1]
For a generic continuous function $f: M \to N$, we define the following function: 
$$
g: M \backslash \partial_C M \to \{0\dots n\}, \quad p \mapsto C_{f,p}.
$$
Where we endow $\{ 0\dots n \}$ with the discrete topology. We define the colour partition as the collection of subsets $P_k := g^{-1}(k)$, together with the colour boundary $\partial_C M$.

[^2]: We should specify in some way that the sphere we take is large enough.

#### Definition (Colour boundary graph)[^2]
We define the colour boundary graph as $\mathbb{S}^2 \cap \partial_C M$. 

#### Conjecture (needs work)
For a generic continuous function $f: M \to N$, having colour degree 3 is generic in the collection of high ($ \geq 3 $) degree boundary points.


