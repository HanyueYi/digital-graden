---
{"dg-publish":true,"permalink":"/MATH/抽象代数III/Nodes/Projective Cover/","dgPassFrontmatter":true}
---



> [!definition]
> An epimorphism of modules $f:U\twoheadrightarrow V$ is called *essential* if no proper submodule of $U$ is mapped surjectively onto $V$ by $f$. Equivalently, whenever $g:W\to U$ is a map such that $fg$ is an epimorphism, then $g$ is an epimorphism. 

> [!definition]
> A *projective cover* of a module $U$ is an essential epimorphism $P\stackrel{\tau}{\twoheadrightarrow} U$ where $P$ is projective. 

**Remark.** Projective cover does not always exist.

> [!proposition]
> Suppose that $f:P\to U$ is a projective cover of a module $U$ and $g:Q\to U$ is an epimorphism where $Q$ is projective. Then $Q=Q_1\oplus Q_2$ so that $g$ has the component $g=(g_1,0)$ with respect to the direct sum decomposition and $g_1:Q_1\to U$ satisfies that the diagram commutes
> 
> ![Pasted image 20250311214906.png|120](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250311214906.png)
> 
> where $\gamma$ is an isomorphism. 
> 
> If any exists, the projective covers of a module $U$ are all isomorphic, by isomorphisms that commute with the essential epimorphism.
{ #9so7ao}


**_Proof._**
![Pasted image 20250316173427.png|500](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250316173427.png)
□
{ #racwl1}


*****

> [!theorem]
> Let $A$ be an Artinian ring, and let $U$ be $A$-module. Then $U$ has a projective cover. 

**_Proof._**
We only prove for $U$ finitely generated. 

Note that $U/\mathrm{Rad} U\simeq S_1\oplus\cdots\oplus S_n$ with $S_i$ simple, and then by [[MATH/抽象代数III/Nodes/Idempotents and Module Structure#^koarlo\|Idempotents and Module Structure#^koarlo]] $h:P\to U/\mathrm{Rad} U$ is a projective cover of $U/\mathrm{Rad} U$, where $P:=P_{S_1}\oplus\cdots\oplus P_{S_n}$. Now consider the natural surjection 

$$g:U\twoheadrightarrow U/\mathrm{Rad} U.$$

Since $P$ is projective, there exists a lift $f:P\to U$ such that the following diagram commutes by [[BYSTH\|BYSTH]]. 

![Pasted image 20250413173613.png|270](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250413173613.png)

Since $h$ is a projective cover and $f$ is a lift of $h$, we conclude that $f:P\to U$ is a projective cover of $U$. Therefore, $U$ admits a projective cover. 
□

**Remark.** In particular, $U$ has the same projective cover as $U/\mathrm{Rad} U$. 
