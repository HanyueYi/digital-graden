---
{"dg-publish":true,"permalink":"/MATH/抽象代数III/Nodes/Category and Hom, Tensor Functors/","dgPassFrontmatter":true}
---


# Category

> [!definition]
> A category $\mathcal D$ is called a subcategory of a category $\mathcal C$ if
> - the objects of $\mathcal D$ is a subclass of the objects of $\mathcal C$
> - for any objects $A,B$ of $\mathcal D$, one has that 
> 	- $\mathrm{Hom}_{\mathcal D}(A,B)\subseteq\mathrm{Hom}_{\mathcal C}(A,B)$;
> 	- $1_A$ and the product of morphisms for $\mathcal D$ is the same as for $\mathcal C$. 
> 
> The subcategory $\mathcal D$ is called *full* if $\mathrm{Hom}_{\mathcal D}(A,B)=\mathrm{Hom}_{\mathcal C}(A,B)$.

> [!definition]
> Let $\mathcal C$ be a category. Define $\mathcal C^{\mathrm{op}}$ as
> - objects of $\mathcal{C}^{\mathrm{op}}$ are the objects of $\mathcal{C}$
> - $\mathrm{Hom}_{\mathcal{C}^{\mathrm{op}}}(A,B)=\mathrm{Hom}_{\mathcal{C}^{\mathrm{op}}}(B,A)$
> 
> satisfying that
> - if $f\in \mathrm{Hom}_{\mathcal{C}^\mathrm{op}}(A,B)$ and $g\in \mathrm{Hom}_{\mathcal{C}^\mathrm{op}}(B,C)$, then $gf$ in $\mathcal{C}^\mathrm{op}$ equals $fg$ in $\mathcal{C}$; and
> - $1_{\mathcal{C}^\mathrm{op}}=1_{\mathcal{C}}$.

> [!definition]
> Let $\mathcal{C}$ and $\mathcal{D}$ be two categories. A *covariant functor* $F$ form $\mathcal{C}$ to $\mathcal{D}$ satisfies
> - for any object $X\in\mathcal{C}$, $F(X)$ is an object of $\mathcal{D}$;
> - for any $f\in\mathrm{Hom}_{\mathcal{C}}(X,Y)$, $F(f)\in\mathrm{Hom}_{\mathcal{D}}(F(X),F(Y))$ such that
>   
>   $$F(g \circ f)=F(g) \circ F(f) ,\mbox{ for any } f\in\mathrm{Hom}_{\mathcal{C}}(X,Y),g\in\mathrm{Hom}_{\mathcal{C}}(Y,Z)\tag{*}$$
> 
> - $F(\mathrm{id}_X)=\mathrm{id}_{F(X)}$.
> 
> If $(*)$ is modified to
> 
> $$F(g \circ f)=F(f) \circ F(g) ,\mbox{ for any } f\in\mathrm{Hom}_{\mathcal{C}}(X,Y),g\in\mathrm{Hom}_{\mathcal{C}}(Y,Z)$$
> 
> then $F:\mathcal{C}\to \mathcal{D}$ is called a *contravariant functor*. In particular, a contravariant functor from $\mathcal C$ to $\mathcal{D}$ is a covariant functor from $\mathcal{C}^\mathrm{op}$ to $\mathcal{D}$. 

**Remark.** In general, if $R$ is non-commutative, $\mathrm{Hom}_R(M,N)$ is not an $R$-module. Notice that 

$$(r_1r_2)f(m)=f(r_1r_2m)=(r_1f)(r_2m)=(r_2r_1f)(m)$$

and $r_1r_2,r_2r_1$ are not always equal.

## Hom Functor

In the category of $R$-modules, Hom functors can be defined as either covariant or contravariant, depending on whether the argument appears in the first or second slot.
- Given $R$-module $M$, define
  
  $$\begin{aligned}\mathrm{Hom}_R(M,\cdot):R\mbox{-module}&\to \mbox{Ab},\\N&\mapsto\mathrm{Hom}_R(M,N),\\f&\mapsto h_f:t\mapsto f\circ t.\end{aligned}$$
  
  We can verify that $\mathrm{Hom}_R(M,\cdot)$ is a covariant functor. 
- Similarly, given $R$-module $M$, define 
  
  $$\begin{aligned}\mathrm{Hom}_R(\cdot, M):R\mbox{-module}&\to \mathrm{Ab},\\N&\mapsto\mathrm{Hom}(N,M),\\f&\mapsto h_f:t\mapsto t\circ f\end{aligned}$$
  
  We can verify that $\mathrm{Hom}_R(\cdot, M)$ is a contravariant functor.


Similar results hold in the setting of bimodules.

> [!definition]
> Let $R$ and $S$ be rings with identity. An abelian group $M$ is a *left $R$- right $S$-bimodule* in case $M$ is both a left $R$-module and a right $S$-module for which the two scalar multiplication jointly satisfy $r(xs)=(rx)s$ for any $r\in R,x\in M,s\in S$. 
{ #559amp}


**Remark.** Here are some notations:
- ${}_RM$: $M$ is a left $R$-module
- $M_R$: $M$ is a right $R$-module
- ${}_{R}M_S$: $M$ is a left $R$- right $S$-bimodule.

Let $U:={}_RU_S$ be a bimodule. Then for any $R$-module ${}_RM$, 
- $\mathrm{Hom}_R(U,M)$ is a left $S$-module. 
	- For any $f\in\mathrm{Hom}_R(U,M)$, define $(sf)(u)=f(us)$. 
	- $\mathrm{Hom}_R(U,\cdot):R\mbox{-module}\to S\mbox{-module}$ is a covariant functor; 
- $\mathrm{Hom}_R(M,U)$ is a right module-$S$. 
	- For any $g\in\mathrm{Hom}_R(M,U)$, define $(gs)(m)=g(m)s$.
	- $\mathrm{Hom}_R(\cdot,U):R\mbox{-module}\to \mbox{module-}S$ is a contravariant functor. 

## Tensor Functor

Suppose $M={}_SM_R$ and $N={}_RN$ are two modules, then $M\otimes _RN$ is a $S$-module. Similarly, suppose $M=M_R$ and $N={}_RN_T$ are two modules, then $M\otimes_RN$ is a module-$T$. 

If ${}_SM_R$ and ${}_RN_T$ are bimodules, then $M\otimes_R N$ is a left $S$- right $T$-bimodule with $s(m\otimes n)=(sm)\otimes n$ and $(m\otimes n)t=m\otimes(nt)$. 

> [!proposition]
> Given a bimodule ${}_SU_R$, define 
> 
> $$U\otimes_R\cdot:R\mbox{-module}\to S\mbox{-module}, M\mapsto U\otimes_RM,f\mapsto \mathrm{id} _U\otimes f$$
> 
> and it is a covariant functor.
> 
> Similarly, define 
> 
> $$\cdot\otimes_RR:\mbox{module-}S\to \mbox{module-}R, M\mapsto M\otimes_RU,f\mapsto f\otimes\mathrm{id} _U$$
> 
> and it is also a covariant functor.


# Exact Sequence and Exact Functors


> [!definition]
> Let $F:R\mbox{-module}\to S\mbox{-module}$ be a covariant functor. 
> - We say $F$ is *left exact* if for any exact sequence $0\to N\stackrel{\varphi}{\to}M\stackrel{\psi}{\to}P$, the sequence $0\to F(N)\stackrel{F(\varphi)}{\to}F(M)\stackrel{F(\psi)}{\to}F(P)$ is exact. 
> - We say $F$ is *right exact* if for any exact sequence $N\stackrel{\varphi}{\to}M\stackrel{\psi}{\to}P\to 0$, the sequence $F(N)\stackrel{F(\varphi)}{\to}F(M)\stackrel{F(\psi)}{\to}F(P)\to 0$ is exact.

> [!definition]
> A contravariant $G:R\mbox{-module}\to\rm{Ab}$ is called left (rep. right) exact if it is a left (rep. right) exact as a covariant functor $(R\mbox{-module})^\mathrm{op}\to\rm{Ab}$. 

> [!definition]
> A functor is called *exact* if it is both left exact and right exact.

> [!theorem]
>  Let ${}_SU_R$ be a bimodule. The functor $U\otimes_R\cdot:R\mbox{-module}\to S\mbox{-module}$ is right exact. 

**_Proof._**
![Pasted image 20250316235524.png|500](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250316235524.png)

Remark that Theorem 7.4 is same as [[MATH/交换代数/Nodes/2 Modules#^60fa98\|2 Modules#^60fa98]]
<p align="right">□</p>
