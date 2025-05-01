---
{"dg-publish":true,"aliases":"Sylow theorems","draft":false,"permalink":"/MATH/Cards/Nodes/Sylow Theorems/","dgPassFrontmatter":true}
---


> [!theorem]
> For every prime factor $p$ with multiplicity $n$ of the order of a finite group $G$, there exists a Sylow $p$-subgroup of $G$, of order $p^n$.

> [!theorem]
> Given a finite group $G$ and a prime number $p$, all Sylow $p$-subgroups of $G$ are conjugate to each other.
{ #ueqhoc}


> [!theorem]
> Let $p$ be a prime factor with multiplicity $n$ of the order of a finite group $G$, so that $|G|=p^nm$ where $n>0$ and $(p,m)=1$. Let $n_p$ be the number of Sylow $p$-subgroups of $G$. Then the following hold:
> - $n_p$ divides $m$.
> - $n_p\equiv 1\mod p$.
> - $n_p=|G:N_G(P)|$, where $P$ is any Sylow $p$-subgroup of $G$.
{ #7zwgij}



# Some Corollary


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/math/ii/nodes/1-5-sylow-theorem/#ne0n10" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



> [!corollary]
> Let $H<G$ be a $p$-group. If $p\mid[G:H]$, then $N_G(H)\supsetneq H$.  

</div></div>



> [!corollary]
> Let $M$ be a maximal subgroup of a $p$-group $G$, then $|G:M|=p$ and $M\lhd G$. 
{ #qes1qo}


**_Proof._**
By [[MATH/抽象代数II/Nodes/1.5 Sylow Theorem#^ne0n10\|1.5 Sylow Theorem#^ne0n10]].
<p align="left">□</p>


> [!corollary]
> Let $G$ be a finite group and let $P\in\mathrm{Syl}_p(G)$. Consider $G$ acting on $\Omega=\{N_G(P)g:g\in G\}$, which induces a map $\varphi:G\to\mathrm{Sym}(\Omega)$, then $\varphi(P)$ on $\Omega$ has only one fixed point $N_G(P)$.
> 
> Assume that $\varphi(P)$ acting on $\Omega$ has $k$ orbits, then for any $x\in N_G(P)-C_G(P)$, the number of fixed points of $\varphi(x)$ is $\leqslant k$.
{ #x4xxhg}


**_Proof._**
i) If $N_G(P)xP=N_G(P)x$, then $P^x\leqslant N_G(P)$. Then $P^x=P$ and so $N_G(P)x=N_G(P)$.

ii) Otherwise, there exist two fixed points of $\varphi(x)$ $N_G(P)a$ and $N_G(P)b$ in the same orbit of $\varphi(P)$, and so there exists $p\in P$ such that $N_G(P)a\varphi(p)=N_G(P)b$. On the other hand, we have $N_G(P)a\varphi(x)=N_G(P)a$ and $N_G(P)b\varphi(x)=N_G(P)b$. It deduces that 

$$N_G(P)a\varphi(px)=N_G(P)b=N_G(P)a\varphi(p)=N_G(P)a\varphi(xp)$$

and so $[p,x]\in P$ fixes $N_G(P)a$. It deduces that $[p,x]=1$ for all $p\in P$ and $x\in C_G(P)$, which is impossible. 
<p align="left">□</p>


# Application

The key idea of the following propositions are similar:
- To show $G$ is (not) simple:
	- If $G$ has a subgroup $H$ of index $n$, then $G$ acting on $\{Hg:g\in G\}$ induces a normal subgroup $H_G\lhd G$ and $G/H_G\lesssim S_n$. If $G$ is simple, then $H_G=\{1\}$ and $G\lesssim S_n$. Thus, there is a lower bound of index of subgroups of $G$.
	- Since $n_p=[G:N_G(P)]$ has lower bounder, we can determine $n_p$.
	- If $n_p$ is large enough, the intersection of Sylow $p$-subgroups may not trivial. Let $A=P_i\cap P_j$ for example. Then consider the index/order of $C_G(A)$ or $N_G(A)$. 
	- [[MATH/Cards/Nodes/Sylow Theorems#^56a6de\|#^56a6de]] describes the order of intersection of two Sylow $p$-subgroups. 


> [!theorem]
> A simple group of order $60$ is isomorphic to $A_5$.
{ #24a4c2}


**_Proof._**
Assume that $H\leqslant G$ with $[G:H]=m$, then consider $G$ acting on $\Omega=\{Hg:g\in G\}$. There exists $H_G\lhd G$ such that $G/H_G\lesssim S_m$. If $m\leqslant 4$, then $H_G\neq 1$ and $G$ is not simple, which is impossible. Therefore, $G$ does not has subgroups of index $\leqslant 4$. We claim that $G$ has a subgroup of index $5$. If it holds, then $G/H_G\lesssim S_5$ with $H_G=\{1\}$, i.e., $G$ is a subgroup of $S_5$. Since $S_5$ has only one subgroup of order $60$, we have $G\simeq A_5$. 

Now we prove the claim. [[MATH/Cards/Nodes/Sylow Theorems#^7zwgij\|Recall]] that $n_p=|G:N_G(P)|$, we have $n_p\geqslant 5$ for any $p\in\{2,3,5\}$. It deduces that $n_3=10$, $n_2\in\{5,15\}$ and $n_5=6$. 
- If $n_2=5$, $N_G(P)$ with $P\in\mathrm{Syl_2(G)}$ is what we desire. 
- Now assume $n_2=15$. 
	- If any $2$ Sylow $2$-subgroups intersect trivially, then there are $1+3\times 15=46$ elements of order $2^k$, contradicting with $n_5=6$. 
	- Thus there exist Sylow $2$-groups $P_1$ and $P_2$ such that $P_1\cap P_2=A$ with $|A|=2$. Then $C_G(A)\geqslant\left\langle P_1,P_2\right\rangle$ and so $C_G(A)\geqslant P_1$ and $|C_G(A)|>4$. It deduces that $|C_G(A)|\geqslant 12$. On the other hand, $[G:C_G(A)]\geqslant 4$ yields $|C_G(A)|\leqslant15$. Thus $|C_G(A)|=12$ and it is a subgroup of index $5$. 

Now we finish the proof.
<p align="left">□</p>


> [!proposition]
> Group of order $144$ is not simple.
{ #9a9397}


**_Proof._**
Assume that $G$ with $|G|=144$ is simple. For any $H\leqslant G$ and $[G:H]=m$, there is $G\lesssim S_m$ and so $m\geqslant 6$. 

Note that $n_2\in\{1,3,9\}$ and $n_3\in\{1,4,16\}$. As $n_p=[G:N_G(P)]$, we have $n_2=9$ and $n_3=16$. 
- If any $2$ Sylow $3$-subgroups intersect trivially, then there are $8\times16+1=129$ elements of order $3^k$ and then $n_2=1$, which is impossible. 
- Hence there exist Sylow $3$-subgroups $P_1$ and $P_2$ such that $P_1\cap P_2=D$ and $|D|=3$. Then consider the group $H:=N_G(D)\geqslant\left\langle P_1,P_2\right\rangle$. Assume the number of Sylow $3$-subgroups of $H$ is $m_3$. Then $m_3\equiv 1\pmod 3$ and $m_3\geqslant 2$. It deduces that $m_3\geqslant 4$. Notice that $|H|=|N_H(P)|\cdot m_3\geqslant|P|\cdot m_3=9\times 4=36$ and so $[G:H]\leqslant 4$. It is a contradiction. 

Now we finish the proof.
<p align="left">□</p>


In [[MATH/Cards/Nodes/Sylow Theorems#^24a4c2\|#^24a4c2]] and [[MATH/Cards/Nodes/Sylow Theorems#^9a9397\|#^9a9397]], the key is to consider the intersection of two Sylow $p$-subgroups. Here is a more refined result, which is used to prove [[MATH/Cards/Nodes/Sylow Theorems#^f95b09\|#^f95b09]].

> [!theorem]
> Let $P_1,\cdots,P_n$ be all Sylow $p$-subgroups of $G$. If for any $i\neq j$ there is $|P_i:P_i\cap P_j|\geqslant p^d$, then $n\equiv 1\pmod{p^d}$.
{ #56a6de}


**_Proof._**
Let $\Omega=\{P_1,\cdots,P_n\}$ be the set of Sylow $p$-subgroups. Consider $P_n$ acts on $\{P_1,\cdots,P_{n-1}\}$ by conjugation. Note that $P_i^x\neq P_n$ for any $x\in P_n$, so the action is well-defined. Let $H_i=P_n{}_{P_i}$ be the point stabilizer of $P_i$, then $H\leqslant N_G(P_i)\cap P_n$. Since $N_G(P_i)$ has only one Sylow $p$-subgroup $P_i$, there is $N_G(P_i)\cap P_n\leqslant P_i$ and so $N_G(P_i)\cap P_n=P_i\cap P_n$. Hence, $|P_n:P_n\cap P_i|=o(P_i)\geqslant p^d$ equals to the length of the orbit containing $P_i$ and so each orbit length is $kp^d$ for some $k\in \mathbb{N}_+$. Therefore, $p^d\mid n-1$ and $n\equiv 1\pmod{p^d}$.
<p align="left">□</p>


> [!proposition]
> Group of order $432=2^4\cdot 3^3$ is not simple.
{ #f95b09}


**_Proof._**
Assume that $G$ is simple. Note that $n_3\in\{4,16\}$. If $n_3=4$, $G$ has a subgroup of index $4$ and $G\lesssim S_4$, which is impossible. Thus $n_3=16$. Since $n_3\not\equiv 1\pmod{3^2}$, there exist Sylow $3$-subgroups $P_i$ and $P_j$ such that $|P_i:P_i\cap P_j|=3$. Then $|P_i\cap P_j|=9$. 

By [[MATH/Cards/Nodes/Sylow Theorems#^qes1qo\|#^qes1qo]], $P_i\cap P_j$ is a maximal subgroup of $P_i$, so $N_{P_i}(P_i\cap P_j)=P_i$. It deduces that $N_G(P_i\cap P_j)\geqslant\left\langle P_i,P_j\right\rangle$. Since $N_G(P_i\cap P_j)$ has at least $4$ Sylow $3$-subgroups, we have $|N_G(P_i\cap P_j)|\geqslant 4\cdot N_{N_G(P_i\cap P_j)}(P_i)\geqslant 4\cdot 3^3=108$ and $[G:N_G(P_i\cap P_j)]\leqslant 4$. Then $G$ has a subgroup of index $\leqslant 4$ and $G\lesssim S_4$, which is impossible.
<p align="left">□</p>
