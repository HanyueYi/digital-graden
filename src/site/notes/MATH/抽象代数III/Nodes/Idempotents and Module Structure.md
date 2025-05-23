---
{"dg-publish":true,"draft":false,"permalink":"/MATH/抽象代数III/Nodes/Idempotents and Module Structure/","dgPassFrontmatter":true}
---


## Definitions and Basic Properties of Idempotents

> [!definition] 
> Let $R$ be a ring with identity. An *idempotent* in $R$ is a non-zero element $e$ with $e^2=e$. 

**Facts.**
- $eRe$ is a ring with identity $e$, where $eRe=\{eae:a\in R\}$. 
- For any $x\in Re$, $x=re$ for some $r\in R$ and then $xe=ree=re=x$. 

> [!definition]
> Two idempotents $e_1,e_2$ are called *orthogonal* if $e_1e_2=0=e_2e_1$. More generally, $n$ idempotents $e_1,\cdots,e_n$ are called pairwise orthogonal if $e_ie_j=0=e_je_i$ for any $i\neq j$.
> - An idempotent $e$ is called *primitive*, if it is not a sum of two orthogonal idempotents.
> - An *idempotent decomposition* of an idempotent $e$ is a representation $e=e_1+\cdots+e_n$, where $e_1,\cdots,e_n$ are pairwise orthogonal. If moreover $e_1,\cdots,e_n$ are primitive, then the decomposition is called a *primitive idempotent decomposition*. 

**Remarks.** 
- If $e_1,\cdots,e_n$ are orthogonal idempotents, then $e_1+\cdots+e_n$ is also an idempotent.
- For $e\in R$ with $e^2=e$, $1=e+(1-e)$ is a idempotent decomposition. 

## Modules Generated by Idempotents

> [!theorem]
> Let $e$ be an idempotent of $R$. If $e=e_1+\cdots+e_n$ is an idempotent decomposition, then $Re=Re_1\oplus\cdots\oplus Re_n$ as left ideals or left $R$-modules. 
> 
> Conversely, if $Re$ is a direct sum of left ideals of $R$, $Re=I_1\oplus\cdots\oplus I_n$, then there is an idempotent decomposition $e=e_1+\cdots+e_n$ with $e_i\in I_i$ and $I_i=Re_i$. 
> 
> In this way, the idempotent decompositions of $e$ are in bijection with the direct sum decompositions of the left ideals $Re$. 
{ #1dezlm}


**_Proof._**
Let $e=e_1+\cdots+e_n$ be an idempotent decomposition. Then $e_ie=e_i$ yields that $Re_i\subseteq Re$. For any $a\in R$, $ae=ae_1+\cdots+ae_n\in Re_1+\cdots+Re_n$. So $Re=Re_1+\cdots+Re_n$. For another expression $ae=a_1e_1+\cdots+a_n e_n$, note that $ae_i=aee_i=a_ie_i$. So the expression is unique. 

Conversely, let $Re=I_1\oplus\cdots\oplus I_n$. Since $e\in Re$, $e$ can be written as $e=e_1+\cdots+e_n$ with $e_i\in I_i$. For any $a_i\in I_i\subseteq Re$, note that

$$a_i=a_ie=a_ie_1+\cdots+a_ie_n$$

where $a_ie_i\in I_i$. Since $I_1\oplus\cdots\oplus I_n$ is a direct sum, the decomposition of $a_i$ is unique and so $a_ie_i=a_i$ and $a_ie_j=0$ for any $i\neq j$. Take $a_i=e_i$, then $e_i$ is idempotent and $e_ie_j=e_je_i=0$. Therefore, $e=e_1+\cdots+e_n$ is a idempotent decomposition.  
<p align="left">□</p>


> [!corollary]
> Let $e$ be an idem of $R$. TFAE:
> - $e$ is primitive;
> - ${}_R(Re)$ is indecomposable as a left $R$-module;
> - $e$ is the unique idempotent in $eRe$. 
{ #tv7l9r}


**_Proof._**
i)<->ii) is easy. 

i)->iii) Suppose $e'\in eRe$ such that $e'\neq 0$ and $e'^2=e'$. Then $e=e'+(e-e')$ is a decomposition, which contradicts with $e$ primitive. 

iii)->i) If $e=e_1+e_2$ is an imprimitive idempotent in $R$, then $e_1,e_2\in eRe$, because $ee_1e=e_1$ and $ee_2e=e_2$, which is impossible. 
<p align="left">□</p>


> [!theorem]
> Let $e,f$ be idempotents of $R$, and let $V$ be an $R$-module. 
> - $\mathrm{Hom}_R(Re,V)\simeq eV$. In particular, $\mathrm{Hom}_R(Re,Rf)\simeq fRe$ as abelian groups. 
> - $\mathrm{End}_R(Re)\simeq (eRe)^\mathrm{op}$ as rings. 
{ #yr2ffd}


**_Proof._**
i) Let $\varphi\in \mathrm{Hom}_R(Re,V)$, then $\varphi(e)=\varphi(ee)=e\varphi(e)\in eV$. Consider the map $g:\mathrm{Hom}_R(Re,V)\to eV$, $\varphi\mapsto\varphi(e)$. 

Note that 
- $\varphi(ae)=a\varphi(e)$ for any $a\in R$. So $\varphi$ is determined by $\varphi(e)$ and so $g$ is injective. 
- Take arbitrary $v\in eV$. For a $R$-homomorphism $\psi:Re\to V,xe\mapsto xev=xv$, $g(\psi)=v$. So $g$ is surjective. 

Therefore, $\mathrm{Hom}_R(Re,V)\simeq eV$. 

ii) Define $V=Re$. For $\sigma,\tau\in \mathrm{End}_R(Re)$, we have 

$$\sigma(\tau(e))=\sigma(\tau(e)e)=\tau(e)\sigma(e)$$

and so $\mathrm{End}_R(Re)\simeq (eRe)^\mathrm{op}$. 
<p align="left">□</p>


> [!theorem]
> Let $e,f$ be idempotent of $R$. TFAE:
> - $Re\simeq Rf$ as left $R$-modules.
> - $eR\simeq fR$ as right $R$-modules.
> - There exist $b\in fRe$ and $a\in eRf$ with $ab=e$, $ba=f$. 
{ #spaio1}


**_Proof._**
Here we only prove i) and iii) are equivalent. 

i)->iii) Let $\varphi:Re\to Rf$ be an $R$-isomorphism. Set $a=\varphi(e)$ and $b=\varphi^{-1}(f)$. Then we have 

$$a=\varphi(ee)=e\varphi(e)\in eRf,\text{ and }b\in fRe.$$

Note that

$$f=\varphi(\varphi^{-1}(f))=\varphi(b)=\varphi(be)=b\varphi (e)=ba$$

and we can similarly prove that 

$$e=\varphi^{-1}(\varphi(e))=\varphi^{-1}(af)=a\varphi^{-1}(f)=ab.$$

iii)->i) Assume that there exist $b\in fRe$ and $a\in eRf$ with $ab=e$ and $ba=f$. Since $a\in eRf$, there is $eaf=a$. Define $\varphi_a:Re\to Rf,xe\mapsto xa$ and $\varphi_b:Rf\to Re,xf\to xb$. Then we can check that $\varphi_a\circ\varphi_b=\mathrm{id}_{Re}$ and $\varphi_b\circ \varphi_a=\mathrm{id}_{Rf}$.
- For any $xe\in Re$, we have $(\varphi_b\circ \varphi_a)(xe)=xa=xaf=xab=xe$.
- For any $xf\in Rf$, we have $(\varphi_a\circ\varphi_b)(xf)=xb=xbe=xba=xf$. 

Now we finish the proof.
<p align="left">□</p>


## Lifting Idempotents Over Nilpotent Ideals

> [!definition]
> Let $I$ be a $2$-sided ideal of $R$, and let $f$ is an idempotent of $R$. If $e=f+I$ is an idempotent in $R/I$, we say $f$ lifts $e$. 
> 
> If there is an idempotent $f\in R$ lifting $e$ for every idempotent $e$ of $R/I$, then we say we can lift idempotents from $R/I$ to $R$. 


> [!theorem]
> If $I$ is a nilpotent ideal of $R$, then we can lift idempotents from $R/I$ to $R$. Moreover, if $e \in R/I$  is a primitive idempotent, then any idempotent lift $f\in R$ of $e$ is also primitive.
{ #84f4de}


**_Proof._**
Suppose $\bar{r}$ is idempotent in $R / I$. Consider its preimage $r \in R$ and define $s=1-r$. Note that $\overline s$ is also an idempotent in $R/I$.

We have that $r s=r-r^2 \in I$ and $r s=s r$. So there is some $k$ such that $r^k s^k=0$. Since 

$$\bar{r}^k+\bar{s}^k = \bar{r}+\bar{s} =\overline{1}\in R/I,$$

we have $x=1-r^k-s^k \in I$ is nilpotent and then $1-x=r^k+s^k$ is invertible in $R$, whose inverse is $u=1+x+x^2+\ldots+x^{l-1}$ with $x^l=0$. Notice that $\bar{u}= \overline{1}\in R/I$, and $u$ commutes with $r$ and $s$ (since $x$ does).

Finally, we have $u(r^k+s^k)=1$. It deduces that 

$$(ur^k)^2+u^2r^ks^k=ur^k,$$

where $u^2 r^k s^k=0$ by definition of $k$. Also note that $\overline {ur^k}=\overline {r^k}=\overline r$. Therefore, $ur^k$ is what we desire.


Suppose $e$ is primitive and $f$ has an idempotent decomposition $f=f_1+f_2$. Then $e=e_1+e_2$ with $e_i=\overline {f_i}$. Since $e$ is primitive, one of $e_1,e_2$ is $0$ and so WLOG $\overline {f_1}=0$ and so $f_1\in I$. It contradicts with $f_1$ idempotent. 
<p align="left">□</p>


> [!corollary]
> Let $I$ be a two-sided nilpotent ideal or $R$, and let $1=e_1+\cdots+e_n$ be an idempotent decomposition in $R/I$. Then there is an idempotent decomposition $1=f_1+\cdots+f_n$ in $R$ with $e_i=f_i+I$. If $e_i$ are primitive, so are $f_i$. 
{ #3rmbjt}


**_Proof._**
Induction on $n$. When $n=1$, it is trivial, and now we assume that it holds for $m<n$. 

Define $e_2+\cdots+e_n=E$, then $E$ is idempotent and $1=e_1+E$ in $R/I$. We lift $e_1$ to $f_1\in R$ and define $F=1-f_1$. Then $F$ is a lift of $E$. 

Note that $F$ is the identity of the ring $FRF$, and $FIF$ is a nilpotent ideal of $FRF$. Consider the composition homomorphism 

$$FRF\hookrightarrow R\twoheadrightarrow R/I,$$

whose kernel is $FRF\cap I$. There is $FRF\cap I=FIF$, because
- $FIF\subseteq FRF\cap I$ 
- for any $x\in FRF\cap I$, $FxF\subseteq FIF$. 

So we get an inclusion $FRF/FIF\hookrightarrow R/I$, and its image is $E(R/I)E$. As $E(R/I)E$ has identity $E=e_2+\cdots+e_n$, by induction hypothesis one have $F=f_2+\cdots+f_n$ with $f_i+I=e_i$ for $i\geqslant 2$. Thus $1=f_1+\cdots+f_n$ and we finish the proof.
<p align="left">□</p>


> [!corollary]
> Let $f$ be an idempotent in a ring $R$ that has a nilpotent ideal $I$. Then $f$ is primitive in $R$ iff $f+I$ is primitive in $R/I$. 
{ #lz95r0}


## Structure of Artinian Rings and their Modules

> [!lemma]
> Let $A$ be a semisimple Artinian ring. 
> - There is a primitive idempotent decomposition $1=e_1+\cdots+e_n$. This corresponds $A=Ae_1\oplus\cdots\oplus Ae_n$ where $Ae_i$ is simple. 
> - For every simple $A$-module $S$, there is a primitive idempotent $e$ with $S\simeq Ae$.
> - for any simple $A$-module $S$, there exists $1\leqslant i\leqslant n$, $e_iS\neq 0$. If $T$ is a simple $A$-module with $T\not\simeq S$, then $e_i T=0$. 
{ #drcz17}


 **_Proof._**
i) [[MATH/抽象代数III/Nodes/Idempotents and Module Structure#^1dezlm\|Recall]] that there is a bijection between the idempotent decomposition of $e$ are in bijection with the direct sum decomposition of the left ideals $Ae$. Since $A$ is semisimple and Artinian, there is a decomposition $1=e_1+\cdots+e_n$ and $A=\oplus_{i=1}^nAe_i$. By [[MATH/抽象代数III/Nodes/Idempotents and Module Structure#^tv7l9r\|#^tv7l9r]], $Ae_i$ is simple. 

ii) Since each simple $A$-module is a quotient of the left regular module ${}_A A$ by [[MATH/抽象代数III/Nodes/Annihilator and Jacobson Radical#^09efb3\|Annihilator and Jacobson Radical#^09efb3]], $S$ is isomorphic to $Ae$ for some primitive idempotent $e$. 

iii) Notice that $S=1S=(e_1+\cdots+e_n)S$, and there exists $i$ such that $e_iS\neq 0$. For any given simple $A$-module $T$, there exists $e$ such that $T\simeq Ae$. By [[MATH/抽象代数III/Nodes/Idempotents and Module Structure#^yr2ffd\|#^yr2ffd]], one have

$$e_iT=e_iAe\simeq \mathrm{Hom}_R(Ae,Ae_i)=0$$

if $Ae\not\simeq A e_i$. Now we finish the proof. 
<p align="left">□</p>


> [!theorem]
> Let $A$ be an Artinian ring, and let $S$ be a simple $A$-module. 
> - There is an indecomposable projective $A$-module $P_S$ with $P_S/\mathrm{Rad}(P_S)\simeq S$ of the form $P_S\simeq Af$ where $f$ is a primitive idempotent in $A$.
> - The idempotent $f$ has the property that $fS\neq 0$, and if $T$ is any simple module with $T\not\simeq S$ then $fT=0$. 
> - $P_S$ is the projective cover of $S$, it is uniquely determined up to isomorphism by $S$. 
{ #koarlo}


**_Proof._**
Let $e\in A/J(A)$ be any primitive idempotent element with $eS\neq \emptyset$. Let $f$ be any lift of $e$ to $A$, then $f$ is primitive. 

- [ ] Note that $fS=eS\neq 0$ and $fT=eT=0$ for any simple module $T\not\simeq S$. 

- [ ] Set $P_S=Af$, which is a indecomposable projective module.   

Notice that 

$$\begin{aligned}
Af &\to (A/J(A))(f+J(A))=S\\
af&\mapsto(a+J(A))(f+J(A))
\end{aligned}$$

is an $A$-morphism with kernel $J(A)Af=\mathrm{Rad}(Af)=\mathrm{Rad}(P_S)$. Then $P_S/\mathrm{Rad}P_S\simeq S$. 
<p align="left">□</p>



> [!theorem]
> Let $A$ be an Artinian ring. 
> 
> Up to isomorphism, the indecomposable projective $A$-modules are exactly the module $P_S$ that are the projective covers of simple modules, and $P_S\simeq P_T$ iff $S\simeq T$. 
> 
> Each $P_S$ appears as direct summand of ${}_A A$ (left regular module) with multiplicity equal to the multiplicity of $S$ as a summand of ${}_{A/J(A)}A/J(A)$. Precisely, ${}_A A\simeq \oplus_S(P_S)^{n_S}$, where $S$ runs through simple $A$-modules up to isomorphism, and $n_S=\dim_D S$ with $D=\mathrm{End}_A(S)$. 
{ #u11ppk}


**_Proof._**
Let $\bar{A}=A / J(A)$. Since $A$ is Artinian, $\overline A$ is an Artinian semisimple ring. Hence by [[MATH/抽象代数III/Nodes/Idempotents and Module Structure#^drcz17\|#^drcz17]], one have a primitive idempotent decomposition $1=e_1+\cdots+e_n$ in $\overline A$. By [[MATH/抽象代数III/Nodes/Idempotents and Module Structure#^3rmbjt\|#^3rmbjt]], lift each $e_i$ to an idempotent $f_i \in A$ and so $1=f_1+\cdots+f_n$ in $A$.

Thus, the regular module $A^A$ decomposes as

$${ }_A A=A f_1 \oplus \cdots \oplus A f_n,$$

where each $A f_i$ is an indecomposable projective module. By [[MATH/抽象代数III/Nodes/Idempotents and Module Structure#^koarlo\|#^koarlo]], we know

$$A f_i / \operatorname{Rad}\left(A f_i\right) \simeq A e_i$$

is a simple $\bar{A}$-module and hence a simple $A$-module. So each $A f_i$ is the projective cover $P_S$ of some simple module $S$, and every such cover arises this way.

Now let $P$ be any indecomposable projective $A$-module. Then

$$P / \operatorname{Rad}(P) \simeq S_1 \oplus \cdots \oplus S_t$$

where each $S_i$ is a simple module. On the other hand, $P_{S_1} \oplus \cdots \oplus P_{S_t} \rightarrow S_1 \oplus \cdots \oplus S_t$ is also a projective cover. By the uniqueness of projective covers, it follows that

$$P \simeq P_{S_1} \oplus \cdots \oplus P_{S_t}$$

Since $P$ is indecomposable, we must have $t=1$, and $P \simeq P_S$ for some simple module $S$. Therefore, every indecomposable projective is isomorphic to some $P_S$.

Finally, since $A / J(A)$ is semisimple, we have:

$$A / J(A) \simeq \bigoplus_S S^{n_s}$$

and ${}_A A \simeq \bigoplus_S\left(P_S\right)^{n_S}$, where $n_S=\operatorname{dim}_{\operatorname{End}_A(S) }S$ by [[MATH/抽象代数III/Nodes/Semisimple Artinian Rings and Algebras#^8omj6z\|Semisimple Artinian Rings and Algebras#^8omj6z]], as desired.
<p align="left">□</p>


> [!theorem]
> Let $A$ be an Artinian ring, and let $f$ be a primitive idempotent of $A$. Define $e=f+J(A)\in A/J(A)=\overline A$. 
> In any finitely generated $A$-module $V$, the multiplicity of $\overline A e$ in $V$ is equal to the composition length of $fV$ as an $fAf$-module. 
{ #3hxo3d}


**_Proof._**
Since $A$ is an Artinian ring and $V$ is a finitely generated $A$-module, we know $V$ has a finite length composition series by [[MATH/抽象代数III/Nodes/Socle and Radical Series#^u3of0p\|Socle and Radical Series#^u3of0p]]. Notice that $e$ is primitive by [[MATH/抽象代数III/Nodes/Idempotents and Module Structure#^lz95r0\|#^lz95r0]]. 

Let $V=V_0\supseteq V_1\supseteq\cdots\supseteq V_n=0$ be a composition series of $V$. Consider the chain of $fAf$-modules 

$$fV=fV_0\supseteq\cdots\supseteq fV_n=0,$$

where $V_i/V_{i+1}\simeq \overline A e$ iff $fV_i/fV_{i+1}\neq 0$. Furthermore, 

$$e\overline Ae\simeq f\left(V_i / V_{i+1}\right) \cong f V_i /\left(f V_i \cap V_{i+1}\right)=f V_i / f V_{i+1}.$$

By [[MATH/抽象代数III/Nodes/Idempotents and Module Structure#^yr2ffd\|#^yr2ffd]], $e\overline Ae\simeq (\mathrm{End}_{\overline A}(\overline A e))^\mathrm{op}$ is a division ring by [[MATH/Cards/Nodes/Schur Lemma\|Schur's lemma]]. Since $fAf/J(fAf)\simeq e\overline {A}e$, we know $e\overline A e$ is a simple $fAf$-module. Therefore, the multiplicity of $\overline A e$ in any finitely generated $A$-module $V$ is equal to the composition length of $fV$ as an $fAf$-module. 
<p align="left">□</p>


**Remark.** For a primitive idempotent $f\in A$ with Artinian ring $A$, $fAf$ is a local ring.  
- We claim that $J(fAf)=fJ(A)f$.
	- Since $J:=J(A)$ is an ideal of $A$, $fJf$ is an ideal of $fAf$. 
	- For any $x\in fJf$, there is $x=faf$ for some $a\in J$. Since $A$ is Artinian, $J$ is nilpotent and so $fJf$ is nilpotent. It deduces that $fJf\subseteq J(fAf)$. 
	- On the other hand, $fAf/fJf=f\overline Af$ is semisimple and so $fJf\supseteq J(fAf)$. 
- We claim that $fAf$ is local. 
	- By [[MATH/抽象代数III/Nodes/Idempotents and Module Structure#^yr2ffd\|#^yr2ffd]], $e\overline Ae\simeq (\mathrm{End}_{\overline A}(\overline A e))^\mathrm{op}$ is a division ring by [[MATH/Cards/Nodes/Schur Lemma\|Schur's lemma]].
	- Since $fAf/J(fAf)\simeq e\overline {A}e$, we know $J(fAf)$ is a maximal ideal and $fAf$ is local. 


## Cartan Matrix

Let $1=e_1+\cdots+e_n$ be a primitive idempotent decomposition in $A/J(A)$, and let $1=f_1+\cdots+f_n$ be a primitive idempotent decomposition in $A$ with $e_i=f_i+J(A)$. 

> [!definition]
> We denote by $c_{ij}$ the multiplicity of $(A/J(A))e_i$ in $Af_j$, which is called the Cartan variant in $A$. The $n\times n$ matrix $(c_{ij})_{n\times n}$ is called the *Cartan matrix* of $A$. 

> [!theorem]
> $c_{ij}\neq 0$ iff $f_iAf_j\neq 0$. 
{ #e4tl53}


**_Proof._**
It is a direct corollary of [[MATH/抽象代数III/Nodes/Idempotents and Module Structure#^3hxo3d\|#^3hxo3d]]. 
<p align="left">□</p>


For convenience, if $S$ and $T$ are two simple $A$-modules, we denote the corresponding Cartan invariant by $c_{ST}$, i.e., the multiplicity of $S$ in $P_T$. 

> [!proposition]
> Let $A$ be a finitely generated $k$-algebra over a field $k$, and let $S$ be a simple $A$-module with projective over $P_S$. Let $U$ be a finitely dimensional $A$-module. 
> - If $T$ is a simple $A$-module, then 
>   
>   $$\dim_k\mathrm{Hom}_A(P_S,T)=\begin{cases}\dim\mathrm{End} _A(S)&\text{if }S\simeq T,\\ 0 &\text{otherwise.}\end{cases}$$
>   
> - The multiplicity of $S$ in $U$ is $\dim\mathrm{Hom}_A(P_S,U)/\dim \mathrm{End}_A(S)$. 
> - If $e\in A$ is an idempotent, then $\dim\mathrm{Hom}(Ae,U)=\dim eU$.
> - Let $e_S$ and $e_T$ be idempotents so that $P_S=Ae_S$ and $P_T=Ae_T$ are projective covers of $S$ and $T$. Then 
>   
>   $$c_{ST}=\dim\mathrm{Hom}_A(P_S,P_T)/\dim\mathrm{End}_A(S)=\dim e_SAe_T/\dim \mathrm{End}_A(S).$$
>   
>   If moreover $k=\overline k$, then $c_{ST}=\dim\mathrm{Hom}_A(P_S,P_T)=\dim e_S Ae_T$. 
{ #qi7oer}


**_Proof._**
i) If $P_S\to T$ is nonzero, then the kernel must be a maximal submodule, containing $\mathrm{Rad}(P_S)$. But $P_S/\mathrm{Rad}(P_S)\simeq S$, so $S\simeq T$. Note that there is a commutative diagram

![Pasted image 20250408192218.png|160](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250408192218.png)

one have $\mathrm{Hom}_A(S,T)\simeq \mathrm{End}_A(S)$. 

ii) is trivial by i).

iii) is trivial by [[MATH/抽象代数III/Nodes/Idempotents and Module Structure#^yr2ffd\|#^yr2ffd]].

iv) is trivial by iii) and note that $\dim_k\mathrm{End}_A(S)=1$ by [[MATH/Cards/Nodes/Schur Lemma\|Schur's lemma]]. 
<p align="left">□</p>


# 从9节来的

Let $A$ be an $R$-algebra, which is finitely generated as an $R$-module. 

**Fact.** $A\times A\to A,(a,b)\mapsto ab$ is continuous. 

$A^*=A/\pi A$ is a finitely generated $F$-algebra. 

> [!theorem]
> Let $A$ be finitely generated $R$-algebra. Then 
> - $A\pi\subseteq J(A)$;
> - $J(A)^n\subseteq A\pi$ for some $n>0$. 
{ #nuyi3u}


**_Proof._**
i) Let $V$ be a simple $A$-module. Then either $\pi V=V$ or $\pi V=0$. Since $V=Av$ for any $0\neq v\in V$ and $A$ is finitely generated over $R$, we know $V$ is finitely generated over $R$. Thus if $\pi V=V$, then $V=0$ by [[MATH/交换代数/Nodes/2 Modules#^c2a5d0\|Nakayama lemma]]. So $\pi V=A\pi V=0$ and $A\pi\subseteq J(A)$. 

ii) Define $A^*=A/A\pi$. Then $J(A^*)=J(A)/A\pi$. Since $A^*$ is a finite-dimensional $F$-algebra, we have $A^*$ is Artinian and $J(A^*)$ is nilpotent. It deduces that $J(A)^n\subseteq A\pi$ for some $n>0$. 
<p align="left">□</p>


> [!theorem]
> Let $A$ be a finitely generated $R$-algebra. Let $I$ be an ideal of $A$ with $I\subseteq J(A)$ and $\overline A=A/I$. 
> - Let $\overline c$ be an idempotent in $\overline A$, and let $\overline c=\overline c_1+\cdots+\overline c_n$ be an idempotent decomposition in $\overline A$. Then $\overline c$ lifts to an idempotent $e$ of $A$ and there exists orthogonal idempotent $e_1,\cdots,e_n$ of $A$ satisfying $\overline e_i=\overline c_i$ and $e=e_1+\cdots+e_n$. 
> - An idempotent $e$ of $A$ is primitive iff $\overline e$ is primitive in $\overline A$.
> - Let $e,f$ be primitive idempotent of $A$, the. $Ae\simeq Af$ iff $\overline A\overline e\simeq \overline A\overline f$. 
{ #4kwh24}


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