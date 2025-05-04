---
{"dg-publish":true,"draft":false,"permalink":"/MATH/抽象代数III/Nodes/Semisimple Artinian Rings and Algebras/","dgPassFrontmatter":true}
---


# Semisimple 

> [!definition]
> A ring $R$ with identity is called *semisimple* if ${}_RR$ is semisimple as a left $R$-modules. 

**Remark.** ${}_R R$ is called (left) *regular module*.

> [!theorem]
> TFAE for an Artinian ring $R$. 
> - $R$ is a semisimple Artinian ring.
> - Every $R$-module $V$ is semisimple.
{ #7dokb6}


**_Proof._**
i)->ii) Let ${}_R R=\sum_\lambda I_\lambda$ be a sum of left simple $R$-submodules. Then $V=\sum_{v\in V}\sum_{\lambda}I_\lambda v$. Note that $f:I_\lambda\to I_\lambda v,i\mapsto iv$ is an $R$-homomorphism, then $\ker f=0$ or $I_\lambda$, that is, $I_\lambda v$ is $0$ or simple. 

ii)->i) is trivial.
<p align="left">□</p>


# Some Isomorphisms

In this section, we discuss some statements that will be useful later.

> [!lemma]
> Let $M$ be a left $R$-module. Then $M\simeq \mathrm{Hom}_R({}_R R_R,{}_RM)$. 
{ #cj265g}


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
{ #hvg28s}


**_Proof._**
Consider 

$$\varphi:\mathrm{M}_n(R)^{\mathrm{op}}\simeq \mathrm{M}_n(R^\mathrm{op}), A\mapsto A^T.$$

Assume that $(\mathrm{M}_n(R),\cdot)$, $(\mathrm{M}_n(R)^\mathrm{op},*)$ and $(\mathrm{M}_n(R)^\mathrm{op},\circ)$. Then $\varphi(A*B)=\varphi(B\cdot A)=(B\cdot A)^T$ and $\varphi(A)\circ \varphi(B)=A^T\circ B^T$, and we can prove that $(BA)^T=A^T\circ B^T$. 
<p align="left">□</p>


# Schur Lemma and Artin-Wedderburn Theorem

> [!theorem] Schur lemma
> Let $S_1$ and $S_2$ be simple $R$-modules. Then $\mathrm{Hom}_R(S_1,S_2)=0$ unless $S_1\simeq S_2$ in which case the endomorphism ring $\mathrm{End}_R(S_1)$ is a division ring. 
{ #qk0ias}


**_Proof._**
See [[MATH/Cards/Nodes/Schur Lemma\|Schur lemma]].
<p align="left">□</p>

> [!lemma]
> Let $R$ be a ring with identity $1$. Suppose that $U=S_1+\cdots+S_n$ is an $R$-module that can be expressed as the sum of finitely many simple submodule. If $V$ is any submodule of $U$, then there is a subset $I\subseteq\{1,\cdots,n\}$ such that $U=V\oplus (\oplus_{i\in I}S_i)$. 
> 
> In particular, $V$ is a direct summand of $U$, and $U$ is a direct sum of some subset of the $S_i$'s and hence necessarily semisimple.

**_Proof._**
Let $\mathcal{F}$ be the collection of all subsets $J \subseteq\{1, \ldots, n\}$ such that $V \cap\left(\bigoplus_{j \in J} S_j\right)=\{0\}$. Note that $\mathcal{F}$ is non-empty since $\emptyset \in \mathcal{F}$, then $\mathcal{F}$ contains a maximal element by $\{1,\cdots,n\}$ finite. Let $I$ be such a maximal subset, and let $W=V \oplus\left(\bigoplus_{i \in I} S_i\right)$. Now we claim that $W=U$. Otherwise, since $U=S_1+\cdots+S_n$, there exists some $k \in\{1, \ldots, n\}$ such that $S_k \nsubseteq W$. Then $S_k\cap W=\{0\}$ by $S_k$ simple. Define $I'=I\cup\{k\}$, then $I'\in\mathcal{F}$, leading to a contradiction by the maximality of $I$. Now we finish the proof. 
<p align="left">□</p>


> [!theorem]
> Let $U$ be an $R$-module. TFAE:
> - $U$ is semisimple;
> - $U$ is a sum of simple $R$-modules;
> - any $R$-submodule of $U$ is a direct summand of $U$. 

**_Proof._**
See [[MATH/抽象代数III/Nodes/HW4#^ggoc0z\|here]].
<p align="left">□</p>

> [!corollary]
> Let $U$ be the $R$-module with composition series of finite composition length. 
> - The sum of all the simple submodule of $U$ is a semisimple module that is the unique largest semisimple submodule of $U$, which is called [[MATH/抽象代数III/Nodes/Socle and Radical of Module#^4du342\|socle]].
> - The sum of all submodules of $U$ isomorphic to some given simple module $S$ is a submodule isomorphic to a direct sum of copies of $S$. It is the unique largest submodule with this property. 


> [!corollary]
> Let $U=S_1^{a_1}\oplus\cdots\oplus S_r^{a_r}$ be a semisimple submodule where the $S_i$ are non-isomorphic simple $R$-modules. Then each submodule $S_i^{a_i}$ is uniquely determined and characterized as unique largest submodule of $U$ expressed as a direct sum of copies of $S_i$. 

**_Proof._**
It suffices to show that $S_i^{a_i}$ contains every submodule of $U$ isomorphic to $S_i$. Let $T$ be a non-zero simple submodule of $U$ with $T\not\subseteq S_i^{a_i}$. Define a projective $\pi_i:U\to S_i^{a_i}$, then $\pi_j(T)\neq 0$ for some $j\neq i$ and $T\simeq S_j\not\simeq S_i$. Now we finish the proof. 
<p align="left">□</p>


> [!theorem]
> Let $R$ be a ring with $1$. Let ${}_RV=V_1\oplus V_2\oplus\cdots\oplus V_n$ be a direct sum of simple $R$-modules $V_i$ such that $V_i\simeq V_j$ for any $i,j$. Then $\mathrm{End}_R(V)$ is isomorphic to the full matrix ring of degree $n$ over the division ring $\mathrm{End}_R(V_1)$. 
{ #8omj6z}


**_Proof._**
Let $\pi_i:V\to V_i$ be the projection, and let $\theta_i:V_1\stackrel{\sim}{\to}V_i$ be an isomorphism. For $\sigma\in \mathrm{End}_R(V)$, define the composition 

$$V_1\stackrel{\sigma_j}{\to}V_j\stackrel{\sigma}{\to}V\stackrel{\pi_i}{\to}V_i\stackrel{\theta_i^{-1}}{\to}V_1$$

as $\varphi_{ij}(\sigma):=\theta_i^{-1}\pi_i\sigma\theta_j\in\mathrm{End}_R(V_1)$. Then we have map 

$$\varphi:\mathrm{End}_R(V)\to\mathrm{M}_n(E_1),\sigma\mapsto(\varphi_{ij}(\sigma))_{n\times n}$$

where $E_1=\mathrm{End}_R(V_1)$. It is easy to check $\varphi$ is a ring homomorphism. 

Nest, we show $\varphi$ is an isomorphism. If $\varphi(\sigma)=0$, then $\theta_i^{-1}\pi_i\sigma\theta_j=0$ for all $i,j$. It deduces that $\pi_i(\sigma(V_j))=0$ for all $i,j$ and so $\sigma(V_j)=0$ for all $j$. Hence $\sigma=0$ and so $\varphi$ is injective. To see $\varphi$ is an epimorphism, for any given $(\sigma_{ij})\in \mathrm{M}_n(E_1)$ we can define 

$$\sigma=\sum_{i,j}\tau_i\theta_i \sigma_{ij}\theta_j^{-1}\pi_j$$

where $\tau_i:V_i\hookrightarrow V$ is an inclusion. Therefore, $\varphi$ is an isomorphism and so $\mathrm{End}_R(V)\simeq \mathrm M_n(E_1)$ with $E_1=\mathrm{End}_R(V_1)$. 
<p align="left">□</p>


> [!theorem] Artin–Wedderburn
> Let $A$ be a semisimple Artinian ring with identity. Then $A$ is a direct sum of matrix rings over division rings. Specifically, if ${}_AA\simeq S_1^{n_1}\oplus\cdots\oplus S_r^{n_r}$ where $S_1,\cdots,S_r$ are non-isomorphic simple modules occurring with multiplications $n_1,\cdots,n_r$, then $A\simeq \mathrm{M}_{n_1}(D_1)\oplus\cdots\oplus \mathrm{M}_{n_r}(D_r)$ where $D_i=\mathrm{End}_A(S_i)^\mathrm{op}$. 
{ #f43ojz}


**_Proof._**
Since $A$ is a semisimple Artinian ring, we can assume that ${}_A A\simeq S_1^{n_1}\oplus\cdots\oplus S_r^{n_r}$. Then by [[MATH/抽象代数III/Nodes/Semisimple Artinian Rings and Algebras#^qk0ias\|#^qk0ias]] we have

$$\mathrm{End}_A({}_A A)\simeq \oplus_{i,j}\mathrm{Hom}(S_i^{n_i},S_j^{n_j})=\oplus_{i=1}^r\mathrm{Hom}(S_i^{n_i},S_i^{n_i})=\oplus_{i=1}^r\mathrm{End}_A(S_r^{n_r}).$$

Furthermore, by [[MATH/抽象代数III/Nodes/Semisimple Artinian Rings and Algebras#^8omj6z\|#^8omj6z]] there is $\mathrm{End}_A(S_r^{n_r})\simeq\mathrm{M}_n(\mathrm{End}_R(S_1))$. By [[MATH/抽象代数III/Nodes/Semisimple Artinian Rings and Algebras#^qk0ias\|#^qk0ias]] we know $\mathrm{End}_R(S_1)$ is a division ring and so $A$ is a direct sum of matrix rings over division rings. 

Specifically, recall that $\mathrm{End}_R({}_RR)\simeq R^{\mathrm{op}}$ by [[MATH/抽象代数III/Nodes/Semisimple Artinian Rings and Algebras#^5830df\|#^5830df]], then by [[MATH/抽象代数III/Nodes/Semisimple Artinian Rings and Algebras#^hvg28s\|#^hvg28s]] one can get 

$$A\simeq \mathrm{End} _{A}({}_A A)^{\mathrm{op}}\simeq\oplus_{i=1}^r\mathrm{End} _A(S_r^{n_r})^{\mathrm{op}}\simeq\oplus_{i=1}^r \mathrm{M} _n(\mathrm{End} _A(S_i))^{\mathrm{op}}\simeq \oplus_{i=1}^r \mathrm{M} _n(D_i)$$

where $D_i=\mathrm{End}_A(S_i)^{\mathrm{op}}$. Now we finish the proof.
<p align="left">□</p>


# Simple Modules

> [!definition]
> A ring is called *simple* if it has no ideal other than $0$ and $R$.

**Example.** $\mathrm{M}_n(D)$ is a simple ring if $D$ is a division ring. Additionally, notice that 

$$\mathrm{M} _n(D)=\left\{\begin{pmatrix} * & 0 & \cdots & 0 \\* & 0 & \cdots & 0 \\ \vdots & \vdots &  & \vdots \\ * & 0 & \cdots & 0\end{pmatrix}\right\}\oplus \cdots\oplus \left\{\begin{pmatrix} 0 & \cdots & 0 & * \\ 0 & \cdots & 0 & * \\ \vdots &  & \vdots &  \vdots \\ 0 & \cdots & 0 & *\end{pmatrix}\right\}$$

and each part is a simple left $\mathrm{M}_n(D)$-module. 

# Algebras

> [!definition]
> Let $R$ be a commutative ring with identity, and let $A$ be a ring with identity. We call $A$ an *$R$-algebra* if $A$ is an $R$-module such that $a(xy)=(ax)y=x(ay)$ for any $a\in R$ and any $x,y\in A$. Equivalently, there is a ring homomorphism $R\to A$ such that the image of $R$ lies in the center of $A$. 
> 
> Moreover, if $R$ is a field and $A$ is a finite-dimensional over $R$, then we shall say that the algebra is finite-dimensional, which is both Noetherian and Artinian.
{ #ef1283}


**Examples.**
- Suppose $R$ is a commutative ring with identity and $G$ is a finite group. Define group algebra/group ring as $RG=\{\sum_{g\in G}a_gg:a_g\in R\}$, which is a free $R$-module with basis $\{g:g\in G\}$. Thus, $RG$ is a $R$-algebra. 
- For a field $F$, the polynomial ring $F[x]$ is a $F$-algebra. 
- For a commutative ring $R$, $\mathrm{M}_n(R)$ is a $R$-algebra, where $r\mapsto \mathrm{diag}(r,\cdots,r)$. 

> [!lemma] Schur
> The following statements hold.
> - Let $A$ be a $k$-algebra, where $k$ is a field. Let $S$ be a simple $A$-module. Then $\mathrm{End}_A(S)$ is a division ring, which is a $k$-algebra. 
> - If $A$ is finite-dimensional over $k$, so is $\mathrm{End}_A(S)$. 
> 
> Furthermore, if $A$ is finite dimensional and $k$ is algebraically closed, then $\mathrm{End}_A(S)\simeq k$. 
{ #evw7zf}


**_Proof._**
i) Note that $\mathrm{End}_A(S)$ is a division ring by [[MATH/抽象代数III/Nodes/Semisimple Artinian Rings and Algebras#^qk0ias\|#^qk0ias]], and one can easily check that $\mathrm{End}_A(S)$ is an $k$-module with $k\varphi_1\varphi_2=(k\varphi_1)\varphi_2=\varphi_1(k\varphi_2)$ by $k\in A$. Thus $\mathrm{End}_A(S)$ is a $k$-algebra.

ii) If $A$ is finite-dimensional over $k$, then by [[MATH/抽象代数III/Nodes/Semisimple Artinian Rings and Algebras#^ef1283\|#^ef1283]] we know $A$ is Artinian. Since $S$ is a simple $A$-module, there exists a left maximal ideal $M\subseteq A$ such that $A/M\simeq S$ by [[MATH/抽象代数III/Nodes/Annihilator and Jacobson Radical#^09efb3\|Annihilator and Jacobson Radical#^09efb3]]. Then $S$ is finite-dimensional over $k$, because $S$ is a quotient space of $A$. Suppose $\dim_kS=d$, then $\mathrm{End}_k(S)\simeq\mathrm{M}_d(k)$ and it is also finite-dimensional over $k$. Then $\mathrm{End}_A(S)$ is finite-dimensional by $\mathrm{End}_A(S)\subseteq\mathrm{End}_k(S)$. 

iii) By i) and ii), $\mathrm{End}_A(S)$ is a finite-dimensional division ring over algebraically closed field $k$. Then by [[MATH/Cards/Nodes/Schur Lemma#^190f7e\|Schur Lemma#^190f7e]], $\mathrm{End}_A(S)\simeq k$. 
<p align="left">□</p>


> [!theorem]
> A finite-dimensional semisimple $k$-algebra $A$ over a field $k$ with $k=\overline k$ is isomorphism to a direct sum of matrix algebras over $k$, that is, 
> 
> $$A\simeq \mathrm{M}_{n_1}(k)\oplus\cdots\oplus\mathrm{M}_{n_r}(k)\text{ for some }n_i\in \mathbb{N}_+.$$
> 
>
{ #88dlwq}


**_Proof._**
Recall that $A=\mathrm{M}_{n_1}(D_1)\oplus\cdots\oplus \mathrm{M}_{n_r}(D_r)$ by [[MATH/抽象代数III/Nodes/Semisimple Artinian Rings and Algebras#^f43ojz\|#^f43ojz]]. Since $k$ is algebraically closed, $D_i=k$ for each $i$ by [[MATH/抽象代数III/Nodes/Semisimple Artinian Rings and Algebras#^evw7zf\|#^evw7zf]].
<p align="left">□</p>


> [!corollary]
> If $A$ is a finite-dimensional $k$-algebra, then any simple $A$-module is of finite-dimensional as $k$-vector space.

**_Proof._**
See the argument of [[MATH/抽象代数III/Nodes/Semisimple Artinian Rings and Algebras#^evw7zf\|#^evw7zf]], ii). 
<p align="left">□</p>


> [!proposition]
> Let $A$ be a finite-dimensional semisimple $k$-algebra over a field $k$. In any decomposition ${}_A A=S_1^{n_1}\oplus\cdots\oplus S_r^{n_r}$ where the $S_i$ are pairwise non-isomorphic simple $A$-modules, we have $S_1,\cdots,S_r$ is a complete set of representative of the isomorphism of simple $A$-modules. 
> 
> If moreover $k=\overline k$, then $n_i=\dim _kS_i$ and $\dim_k{}_A A=\sum_{i=1}^r n_i^2$. 
{ #yo1zc8}


**_Proof._**
By [[MATH/抽象代数III/Nodes/Annihilator and Jacobson Radical#^09efb3\|Annihilator and Jacobson Radical#^09efb3]], each simple $A$-module $M$ is a quotient of ${}_A A$. Since ${}_A A$ is semisimple, we have that $M$ is a direct summand of ${}_A A$ and so $S_1,\cdots,S_r$ are all representative of the isomorphism of simple $A$-modules. 

Furthermore, if $k$ is algebraically closed, by [[MATH/抽象代数III/Nodes/Semisimple Artinian Rings and Algebras#^88dlwq\|#^88dlwq]] one can get $\dim _k {}_A A=\sum_{i=1}^r n_i^2$. 
<p align="left">□</p>

