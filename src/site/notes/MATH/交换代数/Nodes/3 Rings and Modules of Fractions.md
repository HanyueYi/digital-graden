---
{"dg-publish":true,"permalink":"/MATH/交换代数/Nodes/3 Rings and Modules of Fractions/","dgPassFrontmatter":true}
---


> [!definition]
> Let $A$ be a ring. We say a subset $S\subseteq A$ is multiplicatively closed if $1\in S$ and $S$ is closed under multiplication. 


> [!definition]
> For multiplication closed $S\subseteq A$, define a relation $\equiv$ on $A\times S$, where $(a,s)\equiv (b,t)$ iff $(at-bs)u=0$ for some non-zero $u\in S$. 
> 
> We claim that $\equiv$ is an equivalent relation. It suffices to check transitivity. Suppose $(a,s)\equiv (b,t)$ and $(b,t)\equiv (c,u)$, then $(at-bs)v=(bu-ct)w=0$ for some $v,w\in S$. Notice that $(au-cs)tvw=atvuw-ctwsv=bsvuw-buwsv=0$ and we have done.


> [!definition]
> Let $a/s$ be the equivalent class of $(a,s)$. Let $S^{-1}A$ be the set of equivalent classes, that is, $S^{-1}A:=A\times S/\sim$. One can define a ring structure by $a/s+b/t=(at+bs)/st$ and $a/s\cdot b/t=ab/st$. We call $S^{-1}A$ *the ring of fractions* of $A$ w.r.t. $S$.  

**Remark.** We need to check the computation is well-defined. See [[Pasted image 20250331195545.png|here]]. 

**Fact.** We have a map $A\to S^{-1}A:a\mapsto a/1$. It is NOT necessarily injective. For example, if $0\in S$, then $S^{-1}A=0$. e.g. $A=\mathbb{Z}$ and $S=\{0,1\}$. 


> [!example] important
> Let $I\subseteq A$ be an ideal. Easy fact: $I$ is prime iff $A-I$ is multiplication closed. (if $a,b\notin I$, then $ab\notin I$)
> 
> In this case for $S=A-p$, denote $S^{-1}A$ be $A_p$, and call it the *localization* of $A$ at $p$. 
> 
> Fact: $A_p$ is a local ring. Indeed, consider $m=\{a/s:a\in p\}\subseteq A_p$, which is an ideal. For any $b/t\notin m$, $b\in A-p$ and $t/b\in A_p$ and so $b/t\in (A_p)^\times$. By [[MATH/交换代数/Nodes/1 Rings and Ideals#^ysw57c\|1 Rings and Ideals#^ysw57c]], $m$ is the unique maximal ideal. 
> 
> Fact: $A_p/m\simeq \mathrm{Frac}(A/p)$. Prove later. 


> [!example] also important
> Let $f\in A$. Let $S=\{1,f,\cdots,f^n,\cdots\}$. Then denote $S^{-1}A$ by $A_f$. Note that if $0\in S$, $S^{-1}A=0$. 
> 
> - $A=\mathbb{Z}$, $f=p$, $S=\{p^n\}_{n\geqslant 0}$. $S^{-1}A=\{a/p^n\}_{n\geqslant 0,a\in \mathbb{Z}}$. Here we do not use $\mathbb{Z}_p$ here. 
> - $A=\mathbb{Z}$, $S=\mathbb{Z}-(p)$, then get $\mathbb{Z}_{(p)}=\{a/b:(b,p)=1\}$. 

> [!proposition]
> Let $S$ be a multiplicative closed set, and let $g:A\to B$ be a ring homomorphism such that $g(s)\in B^\times$ for all $s\in S$. Then there exists unique $h$ such that 
> 
> ![Pasted image 20250331202034.png|180](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250331202034.png)
> 
> is commute.

**_Proof._**
Define $h(a/s)=g(a)/g(s)\in B$. We only check it is well-defined. If $a/s=a'/s'$, we aim to show $g(a)/g(s)=g(a')/g(s')$. Since $(as'-a's)t=0$ for some $t\in S$, one have $(g(as')-g(a's))g(t)=0$. Thus $g(as')=g(a's)$ by $g(t)\in B^\times$. 
<p align="left">□</p>


> [!definition]
> Let $M$ be an $A$-module. For a multiplicative closed set $S$, define relation on $M\times S$, 
> 
> $$(m,s)=(m',s') \iff \exists t\in S, t(sm'-s'm)=0$$
> 
> which is an equivalent relation. Define $S^{-1}M=\{m/s:m\in M,s\in M\}$ as the set of equivalent classes. 

**Fact.** $S^{-1}M$ is an $S^{-1}A$-module via $a/s\cdot m/t=am/st$. Also there is a $A$-module homomorphism $M\to S^{-1}M,m\mapsto m/1$. 

**Notation.** If $S=A-p$, denote $M_p$; if $S=\{f^n:n\geqslant 0\}$, denote $M_f$. 

**Easy Fact.** $u:M\to N$ is an $A$-module homomorphism induces an $S^{-1}A$-module homomorphism. $S^{-1}u:S^{-1}M\to S^{-1}N,m/s\to u(m)/s$. 

> [!proposition]
> The operation $S^{-1}$ is exact on $A$-modules. That is, if $M'\stackrel{f}{\to} M\stackrel{g}{\to}M''$ is a exact sequence of $A$-module, then $S^{-1}M'\stackrel{S^{-1}f}{\to} S^{-1}M\stackrel{S^{-1}g}{\to}S^{-1}M''$ is also exact.
{ #092787}


**_Proof._**
We aim to show $\mathrm{im}(S^{-1}f)=\ker (S^{-1}g)$. Since $(S^{-1}g)\circ(S^{-1}f)=S^{-1}(g\circ f)=0$, one have $\mathrm{im}(S^{-1}f)\subseteq\ker(S^{-1}g)$. 

On the other hand, suppose $m/s\in\ker (S^{-1}g)$, then $g(m)/s=0/1$ in $S^{-1}M''$. It deduces that $g(m)t=0$ for some $t\in S$ and so $g(tm)=0$, $tm\in \ker g=\mathrm{im} f$. Assume that $tm=f(m')$ for some $m'\in M'$. So $m/s=tm/ts=f(m')/ts\in\mathrm{im}(S^{-1}f)$. 
<p align="left">□</p>


> [!proposition]
> There exists unique $S^{-1}A$-module isomorphism 
> 
> $$f:S^{-1}A\otimes_A M\simeq S^{-1}M,a/s\otimes m\mapsto am/s.$$
> 
>
{ #d61f0b}


**_Proof._**
Consider $S^{-1}A\times M\to S^{-1}M$ by $(a/s,m)\mapsto am/s$. It is clearly $A$-bilinear, so there exists a unique map $f:S^{-1}A\otimes _A M\to S^{-1}M$. It is easy to check $f$ is $S^{-1}A$-linear and surjective. 

To show $f$ injective, let $f(x)=0$. Note that $x=\sum_{i=1}^n a_i/s_i\otimes m_i=1/(s_1\cdots s_n)\otimes m$ for some $m$. It deduces that $f(x)=f((1/s)\otimes m)=m/s=0$. Then there exists $t\in S$ such that $tm=0$ and so $x=(1/s)\otimes m=(1/st)\otimes (tm)=0$. 
<p align="left">□</p>


> [!corollary]
> $S^{-1}A$ is a flat $A$-module.
{ #8p663h}


**_Proof._**
By [[MATH/交换代数/Nodes/3 Rings and Modules of Fractions#^092787\|#^092787]] and [[MATH/交换代数/Nodes/3 Rings and Modules of Fractions#^d61f0b\|#^d61f0b]].
<p align="left">□</p>


> [!proposition]
> Let $M,N$ be $A$-modules. Then $S^{-1}M\otimes_{S^{-1}A}S^{-1}N\simeq S^{-1}(M\otimes_A N)$. 
{ #udklm4}


**_Proof._**
By [[MATH/交换代数/Nodes/3 Rings and Modules of Fractions#^d61f0b\|#^d61f0b]], we have 

$$\begin{aligned}
S^{-1}M\otimes_{S^{-1}A} S^{-1}N&\simeq (M\otimes_A S^{-1}A)\otimes_{S^{-1}A}(N\otimes_A S^{-1}A)\\&=M\otimes _A N\otimes _AS^{-1}A\\
&=(M\otimes _AN)\otimes_A S^{-1}A\\&=S^{-1}(M\otimes _A N)
\end{aligned}$$

and we finish the proof.
<p align="left">□</p>


**Example.** $M_p\otimes_{A_p}N_p=(M\otimes_A N)_p$. 

# Local Properties

> [!definition]
> A property $P$ of a ring $A$ (or of an $A$-module $M$) is said to be a "local property", if $A$ (or $M$) has $P$ $\iff$ $A_p$ (or $M_p$) has $P$ for any $p\in \mathrm{Spec} A$.

> [!proposition]
> Let $M$ be a $A$-module. TFAE:
> - $M=0$;
> - $M_p=0$ for all prime ideal $p$;
> - $M_m=0$ for all maximal ideal $m$.
{ #663ccb}


**_Proof._**
i)->ii)->iii) is trivial. 

iii)->i) If $M\neq 0$, take nonzero $x\in M$ and then $\mathrm{Ann}(x)\subseteq A$ is a proper ideal and $\mathrm{Ann}(x)\subseteq m$ for some maximal ideal $m$. 

Consider $M\to M_m=M\otimes_A (A-m)^{-1}A,x\mapsto x\otimes 1$. Since $M_m=0$, $x/1=0$. Then there exists $t\in A-m$ such that $tx=0$ and so $t\in \mathrm{Ann}(x)\subseteq m$, contradicting with $t\notin m$. 
<p align="left">□</p>


> [!proposition]
> Let $\phi:M\to N$ be a homomorphism between $A$-modules. TFAE:
> - $\phi$ is injective;
> - $\phi_p:M_p\to N_p$ is injective for all prime ideal $p$;
> - $\phi_m:M_m\to N_m$ is injective for all maximal ideal $m$.
> 
> Similar statements hold after replacing "injective" by "surjective" or "bijective".
{ #766550}


**_Proof._**
i)->ii) Recall $M_p\simeq M\otimes_A A_p$ and by [[MATH/交换代数/Nodes/3 Rings and Modules of Fractions#^8p663h\|#^8p663h]].

ii)->iii) Trivial. 

iii)->i) Let $P=\ker \phi$. Then $0\to P\to M\to N$ is left exact. For any maximal ideal $m$, $A_m$ is flat $A$-module yields that $0\to P_m\to M_n\to N_n$ is left exact. It deduces that $P_m=0$ and so $P=0$ by [[MATH/交换代数/Nodes/3 Rings and Modules of Fractions#^663ccb\|#^663ccb]]. 
<p align="left">□</p>


> [!proposition]
> Let $M$ be an $A$-module. TFAE:
> - $M$ is a flat $A$-module;
> - $M_p$ is a flat $A_p$-module for all prime ideal $p$;
> - $M_m$ is a flat $A_m$-module for all maximal ideal $m$. 

**_Proof._**
i)->ii) Given injective homomorphism $X\hookrightarrow Y$ of $A_p$-module, we aim to show $X\otimes_{A_p}M_p\to Y\otimes_{A_p}M_p$ is injective. Note that $X\otimes_{A_p} M_p=X\otimes_{A_p}(A_p\otimes_A M)=X\otimes _A M$ and $X\otimes _A M\to Y\otimes_A M$ is injective. Now we finish the proof. 

ii)->iii) is trivial. 

iii)->i) Suppose $N\hookrightarrow P$ is an injective homomorphism of $A$-modules. By [[MATH/交换代数/Nodes/3 Rings and Modules of Fractions#^766550\|#^766550]], it suffices to check injective after localization at any maximal ideal $m$. By [[MATH/交换代数/Nodes/3 Rings and Modules of Fractions#^udklm4\|#^udklm4]], it is same as $N_m\otimes_{A_m} M_m\to P_m\otimes_{A_m}M_m$, which is injective by iii).
<p align="left">□</p>


# Extended and Contracted Ideals in $S^{-1}A$

Let $f:A\to S^{-1}A,a\mapsto a/1$. Let $C$ be the set of contracted ideals in $A$, that is, 

$$C=\{f^{-1}(\beta)=\beta^c:\beta\subseteq S^{-1}A\text{ is an ideal}\}.$$

Let $E$ be the set of extended ideals in $S^{-1}A$, that is, 

$$E=\{\alpha^e=\left\langle \alpha\right\rangle _{S^{-1}A}:\alpha\subseteq A\text{ is an ideal}\}.$$

**Fact.** $\alpha^e=S^{-1}\alpha=\alpha\otimes_A S^{-1}A$. 


> [!proposition]
> Part 1:
> - If $\beta\subseteq S^{-1}A$ is an ideal, then $\beta=(\beta^c)^e$, that is, $\beta$ is an extended ideal.
> - Let $\alpha\subseteq A$ be an ideal, then $\alpha^{ec}=\cup_{s\in S}(\alpha:s)$. Also $\alpha^e=S^{-1}A$ iff $\alpha^{ec}=A$ iff $\alpha\cap S\neq \emptyset$. Recall that $(\alpha:s)=\{x\in A:xs\in \alpha\}$.
> - If $C$ is the set of contracted ideals in $A$, then $\alpha\in C$ iff $\forall s\in S$, $s$ is not zero divisor in $A/\alpha$ iff $(\alpha:s)=\alpha$ for all $s\in S$. 
> 
> Part 2:
> - $P\to S^{-1}P$ gives a $1$-$1$ correspondence between 
>   
>   $$\{\text{prime ideals }p\subseteq A,p\cap S=\emptyset\}\leftrightarrow\{\text{prime ideals of }S^{-1}A\}.$$
>   
> - The operation $S^{-1}$ commutes with $+$, $\times$, $\cap$, radical.
{ #961e0a}


**_Proof._**
i) By definition, $\beta^{ce}\subseteq \beta$. On the other hand, for any $x/s\in\beta$, one have $x/1=s\cdot x/s\in \beta$ and $x\in\beta^c$. It deduces that $x/1\in \beta^{ce}$ and so $x/s=1/s\cdot x/1\in \beta^{ce}$. Now we finish the proof.

ii) Note that $x\in \alpha^{ec}=(S^{-1}\alpha)^c$ iff $x/1=a/s$ for some $a\in \alpha$ and $s\in S$ iff $(xs-a)t=0$ for some $t\in S$. It yields that $xst=at\in \alpha$ as $a\in \alpha$ and $x\in (\alpha:st)$. Thus, $\alpha^{ec}\subseteq \cup_{s\in S}(\alpha:s)$. Conversely, if $x\in (\alpha:s)$, then $sx=a\in \alpha$ and $x=a/s\in S^{-1}\alpha$ and so $x\in (\alpha^e)^c$. 

For the "iff" statement,
- $\alpha^{ec}=A$ iff $1\in \alpha^{ec}$ iff $1\in (\alpha:s)$ for some $s\in S$ iff $s\in \alpha$ for some $s\in S$ iff $\alpha\cap S\neq \emptyset$. 
- Also
	- $\alpha^e=S^{-1}A$ yields $(\alpha^e)^c=A$.
	- $\alpha^{ec}=A$ yields $(\alpha^{ec})^e=A^e=S^{-1}A$. Also note that $(\alpha^e)^{ce}=\alpha^e$ by i) and then $\alpha^e=S^{-1}A$.

iii) Recall that $\alpha\in C$ iff $\alpha=(\alpha^e)^c$, it is a HW. See [[MATH/交换代数/Nodes/HW1#^gec7z6\|Proposition 1.17]]. 

By ii), $\alpha^{ec}=\cup_{s\in S}(\alpha:s)$, where $(\alpha:s)\supseteq \alpha$. Hence $\alpha\in C$ iff $\alpha=\alpha^{ec}$ iff $(\alpha:s)=\alpha$ for all $s\in S$ iff $\forall s\in S$, $s$ is not zero divisor in $A/\alpha$. 

iv) **Step 1. For a given prime ideal $p$ with $p\cap S=\emptyset$, we show $S^{-1}p$ is prime.** Since $0\to p\to A\to A/p\to 0$ is exact, $0\to S^{-1}p\to S^{-1}A\to S^{-1}A/p\to 0$ is also exact by [[MATH/交换代数/Nodes/3 Rings and Modules of Fractions#^092787\|#^092787]] and [[MATH/交换代数/Nodes/3 Rings and Modules of Fractions#^d61f0b\|#^d61f0b]]. It deduces that $S^{-1}A/S^{-1}p\simeq S^{-1}A/(S^{-1}A\otimes_A p)\simeq S^{-1}A\otimes_A A/p$, and it suffices to show $S^{-1}(A/p)$ is an integral domain. 

It is easy to check $S^{-1}(A/p)\simeq \overline S^{-1}(A/p)$ where $\overline S=\mathrm{im}(S\to A/p)$. Note that $P\cap S=\emptyset$ yields that $0\notin \overline S$. Since $A/p$ is an integral domain and $\overline S$ is a subset without $0$, one have $\overline S^{-1} (A/p)\subseteq \mathrm{Frac}(A/p)$ and so $S^{-1}(A/p)$ is an integral domain.

**Step 2. We show the map $p\to S^{-1}p$ is injective map.** For any $s\in S$, $s$ is not a zero divisor of $A/p$ because $A/p$ is an integral domain and $S\cap p=\emptyset$. By iii), $p\in C$ and then $p^{ec}=p$ by [[MATH/交换代数/Nodes/HW1#^gec7z6\|Proposition 1.17]]. 

**Step 3. We show the above map is surjective.** That is, given a prime ideal $\subseteq S^{-1}A$, it is of form $S^{-1}p$. By i), for $q\subseteq S^{-1}A$ prime, then $q=q^{ce}$. So it suffices to show $q^c$ is prime in $A$. Recall that for a ring homomorphism $\theta:G\to H$ and prime ideal $\delta\subseteq H$, one have $\theta^{-1}(\delta)\subseteq G$ prime. Indeed, $\theta$ induces a map $\mathrm{Spec}H\to \mathrm{Spec} G$. Now $q^c=f^{-1}(q)$ for $f:A\to S^{-1}A$. Finally, note $q^c\cap S=\emptyset$, otherwise $S^{-1}(q^c)=q^{ce}=S^{-1}A$. 

v) This says 
- $S^{-1}M+S^{-1}N=S^{-1}(M+N)$ as $S^{-1}M=M\otimes S^{-1}A$ and so for $N,M+N$. 
- $S^{-1}(M\oplus N)=S^{-1}A\otimes_A(M\oplus N)$
- $S^{-1}(M\cap N)=S^{-1}M\cap S^{-1}N$, whose proof is as follows.
	- Note that $S^{-1}(M\cap N)=S^{-1}A\otimes _A(M\cap N)$ and $S^{-1}M\cap S^{-1}N=(S^{-1}A\otimes _A M)\cap (S^{-1}A\otimes _AN)$. 
	- Consider the left exact sequence $0\to M\cap N\stackrel{\iota}{\to} M\oplus N\stackrel{\varphi}{\to} P$ where $\iota(x)=(x,x)$ and $\varphi(m,n)=m-n$. 
	- Tensor with the flat $A$-module $S^{-1}A$, and there is a exact sequence
	  
	  $$0\to( M\cap N)\otimes_A S^{-1}A\stackrel{}{\to} (M\otimes _A S^{-1}A)\oplus (N\otimes_A S^{-1}A)\stackrel{}{\to} P\otimes_A S^{-1}A$$
	  
	  Then conclude. 
- To show $S^{-1}(r(I))=r(S^{-1}I)$:
	- For any given $x/s\in r(S^{-1}I)$, there is $(x/s)^n\in S^{-1}I$ for some $n$ and $x^n/s^n=i/t$ for some $i\in I$ and $t\in S$. Then $(uxt)^n\in I$, $uxt\in r(I)$ and $uxt/uts=x/s\in S^{-1}(r(I))$.
	- Conversely, for any given $x/s\in S^{-1}(r(I))$, $x^n\in I$ and $s\in S$, one have $x^n/s^n\in S^{-1}I$ and so $x/s\in r(S^{-1}I)$. 

Now we finish the proof. 
<p align="left">□</p>

**Remarks.** "Many fields."
- Let $p\subseteq A$ be a prime ideal. Then $A_p$ is a local ring, where $p^e=(A-p)^{-1}p$ is the unique maximal ideal. It deduces that $A_p/p^e$ is the residue field of $A_p$. In fact, $\mathrm{Frac}(A/p)\simeq A_p/p^e$.
	- RHS equals $(A-p)^{-1}A/(A-p)^{-1}p=A_p/p\otimes_A A_p=A_p\otimes_A A/p=(A-p)^{-1}(A/p)$
	- as argument in [[MATH/交换代数/Nodes/3 Rings and Modules of Fractions#^961e0a\|#^961e0a]] iv), it is isomorphic to $(\overline {A-p})^{-1}(A/p)=\mathrm{Frac}(A/p)$, where $\overline {A-p}=\mathrm{im}(A-p\to A/p)=A/p\setminus\{0\}$.
	- **Examples.**
		- $(p)\subseteq \mathbb{Z}$, $\mathbb{Z}_{(p)}=\mathbb{Z}/(\mathbb{Z}-p\mathbb{Z})$ and $\mathbb{Z}_{(p)}/p\mathbb{Z}_{(p)}\simeq \mathbb{F}_p=\mathrm{Frac}(\mathbb{Z}/p)$
		- $(0)\subseteq \mathbb{Z}$, $\mathbb{Z}_{(0)}=\mathbb{Q}$ and $\mathbb{Q}/(0)=\mathbb{Q}=\mathrm{Frac}(\mathbb{Z}/(0))$. 
		- $A=\mathbb{Z}[x]$, $p=(p)$ and $A_{(p)}=\mathbb{Z}[x]/(\mathbb{Z}[x]-p\mathbb{Z}[x])$. We have $A_{(p)}/pA(p)\simeq \mathbb{F}_p(x)$ and $\mathrm{Frac}(\mathbb{Z}[x]/(p))=\mathrm{Frac}(\mathbb{F}_p[x])=\mathbb{F}_p(x)$. 
- Even if $A$ is integral, $\mathrm{Frac}(A/p)$ in general is not $\mathrm{Frac}(A)$. 
- Let $A$ be an integral domain, and let $p\subseteq A$ be a prime ideal. Then $A_p=(A-p)^{-1}A\hookrightarrow\mathrm{Frac}(A)$ and so $A_p$ is an integral domain. 
	- In fact, $\mathrm{Frac}(A_p)=\mathrm{Frac}(A)$. 
		- Proof. $A\hookrightarrow A_p\hookrightarrow \mathrm{Frac}(A)$ is integral domain(?), which yields that $\mathrm{Frac}(A_p)=\mathrm{Frac}(A)$.
		- Example. $\mathrm{Frac}(\mathbb{Z}_{(p)})=\mathrm{Frac}(\mathbb{Z})=\mathbb{Q}$.


> [!proposition]
> Let $M$ be a finitely generated $A$-module. Then $S^{-1}(\mathrm{Ann}(M))=\mathrm{Ann}(S^{-1}M)(*)$. 

**_Proof._**
Let $\{m_1,\cdots,m_n\}$ be generators of $M$. For $(*)$, $\subseteq$ is obvious, because $a$ kills all $m\in M$ yields that $a/s$ kills $m/t$ for all $m/t\in S^{-1}M$. 

Now for $\supseteq$. For $0\neq a/s\in \mathrm{Ann}(S^{-1}M)$, we have $a/s\cdot m_i/1=0$ for all $i$. It deduces that $t_iam_i=0$ for some $t_i\in S$. Then $((\prod_{i=1}^n t_i)a)m_i=0$ for all $i$ and $a(\prod_{i=1}^n t_i)\in\mathrm{Ann}(M)$ is not zero. Therefore, $a/s=(a\prod t_i)/(s\prod t_i)\in S^{-1}(\mathrm{Ann}(M))$.
<p align="left">□</p>

> [!proposition]
> Let $A\to B$ be a ring homomorphism, and let $p\subseteq A$ be a prime ideal. Then $p$ is a contraction of a prime $q\subseteq B$ iff $p^{ec}=p$. Remark that even in this case, $p^e$ might not be prime. 
{ #7xys15}


**_Proof._**
"->" As $p=q^c$, we have $p^{ec}=(q^c)^{ec}=q^c=p$ by [[MATH/交换代数/Nodes/HW1#^gec7z6\|Proposition 1.17]]. 

"<-" Now suppose $p^{ec}=p$. Let $S=\mathrm{im}((A-p)\to B)$, which is multiplicatively closed in $B$. Consider 

$$A\stackrel{f}{\to}B\to S^{-1}B,p\mapsto p^e\mapsto S^{-1}p^e.$$

We claim that $p^e\cap S=\emptyset$. If $x\in p^e\cap S$, then $f^{-1}(x)\cap A-p\neq\emptyset$. But $f^{-1}(p^e)=p^{ec}=p$ by assumption, which is a contradiction. 

This implies $S^{-1}p^e\subseteq S^{-1}B$ is a proper ideal: Otherwise, $1/1=a/s$ where $a\in p^e$, and $1/1=a/s$ means $s'(s-a)=0$ and $s's=s'a\in S\cap p^e=\emptyset$.

Now there exists a maximal ideal of $S^{-1}B$ which containing $S^{-1}(p^e)$. By [[MATH/交换代数/Nodes/3 Rings and Modules of Fractions#^961e0a\|#^961e0a]], this maximal ideal is of form $S^{-1}m$ with $m\cap S=\emptyset$ and $m\subseteq B$ is prime. 

Claim that $m^c=p$. Indeed, $S^{-1}m\supseteq S^{-1}(p^e)$ yields $m\supseteq p^e$ and so $m^c\supseteq p^{ec}=p$. Since $m\cap S=\emptyset$, one have $f^{-1}(m\cap S)=\emptyset$, $m^c\cap (A-p)=\emptyset$ and $m^c\subseteq p$. Therefore, $m^c=p$. 
<p align="left">□</p>

> [!Remark]
> In [[MATH/交换代数/Nodes/3 Rings and Modules of Fractions#^961e0a\|#^961e0a]] (iv), the preimage of a maximal ideal in $S^{-1}A$ under the localization map is not necessarily maximal in $A$. For instance, consider the canonical map $A_p \to S^{-1}A_p$. The ideal $pA_p$ is the unique maximal ideal of $S^{-1}A_p$, but its preimage in $A$ is the prime ideal $p$, which may not be maximal.
> 
> Conversely, if $m\subseteq A$ is a maximal element in the set  $\{\mathfrak{p} \subseteq A :\mathfrak{p} \cap S = \emptyset\}$, then its extension $m^e \subseteq S^{-1}A$ is a maximal ideal. Indeed, suppose otherwise: there exists a prime ideal $q=n^e\in S^{-1}A$ such that $q \supsetneq m^e$. Then its contraction $n \supsetneq m$ in $A$ would contradict the maximality of $m$ in the set of primes disjoint from $S$.
> 
> In summary, in $1$-$1$ correspondence in [[MATH/交换代数/Nodes/3 Rings and Modules of Fractions#^961e0a\|#^961e0a]] (iv), 
> 
> $$\{\text{prime ideals of }p\subseteq A,p\cap S=\emptyset\}\leftrightarrow\{\text{prime ideals of }S^{-1}A\}.$$
> 
> this induces a $1$-$1$ map 
> 
> $$\{\text{maximal elements above}\}\leftrightarrow\{\text{maximal ideals in }S^{-1}A\}.$$
> 
> But a maximal element in LHS is not necessary a maximal ideal in $A$. 