---
{"dg-publish":true,"aliases":"Frattini's argument","permalink":"/MATH/Cards/Nodes/Frattini's Argument/","dgPassFrontmatter":true}
---


> [!lemma]
> Suppose $G$ is a transitive on $\Omega$. Then $H<G$ is transitive on $\Omega$ iff $G=HG_\omega$ for $\omega\in \Omega$.
{ #9wyb80}


**_Proof._**
Suppose that $H$ is transitive on $\Omega$. For any $\omega\in\Omega$ and any $g\in G$, define $\omega':=\omega^g$. Since $H$ is transitive, there is $h\in H$ such that $\omega^h=\omega'=\omega^g$. So we have $h^{-1}g\in G_\omega$ and $g=h(h^{-1}g)\in HG_\omega$. Therefore, $G=HG_\omega$.

Conversely, assume that $G=HG_{\omega}$. For any $\omega,\omega'\in\Omega$, there is $g\in G$ such that $\omega^g=\omega'$. As $g$ can be written as $g=xh$ with $x\in G_\omega$ and $h\in H$, there is $\omega^g=\omega^{xh}=\omega^h=\omega'$, i.e., $H$ acts on $\Omega$ transitively.
□

Here is another version of Frattini's argument from [wiki](https://en.wikipedia.org/wiki/Frattini%27s_argument). In fact, it is a special case of [[#^9wyb80]]. Let $\Omega$ be the set of Sylow subgroups of $H\lhd G$. Then both $G$ and $H$ act on $\Omega$ by conjugation transitively, and the point stabilizer $G_P=N_G(P)$ for a $P\in\Omega$. 


> [!corollary]
> If $H\lhd G$ and $P$ is a Sylow subgroup of $H$, then $G=HN_G(P)$.
{ #iy9o9t}


**_Proof._**
Let $g\in G$. Since $H\lhd G$ and $P\leqslant H$, the group $gPg^{-1}\leqslant H$ is also a Sylow $p$-subgroup of $H$. By [[MATH/Cards/Nodes/Sylow Theorems#^ueqhoc\|Sylow Theorems#^ueqhoc]], there is a $h\in H$ such that $gPg^{-1}=hPh^{-1}$. Then $h^{-1}g\in N_G(P)$ and $g$ can be written as $g=h(h^{-1}g)\in HN_G(P)$. Hence $G=HN_G(P)$. 
□


