---
title: Genericity exercises
publish: true
---

For most of this page, we refer to [Golubitsky and Guillemin](books/Stable_Mappings_and_their_Singularities.pdf) for definitions etc. We always implictly endow $C^k(X,Y)$ with the Whitney $C^k$ topology.

### Definition transversality of vector spaces
Assume We have two vectorsubspaces $A,B \subset X$ of some vector space $X$. We write $A \pitchfork B$ if $A + B = X$.

### Definition transversality of manifolds
Assume we have two submanifolds $A,B \subset M$ of some manifold $M$. We write $A \pitchfork B$ if for each $p \in A \cap B, \; T_pA \pitchfork T_pB$ (as vector spaces).

### Definition 4.1. (p.50) Transversality

Let X, Y be smooth manifolds and $f: X \to Y$ be a smooth mapping. Let $W$ be a submanifold of $Y$ and $x \in X$. Then $f$ intersects $W$ transversally at $x$ (denoted by $f \pitchfork W$ at $x$) if either:
1. $f(x) \not\in W$, or
2. $f(x) \in W$, and $T_{f(x)}W \pitchfork (df)_x(T_xX)$ (as vector spaces).

We write $f \pitchfork W$ on $A$ if $f \pitchfork W$ at $x, \; \forall x \in A$. We leave the "on ..." if $f$ intersects $W$ transversally on the entire $X$. 

Note that for the case were $\dim(T_{f(x)}) + \dim((df)_x(T_xX)) < T_{f(x)}Y$, the only way the function can intersect $W$ transversally is if $f(X) \cap W = \empty$.

For a definition when $X$ has a boundary, see [Wikipedia](https://en.wikipedia.org/wiki/Transversality_theorem).

### Definition of corank
Let $X,Y$ be differentiable manifolds and $f: X \to Y$ a $C^1$ map. Then we define:
$$
\text{corank}(df)_p = \min(\dim(X), \dim(Y)) - \text{rank}(df)_p.
$$
We call a point $p \in X$ a critical point of $f$ if $\text{corank}(df)_p > 0$, and we denote the set of critical points of $f$ by $\Sigma_{\text{crit}, f}$. 

<!-- ### Definition of jet space 
We define the following: $J^k(M,N) = M \times N \times \mathbb{R}^k$. -->

### Definition 3.2 (p.44) residual set
Say we have a space $X$. We then call a subset $A \subset X$ a residual set if $A$ is a countable intersection of dense open subsets of $X$.

## Exercise
1. Assume we have two (k-differentiable) maps $(f,g) \in C^k(\mathbb{D}^2, \mathbb{R}^2) \times C^k(\mathbb{D}^2, \mathbb{R}^2)$. We identify $\partial\mathbb{D}^2$ with $\mathbb{S}^1$. Show that $f(\mathbb{S}^1) \pitchfork g(\mathbb{S}^1)$ (as manifolds) is a generic property of $C^k(\mathbb{D}^2, \mathbb{R}^2) \times C^k(\mathbb{D}^2, \mathbb{R}^2)$.   

We note that $f(\mathbb{S}^1) \pitchfork g(\mathbb{S}^1)$ means that $\forall q \in f(\mathbb{S}^1) \cap g(\mathbb{S}^1), T_qf(\mathbb{S}^1) + T_qg(\mathbb{S}^1) = T_q\mathbb{R}^2 \cong \mathbb{R}^2$.



#### Proof: 
<center>The most straightforward way to do this is with multijets.</center>

<!-- Define the following spaces:
$$
I_{\Sigma_{\text{crit}, f}} = \{ f \in C^k(\mathbb{D}^2, \mathbb{R}^2) \mid J^1f \pitchfork \Sigma_{\text{crit}, f} \}
$$
$$
I_{\Sigma_{\text{crit}, g}} = \{ g \in C^k(\mathbb{D}^2, \mathbb{R}^2) \mid J^1g \pitchfork \Sigma_{\text{crit}, g} \}
$$

Then, since $\Sigma_{\text{crit}, f}$ is a submanifold of $J^k f$ for any $f$, we have by Thom's transversality theorem that $I_{\Sigma_{\text{crit}, f}} \times I_{\Sigma_{\text{crit}, g}}$ is a residual set of $C^k(\mathbb{D}^2, \mathbb{R}^2) \times C^k(\mathbb{D}^2, \mathbb{R}^2)$.  -->

2. Show this implies the images of $f$ and $g$ (along the boundary) intersect in finitely many points, generically. 


3. Show that for three functions $f,g,h$ the generic case is no triple intersection.

## Questions
1. Is it true that for two smooth ($k$-smooth?) manifolds that $C^k(X,Y)$ with the Whitney $C^{k}$ topology is a baire space? Or only in the $\infty$ case? (We discussed things on the board for $C^k$, but in the book it only mentions $C^\infty$)
2. What is the intuition for allowing a countable amount of intersections in the definition of a residual set? This is fine in a Baire space, but does this break in other spaces? As in does this allow you to construct a generic property that does not hold on a dense subset of the space?   