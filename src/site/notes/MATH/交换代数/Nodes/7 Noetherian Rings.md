---
{"dg-publish":true,"draft":false,"permalink":"/MATH/交换代数/Nodes/7 Noetherian Rings/","dgPassFrontmatter":true}
---


> Highlight: Hilbert basis theorem, Hilbert Nullstellensatz

> [!proposition]
> If $A$ is Noetherian, then $A/\alpha$ is also Noetherian.

**_Proof._**
By [[MATH/交换代数/Nodes/6 Chain Condition#^7j4294\|6 Chain Condition#^7j4294]].
<p align="left">□</p>


> [!proposition]
> Let $A\subseteq B$ be a subring, where $A$ is Noetherian and $B$ is a finitely generated $A$-module. Then $B$ is a Noetherian ring. 

**_Proof._**
By [[MATH/交换代数/Nodes/6 Chain Condition#^8ezl57\|6 Chain Condition#^8ezl57]], $B$ is a Noetherian $A$-module. For any $B$-submodule $N$ of $B$, it is also a $A$-submodule and so is finitely generated over $A$. Then $N$ is finitely generated over $B$. Thus $B$ is a Noetherian $B$-module.
<p align="left">□</p>


> [!proposition]
> For a Noetherian ring $A$ and a multiplicatively closed set $S$, $S^{-1}A$ is Noetherian. 

**_Proof._**
By [[MATH/交换代数/Nodes/3 Rings and Modules of Fractions#^961e0a\|3 Rings and Modules of Fractions#^961e0a]], ideals in $S^{-1}A$ are of form $S^{-1}I$ with $I\subseteq A$ ideal. But $I$ is finitely generated $A$-module. Then $S^{-1}I=S^{-1}A\otimes _A I$ is a finitely generated $S^{-1}A$-module.
<p align="left">□</p>


> [!corollary]
> If $A$ is Noetherian, then $A_p$ is Noetherian. 

**Remark.** There exists a ring $A$ such that $A_p$ is Noetherian, but $A$ is not Noetherian. Indeed, let $A=(\prod_{n=1}^\infty \mathbb{F})$ with $\mathbb{F}=\mathbb{Z}/2\mathbb{Z}$, which is non-Noetherian, because $\mathbb{F}\times 0\times 0\cdots\subseteq \mathbb{F}\times \mathbb{F}\times 0\times\cdots\subseteq\cdots$ does not terminate. A prime ideal $p=\mathbb{F}\times \mathbb{F}\times \cdots\times\{0\}\times \mathbb{F}\times \cdots$ and $A_p=\mathbb{F}$ is Noetherian. See [here](https://math.stackexchange.com/a/73442/1445401). 

![Pasted image 20250414203157.png|500](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250414203157.png)




> [!theorem] Hilbert basis theorem
> Let $A$ be a Noetherian ring. Then $A[x]$ is also a Noetherian ring.
{ #b4d5c1}


**_Proof._**
Let $\alpha\subseteq A[x]$ be an ideal. Let $I=\{\text{leading coefficients of }f(x)\in \alpha\}$. Note that $I$ is an ideal of $A$, and then $I$ is finitely generated, that is, $I=(a_1,\cdots,a_n)A$. For each $i$, let $f_i=a_ix^{r_i}+\text{lower terms}\in \alpha$. Let $r=\max\{r_i\}_{i=1}^n$. Then we get a sub-ideal $\alpha'=(f_1,\cdots,f_n)A[x]\subseteq \alpha$. 

Let $f\in \alpha$ with $f=ax^m+\text{lower terms}$ and $a\in I$. If $m\geqslant r$, then one can do division using $f_1,\cdots,f_n$, namely, if $a=\sum_{i=1}^n u_ia_i$ with $u_i\in A$, then one can construct 

$$f-\sum_{i=1}^n u_i f_ix^{m-r_i}\in \alpha$$

and its degree $<\deg f$. Repeat this procedure, and we get $f=g+h$ where $g\in \alpha'$ and $\deg h<r$. 

Let $M=\oplus_{i=1}^{r-1}Ax^i\subseteq A[x]$ be a $A$-submodule. By the decomposition $f=g+h$, we have $\alpha=\alpha'+\alpha\cap M$ as $A$-modules. 

But now, $M$ is a Noetherian $A$-module and $\alpha \cap M$ is also Noetherian $A$-module. So $\alpha\cap M=(g_1,\cdots,g_m)_A$. It is easy to see $\alpha=(f_1,\cdots,f_n,g_1,\cdots,g_m)_{A[x]}$ and so $\alpha$ is finitely generated. 
<p align="left">□</p>

**Remark.** We have proved it [[MATH/抽象代数II/Nodes/2.3 Noetherian Rings and Modules#^75xtmd\|here]]. Similarly, we can prove that if $A$ is Noetherian, then $A[\![x]\!]$ is also Noetherian. The proof is similar, using "lowest term coefficient". See [[MATH/交换代数/Nodes/HW6#^elab7i\|here]]. 


> [!corollary]
> If $A$ is Noetherian, then $A[x_1,\cdots,x_n]$ is also Noetherian. 

> [!corollary]
> Let $B$ be a finitely generated $A$-algebra. If $A$ is Noetherian, then so is $B$. In particular, every finitely generated ring, and every finitely generated algebra over a field, is Noetherian.

**_Proof._**
There exists surjective map $A[x_1,\cdots,x_n]\twoheadrightarrow B$. 

Or see [[MATH/抽象代数II/Nodes/2.3 Noetherian Rings and Modules#^gmjk45\|2.3 Noetherian Rings and Modules#^gmjk45]]. 
<p align="left">□</p>


> [!proposition]
> Let $A \subseteq B \subseteq C$ be rings. Suppose that $A$ is Noetherian, that $C$ is finitely generated as an A-algebra and that $C$ is finitely generated as a B-module. Then $B$ is finitely generated as an A-algebra.
{ #983c2e}


**Example & Counterexample.**
- $k\subseteq k[x^n]\subseteq k[x]$.
- $k\subseteq B\subseteq k[x]$, where $B=k[x^2+x^3,x^4+x^6,\cdots]$. Since $B$ is not finitely generated $A$-algebra, $C$ is not finitely generated as a $B$-module. 

**_Proof._**
Write $C=A[x_1,\cdots,x_m]$ with $x_i\in C$, and write $C=\left\langle y_1,\cdots,y_n\right\rangle_B$ as $B$-module with $y_i\in C$. Then 

$$\begin{aligned}
&x_i=\sum_{j=1}^n b_{ij}y_j,\; b_{ij}\in B\;\;\;(1)\\
&y_iy_j=\sum_{k=1}^n b_{ijk}y_k, \; b_{ijk}\in B\;\;\;(2)
\end{aligned}$$

Let $B_0=A[b_{ij},b_{ijk}]\subseteq B$ be a subring, which is a finitely generated $A$-algebra. So now, it suffices to show $B$ is a finitely generated $B_0$-algebra. But in fact, one can show that $B$ is a finitely generated $B_0$-module. 

Indeed, for any $b\in B\subseteq C=A[x_1,\cdots,x_m]$, $B$ is a polynomial in $x_1,\cdots,x_m$ over $A$ and so $b$ is a polynomial in $y_1,\cdots,y_n$ over $B$ by (1). Furthermore, $b$ is a linear combination of $y_1,\cdots,y_n$ over $B_0$ by (2). Remark that $y_j\in C$ NOT in $B$, so they are not a set of generator of $B$ over $B_0$. But the above argument shows $B\subseteq \left\langle y_1,\cdots,y_n\right\rangle_{B_0}\subseteq C$. 

Since $A$ is a Noetherian ring, by [[MATH/交换代数/Nodes/7 Noetherian Rings#^b4d5c1\|#^b4d5c1]], $B_0=A[b_{ij},b_{ijk}]$ is also Noetherian ring. Then it yields that $\left\langle y_1,\cdots,y_n\right\rangle_{B_0}\supseteq B$ is a Noetherian $B_0$-module. So $B$ is a Noetherian $B_0$-module, proving the claim. 
<p align="left">□</p>


> [!proposition]
> Let $k$ be a field, and let $E$ be a finitely generated $k$-algebra. If $E$ is also a field, then $E/k$ is a finite extension.
{ #f58c35}


**_Proof._**
Write $E=k[x_1,\cdots,x_n]$ where $x_i\in E$. Since $E$ is also a field, $E=k(x_1,\cdots,x_n)$. If $E/k$ is not a finite extension, then not all $x_i$ are algebraic over $k$. We can reorder $x_i$ such that $x_1,\cdots,x_r$ are algebraic independent over $k$, and $x_{r+1},\cdots,x_n$ are algebraic over $k(x_1,\cdots,x_r):=F$. So we get $k\subseteq F\subseteq E$ where $E$ is a finitely generated $k$-algebra and $E$ is finitely generated $F$-module. By [[MATH/交换代数/Nodes/7 Noetherian Rings#^983c2e\|#^983c2e]], $F$ is a finitely generated $k$-algebra.

We claim that it is impossible. That is, it is impossible to write $k(x_1,\cdots,x_r)=k[y_1,\cdots,y_m]$. Indeed, write $y_j=f_j(x_1,\cdots,x_r)/g_j(x_1,\cdots,x_r)$ where $f_j,g_j\in k[x_1,\cdots,x_r]$, then $1/(g_1\cdots g_m+1)\notin\text{RHS}$. 
<p align="left">□</p>


> [!corollary]
> Let $k$ be a field, and let $A$ be a finitely generated $k$-algebra. If $m\subseteq A$ is a maximal ideal, then $A/m$ is a finitely extension of $k$.
{ #0346fb}


**_Proof._**
Let $E=A/m$ in [[MATH/交换代数/Nodes/7 Noetherian Rings#^f58c35\|#^f58c35]]. 
<p align="left">□</p>


> [!corollary] Hilbert Nullstellensatz, weak form
> Let $k$ be a algebraic closed field. If $m\subseteq k[x_1,\cdots,x_n]$ is a maximal ideal, then $m=(x_1-a_1,\cdots,x_n-a_n)$ with $a_i\in k$.
{ #8sohrm}


**Remark.** "null"=zero, "stellen"=point, "satz"=theorem

**_Proof._**
It has been proved in [[MATH/代数几何/Nodes/1.1 Some Algebra#^6rh0cw\|1.1 Some Algebra#^6rh0cw]]. 

By [[MATH/交换代数/Nodes/7 Noetherian Rings#^0346fb\|#^0346fb]], $k[x_1,\cdots,x_n]/m$ is a finite extension over $k$. Since $\overline k=k$, one have $k[x_1,\cdots,x_n]/m\stackrel{\theta}{\simeq} k$. Write $\theta(x_i)=a_i\in k$. Then $(x_1-a_1,\cdots,x_n-a_n)\subseteq m$. But LHS is maximal, which yields that $(x_1-a_1,\cdots,x_n-a_n)=m$.
<p align="left">□</p>


> [!corollary] Equivalent form of [[MATH/交换代数/Nodes/7 Noetherian Rings#^8sohrm\|#^8sohrm]]
> Let $k$ be a algebraic closed field. Let $I=(f_1,\cdots,f_m)\subsetneq k[x_1,\cdots,x_n]$ be a proper ideal. Then these $f_i$ have a common solution in $k^n$. 

**_Proof._**
Since $I$ is proper, $I\subseteq m$ for some maximal ideal $m$. By [[MATH/交换代数/Nodes/7 Noetherian Rings#^8sohrm\|#^8sohrm]], $I\subseteq (x_1-a_1,\cdots,x_n-a_n)$ and so $(a_1,\cdots,a_n)$ is a common solution for any $f\in I$. 
<p align="left">□</p>


**Remark.** For an ideal $I\subseteq k[x_1,\cdots,x_n]$, solution of $I$ is empty iff $I=k[x_1,\cdots,x_n]$. 


> [!theorem] Text-Ex. 7.14.
> It is a strong form of Hilbert Nullstellensatz. 
> 
> Let $\alpha\subsetneq k[x_1,\cdots,x_n]$ be an ideal. Define $V=\{(a_1,\cdots,a_n)\in k^n:f(a_1,\cdots,a_n)=0,\forall f\in \alpha\}$ as the solution set of $\alpha$. Define $I(V)=\{g\in k[x_1,\cdots,x_n]:g(a_1,\cdots,a_n)=0,\forall (a_1,\cdots,a_n)\in \alpha\}$. Then $I(V)=r(\alpha)$. 

**_Proof._**
See [[MATH/交换代数/Nodes/HW6#^oex7wh\|here]]. 
<p align="left">□</p>


# Primary Decomposition

> [!definition]
> Say an ideal $\alpha$ is irreducible, if for any $\alpha=\beta\cap \gamma$, then $\alpha=\beta$ or $\alpha=\gamma$. Say $\alpha$ is reducible, if $\alpha$ can be written as $\alpha=\beta\cap \gamma$ with $\beta,\gamma\supsetneq \alpha$. 


> [!lemma]
> Let $A$ be a Noetherian ring. Then any ideal is a finite intersection of irreducible ideals, that is, for any ideal $\alpha$, $\alpha$ can be written as $\alpha=\cap_{i=1}^n\beta_i$.
{ #98d425}


**_Proof._**
Let $S=\{\alpha\subseteq A:\alpha\text{ is not a finite intersection of irreducible ideals}\}$. If $S\neq \emptyset$, then by $A$ Noetherian $S$ has a maximal element $\alpha$. Since $\alpha$ is reducible, $\alpha$ can be written as $\alpha=\beta\cap \gamma$ and both $\beta,\gamma$ are finite intersection of irreducible ideals, leading to contradiction. 
<p align="left">□</p>


> [!lemma]
> For a Noetherian ring $A$, an irreducible ideal is primary.
{ #3e8c56}


**_Proof._**
Note that $\alpha\subseteq A$ is irreducible iff $\overline 0\subseteq A/\alpha$ is irreducible, and $\alpha\subseteq A$ is primary iff $\overline 0\subseteq A/\alpha$ is primary. So WLOG just consider the case where $0\subseteq A$ is an irreducible ideal. We aim to show $0$ irreducible yields $0$ primary. Suppose $xy=0$ and $y\neq 0$, it is enough to show $x^n=0$ for some $n$. Consider the chain 

$$\mathrm{Ann} (x)\subseteq \mathrm{Ann} (x^2)\subseteq\cdots.$$

As $A$ Noetherian, there exists $n$ such that $\mathrm{Ann}(x^n)=\mathrm{Ann}(x^{n+1})=\cdots$. 

We claim that $(x^n)\cap (y)=(0)$. For any $a\in (x^n)\cap (y)$, we have $ax=0$ by $xy=0$ and $a=x^nb$ for some $b\in A$. It deduces that $bx^{n+1}=0$ and $b\in \mathrm{Ann}(x^{n+1})=\mathrm{Ann}(x^n)$ and so $a=x^nb=0$. Now we prove the claim. 

Since $(0)$ is irreducible and $(y)\neq 0$, we have $(x^n)=(0)$ and so we finish the proof.
<p align="left">□</p>


> [!theorem]
> A Noetherian proper ideals have primary decomposition. 
{ #k8wbyb}


**_Proof._**
By [[MATH/交换代数/Nodes/7 Noetherian Rings#^98d425\|#^98d425]] and [[MATH/交换代数/Nodes/7 Noetherian Rings#^3e8c56\|#^3e8c56]]. 
<p align="left">□</p>


> [!proposition]
> Let $A$ be a Noetherian ring, and let $\alpha$ be an ideal of $A$. Then $\alpha\supseteq (r(\alpha))^n$ for some $n$.
{ #384015}


**_Proof._**
Suppose $r(\alpha)$ is finitely generated by $x_1,\cdots,x_k$ with $x_i^n\in \alpha$ for big enough $n$. Then $\alpha\supseteq (r(\alpha))^{nk+1}$ and we have done. 
<p align="left">□</p>


> [!corollary]
> For a Noetherian ring $A$, then there exists $n$ such that $(\mathrm{Nil}(A))^n=0$. 

**_Proof._**
Take $\alpha=(0)$ in [[MATH/交换代数/Nodes/7 Noetherian Rings#^384015\|#^384015]]. 
<p align="left">□</p>


> [!corollary]
> Let $A$ be a Noetherian ring, and let $m\subseteq A$ be a maximal ideal. For an ideal $q\subseteq A$, TFAE:
> - $q$ is $m$-primary
> - $r(q)=m$
> - $m^n\subseteq q\subseteq m$ for some $n$

**_Proof._**
i)->ii) by definition. 

- [ ] ii)->i) by 4 ? 这个证明没看懂

ii)->iii) by [[MATH/交换代数/Nodes/7 Noetherian Rings#^384015\|#^384015]]

iii)->ii) obvious.
<p align="left">□</p>

