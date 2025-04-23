---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/a Lemma of Cohomology/","dgPassFrontmatter":true}
---


> [!lemma] [[Aschbacher 和 Guralnick - 1984 - Some applications of the first cohomology group.pdf#page=5&selection=514,1,514,5|Aschbacher 和 Guralnick - 1984 - Some applications of the first cohomology group, Lemma 2.7(a)]]
> Let $V$ be a $G$-module. If $N\lhd G$ and $C_V(N)=0$, then $|\mathrm H^1(G,V)|\leqslant|\mathrm H^1(N,V)|$.
{ #uexqcl}


**_Proof._**
Suppose $G_0$ is a complement of $V$ in $V{:}G$. Then $N_0:=G_0\cap (V{:}N)$ is a complement of $V$ in $V{:}N$ and $N_0\lhd G_0$. Claim that $G_0=N_{V{:G}}(N_0)$. Otherwise, there exists a nontrivial $v\in V$ such that $N_0^v=N_0$ and so $v\in C_V(N_0)$. Since $H^0(N,V)=0$, we have $\{0\}=C_V(N)=C_V(N_0)$, which conducts a contradiction. Let $\Gamma$ and $\varGamma$ be the complements of $V$ in $V{:}G$ and $V{:}N$, respectively. Then by $G_0=N_{V{:G}}(N_0)$ the map 

$$\begin{aligned}
\varphi:\Gamma&\to\varGamma,\\
G_0&\mapsto N_0=G_0\cap (V{:}N)
\end{aligned}$$

is injective and so $|\mathrm H^1(G,V)|\leqslant |\mathrm H^1(N,V)|$.
<p align="right">□</p>
