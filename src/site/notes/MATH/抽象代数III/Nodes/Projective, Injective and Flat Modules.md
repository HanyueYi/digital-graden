---
{"dg-publish":true,"draft":false,"permalink":"/MATH/抽象代数III/Nodes/Projective, Injective and Flat Modules/","dgPassFrontmatter":true}
---


> [!definition]
> Let $M$ be an $R$-module. 
> - $M$ is called *projective* $R$-module if $\mathrm{Hom}_R(M,\cdot)$ is exact.
> - $M$ is called *injective* $R$-module if $\mathrm{Hom}_R(\cdot, M)$ is exact.
> - $M$ is called *flat* $R$-module if $M\otimes_R\cdot$ is exact.


> [!theorem]
> The following statements about a left $R$-module $P$ are equivalent.
> - Whenever there is an $R$-epimorphism $M\stackrel{g}{\to}N$, and an $R$-homomorphism $P\stackrel{\gamma}{\to}N$, there exists an $R$-homomorphism $\overline\gamma:P\to M$ such that $\gamma=g\overline\gamma$. (lifting property)
> - For each epimorphism $f:{_R}M\to{}_RN$, the map $\mathrm{Hom}_R(P,M)\to\mathrm{Hom}_R(P,N)$ is an epimorphism.
> - For each bimodule structure ${}_RP_S$, the functor $\mathrm{Hom}_R(P,\cdot):R\mbox{-module}\to S\mbox{-module}$ is exact.
> - For every exact sequence $0\to M\stackrel{f'}{\to}M\stackrel{g}{\to}M''\to 0$ in $R$-module, the sequence $0\to \mathrm{Hom}_R(P,M')\stackrel{\mathrm{Hom}_R(P,f)}{\to}\mathrm{Hom}_R(P,M)\stackrel{\mathrm{Hom}_R(P,g)}{\to}\mathrm{Hom}_R(P,M'')\to 0$ is exact. 
{ #9f21f9}


**_Proof._**
i)->ii) Assume that i) holds, and $f:M\to N$ is an epimorphism. For any $\gamma\in \mathrm{Hom}_R(P,N)$, there exists $\overline \gamma:P\to M$ such that $f\circ \overline\gamma=\gamma$. Thus, the map

$$\mathrm{Hom}_R(P,M)\to \mathrm{Hom}_R(P,N),\overline \gamma\mapsto f\circ \overline \gamma$$

is surjective and so ii) holds. 

ii)->i) Assume that ii) holds, then for any $g:M\to N$, the induced map $\varphi:\mathrm{Hom}_R(P,M)\to\mathrm{Hom}_R(P,N),\tau\mapsto g\circ\tau$ is surjective. For any $\gamma\in\mathrm{Hom}_R(P,N)$, there exists $\overline\gamma\in \mathrm{Hom}(P,M)$ such that $g\circ\overline\gamma=\gamma$ by $\varphi$ surjective. Thus $\overline\gamma$ is what we desired and we proved i).

ii)<->iii) [[MATH/交换代数/Nodes/2 Modules#^jj28ws\|Recall]] that the functor $F = \mathrm{Hom}_R(P, \cdot)$ is always left-exact, so it remains to show that for every epimorphism $g: M \to M''$, the induced map $\mathrm{Hom}_R(P, g): \mathrm{Hom}_R(P, M) \to \mathrm{Hom}_R(P, M'')$ is also an epimorphism. It is exactly ii). Another direction is similar. 

Finally, iv) is equivalent to iii). Now we finish the proof. 
<p align="left">□</p>


> [!theorem]
> The following statements about a (left) $R$-module $P$ are equivalent:
> - $P$ is projective.
> - Every epimorphism $M\stackrel{f}{\to}P$ splits, that is, there exists $R$-homomorphism $g:P\to M$ such that $fg=1_P$.
> - $P$ is isomorphic to a direct summand of a free left $R$-module.
{ #3rkmd6}


**_Proof._**
i) -> ii) Take $\gamma=\mathrm{id}_P:P\to P$ and apply [[MATH/抽象代数III/Nodes/Projective, Injective and Flat Modules#^9f21f9\|#^9f21f9]] i).

ii)->iii) Note that every module is a quotient of free modules, then by [[MATH/抽象代数II/Nodes/2.2 Modules#^qtklfv\|2.2 Modules#^qtklfv]] we finish the proof.

iii)->i) Assume that $P\oplus Q=F$ is a free $R$-module. Note that the free module $F=\oplus_{i\in I}R$ is projective as the functor 

$$M\mapsto\mathrm{Hom}_R(F,M)=\prod_{i\in I}\mathrm{Hom}_R(R,M)=\prod_{i\in I}M$$

is exact. Then $\mathrm{Hom}_R(F,\cdot)=\mathrm{Hom}_R(P,\cdot)\times\mathrm{Hom}_R(Q,\cdot)$ as functors, hence both $P$ and $Q$ are projective.
<p align="left">□</p>


> [!corollary]
> A finitely generated projective $R$-module is a a direct summand of $R^n$ for some $n\in \mathbb{N}_+$. 
{ #ajkzkw}


**_Proof._**
It is a direct corollary of [[MATH/抽象代数III/Nodes/Projective, Injective and Flat Modules#^3rkmd6\|#^3rkmd6]], iii).
<p align="left">□</p>


> [!theorem] Schanuel's lemma
> Let $R$ be a ring with identity. If $0 \rightarrow K \rightarrow P \rightarrow M \rightarrow 0$ and $0 \rightarrow K^{\prime} \rightarrow P^{\prime} \rightarrow M \rightarrow 0$ are short exact sequences of $R$-modules and $P$ and $P^{\prime}$ are projective, then $K \oplus P^{\prime}$ is isomorphic to $K^{\prime} \oplus P$.
{ #vjcaf5}


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

Since $P$ is projective and this sequence splits, so $X \cong K^{\prime} \oplus P$ by [[MATH/抽象代数III/Nodes/Projective, Injective and Flat Modules#^3rkmd6\|#^3rkmd6]]. Similarly, we can write another map $\pi^{\prime}: X \rightarrow P^{\prime}$, and the same argument as above shows that there is another short exact sequence

$$
0 \rightarrow K \rightarrow X \rightarrow P^{\prime} \rightarrow 0
$$

and so $X \cong P^{\prime} \oplus K$. Combining the two equivalences for $X$ gives the desired result.
<p align="left">□</p>


**Remark.** This argument is very similar to the proof of [[MATH/Cards/Nodes/Goursat's Lemma\|Goursat's lemma]]. 
