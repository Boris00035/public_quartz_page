---
title: Stratification
publish: true
---
## Sketch
We have a function $f: M \to \mathbb{R}^n$, with $n$ the number of colours we use. $\mathbb{R}^n$ is stratified with $n$ types of strata, according to which coordinate is maximal. We want to look at how $f$ pulls this stratification back to $M$.


## Formal
Manifold always means smooth manifold.


#### Definition (is this enough? Can the homeomorphisms change how the strata fit together?)
Let $(X, \mathcal{S}_X), (X, \mathcal{S}_{X'})$ two stratified manifolds. We say the stratifications $\mathcal{S}_X, \mathcal{S}_{X'}$ are equivalent if: 
* There is a bijection $b: \mathcal{S}_X \to \mathcal{S}_{X'}$ 
* and $b(s)$ is homeomorphic to $s$ for all $s \in \mathcal{S}_{X}$. 

#### Definition (is this the right way to do this?) 
Let $(X, \mathcal{S}_X), (Y, \mathcal{S}_Y)$ two stratified manifold. We say $f$ is a diffeomorphism of these, if:
* $f$ is a diffeomorphism between $X$ and $Y$.
* $f(\mathcal{S}_X)$ is equivalent to $\mathcal{S}_Y$.
* $f(\mathcal{S}_Y)$ is equivalent to $\mathcal{S}_X$.

Where $f(\mathcal{S}_X)$ is defined as the collection of images of $f$ of the components of $\mathcal{S}_X$.

[^strat]: Does a stratification always descent to subsets?

#### Definition (stratified model) 
Let $M$ some stratified manifold. We say that a collection of stratified manifolds $\mathcal{M}$ is a _stratified model_ of $M$, if for every point $p \in M$, there exists a neighbourhood (endowed with the subset stratification[^strat]) which is diffeomorphic to some component of $\mathcal{M}$.

#### Definition / Claim (max-stratification)
Let $\mathcal{S}_m := \{U_S \; | \; S \subset \{0..n\} \}$ be a collection of subsets of $\mathbb{R}^n$ with $U_S$ given by:

$$ 
U_S := \{ p \in \mathbb{R}^n | \; p_i \in \max_j(p_j), \; \forall i \in S \}.
$$

Then $\mathcal{S}_m$ is a stratification, which we will call the max-stratification. Additionally, the dimension of $U_S$ will be given by $\dim(U_S) = n - |S|$. 


#### Claim (needs work)
Let $f: M \to \mathbb{R}^n$ a (generic?) smooth map. Then this induces a stratification on $M$ by "pulling back" the max-stratification.

[^model]: Need to define these model manifolds along with their stratification. 

[^genericity]: Is this if and only if? If so, then we could also state that a bifurcation point is a point (x,t) where the stratified model is not actually a model.

#### Claim [^genericity]
Let $f: M \to \mathbb{R}^n$ a generic smooth map. We endow $M$ with the stratification induced by pulling back the max-stratification on $\mathbb{R}^n$ over $f$. Then $\{ \text{Y}, - \}$ [^model] is a stratified model of $M$.

#### Definition
We define an _almost family of generic functions_ as a family of functions $g: M \times \mathbb{R} \to \mathbb{R}^n$ together with a set of _bifurcation points_ $\subset M \times \mathbb{R}$, where for each $t$ not part of a bifurcation point, $g(\_, t)$ is generic.

#### Claim
Let $(x_b,t_b)$ be a bifurcation point. Then we can model this bifurcation as a half plane moving over the point $x_b$, crossing it exactly at $t_b$.



## Evolution of $f$
* Investigate how this $f$ should evolve according to the cell growth specified in this [paper](https://repository.kulib.kyoto-u.ac.jp/server/api/core/bitstreams/7de154cb-2df4-4436-8a90-6dca9da1b221/content).

<!-- ----

## Sketch (old)

What we want to to look at is a function $f: \mathbb{R}^3 \to \mathbb{R}^n$, where $n$ is the number of "colours" we consider. (This is actually an interesting parameter, would this induce some sort of homology?) This function signifies how close each point is to being that colour. We then can partition $\mathbb{R}^3$ into the following: $U_k := \{ p \in \mathbb{R}^3 | \; \text{max}_i(f(p)_i) = k \}$. This is actually a pullback of a partition defined on $\mathbb{R}^n$ by: $V_k := \{ p \in \mathbb{R}^n | \; p_k > p_i \}$. 

We can define the boundary space as being: $B = \{ p \in \mathbb{R}^3 \; | \; \exist i,j, \; i \not= j, \; s.t. \; f(p)_i = f(p)_j \}$. Then the graph on the surface of the sphere would be $G := B \cap \mathbb{S^2}$.

If we define the $V_k$'s with $\geq$ instead, we could replace the above definition for the boundary space with the union of pairs of intersections. (do we want the preimages to be open or closed? does it matter?)

To find the evolution of the function, we can define a pointwise recurrence relation. (How would this be continuous (differentiable?)). Can we get a pde / vector field on $\mathbb{R}^3$ out of this? Or, should the evolution of this function be some sort of (discrete?) homotopy which we get out of some other pde? 

What can we say about generic points in this partition? Generic points on the graph are where 2 colours meet. 

Something with stratifications

The zero colour is the colour of the outside, thus if we initially partition the knot in $n$ colours, we have $n + 1$ total colours.

Maybe we could / should define something like a colour bundle?

Should it be written as a partition of $N$ being pulled back to a partition on $M$?

## Formal (old)

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

[^2]: We should specify in some way that the sphere we take is large enough to contain the entire knot.

#### Definition (Colour boundary graph)[^2]
We define the colour boundary graph as $\mathbb{S}^2 \cap \partial_C M$. 

#### Conjecture (needs work)
For a generic continuous function $f: M \to N$, having colour degree 3 is generic in the collection of high ($ \geq 3 $) degree boundary points.

 -->
