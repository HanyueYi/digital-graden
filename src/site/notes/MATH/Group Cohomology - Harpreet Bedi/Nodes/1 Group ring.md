---
{"dg-publish":true,"permalink":"/MATH/Group Cohomology - Harpreet Bedi/Nodes/1 Group ring/","dgPassFrontmatter":true}
---


Let $G$ be a group and let $A$ be a $G$-module.

> [!definition] $G$-homomorphism 
> A homomorphism of $G$-module (or a $G$-homomorphism) is a map $\phi:A\to B$ such that 
> 
> $$\begin{aligned} \phi(a+a')&=\phi(a)+\phi(a'),\\ \phi(ga) &= g\cdot\phi(a),\end{aligned}$$
> we denote it as $\mathrm{Hom}_G(A,B)$.

> [!definition] $G$-invariants
> Let $A$ be a $G$-module. We define the fixed points in $A$ by 
> 
> $$A^G:=\{a\in A|\space g\cdot a=a,\forall g\in G,a\in A\}.$$



Notice that the group ring $\mathbb{Z}[G]$ is a $G$-module. Let $A=\mathbb{Z}[G]$.

> [!definition] 
> Augmentation ideal $I_G$ in $\mathbb{Z}[G]$ is defined to be the kernel of the augmentation map
> 
> $$\mathbb{Z}[G]\to \mathbb{Z},\space \sum_{g\in G}a_gg\mapsto\sum_{g\in G}a_g.$$

If $x\in I_G$, then $x=\sum_{g\in G}a_gg=\sum_{g\in G}a_g(g-1)$. Define 

$$I_GA=\langle a(g-1)\big|a\in A,g\in G\rangle.$$

Let $A_G=A/I_GA$. Then $A_G$ is the largest quotient of $A$ on which $G$ acts trivially and $A^G$ is largest subobject of $A$ on which $G$ acts trivially. 

> [!definition]
> Let $N_G=\sum_{g\in G}g\in \mathbb{Z}[G]$. We define coaugmentation map as
> 
> $$\mu:\mathbb{Z}\to \mathbb{Z}[G],\space n\mapsto nN_G.$$

**Examples.**
- $\mathbb{Z}[G]_G=\mathbb{Z}$
- $\mathbb{Z}[G]^G=\langle N_G\rangle$ for finite $G$
- $\mathbb{Z}[G]^G=0$ for infinite $G$



