---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/PGL(V) Sharply 3-transitive iff n=2/","dgPassFrontmatter":true}
---


> [!proposition]
> Let $G=\mathrm{PGL}_n(q)$, and let $V=\mathbb{F}_q^n$. Then $G$ is sharply $3$-transitive on projective line iff $n=2$.
{ #tiw1p7}


**_Proof._**
Note that $G$ must send $3$ collinear points to $3$ other collinear points. So when $n\geqslant 3$ $G$ is not $3$-transitive.

When $n=2$, any two elements $(v_1,v_2,v_3)$ and $(w_1,w_2,w_3)$ can be mapped to $(e_1,e_2,f_1)$ and $(e_1,e_2,f_2)$ by $g_1$ and $g_2$, respectively. Since $f_i=a_ie_1+b_ie_2$ for $a_i,b_i\in \mathbb{F}_q$, there is a $g=\begin{pmatrix}a_2/a_1 & \\ & b_2/b_1\end{pmatrix}$ such that $\overline g\in G$ satisfying $(e_1,e_2,f_1)^{\overline g}=(e_1,e_2,f_2)$. And $g_1gg_2^{-1}$ is the unique such map that does so.
<p align="left">□</p>