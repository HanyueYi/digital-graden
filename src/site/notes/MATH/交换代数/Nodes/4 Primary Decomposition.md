---
{"dg-publish":true,"draft":false,"permalink":"/MATH/交换代数/Nodes/4 Primary Decomposition/","dgPassFrontmatter":true}
---


> 4.8 不讲，10.21 用 4.8，但不讲10.2！  
> 4.9-4.11 不讲。
> 包含4.1-4.7 + ch7 part2.  

> [!definition]
> We call $q\subsetneq A$ as a primary ideal, if all zero-divisors of $A/q$ are nilpotent. 

TFAE:
- $q\subsetneq A$ primary
- for any $x,y\in q$, $x\in q$ or $y^n\in q$ for some $n>0$
- for any $xy\in q$, $y\in q$ or $x^n\in q$ for some $n>0$
- for any $xy\in q$, one of $x,y\in q$, or, both $x^n,y^n\in q$ for some $n>0$. 

**_Proof._**
i)<->iv) is easy. Note that $xy\in q$ iff $\overline{xy}=0$ in $A/q$. 

The rest is trivial. 
<p align="left">□</p>

**Examples.**
- Any prime ideal is primary.
- For a ring homomorphism $f:A\to B$ with $q\subseteq B$ primary, then $q^c:f^{-1}(q)\subseteq A$ is primary. (Consider $A/q^c\hookrightarrow B/q$. )

> [!proposition]
> Let $q\subseteq A$ be a primary ideal. Then $r(q)=\text{smallest prime containing }q$. In this case, if $p=r(q)$, then we say $q$ is $p$-primary.
{ #a0aed8}


**_Proof._**
Recall that $r(q)=\cap_{p\supseteq q}p$, so it suffices to show $r(q)$ is a prime. If $xy\in r(q)$, then $x^ny^n\in q$. By definition, $x^{nn'}\in q$ or $y^{nn'}\in q$. Then one of $x$, $y\in r(q)$ and so $r(q)$ is prime.
<p align="left">□</p>


**Examples.**
- $(p^n)\subseteq \mathbb{Z}$ is $(p)$-primary. 
- A primary ideal is not necessary powers of prime ideal. 
	- $q=(x,y^2)\subseteq A=k[x,y]$. Then $A/q=k[y]/(y^2)$ and $q$ is primary. Note that $r(q)=(x,y)$ is a maximal ideal of $A$ and $p^2\subsetneq q\subsetneq p$. 
- A prime power is not necessary primary. 
	- Consider $p=(\overline x,\overline z)\subseteq A=k[x,y,z]/(xy-z^2)$. Notice that $A/p\simeq k[xy,z]/(x,z,xy-z^2)\simeq k[y]$ and so $p$ is prime. 
	- $p^2$ is not primary. Indeed, $\overline x\cdot \overline y=\overline z^2\in p^2$. Since $y^n\notin p^2$ and $\overline x,\overline y\notin p^2$, we know $p^2$ is not primary. 


> [!proposition]
> Let $\alpha\subseteq A$ be an ideal. If $r(\alpha)$ is a maximal ideal, then $\alpha$ is a primary. In particular, if $m\subseteq A$ is a maximal ideal, then $m^n$ is primary. 

**_Proof._**
Note that $\alpha\subseteq r(\alpha)=\cap_{p\supseteq\alpha}p=m$ is maximal. Then $m$ is the unique prime ideal containing $\alpha$, and so $m$ is the unique maximal ideal in $A/\alpha$. Hence $A/\alpha$ is a local ring. Suppose $xy\in \alpha$, if $x\notin m=r(\alpha)$, i.e., $x^n\notin \alpha$, then we aim to show $y\in \alpha$. Since $A/\alpha$ is local, $\overline x\in (A/\alpha)^\times$ and so $\overline y=0\in A/\alpha$. Thus, $y\in \alpha$. 

For "in particular" part, because $r(m^n)\supseteq m$ and $m$ is maximal, one have $r(m^n)=m$ and so $m^n$ is primary.
<p align="left">□</p>


> [!lemma]
> Let $q_i$ with $1\leqslant i\leqslant n$ be $p$-primary. Then $q=\cap_{i=1}^n q_i$ is $p$-primary.
{ #188cbb}


**_Proof._**
First, $r(q)=\cap r(q^i)=p$. Now, let $xy\in q$. Suppose $x\notin q$, then $x\notin q_i$ for some $i$ and so $y^n\in q_i$ for some $n$. Then $y\in r(q_i)=p=r(q)$ and so $y^n\in q$. 
<p align="left">□</p>


> [!lemma]
> Suppose $q$ is $p$-primary. For $x\in A$, we have
> - if $x\in q$, then $(q:x)=(1)=A$
> - if $x\notin q$, then $(q:x)$ is $p$-primary
> - if $x\notin p$, then $(q:x)=q$.
{ #2df6cb}


**_Proof._**
i) is trivial.  

iii) If $y\in (q:x)$, then $xy\in q$. Since $x\notin r(q)$, $y\in q$.

ii) Let $y\in (q:x)$, then $xy\in q$. Since $x\notin q$, there is $y\in r(q)=p$. Then $q\subseteq (q:x)\subseteq p$ and so $p=r(q)\subseteq r(q:x)\subseteq r(p)=p$. It remains to show $(q:x)$ is primary. For $yz\in (q:x)$ and $y\notin p$, we aim to show $z\in (q:x)$. Since $yz\in (q:x)$, we have $xyz\in q$. By $y\notin p$, $xy\in q$ and so $z\in (q:x)$. Now we finish the proof.
<p align="left">□</p>


> [!definition]
> A primary decomposition of ideal $\alpha\subseteq A$ is an expression $\alpha=\cap_{i=1}^n q_i$ for finitely many primary ideal. 
> - If it exists, then we can apply [[MATH/交换代数/Nodes/4 Primary Decomposition#^188cbb\|#^188cbb]] and assume $r(q_i)=p_i$ are all distinct. $(*)$
> - We can also "throw away" the big deals, that is, we can assume for all $i$, $q_i\not\supseteq\cap _{j\neq i}q_j$. $(**)$
> 
> We call a decomposition satisfying $(*)$ and $(**)$ a minimal decomposition. 

**Example.** In $\mathbb{Z}$, $(n)=\cap(p_i^{n_i})$ is the unique minimal decomposition. 

**Remarks.**
- possibly $\alpha$ has no primary decomposition
- could have more than one primary decomposition
- in theorem 7.13, $\alpha\subseteq A$ with Noetherian $A$, $\alpha$ has primary decomposition (not necessary unique)
- if $\alpha$ has a primary decomposition, then $n$ is unique. in theorem 4.5
- will see: primary decomposition is related with irreducible component of $\mathrm{Spec}(A/\alpha)$. 

> [!theorem] First uniqueness theorem
> Suppose $\alpha\in A$ is decomposable, and suppose $\alpha=\cap_{i=1}^n q_i$ is a minimal decomposition. Let $p_i=r(q_i)$. Then 
> 
> $$\{p_1,\cdots,p_n\}=\{\text{prime ideals of form }r(\alpha:x)\text{ with some }x\in A\}.\tag{*}$$
> 
> In particular, LHS is independent of the primary decomposition.
{ #3049a9}


**_Proof._**
**Step 1.** Show LHS $(*)\supseteq$ RHS $(*)$. 

For $x\in A$, one have $(\alpha:x)=\cap_{i=1}^n (q_i:x)$. It deduces $r(\alpha:x)=\cap_{i=1}^n r(q_i:x)$. By [[MATH/交换代数/Nodes/4 Primary Decomposition#^2df6cb\|#^2df6cb]],  

$$\cap_{i=1}^n r(q_i:x)=\cap_{x\notin q_j}p_j.$$

Now suppose $r(\alpha:x)\in\text{RHS}(*)$, that is, $\cap_{x\notin q_j}p_j=p$ prime, by [[MATH/交换代数/Nodes/1 Rings and Ideals#^tepoo1\|1 Rings and Ideals#^tepoo1]] $p=p_j$ for some $j$. Then $r(\alpha:x)=p=p_j\in \text{LHS}(*)$. 

**Step 2.** Show LHS $(*)\subseteq$ RHS $(*)$. 

Take $p_i\in \text{LHS}$. Suppose $\alpha=\cap _{i=1}^n q_i$ is a minimal decomposition. Then there exists $x\notin q_i$ such that $x=\cap_{j\neq i}q_j$. By [[MATH/交换代数/Nodes/4 Primary Decomposition#^2df6cb\|#^2df6cb]], $r(\alpha:x)=\cap_{i=1}^nr(q_i:x)=r(q_i:x)=p_i$ and so $p_i\in \text{RHS}$. 
<p align="left">□</p>


> [!definition]
> In [[MATH/交换代数/Nodes/4 Primary Decomposition#^3049a9\|#^3049a9]], we call $\{p_1,\cdots,p_n\}$ the associated primes of $\alpha$; or say $p_1,\cdots,p_n$ belong to $\alpha$. 

**Example.** $\alpha=(x^2,xy)=(x)\cap(x,y)^2$ is a minimal decomposition;

$A=k[x,y]=(x)\cap(x^2,y)$ is a minimal decomposition. 

Associated primes are $\{(x),(xy)\}$. 

> [!definition]
> In the associated primes $\{p_1,\cdots,p_n\}$, a minimal element is called a minimal (or isolated) associated prime ideal. Others are called embedded associated prime ideals.

> [!proposition]
> Suppose $\alpha$ is decomposable. Then minimal associated prime ideals 
> 
> $$\{p_1,\cdots,p_n\}\leftrightarrow\{\text{minimal elements in }\mathrm{Spec}(A/\alpha)\}\,,p_i\stackrel{\theta}{\mapsto} p_i/\alpha.$$
{ #6e2c2b}


**_Proof._**
If $p$ is prime, then $p\supseteq\alpha=\cap q_i$ yields $p\supseteq r(\alpha)=\cap r(q_i)=\cap p_i$. By [[MATH/交换代数/Nodes/1 Rings and Ideals#^tepoo1\|1 Rings and Ideals#^tepoo1]], $p\supseteq p_i$ for some $i$. So given a minimal element $p/\alpha$ on RHS, $p\supseteq p_i$. By minimality, $p=p_i$ and $p_i$ has to be minimal in LHS. So $\theta$ is surjective. 

In remains to show, if $p_i$ is minimal element in $\{p_1,\cdots,p_n\}$, then $p_i/\alpha$ is a minimal element in $\mathrm{Spec}(A/\alpha)$. Otherwise, minimal element $p_i\supsetneq p$ for some $p$ such that $p/\alpha$ is minimal in $\mathrm{Spec}(A/\alpha)$. But by Step 1, $p=p_j$ for some $j$ but $p_i\supsetneq p_j$ leading to a contradiction. 
<p align="left">□</p>

- [ ] existence of minimal prime

# Interlude: relation between primary decomposition and irreducible components

Recall that


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/math//nodes/1-rings-and-ideals/#gz1sp0" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



> [!proposition] Text-Ex. 1.19
> $\mathrm{Spec}A$ is [[MATH/代数几何/Nodes/1.5 Definition of Prevarieties and Morphisms#^pcfcsm\|irreducible]] iff $\mathrm{Nil}(A)$ is a prime ideal.  

</div></div>


and an irreducible component is defined as a maximal irreducible subspace.

- [ ] In general, irreducible component of $\mathrm{Spec}A$ are $V(p)$'s where $p$ is a minimal prime ideal.

If $\alpha$ is decomposable, then by [[MATH/交换代数/Nodes/4 Primary Decomposition#^6e2c2b\|#^6e2c2b]], $\mathrm{Spec}(A/\alpha)$ has finitely many irreducible components. 

**Example.** $k[x,y]\supseteq \alpha=(x^2,xy)=(x)\cap (x,y)^2$, then $(x)$ is the minimal associated prime ideal.

**Remark.** So above discussion, together with [[MATH/交换代数/Nodes/4 Primary Decomposition#^6e2c2b\|#^6e2c2b]] tells us, to compute irreducible components of $\mathrm{Spec}(A/\alpha)$, it suffices to find a primary decomposition of $\alpha$. 

**Remark.** Consider the closed subspace $V(\alpha)\subseteq \mathrm{Spec}(A)$ with induced topology, also $\mathrm{Spec}(A/\alpha)$ with its own topology. Then the map 

$$V(\alpha)\to \mathrm{Spec}(A/\alpha),p\mapsto p/\alpha$$

is a homeomorphism. 
- [ ] proof


> [!proposition]
> Let $\alpha=\cap_{i=1}^n q_i$ be a minimal decomposition with $r(q_i)=p_i$. Then $\cup_{i=1}^n p_i=\{x\in A:(\alpha:x)\neq \alpha\}$. In particular, if $0$ is decomposable, then the set of zero divisors of $A$, denoted by $D$, is the union of associate prime s of $0$. 

**_Proof._**
$\alpha=\cap_{i=1}^n q_i$ iff $\overline 0=\cap_{i=1}^n \overline {q_i}$ in $A/\alpha$. 

$(\alpha:x)\neq \alpha$ iff $(\overline 0:\overline x)\neq \overline 0$ in $A/\alpha$. 

So WLOG we can assume $\alpha=0$. 

So $D=\cup_{x\neq 0}(0:x)=\cup_{x\neq 0}r(0:x)$ because $r(D)=D$. Since $0=\cap_{i=1}^n q_i$, in the proof of [[MATH/交换代数/Nodes/4 Primary Decomposition#^3049a9\|#^3049a9]], $r(0:x)=\cap _{x\notin q_j}p_j\subseteq p_j$ for some $j$. Then $D\subseteq \cup_{i=1}^n p_i$. 

Also by [[MATH/交换代数/Nodes/4 Primary Decomposition#^3049a9\|#^3049a9]], each $p_i=r(0:x)$ with $x\notin q_i$, $x\notin \cap_{j\neq i}p_j$. Then $\cup_{i=1}^n p_i\subseteq D$
<p align="left">□</p>
# Part 2 of Chapter 7: primary decomposition in Noetherian rings


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/math//nodes/7-noetherian-rings/#primary-decomposition" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



# Primary Decomposition

> [!definition]
> Say an ideal $\alpha$ is irreducible, if for any $\alpha=\beta\cap \gamma$, then $\alpha=\beta$ or $\alpha=\gamma$. Say $\alpha$ is reducible, if $\alpha$ can be written as $\alpha=\beta\cap \gamma$ with $\beta,\gamma\supsetneq \alpha$. 


> [!lemma]
> Let $A$ be a Noetherian ring. Then any ideal is a finite intersection of irreducible ideals, that is, for any ideal $\alpha$, $\alpha$ can be written as $\alpha=\cap_{i=1}^n\beta_i$. 
**_Proof._**
Let $S=\{\alpha\subseteq A:\alpha\text{ is not a finite intersection of irreducible ideals}\}$. If $S\neq \emptyset$, then by $A$ Noetherian $S$ has a maximal element $\alpha$. Since $\alpha$ is reducible, $\alpha$ can be written as $\alpha=\beta\cap \gamma$ and both $\beta,\gamma$ are finite intersection of irreducible ideals, leading to contradiction. 
<p align="left">□</p>


> [!lemma]
> For a Noetherian ring $A$, an irreducible ideal is primary. 
**_Proof._**
Note that $\alpha\subseteq A$ is irreducible iff $\overline 0\subseteq A/\alpha$ is irreducible, and $\alpha\subseteq A$ is primary iff $\overline 0\subseteq A/\alpha$ is primary. So WLOG just consider the case where $0\subseteq A$ is an irreducible ideal. We aim to show $0$ irreducible yields $0$ primary. Suppose $xy=0$ and $y\neq 0$, it is enough to show $x^n=0$ for some $n$. Consider the chain 

$\mathrm{Ann} (x)\subseteq \mathrm{Ann} (x^2)\subseteq\cdots.$

As $A$ Noetherian, there exists $n$ such that $\mathrm{Ann}(x^n)=\mathrm{Ann}(x^{n+1})=\cdots$. 

We claim that $(x^n)\cap (y)=(0)$. For any $a\in (x^n)\cap (y)$, we have $ax=0$ by $xy=0$ and $a=x^nb$ for some $b\in A$. It deduces that $bx^{n+1}=0$ and $b\in \mathrm{Ann}(x^{n+1})=\mathrm{Ann}(x^n)$ and so $a=x^nb=0$. Now we prove the claim. 

Since $(0)$ is irreducible and $(y)\neq 0$, we have $(x^n)=(0)$ and so we finish the proof.
<p align="left">□</p>


> [!theorem]
> A Noetherian proper ideals have primary decomposition.  
**_Proof._**
By [[MATH/交换代数/Nodes/4 Primary Decomposition#^98d425\|#^98d425]] and [[MATH/交换代数/Nodes/4 Primary Decomposition#^3e8c56\|#^3e8c56]]. 
<p align="left">□</p>


> [!proposition]
> Let $A$ be a Noetherian ring, and let $\alpha$ be an ideal of $A$. Then $\alpha\supseteq (r(\alpha))^n$ for some $n$. 
**_Proof._**
Suppose $r(\alpha)$ is finitely generated by $x_1,\cdots,x_k$ with $x_i^n\in \alpha$ for big enough $n$. Then $\alpha\supseteq (r(\alpha))^{nk+1}$ and we have done. 
<p align="left">□</p>


> [!corollary]
> For a Noetherian ring $A$, then there exists $n$ such that $(\mathrm{Nil}(A))^n=0$. 

**_Proof._**
Take $\alpha=(0)$ in [[MATH/交换代数/Nodes/4 Primary Decomposition#^384015\|#^384015]]. 
<p align="left">□</p>


> [!corollary]
> Let $A$ be a Noetherian ring, and let $m\subseteq A$ be a maximal ideal. For an ideal $q\subseteq A$, TFAE:
> - $q$ is $m$-primary
> - $r(q)=m$
> - $m^n\subseteq q\subseteq m$ for some $n$

**_Proof._**
i)->ii) by definition. 

- [ ] ii)->i) by 4 ? 这个证明没看懂

ii)->iii) by [[MATH/交换代数/Nodes/4 Primary Decomposition#^384015\|#^384015]]

iii)->ii) obvious.
<p align="left">□</p>



</div></div>
