---
{"dg-publish":true,"draft":false,"permalink":"/MATH/Cards/Nodes/Uniqueness of Block System of Imprimitive Rank 3 Group/","dgPassFrontmatter":true}
---


> [!lemma]
> Assume that $G\leqslant\mathrm{Sym}(\Omega)$ is a finite imprimitive rank $3$ group. Then $G$ has a unique non-trivial proper block system $\mathcal{B}$.

**_Proof._**
Let $\alpha\in \Omega$, and let $n=|\Omega|$. Then $G_{\alpha}$ has three orbits: $\{\alpha\}$, $\Gamma_\alpha$ and $\Delta_\alpha$. We claim that a non-trivial proper block containing $\alpha$ is either $\{\alpha\}\cup\Gamma_\alpha$ or $\{\alpha\}\cup\Delta_\alpha$. Let $B$ be a block containing $\alpha$ such that $B\neq\{\alpha\}$ or $\Omega$. Then $B^{G_\alpha}=B$ as $\alpha\in B^{G_\alpha}$. It follows that $B$ is a union of some orbits of $G_\alpha$. Thus, either $B=\{\alpha\}\cup\Gamma_\alpha$ or $B=\{\alpha\}\cup\Delta_\alpha$. 

Assume that $|\Gamma_\alpha|=k$ and $|\Delta_\alpha|=\ell$. Then $n=1+k+\ell$. We may assume that $k\leqslant \ell$. If $\{\alpha\}\cup \Delta_\alpha$ is a block, then $1+k+\ell$ is divided by $\ell +1$, which is impossible. Hence, $\{\alpha\}\cup \Gamma_\alpha$ is the unique non-trivial proper block containing $\alpha$.
<p align="left">□</p>

**Remark.** This also tells us that $|\Gamma_\alpha|\neq |\Delta_\alpha|$ if $G$ is imprimitive. 

ref: [[Literature/Nodes/higmanFinitePermutationGroups1964\|higmanFinitePermutationGroups1964]]

