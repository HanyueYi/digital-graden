---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Finite Group of Field/","dgPassFrontmatter":true}
---



<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



**Exercise.** Show that finite subgroups of the multiplicative group of a field are cyclic. 

</div></div>


To show it, it suffices to show the following lemma. If $G$ is a finite subgroup of the multiplicative group of a field, then $G$ satisfies the hypothesis because the polynomial $x^d-1$ has $d$ roots at most.

> [!lemma]
> Let $G$ a finite group with $n$ elements. If for every $d \mid n, \#\left\{x \in G \mid x^d=1\right\} \leq d$, then $G$ is cyclic.

**_Proof._**
Fix $d \mid n$ and consider the set $G_d$ made up of elements of $G$ with order $d$. Suppose that $G_d \neq \varnothing$, so there exists $y \in G_d$; it is clear that $\langle y\rangle \subseteq\left\{x \in G \mid x^d=1\right\}$. But the subgroup $\langle y\rangle$ has cardinality $d$, so from the hypothesis we have that $\langle y\rangle=\left\{x \in G \mid x^d=1\right\}$. Therefore $G_d$ is the set of generators of the cyclic group $\langle y\rangle$ of order $d$, so $\#G_d=\phi(d)$.

We have proved that $G_d$ is empty or has cardinality $\phi(d)$, for every $d \mid n$. So we have:

$$
\begin{aligned}
n & =\# G \\
& =\sum_{d \mid n} \# G_d \\
& \leq \sum_{d \mid n} \phi(d) \\
& =n
\end{aligned}
$$


Therefore $\# G_d=\phi(d)$ for every $d \mid n$. In particular $G_n \neq \varnothing$. This proves that $G$ is cyclic.
□