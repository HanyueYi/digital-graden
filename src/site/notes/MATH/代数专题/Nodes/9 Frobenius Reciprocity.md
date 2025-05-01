---
{"dg-publish":true,"draft":false,"permalink":"/MATH/代数专题/Nodes/9 Frobenius Reciprocity/","dgPassFrontmatter":true}
---


> [!theorem]
> Let $H<G$, and let $\chi,\psi$ be characters of $G,H$, respectively. Then $\left\langle\psi\uparrow_H^G,\chi\right\rangle=\left\langle\psi,\chi\downarrow_H^G\right\rangle$.

**_Proof._**
Note that 

$$\begin{aligned}
\left\langle\psi\uparrow_H^G,\chi\right\rangle&=\frac{1}{|G|}\sum_{g\in G}\psi\uparrow_H^G(g)\chi(g^{-1})=\frac{1}{|G|}\frac{1}{|H|}\sum_{g\in G}\sum_{x\in G}\psi(x^{-1}gx)\chi(g^{-1})\\
&=\frac{1}{|G||H|}\sum_{y\in G}\sum_{x\in G}\psi(y)\chi(xy^{-1}x^{-1})=\frac{1}{|G||H|}\sum_{y\in G}\sum_{x\in G}\psi(y)\chi(y^{-1})=\frac{1}{|H|}\sum_{y\in G}\psi(y)\chi(y^{-1})\\
&=\frac{1}{|H|}\sum_{y\in H}\psi(y)\chi(y^{-1})=\left\langle\psi,\chi\downarrow_H^G\right\rangle.
\end{aligned}$$

Now we finish the proof.
<p align="left">□</p>





 