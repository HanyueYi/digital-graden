---
{"dg-publish":true,"draft":false,"permalink":"/MATH/抽象代数III/Nodes/Valuation Rings and DVRs/","dgPassFrontmatter":true}
---


# Valuations on Fields

## Exponential Valuations

> [!definition]
> Let $k$ be a field. An *(exponential) valuation* of $k$ is a real-valued function $\nu$ defined on $k^*=k\setminus\{0\}$ satisfying
> - $\nu(ab)=\nu(a)+\nu(b)$ and
> - $\nu(a+b)\geqslant \min\{\nu(a),\nu(b)\}$.
> 
> Note that $\nu:K^\times\to (R,+)$ is a group homomorphism. The image $\nu(k^\times)$ is called the value group of $\nu$, and we set $\nu(0)=\infty$. We call $(k,\nu)$ *valuation field*. 

**Facts.** 
- $\nu(1)=\nu(-1)=0$, $\nu(a)=\nu(-a)$, $\nu(a^{-1})=-\nu(a)$
- $\nu(a)>\nu(b)$ yields $\nu(a+b)=\nu(b)$, see 
	- Since $\nu(a+b)\geqslant\min\{\nu(a),\nu(b)\}=\nu(b)$, it suffices to show $\nu(a+b)>\nu(b)$ is impossible. Otherwise assume $\nu(a+b)>\nu(b)$ holds, then $\nu(b)=\nu(a+b+(-a))\geqslant \min\{\nu(a+b),\nu(a)\}>\nu(b)$, which is impossible. Hence $\nu(a+b)=\nu(b)$. 

> [!definition]
> Let $(k,\nu)$ be a valuation field. Then $R=\{a\in k:\nu(a)\geqslant 0\}$ is a subring of $k$, which is called *valuation ring* of $\nu$. 
> 
> Let $R^{-1}=\{a^{-1}:a\in R\setminus\{0\}\}=\{a\in k:\nu(a)<0\}$. Then $k=R\cup R^{-1}$ and so $k$ is a fractional field of $R$.
> 
> The set $P=\{a\in l:\nu(a)>0\}$ is an ideal of $R$, which is called the *valuation ideal* of $\nu$. 
> 
> The group of units of $R$ is $\{a\in k:\nu(a)=0\}$. 
> 
> Note that $R$ is a local ring with $P=J(R)=\{\text{nonunits of }R\}$, and $R/P$ is called *residue field* of $\nu$. 


> [!definition]
> Let $\lambda\in R$ with $\lambda >0$. Define $\nu'(a)=\lambda\nu(a)$ for all $a\in k^\times$. Then $\nu$ is also a valuation. We say $\nu$ is *equivalent* to $\nu'$, and write $\nu\sim \nu'$. 


> [!definition]
> A valuation $\nu$ of $k$ is called *discrete* if its value group is isomorphic to $\mathbb{Z}$. In this situation, $R$ is called a *discrete valuation ring*. 
> 
> In the case $\nu(k^\times)=\mathbb{Z}$, $\nu$ is said to be *normalized*. 


> [!theorem]
> Let $(k,\nu)$ be a discrete normalized valuation field. Let $R$ be its valuation ring, and let $P$ be its valuation ideal. 
> - Let $\pi\in R$ with $\nu(\pi)=1$. Then any $\alpha\in k$ is expressed as $\alpha=\pi^i u$ where $i=\nu(\alpha)$, $u\in R\setminus P$. 
> - Any nonzero ideal of $R$ is of the form $p^i=(\pi^i)$ for some $i\geqslant 0$. In particular, $R$ is a $PID$. 
> - $R$ is integral closed.
{ #bb0319}


**_Proof._**
i) For $\alpha\in k$ with $\nu(\alpha)=i$, we have $\nu(\alpha \pi^{-i})=0$ and $\alpha\pi^{-i}\in R\setminus P$. 

ii) Let $I$ be a nonzero ideal of $R$. Let $i=\min\{\nu(a):a\in I\}$. Then $\pi^i=a u^{-1}\in I$. Let $0\neq a\in I$ with $\nu(a)=j\geqslant i$. Then $a=\pi^j u=\pi^i(\pi^{j-i}u)\in (\pi^i)$. So $I=(\pi^i)$. In particular, $P=(\pi)$ and $I=P^i$.

iii) Take integral $\alpha\in k$, then there exists $a_i\in R$ such that 

$$\alpha^n+a_{n-1}\alpha^{n-1}+\cdots+a_0=0.$$

If $\alpha\notin R$, then $\alpha$ can be written as $\alpha=\pi^{-j}u$ with $j\in \mathbb{N}_+$. It deduces that 

$$u^n+a_{n-1} \pi^j u^{n-1}+a_{n-2} \pi^{2 j} u^{n-2}+\cdots+a_1 \pi^{(n-1) j} u+a_0 \pi^{n j}=0$$

and so 

$$u^n=-\pi^j\left(a_{n-1} u^{n-1}+a_{n-2} \pi^j u^{n-2}+\cdots+a_1 \pi^{(n-2) j} u+a_0 \pi^{(n-1) j}\right).$$

Note that $\nu(\text{LHS})=n\nu(u)=0$ and $\nu(\text{RHS})=j+\nu(x)$ with $x\in R$, then we have $0=j+\nu(x)>0$, which is impossible. Therefore, $\alpha\in R$. 
<p align="left">□</p>


> [!corollary]
> Two discrete valuations $\nu$ and $\nu'$ of $k$ are equivalent iff they have the same valuation ideal.
{ #ox907z}


**_Proof._**
Suppose that $\nu$ and $\nu'$ have the same valuation ideal, say $P$. Then $R=k\setminus P^{-1}$ is the valuation ring, where $P^{-1}=\{x^{-1}:x\in P\setminus \set0\}$. Suppose $\nu$ and $\nu'$ are normalized, then they have the same value in $R$ and so in $k$ by [[MATH/抽象代数III/Nodes/Valuation Rings and DVRs#^bb0319\|#^bb0319]]. Thus $\nu$ and $\nu'$ are equivalent of $k$. 
<p align="left">□</p>


> [!theorem]
> Discrete valuation ring is a local PID. 
{ #ve57xd}


**_Proof._**
"<-" Let $R$ be a local PID. Let $P=J(R)=(\pi)$. We claim that $\cap_{i=1}^\infty P^i=0$. Otherwise, if $0\neq a\in\cap_{i=1}^\infty P^i$, then $a=\pi a_1=\pi^2 a_2=\cdots$ with $a_i\in R$. It deduces that $a_i=\pi a_{i+1}$ and so we get a ascending series $(a_1)\subsetneq (a_2)\subsetneq \cdots$ Since $R$ is PID, the series terminate, leading to a contradiction. 

For any $0\neq a\in R$, there exists $i\in \mathbb{N}_+$ such that $a\in P^i$ and $a\notin P^{i+1}$. Thus $a=\pi^i u$ for some $u\in R\setminus P$.  Let $k$ be the fractional field of $R$. Define $\nu(a/b)=\nu(a)-\nu(b)$ and $\nu$ is a discrete valuation. 

"->" By [[MATH/抽象代数III/Nodes/Valuation Rings and DVRs#^bb0319\|#^bb0319]].
<p align="left">□</p>


## Multiplicative Valuation

> [!definition]
> Let $\nu$ be an exponential valuation of a field $k$. Fix a real number $\gamma$ with $0<\gamma<1$. Define $\varphi:k\to \mathbb{R},a\mapsto \gamma^{\nu(a)}$. Then 
> - $\varphi(a)\geqslant 0$ and $\varphi(a)=0$ yields $a=0$;
> - $\varphi(ab)=\varphi(a)\varphi(b)$
> - $\varphi(a+b)\leqslant \max\{\varphi(a),\varphi(b)\}$
> - $\varphi(a^{-1})=\varphi(a)^{-1}$
> - $\varphi(a)<\varphi(b)$ yields $\varphi(a+b)=\varphi(b)$. 
> 
> Define the valuation ring $R=\{a\in k:\varphi(a)\leqslant 1\}$ and valuation ideal $P=\{a\in k:\varphi(a)<1\}$. 
> 
> Two multiplicative valuation $\varphi_1$ and $\varphi_2$ are called equivalent if there exists $r\in \mathbb{R}_{\geqslant 0}$ such that $\varphi_2(a)=\varphi_1(a)^r$ for all $a\in k$. 

**Remark.** We can get a multiplicative valuation from an exponential valuation. For a given a function $\varphi:k\to R$ satisfying 
- $\varphi(a)\geqslant 0$ and $\varphi(a)=0$ yields $a=0$;
- $\varphi(ab)=\varphi(a)\varphi(b)$
- $\varphi(a+b)\leqslant \max\{\varphi(a),\varphi(b)\}$

define $\nu(a)=\log_{\gamma}\varphi(a)$, then $\nu$ is a valuation on $k$. 


> [!definition]
> Define $d(a,b)=\varphi(a-b)$, which is a **metric** on $k$. Then $k$ is a Hausdorff space and
> - $k\times k \to k,(a,b)\mapsto a+b$
> - $k\times k\to k,(a,b)\mapsto ab$
> - $k^\times\times k^\times\to k,(a,b)\mapsto ab^{-1}$
> 
> are continuous. 

# Completion

Recall that if every Cauchy sequence in $k$ converges, then $k$ is called *complete*, or a complete field. The associated valuation ring is said to be a complete valuation ring. 

Given a valuation field $k$, let $C$ denote the set of Cauchy sequence in $k$. Define $(a_n)+(b_n)=(a_n+b_n)$ and $(a_n)(b_n)=(a_nb_n)$. Then $C$ is a commutative ring. If $I$ denotes the subset of $C$ consisting of the sequences converge to $0$, then $I$ is a maximal ideal. Hence $\widetilde k=C/I$ is a field. 

If $(a_n)$ is a Cauchy sequence, then $|\varphi(a_m)-\varphi(a_n)|\leqslant \varphi(a_m-a_n)$. Hence $(\varphi(a_n))$ is a Cauchy sequence in $\mathbb{R}$ and $\lim_{n\to \infty} \varphi(a_n)$ exists. 
{ #147dxw}


If $(a_n)-(b_n)\in I$, then $\lim_{n\to\infty}\varphi(a_n)=\lim_{n\to \infty}\varphi(b_n)$. Define 

$$\widetilde \varphi:\widetilde k\to R,\widetilde{(a_n)}=\lim_{n\to \infty}\varphi(a_n)$$

for $\widetilde{(a_n)}=(a_n)+I$. It is well-defined by [[MATH/抽象代数III/Nodes/Valuation Rings and DVRs#^147dxw\|#^147dxw]]. Furthermore, we can check $\widetilde \varphi$ is a multiplicative valuation of $\widetilde k$. 

For $a\in k$, the sequence $(a)=(a,a,a,\cdots)$ is a Cauchy sequence and $\widetilde{(a)}\neq \widetilde{(b)}$ if $a\neq b$. Thus we can regard $k$ as a subfield of $\widetilde k$ by identifying $a$ with $\widetilde{(a)}$. So $\widetilde \varphi$ is an extension of $\varphi$ and $k$ is dense in $\widetilde k$ by definition. It deduces the following lemma. 


> [!lemma]
> $\widetilde k$ is a complete field. 


> [!theorem]
> Let $\widetilde R$ and $\widetilde P$ be the valuation ring and valuation ideal of $\widetilde \varphi$ respectively. Then $\widetilde R/\widetilde P\simeq R/P$. 

**_Proof._**
It suffices to show $R+\widetilde P=\widetilde R$. Note that $R+\widetilde P\subseteq \widetilde R$ is trivial. 

Let $a\in \widetilde R$ with $a\neq 0$. Then $0<\widetilde \varphi(a)\leqslant 1$ and there exists $a_n\in k$ such that $a=\lim_{n\to\infty} a_n$. Hence $\lim_{n\to\infty}\widetilde\varphi(a_n-a)=0$. So there exists $n$ such that $\widetilde \varphi(a_n-a)<\widetilde \varphi(a)$. 

Notice that $\varphi(a_n)=\widetilde\varphi(a_n-a+a)=\widetilde \varphi(a)\leqslant 1$ and $a_n\in R$. And $\widetilde \varphi(a_n-a)<\widetilde \varphi(a)\leqslant 1$ yields $a_n-a\in \widetilde P$, Then $a=a_n-a+a\in R+\widetilde P$. 
<p align="left">□</p>

# Valuations on Vector Spaces and Field Extensions
## Norms and Topology on Vector Spaces over Valued Fields

Let $\nu$ be a normalized discrete valuation of $k$ with valuation ring $R$ and valuation ideal $P=(\pi)$. Then $\{P,P^2,\cdots\}$ is a fundamental neighborhood system of $0$ by $\cap_{i=1}^\infty(\pi^i)=0$. Therefore, $(a_n)$ is a Cauchy sequence iff for any $\ell\in \mathbb{Z}_{>0}$, there exists $N$ such that $a_m-a_n\in P^\ell$ for all $m,n\geqslant N$. Also $\lim_{n\to \infty} a_n=a$ iff given $\ell$, there exists $N$ such that $a_n-a\in P^\ell$ for all $n\geqslant N$. 


> [!lemma]
> Let $\varphi_1,\varphi_2$ be discrete multiplicative valuations of $k$. TFAE:
> - $\varphi_1$ and $\varphi_2$ are equivalent;
> - $\{a\in k:\varphi_1(a)<1\}=\{a\in k:\varphi_2(a)<1\}$;
> - the topologies on $k$ induced by $\varphi_1$ and $\varphi_2$ are same. 

**_Proof._**
i)<->ii) See [[MATH/抽象代数III/Nodes/Valuation Rings and DVRs#^ox907z\|#^ox907z]].

ii)->iii) It suffices to show i)->iii), which is trivial because their fundamental neighborhood systems are equivalent. 

iii)->ii) Suppose $\varphi_1(a)<1$, then $\lim_{n\to\infty}\varphi_1(a^n)=\lim_{n\to\infty}\varphi_1(a)^n=0$. So $\lim_{n\to\infty}\varphi_2(a)^n=0$ and $\varphi_2(a)<1$. Similarly, $\varphi_2(a)<1$ yields $\varphi_1(a)<1$. 
<p align="left">□</p>


> [!definition]
> Let $\varphi$ be a multiplicative valuation of $k$. Let $V$ be a vector space over $k$. A real-valued function $||\cdot||$ defined on $V$ is said to be a *norm* on $V$ if 
> - $||v||\geqslant 0$ and $||v||=0\iff v=0$.
> - $||a v||=\varphi(a)||v||$ for any $a\in k$ and $v\in V$. 
> - $||u+v||\leqslant \max\{||u||,||v||\}$. 

If we set $d(u,v)=||u-v||$, then $V$ is a metric space. Note that $V\times V\to V,(u,v)\mapsto u+v$ and $k\times V\to V,(a,v)\mapsto av$ are continuous. Remark that norm induces metric, but not vice versa.

> [!lemma]
> Let $u_1,\cdots,u_n$ be a basis of a finite-dimensional $k$-space $V$. For $v=a_1u_1+\cdots+a_nu_n\in V$, define $||v||_0=\max\{\varphi(a_i):1\leqslant i\leqslant n\}$. Then $||\cdot||_0$ is a norm on $V$. The following holds for the metric indeed by $||\cdot||_0$. 
> - Let $\nu_r=a_{r_1}u_1+\cdots+a_{r_n}u_n$ be given for $r=1,2,\cdots$. Then the sequence $\{v_r\}_r$ is a Cauchy sequence iff the sequence $(a_{r_i})_r$ is a Cauchy sequence in $k$ for all $i=1,\cdots,n$. Also $\lim_{r\to\infty} v_r=\sum_{i=1}^n a_iv_i$ iff $\lim_{r\to \infty} a_{r_i}=a_i$ for all $i$. 
> - If $k$ is complete, then so is $V$. 

**_Proof._**
See [[MATH/抽象代数III/Nodes/HW10#^wlky1j\|homework]]. 
<p align="left">□</p>


> [!lemma] all norms are equivalent
> Suppose that $k$ is complete. Then for any norm $||v||$ on $V$, there exists constant $\lambda,\mu$ such that $||v||\leqslant \lambda||v||_0$, $||v||_0\leqslant \mu||v||$ for all $v\in V$. Thus the topological induces by these two norms are the same. 

**_Proof._**
Let $\lambda=\max\{||u_i||:1\leqslant i\leqslant n\}$. Then for $v=\sum_{i=1}^n a_iu_i$, $||v||\leqslant \max\{\varphi(a_i)||u_i||\}\leqslant \lambda||v||_0$. 

We will show the existence of $\mu$ by induction on $n$. 

The case of $n=1$ is trivial. Let $n>1$. For $v=a_1u_1+\cdots+a_nu_n$, set $\varphi_i(v)=\varphi(a_i)$. Claim that for all $i$, there exists $\mu_i$ such that $\varphi_i(v)\leqslant \mu_i||v||$. If it is true, then 

$$||v||_0=\max\{\varphi_i(v)\}\leqslant \max\{\mu_i||v||\}=(\max \{\mu_i\})||v||$$

and $\mu=\max\{\mu_i\}$ is what we desired.

Let $V'=ku_1\oplus\cdots\oplus ku_{n-1}$. By induction $||\cdot||$ and $||\cdot||_0$ induce the same topologies on $V$. In particular, $V'$ is complete w.r.t. $||\cdot||$ or $||\cdot||_0$. 

Suppose by way of contradiction that there is no $\mu_n$ with $\varphi_n(v)\leqslant \mu_n||v||$ for all $v\in V$. Then for any $j\in \mathbb{Z}_{>0}$, there exists $v_j\in V\setminus V'$ such that $\varphi_n(v_j)>j||v_j||$. 

This holds if $v_j$ is replaced by its nonzero scalar multiples, so we can assume that $v_j=a_{j,1}u_1+\cdots+a_{j,n-1}u_{n-1}+1\cdot u_n$. Then $||v_j||<1/j\varphi_n(v_j)=1/j$, which
yields $\lim_j v_j=0$ w.r.t. $||\cdot||$. So $\lim_{j}(v_j-u_n)=-u_n$. But note that $v_j-u_n\in V'$ for all $j$ and $V'$ is closed in $V$, so $-u_n\in V'$, leading to a contradiction. 
<p align="left">□</p>

## Extension of Valuations in Field Extensions

Let $K,L$ be discrete valuation fields with multiplicative valuation $\varphi$ and $\Phi$, respectively. If $K\subseteq L$ and $\Phi$ is an extension of $\varphi$, then we say $(L,\Phi)$ is an extension of $(K,\varphi)$, and write $(K,\varphi)\subseteq (L,\Phi)$. Consider $L$ as an $K$-space. Let $||x||=\Phi(x)$ for $x\in L$. 

> [!theorem]
> Let $\varphi$ be a complete discrete multiplicative valuation of $K$ and $L$ be a finite extension of $K$. If there exists an extension $(L,\Phi)$ of $(K,\varphi)$, then $\Phi$ is unique up to equivalent. Furthermore, $(L,\Phi)$ is complete. 

# $I$-adic Theory

Let $R$ be a ring, and let $V$ be an $R$-module. For an ideal $I\subseteq R$, assume that $\cap_{i=1}^\infty I^iV=0$. Fix $\gamma\in \mathbb{R}$ with $0<r<1$, define $||\cdot||_I$ on $V$ by 
- $||0||_I=0$
- $||v||_I=\gamma^i$ for $v\in I^iV\setminus I^{i+1}V$. 

Define $d_I(u,v):=||u-v||_I$. Check: $d_I(u,v)\leqslant \max\{d_I(u,w),d_I(w,v)\}$. So $d_I$ is a metric on $V$. 

In this situation, we say $d_I$ is defined on $V$. 

Note that
- $v_n\in V$, $\{v_n\}_n$ is a Cauchy sequence iff for any integer $m>0$, there exists $N>0$ such that $v_i-v_j\in I^n V$ for all $i,j\geqslant N$.
- $v=\lim_{n\to\infty}v_n$ iff for any integer $m>0$, there exists $N>0$ such that $v_i-v\in I^mV$ for all $i\geqslant N$. 

> [!lemma]
> The maps 
> - $V\times V\to V$, $(a,b)\mapsto a+b$
> - $R\times V\to V$, $(r,a)\mapsto ra$
> - $f\in \mathrm{Hom}_R(V,W)$, where for $W$ we define $d_I$ 
> 
> are continuous.

> [!theorem]
> Assume that $V$ is finitely generated. If $R$ is complete (w.r.t. $d_I$), then $V$ is complete. 
{ #ffpm0c}


**_Proof._**
Let $\{v_1,\cdots,v_s\}$ be a set of generators of $V$, and let $\{w_i\}$ be a Cauchy sequence in $V$. There exists a sequence $\{m(n)\}$ of nonnegative integers such that $w_i-w_j\in I^{m(n)}V$ for all $i,j>n$. Note that $m(n)\leqslant m(n+1)$ and $\lim_{n\to\infty}m(n)=\infty$. 

Let $w_1=\sum_{t=1}^s b_{1t}v_t$ for $b_{1t}\in R$, and let 

$$w_{n+1}-w_n=\sum_{t=1}^s a_{nt}v_t\,\text{ with }a_{nt}\in I^{m(n)}.$$

So $w_n=\sum_{i=1}^s b_{nt}v_t$ with $b_{nt}=b_{1t}+\sum_{j=1}^{n-1}a_{jt}$. Notice that $b_{n+k,t}-b_{n,t}=\sum_{j=n}^{n+k-1}a_{jt}\in I^{m(n)}$. Then $(b_{nt})_n$ is a Cauchy sequence in $R$. It yields $b_t=\lim_{n\to\infty} b_{nt}$ exists in $R$. Let $w=\sum_{t=1}^s b_tv_t$. It is easy to check $\lim_{n\to\infty}w_t=w$ and $V$ is complete. 
<p align="left">□</p>


> [!lemma]
> Suppose that $d_I$ is defined for all finitely generated $R$-modules. If $V$ is a finitely generated $R$-module, then every submodule of $V$ is closed. 

**_Proof._**
Let $W$ be a submodule of $V$. Since $f:V\to V/W$ is continuous, we have $W=f^{-1}(0)$ is closed. 
<p align="left">□</p>


Let $R$ be complete discrete valuation ring with valuation $\nu$, and let $P=(\pi)$ and $F=R/P$ be the valuation ideal and residue field of $\nu$ respectively. 

Let $V$ be a finitely generated $R$-module. Then $V=Ru_1\oplus \cdots\oplus R u_r$ is a direct sum of cyclic submodule. Since $(\pi^n)V=(\pi^n)u_1\oplus\cdots\oplus (\pi^n)u_r$, there is $\cap_{n=1}^\infty \pi^n V=0$. Then $d_P$ is defined for all finitely generated $R$-module. Since $R$ is complete, the module $V$ is also complete by [[MATH/抽象代数III/Nodes/Valuation Rings and DVRs#^ffpm0c\|#^ffpm0c]]. 

# 这又是什么，这不该在这一章吧

Let $A$ be an $R$-algebra, which is finitely generated as an $R$-module. 

**Fact.** $A\times A\to A,(a,b)\mapsto ab$ is continuous. 

$A^*=A/\pi A$ is a finitely generated $F$-algebra. 

> [!theorem]
> Let $A$ be finitely generated $R$-algebra. Then 
> - $A\pi\subseteq J(A)$;
> - $J(A)^n\subseteq A\pi$ for some $n>0$. 

**_Proof._**
i) Let $V$ be a simple $A$-module. Then either $\pi V=V$ or $\pi V=0$. Since $V=Av$ for any $0\neq v\in V$ and $A$ is finitely generated over $R$, we know $V$ is finitely generated over $R$. Thus if $\pi V=V$, then $V=0$ by [[MATH/交换代数/Nodes/2 Modules#^c2a5d0\|Nakayama lemma]]. So $\pi V=A\pi V=0$ and $A\pi\subseteq J(A)$. 

ii) Define $A^*=A/A\pi$. Then $J(A^*)=J(A)/A\pi$. Since $A^*$ is a finite-dimensional $F$-algebra, we have $A^*$ is Artinian and $J(A^*)$ is nilpotent. It deduces that $J(A)^n\subseteq A\pi$ for some $n>0$. 
<p align="left">□</p>


> [!theorem]
> Let $A$ be a finitely generated $R$-algebra. Let $I$ be an ideal of $A$ with $I\subseteq J(A)$ and $\overline A=A/I$. 
> - Let $\overline c$ be an idempotent in $\overline A$, and let $\overline c=\overline c_1+\cdots+\overline c_n$ be an idempotent decomposition in $\overline A$. Then $\overline c$ lifts to an idempotent $e$ of $A$ and there exists orthogonal idempotent $e_1,\cdots,e_n$ of $A$ satisfying $\overline e_i=\overline c_i$ and $e=e_1+\cdots+e_n$. 
> - An idempotent $e$ of $A$ is primitive iff $\overline e$ is primitive in $\overline A$.
> - Let $e,f$ be primitive idempotent of $A$, the. $Ae\simeq Af$ iff $\overline A\overline e\simeq \overline A\overline f$. 

**_Proof._**
$I\subseteq J(A)$ yields $I^m\subseteq A\pi$ for some $m$. Hence $I^m\subseteq A\pi^r$ for all $r\geqslant 1$. Set $\overline A^{(r)}=A/I^{mr}$. 

i) $I/I^m$ is an nilpotent ideal in $\overline A^{(1)}$. $\overline c$ lifts to a idempotent of $\overline A^{(1)}$, namely, there exists $c^{(1)}\in A$ such that $(c^{(1)})^2\equiv c^{(1)}\pmod{I^m}$ and $c^{(1)}\equiv c\pmod I$. 

Next, $I^m/I^{2m}$ is a nilpotent ideal in $\overline A^{(2)}$, there exists $c^{(2)}\in A$ such that $(c^{(2)})^2\equiv c^{(2)}\pmod{I^{2m}}$ and $c^{(2)}\equiv c^{(1)}\pmod{I^{(r-1)m}}$. 

Then $\{c(r)\}_r$ is a Cauchy sequence, and $e=\lim_{r\to\infty}c^{(r)}$ exists. We can check that $e$ is an idempotent of $A$ that lifts $\overline c$ to $A$. 

Show existence of $e_1,\cdots,e_n$. Let $e$ is any idempotent of $A$ that lifts $\overline c$. 

Similar as the above arguments, there exists $c_i^{(r)}\in A$ for each $r$ such that $c_i^{(r)}\equiv c_i^{(r-1)}\pmod{I^{(r-1)m}}$ and $e=c_1^{(r)}+\cdots+c_n^{(r)}\pmod I^{rm}$ is an idempotent decomposition in $\overline A^{(r)}$. 

Each $(c_i^{(r)})_r$ is a Cauchy sequence. Let $e_i=\lim_{r\to\infty} c_i^{(r)}$. Then $e_1,\cdots,e_n$ satisfy our requirement. 

ii) $J(A)$ has no idempotent. Similar as before.

iii) $Ae$ is the projective cover of $\overline A\overline e$. 




**Remark.** Let $I=A\pi$, then $\overline A=A^*$ where $A$ is an $R$-algebra, $A^*$ is an $F$-algebra and $k\otimes _R A$ is a $k$-algebra. 

定理描述了R代数和F代数之间的idem提升的性质