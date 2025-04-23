---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Normalizer of p-subgroup/","dgPassFrontmatter":true}
---


# non-Sylow Subgroup

> [!lemma]
> The number of right cosets of $P$ contained in $PxP$ is equal to $|P|/|P^x\cap P|$.

**_Proof._**
Let $S$ be the set of right cosets of $P$ contained in $PxP$. Then for every $s\in S$, there exists $y\in xP$ such that $Py=s$. Suppose $y_1=xp_1$ and $y_2=xp_2$ satisfy $Py_1=Py_2$, then $p_1p_2^{-1}\in x^{-1}Px=P^x$. Therefore, for a fixed $y\in xP$, there are $|P^x\cap P|$ elements $y_i$ in $xP$ such that $Py=Py_i$. Therefore, the number of right cosets of $P$ contained in $PxP$ is equal to $|P|/|P^x\cap P|$. 
<p align="left">□</p>

> [!theorem]
> Let $G$ be finite, and let $P$ be a non-Sylow $p$ subgroup of $G$, then $P< N_G(P)$.
{ #1c3218}


**_Proof._**
Decompose $G$ as $G=\cup_{x\in G}PxP$. Note that 

$$|G|=|P1P|+\cdots+|Px_nP|,$$

and so

$$|G|/|P|=1+|P|/|P^{x_1}\cap P|+\cdots+|P|/|P^{x_n}\cap P|.\tag{*}$$

Since $P$ is not a Sylow $p$-group, then LHS of $(*)$ is divisible by $p$. Thus there exists at least one $i$ such that $|P^{x_i}\cap P|=|P|$. It yields $P^{x_i}=P$ and so $x_i\in N_G(P)$. Therefore, $P< N_G(P)$ by $x_i\notin P$.
<p align="left">□</p>
> [!corollary]
> Let $G$ be a $p$-group. 
> - If $H<G$, then $H<N_G(H)$.
> - If $H<_{\max} G$, then $H\lhd G$ and $|G|/|H|=p$. 
> - If $N$ is a normal subgroup of $G$ and $|N|=p$, then $N\leqslant Z(G)$.

**_Proof._**
i) Since $H<G$, then $H$ is not a Sylow subgroup of $G$ and so $H<N_G(H)$ by [[MATH/Cards/Nodes/Normalizer of p-subgroup#^1c3218\|#^1c3218]]. 

ii) By i), we obtain that $H<N_G(H)$ and so $N_G(H)=G$. Thus $H\lhd G$ and $G/H$ is simple. Therefore, $G/H\cong \mathbb{Z}_p$ by [[MATH/Cards/Nodes/Minimal Normal Subgroup and Maximal Normal Subgroup#^afncdw\|here]] and $|G|/|H|=p$. 

iii) By NC lemma, $G/C_G(N)\leqslant\mathrm{Aut}(N)=\mathbb{Z}_{p-1}$. Thus $C_G(N)=G$, that is, all elements in $G$ commutes with $N$. So $N\leqslant Z(G)$.
<p align="left">□</p>

# Sylow Subgroup

> [!theorem]
> Let $G$ be a finite group and $P<G$ be a Sylow p-subgroup. Let $N_G(P)$ be the normalizer of $P$ in $G$ . Let $H<G$ be a subgroup containing $N_G(P)$. Prove that $N_G(H)=H$.
{ #d0505d}


**_Proof._**
For any $g\in N_G(H)$, there is 

$$g^{-1}Pg\leqslant g^{-1}Hg=H<G.$$

Since $g^{-1}Pg$ and $P$ are Sylow subgroups of $H$, by [[MATH/Cards/Nodes/Sylow Theorems\|Sylow theorem]] there exists $h\in H$ such that $g^{-1}Pg=h^{-1}Ph$. Then $gh^{-1}\in H$ and so $g\in H$. Therefore, $N_G(H)=H$.
<p align="left">□</p>

> [!corollary]
> Let $P$ be a Sylow subgroup of $G$. Then $N_G(P)=N_G\left(N_G(P)\right)$.
{ #srj1g6}


**_Proof._**
By [[MATH/Cards/Nodes/Normalizer of p-subgroup#^d0505d\|#^d0505d]].
<p align="left">□</p>

> [!theorem]
> Let $G$ be a finite group and $p$ be a prime. Let $H$ be a p-subgroup of $G$. Then 
> 
> $$[G:H]\equiv[N_G(H):H]\mod p.$$

**_Proof._**
Let a group $G$ act on a finite set $X$; then

$$|X|=|\mathrm{Fix}(X)|+\sum[G: C(x)]$$

where $C(x)=\{g \in G: g x=x\}$ for every $x \in X$, and the sum is over a system of representatives of all distinct nontrivial $G$-orbits on $X$. 

In this case let $H$ act on $[G:H]$. If $Hg$ is fixed for all $h \in H$, we have

$$Hgh=Hg$$

which means that

$$ghg^{-1}\in H$$

and clearly this holds for all $h \in H$ if and only if $g \in N_G(H)$. Since $Hg=Hg_1$ iff $g_1^{-1} g \in H$, the number of fixed cosets is $\left[N_G(H): H\right]$. 

Since $H$ is a $p$-group, $[H:C(x)]$ is divided by $p$. Now we finish the proof.
<p align="left">□</p>
