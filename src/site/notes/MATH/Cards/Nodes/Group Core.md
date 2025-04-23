---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Group Core/","dgPassFrontmatter":true}
---


# Definitions

> [!definition]
> For a group $G$, the *normal core* of a subgroup $H$ is the largest normal subgroup of $G$ that is contained in $H$, i.e. $\mathrm{Core}_G(H)=\cap_{g\in G}g^{-1}Hg$. Moreover, if $\mathrm{Core}_G(H)=1$, we say $H$ is *core-free*.

> [!definition]
> For a prime $p$, the *$p$-core* of a finite group is defined to be its largest normal $p$-subgroup, denoted by $O_p(G)$.

> [!definition]
> The *solvable radical* of $G$ is defined to be the largest solvable normal subgroup, and is denoted $O_\infty(G)$.

**Remark.** "Core" means the largest normal subgroup with some properties, like containing some subgroup, being a $p$-group, or solvable.

# Core-free and Faithful Coset Action

Let $G$ be a finite group, and let $\Omega:=[G:H]$ where $H<G$. Then
- $G_{(\Omega)}=\mathrm{Core}_G(H)$, and
- $G/\mathrm{Core}_G(H)\cong G^\Omega$.

> [!lemma]
> If $H\leqslant G$ is core-free, then $G$ acting on $[G:H]$ is faithful.

**_Proof._**
If there is a $g\in G$ such that $Hg_ig=Hg_i$ for all $g_i\in G$, then $g^G\in H$ and $g\in \cap_{g_i\in G} H^{g_i}=\mathrm{Core}_G(H)=\{1\}$. Therefore, $g=1$ and so the action is faithful.
<p align="right">□</p>

# Properties of $p$-core

> [!proposition]
> Note that $O_p(G)$ is the intersection of all Sylow $p$-groups of $G$, and the following holds:
> - $O_p(G)$ is the normal core of every Sylow $p$-subgroup of the group $G$.
> - $O_p(G)\lhd_{\mathrm{char}} G$ and $\overline G:=G/O_p(G)$ is such that $O_p(\overline G)=1$. 
> - If $\pi(G)=\{p_1,\cdots,p_k\}$, then its [[MATH/Cards/Nodes/Fitting Subgroups\|Fitting subgroups]] is $O_{p_1}(G)\times\cdots\times O_{p_k}(G)$.

**_Proof._**
i) Easy.

ii) Since $O_p(G)$ is the intersection of all Sylow $p$-subgroups, then $O_p(G)\lhd_{\mathrm{char}} G$. Suppose $\overline{P_1},\cdots,\overline {P_k}$ are all Sylow $p$-subgroups of $\overline G$, and suppose $P_i$ are preimage of $\overline{P_i}$. Then $\cap_{i=1}^kP_i\leqslant O_p(G)$ and so $\cap_{i=1}^k\overline{P_i}=1$, i.e., $O_p(\overline G)=1$. 

iii) See [[MATH/Cards/Nodes/Fitting Subgroups#^mudriu\|here]]. 
<p align="right">□</p>

> [!proposition]
> If $G$ is solvable, then there exists a prime $p$ such that $O_p(G)\neq 1$.
{ #a65a1w}


**_Proof._**
Let $M$ be a minimal normal subgroup of $G$. [[MATH/Cards/Nodes/Minimal Normal Subgroup and Maximal Normal Subgroup\|Then]] $M\cong \mathbb{Z}_p^d$ for some prime $p$ and some positive integer $d$. Thus $O_p(G)$ is not trivial.
<p align="right">□</p>

