---
date: 2020-11-10
title: DS Lecture 24
author: Abhinav S Menon
code: ma5.101
number: 24
---

# MA5.101 - Discrete Structures | Lecture 024 | 11 Nov 2020
with Prof Ashok Kumar Das

## Miscellaneous Theorems
#### Theorem 1.
The intersection of two subgroups $H_{1}$ and $H_{2}$ of $G$ is also a subgroup.

**Proof.** This can be proved using Theorem 3 (Lecture 23). Let $h_{1}, h_{2} \in H_{1} \cap H_{2}$ [so $h_{1}$ and $h_{2}$ are both in $H_{1}$ as well as $H_{2}$]. Since $H_{1}$ is a subgroup, $h_{1} \cdot h_{2}^{-1} \in H_{1}$. Similarly, since $H_{2}$ is a subgroup, $h_{1} \cdot h_{2}^{-1} \in H_{2}$. Therefore, $h_{1} \cdot h_{2}^{-1} \in H_{1} \cap H_{2}$, QED.

Note that this is not necessarily true for union, because if $h_{1} \in H_{1}$ and $h_{2} \in H_{2}$, then $h_{1} \cdot h_{2}^{-1}$ may not be in either $H_{1}$ or $H_{2}$.

#### Theorem 2.
For a given $a \in G$, the set
<div>
$$
N(a) = \{x \in G | xa = ax\}
$$
</div>
is a subgroup of $G$.

**Proof.** We will prove this also using Theorem 3. Let $h_{1}, h_{2} \in N(a)$; then $h_{1}a = ah_{1}$ and $h_{2}a = ah_{2}$.

Pre- and postmultiplying the second equation by $h_{2}^{-1}$, we see that  $h_{2}^{-1}a = ah_{2}^{-1}$.

Now $(h_{1} h_{2}^{-1})a = h_{1} (h_{2}^{-1}a) = h_{1} (ah_{2}^{-1}) = (h_{1}a) h_{2}^{-1} = (ah_{1})h_{2}^{-1} = a(h_{1}h_{2}^{-1})$. Hence $h_{1} \cdot h_{2}^{-1} \in N(a)$, QED.

#### Theorem 3.
A group $\langle G, \cdot \rangle$ is abelian iff $(ab)^{-1} = a^{-1}b^{-1}$, $\forall a,b \in G$.

**Proof.**

(i) $(ab)^{-1} = a^{-1}b^{-1}$, $\forall a,b \in G \Rightarrow G$ is abelian.

Let $g_{1}, g_{2} \in G$. We will prove that $g_{2}g_{1} = g_{1}g_{2}$.

Letting $a = g_{1}^{-1}, b = g_{2}^{-1}$, we see that $(g_{1}^{-1} g_{2}^{-1})^{-1} = (g_{1}^{-1})^{-1} (g_{2}^{-1})^{-1}$.

However, $(xy)^{-1} = y^{-1}x^{-1}$. Using this property on the LHS, we get $(g_{2}^{-1})^{-1} (g_{1}^{-1})^{-1} = (g_{1}^{-1})^{-1} (g_{2}^{-1})^{-1}$.

Now, $(x^{-1})^{-1} = x$, so $g_{2}g_{1} = g_{1}g_{2}$. This proves the forward direction.

(ii) $G$ is abelian $\Rightarrow (ab)^{-1} = a^{-1}b^{-1}$, $\forall a,b \in G$.

Since $G$ is abelian, $b^{-1}a^{-1} = a^{-1}b^{-1}$. However, we know the LHS to be equal to $(ab)^{-1}$. Hence $(ab)^{-1} = a^{-1}b^{-1}$, $\forall a,b \in G$. This completes the proof.
