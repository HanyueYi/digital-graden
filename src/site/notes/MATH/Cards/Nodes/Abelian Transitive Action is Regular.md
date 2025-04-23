---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Abelian Transitive Action is Regular/","dgPassFrontmatter":true}
---


> [!theorem]
> Let $G$ be an abelian transitive subgroup of the symmetric group $S_n$. Show that $G$ has order $n$.

**_Proof._**
Let $G$ be an transitive abelian subgroup of $S_n$. By transitivity, for each $x \in\{1, \ldots, n\}$ there is a $\sigma \in G$ such that $\sigma(1)=x$. Below, we show that $\sigma$ is uniquely determined by $x$, implying that $\# G=n$.

For showing uniqueness, let $\sigma, \tau \in G$ with $\sigma(1)=\tau(1)=x$. Let $y \in\{1, \ldots, n\}$. From transitivity we get a $\pi \in G$ with $\pi(x)=y$.

Now

$$
\sigma(y)=\sigma \pi(x)=\sigma \pi \tau(1) \stackrel{G \text { abelian }}{=} \tau \pi \sigma(1)=\tau \pi(x)=\tau(y)
$$

and therefore $\sigma=\tau$.
<p align="left">□</p>
