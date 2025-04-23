---
{"dg-publish":true,"permalink":"/有限群导引/Nodes/Double Cosets/","dgPassFrontmatter":true}
---


> [!definition]
> Let $H,K$ be subgroups of group $G$. The set $HaK$ is called a double cosets of $H$ and $K$.


> [!proposition]
> For any $H,K\leqslant G$, there exists $a_1,\cdots,a_s$ such that 
> 
> $$G=Ha_1K\sqcup\cdots\sqcup Ha_sK.$$


> [!theorem]
> Any double coset $HaK$ can be written as unions of $m$ right cosets of $H$, or unions of $n$ left cosets of $K$, where $m=|K:H^a\cap K|$ and $n=|H^a:H^a\cap K|$. 

**_Proof._**
For any $g\in HaK$, there is $Hg\subseteq H(HaK)=HaK$. Assume that $HaK$ contains $m$ right cosets of $H$, then $n=|HaK|/|H|$. Note that 

$$|HaK|=a^{-1}HaK=H^aK=\frac{|H^a||K|}{|H^a\cap K|}=\frac{|H||K|}{|H^a\cap K|},$$

and it deduces that $m=|K|/|H^a\cap K|=|K:H^a\cap K|$.
<p align="right">□</p>


**Remark.** In particular, when $H=K$, we say $HaH$ is a $H$-double coset, and the number of double cosets coincides with the rank of $H\leqslant G$ on $[G:H]$. See [[Literature/Nodes/bannaiMaximalSubgroupsLow1972#^f1n6qy\|here]]. 

