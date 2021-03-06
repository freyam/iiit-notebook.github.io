---
date: 2020-11-12
title: DS Lecture 25
author: Abhinav S Menon
code: ma5.101
number: 25
---

## Cosets
### Definition
The left cosets of a group $G$ with respect to a subgroup $H \subseteq G$ are defined as
<div>
$$
gH = \{gh | h \in H\}
$$
</div>
for each $g \in G$. Similarly, the right cosets of a group $G$ with respect to a subgroup $H \subseteq G$ are defined as
<div>
$$
Hg = \{hg | h \in H\}
$$
</div>
for each $g \in G$.

### Example
Consider the set 
<div>
$$
G_{3} = \{1,2,3\}
$$
</div>
and its set of permutations
<div>
$$
S_{3} = \{e,(1 \, 2), (1 \, 3), (2 \, 3), (1 \, 2 \, 3), (1 \, 3 \, 2)\}
$$
</div>
under the operation of composition, denoted by $\cdot$. (This is called the *symmetric group of degree 3*). We will find the left and right cosets of a subgroup of $S_{3}$,
<div>
$$
H = \{e, (1 \, 2)\}.
$$
</div>

1. Left
    <div>
    $$
    eH = H
    $$
    $$
    (1 \, 2)H = \{(1 \, 2) \cdot e, (1 \, 2) \cdot (1 \, 2)\} = \{(1 \, 2), e\}
    $$
    $$
    (2 \, 3)H = \{(2 \, 3) \cdot e, (2 \, 3) \cdot (1 \, 2)\} = \{(2 \, 3), (1 \, 3 \, 2)\}
    $$
    $$
    (1 \, 3)H = \{(1 \, 3) \cdot e, (1 \, 3) \cdot (1 \, 2)\} = \{(1 \, 3), (1 \, 2 \, 3)\}
    $$
    $$
    (1 \, 2 \, 3)H = \{(1 \, 2 \, 3) \cdot e, (1 \, 2 \, 3) \cdot (1 \, 2)\} = \{(1 \, 2 \, 3), (1 \, 3)\}
    $$
    $$
    (1 \, 3 \, 2)H = \{(1 \, 3 \, 2) \cdot e, (1 \, 3 \, 2) \cdot (1 \, 2)\} = \{(1 \, 3 \, 2), (1 \, 2)\}
    $$
    </div>

2. Right
    <div>
    $$
    He = H
    $$
    $$
    H(1 \, 2) = \{e \cdot (1 \, 2), (1 \, 2) \cdot (1 \, 2)\} = \{(1 \, 2), e\}
    $$
    $$
    H(2 \, 3) = \{e \cdot (2 \, 3), (1 \, 2) \cdot (2 \, 3)\} = \{(2 \, 3), (1 \, 2 \, 3)\}
    $$
    $$
    H(1 \, 3) = \{e \cdot (1 \, 3), (1 \, 2) \cdot (1 \, 3)\} = \{(1 \, 3), (1 \, 3 \, 2)\}
    $$
    $$
    H(1 \, 2 \, 3) = \{e \cdot (1 \, 2 \, 3), (1 \, 2) \cdot (1 \, 2 \, 3)\} = \{(1 \, 2 \, 3), (2 \, 3)\}
    $$
    $$
    H(1 \, 3 \, 2) = \{e \cdot (1 \, 3 \, 2), (1 \, 2) \cdot (1 \, 3 \, 2)\} = \{(1 \, 3 \, 2), (1 \, 3)\}
    $$
    </div>
    
We can see that all cosets have the same number of elements as $H$ and as each other. To prove this, consider distinct $h_{1}, h_{2} \in H$; therefore $gh_{1}$ and $gh_{2}$ are in $gH$. If $gh_{1} = gh_{2}$, then $h_{1} = h_{2}$, which is a contradiction; therefore, for each $h \in H$, there is a unique $gh \in gH$, which means that $gH$ and $H$ have the same cardinality.

## Cosets as Partitions
#### Theorem 1.
The (left or right) cosets of a group $G$ with respect to a subgroup $H$ form a partition of the group.

**Proof.** We will show first that the union of all left cosets gives the group, *i.e.* that every $g \in G$ is in some left coset, and then that any two left cosets are either equal or disjoint.

Consider an arbitrary $g \in G$, and the coset $gH$. Since $e \in H$, we know that $ge \in gH \Rightarrow g \in gH$. Hence, each element is included in some coset; therefore,
<div>
$$
\bigcup_{g \in G} gH = G.
$$
</div>

Now, suppose there are two left cosets $g_{1}H$ and $g_{2}H$ which are not disjoint, *i.e.*, $\exists g \in G$ such that $g \in g_{1}H$ and $g \in g_{2}H$.

First, we note that if $h \in H$, then by closure, $hH = H$.

Now, we know that since $g$ is in $g_{1}H$ and $g_{2}H$, there must exist $h_{1}$ and $h_{2}$ such that $g = g_{1}h_{1}$ and $g = g_{2}h_{2}$.

Now, $gH = (g_{1}h_{1})H = g_{1}(h_{1}H)$. Since $h_{1} \in H$, this means that $gH = g_{1}H$.

Similarly, $gH = (g_{2}h_{2})H = g_{2}(h_{2}H)$. Since $h_{2} \in H$, this means that $gH = g_{2}H$.

Consequently, $g_{1}H = g_{2}H$. This completes the proof.

### The Coset Relations
The left coset relation on the group $G$ with respect to a subgroup $H$ is defined as $_ {g_{1}}R_{g_{2}} \Leftrightarrow g_{1}^{-1} \cdot g_{2} \in H$. Similarly, the right coset relation on the group $G$ with respect to a subgroup $H$ is defined as $_ {g_{1}}R_{g_{2}} \Leftrightarrow g_{1} \cdot g_{2}^{-1} \in H$.

#### Theorem 2.
The coset relations are equivalence relations on $G$.

**Proof.** We will show the reflexivity, symmetry and transitivity of the left coset relation; the proof for the right coset relation is analogous.

(i) **Reflexivity.** $g^{-1} \cdot g = e \in H$; hence $_gR_g$, $\forall g \in G$, and $R$ is symmetric.

(ii) **Symmetry.** Suppose $_ {g_{1}}R_{g_{2}}$, *i.e.*, $g_{1}^{-1} \cdot g_{2} \in H$. However, $(g_{1}^{-1} \cdot g_{2})^{-1} = g_{2}^{-1} \cdot g_{1}$. Since $H$ is a subgroup, $h \in H \Rightarrow h^{-1} \in H$; letting $h = g_{1}^{-1} \cdot g_{2}$, we see that $g_{2}^{-1} \cdot g_{1} \in H \Rightarrow _ {g_{2}}R_{g{1}}$, and $R$ is symmetric.

(iii) **Transitivity.** Let $_ {g_{1}}R_{g_{2}}$ and $_ {g_{2}}R_{g_{3}}$, *i.e.*, $g_{1}^{-1} \cdot g_{2} \in H$ and $g_{2}^{-1} \cdot g_{3} \in H$. Since $H$ is a subgroup, $h_{1}, h_{2} \in H \Rightarrow h_{1}h_{2} \in H$. Letting $h_{1} = g_{1}^{-1} \cdot g_{2}$ and $h_{2} = g_{2}^{-1} \cdot g_{3}$, we see that $(g_{1}^{-1} \cdot g_{2}) \cdot (g_{2}^{-1} \cdot g_{3}) = g_{1}^{-1} \cdot (g_{2} \cdot g_{2}^{-1}) \cdot g_{3} = g_{1}^{-1} \cdot g_{3} \in H$. Hence $_ {g_{1}}R_{g_{3}}$, and $R$ is transitive.

This proves that the left coset relation is an equivalence relation. Further, its equivalence classes are simply the left cosets of $G$ (which have been shown to form a partition).

We can show that $_ {g_{1}}R_{g_{2}} \Leftrightarrow (g_{1}$ and $g_{2}$ are in the same left coset $gH)$:

(i) $_ {g_{1}}R_{g_{2}} \Rightarrow (g_{1}$ and $g_{2}$ are in the same left coset $gH)$

If $_ {g_{1}}R_{g_{2}}$, then $g_{1}^{-1} \cdot g_{2} \in H$. Let $g_{1}^{-1} \cdot g_{2} = h \in H$; this implies that $g_{2} = g_{1}h$, and therefore $g_{2} \in g_{1}H$.

Trivially, $g_{2} \in g_{2}H$, so $g_{1}H$ and $g_{2}H$ are not disjoint. Hence, by Theorem 1, $g_{1}H = g_{2}H$ and $g_{1}$ and $g_{2}$ are in the same left coset of $H$.

(ii) $(g_{1}$ and $g_{2}$ are in the same left coset $gH) \Rightarrow _ {g_{1}}R_{g_{2}}$.

Since $g_{1}$ and $g_{2}$ are in the same left coset $gH$, we see that $g_{1} = gh_{1}$ and $g_{2} = gh_{2}$ for some $h_{1}, h_{2} \in H$. Therefore, $g_{1}^{-1} = h_{1}^{-1} \cdot g^{-1}$.

Now, $g_{1}^{-1} \cdot g_{2} = (h_{1}^{-1} \cdot g^{-1}) \cdot (g \cdot h_{2}) = h_{1}^{-1} \cdot (g^{-1} \cdot g) \cdot h_{2} = h_{1}^{-1} \cdot h_{2} \in H$, by closure. Hence, $_ {g_{1}}R_{g_{2}}$. This completes the proof.
