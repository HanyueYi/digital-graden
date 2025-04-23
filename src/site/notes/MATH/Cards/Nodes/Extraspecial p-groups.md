---
{"dg-publish":true,"aliases":["extraspecial p-group"],"permalink":"/MATH/Cards/Nodes/Extraspecial p-groups/","dgPassFrontmatter":true}
---


> [!definition] [wiki](https://en.wikipedia.org/wiki/Extra_special_group)
> A $p$-group $G$ is called *extraspecial* if its center $Z$ is cyclic of order $p$, and the quotient $G/Z$ is a non-trivial elementary abelian $p$-group. Extraspecial groups of order $p^{1+2n}$ are often denoted by the symbol $p^{1+2n}$. 

**Remark.** Since $G/Z$ is elementary abelian, we have that $Z\geqslant G'$ and $Z\geqslant \Phi(G)$. If $G$ is abelian, then $G\cong \mathbb{Z}_p$, which is impossible. So $G$ is non-abelian and $G',\Phi(G)$ are non-trivial. Therefore, it deduces that $\mathrm{Z}(G)=G'=\Phi(G)\cong \mathbb{Z}_p$ and so $G$ is a [[MATH/Cards/Nodes/Special p-Group\|special p-group]].

If $n$ is a positive integer there are two extraspecial groups of order $p^{1+2n}$, which for $p$ odd are given by
- The [[MATH/Group theory and applications/Nodes/2 Central Product\|central product]] of $n$ extraspecial groups of order $p^3$, all of exponent $p$. This extraspecial group has exponent $p$, denoted by $p_{+}^{1+2m}$. 
	- It is known that $p_{+}^{1+2}\cong\mathrm{SL}_3(p)_p$, where $\mathrm{SL}_3(p)_p$ is a Sylow $p$-subgroup of $\mathrm{SL}_3(p)$. Thus $p_{+}^{1+2m}$ is the central product of $m$ copies of $\mathrm{SL}(3,p)_p$ for odd prime $p$, see [[Li 和 Zhu - 2024 - The finite groups with three automorphism orbits.pdf#page=2&selection=689,2,774,1|here]]. 
	- On the other hand, $p_{+}^{1+2}=\langle a,b|a^p=b^p=c^p=1,[a,b]=c\rangle$, see [[MATH/Cards/Nodes/Structure of p-groups\|here]]. With this definition, it is easy to show that $\mathrm{Aut}(p_{+}^{1+2})\cong \mathrm{GL}_2(p)$. 
	- $\mathrm{Out}(p_{+}^{1+2m})\cong \mathrm{CSp}_{2m}(p)\cong \mathrm{Sp}_{2m}(p){:}\mathbb{Z}_{p-1}$. See [[Li 和 Zhu - 2024 - The finite groups with three automorphism orbits.pdf#page=2&selection=689,2,774,1|here]].
{ #57vzy2}

- The central product of _n_ extraspecial groups of order $p^3$, at least one of exponent $p^2$. This extraspecial group has exponent $p^2$, denoted by $p_{-}^{1+2m}$. 

When $p=2$, 
- there are two extraspecial groups of order $8=2^3$, which are given by:
	- The dihedral group $D_8$, which has $2$ elements of order $4$.
	- The quaternion group $Q_8$, which has $6$ elements of order $4$.
- If $n$ is a positive integer there are two extraspecial groups of order $2^{1+2n}$, which are given by
	- The central product of $n$ extraspecial groups of order $8$, an **odd** number of which are quaternion groups.
	- The central product of $n$ extraspecial groups of order $8$, an **even** number of which are quaternion groups.

