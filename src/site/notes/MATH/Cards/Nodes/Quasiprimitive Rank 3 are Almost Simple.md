---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Quasiprimitive Rank 3 are Almost Simple/","dgPassFrontmatter":true}
---

#TERMS/quasiprimitive #TERMS/rank-3 #TERMS/almost-simple 

> [!proposition]
> Let $G$ be a quasiprimitive but not primitive group. Then $G$ is almost simple.

**_Proof._**
By [[MATH/Cards/Nodes/Imprimitive Rank 3 Group is a Wreath Product of two 2-Transitive Groups\|Imprimitive Rank 3 Group is a Wreath Product of two 2-Transitive Groups]], group $G$ is isomorphic to $G_B^B{:}G^{\mathcal B}$, where $G_B^B$ and $G^\mathcal B$ are $2$-transitive groups. If $G^\mathcal B$ is affine, then there is $N\lhd G^\mathcal B$ such that $N$ is regular on $\mathcal B$. Then the orbits of $N$ on $\Omega$ forms a different block system, which is impossible by [[MATH/Cards/Nodes/Uniqueness of Block System of Imprimitive Rank 3 Group\|Uniqueness of Block System of Imprimitive Rank 3 Group]]. So $G^\mathcal B$ is almost simple. 

We claim that $G\cong G^\mathcal B$. Otherwise, there is a nontrivial normal subgroup $M$ such that $G^\mathcal B\cong G/M$. Since $M$ is the kernel of $G$ acting on $\mathcal B$, it is not transitive on $\Omega$, contradiction. Therefore, it yields that $G\cong G^\mathcal B$ is almost simple.
□

ref: [[Literature/Nodes/devillersImprimitiveRankPermutation2011\|devillersImprimitiveRankPermutation2011]], Lemma 3.3 and Corollary 3.4. 