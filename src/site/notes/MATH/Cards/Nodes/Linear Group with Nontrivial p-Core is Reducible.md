---
{"dg-publish":true,"draft":false,"permalink":"/MATH/Cards/Nodes/Linear Group with Nontrivial p-Core is Reducible/","dgPassFrontmatter":true}
---

#TERMS/p-core #TERMS/reducible 

> [!proposition]
> Let $G\leqslant\mathrm{GL}(n,p)$ be a linear group. If $O_p(G)\neq 1$, then $G$ is reducible.

**_Proof._**
Let $N:=O_p(G)$ be the [[MATH/Cards/Nodes/Group Core\|$p$-core]] of $G$, that is, the largest normal $p$-subgroup of $G$. Then $X:=V{:}G$ has a normal subgroup $Y:=V{:}N$. Since $Y$ is a $p$-group, the center $Z(Y)$ is non-trivial and it is easy to verify that $Z(Y)\lhd V$. Thus, $Z(Y)$ is a non-trivial subspace of $\mathbb{F}_p^n$. For any $g\in G$, $n\in N$ and $z\in Z(Y)$, there is $(z^{g})^n=z^{gng^{-1}g}=z^g$ and so $z^g\in Z(Y)$. Consequently, $Z(Y)$ is fixed by $G$ and so $G$ is reducible.
<p align="left">□</p>