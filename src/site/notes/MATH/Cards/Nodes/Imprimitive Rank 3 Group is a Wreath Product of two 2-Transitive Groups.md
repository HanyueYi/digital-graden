---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Imprimitive Rank 3 Group is a Wreath Product of two 2-Transitive Groups/","dgPassFrontmatter":true}
---

#TERMS/rank-3 #TERMS/imprimitive #RESOURCE/cards 


<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



$G$ can be seen as a subgroup of a wreath product: Let $G$ be a transitive imprimitive group acting on a set $\Omega$, and suppose that $G$ preserves a non-trivial block-system $B\in\mathcal B$ and identify $\Omega$ with the set $B\times\{1,\cdots,n\}$ where $n=|\mathcal B|$. [[Pasted image 20240205122710.png|Then]] view $G$ as a subgroup of the wreath product $H\wr X$ where $G^\mathcal B\cong X\leq S_n$ and $H:=G_B^B$ is called the component of $G$. 

</div></div>


> [!lemma]
> Let $B$ be a set and suppose that $G\leqslant \mathrm{Sym}(B)\wr S_n$ is transitive of rank $3$. Then both $G_B^B$ and the projection $X$ of $G$ to $S_n$ are $2$-transitive.

**_Proof._**
Let $\alpha\in B$. Then $G_{(\alpha,1)}$ has $3$ orbits on the points of $B\times\{1,\cdots,n\}$. Since $B_1=B\times\{1\}$ is a block for $G$, any orbit intersecting non-trivially with $B_1\setminus\{(\alpha,1)\}$ is contained in $B_1$. Hence, the $3$ orbits of $G_{(\alpha,1)}$ are $\{(\alpha,1)\}$, $B_1\setminus\{(\alpha,1)\}$ and $B\times\{2,\cdots,n\}$. It yields that $(G_B^B)_\alpha$ is transitive on $B\setminus\{\alpha\}$ and so $G_B^B$ is $2$-transitive on $B$. Moreover, as $(G^{\mathcal B})_1$ is transitive on $\{2,\cdots,n\}$, we have $G^\mathcal B$ is $2$-transitive.
<p align="left">□</p>

ref: [[Literature/Nodes/devillersImprimitiveRankPermutation2011\|devillersImprimitiveRankPermutation2011]]