---
title: Proposal - Laterally Growing Knots and their Graphs
publish: true
---
[[thesis]]

There are multiple ways of looking at knots. We build upon an alternative approach to study knots by growing them out laterally. In this approach the knot is partitioned into N “cells,” each of which is labelled (or colored). These are grown out (under constant-volume-increase, cohesion, and non-penetration restrictions), until the knot has assumed a sufficiently spherical shape.
Cells that were not neighbors initially, have now become neighbors, and the structure of this surface-covering of the sphere is believed to encode the knot structure. The bounding line between non-neighboring regions allows for the construction of a graph, where the vertices are where various neighboring regions meet.

Usually, this results in a polyhedral graph. All polyhedral graphs have connectivity 3, and in most cases the vertices have 3 edges come together, as the “easiest” case is when three cells meet.

On energetic grounds, higher-order vertices tend to “decay” to order 3 vertices, which interferes with the clean identification of toroidal knots, which would produce a non-polyhedral graph.

### Research Question:
Currently, the knot-growth approach takes the form of an algorithm. We will attempt to define this construction in a mathematically rigorous way. This construction is applied on a concrete embedding, so we investigate how this graph changes under isotopy, and see if we can find a knot invariant. We also try to relate this construction to the construction of the Tait graph of the embedding. 

### Approach: 
We will investigate this “decaying” behavior of the graph during the growth process by means of bifurcation theory.