---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Equivalent Condition of Primitivity/","dgPassFrontmatter":true}
---

#TERMS/primitive #TERMS/maximal-subgroup #RESOURCE/cards 

> [!theorem]
> A transitive permutation group is primitive iff its some point stabilizer is a maximal subgroup.

**_Proof._**
Let $G\leq\mathrm{Sym}(\Omega)$ be a primitive permutation group. Assume that the point stabilizer $G_\omega$ is not a maximal subgroup. Then there exists a subgroup $H$ such that $G_\omega<H<G$. Let $B=H\omega$. We claim that $B$ is a block. If there is a $\sigma\in G$ such that $\sigma(B)\cap B\neq\emptyset$, then we have $h_1,h_2$ satisfying $\sigma h_2\omega=h_1\omega$ and so $h_1^{-1}\sigma h_2\in G_\omega<H$. It yields that $\sigma\in H$ and $\sigma(B)=B$, i.e., $B$ is a block. By the primitivity of $G$, either $B=\{\omega\}$ or $B=\Omega$. However, both of them are impossible.

Conversely, if $G$ is imprimitive, then there is a non-trivial block system $\mathcal B$. For any $\omega\in\Omega$, there is a $B\in\mathcal B$ such that $\omega\in B$. Since $G_\omega<G_B<G$, the group $G_\omega$ is not a maximal subgroup.
□
