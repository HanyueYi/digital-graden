---
{"dg-publish":true,"permalink":"/MATH/交换代数/Nodes/8 Artinian Rings/","dgPassFrontmatter":true}
---


> [!definition]
> We say $A$ is an Artinian ring if it satisfies d.c.c. for ideals.

**Examples.**
- field
- $k[x]/(x^2)$ (it has only $3$ ideals)
- $k[x,y]/(xy)$ is not Artinian, because $(xy,y^2)\supseteq (xy,y^3)\supseteq\cdots$ is not d.c.c.


> [!proposition]
> Let $A$ be an Artinian ring. Then each prime ideal is maximal. 
{ #fsei3o}


**_Proof._**
Let $p\subseteq A$ be an prime ideal. Then $B=A/p$ is an Artinian integral domain. We claim that $B$ is a field. 

Let $x\in B$ with $x\neq 0$. Then $(x)\supseteq (x^2)\supseteq\cdots$ terminates. Then $x^n=x^{n+1}y$ for some $y\in B$ and so $xy=1$ by $B$ integral domain. 

Therefore, $p$ is maximal, by $A/p$ being a field. 
□


> [!corollary]
> Let $A$ be an Artinian ring. Then $\mathrm{Nil}(A)=\mathrm{Jac}(A)$. 

> [!proposition]
> If $A$ is an Artinian ring, then it has finitely many maximal ideals. 
{ #steden}


**_Proof._**
Let $S=\{m_1\cap\cdots\cap m_r:m_i\text{ is maximal}\}$ be the set of finite intersections of maximal ideals. By d.c.c. $S$ has a minimal element, denoted by $m_1\cap\cdots\cap m_n$. Now let $m\subseteq A$ be a maximal ideal. Then $m\cap(\cap_{i=1}^n m_i)=\cap_{i=1}^n m_i$ and so $m\supseteq \cap_{i=1}^n m_i$. By [[MATH/交换代数/Nodes/1 Rings and Ideals#^tepoo1\|1 Rings and Ideals#^tepoo1]], $m\supseteq m_i$ for some $i$ and so $m=m_i$. So $\mathrm{Spec}(A)=\{m_1,\cdots,m_n\}$. 
□


> [!proposition]
> If $A$ is an Artinian ring, then $N=\mathrm{Nil}(A)$ is nilpotent. 
{ #eii4v9}


**_Proof._**
By d.c.c, the chain $N\supseteq N^2\supseteq\cdots$ terminates and so $\alpha=N^k=N^{k+1}=\cdots$. We aim to show $\alpha=(0)$. 

If $\alpha\neq 0$, define $\Sigma=\{\beta\subseteq A:\beta\text{ is an ideal, }\alpha\beta\neq 0\}$. Since $A\in \Sigma$, the ideal $\Sigma\neq 0$ and so it has a minimal element $c$. Since $c\alpha\neq 0$, there exists $x\in c$ such that $x\alpha\neq 0$. It deduces that $(x)\in \Sigma$ and $c=(x)$ by minimality. 

Note that $x\alpha\neq 0$ yields $(x\alpha)\alpha=x\alpha\neq 0$ and $x\alpha\in \sigma$. By minimality, $x\alpha=(x)$ and $x=xy$ for some $y\in \alpha=N^k$. Now 

$$x=xy=xy^2=\cdots=xy^n=0$$

for some $n$, which contradicts with $(x)\in \Sigma$. 
□


> [!definition]
> A chain of prime ideals is $p_0\subset p_1\subset\cdots\subset p_n\subset\cdots$. Its length is the number of jumps. Define the (Krull-)dimension of $A$ to be the maximal length of chaim of prime ideal. 

**Examples.** 我觉得我完全没学会怎么算这玩意
- For a field $k$, $\dim k=0$. 
- $(0)\subseteq (p)$ is the longest prime chain of $\mathbb{Z}$, so $\dim \mathbb{Z}=1$. 
- In $\mathbb{C}[x]$, one have $(0)\subseteq (x-a)$ and so $\dim \mathbb{C}[x]=1$. Remark that Every non-zero prime ideal in a Principal Ideal Domain (PID) is a maximal ideal.
- In $\mathbb{C}[x]/(x^2)$, $(\overline x)$ is the unique prime ideal and so $\dim \mathbb{C}[x]/(x^2)=0$. 
- Chain of prime ideal of $\mathbb{C}[x,y]/(xy)$ is $\overline{(x)}=\overline{(x,xy)}\subseteq \overline{(x,y-a)}$ and $\dim \mathbb{C}[x,y]/(xy)=1$. 
- $\dim(A\times B)=\max\{\dim A,\dim B\}$. Recall that $\mathrm{Spec}(A\times B)=\mathrm{Spec}(A)\sqcup \mathrm{Spec}(B)$. 
- $\dim(\mathbb{C}[x,y])=2$ (not easy) (he said it use [[MATH/代数几何/Nodes/1.1 Some Algebra#^d13b03\|1.1 Some Algebra#^d13b03]])


> [!theorem]
> $A$ is Artinian iff $A$ is Noetherian and $\dim A=0$.
{ #myy86x}


**_Proof._**
Recall that if $(0)=m_1\cdots m_n$ is a product of some maximal ideals, then $A$ Noetherian iff $A$ Artinian by [[MATH/交换代数/Nodes/6 Chain Condition#^3gn38j\|6 Chain Condition#^3gn38j]]. 

"->" By [[MATH/交换代数/Nodes/8 Artinian Rings#^fsei3o\|#^fsei3o]], one have $\dim A=0$. By [[MATH/交换代数/Nodes/8 Artinian Rings#^eii4v9\|#^eii4v9]], $N^k=0$ for some $k$. By [[MATH/交换代数/Nodes/8 Artinian Rings#^steden\|#^steden]], $N$ is the intersection of all prime ideals, which is a finite intersection. It deduces that $(m_1\cdots m_k)^k\subseteq \cap_{i=1}^n m_i^k=(0)$, verifying assumption of [[MATH/交换代数/Nodes/6 Chain Condition#^3gn38j\|6 Chain Condition#^3gn38j]]. 


"<-" By [[MATH/交换代数/Nodes/7 Noetherian Rings#^k8wbyb\|7 Noetherian Rings#^k8wbyb]], $(0)=\cap_{i=1}^n q_i$ with distinct $r(q_i)=p_i$. Since $\dim A=0$, we have $p_i$ are maximal ideals. It deduces that $\mathrm{Nil}(A)=r((0))=\cap _{i=1}^n p_i$. Since $A$ is Noetherian, $N$ is nilpotent. Then $(0)=N^k\supseteq (p_1\cdots p_n)^k$ verifying assumption of [[MATH/交换代数/Nodes/6 Chain Condition#^3gn38j\|6 Chain Condition#^3gn38j]]. 
□


**Example.** Note that $\prod_{i=1}^\infty k$ is dimension $0$ but not Artinian. 

> [!proposition]
> If $A$ is a Noetherian ring and $m$ is a maximal ideal, then exactly one of following is true. 
> - $m^n\neq m^{n+1}$ for all $n\geqslant 0$;
> - $m^n=0$ for some $n\geqslant 0$ in which case $A$ is Artinian. 

**_Proof._**
If i) does not hold, then $m^n=m^{n+1}$. By [[MATH/交换代数/Nodes/2 Modules#^mzvcc5\|Nakayama lemma]], $m^n=0$. By [[MATH/交换代数/Nodes/6 Chain Condition#^3gn38j\|6 Chain Condition#^3gn38j]], $A$ is Artinian. 
□

> [!theorem]
> $A$ is Artinian if $A=\prod_{i=1}^n A_i$ is a finite product of Artinian local rings. 

**_Proof._**
"<-" Each $A_i$ is Noetherian and dimension $0$. Then by [[MATH/交换代数/Nodes/8 Artinian Rings#^myy86x\|#^myy86x]], $A$ is also Noetherian and dimension $0$. It deduces that $A$ is Artinian. 

"->" By [[MATH/交换代数/Nodes/8 Artinian Rings#^steden\|#^steden]], $A$ has finitely many maximal ideals $m_1,\cdots,m_n$. By proof of [[MATH/交换代数/Nodes/8 Artinian Rings#^myy86x\|#^myy86x]], we have $(m_1\cdots m_n)^k=0$. 

Note that $\{m_i\}_{i=1}^n$ are pairwise coprime, so $\{m_i^k\}$ are also coprime 

![Pasted image 20250421203354.png](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250421203354.png)

□


- [ ] Now given （最后一行

![Pasted image 20250421204722.png](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250421204722.png)


> [!proposition]
> Suppose $(A,m)$ is Artinian local. Then TFAE:
> - all ideals of $A$ are principal;
> - $m$ is principal;
> - $\dim_k m/m^2\leqslant 1$.

**_Proof._**
i)->ii) Obvious. 

ii)->iii) $m=(x)$ yields $m/m^2=k\cdot \overline x$. Then $\dim_k m/m^2\leqslant 1$. 

iii)->i) $\dim_k m/m^2\leqslant 1$ yields that there exists $x\in m$ such that $\overline x\in m/m^2$ generate $m/m^2$ as a $k$-vector space. 

Note that [[MATH/交换代数/Nodes/2 Modules#^w0idub\|2 Modules#^w0idub]] yields that $m=(x)$. Let $\alpha\subseteq A$ be a proper ideal. Since $\mathrm{Nil}(A)=m$, we have $m^k=0$ for a big enough $k$ by [[MATH/交换代数/Nodes/8 Artinian Rings#^eii4v9\|#^eii4v9]]. It deduces that $m^k\subseteq \alpha\subseteq m$.

So there exists $r$ such that $\alpha\subseteq m^r=(x^r)$ but $\alpha\not\subseteq m^{r+1}=(x^{r+1})$. Then there is $y\in \alpha$ such that $y\notin (x^{r+1})$. But $y\in (x^r)$ yields $y=x^ra$. It deduces $a\notin (x)=m$ and $a$ is a unit. Thus $\alpha\supseteq(y)=(x^r)\supseteq \alpha$ and so $\alpha=(x^r)$ is principal.
□

