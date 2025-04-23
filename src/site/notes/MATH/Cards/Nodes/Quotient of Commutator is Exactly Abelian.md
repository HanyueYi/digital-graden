---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Quotient of Commutator is Exactly Abelian/","dgPassFrontmatter":true}
---

#TERMS/commutator #RESOURCE/cards #TERMS/basic 

> [!proposition]
> Let $G$ be a finite group and let $N\lhd G$ be a normal subgroup. Then $G/H$ is abelian if and only if $G'\leqslant H$.

**_Proof._**
Define the canonical map as $\pi:G\to G/H,\ g\mapsto \overline g$. If $G/H$ is abelian, then $\pi(aba^{-1}b^{-1})=\overline a \overline b \overline a^{-1} \overline b^{-1}=\overline e$ and so $aba^{-1}b^{-1}\in\ker \pi=H$. It yields that $G'\leqslant H$. Conversely, if $aba^{-1}b^{-1}\in H$ for any $a,b\in G$, then $\overline{aba^{-1}b^{-1}}=\overline e$ and $\overline a\overline b=\overline b \overline a$. Therefore, we have $G/H$ is abelian.
□
