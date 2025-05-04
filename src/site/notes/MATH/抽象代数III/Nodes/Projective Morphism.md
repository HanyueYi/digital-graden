---
{"dg-publish":true,"draft":false,"permalink":"/MATH/抽象代数III/Nodes/Projective Morphism/","dgPassFrontmatter":true}
---


> [!proposition]
> Let $R$ be a commutative ring with $1$. For $R$-modules $X,Y$ and $M$, we have an $R$-morphism 
> 
> $$\begin{aligned}\mathrm{Hom}_R(X,M)\otimes_R\mathrm{Hom}_R(M,Y)&\to \mathrm{Hom}_R(X,Y),\\\varphi\otimes \psi&\mapsto \psi\varphi.\end{aligned}$$
> 
> The image of this morphism is comprised of those morphism from $X$ to $Y$ which factor through some finite power of $M$.
> 
> ![Pasted image 20250408192748.png|160](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250408192748.png)
{ #v26ddz}


**_Proof._**
An element of the image is $\sum_{i\in I}\psi_i\varphi_i$, where $\psi_i:X\to M$ and $\varphi_i:M\to Y$. Give a morphism $\varphi:X\to M^I,x\mapsto (\varphi_i(x))$ and a morphism $\psi:M^I\to Y,(m_i)\to \sum \psi_i(m_i)$. Now we finish the proof.
<p align="left">□</p>



> [!definition] projective morphisms
> Recall that the dual of an $R$-module $X$ is defined as $X^*=\operatorname{Hom}_R(X, R)$. Taking $M=R$, we obtain a natural $R$-linear map
> 
> $$\tau_{X, Y}: X^* \otimes_R Y \longrightarrow \operatorname{Hom}_R(X, Y),  \varphi \otimes y \mapsto(x \mapsto \varphi(x) \cdot y).$$
> 
> The image of $\tau_{X,Y}$ is denoted by $\operatorname{Hom}_R^{\text {pr }}(X, Y)$, and its elements are called *projective morphisms* from $X$ to $Y$. 
{ #n1mk04}


> [!lemma]
> For any $R$-module $M$, $\mathrm{Hom}_R^{\rm pr}(M,M)$ is a $2$-sided ideal of the ring $\mathrm{End}_R(M)=\mathrm{Hom}_R(M,M)$. 
{ #smhffy}


**_Proof._**
It is easy to check for any $\varphi\in \mathrm{Hom}_R^\mathrm{pr}(M,M)$ and $\psi\in\mathrm{End}_R(M)$, one have $\varphi\circ \psi,\psi\circ\varphi\in \mathrm{Hom}_R^\mathrm{pr}(M,M)$.  
<p align="left">□</p>


> [!theorem] 
> Let $P$ be an $R$-module. TFAE:
> - $P$ is a finitely generated projective module.
> - $\mathrm{Hom}_R^{\rm pr}(P,P)=\mathrm{End}_R(P)$.
> - For any $R$-module $X$, the morphism $\tau_{X,P}:X^*\otimes_R P\to \mathrm{Hom}_R(X,P)$ is an isomorphism.
> - For any $R$-module $X$, the morphism $\tau_{P,X}:P^*\otimes X\to\mathrm{Hom}_R(P,X)$ is an isomorphism.
> - The morphism $\tau_{P,P}:P^*\otimes_R P\to \mathrm{End}_R(P)$ is an isomorphism. 
{ #joizl5}


**_Proof._**
i)->ii) Since $P$ is a finitely generated projective $R$-module, there exists $n$ such that $R^n\simeq P\oplus Q$, that is, $P$ is a direct summand of $R^n$. Define $\iota:P\hookrightarrow R^n$ and $f=\iota\circ \varphi$. Notice that $\tau_{P,P}(f\otimes \mathrm{id}_P)(x)=f(x)\cdot\mathrm{id}_P=\varphi(x)$, so $\varphi=\tau_{P,P}(f\otimes \mathrm{id}_P)\in\mathrm{Hom}_R^\mathrm{pr}(P,P)$. Now we finish the proof. 

ii)->iii) Assume $\mathrm{id}_P=\tau_{P,P}(\sum_{i\in I}\varphi_i\otimes m_i)$, then $v=\varphi_i(v)m_i$ for any $v\in P$. Consider the morphism 

$$\begin{aligned}
\sigma:\mathrm{Hom}_R(X,P)&\to X^*\otimes P,\\
\alpha&\mapsto \sum_{i\in I} \varphi_i\alpha\otimes m_i.
\end{aligned}$$

Now we check that $\sigma$ is the inverse of $\tau_{X,P}$. Notice that

$$\begin{aligned}
\mathrm{Hom}_R(X,P)&\stackrel{\sigma}{\to}X^*\otimes_R P\stackrel{\tau_{X,P}}{\to} \mathrm{Hom}_R(X,P),\\
\alpha&\mapsto \sum_i\varphi_i\alpha\otimes m_i\mapsto (x\mapsto \sum_i\varphi_i(\alpha(x))m_i),
\end{aligned}$$

where $\sum_i\varphi_i(\alpha(x))m_i=\alpha(x)$ and so $\tau_{X,P}\circ \sigma=\mathrm{id}_{\mathrm{Hom}_R(X,P)}$. On the other hand, notice that 

$$\begin{aligned}
X^*\otimes P&\stackrel{\tau_{X,P}}{\to}\mathrm{Hom}_R(X,P)\stackrel{\sigma}{\to} X^*\otimes_R P,\\
\psi\otimes v&\mapsto\tau_{X,P}(\psi\otimes v)\mapsto\sum_i\varphi_i\tau_{X,P}(\psi\otimes v)\otimes m_i.
\end{aligned}$$

It remains to verify $\psi\otimes v=\sum_i\varphi_i\tau_{X,P}(\psi\otimes v)\otimes m_i$. Observe that $\varphi_i(v)\psi=\varphi_i\cdot \tau_{X,P}(\psi\otimes v)$, then 

$$\psi\otimes v=\psi\otimes(\sum_i \varphi_i(v)m_i)=\sum_i\psi\otimes\varphi_i(v)m_i=\sum_i\varphi_i(v)\psi\otimes m_i=\sum_i\varphi_i\tau_{X,P}(\psi\otimes v)\otimes m_i$$

and we have done. 

- [ ] iii)->iv) 
{ #h2h0al}


iv)->v) It is trivial, by taking $X=P$. 

v)->i) Assume $\{\varphi_1,\cdots,\varphi_n\}\subseteq P^*$ and $\{x_1,\cdots,x_n\}\subseteq P$ such that

$$\tau_{P,P}\left(\sum_{i=1}^n\varphi_i\otimes x_i\right)=\mathrm{id}_P\implies \sum_{i=1}^n\varphi_i(x)x_i=x.$$

It deduces that $P=\left\langle x_1,\cdots,x_n\right\rangle_R$. Define $R$-module homomorphisms $\phi:R^n\to P,(r_1,\cdots,r_n)\mapsto \sum_{i=1}^n r_ix_i$ and $\psi:P\to R^n,x\mapsto(\varphi_1(x),\cdots,\varphi_n(x))$. Then $\phi\circ\psi=\mathrm{id}_P$ and so $R^n=\ker\phi\oplus \mathrm{im}\psi\simeq \ker\phi\oplus P$, i.e., $P$ is a direct summand of $R^n$. Therefore, $P$ is a finitely generated projective module. 
<p align="left">□</p>
