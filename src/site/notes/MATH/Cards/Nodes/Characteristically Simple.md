---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Characteristically Simple/","dgPassFrontmatter":true}
---


> [!definition]
> A group is said to be *characteristically simple* if it has no proper nontrivial characteristic subgroups.

> [!proposition]
> Any characteristically simple group is a product of isomorphic simple groups.

**_Proof._**
Let $T$ be a minimal normal subgroup of $G$. Then $T$ is isomorphic to a direct product of isomorphic simple groups, see [[MATH/Cards/Nodes/Minimal Normal Subgroup and Maximal Normal Subgroup\|here]]. Define $M=\langle T^\phi:\phi\in\mathrm{Aut}(G)\rangle$. Note that $M$ is a characteristic group of $G$ and so $M=G$. Since $T^\phi$ is normal in $G$ and $T^\phi\cap T\in\left\{1,T\right\}$ by $T$ minimal normal subgroup, we have $M\cong T\times\cdots\times T$ by [[MATH/Cards/Nodes/Normal Subgroups that Intersect Trivially\|this lemma]]. Therefore, $G$ is a product of isomorphic simple groups.
<p align="left">□</p>