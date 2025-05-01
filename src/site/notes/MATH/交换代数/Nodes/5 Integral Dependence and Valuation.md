---
{"dg-publish":true,"draft":false,"permalink":"/MATH/交换代数/Nodes/5 Integral Dependence and Valuation/","dgPassFrontmatter":true}
---


> [!definition]
> Let $A\subseteq B$ be a subring. We say $x\in B$ is integral over $A$, if there exists a monic polynomial $f(T)\in A[T]$ such that $f(x)=0$. Remark that if $A$ is a field, then integral iff algebraic. 

**Examples.** 
- Suppose $x=r/s\in \mathbb{Q}$ is integral over $\mathbb{Z}$ with $(r,s)=1$ then 
  
  $$(r/s)^n+a_{n-1}(r/s)^{n-1}+\cdots+ a_1r/s+a_0=0$$
  
  with $a_i\in \mathbb{Z}$. Multiply by $s^n$, then $s\mid r^n$ and $s=1$. Thus $x\in \mathbb{Z}$. 
- $\mathbb{Z}\subseteq \mathbb{Q}[i]$, one can check $x\in \mathbb{Q}[i]$ integral over $\mathbb{Z}$ iff $x\in \mathbb{Z}[i]$. 

**Remark.** A finite extension $E/\mathbb{Q}$ is called a number field. The subset $\mathcal O_E\subseteq E$ with elements integral over $\mathbb{Z}$, is called the ring of integers. 

> [!proposition]
> Let $A\subseteq B$ be a subring. Let $x\in B$. TFAE:
> - $x$ is integral over $A$;
> - $A[x]$ is a finitely generated $A$-module;
> - $A[x]\subseteq C\subseteq B$ where $C$ is a subring, and $C$ is a finitely generated $A$-module;
> - there exists a faithful $A[x]$-module $M$, such that $M$ is a finitely generated $A$-module.
{ #jy6o7s}


**_Proof._**
i)->ii) Since $x$ is integral over $A$, we have $x^n+a_{n-1}x^{n-1}+\cdots+a_1x+a_0=0$ and so $A[x]=\left\langle 1,x,\cdots,x^{n-1}\right\rangle_A$ is finitely generated. 

ii)->iii) Let $C=A[x]$. 

iii)->iv) Let $M=C$. For $y\in \mathrm{Ann}(C)$, $y\cdot 1_C=0$ and $y=0$, that is, $M$ is faithful. 

iv)->i) Recall [[MATH/交换代数/Nodes/2 Modules#^41223f\|2 Modules#^41223f]], for a finitely generated $A$-module $M$, an ideal $\alpha\subseteq A$ and $\phi:M\to M$ such that $\phi(M)\subseteq \alpha M$, $\phi$ satisfies 

$$\phi^n+a_1\phi^{n-1}+\cdots+a_n=0.$$

In our situation, $M$ is a finitely generated $A$-module, and let 

$$\phi:M\to M,m\mapsto xm$$

be a homomorphism of $A$-modules with $\alpha=A$. Then there exist $a_1,\cdots,a_n\in A$ such that 

$$\phi^n+a+1\phi^{n-1}+\cdots+ a_n$$

kills $M$. Then $x^n+a_1x+\cdots+a_n\in\mathrm{Ann}(M)$. Since $M$ is an $A[x]$-module, we know $x$ is integral over $A$. 
<p align="left">□</p>


> [!corollary]
> For a subring $A\subseteq B$, where $x_1,\cdots,x_n\in B$ is integral over $A$, the ring $A[x_1,\cdots,x_n]$ is a finitely generated $A$-module. 
{ #ig1gwo}


**_Proof._**
By [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^jy6o7s\|#^jy6o7s]] and induction. 
<p align="left">□</p>


> [!corollary]
> For subring $A\subseteq B$, let $C=\{x\in B:x\text{ is integral over }A\}$. Then $C$ is a subring.
{ #4b091b}


**_Proof._**
Let $x,y\in C$, then $A[x,y]$ is a finitely generated $A$-module by [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^ig1gwo\|#^ig1gwo]]. By [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^jy6o7s\|#^jy6o7s]] iii), since $A[x\pm y]\subseteq A[x,y]\subseteq B$ and $A[xy]\subseteq A[x,y]\subseteq B$, we know $x\pm y$ and $xy$ are integral. Now we finish the proof.
<p align="left">□</p>


> [!definition]
> $C$ in [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^4b091b\|#^4b091b]] is called the integral closure of $A$ in $B$. 
> - If $C$ above is equal to $A$, then we say $A$ is integrally closed in $B$. 
> - If $C=B$, then we say $B$ is integral over $A$. 

**Remark.** Let $f:A\to B$ be a ring homomorphism. We say $f$ is an integral homomorphism if $B$ is integral over $f(A)$. In this case, we say $B$ is an integral $A$-algebra. 

**Note.** If $f$ is of [[MATH/交换代数/Nodes/2 Modules#^5pmtvz\|finite type]] and $f$ is an integral homomorphism, then $f$ is finite.

> [!corollary]
> If $A\subseteq_{\text{int}}B\subseteq_{\text{int}}C$, then $A$ is also integral over $C$. 
{ #342aup}


**_Proof._**
For any given $x\in C$, since $C$ is integral over $B$, there exists

$$x^n+b_{1}x^{n-1}+\cdots+ b_n=0$$

with $b_i\in B$. Consider $B'=A[b_1,\cdots,b_n]\subseteq B$, then $x$ is also integral over $B'$. Hence, $B'[x]$ is a finitely generated $B'$-module. Since each $b_i$ is integral over $A$, by [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^ig1gwo\|#^ig1gwo]] $B'$ is a finitely generated $A$-module and so for $B'[x]$. By [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^jy6o7s\|#^jy6o7s]] iii), $x$ is integral over $A$. 
<p align="left">□</p>


> [!corollary]
> For a subring $A\subseteq B$, let $C$ be the integral closure of $A$ in $B$. Then $C\subseteq B$ is integral closed. 

**_Proof._**
If $x\in B$ is integral over $C$, then by [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^342aup\|#^342aup]], $x$ is integral over $A$ and so $x\in C$. 
<p align="left">□</p>


> [!proposition]
> Let $B$ is integral over $A$. Then:
> - For an ideal $\beta\subseteq B$, let $\alpha=\beta\cap A$m then $B/\beta$ is integral over $A/\alpha$. 
> - If $S\subseteq A$ is multiplicative closed, then $S^{-1}B$ is integral over $S^{-1}A$. 
{ #f6d0xm}


**_Proof._**
i) For any $x\in B$, $x^n+a_{n-1}x^{n-1}+\cdots+a_0=0$ for some $a_i\in A$. Then $\overline x^n+\overline a_{n-1}\overline x^{n-1}+\cdots+\overline a_0=0$ and we finish the proof. 

ii) For any $x/s\in S^{-1}B$, there is

$$(x/s)^n+(a_1/s)(x/s)^{n-1}+\cdots+(a_0/s^n)=0$$

and so $x/s$ is integral over $S^{-1}A$. 
<p align="left">□</p>


# Going-up Theorem

> [!proposition]
> Let $A,B$ be integral domain with $B/A$ integral. Then $B$ is a field iff $A$ is a field. 
{ #mun8kw}


**_Proof._**
"<-" For any non-zero $y\in B$, there is 

$$y^n+a_{n-1}y^{n-1}+\cdots+a_1y+a_0=0.$$

Suppose $n$ is the minimal degree, which yields $a_0\neq 0$ by $A$ integral domain. Then 

$$y(y^{n-1}+a_{n-1}y^{n-2}+\cdots+a_1)=-a_0\neq 0$$

and so $y$ is a unit. Therefore, $A$ is a field. 

"->" Let $x\in A$ be non-zero. Since $B$ is a field, $x^{-1}\in B$. Since $B/A$ is integral, we have 

$$(x^{-1})^n+a_{n-1}(x^{-1})^{n-1}+\cdots+a_0=0$$

and so $x^{-1}=-(a_{n-1}+a_{n-2}x+\cdots+a_0x^{n-1})\in A$. 
<p align="left">□</p>


> [!corollary]
> Assume $B/A$ is integral. If $q\subseteq B$ is a prime ideal of $B$, then $q$ is maximal iff $q^c$ is maximal in $A$. 
{ #8zjrn5}


**_Proof._**
By [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^f6d0xm\|#^f6d0xm]], $B/q$ is integral over $A/q^c$. Then apply [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^mun8kw\|#^mun8kw]]. 
<p align="left">□</p>


> [!corollary]
> Suppose $B/A$ is integral. Let $q\subseteq q'\subseteq B$ be a prime ideal. If $q^c=q'^c=p\subseteq A$, then $q=q'$. 

**_Proof._**
Consider the following diagram. 

![Pasted image 20250428202432.png|430](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250428202432.png)

Note $f^{-1}(n)\supseteq p A_p=m$. Since $m$ is the unique maximal ideal of $A_p$, we know $f^{-1}(n)=m$. Similarly, $f^{-1}(n')=m$. 

By [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^f6d0xm\|#^f6d0xm]] $B_p$ is integral over $A_p$. 

By [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^8zjrn5\|#^8zjrn5]] $n$ and $n'$ are maximal in $B_p$, which deduces $n=n'$. 

Then $q=q'$ by [[MATH/交换代数/Nodes/3 Rings and Modules of Fractions#^961e0a\|3 Rings and Modules of Fractions#^961e0a]]. 
<p align="left">□</p>

我没听懂（）回头再看。

> [!corollary]
> Assume $A\subseteq_{\text{int}}B$. Then $\dim A\geqslant \dim B$. 
{ #2uikai}


**_Proof._**
Let $q_0\subsetneq q_1\subsetneq \cdots\subsetneq q_n$ be the largest chain of primes in $B$. Then 

$$q_0^c\subsetneq q_1^c\subsetneq \cdots\subsetneq q_n^c$$

is also a chain in $A$. Then $\dim A\geqslant n$. 
<p align="left">□</p>


> [!theorem]
> Let $B/A$ be integral. For any prime ideal $p\subseteq A$, there exists prime $q\subseteq B$ such that $q^c=p$. 
{ #k2927t}


**_Proof._**
Consider the following diagram

![Pasted image 20250428203212.png|280](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250428203212.png)

Let $n$ be any maximal ideal of $B_p$. By [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^8zjrn5\|5 Integral Dependence and Valuation#^8zjrn5]], $f^{-1}(n)$ is maximal and so $f^{-1}(n)=m$. Let $q=\beta^{-1}(n)$, which is a prime. Further 

$$q\cap A=\alpha^{-1}(f^{-1}(n))=\alpha^{-1}(m)=p$$

and so we finish the proof.
<p align="left">□</p>


> [!theorem] going-up theorem
> Assume $A\subseteq_{\text{int}}B$. Let $q_1\subseteq\cdots\subseteq q_n$ be a chain of prime ideals in $A$, and let $q_1\subseteq \cdots\subseteq q_m$ be a chain of prime ideals in $B$ with $0\leqslant m<n$ and $q_i^c=p_i$. Then one can extend the second chain to 
> 
> $$q_1\subseteq \cdots\subseteq q_{m}\subseteq q_{m+1}\subseteq\cdots \subseteq q_{n}$$
> 
> such that $q_i^c=p_i$ for all $i$. 
{ #whjkcj}


**_Proof._**
First, if $m=0$, then by [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^k2927t\|#^k2927t]] there exists $q_1$. So by induction, it suffices to show the case $n=2$, $m=1$. Namely, we now have $p_1\subseteq p_2\subseteq A$ and $q_1\subseteq\text?\subseteq B$. Consider $A/p_1\hookrightarrow B/q_1$, which is integral by [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^f6d0xm\|#^f6d0xm]]. Since $\overline p_2$ is prime in LHS, by [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^k2927t\|#^k2927t]] there exists $q_2/q_1$ such that $(q_2/q_1)^c=p_2/p_1$. Therefore, $q_2^c=p_2$. 
<p align="left">□</p>


> [!corollary]
> If $A\subseteq B$ is integral, then $\dim A=\dim B$. 

**_Proof._**
By [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^whjkcj\|#^whjkcj]], we have $\dim A\leqslant \dim B$. By [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^2uikai\|#^2uikai]] we finish the proof.
<p align="left">□</p>


# Integrally Closed Integral Domain

> [!proposition]
> Let $A\subseteq B$, and let $C$ be an integral closure of $A$ in $B$. For a multiplicative closed set $S\subseteq A$, $S^{-1}C$ is a integral closure of $S^{-1}A$ in $S^{-1}B$. 
{ #9iz2fs}


**_Proof._**
By [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^f6d0xm\|#^f6d0xm]], $S^{-1}C$ is integral over $S^{-1}A$. Now suppose $b/s\in S^{-1}B$ is integral over $S^{-1}A$, we aim to show $b/s\in S^{-1}C$. There is 

$$(b/s)^n+(a_1/s_1)(b/s)^{n-1}+\cdots+(a_n/s_n)=0$$

with $a_i/s_i\in S^{-1}A$. Multiply by $s^ns_1^n\cdots s_n^n$ and we get 

$$(bs_1\cdots s_n)^n+\cdots =0$$

and so $bs_1\cdots s_n$ is integral over $A$. Thus $bs_1\cdots s_n\in C$, leading to $b/s=(bs_1\cdots s_n)/(ss_1\cdots s_n)\in S^{-1}C$. 
<p align="left">□</p>


> [!definition]
> For any integral domain $A$, we say it is integrally closed, if $A$ is integral closed in $\mathrm{Frac} A$. 

**Example.** $\mathbb{Z}$, UFD (see [[MATH/抽象代数III/Nodes/7 250408#^ygwlsh\|here]]). 

> [!proposition] integrally closed is a local property
> For an integral domain $A$, TFAE:
> - $A$ is integrally closed;
> - $A_p$ is integrally closed for any prime ideal $p$;
> - $A_m$ is integrally closed for any maximal ideal $m$.

**_Proof._**
Let $C$ be the integral closure of $A$ in $\mathrm{Frac}A$. By [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^9iz2fs\|#^9iz2fs]], $C_p$ is the integral closed of $A_p$ in $\mathrm{Frac}(A_p)=\mathrm{Frac} A$. Since $A$ is integrally closed, we have $C=A$ and so $A_p=C_p$ for any prime ideal $p$. Then by [[MATH/交换代数/Nodes/3 Rings and Modules of Fractions#^766550\|3 Rings and Modules of Fractions#^766550]], $A_p=C_p$ for all $p$ iff $A_m=C_m$ for all $m$ iff $A=C$. 
<p align="left">□</p>


> [!definition]
> Let $A\subseteq B$, and let $\alpha\subseteq A$ be an ideal. Say $x\in B$ is integral over $\alpha$ if $x^n+a_1x^{n-1}+\cdots+a_n=0$ with $a_i\in \alpha$. The integral closure of $\alpha$ in $B$ is the set of all such elements. 


> [!lemma]
> Let $A\subseteq B$, and let $C$ be the integral closure of $A$ in $B$. For an ideal $\alpha\subseteq A$ with $\alpha^e\subseteq C$. then the integral closure of $\alpha$ in $B$ is $r(\alpha^e)\subseteq C$, which is an ideal in $C$.
{ #vwwek4}


**_Proof._**
"$\subseteq$" If $x\in B$ is integral over $\alpha$, then $x^n=-(a_1x^{n-1}+\cdots+a_n)\subseteq\alpha^e$ and so $x\in r(\alpha^e)$. 

"$\supseteq$" Consider $x\in r(\alpha^e)$, then $x^n=\sum_{i=1}^N a_ix_i$ with $a_i\in \alpha$ and $x_i\in C$. Consider $M=A[x_1,\cdots,x_N]\subseteq C$. Since $x_i$ is integral over $A$, we know $M$ is a finitely generated $A$-module by [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^jy6o7s\|#^jy6o7s]]. Consider $\phi:M\to M,m\mapsto x^nm$, where $\mathrm{im}(\phi)\subseteq \alpha M$. By [[MATH/交换代数/Nodes/2 Modules#^41223f\|2 Modules#^41223f]], there is 

$$\phi^m+b_1\phi^{m-1}+\cdots+b_m=0\;\text{with }b_i\in \alpha.$$

It deduces that $x^{mn}+b_1x^{n(m-1)}+\cdots+b_m=0$ by $\phi(1)=x^n$ and so $x$ is integral over $\alpha$. 
<p align="left">□</p>


> [!proposition]
> Let $A\subseteq B$ be two integral domains. Suppose $A$ is integrally closed and $\alpha\subseteq A$ is an ideal. If $x\in B$ is integral over $\alpha$, then $x$ is algebraic over $k=\mathrm{Frac}A$. Furthermore, if $\mathrm{Irr}(x,K)=t^n+a_1t^{n-1}+\cdots+a_n$, then $a_i\in r(\alpha)$. 
{ #fbc39e}


**_Proof._**
Since $x$ is integral over $\alpha$, we have $g(x)=x^m+b_1x^{m-1}+\cdots+ b_m=0$ with $b_i\in \alpha$. Then $b_i\in \alpha\subseteq A\subseteq \mathrm{Frac} A=k$ yields $x$ is algebraic over $k$. 

However, note possibly $m>n=\deg(\mathrm{Irr}(x,K))$. Now let $x_1,\cdots,x_n$ be all the roots of $f(t):=\mathrm{Irr}(x,K)$, then $x_1,\cdots,x_n$ are also roots of $g(x)$ and $x_i$ is integral over $\alpha$. By Vita's theorem, $a_i$ are symmetric functions in $x_i$. By [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^vwwek4\|#^vwwek4]], $a_i$ are integral over $\alpha$. 

Apply [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^vwwek4\|#^vwwek4]] in the setting $A\subseteq A\subseteq\mathrm{Frac}A$, and we know $a_i\in r(\alpha^e)=r(\alpha)$. Now we finish the proof.
<p align="left">□</p>


> [!theorem] Going-down theorem
> Let $A\subseteq B$ be integral domains. Suppose $A$ is integrally closed and $B$ is integral over $A$. Let $p_1\supseteq\cdots\supseteq p_n$ be a chain of prime ideals in $A$, and let $q_1\supseteq\cdots\supseteq q_m$ be a chain of prime ideals in $B$ with $q_i^c=p_i$ and $m<n$. Then there exists $q_1\supseteq\cdots\supseteq q_m\supseteq\cdots\supseteq q_n$ such that $q_i^c=p_i$.

**_Proof._**
The case of $n=1$ is trivial by [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^whjkcj\|#^whjkcj]]. For $n\geqslant 2$, similarly it suffices to consider the case of $n=2$ and $m=1$. So we have $p_1\supseteq p_2$ and $q_1\supseteq ?$. Recall [[MATH/交换代数/Nodes/3 Rings and Modules of Fractions#^7xys15\|3 Rings and Modules of Fractions#^7xys15]], for a ring homomorphism $A\to B$, prime ideal $p\subseteq A$ is a contraction iff $p^{ec}=p$. 

Consider $A\to B\to B_{q_1}$. Note prime ideals of $B_{q_1}$ are precisely $qB_{q_1}$ with $q\subseteq q_1\subseteq B$. By [[MATH/交换代数/Nodes/3 Rings and Modules of Fractions#^7xys15\|3 Rings and Modules of Fractions#^7xys15]], it suffices to prove $p_2B_{q_1}\cap A=p_2$. Notice that "$\supseteq$" is obvious. Now we prove "$\subseteq$". 

For any $x\in p_2B_{q_1}$, $x$ can be written as $x=y/s$ with $y\in p_2B$ and $s\in B-q_1$. By [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^vwwek4\|#^vwwek4]], integral closure of $p_2$ in $B$ is $r(p_2B)\supseteq p_2B$. Thus $y\in p_2B$ is integral over $p_2$. Since $A$ is integrally closed, by [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^fbc39e\|#^fbc39e]], 

$$\mathrm{Irr}(y,\mathrm{Frac}A)=t^r+u_1t^{r-1}+\cdots+u_r\tag{*}$$

with $u_i\in r(p_2)=p_2$. 

Now suppose $x\in p_2B_{q_1}\cap A$, $x=y/s$. Then $s=yx^{-1}$. Plug $y=xs$ to $(*)$, then divide $x^r$, get 

$$s^r+(u_1/x) s^{r-1}+\cdots+u_r/x^r=0\tag{**}$$

with coefficients in $\mathrm{Frac} A$. Thus $s$ is algebraic over $\mathrm{Frac} A$. Since $(*)$ is irreducible, we know $(**)$ is irreducible and so $\mathrm{Irr}(s,\mathrm{Frac} A)=(**)$. 

But $s\in B-q_1\subseteq B$ yields $s$ is integral over $A$. Apply [[MATH/交换代数/Nodes/5 Integral Dependence and Valuation#^fbc39e\|#^fbc39e]] with $\alpha=A$, then we get coefficients of $(**)$ are in $r(A)=A$. Define $v_i=u_i/x^r\in A$. 

Recall that we aim to show $x\in p_2$. Suppose otherwise, since $v_ix^r=u_i\in p_2$ and $x\notin p_2$, there is $v_i\in p_2$ and so $s^r\in p_2B\subseteq p_1B\subseteq q_1$, contradicting with $s\notin q_1$. 
<p align="left">□</p>


> [!notes] 高辉说：
> 
> “这一章要考的话，主要考integral的判别法则。”
> 
> “going up going down 不考，主要是欣赏一下。”