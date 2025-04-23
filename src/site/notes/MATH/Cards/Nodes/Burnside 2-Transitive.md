---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Burnside 2-Transitive/","dgPassFrontmatter":true}
---


> [!theorem]
> A $2$-transitive permutation group $G$ has a unique minimal normal subgroup which is either:
> - non-abelian simple group, where $G$ is called almost simple;
> - elementary abelian, where $G$ is called affine.

**_Proof._**
#todo By [[MATH/Cards/Nodes/Burnside 2-Transitive#^e3ccf0\|#^e3ccf0]], $\mathrm{soc}(G)\cong T^n$ with simple group $t$ and some $n\in \mathbb{N}_+$. If $\mathrm{soc}(G)\cong \mathbb{F}_p^n:=V$, then by [[MATH/Cards/Nodes/Frattini's Argument\|Frattini's Argument]] we have $G=V{:}G_0$ where $G_0\leq \mathrm{GL}(V)$. Therefore, $G$ is affine. 

Now we assume that $\mathrm{soc}(G)$ is a direct product of isomorphic non abelian simple groups. 

(to be continued)

□

> [!lemma]
> If $G\leqslant \mathrm{Sym}(\Omega)$ is a $2$-transitive permutation group, then $G$ has a unique minimal normal subgroup.
{ #e3ccf0}


**_Proof._**
Suppose that $K_1$ and $K_2$ are minimal normal subgroups of $G$. Then $K_1$ and $K_2$ are transitive by [[MATH/Cards/Nodes/Orbits of Normal Subgroups Form a Block System\|Orbits of Normal Subgroups Form a Block System]]. Since $K_1\cap K_2=\{1\}$, we have $K_1\leqslant C_G(K_2)$ and $K_2\leqslant C_G(K_1)$. It yields that $C_G(K_1)=K_2$ and $C_G(K_2)=K_1$ are regular normal subgroups of $G$ by [[MATH/Cards/Nodes/Minimal Normal Subgroups of Permutation Groups\|Minimal Normal Subgroups of Permutation Groups]]. Then we have $G=K_1{:}G_\omega$ and so $G_\omega$ acting on $\Omega$ can be identified by $G_\omega$ acting $K_1$ by conjugation.

If $K_1$ is solvable, then $K_1$ is elementary abelian. It contradicts with $C_G(K_1)=K_2$ and $K_1\cap K_2=\{1\}$. If $K_1$ is nonsolvable, then $|K_1|$ has at least $3$ prime divisors $r,s,t$ by [[MATH/Cards/Nodes/Burnside's Theorem\|Burnside's Theorem]]. Let $x,y,z$ be elements of $K_1$ such that $|x|=r$, $|y|=s$ and $|z|=t$. Then $x^{G_\omega}$, $y^{G_\omega}$ and $z^{G_\omega}$ are three orbits and $\mathrm{rank}(G)\geqslant 4$, which is impossible. Therefore, the minimal normal subgroup of $G$ is unique.
□