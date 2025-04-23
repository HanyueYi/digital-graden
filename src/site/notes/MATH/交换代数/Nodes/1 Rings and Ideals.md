---
{"dg-publish":true,"permalink":"/MATH/交换代数/Nodes/1 Rings and Ideals/","dgPassFrontmatter":true}
---


> Highlights: nilradical, Jacobson radical, Zariski topology

**Convention.** 
- All rings are commutative with $1_A$.
- $A=\{0\}$ iff $1_A=0_A$.
- Ring homomorphism $f:A\to B$ always satisfies $f(1_A)=1_B$

> [!proposition]
> Let $\alpha\subseteq A$ be an ideal. Then there exists an bijection:
> 
> $$\{\beta\subseteq A:\beta\mbox{ is an ideal, }\alpha\subseteq\beta\}\longleftrightarrow\{\mbox{ideals of }A/\alpha\}.$$
{ #9eaa9e}


# Local

> [!definition]
> We say $A$ is a *local ring*, if it has a unique maximal ideal $m_A$. Furthermore, $A/m_A$ is called *residue field*.

**Example.**
- all fields
- $k[\![x]\!]$ with $k$ field. Recall that it has the unique maximal ideal $(x)$.
- $\mathbb{Z}_p = \varprojlim_{n \geqslant 1} \mathbb{Z}/p^n\mathbb{Z}$, where $m_A=(p)$ and $\mathbb{Z}_p/p\mathbb{Z}_p\simeq \mathbb{F}_p$.

> [!proposition]
> Let $A$ be a ring, and let $m\subseteq A$ be an ideal.
> - If $\forall x\in A\setminus m$ satisfies $x\in A^\times$, then $A$ is local and $m=m_A$.
> - Suppose $m$ is maximal and for all $x\in m$ there is $1+x\in A^\times$, then $A$ is local.   
{ #ysw57c}


**_Proof._**
i) For any ideal $I\subsetneq A$ and any $i\in I$, $i\not\in A^\times$. Hence $I\subseteq m$ and so $m$ is the unique maximal ideal. 

ii) Let $y\in A\setminus m$, then $m+(y)=A$ and so $1=m_0+ay$ for some $m_0\in M$. Then $ay\in A^\times$ and so for $y$. By i) we finish the proof.
□


> [!definition]
> We say a ring is *semi-local*, if it has a finite number of maximal ideals. 

**Example.**
- If $A_1,A_2$ are local, then $A_1\times A_2$ is semi-local, as it has only two maximal ideals.
- $\mathbb{C}[x]/(x-1)(x-2)$. By [[MATH/交换代数/Nodes/1 Rings and Ideals#^9eaa9e\|#^9eaa9e]], there is a bijection between ideals of $\mathbb{C}[x]/(x-1)(x-2)$ and ideals of $\mathbb{C}[x]$ containing $(x-1)(x-2)$. Hence, all maximal ideals of $\mathbb{C}[x]/(x-1)(x-2)$ are $(x-1)$ and $(x-2)$. 

# Nilradical

> [!proposition]
> Let $\mathcal N=\{x\in A:x\mbox{ is nilpotent}\}$. Then $\mathcal N$ is an ideal and $A/\mathcal N$ has no nontrivial nilpotent element. We say $\mathcal N$ is the *nilradical*, denoted by $\mathrm{Nil}(A)$.

**_Proof._**
It is easy to verify $\mathcal N$ is an ideal: for any $a,b\in\mathcal N$, we have $a+b,ab,ra\in\mathcal N$ for any $r\in A$. 

Let $\overline x\in A/\mathcal N$. If $\overline x$ is nilpotent, then $\overline x^n=0$ and so $x^n\in\mathcal N$. Then $(x^n)^m=0$ and $x\in\mathcal N$. It deduces that $\overline x=0$.
□


> [!proposition]
> For any ring $A$, there is
> 
> $$\mathcal N(A)=\cap_{\mathcal{P}\subseteq A\mbox{ is a prime ideal}} \mathcal P.$$
{ #bgejpl}


**_Proof._**
Let $\cap_{\mathcal{P}\subseteq A\mbox{ is prime}} \mathcal P:=\mathbb P$. For any $x\in\mathcal N$ and any prime ideal $\mathcal P$, we have $x^n=0\in \mathcal P$ and so $x\in\mathcal P$. Hence $\mathcal N(A)\subseteq \mathbb P$.

On the other hand, if $f\in \mathbb P$ and $f^n\neq 0$ for any $n$, define 

$$\Sigma=\{\alpha\subseteq A:\alpha\mbox{ is an ideal and }f^n\not\in\alpha,\forall n\geqslant 1\}.$$

Notice that $\Sigma\neq\emptyset$ as $(0)\in\Sigma$. By Zorn's lemma, there exists a maximal element $\beta\in \Sigma$. 

We claim that $\beta$ is a prime ideal. Otherwise, there exist $x,y\notin \beta$ such that $xy\in\beta$. Since $\beta+(x)$ and $\beta+(y)$ are not contained in $\Sigma$, there are $t$ and $s$ such that $f^t\in \beta+(x)$ and $f^s\in \beta+(y)$. It deduces that $f^{t+s}\in (\beta+(x))(\beta+(y))\subseteq \beta$, which is a contradiction. Hence $\beta$ is a prime ideal and $f\notin\beta$. It contradicts with $f\in \mathbb P$.
□


# Jacobson Radical

> [!definition]
> Define the *Jacobson radical* as the intersection of all maximal ideals. Remark that $\mathrm{Jac}(A)\supseteq \mathrm{Nil}(A)$.

**Example.**
- $\mathrm{Jac}(\mathbb{Z})=(0)=\mathrm{Nil}(\mathbb{Z})$
- $\mathrm{Jac}(k[\![x]\!])=(x)$ and $\mathrm{Nil}(k[\![x]\!])=(0)$

> [!proposition]
> Let $\mathcal R=\mathrm{Jac}(A)$. Then $x\in R$ iff $1-xy\in A^\times$ for all $y\in A$.
{ #h2e8bp}


**_Proof._**
"->" If $1-xy\notin A^\times$, then there exists a maximal ideal $m$ such that $1-xy\in m$. Since $x\in m$, we have $1\in m$, which is impossible.

"<-" If $x\notin R$, then there is a maximal ideal $m$ such that $x\not\in m$. Then $m+(x)=A$ and so $1=m_0+xy_0$ for some $m_0\in m$ and $y_0\in A$. It deduces that $1-xy_0\in m$ and so $1-xy^0\notin A^\times$, contradiction.
□

# Some Propositions

Recall that if $\alpha$ and $\beta$ are coprime, i.e., $\alpha+\beta=A$, then $\alpha\beta=\alpha\cap \beta$, where $\alpha\beta=\{\sum_{i=1}^na_ib_j:a_i\in\alpha,b_i\in\beta\}$. We have the following theorem, which is similar to the Chinese remainder theorem.

> [!proposition]
> Let $\alpha_1,\cdots,\alpha_n$ be ideals. Consider $\phi:A\to\prod_{i=1}^n(A/\alpha_i)$.
> - If $\alpha_i,\alpha_j$ are pairwise coprime, then $\prod{\alpha_i}=\cap \alpha_i$.
> - $\phi$ is surjective if $\alpha_i,\alpha_j$ are pairwise coprime.
> - $\phi$ is injective if $\cap\alpha_i=(0)$.

**_Proof._**
i) is a generalization of the above "recall" part. 

ii) By the Chinese remainder theorem, if $\alpha_i,\alpha_j$ are coprime, then $A/(\cap_{i=1}^n \alpha_i)\simeq \prod_{i=1}^n (A/\alpha_i)$ and so $\phi$ can be identified as a quotient map. 

iii) By ii).
□


> [!proposition]
> - Let $p_1,\cdots,p_n$ be prime ideals, and let $\alpha$ be an ideal with $\alpha\subseteq\cup_{i=1}^n p_i$. Then $\alpha\subseteq p_i$ for some $i$.
> - Let $\alpha_1,\cdots,\alpha_n$ be ideals, and let $p$ be a prime ideal such that $p\supseteq \cap_{i=1}^n \alpha_i$. Then $p\supseteq \alpha_i$ for some $i$. Furthermore, if $p=\cap \alpha_i$, then $p=\alpha_i$ for some $i$.
{ #tepoo1}


**Remark.** We cannot change $n$ to $\infty$. Here are two counterexamples.
- $A=\mathbb{C}[x_1,\cdots,x_n,\cdots]$. Let $p_i=(x_1\cdots x_i)$, then $\alpha=(x_1\cdots x_n\cdots)\subseteq \cup_{i=1}^\infty p_i$ is not contained in $p_i$ for all $i$.
- $A=\mathbb{Z}$. Let $\alpha_i=(p_i)$, then $\cap \alpha_i=(0)$ and $(0)\not\supseteq \alpha_i$ for all $i$. 

**_Proof._**
i) Consider the contrapositive statement. If $\alpha\not\subseteq p_i$ for all $i$, then $\alpha\not\subseteq\cup_{i=1}^n p_i$. We prove it by induction. The case of $n=1$ is trivial. Suppose it is true for $n-1$. By induction hypothesis, we have $\alpha\not\subseteq \cup_{j\neq i }p_j$ for each $1\leqslant i\leqslant n$. Take $x_i\in \alpha$ such that $x_i\not\in p_j$ for all $j\neq i$. If for some $i$ there is $x_i\notin p_i$, then $x_i\not\in \cup_{i=1}^n p_i$ and we have done. Otherwise $x_i\in p_i$ for all $i$. Define $y:=\sum_{i=1}^n x_1\cdots \hat x_i\cdots x_n$, then $y\in\alpha$ and $y\notin \cup_{i=1}^n p_i$. 

ii) If not, we have $p\not\supseteq \alpha_i$ for all $i$. Then there exists $x_i\in\alpha_i$ such that $x_i\not\in p$. Consider $y\in x_1\cdots x_n$, then $y\in\cap_{i=1}^n\alpha_i$ and so $y\in p$, which is a contradiction.
□

# Ideal Quotient

> [!definition]
> Let $\alpha, \beta\subseteq A$ be ideals. Define their *ideal quotient* as 
> 
> $$(\alpha:\beta)=\{x\in A:x\beta\subseteq\alpha\}.$$
> 
> This is an ideal of $A$. 
> 
> In particular, if $\alpha=(0)$, then $(0:\beta)$ is called the *annihilator* of $\beta$, denoted by $\mathrm{Ann}(\beta)$.

**Example.** Let $A=\mathbb{Z}$. Then $((m):(n))=(m/(m,n))$.

# Radical

> [!definition]
> Let $\alpha\subseteq A$ be an ideal. Define the *radical* of $\alpha$ as
> 
> $$r(\alpha)=\{x\in A:x^n\in\alpha\mbox{ for some }n\}.$$
> 
> Indeed, consider $\phi:A\to A/\alpha$, then $r(\alpha)=\phi^{-1}(\mathrm{Nil}(A/\alpha))$.

**Text-Exercise.** Let $P$ be a prime ideal, then $r(P^n)=P$ for all $n\geqslant 1$. 

**_Proof._**
It is easy to show $P\subseteq r(P^n)$. For any $y\in r(P^n)$, there exists $m$ such that $y^m\in P^n\subseteq P$ and so $y\in P$. Hence, $r(P^n)\subseteq P$. 

□


> [!proposition]
> For any ideal $\alpha\subseteq A$, there is
> 
> $$r(\alpha)=\cap_{\alpha\subseteq P,P\mbox{ is prime}}P.$$
{ #8da6f1}


**_Proof._**
Note that 

$$r(\alpha)/\alpha=\mathrm{Nil}(A/\alpha)=\cap _{\alpha\subseteq P,P\mbox{ is prime}}(P/\alpha)=(\cap _{\alpha\subseteq P}P)/\alpha$$

by [[MATH/交换代数/Nodes/1 Rings and Ideals#^bgejpl\|#^bgejpl]]. Now we finish the proof.
□


> [!proposition]
> If $r(\alpha),r(\beta)$ are coprime, then $\alpha,\beta$ are coprime.

**_Proof._**
It is easy to verify that $r(\alpha+\beta)=r(r(\alpha)+r(\beta))$, and it deduces that $r(\alpha+\beta)=r(r(\alpha)+r(\beta))=r(A)=A$.
□


# Extension and Contraction

> [!definition] 
> Define a ring homomorphism $f:A\to B$. For an ideal $\alpha\subseteq A$, $f(\alpha)$ is not necessarily an ideal. Define the *extension ideal* as 
> 
> $$\alpha^e=\left\langle f(\alpha)\right\rangle\subseteq B.$$
> 
> For ideal $\beta\subseteq B$, define the *contraction ideal* as 
> 
> $$\beta^c=f^{-1}(\beta)\subseteq A.$$

**Important Fact.** Let $f:A\to B$ be a ring homomorphism, and let $\beta\subseteq B$ be a prime ideal. Then $\beta^c=f^{-1}(\beta)\subseteq A$ is prime. (Proof: $f$ induces a map $A/f^{-1}(\beta)\to B/\beta$, which is injective. Note that $\beta$ is prime $\iff$ $B/\beta$ is integral domain $\implies$ $A/f^{-1}(\beta)$ is integral domain $\iff$ $f^{-1}(\beta)$ is prime.)

**Example.** If $\alpha$ is prime, then $\alpha^e$ is not necessary prime. Define $f:\mathbb{Z}\to \mathbb{Z}[i]$. Note that $(2)\subseteq \mathbb{Z}$ is prime, but $2\mathbb{Z}[i]$ containing $(1+i)(1-i)$ is not prime.


# Spectrum and Zariski Topology

> [!proposition] Text-Ex. 1.15
> Let $A$ be a ring. Define $X:=\{P:P\mbox{ is a prime ideal of }A\}$. For a subset $E\subseteq A$, let $V(E)=\{P:P\in X,P\supseteq E\}$. Then
> - If $\alpha=\left\langle E\right\rangle$, then $V(E)=V(\alpha)=V(r(\alpha))$.
> - $V(0)=X$, $V(1)=\emptyset$.
> - Let $E_i\subseteq A$ with $i\in I$ be a system of subsets. Then $\cap_{i\in I}V(E_i)=V(\cup_{i\in I}E)$.
> - $V(\alpha)\cup V(\beta)=V(\alpha\beta)=V(\alpha\cap \beta)$ for any ideals $\alpha,\beta$.
{ #vf0aa5}


**_Proof._**
i) Note that $E\subseteq \alpha\subseteq r(\alpha)$, and then $V(E)=V(\alpha)\supseteq V(r(\alpha))$. For any $q\supseteq\alpha$, note that $r(\alpha)=\cap_{P\supseteq \alpha}P$ by [[MATH/交换代数/Nodes/1 Rings and Ideals#^8da6f1\|#^8da6f1]] and so $q\supseteq r(\alpha)$. Hence $q\in V(r(\alpha))$ and then $V(\alpha)=V(r(\alpha))$. Now we finish the proof.

ii) and iii) are trivial.

iv) Since $\alpha\supseteq\alpha\cap\beta\supseteq \alpha\beta$, there is $V(\alpha)\subseteq V(\alpha\cap\beta)\subseteq V(\alpha\beta)$ and $V(\beta)\subseteq V(\alpha\cap\beta)\subseteq V(\alpha\beta)$. It remains to show $V(\alpha)\cup V(\beta)\supseteq V(\alpha\beta)$. For $P\in X$ with $P\supseteq\alpha\beta$, we have $P\supseteq\alpha$ or $P\supseteq\beta$ (otherwise, there exist $x\in \alpha\setminus P$ and $y\in\beta\setminus P$, which is impossible as $xy\in P$). 
□


**Remark.** Notice that $X=\{P:P\mbox{ is a prime ideal of }A\}$ is a topological space, using $\mathcal S:=\{V(E):E\subseteq A\}$ as the set of closed subsets of $X$. Denote $X$ by $\mathrm{Spec}A$, call the topology the *Zariski topology*.


> [!proposition] Text-Ex. 1.16
> Draw picture for $\mathrm{Spec}A$.
> - $\mathrm{Spec}(\mathbb{Z})=\{(0),(p):p\mbox{ is a prime}\}$. 
> 	- The set of closed subsets is $\mathcal S=\{V(E):E\subseteq \mathbb{Z}\}=\{V((n)):n\in \mathbb{Z}\}\cup\emptyset\cup \mathrm{Spec}(\mathbb{Z})$, where $V((n))=\{(p_1),\cdots,(p_k)\}$ with $n=\prod_{i=1}^k p_i^{n_i}$.
> 	- The set of open subsets is $\mathcal T=\mathrm{Spec}(\mathbb{Z})\cup \emptyset\cup \{\mathrm{Spec}(\mathbb{Z})\setminus \{(p_1),\cdots,(p_k)\}\}$. 
> 	- The closure of $(0)$ is $\mathrm{Spec}(\mathbb{Z})$, and so $(0)$ is called "fat point". 
> - $\mathrm{Spec}(\mathbb{R})=\{(0)\}$.
> - $\mathrm{Spec}(\mathbb{C}[x])=\{(0),(x-a)_{a\in \mathbb{C}}\}$. 
> 	- This is called the $1$-dimensional affine space over $\mathbb{C}$.  
> 	- Any non-empty open subset is dense.
> - $\mathrm{Spec}(\mathbb{R}[x])=\{(0),(x-\alpha)_{\alpha\in \mathbb{R}},(x-z)(x-\overline z)_{z\in \mathbb{C}\setminus \mathbb{R}}\}$.
> - $\mathrm{Spec}(\mathbb{Z}[x])=\{(0),(p),(f(x)),(p,g(x)):p\mbox{ is prime}, f\mbox{ is irreducible},\overline g\in \mathbb{F}_p[x]\mbox{ is irreducible}\}$.

**Remark.** 
- $\mathrm{Spec}(\mathbb{C}[x])$ can be seen as a plane + a fat point, and $\mathrm{Spec}(\mathbb{R}[x])$ can be seen as a upper half plane + a fat point.
- The Red Book of Varieties and Schemes, page 75, gives us a picture of $\mathbb{Z}[x]$. 

![Pasted image 20250219201048.png|500](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250219201048.png)

> [!definition]
>  Let $X$ be a set. A basis for a topology on $X$ is a collection $\mathcal{B}$ of subsets of $X$ (called the basis element) such that
>  - for any $x\in X$, there exists $B_x\in \mathcal{B}$ such that $x\in B_x$;
>  - if $x\in B_1\cap B_2$ where $B_1,B_2\in\mathcal{B}$, then there exists some $B_3\in\mathcal{B}$ such that $x\in B_3\subseteq B_1\cap B_2$.

> [!lemma]
> If $\mathcal B$ is a basis for a topology, then $\mathcal T:=\{\cup_{i\in I}B_i:B_i\in B\}$. 

> [!proposition] Text-Ex. 1.17
> Let $A$ be a ring and let $X=\mathrm{Spec}(A)$. For $f\in A$, define $X_f=\mathrm{Spec}(A)\setminus V(f)$. Then $\{X_f:f\in A\}$ forms a basis of Zariski topology. Also:
> - $X_f\cap X_g=X_{fg}$;
> - $X_f=\emptyset$ iff $f$ is nilpotent;
> - $X_f=X$ iff $f\in A^\times$;
> - $X_f=X_g$ iff $r((f))=r((g))$;
> - $X$ is quasi-compact, i.e., any open covering has a finite subcover;
> - each $X_f$ is quasi-compact;
> - an open subset of $X$ is quasi-compact iff it is a finite union of some $X_f$.

**_Proof._**
i) By [[MATH/交换代数/Nodes/1 Rings and Ideals#^vf0aa5\|#^vf0aa5]] $V(fg)=V(f)\cup V(g)$. It deduces that $X_f\cap X_g=X_{fg}$. 

ii) $X_f=\emptyset$ iff $V(f)=X$ iff $f\in\cap_{P\mbox{ is prime ideal}} P=\mathrm{Nil}(A)$ iff $f$ is nilpotent.

iii) $X_f=X$ iff $V(f)=\emptyset$ iff $f$ is not contained in any prime ideals. If $f$ is not contained in any prime ideals, then it is not contained in any maximal ideals as [maximal ideal is prime](https://math.stackexchange.com/a/68493/1445401). So it can not contained in any non-trivial ideals and $\left\langle f\right\rangle=A$. On the other hand, if $f\in A^\times$, $\left\langle f\right\rangle=A$ and so $X_f=X$. 

iv) If $r((f))=r((g))$, then $V(f)=V(r(f))=V(r(g))=V(g)$ and $X_f=X_g$. If $V(f)=V(g)$, then $r((f))=r((g))$ by [[MATH/交换代数/Nodes/1 Rings and Ideals#^8da6f1\|#^8da6f1]]. 

v) Suppose $\{X_{f_i}:i\in I\}$ is an open cover of $X$, then $\cup_{i\in I}X_{f_i}=X_{({\{f_i:i\in I\}})}=X$ and so $\{f_i:i\in I\}$ generate $A$. Therefore, there is a finite subset $J$ such that $1=\sum_{j\in J}g_jf_j$ with $g_j\in A$. Now $\{f_j:j\in J\}$ generates $A$ and so $\{X_{_{f_j}}:j\in J\}$ is a finite subcover of $X$. 

vi) Suppose $\{X_{g_i}:i\in I\}$ is an open cover of $X_f$, then 

$$\cup_{i\in I}(X_f\cap X_{g_i})=\cup_{i\in I}X_{fg_i}=X_{\{fg_i:i\in I\}}=X_f$$

and so $V(\{fg_i:i\in I\})=V((f))$. It deduces that $r(\left\langle\{fg_i:i\in I\}\right\rangle)=r((f))$. Since $f\in r((f))$, there exists $n\in \mathbb{N}_+$ and a finite set $J\subseteq I$ such that $\sum_{j\in J}fg_j=f^n$. Thus, $f^n$ can be generated by $\{fg_i:i\in J\}$ and $X_{f^n}=\cup_{j\in J} X_{fg_j}$. 
For any $x\in r((f))$, $x^n\in r((f^n))$ and so $x\in r((f^n))$. Also, for any $x\in r((f^n))$, $x^m=af^n=(af^{n-1})f\in (f)$ yields $x\in r((f))$. Hence $r((f))=r((f^n))$ and then

$$X_{f}=X_{f^n}=\cup_{j\in J}X_{fg_j}\subseteq\cup_{j\in J}X_{g_j}.$$

Therefore, $\{X_{g_j}:j\in J\}\subseteq \{X_{g_i}:i\in I\}$ is an open subcover of $X_f$ and so $X_f$ is quasi-compact.

vii) If an open set is a finite union of some $X_f$, then it is quasi-compact by vi). Otherwise, if an open set $O$ is quasi-compact, then there exists an open cover $\{X_{f_i}:i\in I\}$. Since $\{X_f:f\in A\}$ forms a basis of Zariski topology, we can take $I$ such that $\cup_{i\in I}X_{f_i}=O$. As it has a finite subcover, there is finite $J\subseteq I$ with $O=\cup_{j\in J}X_{f_j}$ and so $O$ is a finite union of some $X_f$. 
□


> [!proposition] Text-Ex. 1.19
> $\mathrm{Spec}A$ is [[MATH/代数几何/Nodes/1.5 Definition of Prevarieties and Morphisms#^pcfcsm\|irreducible]] iff $\mathrm{Nil}(A)$ is a prime ideal. 
{ #gz1sp0}


**_Proof._**
Note that $\mathrm{Spec}A$ is irreducible iff $X_f\cap X_g=X_{fg}\neq\emptyset$ for any $X_f,X_g\neq \emptyset$ iff for any non-nilpotent $f,g$, $fg$ is also not nilpotent iff $\mathrm{Nil}(A)$ is a prime ideal. 
□

