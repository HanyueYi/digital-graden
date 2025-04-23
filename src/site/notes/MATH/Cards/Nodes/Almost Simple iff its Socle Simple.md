---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Almost Simple iff its Socle Simple/","dgPassFrontmatter":true}
---


> [!proposition]
> $G$ is an almost simple group iff $\mathrm{soc}\space G$ is simple.

**_Proof._**
Suppose $G$ is almost simple. Then there is a simple group $T$ such that $T\lhd G\leq\mathrm{Aut}(T)$. Since $T$ is a minimal normal subgroup, $T\leq\mathrm{soc}\space G$. Assume $T'$ is another minimal normal subgroup. Then $[T,T']\leq T\cap T'=\{1\}$ yields $T'\leq C_G(T)$. For any $t\in T$, define $\varphi_t\in\mathrm{Aut}(T)$ by $\varphi_t:t_0\mapsto t^{-1}t_0t$. Then $g^{-1}\varphi_t g=\varphi_t$ for any $g\in C_G(T)$. And for any $x\in T$, $$t^{-1}xt=x^{\varphi_t}=x^{g^{-1}\varphi_tg}=(t^{-1}x^{g^{-1}}t)^g=(t^g)^{-1}xt^g$$yields $t(t^{g})^{-1}\in Z(T)=1$. Hence $t^g=t$, i.e. $g\in\mathrm{Aut}(T)$ acts on $T$ trivially. Therefore, $g=1$ and so $C_G(T)=1$. So $T'$ is trivial and $T$ is the unique minimal normal subgroup. In the other word, $\mathrm{soc}\space G=T$ is simple.

Conversely, suppose $\mathrm{soc}(G):=N$ is simple. If $C_G(N)\neq 1$, then $C_G(N)\lhd G$ contains a minimal normal subgroup of $G$, which must be $N$. It is impossible because $N$ is non-abelian. Therefore, $C_G(N)=1$. By NC lemma there is 

$$G=G/C_G(N)=N_G(N)/C_G(N)\lesssim\mathrm{Aut}(N)$$

and so $G$ is almost simple.
<p align="left">□</p>
