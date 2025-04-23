---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Structure of p-groups/","dgPassFrontmatter":true}
---


> [!theorem]
> A group of order $p^2$ with prime $p$ is abelian.
{ #4ffac3}


**_Proof._**
Assume that $Z(G)\cong \mathbb{Z}_p$. Then by [[MATH/Cards/Nodes/GZ-Theorem\|G/Z theorem]], $G$ is abelian. Otherwise, $Z(G)=G$ and so $G$ is abelian.
<p align="right">□</p>

> [!theorem]
> Let $|G|=p^3$. Then either $G$ is abelian, or:
> - for $p=2$, $G=D_8$ or $Q_8$.
> - for $p\geq 3$, $G=\mathbb{Z}_{p^2}{:}\mathbb{Z}_p$ or $G=\langle a,b|a^p=b^p=c^p=1,[a,b]=c\rangle$ where the exponent of $G$ equals to $p$.
{ #oymbgb}


**_Proof._**
Assume $G$ is non-abelian. First, suppose $G$ has an element $a$ of order $p^2$. Then there exists $b\in G\backslash\langle a\rangle$ and $G=\langle a,b\rangle$. If $|b|=p$, then $G=\langle a\rangle:\langle b\rangle$ is isomorphic to $D_8$ for $p=2$ and is isomorphic to $\mathbb{Z}_{p^2}{:}\mathbb{Z}_p$ for $p\geq 3$. 

Suppose $|b|=p^2$. Then $b^p=a^\lambda$ for some integer $\lambda$. If $p=2$, then $a^b=a^3=a^{-1}$ and $b^a=b^{-1}$. It deduces that $G=Q_8$. If $p\geqslant 3$, then $a^b=a^{1+kp}$ for some $k$ with $1\leqslant k\leqslant p-1$. Claim $(ba^{-l})^p=1$. Let $b'=ba^{-l}$. Since the order of $b'$ is $p$, we get back to the last case. 

Assume $G$ does not have elements of order $p^2$. Then each elements of $G$ is of order $p$. If $p=2$, then $G$ is abelian (see [[MATH/Cards/Nodes/2-Group with Exponent 2 is Abelian\|here]]). Now assume that $p\geqslant 3$. If $|Z(G)|=p^2$, then $G/Z(G)$ is cyclic and so $G$ is abelian by [[MATH/Cards/Nodes/GZ-Theorem\|G/Z theorem]]. If $|Z(G)|=p$, then $G/Z(G)$ is abelian by [[#^4ffac3]]. Then $|G'|\leqslant |Z(G)|=p$ is non-trivial by $G$ non-abelian. Thus we have that $G'=\langle c\rangle=\mathbb{Z}_p$ and $G/G'=\langle aG',bG'\rangle = \mathbb{Z}_p\times \mathbb{Z}_p$, where $c=[a,b]$. 
<p align="right">□</p>

**Remark.** 
- $G=\mathbb{Z}_{p^2}{:}\mathbb{Z}_p$ is defined by $p^{1+2}_{-}$, and
- $G=\langle a,b|a^p=b^p=c^p=1,[a,b]=c\rangle$ is defined by $p^{1+2}_{+}$. Also see [[MATH/Cards/Nodes/Extraspecial p-groups\|extraspecial p-group]].
