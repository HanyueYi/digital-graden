---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Orbits of Normal Subgroups Form a Block System/","dgPassFrontmatter":true}
---

#RESOURCE/cards #TERMS/normal-subgroup #TERMS/primitive 

> [!proposition]
> Let $G\leqslant\mathrm{Sym}(\Omega)$ be a group and let $N\lhd G$ be a normal subgroup of $G$. Then the set of orbits of $N$ forms a block system of $\Omega$.

**_Proof._**
Suppose $O_1,\cdots,O_k$ are orbits of $N$. Then $\sqcup_{i=1}^kO_i=\Omega$ and $O_i\cap O_j=\emptyset$ for any $i\neq j$. For any $g\in G$, we have 

$$(O_i^g)^N=(O_i^{gNg^{-1}})^g=(O_i^N)^g=O_i^g,$$

and it yields $O_i^g$ is a union of $N$-orbits. For $\omega_1^g,\omega_2^g\in O_i^g$, there exists $n\in N$ such that $\omega_1^n=\omega_2$. Then $(\omega_1^g)^m=\omega_2^g$ with $m=g^{-1}ng\in N$. So $N$ is transitive on $O_i^g$ and so $O_i^g=O_j$ for some $j\in\{1,\cdots,k\}$. Therefore, the set of orbits of $N$ forms a block system.
<p align="left">□</p>

