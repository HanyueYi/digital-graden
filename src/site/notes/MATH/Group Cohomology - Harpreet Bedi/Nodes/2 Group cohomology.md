---
{"dg-publish":true,"permalink":"/MATH/Group Cohomology - Harpreet Bedi/Nodes/2 Group cohomology/","dgPassFrontmatter":true}
---


> [!definition] cochain
> The $i$th cochain for a $G$-module $A$ is defined as functions from $G^i$ to $A$
> 
> $$C^i(G,A)=\{f:G^i\to A\},$$
> 
> where $G^i=G\times\cdots\times G$ is a product of i $G$'s. In addition, we set $C^0(G,A)=A$.

> [!definition] differential
> The differential $d^i$ mapping $C^i(G,A)$ to $C^{i+1}(G,A)$ is defined by 
> 
> $$\begin{aligned}
(d^if)(g_0,\cdots,g_i)&=g_0f(g_1,\cdots,g_i)\\
&+\sum_{j=1}^i(-1)^if(g_0,\cdots,g_{j-2},g_{j-1}g_j,g_{j+1},\cdots,g_i)\\
&+(-1)^{i+1}f(g_0,\cdots,g_{i-1}).
\end{aligned}$$

**Remark.** Note that for a $\gamma\in C^1(G,A)$, $d\gamma(g,h)=g\gamma(h)-\gamma(gh)+\gamma(g)$. This is called *cocycle condition* by [[Literature/Nodes of Textbooks/Section 17-Aschbacher#^n7ec3u\|Aschbachar]].

We can check that $d^{i+1}\circ d^i=0$. 

> [!definition] cohomology
> Denote $Z^i(G,A)=\ker d^i$ and $B^i(G,A)=\mathrm{im}d^{i-1}$. The $i$-th cohomology group is defined to be
> 
> $$H^i(G,A)=\frac{Z^i(G,A)}{B^{i}(G,A)}.$$



