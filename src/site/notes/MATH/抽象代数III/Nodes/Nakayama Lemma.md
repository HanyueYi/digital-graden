---
{"dg-publish":true,"aliases":["Nakayama lemma"],"draft":false,"permalink":"/MATH/抽象代数III/Nodes/Nakayama Lemma/","dgPassFrontmatter":true}
---


There are three "Nakayama lemmas". Here we call them "module version", "ideal version" and "general version". 


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/math/iii/nodes/socle-and-radical-of-module/#3f1b99" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



> [!theorem] Nakayama's lemma
> Let $U$ be Noetherian(or finitely generated). Then $U\to U/\mathrm{Rad}U$ is [[MATH/抽象代数III/Nodes/Projective Cover#^ktprge\|essential]]. Equivalently, if $V$ is a submodule of $U$ with $V+\mathrm{Rad}U=U$, then $V=U$. 

</div></div>




<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/math//nodes/2-modules/#c2a5d0" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



> [!proposition] Nakayama lemma
> Let $M$ be a finitely generated $A$-module, and let $\alpha\subseteq A$ be an ideal with $\alpha\subseteq\mathrm{Jac}(A)$. If $\alpha M=M$, then $M=0$. 

</div></div>




<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/math//nodes/1-9-complete-variety/#0ws17n" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



> [!lemma] Nakayama lemma
> Let $M$ be a finitely generated $R$-module, and let $I\subseteq R$ be an ideal of $R$. If $M=IM$, then there exists $f=1+r$ with $r\in I$ such that $f\cdot M=0$.  

</div></div>


# Connections between them

> [!proposition]
> The "ideal version" can be proved by the "module version".

**_Proof._**
Assume that $M$ is a finitely generated $A$-module, $\alpha \subseteq \mathrm{Jac} A$ and $\alpha M=M$. 

[[MATH/抽象代数III/Nodes/Annihilator and Jacobson Radical#^p95eh4\|Since]] $\mathrm{Jac}(A)$ kills all simple modules $M/W$, we know $\mathrm{Jac}(A)M\subseteq W$ for each maximal submodule $W$ and so $J(A)M\subseteq \mathrm{Rad}(M)$. Note $\alpha\subseteq\mathrm{Jac}(A)$, then 

$$M=\alpha M\subseteq \mathrm{Jac}(A)M\subseteq\mathrm{Rad}(M).$$

By [[MATH/抽象代数III/Nodes/Socle and Radical of Module#^3f1b99\|the module version]], because $(0)+\mathrm{Rad}(M)=M$, there is $(0)=M$ and we finish the proof. 
<p align="left">□</p>

> [!proposition]
> The "general version" can be proved by the "module version".

**_Proof._**
Assume that $M$ is a finitely generated $A$-module, $\alpha \subseteq \mathrm{Jac} A$ and $\alpha M=M$. Take $I=\alpha$ and apply [[MATH/代数几何/Nodes/1.9 Complete Variety#^0ws17n\|the general version]], then we have $f=1+r$ with $r\in I$ such that $f\cdot M=0$. Then $M=0$ [[MATH/交换代数/Nodes/1 Rings and Ideals#^h2e8bp\|because]] $1+r$ is a unit.
<p align="left">□</p>
