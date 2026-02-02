---
title: Thesis
publish: true
---

### Short points
* The fundamental group of the complement of a knot is always presented by a [wirtinger presentation](https://en.wikipedia.org/wiki/Wirtinger_presentation)
* We are now growing the knot, why not shrinking the complement?
* [Knot atlas (knot database / library)](https://katlas.org/wiki/Main_Page)
* [Wiki page](https://en.wikipedia.org/wiki/Floer_homology#Heegaard_Floer_homology) on how certain knot invariants are categorified, see also: [Khovanov homology](https://en.wikipedia.org/wiki/Khovanov_homology).
* A very nice [Stack Exchange](https://math.stackexchange.com/questions/1311865/equivalence-of-knots-ambient-isotopy-vs-homeomorphism) thread on using homeomorphisms or isotopies for knot theory and when they are equivalent.

#### Operations on knots
* Connected sum
* [Mutation](https://en.wikipedia.org/wiki/Mutation_(knot_theory))

#### Notations
* [Conway notation](https://www.sciencedirect.com/science/chapter/edited-volume/abs/pii/B9780080129754500345) or [this page](https://www.mi.sanu.ac.rs/vismath/sl/l14.htm)
* Gauss notation for knots (and other notations) [Tabulating knots](https://en.wikipedia.org/wiki/Knot_theory#Tabulating_knots), [Knot tabulation](https://en.wikipedia.org/wiki/Knot_tabulation)
* [Petal projection](https://en.wikipedia.org/wiki/Petal_projection)


#### Braids, Tangles etc
* Look into tangles; the Conway sense might be useful, but the link theoretic sense might be useful to construct the partitioned surface (of the sphere) that we want, to obtain the graph. 
* Look into braids, [alexanders theorem](https://en.wikipedia.org/wiki/Alexander%27s_theorem) and [markov's theorem](https://en.wikipedia.org/wiki/Markov_theoremhttps://en.wikipedia.org/wiki/Markov_theorem)

Both these constructions might enable the "partitioning" of the knot so we can define compatibility to some "knotted partition".

#### Graph corospondences

|left|right|
| ----------- | ----------- |
| "preffered" knot diagram      | Medial graph of G |
| Tate graph     | graph G  |
| "Almost polyhedral graph" (result of the algorithm) | Dual of G |
| ? | Medial graph of the dual of G |

In other words, the almost polyhedral graph is the dual of the tate graph, and the knot diagram is the medial graph of the tate graph. [Medial graph](https://en.wikipedia.org/wiki/Knot_(mathematics)#Applications_to_graph_theory) That a knot diagram is the medial graph of the tate graph is known. To get the result that the AP graph is the dual of the tate graph, we might be interested in looking into the medial graph of this AP graph. If we see cases where this graph is not isomorphic to the medial graph of G, the tate graph and the AP graph cannot be duals (in general) [Properties of dual graph](https://en.wikipedia.org/wiki/Dual_graph#Additional_properties).

1. Maybe the medial graph should be the [line graph](https://en.wikipedia.org/wiki/Line_graph)?
2. There are multiple knot diagrams that represent the same knot, is there a preferred knot diagram that works for this corrospondence? Maybe any diagram with the minimum amount of crossings suffices?
