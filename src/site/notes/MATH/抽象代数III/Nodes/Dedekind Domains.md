---
{"dg-publish":true,"draft":false,"permalink":"/MATH/抽象代数III/Nodes/Dedekind Domains/","dgPassFrontmatter":true}
---


# Duals of Fractional Ideals and Projectivity Criteria

[[MATH/抽象代数III/Nodes/Torsion (Free) Elements and Fractional Modules#^5tlkr4\|Recall]] that $I$ is a fractional ideal, if $I\subseteq F=\mathrm{Frac}(R)$ is an $R$-submodule, and there exists $\lambda\in R$ such that $\lambda I\subseteq R$. If $(e_i)_{1\leqslant i\leqslant r}$ is an $F$-basis of $V$ and $(I_i)_{1\leqslant i\leqslant r}$ is a family of fractional ideals, then $M=\oplus _{i=1}^r I_i e_i$ is a fractional module in $V$. By definition, it is easy to check the following lemma.

> [!lemma]
> Let $I_1,I_2$ be fractional ideals. 
> - $I_1+I_2$, which is the $R$-submodule of $F$ generated by $I_1\cup I_2$
> - $I_1\cap I_2$
> - $I_1I_2$, which is the $R$-submodule of $F$ generated by all $x_1x_2$ with $x_1\in I_1$, $x_2\in I_2$
> 
> are all fractional ideals. 


> [!proposition]
> - For any fractional ideal $I$, there is a natural identification between the dual of $I$ and a set of $F$: $I^*=\{x\in F:xI\subseteq R\}$. 
> - Let $V$ be an $r$-dimensional $F$-space with a basis $(e_i)_{1\leqslant i\leqslant r}$, and let $(I_i)_{1\leqslant i\leqslant r}$ be a family of fractional ideals. Set $M=\oplus_{i=1}^r I_ie_i$. Then 
>     - $M^*=\oplus_{i=1}^r I_i^* e_i^*$, where $e_i^*\in V^*$.
>     - the fractional module $M$ is a finitely generated projective $R$-module iff for all $1\leqslant i\leqslant r$, we have $I_i^* I_i=R$. In particular, a fractional ideal $I$ is finitely generated projective $R$-module iff $I^* I=R$. 
{ #fw9ghu}


**_Proof._**
i) Let $0\neq \lambda\in R$ such that $\lambda I\subseteq R$. Take $\varphi\in \mathrm{Hom}_R(I,R)=I^*$. For $x,y\in I$ and 

$$\varphi(\lambda xy)=\lambda\varphi(xy)=\lambda x\varphi(y)=\lambda y\varphi(x).$$

Since $R$ is an integral domain, one has 

$$\varphi(xy)=x\varphi(y)=y\varphi(x).$$

If $x,y\neq 0$, there is $y^{-1}\varphi(y)=x^{-1}\varphi(x)$. So we can define $h_\varphi\in F$ by $h_\varphi=x^{-1}\varphi(x)$ for any $x\in I\setminus \{0\}$. For any $i\in I$, $h_\varphi$ can be written as $h_\varphi=i^{-1}\varphi(i)$ and so $h_\varphi i=\varphi(i)\in R$. We can check the map $\varphi\mapsto h_\varphi$ is an isomorphism, that is, $\mathrm{Hom}_R(I,R)\mapsto I^*=\{x\in F:xI\subseteq R\}$. Moreover, $I^*$ is a fractional ideal.

ii) a) is easy. 

ii) b) It suffices to show, a fractional ideal $I$ is finitely generated projective iff $I^*I=R$. [[MATH/抽象代数III/Nodes/Projective Morphism#^joizl5\|Recall]] that $I$ is a finitely generated projective module iff $\mathrm{id}\in \tau_{I,I}$, i.e., there exists $\sum_i b_i\otimes a_i\in I^*\otimes_R I$ such that for any $x\in I$, $\sum_i xb_ia_i=x$, i.e. $\sum_i b_ia_i=1$ iff $I^* I=R$. 
<p align="left">□</p>


> [!definition]
> A finitely generated projective fractional ideal is called invertible. That is, for a fractional ideal $I$, $I$ is invertible iff $I^*I=R$.  
{ #iazl34}


# Dedekind Domain

> [!definition]
> A *principal ideal domain* is a integral domain $R$ all ideals of which are free. 

**Remark.** Here the definition of principal ideal domain is equivalent to the standard definition (an integral domain whose ideals are principal). One can get principal ideal is free easily; conversely, if a free ideal $I$ has rank more than $1$, assume $a$ and $b$ are two distinct basis elements of $I$ and then $(-b)\cdot a+a\cdot b=0$ leads to a contradiction. 

As a generalization of PID, we define Dedekind Domain.

> [!definition] 
> A *Dedekind domain* is a integral domain $R$ all ideals of which are finitely generated projective. 


- [ ] **Remark.** 好像另一种定义是一维整闭诺特环。后面在证明这件事。
an integral domain is a Dedekind domain if and only if it is a [hereditary ring](https://en.wikipedia.org/wiki/Hereditary_ring "Hereditary ring")
- Local PID and local Dedekind domain are equivalent. See [[MATH/抽象代数III/Nodes/Dedekind Domains#^wzfm6a\|#^wzfm6a]]. 

# Finitely Generated Projective Modules on Local Rings

> [!tip] Recall definition and properties of local rings:
> 
> > [!definition] 
> > We say a ring $R$ (possibly non-commutative) is local if the set of non-units of $R$ form an ideal of $R$. 
> 
> > [!theorem]
> > TFAE for a ring $R$. 
> > - $R$ is a local ring
> > - the set of nonunits of $R$ coincides with $J(R)$, that is, $J(R)$ is a unique maximal left (or right) ideal of $R$
> > - $R/J(R)$ is a division ring. 
> 

> [!proposition]
> Let $R$ be a commutative ring. Assume $R$ is local with unique maximal ideal $I$. Then every finitely generated projective $R$-module is free. 
{ #spgbvh}


**_Proof._**
Let $X$ be a finitely generated projective $R$-module. Then the module $X/IX$ is a finite-dimensional $(R/I)$-vector space with dimension $r$. The isomorphism $(R/I)^r\stackrel{\sim}{\to} X/IX$ can be lifted to an $R$-morphism $\varphi: R^r\to X$.  

Note that $\varphi$ is an epimorphism iff $\varphi(R^r)+IX=X$ by Nakayama lemma.

Since

$$0\to X'\to R^r\to X\to 0$$

is exact and $R^r$ is projective, one have $X'$ is a direct summand of $R^r$ and so it is finitely generated. Since $R^r\simeq X'\oplus X$, there is $(R/I)^r\simeq (X'/IX')\oplus (X/IX)$. So $X'/IX'=0$ and then $X'=0$. Hence $X=R^r$ is free. 
<p align="left">□</p>


> [!corollary]
> Local Dedekind domain = Local PID
{ #wzfm6a}


**_Proof._**
Recall that PID is always Dedekind. Conversely, for a local Dedekind domain, all its ideals are finitely generated projective and so free by [[MATH/抽象代数III/Nodes/Dedekind Domains#^spgbvh\|#^spgbvh]]. Hence it is PID. 
<p align="left">□</p>


# Localization of PIDs and Dedekind Rings

> [!proposition]
> Let $R$ be an integral domain. Let $S$ be a nonempty multiplicatively closed subset of $R\setminus\{0\}$. 
> - If $R$ is a PID, so is $S^{-1}R$. 
> - If $R$ is a Dedekind domain, so is $S^{-1}R$. 
{ #88mhms}


**_Proof._**
Define $j:R\hookrightarrow S^{-1}R,r\mapsto r/1$, which is an embedding. For any ideal $J\subseteq S^{-1}R$, we have that 

$$I=j^{-1}(J)=\{r\in R:j(r)\in J\}$$

is an ideal of $R$. For any $r/s\in J$, there is $r/1\in J$ and so $r\in I$. Thus $S^{-1}I\supseteq J$. On the other hand, for any $x\in S^{-1}I$, $x$ can be written as $x=r'/s'$ with $r'\in I,s'\in S$. Then $r'/s'\in J$ by $r'\in I$ and $r'/s'=(r'/1)(1/s')$. Now we proved $S^{-1}I=J$, that is, each ideal $J$ of $S^{-1}R$ can be written as $J=S^{-1}I$ for some ideal $I\subseteq R$. 

i) For any ideal $J\subseteq S^{-1}R$, $J=S^{-1}I$ for some ideal $I$ of $R$. Since $R$ is a principal ideal domain, we know $I$ is free. Note that $xy-yx=0$ for any $x,y\in I$, so $\mathrm{rank}I\leqslant 1$. If $I=(0)$, then $J=S^{-1}I=(0)$ is also free. If $I\neq (0)$, then $I=(a)$ for some $a\in I$. In this case, $S^{-1}J=(a/1)$ is also free. By the arbitrary of $J$, $S^{-1}R$ is a principal ideal domain.

ii) For any ideal $J\subseteq S^{-1}R$, $J=S^{-1}I$ for some ideal $I$ of $R$. Since $R$ is a Dedekind ring, $I$ is finitely generated projective, that is, $I$ is a direct summand of $R^n$ for some $n$. Assume that $R^n=I\oplus I'$. Note that $J=S^{-1}R\otimes I$ and $S^{-1}R$ is flat, so we have 

$$(S^{-1}R)^n=S^{-1}R^n=S^{-1}R\otimes R^n=(S^{-1}R\otimes I)\oplus (S^{-1}R\otimes I')=J\oplus J'$$

and $J$ is a direct summand of $(S^{-1}R)^n$. So $J$ is also a finitely generated projective ideal. Now we finish the proof.
<p align="left">□</p>


# Ideal Theory in Dedekind Domains

Recall that we have defined invertible fractional ideal before in [[MATH/抽象代数III/Nodes/Dedekind Domains#^iazl34\|#^iazl34]].

> [!lemma]
> An integral domain $R$ is a Dedekind domain iff all fractional ideals are invertible. 
{ #jn8801}


**_Proof._**
- [ ] later

"->" Assume that $R$ is a Dedekind domain. Given a fractional ideal $I$, if $\lambda I\subseteq R$ with $\lambda\neq 0$, the map $I\to \lambda I,a\mapsto \lambda a$ is an isomorphism of $R$-module and $\lambda I$ is an ideal of $R$.   
??  
<p align="left">□</p>

For Dedekind domain, the dual $I^*$ of a fractional ideal $I$ is denoted by $I^{-1}$. 

> [!lemma]
> The set of fractional ideals of a Dedekind domain $R$ is an abelian group. The identity element is $R$, the inverse of a fractional ideal $I$ is $I^{-1}$. 

> [!definition]
> A fractional ideal $I$ of $R$ is called *integral ideal* if $I\subseteq R$. 
> 
> Let $I$ and $J$ be fractional ideal of $R$, we say $J$ divides $I$, that is, $J\mid I$, if there is an integral ideal such that $I=JK$. 

> [!lemma]
> Let $I$ be fractional ideals in a Dedekind domain $R$. TFAE:
> - $I\subseteq J$;
> - $J\mid I$.
{ #8e8e1e}


**_Proof._**
ii)->i) is easy. 

i)->ii). Let $K=J^{-1}I$. Then $I=JK$. Note that $J^{-1}I\subseteq J^{-1}J=R$ and so $J^{-1}I=K$ is an integral ideal. 
<p align="left">□</p>


> [!corollary]
> Every nonzero prime ideal of a Dedekind domain $R$ is maximal. 
{ #ib3ruw}


**_Proof._**
Assume that $p$ is a nonzero prime ideal and $p\subseteq I$ for some ideal $I$ of $R$. We aim to show $I=p$ or $I=R$. By [[MATH/抽象代数III/Nodes/Dedekind Domains#^8e8e1e\|#^8e8e1e]], there exists an ideal $I'$ such that $p=I'I$. Since $p$ is prime, one have either $I\subseteq p$ or $I'\subseteq p$.

- [ ] exercise: Since $p$ is prime, one have either $I\subseteq p$ or $I'\subseteq p$.

If $I\subseteq p$, we have done. If $I'\subseteq p$, then $p=pI$ and $I=R$. 
<p align="left">□</p>


> [!corollary] 
> A Dedekind domain is integral closed. 
{ #3gnir0}


**_Proof._**
Let $R$ be a Dedekind ring, and let $F$ be the fraction field of $R$. Let $x\in F$ be integral over $R$, i.e., $x^n+a_{n-1}x^{n-1}+\cdots+a_0=0$. Then $x$ belongs to the fractional ideal $I$ generated by $1,x,\cdots,x^{n-1}$. We can check $I^2=I$. So $I=I^2\cdot I^{-1}=II^{-1}=R$ and so $x\in R$. 

***Alternating proof.*** See [[MATH/抽象代数III/Nodes/Integrality and Integral Closures#^26zbyp\|Integrality and Integral Closures#^26zbyp]]. 
<p align="left">□</p>


> [!theorem] unique factorization of ideals in Dedekind domain
> Let $R$ be a Dedekind domain. Every nonzero proper ideal of $R$ can be written in a unique way as a product of prime ideals. 
{ #zio9cz}


**_Proof._**
**Step 1.** Prove any proper ideal is a product of prime ideals. 

If not, then there exists an ideal $I$ which is maximal among proper ideals which are not product of prime ideals. In particular, $I$ is not prime and so not maximal. So there exists a maximal ideal $J$ such that $I\subsetneq J\subsetneq R$. By [[MATH/抽象代数III/Nodes/Dedekind Domains#^8e8e1e\|#^8e8e1e]], $I=JK$ for some ideal $K$ of $R$. 

Note that $I\neq K$, otherwise $J=R$. Hence $I\subsetneq K\subsetneq R$. By maximality of $I$, $J$ and $K$ are products of prime ideals. So $I$ can be written as a product of prime ideal, which is a contradiction. 

**Step 2.** Uniqueness.

Assume that $I=p_1\cdots p_m=q_1\cdots q_n$ where $p_i$, $q_j$ are prime ideals. We do induction on $m$. Note that $q_1\cdots q_n\subseteq p_1$. Since $p_1$ is prime, there exists $j$ such that $q_j\subseteq p_1$. WLOG $j=1$ and $q_1\subseteq p_1$. By [[MATH/抽象代数III/Nodes/Dedekind Domains#^ib3ruw\|#^ib3ruw]], $p_1=q_j$ and then $p_2\cdots p_m=q_2\cdots q_n$. Apply inductive hypothesis and we finish the proof.
<p align="left">□</p>


> [!lemma]
> Let $R$ be a Dedekind domain. For any fractional ideal $I$, there exists integral ideals $J$ and $K$ such that $I=JK^{-1}$. 
{ #814a8z}


**_Proof._**
Since $I$ is a fractional ideal, there exists $\lambda\in R$ such that $\lambda I\subseteq R$. Let $J=\lambda I$ and $K=\lambda R$. Then $K^{-1}=(1/\lambda)R$ and $JK^{-1}=\lambda I\cdot(1/\lambda )R=I$. Now we finish the proof. 
<p align="left">□</p>

> [!definition]
> For every fractional ideal $I$, we write $I=\prod_{p}p^{\nu_p(I)}$ with $\nu_p(I)\in \mathbb{Z}$ and $p$ runs over all prime ideals. We call $\nu_p(I)$ the *valuation* of $I$ at $p$. 

