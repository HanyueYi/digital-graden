---
{"dg-publish":true,"aliases":["tensor-hom adjunction"],"draft":false,"permalink":"/MATH/Cards/Nodes/Tensor-Hom Adjunction for kG-module/","dgPassFrontmatter":true}
---


> [!lemma]
> If $U,V$ and $W$ are $kG$-modules, then
> 
> $$\mathrm{Hom}_{kG}(U\otimes V,W)\cong\mathrm{Hom}_{kG}(U,V^*\otimes W).$$
{ #rtw9uw}


**_Proof._**
Note that there is an isomorphism $U^*\otimes V\cong\mathrm{Hom}_k(U,V)$, which maps $\varphi\otimes v$ to $\phi_v$ where $\varphi_v:u\mapsto\varphi(u)v$. So there is 

$$\begin{aligned}
\mathrm{Hom}_k(U\otimes V,W)&\cong(U\otimes V)^*\otimes W\\
&\cong U^*\otimes (V^*\otimes W)\\
&\cong \mathrm{Hom}_k(U,V^*\otimes W). 
\end{aligned}$$

If $U$ and $V$ are $kG$-modules, then $\mathrm{Hom}_{k}(U,V)$ is also a $kG$-module by $(g\varphi)(u):=g(\varphi(g^{-1}u))$. For any $\varphi\in\mathrm{Hom}_k(U,V)$, if $\varphi$ is an element of $\mathrm{Hom}_{kG}(U,V)$, then we have that $(g\varphi)(gu)=g(\varphi(u))=\varphi(g(u))=\varphi(gu)$ for all $u\in U$ and $g\in G$ (see [[MATH/Representations and Characters of Groups/Nodes/1 Representation & FG-homomorphism#^d9ofk3\|here]]). It yields that $g\varphi=\varphi$ and so $\mathrm{Hom}_{kG}(U,V)$ consists of the elements of $\mathrm{Hom}_k(U,V)$ which are fixed by $G$. 

Since an isomorphism will map the fixed points of $G$ in the one space to the fixed points in the other space, we obtain that $\mathrm{Hom}_{kG}(U\otimes V,W)\cong\mathrm{Hom}_{kG}(U,V^*\otimes W)$. 
<p align="left">□</p>


