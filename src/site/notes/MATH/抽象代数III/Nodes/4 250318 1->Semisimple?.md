---
{"dg-publish":true,"draft":false,"permalink":"/MATH/抽象代数III/Nodes/4 250318 1->Semisimple?/","dgPassFrontmatter":true}
---


# Semisimple 

> [!definition]
> A ring $R$ with identity is called *semisimple* if ${}_RR$ is semisimple as a left $R$-modules. 

**Remark.** ${}_R R$ is called (left) *regular module*.

> [!theorem]
> TFAE for an Artinian ring $R$. 
> - $R$ is a semisimple Artinian ring.
> - Every $R$-module $V$ is semisimple.

**_Proof._**
i)->ii) Let ${}_R R=\sum_\lambda I_\lambda$ be a sum of left simple $R$-submodules. Then $V=\sum_{v\in V}\sum_{\lambda}I_\lambda v$. Note that $f:I_\lambda\to I_\lambda v,i\mapsto iv$ is an $R$-homomorphism, then $\ker f=0$ or $I_\lambda$, that is, $I_\lambda v$ is $0$ or simple. 

ii)->i) is trivial.
<p align="left">□</p>


# Some Isomorphisms

> [!lemma]
> Let $M$ be a left $R$-module. Then $M\simeq \mathrm{Hom}_R({}_R R_R,{}_RM)$. 

**_Proof._**
Define 

$$\mathrm{Hom}_{R}(R,M)\to M,f\mapsto f(1)$$

and define 

$$M\to \mathrm{Hom}_R(R,M),m\mapsto \varphi_m:r\mapsto rm.$$

It is easy to check they are homomorphism and are inverse each other. 
<p align="left">□</p>


> [!corollary]
> For any ring $R$ with identity, one has $\mathrm{End}_R({}_R R)\simeq R^\mathrm{op}$ as rings.
{ #5830df}


**_Proof._**
Define 

$$\mathrm{End} _R({}_R R)\to R^\mathrm{op},f\mapsto f(1).$$

Note that $f_1f_2(1)=f_1(f_2(1))=f_1(f_2(1)\cdot 1)=f_2(1)f_1(1)$. 
<p align="left">□</p>


> [!lemma]
> Let $R$ be a ring, and let $M_n(R)$ be the set of all square matrices of degree $n$ over $R$. Then $\mathrm{M}_n(R)^{\mathrm{op}}\simeq \mathrm{M}_n(R^\mathrm{op})$. 

**_Proof._**
Consider 

$$\varphi:\mathrm{M}_n(R)^{\mathrm{op}}\simeq \mathrm{M}_n(R^\mathrm{op}), A\mapsto A^T.$$

Assume that $(\mathrm{M}_n(R),\cdot)$, $(\mathrm{M}_n(R)^\mathrm{op},*)$ and $(\mathrm{M}_n(R)^\mathrm{op},\circ)$. Then $\varphi(A*B)=\varphi(B\cdot A)=(B\cdot A)^T$ and $\varphi(A)\circ \varphi(B)=A^T\circ B^T$, and we can prove that $(BA)^T=A^T\circ B^T$. 
<p align="left">□</p>


> [!theorem] Artin–Wedderburn
> Let $A$ be a semisimple Artinian ring with identity. Then $A$ is a direct sum of matrix rings over division rings. Specifically, if ${}_AA\simeq S_1^{n_1}\oplus\cdots\oplus S_r^{n_r}$ where $S_1,\cdots,S_r$ are non-isomorphic simple modules occurring with multiplications $n_1,\cdots,n_r$, then $A\simeq \mathrm{M}_{n_1}(D_1)\oplus\cdots\oplus \mathrm{M}_{n_r}(D_r)$ where $D_i=\mathrm{End}_A(S_i)^\mathrm{op}$. 
{ #f43ojz}


**_Proof._**
By [[MATH/抽象代数III/Nodes/3 250311#^qk0ias\|3 250311#^qk0ias]], $D_i$ is a division ring. 

Since ${}_A A\simeq S_1^{n_1}\oplus\cdots\oplus S_r^{n_r}$, we have 

$$\mathrm{End}_A({}_A A)\simeq \oplus_{i,j}\mathrm{Hom}(S_i^{n_i},S_j^{n_j})=\oplus_{i=1}^r\mathrm{Hom}(S_i^{n_i},S_i^{n_i})=\oplus_{i=1}^r\mathrm{End}_A(S_r^{n_r}).$$

Then by [[MATH/抽象代数III/Nodes/3 250311#^8omj6z\|3 250311#^8omj6z]], there is $\mathrm{End}_A(S_i^{n_i})\simeq \mathrm{M}_n(D_i)^\mathrm{op}\simeq\mathrm{M}_n(D_i^{\mathrm{op}})$. 
<p align="left">□</p>

# Simple Modules

> [!definition]
> A ring is called *simple* if it has no ideal other than $0$ and $R$.

**Example.** $\mathrm{M}_n(D)$ is a simple ring if $D$ is a division ring.

Notice that 

$$\mathrm{M} _n(D)=\left\{\begin{pmatrix} * & 0 & \cdots & 0 \\
* & 0 & \cdots & 0 \\
\vdots & \vdots &  & \vdots \\
* & 0 & \cdots & 0\end{pmatrix}\right\}\oplus \cdots\oplus
\left\{\begin{pmatrix} 0 & \cdots & 0 & * \\
0 & \cdots & 0 & * \\
\vdots &  & \vdots &  \vdots \\
0 & \cdots & 0 & *\end{pmatrix}\right\}$$

and each part is a simple left $\mathrm{M}_n(D)$-module. 

# Algebras

> [!definition]
> Let $R$ be a commutative ring with identity, and let $A$ be a ring with identity. We call $A$ an *$R$-algebra* if $A$ is an $R$-module such that $a(xy)=(ax)y=x(ay)$ for any $a\in R$ and any $x,y\in A$. Equivalently, there is a ring homomorphism $R\to A$ such that the image of $R$ lies in the center of $A$. 
> 
> Moreover, if $R$ is a field and $A$ is a finite-dimensional over $R$, then we shall say that the algebra is finite-dimensional, which is both Noetherian and Artinian. 

**Examples.**
- Suppose $R$ is a commutative ring with identity and $G$ is a finite group. Define group algebra/group ring as $RG=\{\sum_{g\in G}a_gg:a_g\in R\}$, which is a free $R$-module with basis $\{g:g\in G\}$, then $RG$ is a $R$-algebra. 
- For a field $F$, the polynomial ring $F[x]$ is a $F$-algebra. 
- For a commutative ring $R$, $\mathrm{M}_n(R)$ is a $R$-algebra, where $r\mapsto \mathrm{diag}(r,\cdots,r)$. 

> [!lemma] Schur
> Let $A$ be a $k$-algebra, where $k$ is a field. Let $S$ be a simple $A$-module. Then $\mathrm{End}_A(S)$ is a division ring, which is a $k$-algebra. 
> 
> If $A$ is finite dimensional over $k$, so is $\mathrm{End}_A(S)$. 
> 
> Furthermore, if $A$ is finite dimensional and $k$ is algebraic closed, then $\mathrm{End}_A(S)\simeq k$. 

**_Proof._**
later.


**Remark.** In [[MATH/抽象代数III/Nodes/4 250318 1->Semisimple?#^f43ojz\|#^f43ojz]],  if $k$ is a closed field..... some direct sum of matrix ring(?)



（下面是从第五节搬过来的）



> [!theorem]
> A finite-dimensional semisimple $k$-algebra $A$ over a field $k$ with $k=\overline k$ is isomorphism to a direct sum of matrix algebras over $k$. 
{ #88dlwq}


**_Proof._**
Recall that $A=\mathrm{M}_{n_1}(D_1)\oplus\cdots\oplus \mathrm{M}_{n_r}(D_r)$ by [[MATH/抽象代数III/Nodes/4 250318#^f43ojz\|4 250318#^f43ojz]]. Since $k$ is algebraic closed, $D_i=k$ for each $i$ by [[MATH/Cards/Nodes/Schur's Lemma\|Schur's lemma]]. 
<p align="left">□</p>


> [!corollary]
> If $A$ is a finite-dimensional $k$-algebra, then any simple $A$-module is of finite-dimensional as $k$-vector space.

> [!proposition]
> Let $A$ be a finite-dimensional semisimple $k$-algebra over a field $k$. In any decomposition ${}_A A=S_1^{n_1}\oplus\cdots\oplus S_r^{n_r}$ where the $S_i$ are pairwise non-isomorphic simple $A$-modules, we have $S_1,\cdots,S_r$ is a complete set of representative of the isomorphism of simple $A$-modules. 
> 
> If moreover $k=\overline k$, then $n_i=\dim _kS_i$ and $\dim{}_A A=\sum_{i=1}^r n_i^2$. 
{ #yo1zc8}


**_Proof._**
By [[MATH/抽象代数III/Nodes/Annihilator and Jacobson Radical#^09efb3\|Annihilator and Jacobson Radical#^09efb3]], each simple $A$-module $M$ is a quotient of ${}_A A$. Since ${}_A A$ is semisimple, we have that $M$ is a direct summand of ${}_A A$. 
<p align="left">□</p>

