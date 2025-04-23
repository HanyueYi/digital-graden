---
{"dg-publish":true,"permalink":"/MATH/抽象代数III/Nodes/2 250304 1 -> projective module/","dgPassFrontmatter":true}
---

# Projective, Injective and Flat Modules

> [!definition]
> Let $M$ be an $R$-module. 
> - $M$ is called *projective* $R$-module if $\mathrm{Hom}_R(M,\cdot)$ is exact.
> - $M$ is called *injective* $R$-module if $\mathrm{Hom}_R(\cdot, M)$ is exact.
> - $M$ is called flat $R$-module if $M\otimes_R\cdot$ is exact.


> [!theorem]
> The following statements about a left $R$-module $P$ are equivalent.
> - Whenever there is an $R$-epimorphism $M\stackrel{g}{\to}N$, and an $R$-homomorphism $P\stackrel{\gamma}{\to}N$, there exists an $R$-homomorphism $\overline\gamma:P\to M$ such that $\gamma=g\overline\gamma$.
> - For each epimorphism $f:{_R}M\to{}_RN$, the map $\mathrm{Hom}_R(P,M)\to\mathrm{Hom}_R(P,N)$ is an epimorphism.
> - For each bimodule structure ${}_RP_S$, the functor $\mathrm{Hom}_R(P,\cdot):R\mbox{-module}\to S\mbox{-module}$ is exact.
> - For every exact sequence $M\stackrel{f'}{\to}M\stackrel{g}{\to}M''$ in $R$-module, the sequence $\mathrm{Hom}_R(P,M')\stackrel{\mathrm{Hom}_R(P,f)}{\to}\mathrm{Hom}_R(P,M)\stackrel{\mathrm{Hom}_R(P,g)}{\to}\mathrm{Hom}_R(P,M'')$ is exact. 
{ #9f21f9}


**_Proof._**
Not too hard.
□


> [!theorem]
> The following statements about a (left) $R$-module $P$ are equivalent:
> - $P$ is projective.
> - Every epimorphism $M\stackrel{f}{\to}P$ splits, that is, there exists $R$-homomorphism $g:P\to M$ such that $fg=1_P$.
> - $P$ is isomorphic to a direct summand of a free left $R$-module.
{ #3rkmd6}


**_Proof._**
i) -> ii) By [[#^9f21f9]] i), take $\gamma=\mathrm{id}_P:P\to P$. 

ii)->iii) Note that every module is a quotient of free modules, then by [[MATH/抽象代数II/Nodes/2.2 Modules#^qtklfv\|2.2 Modules#^qtklfv]] we finish the proof.

iii)->i) Assume that $P\oplus Q=F$ is a free $R$-module. Note that the free module $F=\oplus_{i\in I}R$ is projective as $\mathrm{Hom}_R(F,M)=\prod_{i\in I}M$ and the functor $M\mapsto\prod_{i\in I}M$ is exact. Then $\mathrm{Hom}_R(F,\cdot)=\mathrm{Hom}_R(P,\cdot)\times\mathrm{Hom}_R(Q,\cdot)$ as functors, hence both $P$ and $Q$ are projective.
□

> [!corollary]
> A finitely generated projective $R$-module is a a direct summand of $R^n$ for some $n\in \mathbb{N}_+$. 
{ #ajkzkw}



> [!theorem] Schanuel's lemma
> Let $R$ be a ring with identity. If $0 \rightarrow K \rightarrow P \rightarrow M \rightarrow 0$ and $0 \rightarrow K^{\prime} \rightarrow P^{\prime} \rightarrow M \rightarrow 0$ are short exact sequences of $R$-modules and $P$ and $P^{\prime}$ are projective, then $K \oplus P^{\prime}$ is isomorphic to $K^{\prime} \oplus P$.

**_Proof._**
Define the following submodule of $P \oplus P^{\prime}$, where $\phi: P \rightarrow M$ and $\phi^{\prime}: P^{\prime} \rightarrow M$ 

$$X=\left\{(p, q) \in P \oplus P^{\prime}: \phi(p)=\phi^{\prime}(q)\right\}.$$

The map $\pi: X \rightarrow P$, where $\pi$ is defined as the projection of the first coordinate of $X$ into $P$, is surjective. Since $\phi^{\prime}$ is surjective, for any $p \in P$, one may find a $q \in P^{\prime}$ such that $\phi(p)=\phi^{\prime}(q)$. This gives $(p, q) \in X$ with $\pi(p, q)=p$. Now the kernel of the map $\pi$ is

$$\begin{aligned}\operatorname{ker} \pi & =\{(0, q):(0, q) \in X\} \\
& =\left\{(0, q): \phi^{\prime}(q)=0\right\} \\
& \cong \operatorname{ker} \phi^{\prime} \cong K^{\prime}.
\end{aligned}$$

We may conclude that there is a short exact sequence

$$0 \rightarrow K^{\prime} \rightarrow X \rightarrow P \rightarrow 0.$$

Since $P$ is projective and this sequence splits, so $X \cong K^{\prime} \oplus P$ by [[#^3rkmd6]]. Similarly, we can write another map $\pi^{\prime}: X \rightarrow P^{\prime}$, and the same argument as above shows that there is another short exact sequence

$$
0 \rightarrow K \rightarrow X \rightarrow P^{\prime} \rightarrow 0
$$

and so $X \cong P^{\prime} \oplus K$. Combining the two equivalences for $X$ gives the desired result.
□
