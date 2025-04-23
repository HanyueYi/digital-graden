---
{"dg-publish":true,"aliases":["composition series"],"permalink":"/Representation Theory 101/Nodes/Composition Series of Modules/","dgPassFrontmatter":true}
---


> [!definition] [wiki](https://en.wikipedia.org/wiki/Composition_series#For_modules)
> Given a ring $R$ and an $R$-module $M$, a composition series for $M$ is a series of submodules 
> 
> $$\{0\}=J_0\subseteq \cdots\subseteq J_n=M$$
> 
> where all inclusions are strict and $J_k$ is a maximal submodule of $J_{k+1}$ for each $k$. 

**Remark.**
- The [[MATH/Cards/Nodes/Composition Series\|Jordan-Holder theorem]] holds.
- A module has a finite composition series if and only if it is both an [[Artinian module\|Artinian module]] and a [[Noetherian module\|Noetherian module]].

To show a composition series is unique:
- For a module $U$ and a composition factor $M$, consider $\mathrm{Hom}(U,M)$ and $\mathrm{Hom}(M,U)$. As an example, see [[Three Orbits Linear Groups/Nodes/5.5 Module Decomposition of SL\|5.5 Module Decomposition of SL]].
- Suppose $0\subseteq M_1\subseteq M_2$ is a composition series. If it is not unique, then there is another composition series $0\subseteq M_1'\subseteq M_2$. Take $x$ such that $x\in M_1'$ and $x\notin M_1$. Then the minimal submodule containing $x$ is $\left\langle x^G\right\rangle$. To show $0\subseteq M_1\subseteq M_2$ is the unique composition series, it suffices to show $\left\langle x^G\right\rangle=M_2$. 
