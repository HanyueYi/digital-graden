---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Minimal Normal Subgroups of Permutation Groups/","dgPassFrontmatter":true}
---


> [!lemma] [[Bamberg 和 Praeger - 2004 - Finite Permutation Groups with a Transitive Minima.pdf#page=12&selection=14,0,14,10|Finite Permutation Groups with a Transitive Minimal Normal Subgroup, Lemma 5.1]]
> Every finite permutation group $G$ on $\Omega$ has at most two distinct transitive minimal normal subgroups. 
> 
> If $K_1$ and $K_2$ are distinct transitive minimal normal subgroups of $G$, then $C_G(K_1)=K_2$, $C_G(K_2)=K_1$. 
> 
> Moreover, there is an involution of $N_{\mathrm{Sym}(\Omega)}(G)$ that interchanges $K_1$ and $K_2$, and which also centralizes a point stabilizer of $G$.
{ #9gl6q2}


**_Proof._**
#todo Suppose $G$ has three distinct transitive minimal normal subgroups $K_1$, $K_2$ and $K_3$. Then each pair of the $K_i$ intersect trivially and hence $K_2,K_3\leqslant C_G(K_1)$ by [[MATH/Cards/Nodes/Normal Subgroups that Intersect Trivially\|Normal Subgroups that Intersect Trivially]]. However, $C_G(K_1)$ is semiregular by [[MATH/Cards/Nodes/Equivalent Condition of Semiregular\|Equivalent Condition of Semiregular]]. So $K_2$, $K_3$ and $C_G(K_1)$ are regular as $K_i$ are transitive. Consequently, both $K_2$ and $K_3$ equal $C_G(K_1)$, which is impossible.

Suppose now that $K_1$ and $K_2$ are distinct transitive minimal normal subgroups of $G$. As was noted above, $K_1=C_G(K_2)$ and $K_2=C_G(K_1)$, and they are both regular on $\Omega$. 

(to be continued)
<p align="right">□</p>


> [!theorem]
> Suppose $G$ is a solvable group and suppose $G$ acting on $\Omega$ is primitive and transitive. Then the minimal normal subgroup of $G$ is unique.
{ #08ghmq}


**_Proof._**Suppose $M,N$ are two different minimal normal subgroups of primitive $G$. Then $M,N$ are transitive by [[MATH/Cards/Nodes/Orbits of Normal Subgroups Form a Block System\|here]]. By [[MATH/Cards/Nodes/Abelian Transitive Action is Regular\|Abelian Transitive Action is Regular]], we know that $|M|=|N|=|\Omega|$. Note that $M\cap N=\{1\}$. Since $[M,N]\subseteq M\cap N$ by normal, $[M,N]=1$ and so $M$ is in the centralizer of $N$. 

Let $Z$ be the centralizer of $N$. Since $N$ is abelian, $Z\geq N$ and so $Z$ is transitive. For any $\alpha,\beta\in\Omega$, there is $n\in N$ such that $\alpha^n=\beta$. Then $Z_\alpha=Z_\alpha^n=Z_\beta$. By the arbitrary of $\beta$, $Z_\alpha=1$. Thus $Z$ is also regular and so $Z=N$. It contradicts to $M\leq Z$. Hence the minimal normal subgroup is unique.
<p align="right">□</p>





> [!corollary]
> Let $X$ be a quasiprimitive permutation group on a finite set $\Omega$. Then $\mathrm{soc}(B)\cong T^k$ with $k\geq 1$ where $T$ is a simple group. 
{ #7p85qz}


**_Proof._**
By [[#^9gl6q2|Lemma 1]], $X$ has at most two minimal normal subgroup $K_1,K_2$ and they are interchanges by an involution. Thus $K_1\cong K_2$ and so $B=K_1\times K_2\cong T^k$ with $k\geq 1$ where $T$ is a simple group.
<p align="right">□</p>
