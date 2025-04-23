---
{"dg-publish":true,"aliases":["nilpotent","lower central series","central series","upper central series"],"permalink":"/MATH/Cards/Nodes/Nilpotent Group/","dgPassFrontmatter":true}
---


> [!definition] lower central series
> We say $G$ is a *nilpotent group* if it has a lower central series terminating in the trivial subgroup after finitely many steps. That is, a series of normal subgroups 
> 
> $$G=G_0\rhd G_1\rhd\cdots\rhd G_n=\{1\} $$
> 
> where $G_{i+1}=[G_i,G]$. The length of the lower central series $n$ is called the *nilpotency class* of $G$.

> [!definition] central series
> A group $G$ is called *nilpotent* if it has a chain of subgroups, which is called a *central series*,
>
> $$G=K_0>K_1>\cdots>K_{n}=1$$
> 
> such that $K_i\lhd G$ and $K_{i}/K_{i+1}\leqslant Z(G/K_{i+1})$.

> [!definition] upper central series
> A group $G$ has an upper central series terminating in the whole group after finitely many steps. That is, a series of normal subgroups
> 
> $$\{1\}=Z_0 \triangleleft Z_1 \triangleleft \cdots \triangleleft Z_n=G$$
> 
> where $Z_1=Z(G)$ and $Z_{i+1}$ is the subgroup such that $Z_{i+1} / Z_i=Z\left(G / Z_i\right)$.

> [!definition] nilpotency class
> For a nilpotent group, the smallest $n$ such that $G$ has a central series of length $n$ is called the *nilpotency class* of $G$; and $G$ is said to be nilpotent of class $n$.
> 
>  Equivalently, the nilpotency class of $G$ equals the length of the lower central series or upper central series.

**Observations.**
{ #0b8777}

- A nilpotent group is a solvable group.
- For any prime $p$, a $p$-group is a nilpotent group.
- Direct product of two nilpotent groups is nilpotent.
- $A_4$ and $S_4$ are not nilpotent.
- Note that $Z_{n-i}\geqslant K_{i}\geqslant G_i$. (Maybe that's why they are called upper/lower central series.)


> [!theorem]
> The followings are equivalent:
> - $G$ is nilpotent.
> - if $H<G$, then $N_G(H)>H$.
> - each maximal subgroup of $G$ is normal and of prime index.
> - $G$ is a direct product of its Sylow subgroups.
{ #9gfd7n}



**_Proof._**
Assume (i) holds. Then $G$ has a central series

$$G=K_1>K_2>\cdots>K_{s+1}=1.$$

Let $H<G$. Then there exists $i$ such that $H\geqslant K_{i+1}$ and $H\not\geq K_i$. It yields that $[H/K_{i+1},Z(G/K_{i+1})]=1$. So for any $h\in H$ and $y\in K_i$, there is $(hK_{i+1})(yK_{i+1})=(yK_{i+1})(hK_{i+1})$ and so $hy=(yc_1)(hc_2)$ for some $c_1,c_2\in K_{i+1}$. We have

$$(yc_1)(hc_2)=yhc_1^hc_2=yhc_1'c_2\in yhK_{i+1}.$$

So $y^{-1}hy=hc_1'c_2\in HK_{i+1}=H$, i.e. $y\in N_G(H)$ and $K_i\leqslant N_G(H)$. Thus $N_G(H)\geqslant HK_i>H$, as in (ii).

Assume (ii) holds. Let $M$ be a maximal subgroup of $G$. Then $M\lhd N_G(M)\leqslant G$ and so $M\lhd G$. The factor group $G/M$ does not have a proper subgroup as $M$ is maximal. So $|G/M|$ is a prime, as in (iii).

Assume (iii) holds. Let $P\in\mathrm{Syl}_p(G)$. If $P$ is not normal in $G$, then $P<G$ and $P<N_G(P)<G$. Let $M$ be a maximal subgroup of $G$ such that $N_G(P)\leqslant M<G$. Then $M\lhd G$. By [[MATH/Cards/Nodes/Frattini's Argument\|Frattini's argument]], $G=N_G(P)M=M$, a contradiction. Hence, $P\lhd G$ and so $G$ is a direct product of Sylow subgroups.

Assume (iv) holds. [[#^0b8777|Since]] $p$-group is nilpotent and direct product of nilpotent groups is nilpotent, we obtain (i). 
<p align="right">□</p>

**Remark.** [[MATH/Cards/Nodes/Normalizer of p-subgroup#^srj1g6\|Note]] that $N_G(N_G(P))=N_G(P)$ for any Sylow $p$-subgroup. So (ii)->(iv) is easy. 