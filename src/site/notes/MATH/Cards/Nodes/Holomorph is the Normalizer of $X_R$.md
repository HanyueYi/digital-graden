---
{"dg-publish":true,"permalink":"/MATH/Cards/Nodes/Holomorph is the Normalizer of $X_R$/","dgPassFrontmatter":true}
---


> [!theorem]
> Let $G$ be a group. Define $G_R=\{\rho_g:g\in G\}\leqslant\mathrm{Sym}(G)$ where $\rho_g:x\mapsto xg$. Then we have 
> 
> $$\mathrm{Hol}(X):=X_R{:}\mathrm{Aut} (X)=N_{\mathrm{Sym}(X)}(X_R)$$

**_Proof._**
For any $\varphi\in N_{\mathrm{Sym}(G)}(G_R)\leqslant\mathrm{Sym}(G)$, we may assume that $\varphi(1)=1$. Otherwise, take $\varphi'=\varphi\circ\rho_{\varphi^{-1}(1)}$. Since $\varphi\in\mathrm{Sym}(G)$, $\varphi$ is bijective and so it remains to show $\varphi(gh)=\varphi(g)\varphi(h)$ for any $g,h\in G$. Note that $\rho_g^{\varphi}=\varphi^{-1}\circ\rho_g\circ\varphi =\rho_{\varphi^{-1}(g)}$. Then by $\rho_{gh}=\rho_h\circ\rho_g$ we have $\varphi\in\mathrm{Aut}(G)$. 
<p align="right">□</p>

**Remark.** We can readily deduce that 
- $X_L=C_{\mathrm{Sym}(X)}(X_R)$.
- $X_R=C_{\mathrm{Sym}(X)}(X_L)$.
- If $X$ has a trivial center, then $\left\langle X_L,X_R\right\rangle=X_L\times X_R=X_R{:}\mathrm{Inn}(X)$. 

It is similar as [[MATH/Cards/Nodes/Three Permutations on G Induced from G\|Three Permutations on G Induced from G]]. 
