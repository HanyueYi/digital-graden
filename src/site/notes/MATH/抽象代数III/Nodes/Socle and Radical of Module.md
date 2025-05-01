---
{"dg-publish":true,"draft":false,"permalink":"/MATH/抽象代数III/Nodes/Socle and Radical of Module/","dgPassFrontmatter":true}
---


# Socle

> [!definition]
> The unique largest semisimple submodule of $U$ is called the socle of $U$, denote $\mathrm{soc}(U)$. 


# Radical of Modules

> [!definition]
> A *maximal submodule* $N$ of $M$ is a proper submodule $N$ satisfying $N\subseteq U\subseteq M$ $\implies$ $U=N$ or $U=M$. Equivalently, $M/N$ is simple.
> 
> Define $\mathrm{Rad}(M)=\cap_{N}\{\mbox{maximal submodules }N\subseteq M\}$. If $M$ does not have maximal submodules, then define $\mathrm{Rad}(M)=M$. 

> [!lemma]
> Let $W$ be a proper $R$-submodule of ${}_RV$. If $V/W$ is finitely generated over $R$, then there exists a maximal $R$-submodule of $V$ containing $W$. In particular, if $V$ is finitely generated, then there exists a maximal submodule of $V$ containing $W$.
{ #fbacdf}


**_Proof._**
Let $\overline V=V/W=\sum_{i=1}^n R\overline v_i$ with $v_i\in V$. Let $\mathcal O$ be the set of proper $R$-submodule of $V$ containing $W$. It is a poset with inclusion. 

Claim that an arbitrary totally ordered subset $\{W_\lambda:\lambda\in\Lambda\}$ in $\mathcal O$, it has a upper bound. Let $U=\cup_{\lambda\in\Lambda}W_\lambda$. If $U=V$, then for each $i$, there exists $W_{\lambda_i}$ such that $v_i\in W_{\lambda_i}$. Let $W_\alpha$ be the largest among $\{W_{\lambda_i}:i=1,\cdots,n\}$. Then $W_\alpha=V$, which is a contradiction. 

So $U\neq V$, and $U\in\mathcal O$ is a upper bound for $W_\lambda$. By Zorn's lemma, we finish the proof.
<p align="left">□</p>


> [!corollary]
> For every proper left ideal $I$ of $R$, there exists a maximal left ideal of $R$ containing $I$. 

> [!lemma]
> Let $M,N$ be finitely generated $R$-modules, and let $f:M\to N$ be $R$-morphism. 
> - $f(\mathrm{Rad}(M))\subseteq\mathrm{Rad}(N)$. 
> - If $f$ is an epimorphism with $\ker f\subseteq\mathrm{Rad}(M)$, then $\mathrm{Rad}(N)=f(\mathrm{Rad}(M))$. 

**_Proof._**
i) Let $x \in \operatorname{Rad}(M)$. We show $f(x) \in \operatorname{Rad}(N)$. Suppose $K \subseteq N$ is a maximal submodule. Consider the composite map:

$$g: M \xrightarrow{f} N \xrightarrow{\pi} N / K$$

where $\pi$ is the quotient map. Since $N / K$ is simple, $\operatorname{ker}(g)$ is either $M$ or a maximal submodule of $M$.
- If $\operatorname{ker}(g)=M$, then $g(x)=0 \Longrightarrow \pi(f(x))=0 \Longrightarrow f(x) \in K$.
- If $\operatorname{ker}(g)$ is maximal, then $x \in \operatorname{Rad}(M) \subseteq \operatorname{ker}(g)$ (as $\operatorname{Rad}(M)$ is the intersection of all maximal submodules). Hence $g(x)=0 \Longrightarrow f(x) \in K$.

In either case, $f(x) \in K$. Since $K$ was arbitrary, $f(x) \in \operatorname{Rad}(N)$. Thus, $f(\operatorname{Rad}(M)) \subseteq \operatorname{Rad}(N)$.

ii) It suffices to show $\mathrm{Rad}(N)\subseteq f(\mathrm{Rad}(M))$. 

Let $K=\operatorname{ker} f \subseteq \operatorname{Rad}(M)$. By the isomorphism theorem, $N \cong M / K$. For any quotient module $M / K$, we have

$$\operatorname{Rad}(M / K)=(\operatorname{Rad}(M)+K) / K$$

Since $K \subseteq \operatorname{Rad}(M)$, one have $\operatorname{Rad}(M / K)=\operatorname{Rad}(M) / K$. Under the isomorphism $M / K \cong N$, it deduces that $\operatorname{Rad}(N)=f(\operatorname{Rad}(M))$.
<p align="left">□</p>


> [!lemma]
> Let $U$ be an $R$-module.
> - Suppose that $M_1,\cdots,M_n$ are maximal submodules of $U$. Then there is a subset $I\subseteq\{1,\cdots,n\}$ such that 
>   
>   $$U/(M_1\cap\cdots\cap M_n)\simeq \oplus_{i\in I}U/M_i$$
>  
> - Suppose that $U$ is Artinian, then $U/\mathrm{Rad}U$ is a semisimple and $\mathrm{Rad}U$ is the unique smallest submodule of $U$ wite semisimple quotient.
{ #r8oe32}


**_Proof._**
i) Let $I$ be the maximal subset of $\{1,\cdots,n\}$ with the property that the quotient homomorphism $\varphi_i:U/\cap_{i\in I}M_i\to U/M_i$ induce an isomorphism $U/\cap_{i\in I}M_i\to \oplus_{i\in I}U/M_i,u+\cap_{i\in I}M_i\mapsto (\varphi_i(u+\cap_{i\in I}M_i))_{i\in I}$. Note that $I$ exists, because $\{1\}$ is a subset such that the property holds.

We will show $\cap_{i\in I}M_i=M_1\cap\cdots\cap M_n$. If not, there exists $j$ such that $\cap_{i\in I}M_i\not\subseteq M_j$. Consider the homomorphism 

$$f:U\to(\oplus_{i\in I}U/M_i)\oplus (U/M_j),u\mapsto ((u+M_i)_{i\in I},u+M_j),$$

and $f$ has kernel $M_j\cap(\cap_{i\in I}M_i)$. It suffices to show $f$ is surjective, because this implies the larger set $I\cup\{j\}$ has the same property as $I$. Let 

$$g:U\to (U/\cap_{i\in I}M_i)\oplus (U/M_j).$$

Observe that $M_j+(\cap_{i\in I}M_i)=U$. If $x\in U$, then $x=y+z$ with $y\in\cap_{i\in I}M_i$ and $z\in M_j$ such that $g(y)=(0,x+M_j)$ and $g(z)=(x+\cap_{i\in I}M_j,0)$. So $g$ is surjective and $f$ is surjective. 

ii) Since $U$ is Artinian, $\mathrm{Rad}U$ is the intersection of finitely many maximal submodules. So $U/\mathrm{Rad}U$ is semisimple by i). 

If $V$ is a submodule of $U$ with semisimple $U/V$, then $U/V$ is Artinian and $U/V\simeq S_1\oplus\cdots\oplus S_n$ where $S_i$ is simple. Let $M_i$ be the kernel of the composition $U\to U/V\to S_i$, then $M_i$ is maximal and $\cap_{i=1}^n M_i\subseteq V$. Also $V\subseteq M_i$ as $V$ is the kernel of $U\to U/V\to S_i$ for all $i$. It deduces that $M_1\cap\cdots\cap M_n=V$ and so $\mathrm{Rad}U\subseteq V$. 
<p align="left">□</p>

## Radical and Essential

> [!theorem] Nakayama's lemma
> Let $U$ be Noetherian(or finitely generated). Then $U\to U/\mathrm{Rad}U$ is [[MATH/抽象代数III/Nodes/Projective Cover#^ktprge\|essential]]. Equivalently, if $V$ is a submodule of $U$ with $V+\mathrm{Rad}U=U$, then $V=U$.
{ #3f1b99}


**_Proof._**
If $V\neq U$, there exists maximal $W\supseteq U$ by [[MATH/抽象代数III/Nodes/Socle and Radical of Module#^fbacdf\|#^fbacdf]] and $V+\mathrm{Rad}U\subseteq W\neq U$, contradiction.
<p align="left">□</p>


> [!proposition]
> - Suppose that $f:U\to V$ and $g:V\to W$ are $R$-morphisms of $R$-modules. If two of $f,g,gf$ are essential, then so is the third.
> - Let $f:U\to V$ be a homomorphism of Noetherian modules. Then $f$ is an essential epimorphism iff the radical quotient $U/\mathrm{Rad}U\to V/\mathrm{Rad}V$ is an essential epimorphism. In fact, if it holds, then the radical quotient is an isomorphism. 
> - Let $f_i:U_i\to V_i$ be homomorphisms of Noetherian modules for $i=1,\cdots,n$, then $f_i$ are all essential epimorphisms iff $\oplus f_i:\oplus U_i\to \oplus V_i$ is an essential epimorphism. 
{ #q7sonb}


**_Proof._**
i) Suppose $f$ and $g$ are essential, then $gf$ is surjective. If $U_0\subseteq U$ is a proper submodule, then $f(U_0)\subsetneq V$ and $gf(U_0)\subsetneq W$. Hence $gf$ is surjective.

Suppose $f$ and $gf$ are essential, then $g$ is surjective. Let $V_0\subsetneq V$. If $g(V_0)=W$, then $f^{-1}(V_0)\neq U$ satisfying $gf(f^{-1}(V_0))=W$ and $gf$ is not essential, which is impossible. So $g$ is essential. 

Suppose $g$ and $gf$ are essential. If $f$ is not surjective, then $f(U)\subsetneq V$ and $gf(U)=g(f(U))=W$. It contradicts with $g$ essential and so $f$ is surjective. If $f$ is not essential, then there exists $U_0\subsetneq U$ such that $f(U_0)=V$. It deduces that $gf(U_0)=g(V)=W$, leading to a contradiction. Thus, $f$ is essential. 

ii) Consider the commutative diagram 

![Pasted image 20250318202330.png|240](/img/user/%E9%99%84%E4%BB%B6/Pasted%20image%2020250318202330.png)

By [[MATH/抽象代数III/Nodes/Socle and Radical of Module#^3f1b99\|#^3f1b99]], $\downarrow$ 's are essential. So $f$ is essential iff $\overline f$ is essential.

Furthermore, we claim that if $\overline f:U/\mathrm{Rad} U\to V/\mathrm{Rad} V$ is an essential epimorphism, then $\overline f$ is an isomorphism. To show it, it suffices to show $\overline f$ is injective. Otherwise, if $\ker\overline f\neq \{0\}$, then semisimple $U/\mathrm{Rad}U$ can be written as $U/\mathrm{Rad} U=\ker \overline f\oplus K'$. Then $\overline f(K')=V/\mathrm{Rad} V$ contradicts with $\overline f$ essential. Therefore, $\overline f$ is an isomorphism.  

iii) It suffices to consider $\oplus U_i/\mathrm{Rad}(\oplus U_i)\to \oplus V_i/\mathrm{Rad}(\oplus V_i)$. Note that $\oplus(U_i/\mathrm{Rad} U_i)\simeq \oplus U_i/\mathrm{Rad}(\oplus U_i)$ and $\oplus(V_i/\mathrm{Rad} V_i)\simeq \oplus V_i/\mathrm{Rad}(\oplus V_i)$, then we have done.
<p align="left">□</p>

> [!corollary]
> If $P$ and $Q$ are projective Noetherian modules over a ring, then $P\simeq Q$ iff $P/\mathrm{Rad}P\simeq Q/\mathrm{Rad} Q$. 

**_Proof._**
By [[MATH/抽象代数III/Nodes/Socle and Radical of Module#^3f1b99\|#^3f1b99]], $P\to P/\mathrm{Rad} P$ and $Q\to Q/\mathrm{Rad} Q$ are essential. Thus $P$ (rep. $Q$) is a projective cover of $P/\mathrm{Rad} P$ (rep. $Q/\mathrm{Rad} Q$). By [[MATH/抽象代数III/Nodes/Projective Cover#^9so7ao\|Projective Cover#^9so7ao]], projective cover is unique up to isomorphism and so we finish the proof. 
<p align="left">□</p>

