---
title: Knotted Partitions
publish: true
---

[[thesis]]

#### Definition (Ambient isotopy)
Let $N,M$ be manifolds and $g,h: N \to M$ embeddings into $M$. Then a map $F: M \times [0,1] \to M$ is an ambient isotopy taking $g$ to $h$ if for each $t$, $F_t: M \to M, F_t = F(\_, t)$ is a homeomorphism, $F_0$ is the identity, and $F_1 \circ g = h$.      

#### Definition (Knotted partition)
We define a $k$-knotted partition (denoted as $P$) as a partition $\{ P_1, P_2 \dots P_k \}$ of $\mathbb{D}^3$ together with a sequence of $(\sigma)_{i \in 1 \dots k}$ with $\sigma_i = P_q$ for some $q \in 1 \dots k$, that satisfies: 
1. $d(\sigma_i,\sigma_j) = 0$ for all $i,j$ with $|i - j| =1$.
2. ? $\text{vol}(P_i) = \text{vol}(\mathbb{D}^3) / k$ ?

#### Definition (Knotted isotopy)
Let $P$ be a $k$-knotted partition. Then we say that $F$ is a knotted isotopy if for all $t$, $\{ F_t(P_1), F_t(P_2), \dots, F_t(P_k) \}$ is a partition of $\mathbb{D}^3$, and together with the sequence $\sigma'_i = F_t(\sigma_i)$ is a $k$-knotted partition.

#### Definition Compatibility of a knot with a knotted partition
Todo

### Questions
1. Do knotted isotopies of some knotted partition induce ambient isotopies on compatible knots?
2. Do ambient isotopies of some knot induce knotted isotopies on compatible knotted partitions?
3. If 2., does this preserve compatibility? 
4. Is this actually a faithful representation of the existing construction? 