---
{"dg-publish":true,"draft":false,"permalink":"/MATH/交换代数/Nodes/9 DVR & Dedekind Domain/","dgPassFrontmatter":true}
---


> [!definition]
> Let $k$ be a field. A discrete valuation on $k$ is a map $\nu:k^*\to \mathbb{Z}$ such that 
> - $\nu(xy)=\nu(x)+\nu(y)$;
> - $\nu(x+y)\geqslant\min\{\nu(x),\nu(y)\}$ (non-Archimedean valuation)
> 
> (Sometimes define $\nu(0)=+\infty$.)

> [!definition]
> Let $R=\{x\in k:\nu(x)\geqslant 0\}$ which contains $0$, then $R$ is a ring, which is called the valuation ring of $\nu$. It is a local ring with $m_R=\{x\in R:r(x)\geqslant 1\}$. 

**_Proof._**
It is trivial to show $R$ is a ring. To see it is local with the unique maximal ideal $m_R$, it suffices to check $x\in R\setminus m_R$ is a unit. But in this case $\nu(x)=0$ iff $\nu(1/x)=\nu(1)-\nu(x)=0$ and so $1/x\in R$. 
<p align="left">□</p>


**Remark.** Given a valuation as above, one can check $||x||=\epsilon^{\nu(x)}$ with $0<\epsilon<1$ a fixed element defines a norm in $k$. That is to say, $d(x,y)=|||x-y||=\epsilon^{\nu(x-y)}$ is a distance. To show it, it suffices to show it satisfies the triangle inequality.

> [!NOTE] “在这个世界里，所有的三角形都是等腰三角形。” 
> 
> See [[MATH/抽象代数III/Nodes/HW9#^lchh7e\|here]]. 

**Examples.**
- $p$-adic valuation on $\mathbb{Q}$. 
	- Fix a prime $p$, let $x=a/b\in \mathbb{Q}$ with $(a,b)=1$. Define 
	  
	  $$\nu_p(x)=\begin{cases}i,&\text{if }a=p^i\cdot a',\\-j,&\text{if }b=p^j\cdot b'.\end{cases}$$
	  
	- To see it is a valuation, it suffices to check $\nu_p(a/b+c/d)\geqslant\min\{\nu_p(a/b),\nu_p(c/d)\}$. 
		- Suppose $p\not\mid b$ and $p\not\mid d$, then 
		  $$\nu_p(a/b+c/d)=\nu_p((ad+bc)/bd)=\nu_p(ad+bc)\geqslant\min\{\nu_p(a),\nu_p(c)\}.$$
		  
		- For general case, multiply $p^n$ to $a/b$ and $c/d$ for a large enough $n$. Then we get back to the first case. 
	- For $\nu_p$ on $\mathbb{Q}$, the valuation ring is $\dfrac{\mathbb{Z}}{\mathbb{Z}\setminus p\mathbb{Z}}=\mathbb{Z}_{(p)}$, whose unique maximal ideal is $p\mathbb{Z}_{(p)}$ and residue field is $\mathbb{Z}_{(p)}/p\mathbb{Z}_{(p)}\simeq \mathbb{F}_p$. 
- $k=k(x)=\mathrm{Frac} (k[x])$ is a field. 
	- Take an irreducible polynomial $r(x)\in k[x]$. Then we define $\nu(f(x)/g(x))=\nu(f(x))-\nu(g(x))$. For $f(x)=r(x)^a\prod_{i=1}^n r_i(x)$, let $\nu(f(x))=a$. 
	- It is valuation, similar to $\nu_p$ on $\mathbb{Q}$. 

**Remark.** 这个和ED不一样，那个只是一个norm？

> [!definition]
> We say an integral is a DVR (discrete valuation ring) if there exists a discrete valuation $\mathrm{Frac} A\stackrel{\nu}{\twoheadrightarrow} \mathbb{Z}$ such that $A$ us a valuation ring. 

**Fact.** DVR is a PID. 
- Since $\mathrm{Frac} A\stackrel{\nu}{\twoheadrightarrow} \mathbb{Z}$ is surjective, there exists $x\in \mathrm{Frac}A$ such that $\nu(x)=1$ (such $x$ is called a uniformizer). 
- Claim 1: $m_k=(x)$. Indeed, given any $y\in m_k$, notice that $y\in m_k$ iff $\nu(y)\geqslant 1$. Then $\nu(y/x)\geqslant 1-1\geqslant 0$ and $y/x\in A$. Thus $y\in (x)$ and $m_k\subseteq (x)$ yield $m_k=(x)$. 
- Claim 2: given any ideal $I\subseteq A$, $I=(x^k)$ for some $k\geqslant 0$. 
	- Let $k=\min\{\nu(z):z\in I\}$. There exists $y\in I$ such that $\nu(y)=k$. then




<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/math/iii/nodes/8-250415/#bb0319" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



> [!theorem]
> Let $(k,\nu)$ be a discrete normalized valuation field. Let $R$ be its valuation ring, and let $P$ be its valuation ideal. 
> - Let $\pi\in R$ with $\nu(\pi)=1$. Then any $\alpha\in k$ is expressed as $\alpha=\pi^i u$ where $i=\nu(\alpha)$, $u\in R\setminus P$. 
> - Any nonzero ideal of $R$ is of the form $p^i=(\pi^i)$ for some $i\geqslant 0$. In particular, $R$ is a $PID$. 
> - $R$ is integral closed. 

</div></div>
