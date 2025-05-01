---
{"dg-publish":true,"draft":false,"permalink":"/MATH/抽象代数III/Nodes/Annihilator and Jacobson Radical/","dgPassFrontmatter":true}
---


# Annihilator

> [!definition]
> Let $R$ be a ring, and let $M$ be a left $R$-module. For any $x\in M$, define 
> 
> $$\mathrm{Ann}_R(x)=\{r\in R:rx=0\}$$
> 
> as the *annihilator *of $x$ in $R$. Notice that $\mathrm{Ann}_R(x)$ is a left ideal of $R$. 
> 
> For a set $X\subseteq M$, define $\mathrm{Ann}_R(X)=\cap_{x\in X}\mathrm{Ann}_{R}x$. If $N$ is a $R$-submodule of $M$, then $\mathrm{Ann}_R(N)$ is a $2$-sided ideal of $R$.
 
> [!lemma]
> Let $R$ be a ring with identity $1$. Let $S$ be a left simple $R$-module. Then $S$ is a quotient of the left regular module ${}_RR$.
{ #09efb3}


**_Proof._**
Let $x\in S$ be an nonzero element of $S$. Consider cyclic module $0\neq Rx\subseteq S$, then $Rx=S$. Define 

$$\varphi:{}_R R\to S,r\mapsto rx$$

and note that $\varphi$ is an epimorphism. Hence $S\simeq R/\mathrm{Ann}_R(x)$ is a quotient of the left regular module ${}_R R$. 
<p align="left">□</p>


# Jacobson Radical

> [!definition]
> Let $R$ be a ring. The *Jacobson radical* $J(R)$ of $R$ is the intersection of all left maximal ideals of $R$. As a left $R$-module, $J(R)=\mathrm{Rad}({}_R R)$. 

## Intersection of Annihilators of Simples

> [!theorem]
> The following holds for the Jacobson radical of a ring $R$. 
> - $J(R)$ is the intersection of all the annihilator ideals of simple (left) $R$-modules. Consequently, $J(R)$ is a $2$-sided ideal of $R$. 
> - $a\in J(R)$ iff $1-xa$ has a left inverse for all $x\in R$, i.e., there exists $b\in R$ such that $b(1-xa)=1$. 
> - $J(R)$ is the largest one among the ideals of $I$ satisfying the following condition: if $a\in I$, then $1-a$ is a unit of $R$. 
> - $J(R)$ coincides with the intersection of all maximal right ideals of $R$.
{ #p95eh4}


**_Proof._**
i) Let $S$ be a simple $R$-module. As $S\simeq R/\mathrm{Ann}_R(x)$ for any $x\in S$ by [[MATH/抽象代数III/Nodes/Annihilator and Jacobson Radical#^09efb3\|#^09efb3]], $\mathrm{Ann}_R(x)$ is a maximal left ideal of $R$. It deduces that $J(R)\subseteq \mathrm{Ann}_R(x)$ and so $J(R)\subseteq \mathrm{Ann}_R(S)$. 

Conversely, we aim to show that, for any $x\in R$, if $x\in\mathrm{Ann}_R(S)$ for any simple $R$-module $S$, then $x$ is contained in any maximal left ideal. Let $I$ be a maximal left ideal. Then $R/I$ is a simple $R$-module. If $x\in \mathrm{Ann}_R(R/I)$, then $x\in I$. Now we finish the proof.

ii) "->" If $a\in J(R)$ and $1-xa$ has no left inverse for some $x\in R$, then $R(1-xa)\neq R$. Hence there is a maximal left-ideal $M$ of $R$ with $1-xa\in M$. Then $a\in M$ yields $1\in M$, which is a contradiction. 

"<-" If $a\notin J(R)$, then $a\notin M$ for some maximal left ideal $M$ of $R$. Then $Ra+M=R$ and $xa+b=1$ for some $x\in R$ and $b\in M$. So $1-xa\in M$ and $1-xa$ has no left inverse. 

iii) Let $a\in J(R)$. Then there exists $b$ such that $b(1-a)=1$ and then $b=1+ba$ has a left inverse, i.e. there exists $c$ such that $cb=1$. It deduces that $c=cb(1-a)=1-a$ and so $1-a$ is a unit. 

Let $I$ be a $2$-sided ideal with the property "$a\in I$ then $1-a$ is a unit of $R$". If $I\not\subseteq J(R)$, then there exists a maximal ideal $M$ such that $I\not\subseteq M$ and $I+M=R$. So $a'+b=1$ for some $a'\in I$ and $b\in M$. As $1-a'\in M$, $1-a'$ is not a unit, which is a contradiction.

iv) Suppose $K(R)$ is the intersection of all maximal right ideals of $R$, then by the argument of iii), we can prove that $K(R)$ is the largest one among the ideals of $I$ satisfying the following condition: if $a\in I$, then $1-a$ is a unit of $R$. Then by iii) $K(R)=J(R)$ and so we finish the proof.
<p align="left">□</p>

## Nilpotency of $J(A)$ in Artinian Rings

> [!definition]
> - An element $a\in R$ is called *nilpotent* if $a^n=0$ for some $n\in \mathbb{Z}_+$. If so, $(1-a)(1+a+\cdots+a^{n-1})=1$ and $1-a$ is a unit. 
> - An left ideal $I$ of $R$ is called a *nil left ideal* if every element of $I$ is nilpotent. 
> - $I$ is called *nilpotent* if $I^n=0$ for some $n$. Clearly, nilpotent ideals are [nil](https://en.wikipedia.org/wiki/Nil_ideal). 

> [!theorem]
> If $I$ is a nil left ideal, then $I\subseteq J(R)$.
{ #112eab}


**_Proof._**
Let $a\in I$. For any $x\in R$, $xa\in I$. Since $I$ is nil, $1-xa$ is a unit and so $a\in J(R)$. 
<p align="left">□</p>


> [!theorem]
> If $A$ is Artinian, then $J(A)$ is nilpotent.
{ #a43f1d}


**_Proof._**
Consider $J(A)\supseteq J(A)^2\supseteq\cdots$. There exists $n$ such that $J(A)^n=J(A)^{n+1}=\cdots$. Assume that $N=J(A)^n\neq 0$. 

Consider the set of left ideals $\{I:I\subseteq A,NI\neq 0\}$. It is a nonempty set since $N^2\neq 0$. Let $I_0$ be the minimal member of this set. There exists $a\in I_0$ such that $Na\neq 0$. Since $Na\subseteq I_0$ and $N(Na)=Na\neq 0$, by the minimality of $I_0$, we know $Na=I_0$. In particular, there exists $b\in N$ such that $ba=a$, i.e. $(1-b)a=0$. Recall that $b\in N\subseteq J(A)$, then $1-b$ is a unit, leading to a contradiction. 
<p align="left">□</p>

> [!corollary]
> Let $A$ be an Artinian ring, then $J(A)$ is the maximal nilpotent left ideal of $A$. 
{ #8uxtcw}


**_Proof._**
By [[MATH/抽象代数III/Nodes/Annihilator and Jacobson Radical#^112eab\|#^112eab]] and [[MATH/抽象代数III/Nodes/Annihilator and Jacobson Radical#^a43f1d\|#^a43f1d]].
<p align="left">□</p>


> [!corollary]
> Let $A$ be an Artinian ring. Then $J(A)$ is the unique left ideal $U$ of $A$ with the property that $U$ is nilpotnent and $A/U$ is semisimple.
{ #ds8ywb}


**_Proof._**
By [[MATH/抽象代数III/Nodes/Socle and Radical of Module#^r8oe32\|Socle and Radical of Module#^r8oe32]] and [[MATH/抽象代数III/Nodes/Annihilator and Jacobson Radical#^8uxtcw\|#^8uxtcw]].
<p align="left">□</p>


> [!theorem]
> Let $I$ be a $2$-sided ideal of $R$ with $I\subseteq J(R)$. Then $J(R/I)=J(R)/I$. 
{ #dh47bb}


**_Proof._**
By [[MATH/交换代数/Nodes/1 Rings and Ideals#^9eaa9e\|1 Rings and Ideals#^9eaa9e]].
<p align="left">□</p>


> [!theorem]
> Let $A$ be an Artinian. Then $A$ is semisimple iff $J(A)=0$. 
{ #t0akw2}


**_Proof._**
"<-" Assume that $\{M_\lambda,\lambda\in \Lambda\}$ are all maximal left ideals of $A$. We consider the set of left ideals that are expressed a finite intersection of some $M_\lambda$. By Artinian, this set has minimal element, say $L=M_{\lambda_1}\cap\cdots\cap M_{\lambda_r}$. If $L\neq 0$, then there exists $M_\lambda$ such that $M_\lambda\cap L\subsetneq L$, which contradicts to the minimality of $L$. So $L=0$, i.e. $J(A)=M_{\lambda_1}\cap\cdots\cap M_{\lambda_r}$. Define a map $A\to A/M_{\lambda_1}\oplus\cdots\oplus A/M_{\lambda_r}$ is a monomorphism and so ${}_AA$ is semisimple. (This part can also be proved by [[MATH/抽象代数III/Nodes/Socle and Radical of Module#^r8oe32\|Socle and Radical of Module#^r8oe32]].)

"->" Assume ${}_AA$ is semisimple, then $A=S_1\oplus\cdots\oplus S_r$ with $S_i$ simple. Since $J(A)\subseteq \mathrm{Ann}_R(S_i)$, $J(A)A=0$. It deduces that $J(A)=0$. 
<p align="left">□</p>

