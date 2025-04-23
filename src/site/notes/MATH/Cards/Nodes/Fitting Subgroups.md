---
{"dg-publish":true,"aliases":["Fitting subgroups"],"permalink":"/MATH/Cards/Nodes/Fitting Subgroups/","dgPassFrontmatter":true}
---


> [!definition]
> The product of all normal nilpotent subgroups of $G$ is called the *Fitting subgroup* of $G$, denoted by $\mathrm F(G)$. 

Note that $\Phi(G)$ is a normal nilpotent subgroup. So $\Phi(G)\leqslant\mathrm{F}(G)$.

> [!theorem]
> Let $G$ be a **solvable** group, and let $F=\mathrm F(G)$. Then:
> - $F=O_{p_1}(G)\times\cdots\times O_{p_k}(G)$.
> - $C_G(F)\leqslant F$, i.e., $F$ is self-centralizing. Moreover, we have $F/C_G(F)\leqslant\mathrm{Aut}(F)$.
{ #mudriu}


**_Proof._**
(i) Let $N$ be a nilpotent normal subgroup of $G$. Then $N=Q_1\times\cdots\times Q_t$ where $Q_i$ are Sylow subgroups. Now $Q_i\lhd_{\mathrm{char}} N\lhd G$ and so $Q_i\lhd G$. Then $Q_i\leqslant O_{p_i}(G)$ and $N\leqslant O_{p_1}(G)\times\cdots\times O_{p_k}(G)$. By the arbitrary of $N$, we have that $F\leqslant O_{p_1}(G)\times\cdots\times O_{p_k}(G)$. On the other hand, since $O_{p_1}(G)\times\cdots\times O_{p_k}(G)$ is a nilpotent normal subgroup, $F\geqslant O_{p_1}(G)\times\cdots\times O_{p_k}(G)$. Therefore, we obtain that $F=O_{p_1}(G)\times\cdots\times O_{p_k}(G)$. 

(ii) See [here](https://groupprops.subwiki.org/wiki/Solvable_implies_Fitting_subgroup_is_self-centralizing). 
<p align="right">□</p>


