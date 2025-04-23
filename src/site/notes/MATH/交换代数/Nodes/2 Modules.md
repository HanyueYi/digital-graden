---
{"dg-publish":true,"permalink":"/MATH/交换代数/Nodes/2 Modules/","dgPassFrontmatter":true}
---


> Highlights: Nakayama lemma, snake lemma, tensor product, flatness

Define $\mathrm{Hom}_A(M,N)=\{A\mbox{-module homomorphisms }f:M\to N\}$. It has an $A$-module structure. The construction is "functorial", namely. If $u:M'\to M$ is a homomorphism, then it deduces a homomorphism 

$$\mathrm{Hom}(M,N)\to\mathrm{Hom}(M',N),f\mapsto f\circ u.$$

Similarly, given $v:N\to N'$, it induces a homomorphism $\mathrm{Hom}(M,N)\to \mathrm{Hom}(M,N')$.

**Example.** Compute $\mathrm{Hom}_\mathbb{Z}(\mathbb{Z}/4\mathbb{Z},\mathbb{Z}/6\mathbb{Z})$. Since $f(\overline1)$ is divisible by $3$, there is $f(\overline 1)\in\{\overline 0,\overline 3\}$. It deduces that $\mathrm{Hom}_\mathbb{Z}(\mathbb{Z}/4\mathbb{Z},\mathbb{Z}/6\mathbb{Z})\simeq \mathbb{Z}/2\mathbb{Z}$. 

**Easy Facts.**
- $\mathrm{Hom}_A(A,M)\simeq M,f\mapsto f(1)$
- For ideal $\alpha\subseteq A$, define $\alpha M=\{\sum_{i=1}^n \alpha_i x_i:\alpha_i\in \alpha,x_i\in M\}\subseteq M$ is a submodule. When $\alpha=(a)$, write $aM=(a)M$. 

> [!definition]
> For submodules $N,P\subseteq M$, define $(N:P)=\{a\in A:aP\subseteq N\}\subseteq A$ an ideal. Denote annihilator of $M$ as $\mathrm{Ann}(M):=(0:M)$. Note $M$ as an $A$-module can also be regarded as an $A/\mathrm{Ann}(M)$-module. Say $M$ is a faithful $A$-module if $\mathrm{Ann}(M)=0$. 

> [!proposition]
> $M$ is a finitely generated $A$-module iff there exists an surjective $A^n\twoheadrightarrow M$ iff $M$ is a quotient module of $A^n$.

# Nakayama Lemma

> [!proposition]
> Suppose $M$ is a finitely generated $A$-module, and $\alpha\subseteq A$ is an ideal. Let $\phi:M\to M$ be an endomorphism such that $\phi(M)\subseteq\alpha M$. Then $\phi$ satisfies an equation of form 
> 
> $$\phi^n+a_1\phi^{n-1}+\cdots+a_{n-1}\phi+a_n=0$$
> 
> on $M$ for some $a_i\in \alpha$, namely, $\sum_{i=0}^n a_i\phi^{n-i}(m)=0$ for all $m\in M$.
{ #41223f}


**Example.** Let $M=\mathbb{Z}e_1\oplus \mathbb{Z} e_2$ and $\alpha=(2)$. Define $\phi$ by $\phi\begin{pmatrix} e_1\\ e_2\end{pmatrix}=\begin{pmatrix} 2 & 0\\ 4 & 8\end{pmatrix}\begin{pmatrix} e_1\\ e_2\end{pmatrix}$. Then by Cayley-Hamilton, $(\phi-2)(\phi-8)=0$.

**_Proof._**
Choose a set of generators $\{e_1,\cdots,e_n\}$ of $M$. Then $\phi\begin{pmatrix}e_1\\\vdots \\e_n\end{pmatrix}=T\begin{pmatrix}e_1\\\vdots \\e_n\end{pmatrix}$ for some $T\in\mathrm{Mat}_{n\times n}(\alpha)$. Let $P(x)$ be the characteristic polynomial of $T$, then $P(\phi)=0$ by Cayley-Hamilton.
<p align="right">□</p>


> [!corollary]
> Let $M$ be a finitely generated $A$-module, and let $\alpha$ be an ideal of $A$ with $\alpha M=M$. Then there exists $x\equiv 1\pmod{ \alpha}$ such that $xM=0$.
{ #d05ae0}


**_Proof._**
Let $\phi=\mathrm{id}_M:M\to \alpha M=M$. By [[#^41223f]], $\phi$ satisfies 

$$\phi^n+\sum_{i=1}^n a_i \phi^{n-i}=0$$

on $M$ with $a_i\in \alpha$. Let $x=1+a_1+\cdots+a_n$, then $xM=0$.
<p align="right">□</p>


> [!proposition] Nakayama lemma
> Let $M$ be a finitely generated $A$-module, and let $\alpha\subseteq A$ be an ideal with $\alpha\subseteq\mathrm{Jac}(A)$. If $\alpha M=M$, then $M=0$.
{ #c2a5d0}


**_Proof._**
By [[#^d05ae0]] there exists $x=1+a$ with $a\in\mathrm{Jac}(A)$ such that $xM=0$. By [[MATH/交换代数/Nodes/1 Rings and Ideals#^h2e8bp\|1 Rings and Ideals#^h2e8bp]], $1+a\in A^\times$ and so $M=0$.
<p align="right">□</p>

**Remark.** The most useful situation is when $A$ is a local ring with $\alpha=m_A=\mathrm{Jac}(A)$. [[#^c2a5d0]] tells if $M$ is finitely generated and $m_AM=M$, then $M=0$. 
{ #mzvcc5}



> [!corollary]
> Let $M$ be a finitely generated $A$-module with submodule $N\subseteq M$. Let $\alpha\subseteq\mathrm{Jac}(A)$ be an ideal. Then $M=\alpha M+N$ yields that $M=N$.
{ #ffbd3c}


**_Proof._**
Apply [[#^c2a5d0]] to $M/N$. Since $M=\alpha M+N$, there is $M/N=\alpha(M/N)$ and then $M/N=0$. Therefore, $M=N$.
<p align="right">□</p>


> [!proposition]
> Let $(A,m_A)$ be a local ring. Let $k=A/m_A$. Let $M$ be a finitely generated $A$-module, then $M/m_AM$ is a vector space over $k$. Let $x_1,\cdots,x_n\in M$. Suppose $\overline{x_1},\cdots,\overline{x_n}$ is a basis of $M/m_AM$, then $x_1,\cdots,x_n$ generate $M$. 
{ #w0idub}


**_Proof._**
Let $N=\left\langle x_1,\cdots,x_n\right\rangle_A\subseteq M$. Then the composite $N\hookrightarrow M\twoheadrightarrow M/m_AM$ is surjective. It deduces that $M=N+m_AM$. By [[#^ffbd3c]], $M=N$ and so $x_1,\cdots,x_n$ generate $M$.
<p align="right">□</p>


**Remark.** This is quite similar to [[MATH/Cards/Nodes/Frattini Subgroup#^k9gxk1\|Frattini Subgroup#^k9gxk1]]—in fact, the Jacobson radical can be seen as an analogue of the Frattini subgroup, but in the setting of rings instead of groups.

# Exact Sequence


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/MATH/抽象代数II/Nodes/2.2 Modules/#4kfb14" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



> [!definition]
> - Let $A \stackrel{f}{\to} B\stackrel{g}{\to} C$ be a chain and homomorphism of $R$-modules. We say it is *exact* at $B$ if $\mathrm{Im} f=\ker g$.
> - A finite sequence $A_0\stackrel{f_1}{\to} A_1\stackrel{f_2}{\to}\cdots\stackrel{f_n}{\to}A_n$ is exact, if it is exact at each $A_i(1\leqslant i\leqslant n-1)$, that is, $\mathrm{Im} f_i=\ker f_{i+1}$ for any $i$.
> - If $0\stackrel{ 0}{\to}X\stackrel{f}{\to}Y\stackrel{g}{\to}Z\stackrel{0}{\to}0$ is exact, then we say it is *short exact*. 

</div></div>


**Remark.** Any exact sequence can be split into short exact sequences. Namely, given 
{ #4xqpdj}


$$\cdots\to M_{i-2}\stackrel{f_{i-1}}{\to} M_{i-1}\stackrel{f_i}{\to} M_i\stackrel{f_{i+1}}{\to} M_{i+1}\stackrel{f_{i+2}}{\to}M_{i+2}\to \cdots,$$

then we get $0\to \mathrm{im} f_i\to M_i\to M_i/\mathrm{im} f_i\to 0$ and $0\to \mathrm{im} f_{i+1}\to M_{i+1}\to M_{i+1}/\mathrm{im} f_{i+1}\to 0$, where $M_i/\mathrm{im} f_i=M_i/\ker f_{i+1}\simeq\mathrm{im} f_{i+1}$.

## Hom Functor

> [!proposition]
> - Let $M'\stackrel{u}{\to}M\stackrel{ v}{\to}M''\to 0$ $(*)$ be a sequence of $A$-module homomorphism. Then it is exact iff for any $A$-module $N$, the induced sequence
>   
>   $$0\to \mathrm{Hom}(M'',N)\stackrel{\overline{v}}{\to}\mathrm{Hom}(M,N)\stackrel{\overline{u}}{\to}\mathrm{Hom}(M',N)\tag{**}$$
>   
>   is exact, where $\overline v:f\mapsto f\circ v$ and $\overline u:g\mapsto g\circ u$. 
> - (dual statement) Let $0\to N'\stackrel{u}{\to} N\stackrel{v}{\to} N''(☺️)$ be a sequence. It is exact iff for any $A$-module $M$, the induced sequence 
>   
>   $$0\to \mathrm{Hom}(M,N')\stackrel{\overline u}{\to} \mathrm{Hom}(M,N)\stackrel{\overline v}{\to} \mathrm{Hom}(M,N'')\tag{☺️☺️}$$
>   
>   is exact.
{ #jj28ws}


**_Proof._**
i) "->" Assume $(*)$ is exact. It is enough to show $\overline v$ is injective and $\mathrm{im}\overline v=\ker\overline u$. If $\overline v (f)=0$, then $M\stackrel{v}{\to} M''\stackrel{f}{\to}N$ is zero. But $v$ is surjective, then $f=0$. Note that $\overline u\circ\overline v=0$ as $v\circ u=0$, and it deduces that $\mathrm{im}\overline v\subseteq \ker\overline u$. Conversely, for any $g\in\ker\overline u$, we aim to find $f$ such that $g=f\circ v$. For $x\in M''$, let $\hat x\in v^{-1}(x)$ and set $f(x)=g(\hat x)$. We can verify that $f$ is well-defined and is a homomorphism of $A$-modules. Hence $\mathrm{im}\overline v=\ker\overline u$. 

"<-" It suffices to show $v$ is surjective and $\mathrm{im} u=\ker v$. If $v$ is not surjective, then let $N=M''/\mathrm{im} v\neq 0$ and apply to $(**)$, that is, 

$$0\to\mathrm{Hom}(M'',M''/\mathrm{im} v)\stackrel{\overline v}{\to}\mathrm{Hom}(M,M''/\mathrm{im} v)\stackrel{\overline u}{\to}\mathrm{Hom}(M',M''/\mathrm{im} v)$$

is exact. The surjective map $\pi:M''\to M''/\mathrm{im} v$ is a non-zero map, but $\overline v(\pi)$ is a zero map, which is a contradiction. Hence $v$ is surjective. 

Take $N=M''$ and $\mathrm{id}\in \mathrm{Hom}(M'',M'')$. Then $(**)$ is exact yields that $\mathrm{id}\circ v\circ u=0$ and so $\mathrm{im} u\subseteq\ker v$. Finally, we check $\mathrm{im} u\supseteq \ker v$. Now we take $N=M/\mathrm{im} u$ and 

$$0\to\mathrm{Hom}(M'',M/\mathrm{im} u)\stackrel{\overline v}{\to}\mathrm{Hom}(M,M/\mathrm{im} u)\stackrel{\overline u}{\to}\mathrm{Hom}(M',M/\mathrm{im} u)$$

is exact. Define canonical map $\pi:M\to M/\mathrm{im} u$. Notice that $\pi\circ u=0$, then $\pi\in\ker \overline u=\mathrm{im}\overline v$. Then there exists $\phi\in \mathrm{Hom}(M'',M/\mathrm{im} u)$ such that $\phi\circ v=\pi$. It deduces that $\phi(v(x))=\pi(x)=0$ and $x\in \mathrm{im} u$. Now we finish the proof.

ii) "->" Assume that $(☺️)$ is exact. It is enough to show $\overline u$ is injective and $\ker \overline v=\mathrm{im} \overline u$. If $\overline u(f)=0$, then $u\circ f=0$. Since $u$ is injective, we have $f=0$ and so $\overline u$ is injective. Note that $\overline v\circ\overline u=0$ as $v\circ u=0$, so $\mathrm{im}\overline u\subseteq\mathrm{ker} \overline v$. For any $g\in\ker \overline v$, we aim to find $f$ such that $g=f\circ u$. For any $m\in M$, define $f(m)= u^{-1}(g(m))$. Since $g(m)\in\ker v=\mathrm{im} u$ and $u$ is injective, $f$ is well-defined and $g=f\circ u$. Hence $\mathrm{im}\overline u=\mathrm{ker}\overline v$. 

"<-" Assume that $(☺️☺️)$ is exact. It suffices to show $u$ is injective and $\ker v=\mathrm{im} u$. If $u$ is not injective, then $\ker u\neq 0$. Let $M=\ker u$ and apply it to $(☺️☺️)$. The inclusion map $\iota:\ker u\hookrightarrow N'$ is included in $\mathrm{Hom}(M,N')$ and $\overline u(\iota)=0$, which contradicts with $\overline u$ injective. Take $M=N'$ and $\mathrm{id}_{N'}\in\mathrm{Hom}(N',N')$ satisfies $\overline v\circ\overline u\circ f=v\circ u=0$, that is, $\mathrm{im} u\subseteq\ker v$. Conversely, take $M=\ker v$ and 

$$0\to \mathrm{Hom}(\ker v,N')\stackrel{\overline u}{\to} \mathrm{Hom}(\ker v,N)\stackrel{\overline v}{\to} \mathrm{Hom}(\ker v,N'')$$

is exact. Since $\iota':\ker v\to N$ is an element of $\mathrm{Hom}(\ker v,N)$ and $\overline v(\iota')=0$, there is $\iota'\in \ker\overline v=\mathrm{im}\overline u$ and so there exists $\phi$ such that $u\circ\phi=\iota'$. Then for any $m\in\ker v$, we have $m=\iota'(m)=u(\phi(m))$ and $m\in\mathrm{im} u$. Now we finish the proof.  
<p align="right">□</p>


**Remark.** 
- "$\to 0$" in $(*)$ is necessary. For example, consider $\mathbb{Z}\stackrel{\times 0}{\to}\mathbb{Z}\stackrel{\times 2}{\to}\mathbb{Z}$ is exact but right exact. Then $\mathrm{Hom}(\mathbb{Z},\mathbb{Z})\stackrel{\times 2}{\to} \mathrm{Hom}(\mathbb{Z},\mathbb{Z})\stackrel{\times 0}{\to}\mathrm{Hom}(\mathbb{Z},\mathbb{Z})$. 
- "$0\to$" on LHS of $(*)$ is useless, as it cannot add "$\to 0$" to $(**)$. Consider $0\to \mathbb{Z}\stackrel{\times 2}{\to}\mathbb{Z}\to \mathbb{Z}/2\mathbb{Z}\to 0$. Apply $\mathrm{Hom}(*,\mathbb{Z})$, then $0\to 0\to\mathbb{Z}\stackrel{\times 2}{\to}\mathbb{Z}\to 0$ is only left exact. 

## Snake Lemma

> [!proposition] snake lemma
> Consider a commutative diagram where both rows are short exact.
> 
> $$\begin{CD}0 @>>> M' @> G>> M @> H>> M'' @>>> 0 \\@. @V f' VV @V f VV @V f''VV @. \\0 @>>> N' @>g  >> N @> h>> N'' @>>> 0 \\\end{CD}$$
> 
> Then we have an exact sequence 
> 
> $$0\to\ker f'\to \ker f\to \ker f''\to \mathrm{coker}f'\to\mathrm{coker}f\to\mathrm{coker}f''\to 0.$$
> 
>
{ #jgbcg4}


**_Proof._**
Notice that $\ker f'\to\ker f\to \ker f''$ are restriction of $M'\to M\to M''$. We can check that $g$ and $h$ induce maps $\mathrm{coker} f'\to\mathrm{coker} f$ and $\mathrm{coker} f\to\mathrm{coker} f''$. So it suffices to construct $d:\ker f''\to \mathrm{coker} f'$. For any $x\in M''$, take $\hat x\in M$ and so $f(\hat x)\in \ker h$. Then define $\check x\in N'$ such that $g(\check x)=\hat x$ and $\overline {\check x}\in\mathrm{coker} f'$ is what we desire. It is easy to check this map is well-defined. 

It remains to check the sequence is exact. For convenience, define 

$$0\to\ker f'\stackrel{G'}{\to} \ker f\stackrel{H'}{\to} \ker f''\stackrel{d}{\to} \mathrm{coker}f'\stackrel{g'}{\to}\mathrm{coker}f\stackrel{h'}{\to}\mathrm{coker}f''\to 0.$$

For any $x\in\ker d\leqslant M''$, there exists $y\in M$ such that $H(y)=x$. By the definition of $d$, we know $f(y)=g(d(x))=0$ and so $y\in \ker f$. It deduces that $x\in\mathrm{im}(H')$. Conversely, for any $x\in\mathrm{im}(H')$, there exists $y\in\ker f$ such that $x=H'(y)$. By the definition of $d$, there is $g(d(x))=f(y)=0$ and $d(x)=0$. Thus $x\in \ker d$. Now we have proved $\ker d=\mathrm{im} H'$. 

For any $x\in\ker g'$, there is $g'(x)=0$ and so $g(\hat x)\in \mathrm{im} f$ for any given preimage $\hat x\in N'$. Then there is $y\in M$ such that $f(y)=g(\hat x)$. By the definition of $d$, we know $d(H(y))=x$. In addition, since $f''(H(y))=h(f(y))=h(g(\hat x))=0$, $H(y)\in \ker f''$. It yields that $x\in\mathrm{im} d$. Conversely, for any $x\in \mathrm{im} d$, there exists $y$ such that $d(y)=x$ and $z\in M$ such that $H(z)=y$ and $f(z)=g(\hat x)$ for any given $x\in N'$. By the definition of $d$, there is $g'(x)=\overline {f(z)}\in \mathrm{coker} f$ and so $g'(x)=0$, $x\in \ker g'$. Now we have proved $\mathrm{im} d=\ker g'$.
<p align="right">□</p>


**Remark.** It is a general case of [[MATH/抽象代数II/Nodes/2.2 Modules#^b0hne4\|short five lemma]].

# Tensor Product

**Motivations.**
- linear algebra: bilinear map
- algebraic geometry: fibre product of geometry spaces
- flatness: useful for localization

**Linear algebra.** Let $k$ be a field. Notice that bilinear map and linear map are different.
- Consider bilinear map $f:k^m\times k^n\to k^s$. It is different from $k$-linear map $k^{m+n}\stackrel{f'}{\to} k^s$, because $f(ax,ay)=a^2f(x,y)$ and $f'(ax,ay)=af(x,y)$. 
- Define $g:k\times k\to k,(a,b)\to a$, which is linear but not bilinear.
- A $k$-linear map $g:k\times k\to k^s$ is determined by $f(1,0)$ and $f(0,1)$; a $k$-bilinear map $g':k\times k\to k^s$ is determined by $f(1,1)$. 
- A $k$-bilinear map $h:k^m\times k^n\to k^s$ looks like a $k$-linear map $h:k^{mn}\to k^s$, as we will see $k^m\otimes k^n\simeq k^{mn}$. 

**Algebraic geometry.** Note a fact that $\mathrm{Spec}(A\times B)=\{p\times B,A\times q:p\in\mathrm{Spec}(A),q\in\mathrm{Spec}(B)\}$. Hence, $\mathrm{Spec}(\mathbb{C}[x]\times \mathbb{C}[y])=\mathrm{Spec} (\mathbb{C}[x])\sqcup\mathrm{Spec}(\mathbb{C}[y])$. By [[MATH/代数几何/Nodes/1.1 Some Algebra#^6rh0cw\|1.1 Some Algebra#^6rh0cw]], the set of maximal ideal of $\mathbb{C}[x,y]$ is $\mathrm{Spm}(\mathbb{C}[x,y])=\{(x-a,y-b):a,b\in \mathbb{C}\}$. In fact, $\mathbb{C}[x]\otimes \mathbb{C}[y]\simeq \mathbb{C}[x,y]$. 

**Flatness.** Consider $\mathbb{Z}$-bilinear map $f:\mathbb{Z}\times \mathbb{Z}/2\mathbb{Z}\to P$, which is determined by $f(1,\overline 1)$. Note that $f(1,\overline 1)+f(1,\overline 1)=f(1,\overline 0)=0$, then $f(1,\overline 1)\in P[2]$. In summary, the above bilinear map is same as a $\mathbb{Z}$-linear map $\widetilde f:\mathbb{Z}/2\mathbb{Z}\to P$. Later we will see $\mathbb{Z}\otimes _\mathbb{Z} \mathbb{Z}/2\mathbb{Z}\simeq \mathbb{Z}/2\mathbb{Z}$. 

> [!definition]
> Let $A$ be a ring, and let $M,N,P$ be $A$-modules. A map $f:M\times N\to P$ is $A$-bilinear if $f(ax+by,cz+dw)=acf(x,z)+adf(x,w)+bc f(y,z)+bdf(y,w)$. 

> [!proposition]
> Let $M$ and $N$ be $A$-modules. Then there exists a pair $(T,g)$ where $T$ is an $A$-module and $g:M\times N\to T$ is an $A$-bilinear map, with the universal property: Given any $A$-module $P$, and any $A$-bilinear map $f:M\times N\to P$, there exists unique $A$-linear map $f':T\to P$ such that $f=f'\circ g$, that is, $f$ factors through $g$. 
> 
> ![Pasted image 20250305212919.png|200](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250305212919.png)
> 
> Moreover if $(T,g)$ and $(T',g')$ are two such pairs with above property, then there exists unique isomorphism $j:T\to T'$ such that $j\circ g=g'$.
{ #aa5afc}


**_Proof._**
**Uniqueness.** Suppose $(T,g)$ and $(T',g')$ are two distinct pairs with the property above. Apply $T$ with $P=T'$ and $T'$ with $P=T$, then there exist $j:T\to T'$ and $j':T'\to T$ such that $j'\circ j=j\circ j'=\mathrm{id}$. 

![Pasted image 20250305213258.png|180](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250305213258.png)

**Existence.** Let $C$ be the free $A$-module $A^{M\times N}$, namely, a free $A$-module with basis $\{(x,y):x\in M,y\in Y\}$. So an element in $C$ has unique expression $\sum_{i=1}^n a_{i}(x_i,y_i)$. Let $D$ be the submodule of $C$ generated by the following elements:
- $(x+x',y)-(x,y)-(x',y)$,
- $(x,y+y')-(x,y)-(x,y')$,
- $(ax,y)-a(x,y)$,
- $(x,ay)-a(x,y)$.

Let $T=C/D$. For $(x,y)\in C$, denote $x\otimes y$ as image in $T=C/D$. Thus, $T$ is generated by $\{x\otimes y:x\in M,y\in N\}$. Now define 

$$g:M\times N\to T,(m,n)\mapsto m\otimes n,$$

which is a $A$-bilinear map. We now verify the universal property. Let $f:M\times N\to P$ be a bilinear map. It suffices to construct $f':T\to P$ such that $f=f'\circ g$. We define $\overline f:C=A^{M\times N}\to P,(m,n)\mapsto f(m,n)$, and we can easily see $D\subseteq \ker \overline f$. So $\overline f$ induces a map $f':C/D=T\to P$. Remark that 

$$f'\circ g(m,n)=f'(m\otimes n)=f(m,n)$$

and so $f'\circ g=f$. Hence, for each bilinear map $f:M\times N\to P$, we can find $f'$ such that $f'\circ g=f$ and so $(T,g)$ is what we desire. 
<p align="right">□</p>


> [!definition]
> Call the module $T$ above as the *tensor product* of $M$ and $N$, also denote as $T=M\otimes_AN$. Sometimes, just $M\otimes N$ if the context is clear. Also the map $g:M\times N\to M\otimes N$ is simply $g((m,n))=m\otimes n$. In particular, the $A$-module $M\otimes_AN$ is generated by $\{m\otimes n:m\in M,n\in N\}$. Indeed, if $\{m_i:i\in I\}$ generates $M$ and $\{n_i\}$ generates $N$, then $\{m_i\otimes n_j:i\in I,j\in J\}$ generates $M\otimes_AN$. 

**Remark.** Not all elements of $M\otimes_AN$ is of the form $x\otimes y$. In other word, $g:M\times N\to M\otimes N$ is in general not surjective. For example, let $M=\mathbb{Z}e\oplus \mathbb{Z} f$ and $N=\mathbb{Z}g\oplus \mathbb{Z}h$, then $e\otimes g+f\otimes h\in M\otimes_\mathbb{Z}N$ cannot equal to some $x\otimes y$ with $x\in M$ and $y\in Y$. 

> [!proposition]
> Let $M,N,P$ be $A$-modules. Then there exists unique isomorphisms:
> - $M\otimes N\to N\otimes M$ such that $x\otimes y\mapsto y\otimes x$;
> - $(M\otimes N)\otimes P\to M\otimes(N\otimes P)\to M\otimes N\otimes P$;
> - $(M\oplus N)\otimes P\to (M\otimes P)\oplus (N\otimes P)$;
> - $A\otimes M\to M$ such that $a\otimes x\mapsto ax$.
{ #9968ad}


**_Proof._**
i) Consider $f:M\times N\to N\otimes M,(x,y)\mapsto y\otimes x$ and $g:M\times N\to M\otimes N,(x,y)\mapsto x\otimes y$. By [[#^aa5afc]], there exists unique $f':M\otimes N\to N\otimes M$ such that the diagram commutes. 

![Pasted image 20250317192406.png|250](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250317192406.png)

Now, in a parallel way, use the universal property of $N\otimes M$, then we get $\widetilde{f'}(n\otimes m)=m\otimes n$ such that the diagram commutes.

![Pasted image 20250317192848.png|250](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250317192848.png)

It is easy to check $f'$ and $\widetilde{ f'}$ are inverse to each other. 

iv) Consider

![Pasted image 20250317193646.png|220](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250317193646.png)

where $f:A\times M\to M,(a,m)\mapsto am$, then there exists unique $f':A\otimes M\to M$ such that the diagram commutes. Now define $h:M\to A\otimes M,m\mapsto 1\otimes m$. To check $f'$ and $h$ are inverse to each other, it suffices to check $a\otimes m=1\otimes am$. 

Recall the proof of [[#^aa5afc]], let $C$ be the free $A$-module $A^{M\times N}$ and $D$ be the $A$-submodule generated by $(x+x',y)-(x,y)-(x',y)$, $(x,y+y')-(x,y)-(x,y')$, $(ax,y)-a(x,y)$ and  $(x,ay)-a(x,y)$. Let $T=C/D$, and let $g:M\times N\to T,(m,n)\mapsto m\otimes n$. So we must have 

$$(a,m)-(1,am)=(a,m)-a(1,m)+a(1,m)-(1,am)\in D$$

which yields $g((a,m))=g((1,am))$ and so $a\otimes m=1\otimes am$. 
<p align="right">□</p>



> [!proposition]
> Let $M_1,\cdots,M_r$ be $A$-module. Then there exists $(T,g)$ where $g:M_1\times \cdots\times M_r\to T$ is a multilinear map such that for any $A$-module $P$ and multilinear map $f:M_1\times \cdots\times M_r\to P$, there exists unique $f$ such that the diagram commutes. 
> 
> ![Pasted image 20250317200619.png|250](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250317200619.png)
{ #ml3hwi}


**_Proof._**
Similar to [[#^aa5afc]]. 
<p align="right">□</p>

## Strange Things about Tensor Product

Consider $M'\subseteq M$ and $N'\subseteq N$, then $M'\times N'\hookrightarrow M\times N$ is submodule. However, it could happen $M'\otimes N'\to M\otimes N$ is not injective. Use the following diagram to define the map.

![Pasted image 20250317201420.png|250](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250317201420.png)

**Example.** Let $A=\mathbb{Z}$, $M=\mathbb{Z}\cdot e\supseteq M'=\mathbb{Z}\cdot(2e)$, and let $N=\mathbb{Z}/2\mathbb{Z}\cdot f =N'$. So we have 

$$\mathbb{Z}\cdot(2e)\otimes _{\mathbb{Z}}(\mathbb{Z}/2\mathbb{Z})\cdot f\to \mathbb{Z}\cdot e\otimes_\mathbb{Z} (\mathbb{Z}/2\mathbb{Z})\cdot f,2e\otimes f\mapsto 2e\otimes f=e\otimes 2f=0.$$

Claim that $2e\otimes f\neq 0$ in LHS. In fact, we have the following commutative diagram. 

![Pasted image 20250317203330.png|400](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250317203330.png)

Here we use the isomorphism $(\mathbb{Z}\cdot 2e)\otimes_\mathbb{Z}(\mathbb{Z}/2\mathbb{Z})\cdot f\stackrel{\sim}{\to}\mathbb{Z}\cdot e\otimes (\mathbb{Z}/2\mathbb{Z}\cdot f), 2e\otimes f\mapsto e\otimes f$. Recall that $(\mathbb{Z}\cdot e)\otimes_\mathbb{Z}(\mathbb{Z}/2\mathbb{Z}\cdot f)\simeq (\mathbb{Z}/2\mathbb{Z})\cdot f$ by [[#^9968ad]]. So the bottom row being zero map implies the top row is zero map. 

**Remark.** A (practical) guide to tensor product:
- $x\in M\otimes _AN$ is of form $x=\sum_{i=1}^N m_i\otimes n_i$
- get familiar with common operation on $\otimes$
- always keep in mind the expression $x=\sum m_i\otimes n_i$ is NOT unique
- the universal property are not really used in practice like [[#^9968ad]] (you should remember and be able to apply [[#^9968ad]])
- common pitfall: $2x\otimes y\in M\otimes_{\mathbb{Z}}N$ and it is not equal to $1/2 x\otimes 4y$

## Bimodule

> [!definition]
> Let $A,B$ be rings. We say $M$ is an $(A,B)$-bimodule, if it is both an $A$-left module and a $B$-right module, and $(ax)b=a(xb)$ for any $a\in A$, $b\in B$ and $x\in M$. Remark that $ab$ might not exist.

**Remark.** It has been defined in [[MATH/抽象代数III/Nodes/2 250304#^559amp\|2 250304#^559amp]], but I write it again.

> [!proposition] Text-Ex. 2.15.
> Let $A,B$ be rings. Let $M$ be an $A$-module, $P$ be a $B$-module and let $N$ be a $(A,B)$-bimodule. Then $M\otimes _AN$ is a $B$-module and $N\otimes_BP$ is an $A$-module, and we have an isomorphism of $(A,B)$-bimodule
> 
> $$(M\otimes_A B)\otimes_B P\simeq M\otimes_A (N\otimes_B P).$$
{ #489zft}


**_Proof._**
It is easy to check $M\otimes _AN$ is a $B$-module and $N\otimes_BP$ is an $A$-module. The proof of isomorphism of $(A,B)$-bimodule is similar to [[#^9968ad]], ii). 

Fix $z\in P$, define $M\times N\to M\otimes _A (N\otimes_B P),(x,y)\to x\otimes(y\otimes z)$. It is $A$-bilinear and it induces an $A$-linear map $f_z:M\otimes_A N\to M\otimes _A(N\otimes _BP),x\otimes y\mapsto x\otimes(y\otimes z)$.

Define $(M\otimes_AN)\times P\to M\otimes _A(N\otimes _BP),(t,z)\mapsto f_z(t)$, and it is $B$-bilinear. Son it induces a $B$-linear map $(M\otimes_AN)\otimes_BP\to M\otimes_A(N\otimes_BP)$. To prove it is isomorphism, it suffices to construct its inverse, which can be done similarly.
<p align="right">□</p>


> [!corollary]
> Suppose $\sum_{i=1}^n x_i\otimes y_i=0$ in $M\otimes_AN$, with $x_i\in M,y_i\in N$. Then there exists some finitely generated submodule $M_0\subseteq M$ and $N_0\subseteq N$ such that $\sum_{i=1}^n x_i\otimes y_i=0$ in $M_0\otimes_A N_0$. Remark that $M_0\otimes N_0\to M\otimes N$ is not injective, see [[#Strange Things about Tensor Product]] as example.
{ #6zw2e4}


**_Proof._**
Since $\sum_{i=1}^n x_i\otimes y_i=0$ in $M\otimes_AN =C/D$ with $C=A^{M\times N}$, there is $\sum_{i=1}^n x_i\otimes y_i\in D$. Then 

$$\begin{aligned}
\sum_{i=1}^n x_i\otimes y_i=&a_1((x_1+x_1',y_1)-(x_1,y_1)-(x_1',y_1))+a_2((x_2+x_2',y_2)-(x_2,y_2)-(x_2',y_2))+\cdots\\
+&b_1((\alpha_1,\beta_1+\beta_1')-(\alpha_1,\beta_1)-(\alpha_1,\beta_1'))+b_2((\alpha_2,\beta_2+\beta_2')-(\alpha_2,\beta_2)-(\alpha_2,\beta_2'))+\cdots\\
+&c_1((a\gamma,\delta)-a(\gamma,\delta))+\cdots\\ 
+&d_1((\epsilon,b\theta)-b(\epsilon,\theta))+\cdots
\end{aligned}\tag{*}$$

Let $M_0$ be the submodule generated by $(x_1+x_1',x_2+x_2,\cdots,\alpha_1,\cdots,a\gamma,\cdots,\epsilon_1,\cdots)$ and $x_1,\cdots,x_n$. Similarly define $N_0$ be the submodule generated by the second coordinates on RHS and $y_1,\cdots,y_n$. We claim that RHS of $(*)$ in $M_0\otimes N_0$ is also an element in $D_{M_0\times N_0}\subseteq C_{M_0\times N_0}$. 
<p align="right">□</p>


# Restriction and Extension of Scalars

> [!definition]
> Let $f:A\to B$ be a ring homomorphism, and let $N$ be a $B$-module. Then we can also regard $N$ as an $A$-module, so that, for any $a\in A$ and $x\in N$, define $ax=f(a)x$. This $A$-module is said to be obtained from $N$ via *restriction of scalars*.

**Example.** Define $f:\mathbb{Z}\to \mathbb{Q}$ and $N$ is a vector space over $\mathbb{Q}$. Then $N$ can be regarded as a $\mathbb{Z}$-module.

> [!proposition]
> Let $f:A\to B$ and $N$ be a $B$-module as above. Suppose $B$ is finitely generated as $A$-module and $N$ is a finitely generated $B$-module. Then $N$ is also finitely generated as $A$-module.

**_Proof._**
Let $B=\left\langle b_1,\cdots,b_n\right\rangle_A$ and $N=\left\langle n_1,\cdots,n_s\right\rangle_B$. Then $N=\left\langle b_in_j:1\leqslant i\leqslant n,1\leqslant j\leqslant n\right\rangle_A$. 
<p align="right">□</p>


> [!definition]
> Let $f:A\to B$ be a ring homomorphism. Since $M$ is a $A$-module, we can define $M_B=B\otimes_A M$. This is an $A$-module, and it is indeed an $(B,A)$-bimodule via $b(b'\otimes m)a:=bb'\otimes_A am$. We say this $B$-module $M_B$ is obtained via *extension of scalars*.

**Example.** Define $f:\mathbb{Z}\to \mathbb{Q}$ and $M=\mathbb{Z}\oplus \mathbb{Z}/2\mathbb{Z}$. Then $M_\mathbb{Q}=(\mathbb{Z}\oplus \mathbb{Z}/2\mathbb{Z})\otimes_\mathbb{Z}\mathbb{Q}=\mathbb{Q}$, because
- $\mathbb{Z}\otimes _\mathbb{Z} \mathbb{Q}=\mathbb{Q}$ and
- $\mathbb{Q}\otimes_\mathbb{Z}\mathbb{Z}/2\mathbb{Z}=0$ by $x\otimes y=x/2\otimes 2y=0$. 

> [!proposition]
> Assume $f:A\to B$ be a ring homomorphism and $M$ is a finitely generated $A$-module. Then $M_B=B\otimes_AM$ is a finitely generated $B$-module. 

**_Proof._**
Since $M=\left\langle x_1,\cdots,x_n\right\rangle_A$, we have $M_B=\left\langle 1\otimes x_1,\cdots,1\otimes x_n\right\rangle_B$. 
<p align="right">□</p>


# Exactness Property of the Tensor Product

> [!theorem]
> Let $M,N,P$ be $A$-modules, then we have natural isomorphism
> 
> $$\phi:\mathrm{Hom}_A(M\otimes_AN,P)\to\mathrm{Hom}_A(M,\mathrm{Hom}_A(N,P)).$$
>
{ #60fa98}


**_Proof._**
Take $f$ in LHS, and define $\phi(f)$ as follows. For each fixed $x\in M$, the map $f_x:N\to P,n\mapsto f(x\otimes n)$. It is $A$-linear and so $f_x\in \mathrm{Hom}_A(N,P)$. It is easy to check the map 

$$\phi(f):M\to \mathrm{Hom}_A(N,P),x\mapsto f_x$$

is $A$-linear. 

Conversely, given $g$ in RHS. Define 

$$M\times N\to P,(m,n)\mapsto g(m)(n),$$

which is $A$-bilinear and it induces $\psi(g):M\otimes N\to P$. 

Finally, check $\psi$ and $\phi$ are inverse each other. 
<p align="right">□</p>


**Example.** Recall $\mathbb{Z}/m\otimes _\mathbb{Z} \mathbb{Z}/n\simeq \mathbb{Z}/(m,n)$ (See [[MATH/抽象代数III/Nodes/HW2#^rbitq6\|here]] or [[Pasted image 20250319204119.png|here]]). We claim that $\mathrm{Hom}_\mathbb{Z}(\mathbb{Z}/m\mathbb{Z},\mathbb{Z}/n\mathbb{Z})\simeq \mathbb{Z}/(m,n)\mathbb{Z}$. Note that any $f$ in LHS is completely determined by $f(\overline 1)$. Since $f(\overline m)=0$, $f(\overline1)$ is killed by $m$. That is, for any lift $x\in \mathbb{Z}$ of $f(\overline 1)$, we have $n\mid mx$ and so $n/(m,n)\mid x$. Therefore, $\mathrm{Hom}_\mathbb{Z}(\mathbb{Z}/m\mathbb{Z},\mathbb{Z}/n\mathbb{Z})\simeq n/(m,n)\mathbb{Z}/n\mathbb{Z}\simeq \mathbb{Z}/(m,n)\mathbb{Z}$. 

**Example.** Put $\mathbb{Z}/12\mathbb{Z}$, $\mathbb{Z}/2\mathbb{Z}$ and $\mathbb{Z}/6\mathbb{Z}$ to [[#^60fa98]], then we have 

$$\mathrm{Hom}(\mathbb{Z}/12\mathbb{Z}\otimes \mathbb{Z}/2\mathbb{Z},\mathbb{Z}/6\mathbb{Z})\simeq \mathrm{Hom}(\mathbb{Z}/12\mathbb{Z},\mathrm{Hom}(\mathbb{Z}/2\mathbb{Z},\mathbb{Z}/6\mathbb{Z}))$$

where LHS $\simeq\mathrm{Hom}(\mathbb{Z}/2\mathbb{Z},\mathbb{Z}/6\mathbb{Z})\simeq \mathbb{Z}/2\mathbb{Z}$ and RHS $\simeq \mathrm{Hom}(\mathbb{Z}/12\mathbb{Z},\mathbb{Z}/2\mathbb{Z})\simeq \mathbb{Z}/2\mathbb{Z}$. 

> [!proposition]
> Let $M'\to M\to M''\to 0(*)$ be a right exact sequence of $A$-modules. Let $N$ be any $A$-module. Then the sequence 
> 
> $$M'\otimes_A N\stackrel{\widetilde f}{\to} M\otimes_A N\stackrel{\widetilde g}{\to} M''\otimes_A N\to 0\tag{**}$$
> 
> is still right exact.

**_Proof._**
Note that it is easy to see $\widetilde g$ is surjective. It remains to check $\ker \widetilde g\simeq \mathrm{im} \widetilde f$. By [[#^jj28ws]], it suffices to show for any $A$-module $P$, 

$$0\to\mathrm{Hom}(M'\otimes N,P)\to \mathrm{Hom}(M\otimes N,P)\to \mathrm{Hom}(M''\otimes N,P)$$

is left exact. By [[#^60fa98]], it is equivalent to show 

$$0\to \mathrm{Hom}(M',\mathrm{Hom}(N,P))\to \mathrm{Hom}(M,N\otimes P)\to \mathrm{Hom}(M'',N\otimes P)$$

is left exact. By [[#^jj28ws]], we have done. 
<p align="right">□</p>

**Remark.** 
- $\text{right}\to 0$ is necessary. For example, $0\to \mathbb{Z} \stackrel{\times 2}{\to} \mathbb{Z}$ is exact, but after tensor $\mathbb{Z}/2\mathbb{Z}$ we get $0\to \mathbb{Z}/2\mathbb{Z}\to 0$, which is not exact. 
- a left $0\to$ does not product similar result. For example, $0\to \mathbb{Z}\stackrel{\times 2}{\to}\mathbb{Z}\to \mathbb{Z}/2\mathbb{Z}\to 0$ is exact, but after tensor $\mathbb{Z}/2\mathbb{Z}$ we get $0\to \mathbb{Z}/2\mathbb{Z}\stackrel{\times 2}{\to}\mathbb{Z}/2\mathbb{Z}\to Z/2\mathbb{Z}\to 0$ is right exact but not left exact. 
{ #g6xwy9}


> [!definition]
> We say an $A$-module is a *flat $A$-module*, if for any exact sequence 
> 
> $$\cdots\to M_{i-1}\to M_i\to M_{i+1}\to \cdots,\tag{*}$$
> 
> the tensor product sequence $(*)\otimes N$ is still exact. 
{ #8m15t3}


**Examples.** 
- $\mathbb{Z}/2\mathbb{Z}$ is not flat by [[#^g6xwy9|it]]. 
- The $A$-module $A$ is a flat $A$-module.
- $A^{\oplus n}$ is flat $A$-module. 

> [!proposition]
> Let $N$ be a $A$-module. TFAE:
> - $N$ is flat.
> - For any short exact sequence $0\to M'\to M\to M''\to 0(*)$, $(*)\otimes_A N$ is still short exact. 
> - For any injective map $f:M'\hookrightarrow M$, $f\otimes 1$ is also injective.
> - For any injective map $f:M'\hookrightarrow M$ with $M',M$ finitely generated, $f\otimes 1$ is still injective.

**_Proof._**
i)<->ii) is trivial as [[#^4xqpdj|each long exact sequence can be split into short exact sequence]]. 

iii)->iv) is easy. 

i)=ii)->iii) by considering $0\to M'\to M$ exact. 

iii)->ii) When iii) holds, $\otimes$ preserves right exactness. Furthermore, $\otimes_AN$ preserves left exactness by [[#^8m15t3]] and so for short exact sequence.

It remains to show iv)->iii). Suppose $u=\sum_{i=1}^n x_i'\otimes y_i\in \ker(M'\otimes N\to M\otimes N)$, that is, $f(u)=\sum_{i=1}^n f(x_i')\otimes y_i=0$. We aim to show $u=0$. Let $M_0'=\left\langle x_1',\cdots,x_n'\right\rangle_A\subseteq M'$. Let $u_0=\sum_{i=1}^n x_i'\otimes y_i$ be an element in $M_0'\otimes N$. Remark that we do not know if $u_0$ is also zero, as $M_0\otimes N$ may not a submodule of $M'\otimes N$ by [[#Strange Things about Tensor Product]]. 

[[#^6zw2e4]] says that for $\sum_{i=1}^nf(x_i')\otimes y_i=0\in M\otimes N$, there exists finitely generated submodule $M_0\subseteq M$ containing $f(M_0')$ and finitely generated submodule $N_0\subseteq N$ such that $\sum_{i=1}^n f(x_i')\otimes y_i=0$ in $M_0\otimes N_0$. So in particular, from injective map $f:M'\hookrightarrow M$, we have injective map $f:M_0'\hookrightarrow M_0$. Since $M_0'$ and $M_0$ are finitely generated, by iv) we have $M_0'\otimes N\to M_0\otimes N$ is injective. Note that $\sum_{i=1}^n f(x_i)\otimes y_i=0$ in $M_0\otimes N$, then we have $u_0=\sum_{i=1}^n x_i'\otimes y_i$ is $0$ in $M_0'\otimes N$. It deduces that $\sum_{i=1}^n x_i'\otimes y_i=0$ in $M'\otimes N$. 
<p align="right">□</p>


> [!theorem] Text-Ex. 2.20.
> Let $f:A\to B$ be a ring homomorphism and let $N$ be a flat $A$-module. Then $N_B=N\otimes _AB$ is a flat $B$-module. Remark that $N_B$ in general is not flat $A$-module. 

**_Proof._**
Let $M'\hookrightarrow M$ be an injective map of $B$-modules. It remains to show $M'\otimes_BN_B\to M\otimes _BN_B$ is still injective. But 

$$M'\otimes_B N_B=M'\otimes_B(B\otimes_AN)=(M'\otimes_B B)\otimes _AN=M'\otimes_A N$$

and then the map $M'\otimes_A N\to M\otimes_A N$ is injective by $N$ being a flat $A$-module.
<p align="right">□</p>


**Remark.** Let $f:\mathbb{Z}\to \mathbb{Z}/2\mathbb{Z}$ and $N=\mathbb{Z}$. But $N_B=\mathbb{Z}/2\mathbb{Z}$ is not flat over $\mathbb{Z}$. 

# Algebra and Tensor Product of Algebra

> [!definition]
> Given a ring homomorphism $f:A\to B$, we say $B$ is an $A$-algebra. Note that $B$ has an $A$-module structure which is compatible with ring struction on $B$, that is, $(f(a)b)c=f(a)(bc)$. 

**Examples.**
- Any ring is a $\mathbb{Z}$-algebra.
- Field extension $E/K$ is a $K$-algebra with $K\hookrightarrow E$.

> [!definition]
> Given $f:A\to B$ and $g:A\to C$, a ring homomorphism $h:B\to C$ is called a homomorphism of $A$-algebra if it is also a $A$-module homomorphism (i). Equivalently, $h$ is an $A$-algebra homomorphism iff the following diagram commute (ii).
> 
> ![Pasted image 20250324201824.png|160](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250324201824.png)

**_Proof._**
i)->ii). ii) means $h(f(a))=g(a)$. Note that if i) holds, then

$$h(f(a))=h(a\cdot 1_B)=a\cdot h(1_B)=a\cdot 1_C=g(a).$$

ii)->i) It suffices to show $h(ab)=ah(b)$. By

$$h(ab)=h(f(a)b)=h(f(a))h(b)=g(a)h(b)=ah(b)$$

we finish the proof.
<p align="right">□</p>

**Example.** Recall given field extensions $E/K$ and $F/K$, $E$ and $F$ are $K$-algebras and $f:E\to F$ is a field homomorphism. $f$ is also a homomorphism of $K$-vector spaces iff $f$ is a homomorphism between $k$-algebra iff $f:E\to F$ is a homomorphism such that $f(k)=k$ for any $k\in K$ iff the diagram commutes. 

![Pasted image 20250324202837.png|170](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250324202837.png)

> [!definition]
> - Say $f:A\to B$ is a finite morphism of rings, if $B$ is a finitely generated $A$-module. In this case, say $B$ is a finite $A$-algebra.
> - Say $f:A\to B$ is of finite type, if there exists $x_1,\cdots,x_n\in B$ such that any $b\in B$ can be written as a polynomial in $x_1,\cdots,x_n$ with coefficient in $f(A)$. It is equivalent to there exists surjective map $A[t_1,\cdots,t_n]\twoheadrightarrow B, t_i\to x_i$. In this case, say $B$ is a finitely generated $A$-algebra. 
>   
> So finite $A$-algebra is a finitely generated $A$-algebra.

**Examples.**
- $\mathbb{Q}\to \mathbb{Q}(i)$ is a finite $\mathbb{Q}$-algebra
- $\mathbb{Q}\to \mathbb{Q}[x,y]$ is of finite type
- $\mathbb{Q}\to \mathbb{Q}[x,y]/(x^2+y^2)$ is of finite type
- $\mathbb{Q}\to \mathbb{Q}[x,y]/(x^2,y^2)$ is a finite $\mathbb{Q}$-algebra

> [!definition]
> For a ring $A$, we say it is finitely generated if it is finitely generated as $\mathbb{Z}$-algebra. 

**Example.** $A=\mathbb{Z}[x,y]/(x^2+y^2)$

**a Construction on Page 31.** Let $f:A\to B$ and $g:A\to C$ be two ring homomorphisms. Let $D=B\otimes _AC$. Claim that we can define ring structure on $D$ and make it an $A$-algebra. 

**_Proof._**
Consider $B\times C\times B\times C\to D,(b,c,b',c')\mapsto bb'\otimes cc'$. By [[#^ml3hwi]] above, it induces an $A$-linear map 

![Pasted image 20250324204449.png|270](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250324204449.png)

By [[#^aa5afc]], this is the same as an $A$-bilinear map $\mu:D\times D\to D$ with $\mu(b\otimes c,b'\otimes c')=bb'\otimes cc'$. One can check this $\mu$ (used as multiplication) is compatible with $+$ on $D$, giving $D$ a ring structure. 

Define $A\to D$ by $a\mapsto f(a)\otimes 1$. Note that $f(a)\otimes 1=a\cdot 1_V\otimes 1_C=1_B\otimes a\cdot 1_C=1\otimes g(a)$. It is easy to see it is a homomorphism of rings. 

**Remark.** 
- [[Pasted image 20250324205212.png|page 31]] of [[Atiyah - 1969 - Introduction to commutative algebra.pdf|Atiyah]] is not correct, as $\mathbb{Z}\to \mathbb{Z}\otimes \mathbb{Z}$ is not a ring homomorphism.
- In fact there is a commutative diagram of ring homomorphism
  
  ![Pasted image 20250324222015.png|160](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250324222015.png)

**Example (strange $\otimes$).** Define $D=\mathbb{Q}(i)\otimes_\mathbb{Q} \mathbb{Q}(i)$ is not a domain, because 

$$(1\otimes i+i\otimes 1)(1\otimes i-i\otimes 1)=1\otimes(-1)-(-1)\otimes 1=0.$$

To see the above two elements are nonzero, notice that $D=(\mathbb{Q}1\oplus\mathbb{Q} i)\otimes (\mathbb{Q}1\oplus \mathbb{Q}i)$ is a vector space over $\mathbb{Q}$ and 

$$\begin{aligned}
D&=(\mathbb{Q}1\oplus\mathbb{Q} i)\otimes (\mathbb{Q}1\oplus \mathbb{Q}i)\\&=\mathbb{Q}1\otimes \mathbb{Q}1\oplus \mathbb{Q} i\otimes \mathbb{Q}1\oplus\mathbb{Q}1\otimes \mathbb{Q}i\oplus\mathbb{Q}i\otimes \mathbb{Q}i\\
&\simeq \mathbb{Q}\oplus \mathbb{Q}\oplus \mathbb{Q}\oplus \mathbb{Q}
\end{aligned}$$

where $\mathbb{Q}1\otimes_\mathbb{Q}\mathbb{Q}1\simeq \mathbb{Q}\otimes _\mathbb{Q} \mathbb{Q}=\mathbb{Q}$. Hence $D$ is a $4$-dimensional $\mathbb{Q}$-v.s. with a basis $1\otimes 1,1\otimes i,i\otimes 1,i\otimes i$. So the above two elements are nonzero. 

**Examples.**
- $\mathbb{C}[x]\otimes \mathbb{C}[y]\simeq \mathbb{C}[x,y]$. Each element on LHS has a unique expression as $\mathbb{C}[x],\mathbb{C}[y]$ are linear vector spaces, then $\varphi:\sum a_{ij}x^i\otimes y^j\mapsto \sum a_{ij}x^iy^j$ is well-defined. 
- $\mathbb{C}[\![x]\!]\otimes_\mathbb{C} \mathbb{C}[\![y]\!]\neq \mathbb{C}[\![x,y]\!]$. The problem is, $\{x^n:n\geqslant 0\}$ is NOT a basis of $\mathbb{C}[\![x]\!]$. "For example", consider $f=\sum_{i=0}^n (xy)^i$ and $\sum_{i=0}^n x^i\otimes y^i\notin\text{LHS}$. 


> [!proposition]
> Let $\alpha\subseteq A$ be an ideal, and let $M$ be an $A$-module. Then $M/\alpha M\simeq (A/\alpha)\otimes_A M$. 

**_Proof._**
Consider short exact sequence $0\to\alpha\to A\to A/\alpha\to 0$. Tensor with $M$ and we get a right exact sequence 

$$\alpha\otimes_A M\stackrel{f }{\to}M\to A/\alpha\otimes M\to 0.$$

Recall the notation $\alpha M=\{\sum_{i=1}^N a_i m_i:a_i\in \alpha,m_i\in M\}\subseteq M$. It is [[MATH/交换代数/Nodes/HW5#^uvuyea\|easy]] to see $\mathrm{im} f=\alpha M$ (remark that in general $\alpha\otimes M\to \alpha M$ is not injective). So we get a short exact sequence $0\to \alpha M\hookrightarrow M\to A/\alpha\otimes _A M\to 0$. So $M/\alpha M\simeq (A/\alpha)\otimes_A M$. 
<p align="right">□</p>


**Remark.** This is an example where $\alpha\otimes M\to \alpha M$ is not injective. Let $\alpha=(2)\subseteq \mathbb{Z}$, and let $M=\mathbb{Z}/2\mathbb{Z}$. Then $0\neq (2\mathbb{Z})\otimes _\mathbb{Z} \mathbb{Z}/2\mathbb{Z}$ and $(2)\cdot \mathbb{Z}/2\mathbb{Z}=0$. 


> [!lemma] a useful fact
> Let $\alpha\subseteq A$ be an ideal. Let $M,N$ be two $A/\alpha$-modules, then one have an $A$-module isomorphism 
> 
> $$M\otimes _{A/\alpha} N\simeq M\otimes _AN.$$

**Remark.** For general $A\to B$ and two $B$-modules $X$ and $Y$, $X\otimes_B Y\not\simeq X\otimes_A Y$. 

**_Proof._**
Consider

![Pasted image 20250331173925.png|220](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250331173925.png)

Define $g_A:M\times N\to M\otimes _A N,(m,n)\mapsto m\otimes_A n$, then $g_A$ is $A/\alpha$-bilinear and there exists $f'':M\otimes_{A/\alpha}N\to M\otimes _AN$ such that $f''\circ g_{A}=g_{A/\alpha}$. Similarly, define $g_{A/\alpha}:M\times N\to M\otimes_{A/\alpha}N,(m,n)\mapsto m\otimes_{A/\alpha}n$, then $g_{A/\alpha}$ is $A$-bilinear and there exists $f':M\otimes _{A/\alpha}N\to M\otimes_A N$ such that $f'\circ g_{A/\alpha}=g_{A}$. So $f'=f''^{-1}$ and so $M\otimes_{A/\alpha}N\simeq M\otimes _A N$. 
<p align="right">□</p>

