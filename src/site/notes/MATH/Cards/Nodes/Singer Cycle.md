---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Singer Cycle/","dgPassFrontmatter":true}
---


# From Finite Field

> [!definition]
> Let $F=\mathbb{F}_q$ where $q=p^f$, and let $\rho$ be a generator of $F^\times$. The transformation on $\mathbb{F}_q^+\cong \mathbb{F}_p^f$ induced by $\rho$ is called a *Singer cycle*.

> [!proposition]
> Define $G:=F^+{:}\left\langle\rho\right\rangle=\mathbb{Z}_p^f{:}\mathbb{Z}_{p^f-1}\leqslant \mathrm{Hol}(F^+)=\mathbb{Z}_p^f{:}\mathrm{GL}_f(p)$, where for any $a\in F^+$ and $b\in F^\times$, $a^b:=a\cdot b$. Then 
> - $G$ is sharply $2$-transitive on $F^+$; and
> - $\mathrm{Aut}(G)=G{:}\left\langle\tau\right\rangle$ where $\tau$ is the Frobenius automorphism acting on $\mathbb{Z}_{p^f-1}$.
{ #t1vo0l}


**_Proof._**
i) For any distinct ordered pairs $(w_1,w_2)$ and $(v_1,v_2)$ in $F^+\times F^+$, there is $ab\in G$ such that $(w_i+a)\cdot b=v_i$. Then $(v_1-v_2)=(w_1-w_2)\cdot b$ yields that $b$ is unique and so for $a$.

ii) See [[MATH/Cards/Nodes/Affine Group\|here]]. 

<p align="left">□</p>

# From Linear Group

> [!definition]
> A *Singer cycle* of $\mathrm{GL}_n(q)$ is an element of order $q^n-1$.

> [!theorem] [[Kantor - 1980 - Linear groups containing a singer cycle.pdf]]
> If $G$ is a subgroup of $\mathrm{GL}(n,q)$ containing a singer cycle, then $G\rhd\mathrm{GL}(n/s,q^s)$ for some $s$, embedded naturally in $\mathrm{GL}_n(q)$.

