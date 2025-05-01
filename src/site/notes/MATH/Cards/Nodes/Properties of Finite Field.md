---
{"dg-publish":true,"draft":false,"permalink":"/MATH/Cards/Nodes/Properties of Finite Field/","dgPassFrontmatter":true}
---


> [!proposition]
> $\mathbb{F}_{p^s}$ is a subfield of $\mathbb{F}_{p^r}$ if and only if $s \mid r$, and such subfield is unique.
{ #9yfc3g}


**_Proof._**
Note that a finite field $\mathbb{F}_q$ of characteristic $p$ has cardinality $q=p^r$ for some number $r\geqslant 1$. Furthermore, $\mathbb{F}_q$ can be realized as the set of the roots of the polynomial $X^q-X$ in some algebraic closure of $\mathbb{F}_p$.

If $\mathbb{F}_q \supseteq \mathbb{F}_{q'} \supseteq \mathbb{F}_p$ is a sub-extension with $q=p^r$ and $q'=p^s$. Since $\mathbb{F}_q$ is also a $\mathbb{F}_{q'}$-vector space, we have that $s\mid r$. On the other hand, the condition is also sufficient, because the roots of the polynomial $X^{p^s}-X$ roots are also of $X^{p^r}-X$.

Therefore, $\mathbb{F}_{p^r}$ contains a field with $p^s$ elements if and only if $s \mid r$, and such subfield is unique.

<p align="left">□</p>

> [!proposition] 
> The followings hold.
> - For any prime $p$ and positive integer $n$, there exists a finite field $F$ with $|F|=p^n$. Furthermore, $F$ is unique up to isomorphism.
> - In fact, $F$ is isomorphic to the splitting field of $x^{p^n}-x$ over $\mathbb{F}_p$. 
> - $F^\times$ is a cyclic group.